# Red Hat Process Automation Manager (PAM) REST API

This .bprelease file contains 19 Web API implementations that corrospond to the various major elements of the Red Hat Process Automation Manager REST API.

The Web API definitions include:
* Red Hat PAM - Case Instance Admin
* Red Hat PAM - Case Instances
* Red Hat PAM - Case Queries
* Red Hat PAM - Custom Queries
* Red Hat PAM - DMN Models
* Red Hat PAM - Documents
* Red Hat PAM - Jobs
* Red Hat PAM - Planning and Solvers - BRP
* Red Hat PAM - Process and Task Definitions
* Red Hat PAM - Process and Task Forms
* Red Hat PAM - Process Images
* Red Hat PAM - Process Instance Admin
* Red Hat PAM - Process Instances
* Red Hat PAM - Process Queries
* Red Hat PAM - Server and Containers
* Red Hat PAM - Session Assets
* Red Hat PAM - Static Files - BPM
* Red Hat PAM - Task Instance Admin
* Red Hat PAM - Task Instances

The .bprelease also includes the following HTTP Basic credential definition:
* Red Hat PAM Basic Credential

**NOTE:** the Red Hat PAM REST API can support either HTTP Basic or OAuth authentication. These Web API definitions have been configured to support HTTP Basic. If your PAM deployment is configured to utilize OAuth you will need to create a new OAuth credential definition in your Blue Prism environment and modify each of the Web API definitions to use that credential instead of the default HTTP Basic credential.
