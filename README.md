# ShouldKO 

ShouldKO is tiny wrapper around assertion libraries to improve the error messages.

[![Build Status](https://travis-ci.org/miensol/shouldko.svg?branch=master)](https://travis-ci.org/miensol/shouldko)

## Hamcrest

Given standard hamcrest assertions:

```kotlin
assertThat("abcde".startsWith("aa"), equalTo(true))
``` 

you'll get:

```
java.lang.AssertionError: 
Expected: <true>
     but: was <false>
``` 

However, **ShouldKO** improves on that:

```kotlin
"abcd".startsWith("aa").shouldEqual(true)
```

will result in:

```
java.lang.AssertionError: "abcd".startsWith("aa") 
Expected: <true>
     but: was <false>
```

## Installation

Register bintray maven repository:

```groovy
repositories {
    maven {
        url  "https://dl.bintray.com/brightinventions/maven" 
    }
}
```

And add 'pl.miensol.shouldko:hamcrest' to your test implementation dependencies:

```groovy
compile 'pl.miensol.shouldko:hamcrest:0.1.2'
```

