# Maven using command Prompt
##  Follow this to Create a simple Maven Project using CLI
1. Download Maven and follow the installation instructions
You can use this link to download, install and set path for maven.

**link** https://www.javatpoint.com/how-to-install-maven

2. Type the following in a terminal or in a command prompt: 
```shell
mvn --version 
```
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/Screenshot%20(111).png?raw=true)

3. You will need somewhere for your project to reside, create a directory somewhere and start a shell in that directory then On your command line, execute the following Maven goal to start creating a maven project
```shell
mvn archetype:generate
```
![alt text](https://github.com/sumyak/Apache-Maven/blob/master/cmd/target/site/images/logos/1%20(2).png?raw=true)

4. After that do the following on cmd itself
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






