# Minimum JavaFX
Sample project of JavaFX using Gradle with the least files.

Thanks to [test-project](https://github.com/openjfx/javafx-gradle-plugin/tree/bdf717a65ab0caac9cfa677efc9d3943e6f8483e/test-project/modular) of javafx-gradle-plugin and [HelloFX](https://github.com/openjfx/samples/tree/605de7f9fac6b595f787c9d718aa6e523aa1b24f/HelloFX/Gradle) by openjfx team!

This project used them:

| name   | version                                 |
|--------|-----------------------------------------|
| JDK    | 21.0.5 (Eclipse Adoptium 21.0.5+11-LTS) |
| JavaFX | 17                                      |
| Gradle | 8.10 (built 2024-08-14 11:07:45 UTC)    |

Development environment: Windows10, IntelliJ IDEA 2024.3.

## Details
Essential elements of JavaFX project using Gradle:
- build.gradle.kts
  - 'application' plugin make it ease launching Main class
    - `mainClass` refers the name of a class which inherits `javafx.application.Application`
  - 'javafx' plugin provides configuration options to use JavaFX(e.g. if there is no JavaFX library, downloads it automatically)
  - (Optional) 'java' plugin specifies Java version for reproducibility
- Main.java
  - Make sure that this class extends `javafx.application.Application` and overrides `start()` method
  - **Do not** click 'Run Main.main()' button or fails
    - launch via one of tasks of gradle named `application:run`

## References
- [Getting Started with JavaFX#Run HelloWorld using Gradle](https://openjfx.io/openjfx-docs/#gradle)
- [Toolchains for JVM projects](https://docs.gradle.org/8.10/userguide/toolchains.html) Gradle 8.10