# DevOps-06-Nexus-java-app

This repository demonstrates how to build and publish a Java JAR artifact to **Sonatype Nexus Repository** using Gradle.


## Create Nexus User

Security → Users → Create local user
* **ID:** `user-name`
* **Roles:** `nx-anonymous`

Security → Roles → Create Role
* **Type:** `Nexus role`
* **Role name:** `nx-java`
* **Applied Privileges:** `nx-repository-view-maven2-maven-snapshots-*`

Remove the previous role from the user and assign the newly created `nx-java` role.

## Configure Gradle

Configure Gradle to connect to your Nexus Repository by setting the following:

* **Nexus Repository URL:** Set the repository URL in `build.gradle`.
* **Nexus credentials:** Set your Nexus username and password in `gradle.properties`.

## Build and Publish the JAR to Nexus

```bash
gradle build
```
```bash
gradle publish
```

## Acknowledgements

This demo project was created as part of the DevOps Bootcamp by **TechWorld with Nana**.<br>
Many thanks to Nana for creating such a comprehensive and practical learning experience.
