# OCI Devops Build pipeline - Build a java application using Gradle.

This sample shows how build and upload output artifact of a Java application using Gradle ,using OCI Buildpipeline.


## Objectives

- Create a devops project/code repo /buildpiepline .
- Run the test build and push the artifact to artifact repo.

## Procedure to use this illustration.

### OCI Notifications
- Create an OCI notification topic - https://docs.oracle.com/en-us/iaas/Content/Notification/Tasks/managingtopicsandsubscriptions.htm#createTopic

### OCI Artifact repo

- Create an OCI Artifact registry repo . - https://docs.oracle.com/en-us/iaas/Content/artifacts/manage-repos.htm#create-repo 
- You can enable or disable Immutable option as accordingly.We would prefer immutable artifacts

![](images/oci-artifact-repo.png)


