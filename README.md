# java-stuff

# add author information

```bash
# name and email
cd ~/Downloads/java-stuff; git config user.name "Jessica Chen"
cd ~/Downloads/java-stuff; git config user.email "jessica.chen@leocorn.com"

cd ~/Downloads/java-stuff; git config --list
cd ~/Downloads/java-stuff; git log 
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
# compile and run
export JAVA_HOME=/Library/Java/JavaVirtualMachines/zulu-18.jdk/Contents/Home; cd ~/Downloads/java-stuff/demo1; mvn compile exec:java
```

## edit pom.xml file
