# OCI Devops Build pipeline - Build a java application using Gradle.

This sample shows how build and upload output artifact of a Java application using Gradle ,using OCI Buildpipeline.


## Objectives

- Create a devops project/code repo /buildpiepline .
- Run the test build and push the artifact to artifact repo.

## Procedure to use this illustration.

### OCI Access setups.

- Create an OCI Dynamic group and add the below rules. Replace <YOUR_COMPARMENT_OCID> with your compartment OCID. - https://docs.cloud.oracle.com/iaas/Content/Identity/Tasks/managingdynamicgroups.htm 

```java
ALL {resource.type = 'devopsbuildpipeline', resource.compartment.id = '<YOUR_COMPARMENT_OCID>'}
```

- Create an OCI policy and add the following policy statements. Replace <YOUR_DynamicGroup_NAME> with the name of your dynamic group for DevOps and with the name of your compartment. - https://docs.cloud.oracle.com/iaas/Content/Identity/Concepts/policies.htm

```java
Allow dynamic-group <YOUR_DynamicGroup_NAME> to manage ons-topics in compartment <YOUR_COMPARTMENT_NAME>
Allow dynamic-group <YOUR_DynamicGroup_NAME> to manage all-artifacts in compartment <YOUR_COMPARTMENT_NAME>
```

### OCI Notifications
- Create an OCI notification topic - https://docs.oracle.com/en-us/iaas/Content/Notification/Tasks/managingtopicsandsubscriptions.htm#createTopic

### OCI Artifact repo

- Create an OCI Artifact registry repo . - https://docs.oracle.com/en-us/iaas/Content/artifacts/manage-repos.htm#create-repo 
- You can enable or disable Immutable option as accordingly.We would prefer immutable artifacts

![](images/oci-artifact-repo.png)

### OCI Devops Setup.

- Create an OCI notification topic - https://docs.oracle.com/en-us/iaas/Content/Notification/Tasks/managingtopicsandsubscriptions.htm#createTopic
- Create a DevOps project - https://docs.oracle.com/en-us/iaas/Content/devops/using/create_project.htm#create_a_project. Associate with the notification topic.

