## GIT TO TEST MAVEN RELEASE PLUGIN


To prepare:

```
mvn release:clean release:prepare
```                       

The "prepare" goal actually does quite a lot. Indeed, it will:

Make sure that there are no uncommitted changes or SNAPSHOT dependencies (see above)
Update the SNAPSHOT version number to a release version (e.g. going from "1.0.1-SNAPSHOT" to "1.0.1")
Update the SCM section of the POM file to point to the release tag rather than the trunk in the Subversion repository
Run all the application tests to make sure everything still works
Commit the changes made to the POM file
Create a new tag in Subversion for this release
Update the SNAPSHOT version number to a new SNAPSHOT version (e.g. going from "1.0.1" to "1.0.2-SNAPSHOT")
Commit the changes made to the POM file


to release:


```
mvn release:perform
```


