## How to publish a Maven repository

Clone this repository to the same folder where your project's base folder resides.
Put this in your `build.gradle` and run the `gradlew publish` task.

```groovy
task sourcesJar(type: Jar) {
    from sourceSets.main.allJava
    classifier = 'sources'
}

artifacts {
    archives sourcesJar
}

apply plugin: 'maven-publish'
publishing {
    publications {
        mavenJava(MavenPublication) {
            artifact jar
            artifact sourcesJar
        }
    }
    repositories {
        maven {
            url = file("../Forge-Maven")
        }
    }
}
```