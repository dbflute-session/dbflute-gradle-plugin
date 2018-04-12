DBFlute Gradle Plugin
======================

This is a Gradle pluin project for DBFlute.
TODO jflute now writing...

Features
--------

This contains following features:

  * Blank implementation of the plugin (see [HelloPlugin.groovy](src/main/groovy/com/example/HelloPlugin.groovy))
  * Testing with Spock (see [HelloPluginSpec.groovy](src/test/groovy/com/example/HelloPluginSpec.groovy))
  * Acceptance Test using Gradle TestKit
  * Continuous Integration and Delivery on Travis CI
  * Publishing the plugin on [Gradle Plugins](http://plugins.gradle.org)
  * Gradle Wrapper
  * `.gitignore` for Gradle, IDEA and Eclipse


Getting Started
---------------

Create your account on [Gradle Plugins](http://plugins.gradle.org/submit) and get the API key.

```properties
# ~/.gradle/gradle.properties
gradle.publish.key=xxx
gradle.publish.secret=
```

This repository contains the example implementation.
Change files to your Group ID and Plugin ID.

Identifier  | In this repository    | To be changed
------------|-----------------------|--------------
Group ID    | `com.example`         | Package name of production and test code, `group` in the build script
Plugin ID   | `com.example.hello`   | Class name of production and test code, the plugin descriptor in resources, `id` in the build script

Build the plugin.

```sh
./gradlew build
```

Publish the plugin.

```sh
TRAVIS_TAG=0.1.0 ./gradlew publishPlugins
```


Working with Travis CI
----------------------

Travis CI builds the plugin continuously.
It also publishes the plugin if a tag is pushed and following variables are set.

Environment Variable        | Value
----------------------------|------
`$GRADLE_PUBLISH_KEY`       | `gradle.publish.key` of the API key
`$GRADLE_PUBLISH_SECRET`    | `gradle.publish.secret` of the API key


Contributions
-------------

This is an open source software licensed under the Apache License Version 2.0.
Feel free to open issues or pull requests.
