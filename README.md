# lazy-logger

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
