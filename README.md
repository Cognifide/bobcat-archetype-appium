![Cognifide logo](http://cognifide.github.io/images/cognifide-logo.png)

# Bobcat Appium Archetype

## Summary 
This project is Maven archetype for Bobcat using JUnit tests with support for mobile applications using Appium. It contains tests examples based on EspressoApp from [Google Sample Apps](https://github.com/googlesamples/android-testing)

## Prerequisites
* JDK 8
* Maven 3

## Create project
```
mvn archetype:generate \
        -DarchetypeGroupId=com.cognifide.qa.bb.mobile \
        -DarchetypeArtifactId=bb-appium-hello-world-archetype \
        -DarchetypeVersion=1.0.1 \
```
Example properties for archetype
```
Define value for property 'groupId': : com.cognifde.qa.bb
Define value for property 'artifactId': : hello-world
Define value for property 'version':  1.0-SNAPSHOT: : 1.0.0
Define value for property 'package':  com.cognifde.qa.bb: : com.hello.world
```
## Project structure

```
└───hello-world
 |   └───src
 |       ├───main
 |       │   ├───config
 |       │   │   ├───common
 |       │   │   ├───dev
 |       │   └───java
 |       │       └───com
 |       │           └───hello
 |       │               └───world
 |       │                   └───conditions
 |       │                   ├───guice
 |       │                   ├───pageobjects
 |       │                      
 |       └───test
 |           ├───java
 |           │   └───com
 |           │       └───hello
 |           │           └───world
 |           └───resources
 └───pom.xml
```

**Configuration**

Configurations for different environments are stored in the config directory:

```
 |    └───src
 |        ├───main
 |        │   ├───config
 |        │   │   ├───common
 |        │   │   ├───dev
```

**Page object classes**

Page object classes for has their place in com.hello.world.pageobjects package:

```
 |       │       └───com
 |       │           └───hello
 |       │               └───world
 |       │                   └───pageobjects
```

**Test cases**

Test cases written in Java are in com.hello.world package in test directory:

```
 |       └───test
 |           ├───java
 |           │   └───com
 |           │       └───hello
 |           │           └───world
 |           │               ├───EspressoAppTest.java
```

## Running sample AEM test cases
Instruction is the same regardless of a project archetype:
1. Edit _/src/main/config/common/webdriver.properties_ and provide appium settings,
3. Execute following command from the command line:
```
mvn clean test
```
