# Build Systems :

build systems provides a way to automate the tasks( compiling, creating build artifacts, executing test cases and executing check styles) that are very common during the building an application.

I deal with applications in Java. So, I learnt about the basics of ANT, Maven and Gradle.

## ANT(Another Neat Tool) :
- It is build system for java projects. It uses XML as input. 
- The developers have to specify the build steps and action in build.xml file.

```
<?xml version="1.0"?>
<project name="Hello" default="compile">
    <target name="clean" description="remove intermediate files">
        <delete dir="classes"/>
    </target>
    <target name="clobber" depends="clean" description="remove all artifact files">
        <delete file="hello.jar"/>
    </target>
    <target name="compile" description="compile the Java source code to class files">
        <mkdir dir="classes"/>
        <javac srcdir="." destdir="classes"/>
    </target>
    <target name="jar" depends="compile" description="create a Jar file for the application">
        <jar destfile="hello.jar">
            <fileset dir="classes" includes="**/*.class"/>
            <manifest>
                <attribute name="Main-Class" value="HelloProgram"/>
            </manifest>
        </jar>
    </target>
</project>
```

The above is an example of build.xml file in ANT. 
- In ANT, there will be project element which contains muliples target elements and properties.
- Each target element represents an action that it has to execute. Here one target can depend upon other targets. i.e we are telling  ANT to not execute a particular target before executing the targets it depend upon.

## Maven 
It is also a build tool created by Apache Foundation. It is very popular because of its features. Those are managing build process and dependency management.
It was designed using plugin based architecture.That means we can easily extend the functionality using the plugins that we need for specific purpose.

- People like this because it takes care of managing dependecies. (i.e it fetches dependencies if you specify unique coordinates of dependencies. It also fetches the dependencies of dependencies) 
- Maven believes on Convention rather than configuration. i.e Maven provides default values for the project.So developers most of the times don't have to do anything.


```
<project>
  <!-- model version is always 4.0.0 for Maven 2.x POMs -->
  <modelVersion>4.0.0</modelVersion>
  <!-- project coordinates, i.e. a group of values which uniquely identify this project -->
  <groupId>com.mycompany.app</groupId>
  <artifactId>my-app</artifactId>
  <version>1.0</version>
  <!-- library dependencies -->
  <dependencies>
    <dependency>
      <!-- coordinates of the required library -->
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <!-- this dependency is only used for running and compiling tests -->
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
```

From above file we can see that while creating a project, we need to give an unique project coordinates which will be used for identifying the project.
- GroupId - an uniqueIdentifier to a project. 
- artifactId - name of project
- verionId - version number

It has a dependency section where we just need to specify groupId, artifactId and verion. Then maven takes care of downloading them and making it available during the build process.








