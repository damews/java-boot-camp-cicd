# Simple guide to java projects and ecosystem

## Installing Java
When installing java, you may install __JRE__ (Java Runtime Environment) or __JDK__ (Java Development Kit).
On production servers JRE is enough, on development machine you need JDK installed. 

WARNING: DO NOT use [Oracle java](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) (because of possible license issues)! 

* [Java 8](https://adoptium.net/?variant=openjdk8&jvmVariant=hotspot) - download ZIP JDK package.
* [Java 11](https://adoptium.net/?variant=openjdk11&jvmVariant=hotspot) - download ZIP JDK package.

After downloading ZIP package, unzip it into target directory and set PATH and JAVA_HOME environment variables.

## Install maven
Download and install [maven](https://maven.apache.org/download.cgi), use ZIP package. After downloading ZIP package, unzip it into target directory and set PATH environment variable.

## Set your .gitignore properly
Always set your __.gitignore__ file properly, so only project files are in repository.
__Git repository must contain only "clean" maven project.__ 
What should NOT be in git repository:
* target/* files - build products
* IDE related files like *.iml or .idea
* any temporary files

## Always use maven or gradle projects
Always use [maven](https://maven.apache.org/download.cgi) or [gradle](https://gradle.org/install/) projects.
Do not use projects created by your IDE, because different IDEs may be used on same project !
This guide is designed for maven, but same principles apply for gradle build tool as well.

#### Use proper groupName, artefactId and version
Build result of java project is artefact - [jar](https://en.wikipedia.org/wiki/JAR_(file_format)), [war](https://en.wikipedia.org/wiki/WAR_(file_format)), or zip file. 
Always use [proper artefact naming](http://maven.apache.org/guides/mini/guide-naming-conventions.html) for your project atefacts.   
Use [semantic versioning](https://semver.org/) for you projects.

#### Project directory structure
It is very important to follow [java/maven project directory structure](https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html) conventions.
Maven directory structure is used also in gradle projects as default.

#### Build project
You should be able to build your project using ``mvn clean install`` command or ``gradle clean build`` command.

## Check your dependencies
Use well known public maven repositories to check your project dependencies.
* [maven central](https://search.maven.org/)
* [jcenter](https://bintray.com/bintray/jcenter)
* [spring.io](https://repo.spring.io)

Use up-to date dependencies. Maven command ``mvn dependency:tree -Dverbose``

## Recommended Java projects and libraries
When you are looking for java framework or library:
* [Awesome Java](https://github.com/akullpp/awesome-java)
* [Springboot initializr](https://start.spring.io/) and [docs](https://spring.io/docs)

## Recommended 3-rd party projects
* [Linux Foundation](https://www.linuxfoundation.org/projects/)
* [Eclipse Foundation](https://projects.eclipse.org/)
* [Apache foundation](https://www.apache.org/index.html#projects-list)
