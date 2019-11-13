# Forge-Maven
Maven repository for Minecraft Forge mods

## Current mods
* Athenaeum (`com.codetaylor.mc:athenaeum:${athenaeumVersion}`)
* Dropt (`com.sudoplay.mc:dropt:${droptVersion}`)
* Pyrotech (`com.codetaylor.mc:pyrotech:${pyrotechVersion}`)

## Using this Maven repository

```groovy
repositories {
    ...
    maven {
        name "Gilberreke"
        url "https://simonmeskens.github.io/Forge-Maven/"
    }
}
```