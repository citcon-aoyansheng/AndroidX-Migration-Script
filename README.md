# AndroidX-Migration-Script

Use this script to help migrate to AndroidX

## Usage

Add the following properties in gradle.properties
```
android.useAndroidX=true 
android.enableJetifier=true 
```

also add `android.jetifier.blacklist=xxx.jar` to ignore the incompatible jar

Sync the project to make sure the dependencies have changed to androidx.
Copying the file to the parent project will scan all subdirectories in the same directory as.py,

```
work folder:
root
-migrate.py
-androidx-class-mapping.csv
-your-android-project
 |-app
 |-build.gradle
 |-other file
```


execute the command in terminal:

```

python3 migrate.py
```

Get the latest mapping file https://developer.android.com/jetpack/androidx/migrate/class-mappings

## Attention
- Dependency replacement is not supported
- Multiline guided packet replacement is not supported

