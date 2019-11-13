## How to publish a Maven repository

Clone this repository to the same folder where your project's base folder resides.
Put this in your `build.gradle` and run the `gradlew publish` task.

To PR a mod, copy the folder(s) over to the repository and commit.

```groovy
apply plugin: 'maven-publish'
publishing {
    publications {
        mavenJava(MavenPublication) {
            // These should be the default ForgeGradle artifacts
            // sourceJar is sometimes sourcesJar?
            artifact jar
            artifact sourceJar
            // artifact deobfJar
        }
    }
    repositories {
        maven {
            url = "${projectDir}/maven"
        }
    }
}
```