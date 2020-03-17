# Setup of IntelliJ Idea with JavaFX 

`17 March 2020`

This setup is the simplest possible: the JavaFX library is in a folder in the file system.

There is no use of Maven or Gradle.

For further details go [there](https://openjfx.io/openjfx-docs/#IDE-Intellij):



#### 1. IntelliJ Idea Community Edition (Version 2019.3.3)

* Download [IntelliJ Idea Community Edition](https://www.jetbrains.com/idea/download/) 

* Install IntelliJ Idea

#### 2. OpenJDK (version 14)

* Download [OpenJDK](https://jdk.java.net/14/)

* Unzip in a folder in your system

#### 3. JavaFX (version 14)

* Download [JavaFX](https://gluonhq.com/products/javafx/)

* Unzip in a folder in your system

#### 4. Configure IntelliJ Idea to use the OpenJDK

1. Open IntelliJ Idea
2. In the splash screen click on Configure -> Settings
3. In the section Appearance & Behavior -> Path Variables, click on the + and add the name of the variable: `PATH_TO_FX`, then click on the little folder, navigate to the path of the JavaFX folder, select the lib subfolder (javafx-sdk-14/lib) then click ok
4. In the splash screen click on Configure -> Structure for new projects
5. In the section Project Settings, click on project, then click on new and then on jdk. Navigate to the folder of the JDK (jdk-14)

**For each new JavaFX Project**
1. Create new project
2. JavaFX
3. Verify the selected Project SDK is the one downloaded (14)
4. Click next
5. Put a name to the project and select the directory where the project will be deployed
6. Click Finish
7. Once the project is opened, click in the menu File -> Project Structure
8. In the Project section, verify the selected SDK is the one downloaded (12)
9. In the Libraries section, click on the `+`, navigate to the unzipped folder of JavaFX (javafx-sdk-14) select the lib subfolder and click open, apply, ok
10. Click in the menu Run -> Edit Configurations and in the line " VM Options" copy and paste this line: 

`--module-path ${PATH_TO_FX} --add-modules javafx.controls,javafx.fxml`

apply and ok.

11. Click Run and project is ready

You are ready to work on your JavaFX project inside IntelliJ Idea.
