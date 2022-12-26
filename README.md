Hello everyone! This time, I'm using a demo application called "Suggest-Library", for which I've constructed a multibranch-pipeline. It is a Java app, so I'm using Maven. Lastly, I've set up a Maven repository on Jfrog's Artifactory.

Here is what the CI stages look like:
- (when the branch name = release/*) calculate correct version based on branch & last tag
- compile code in all branches
- test in all branches
- (when release/* or master) publish to artifactory
- (when release/*) tag the release itself
