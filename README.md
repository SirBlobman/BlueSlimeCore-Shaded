# BlueSlimeCore Shaded Dependencies Module

This module includes all shaded libraries and dependencies for BlueSlimeCore.
You can use this library in your own projects, but its better to shade in your own dependencies.

## Included Libraries

The following libraries are relocated to the `com.github.sirblobman.api.shaded` package:

- [Cryptomorin XSeries](https://github.com/CryptoMorin/XSeries): MIT License
- [Kyori Adventure](https://github.com/KyoriPowered/adventure): MIT License
- [bStats](https://github.com/Bastian/bStats): MIT License

Folia Helper is kept as-is (not relocated):

- [Folia Helper](https://github.com/SirBlobman/Folia-Helper/): GPL-3.0 License


## License

This project is licensed with GPL-3.0.

## Dependency Information

<details>
<summary>Maven</summary>

**Repository:**
```xml
<repository>
    <id>sirblobman-public</id>
    <url>https://nexus.sirblobman.xyz/public/</url>
</repository>
```

**Dependency:**
```xml
<dependency>
    <groupId>com.github.sirblobman.api</groupId>
    <artifactId>shaded</artifactId>
    <version>3.0-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

</details>
<details>
<summary>Gradle: Kotlin</summary>

```kotlin
repositories {
    maven("https://nexus.sirblobman.xyz/public/")
}

dependencies {
    compileOnly("com.github.sirblobman.api:shaded:3.0-SNAPSHOT")
}
```

</details>
<details>
<summary>Gradle: Groovy</summary>

```groovy
repositories {
    maven {
        name = 'sirblobman-public'
        url = 'https://nexus.sirblobman.xyz/public/'
    }
}

dependencies {
    compileOnly 'com.github.sirblobman.api:shaded:3.0-SNAPSHOT'
}
```

</details>
