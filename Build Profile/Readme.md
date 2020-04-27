# Build Profiles:
## Introduction to Build Profiles:
+  Profiles are specified using a subset of the elements available in the POM itself (plus one extra section), and are triggered in any of a variety of ways.
+  They modify the POM at build time, and are meant to be used in complementary sets to give equivalent-but-different parameters for a set of target environments (providing, for example, the path of the appserver root in the development, testing, and production environments).
+  As such, profiles can easily lead to differing build results from different members of your team. However, used properly, profiles can be used while still preserving project portability. 

## What are the different types of profile? 
**Per Project**
 ```python
 Defined in the POM itself (pom.xml).
 ```

**Per User**
```python
Defined in the Maven-settings (%USER_HOME%/.m2/settings.xml).
```

**Global**
```python
Defined in the global Maven-settings (${maven.home}/conf/settings.xml).
```

## How can a profile be triggered? How does this vary according to the type of profile being used?

A profile can be triggered/activated in several ways:
+ Explicitly
+ Through Maven settings
+ Based on environment variables
+ OS settings
+ Present or missing files

### Before starting with to know different ways on how to trigger your profiles first you have to make a build of your project.
you can see this to know how to make a build using cmd in just simple 5-6 steps!.

[How to make a build ?](/cmd/readme.md)

### For example we are making two profiles profile1 and profile2 there work will be to print something and copy file1 to another folders, and then our goal would be to "test"  like mvn test.

> **NOTE:** complete pom.xml with what to print and how to copy file is given above in pom.xml

## TYPE-1

 Basic syntax to add in your pom.xml
 by doing this you need to call your profile i.e which profile you to be active
 
 
 ```python
  <profile>
         <id>profile1</id>
         <build>
            <plugins>
               <plugin>
                  <groupId>org.apache.maven.plugins</groupId>
                  <artifactId>maven-antrun-plugin</artifactId>
                  <version>1.1</version>
                  <executions>
                     <execution>
                        <phase>test</phase>
                        <goals>
                           <goal>run</goal>
                        </goals>
                        <configuration>
                           <tasks>
                              <echo>this is profile 1</echo>
                              <copy file="src/main/file1.txt"
                                 tofile="src/test/file2.txt"/>
                           </tasks>
                        </configuration>
                     </execution>
                  </executions>
               </plugin>
            </plugins>
         </build>
      </profile>
      
      
       <id>profile2</id>
         <build>
            <plugins>
               <plugin>
                  <groupId>org.apache.maven.plugins</groupId>
                  <artifactId>maven-antrun-plugin</artifactId>
                  <version>1.1</version>
                  <executions>
                     <execution>
                        <phase>test</phase>
                        <goals>
                           <goal>run</goal>
                        </goals>
                        <configuration>
                           <tasks>
                             <echo>this is profile 2</echo>
                              <copy file="src/main/file1.txt"
                                 tofile="src/test/file3.txt"/>
                           </tasks>
                        </configuration>
                     </execution>
                  </executions>
               </plugin>
            </plugins>
         </build>
      </profile>
      
 ```
Commands to run for this type of activation

```python
mvn test -P profile1
```
![alt txt](https://github.com/sumyak/Apache-Maven/blob/master/Build%20Profile/IMAGES/2%20(2).png?raw=true)

```python
mvn test -P profile1,profile2
```

![alt txt](https://github.com/sumyak/Apache-Maven/blob/master/Build%20Profile/IMAGES/4%20(2).png?raw=true)

![alt txt](https://github.com/sumyak/Apache-Maven/blob/master/Build%20Profile/IMAGES/5%20(2).png?raw=true)

## TYPE-2

 Basic syntax to add in your pom.xml 
 this type will make your profiles active by default
 
 ```python
 <profiles>
  <profile>
    <id>profile-1</id>
    <activation>
      <activeByDefault>true</activeByDefault>
    </activation>
    ...
  </profile>
  
  
  
  <profile>
    <id>profile-1</id>
    <activation>
      <activeByDefault>true</activeByDefault>
    </activation>
    ...
  </profile>
</profiles>
 ```
 **OR**
 
```python
 <activeProfiles>
    <activeProfile>profile1</activeProfile>
  </activeProfiles>
  
  <activeProfiles>
    <activeProfile>profile2</activeProfile>
  </activeProfiles>
 ```
 
 Commands to run for this type of activation

```python
mvn test 
```
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/Build%20Profile/IMAGES/5%20(2).png?raw=true)


 




