# Build Profiles:
## Introduction to Build Profiles:
+  Profiles are specified using a subset of the elements available in the POM itself (plus one extra section), and are triggered in any of a variety of ways.
+  They modify the POM at build time, and are meant to be used in complementary sets to give equivalent-but-different parameters for a set of target environments (providing, for example, the path of the appserver root in the development, testing, and production environments).
+  As such, profiles can easily lead to differing build results from different members of your team. However, used properly, profiles can be used while still preserving project portability. 

## What are the different types of profile? 
**Per Project**
 ```python
 Defined in the POM itself (pom.xml).
 ```

**Per User**
```python
Defined in the Maven-settings (%USER_HOME%/.m2/settings.xml).
```

**Global**
```python
Defined in the global Maven-settings (${maven.home}/conf/settings.xml).
```

## How can a profile be triggered? How does this vary according to the type of profile being used?

A profile can be triggered/activated in several ways:
+ Explicitly
+ Through Maven settings
+ Based on environment variables
+ OS settings
+ Present or missing files

### Before starting with to know different ways on how to trigger your profiles first you have to make a build of your project.
you can see this to know how to make a build using cmd in just simple 5-6 steps!.

[How to make a build](/cmd/readme.md)


