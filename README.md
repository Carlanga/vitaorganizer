## VitaOrganizer 0.3

![](extra/screenshot-0.3.png)

Desktop tool for listing and uploading games and homebrew applications to PSVITA without the size requirements
of uploading the whole VPK and extracting it later.

It is written in Kotlin/Java.

It should work on Windows, Linux and MacOS. It is a Java desktop application, packed in an executable .JAR, that
can be executed directly with double click on most cases.

In other cases, you can run it with `java -jar vitaorganizer-0.3.jar`

You can download a prebuild binary here, or just build from source:
[Download VitaOrganizer 0.3 here](https://github.com/soywiz/vitaorganizer/releases/download/0.3/vitaorganizer-0.3.jar)

## CHANGELOG

**0.3**

* Fixes size of games in psvita (please delete vitaorganizer/cache folder)
* Fixed paths in windows
* Allow column sorting
* Improved error reporting

### Building from source

You can open build.gradle in intelliJ IDEA 2016.2 (Community Edition is ok) to get started directly.
The main class is defined in : `src/com/soywiz/vitaorganizer/VitaOrganizer.kt`

You can compile without intelliJ directly from the console just with gradle. Just call

```
gradle jar
```

It will generate the file `build/libs/vitaorganizer-VERSION.jar` with all the dependencies included as an executable jar
that should work on desktop java versions.

In order to generate a native windows executable:

```
gradle launch4j
```

It will generate the file `build/libs/vitaorganizer-VERSION.exe`. It uses launch4j as launcher,
and proguard for minimizing all the files so the executable will be smaller.