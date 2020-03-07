# Build Systems :

build systems provides a way to automate the tasks that are very common during the building an application.

I deal with applications in Java. So, I learnt about the basics of ANT, Maven and Gradle.

## ANT(Another Neat Tool) :
- It is build system in java. It uses XML as input. 
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

The above is an example of build.xml file in ANT. In ANT, there will be project element which contains muliples target elements.
Each target element represents an action that it has to execute. Here one target can depend upon other targets. i.e we are telling 
ANT to not execute a particular target before executing the targets it depend upon.

