# javax.annotation-api
[![Maven Central](https://img.shields.io/maven-central/v/org.rationalityfrontline.workaround/javax.annotation-api.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:%22org.rationalityfrontline.workaround%22%20AND%20a:%22javax.annotation-api%22)  [![Apache License 2.0](https://img.shields.io/github/license/rationalityfrontline/javax.annotation-api)](https://github.com/RationalityFrontline/javax.annotation-api/blob/master/LICENSE)

This library is a temporary workaround for the spilt package problem between javax.annotation:javax.annotation-api and com.google.code.findbugs:jsr305. 
It solved the split package problem by merging the two libraries into a single jar.

## Usage

Just add the following code blocks to your build.gradle.kts file.
(First exclude your dependency of "javax.annotation:javax.annotation-api" and "com.google.code.findbugs:jsr305", then add this library as a dependency)

**Gradle Kotlin DSL:**

```kotlin
repositories {
    mavenCentral()
}

dependencies {
    implementation("org.rationalityfrontline.workaround:javax.annotation-api:1.3.2-3.0.2")
}

configurations.all {
    exclude(group = "javax.annotation", module = "javax.annotation-api")
    exclude(group = "com.google.code.findbugs", module = "jsr305")
}
```

## License

javax.annotation-api is released under the [Apache 2.0 license](https://github.com/RationalityFrontline/javax.annotation-api/blob/master/LICENSE).

```
Copyright 2021 RationalityFrontline

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```