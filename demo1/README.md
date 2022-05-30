# demo1

## add author information

```bash
# name and email
cd ~/Downloads/java-stuff; git config user.name "Jessica Chen"
cd ~/Downloads/java-stuff; git config user.email "jessica.chen@leocorn.com"

cd ~/Downloads/java-stuff; git config --list
cd ~/Downloads/java-stuff; git log 

# copy directory command
#check source folder
ls -la ~/Downloads/School/ICS4/ISP/intellij
#copy
cp -rv ~/Downloads/School/ICS4/ISP/intellij ~/Downloads
#check target
ls -la ~/Downloads
#remove source
rm -rvf ~/Downloads/School/ICS4/ISP/intellij

```

## set up maven
(so you can load correct java)
first download

```bash
# check PATH.
echo $PATH

# set up maven executable

# check maven version
mvn --version

# set up java home
export JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-18.jdk/Contents/Home; mvn --version
# you can test by reading date
:r!date
#Sat 28 May 2022 16:17:28 EDT

# compile the javafx demo's source code, time to show how long it took to run
export JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-18.jdk/Contents/Home; cd ~/Downloads/java-stuff/demo1; time mvn compile
```

## edit pom.xml file
```xml
<!-- in <build><plugins></plugins></build> -->
   <!--
     - add the exec maven plugin to run a Java Main method
     - to run a Java standalone application
     - reference: https://www.baeldung.com/maven-java-main-method
   -->
   <plugin>
       <groupId>org.codehaus.mojo</groupId>
       <artifactId>exec-maven-plugin</artifactId>
       <version>3.0.0</version>
       <configuration>
           <mainClass>com.example.demo1.HelloApplication</mainClass>
       </configuration>
   </plugin>
```

## run
```bash
# compile and run
export JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-18.jdk/Contents/Home; cd ~/Downloads/java-stuff/demo1; mvn compile exec:java
```
