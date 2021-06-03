# lazy-logger

Stop doing this:
```java
if (log.isDebugEnabled()){
  log.debug("some heavy calculation: {}", heavyCalculate(params));
  log.debug("JSON formated: {}", objectMapper.writeValueAsString(someObject));
}
```
...and make this:
```java
  log.debug("some heavy calculation: {}", LazyLogger.of(() -> heavyCalculate(params)));
  log.debug("JSON formated: {}", LazyLogger.asJson(someObject));
```
whithout extra CPU cost.

Lazy Logger isn't evaluated if logger isn't enabled, so you haven't care about CPU cost and only care about your logging information.

## How to install

### Gradle


Step 1. Add it in your root build.gradle at the end of repositories:
```groovy
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
Step 2. Add the dependency
```groovy
	dependencies {
	        implementation 'com.github.nallegrotti:lazy-logger:1.0.1'
	}
```

### Maven
Step 1. Add the JitPack repository to your build file 

```xml
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
```

Step 2. Add the dependency

```xml
	<dependency>
	    <groupId>com.github.nallegrotti</groupId>
	    <artifactId>lazy-logger</artifactId>
	    <version>1.0.1</version>
	</dependency>
```
