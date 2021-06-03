<div align=center>
<img width="500" src="https://cdn.discordapp.com/attachments/841815050187833354/849869083100971008/ether-eternitytwo.png" alt="Yatopia" align="top">
<div align=center>
-

[![Github-CI](https://github.com/YatopiaMC/Yatopia/workflows/CI/badge.svg)](https://github.com/YatopiaMC/Yatopia/actions?query=workflow%3ACI)
[![CodeMC](https://ci.codemc.io/buildStatus/icon?job=YatopiaMC%2FYatopia%2Fver%252F1.16.5)](https://ci.codemc.io/job/YatopiaMC/job/Yatopia/job/ver%252F1.16.5/)
[![Discord](https://img.shields.io/discord/342814924310970398?color=%237289DA&label=Discord&logo=discord&logoColor=white)](https://discord.gg/YatopiaMC)
[![API](https://img.shields.io/website?down_color=lightgrey&down_message=offline&label=API&up_color=green&up_message=online&url=http%3A%2F%2Fapi.yatopiamc.org%2F)](https://api.yatopiamc.org/v2/latestBuild?branch=ver/1.16.5)
<h3>The best serum of Minecraft server performance, stability & configuration you'll ever taste!</h3>
</div>
<div align=left>

## So what is Ether Eternity?
Ether Eternity combines the code from various [Paper](https://github.com/PaperMC/Paper) forks and mods, as well as many unique optimizations. We borrow code from the following repos:

* [Akarin](https://github.com/Akarin-project/Akarin)
* [EMC](https://github.com/starlis/empirecraft)
* [Lithium](https://github.com/jellysquid3/lithium-fabric)
* [Origami](https://github.com/Minebench/Origami)
* [Purpur](https://github.com/pl3xgaming/Purpur)
* [Airplane](https://github.com/Technove/Airplane)
* [Cadmium](https://github.com/LucilleTea/cadmium-fabric)
* [Tic-Tacs](https://github.com/Gegy/tic-tacs)


## Try it out 
The latest stable builds of Ether Eternity are always available over at our [downloads page](https://yatopiamc.org/download.html). You can also download the latest development build [here](https://api.yatopiamc.org/v2/latestBuild/download?branch=ver/1.16.5).

## Documentation

 You can find a full explanation of the Ether Eternity configuration file on the [wiki](https://github.com/YatopiaMC/Yatopia/wiki). Check out the list of patches included in this project and who created them [here](PATCHES.md).

## Building and setting up

Run the following commands in the root directory:

```shell
./gradlew initGitSubmodules
./gradlew setupUpstream
./gradlew applyPatches
./gradlew paperclip
```


## Using Yatopia-API

To build your plugin against the EtherEternity-API, first add the CodeMC maven repository:

# Maven
Add the CodeMC Repo:
```xml
<repositories>
    <repository>
        <id>codemc-repo</id>
        <url>https://repo.codemc.io/repository/maven-public/</url>
    </repository>
</repositories>
```

And then add the EtherEternity-API dependency:
```xml
<dependencies>
    <dependency>
        <groupId>org.yatopiamc</groupId>
        <artifactId>yatopia-api</artifactId>
        <version>1.16.5-R0.1-SNAPSHOT</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```

# Gradle

> Groovy DSL

Add the CodeMC Repo:
```groovy
repositories {
    maven {
        url 'https://repo.codemc.io/repository/maven-public/'
    }
}
```

And then add the EtherEternity-API dependency:
```groovy
dependencies {
    compileOnly 'org.yatopiamc:yatopia-api:1.16.5-R0.1-SNAPSHOT'
}
```

> Kotlin DSL

Add the CodeMC Repo:
```kotlin
repositories {
    maven("https://repo.codemc.io/repository/maven-public/")
}
```

And then add the Yatopia-API dependency:
```kotlin
dependencies {
    compileOnly("org.yatopiamc:yatopia-api:1.16.5-R0.1-SNAPSHOT")
}
```

## Why aren't there many API additions?

(Modified from [starlis/empirecraft](https://github.com/starlis/empirecraft/))
<p>
APIs are tough to design. In projects such as Bukkit, Spigot, Sponge, Paper, etc once an API is committed, it's almost forever. You can't go breaking it without solid justification. This is the politics game.

With that in mind, much thought has to be given to the API in now and future use cases and applications to ensure it can be extended without breaking.

This is a lot of politics that we don't have time in our lives to deal with. 

That being said we make light API additions when requested.
</p>

## License

License information can be found [here](/Licensing/LICENSE.md).

## Security

Security information can be found [here](/SECURITY.md).

## Statistics
[![bStats Graph Data](https://bstats.org/signatures/server-implementation/Yatopia.svg)](https://bstats.org/plugin/server-implementation/Yatopia)

Made with <span style="color: #e25555;">&#9829;</span> by the developers of [Dygamic](https://dygamic.com/team) & [Contributers](https://github.com/Castafers/EtherEternity/graphs/contributors).
