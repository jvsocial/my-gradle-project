# my-gradle-project
Demo
# Creating a Simple Gradle Project and Pushing to GitHub

This guide will walk you through the process of creating a simple Gradle project on your local Linux terminal and pushing it to GitHub.

## Step-by-Step Guide

1. **Create Project Directory**: Open a terminal and create a new directory for your project.
    ```bash
    mkdir my-gradle-project
    ```

2. **Navigate to the Project Directory**:
    ```bash
    cd my-gradle-project
    ```

3. **Create Source Directory Structure**:
    ```bash
    mkdir -p src/main/java/com/example
    ```

4. **Create Main Java File**:
    ```bash
    touch src/main/java/com/example/Main.java
    ```

5. **Open Main.java in a Text Editor**:
    ```bash
    nano src/main/java/com/example/Main.java
    ```
   Add the following content to the `Main.java` file:
    ```java
    package com.example;

    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello, world!");
        }
    }
    ```

6. **Create build.gradle File**:
    ```bash
    touch build.gradle
    ```

7. **Open build.gradle in a Text Editor**:
    ```bash
    nano build.gradle
    ```
   Add the following content to the `build.gradle` file:
    ```groovy
    apply plugin: 'java'

    repositories {
        jcenter()
    }

    dependencies {
        // Add your dependencies here
    }

    jar {
        // Configure JAR packaging
        manifest {
            attributes(
                'Main-Class': 'com.example.Main'
            )
        }
    }
    ```

8. **Initialize Git Repository**:
    ```bash
    git init
    ```

9. **Add Files to Git**:
    ```bash
    git add .
    ```

10. **Commit Changes**:
    ```bash
    git commit -m "Initial commit"
    ```

11. **Create Repository on GitHub**: 
    - Go to [GitHub](https://github.com) and log in.
    - Click on the "+" icon in the top-right corner and select "New repository".
    - Enter a name for your repository (e.g., `my-gradle-project`) and click "Create repository".

12. **Set Remote Origin**:
    ```bash
    git remote add origin https://github.com/your-username/my-gradle-project.git
    ```
   Replace `your-username` with your GitHub username.

13. **Push Changes to GitHub**:
    ```bash
    git push -u origin master
    ```
   You may need to enter your GitHub credentials.

Now your Gradle project is created, committed, and pushed to GitHub successfully. You can check your GitHub repository to verify that the files are uploaded correctly.
