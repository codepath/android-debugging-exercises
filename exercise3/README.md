1. Check your build.gradle file to verify there are no compilation errors.

You may need to update this file depending on what SDK verison you have installed and
what Build Tools you have installed.  The current configuration relies on SDK 18
and Build Tools 19.1.0:

```
android {
    compileSdkVersion 18
    buildToolsVersion "19.1.0"
```

2. Compile and run.

3. The app is supposed to display the Rotten Tomatoes latest box office movies similar to this screenshot:

https://camo.githubusercontent.com/b281aa0286a5c99fc2683c5e2aabf4ba1ae03d62/687474703a2f2f692e696d6775722e636f6d2f7a51507a4178442e706e67
