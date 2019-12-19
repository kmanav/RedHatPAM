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

**NOTE:** The PAM server REST API requires HTTP Basic authentication or token-based authentication for the user role **`kie-server`**. To view configured user roles for your Red Hat Process Automation Manager distribution, navigate to **`~/$SERVER_HOME/standalone/configuration/application-roles.properties`** and **`~/application-users.properties`**. 

The Web API definitions in this .bprelease are configured to use an HTTP Basic credential. If your PAM deployment requires the use of a token credential you must define one within your Blue Prism environment and configure each Web API definition to use that token credential in place of the default HTTP Basic credential.
