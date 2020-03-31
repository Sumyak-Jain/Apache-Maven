# Maven using command Prompt
##  Follow this to Create a simple Maven Project using CLI in just simple! 6 steps from beginning
**STEP 1**. Download Maven and follow the installation instructions
You can use this link to download, install and set path for maven.

**link** https://www.javatpoint.com/how-to-install-maven

**STEP 2**. After doing step 1 Type the following in a terminal or in a command prompt: 
```shell
mvn --version 
```
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/Screenshot%20(111).png?raw=true)

**STEP 3**. You will need somewhere for your project to reside, create a directory somewhere and start a shell in that directory then On your command line, execute the following Maven goal to start creating a maven project
```shell
mvn archetype:generate
```
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/1%20(2).png?raw=true)

**3.1** After that do the following on cmd itself
```shell
Choose org.apache.maven.archetypes:maven-archetype-quickstart version:
1: 1.0-alpha-1
2: 1.0-alpha-2
3: 1.0-alpha-3
4: 1.0-alpha-4
5: 1.0
6: 1.1
7: 1.3
8: 1.4
Choose a number: 8: 8
Define value for property 'groupId': com.mycompany.app
Define value for property 'artifactId': my_app
Define value for property 'version' 1.0-SNAPSHOT: : 1
Define value for property 'package' com.mycompany.app: : com.mycompany.my_app
Confirm properties configuration:
groupId: com.mycompany.app
artifactId: my_app
version: 1
package: com.mycompany.my_app
 Y: : Y
 ```
 ![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/2%20(2).png?raw=true)
 
 After this check the directory on your system which you provided before to reside this project a folder named my_app
 will be made with the following inside it:
 * src
 * pom
 
 *What you just did?* 
 
You executed the Maven goal archetype:generate, and passed in various parameters to that goal. The prefix archetype is the plugin that provides the goal. If you are familiar with Ant, you may conceive of this as similar to a task. This archetype:generate goal created a simple project based upon a maven-archetype-quickstart archetype.

**STEP 4**. Now its time to BUILD your project  BUT!! first you have to enter into the directory where your project resides so type the following command:
```shell
cd my_app
mvn package
```
after this check your directory there will be a .jar file of your project.

![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/3%20(2).png?raw=true)
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/4%20(2).png?raw=true)

**STEP 5**. You may test the newly compiled and packaged JAR with the following command
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/5%20(2).png?raw=true)

**STEP 6**. Genrating the site , type the following command:
```
mvn site
```
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/6%20(2).png?raw=true)
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/7%20(2).png?raw=true)

after this check your directory for this and click on any HTML file in site folder to check the documentation.

![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/8%20(2).png?raw=true)

![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/9%20(2).png?raw=true)


### Maven Phases Although hardly a comprehensive list, these are the most common default lifecycle phases executed. 
*  **validate:** validate the project is correct and all necessary information is available
*  **compile:** compile the source code of the project 
*  **test:** test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
*  **package:** take the compiled code and package it in its distributable format, such as a JAR.
*  **integration-test:** process and deploy the package if necessary into an environment where integration tests can be run 
*  **verify:** run any checks to verify the package is valid and meets quality criteria
*  **install:** install the package into the local repository, for use as a dependency in other projects locally
*  **deploy:** done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects. 

you can practice the above on cmd using
```
mvn <phase> { Ex: mvn install }
```


 






