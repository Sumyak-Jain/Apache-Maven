# Build Profiles:
## Introduction to Build Profiles:
+  Profiles are specified using a subset of the elements available in the POM itself (plus one extra section), and are triggered in any of a variety of ways.
+  They modify the POM at build time, and are meant to be used in complementary sets to give equivalent-but-different parameters for a set of target environments (providing, for example, the path of the appserver root in the development, testing, and production environments).
+  As such, profiles can easily lead to differing build results from different members of your team. However, used properly, profiles can be used while still preserving project portability. 


