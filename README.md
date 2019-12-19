# Red Hat Process Automation Manager (PAM) REST API

This Red Hat Process Automation Manager integration for Blue Prism is made up of 19 Web API definitions that corrospond to the various major elements of the Red Hat Process Automation Manager REST API.

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

The integration also includes the following HTTP Basic credential definition:
* Red Hat PAM Basic Credential

These components are contained in the release file **Red Hat PAM REST API vX.X.bprelease**. You will also find a small example process in this repository titled **Red Hat PAM Test.xml**.

**NOTE:** The PAM server REST API requires HTTP Basic authentication or token-based authentication for the user role **`kie-server`**. To view configured user roles for your Red Hat Process Automation Manager distribution, navigate to **`~/$SERVER_HOME/standalone/configuration/application-roles.properties`** and **`~/application-users.properties`**. 

The Web API definitions in this integration are configured to use an HTTP Basic credential. If your PAM deployment requires the use of a token credential you must define one within your Blue Prism environment, and then you must configure each Web API definition to use that token credential in place of the default HTTP Basic credential.

## Installation ##
To install this integration:
1. Download the .bprelease to your Blue Prism Interactive Client
2. From the Blue Prism Interactive Client, select ***File* -> *Import***
3. Follow the prompts to select and import the .bprelease file.
4. After importing the .bprelease, make sure to enter the details of the ***Red Hat PAM Basic Credential*** or set up your token credential if that applies to your environment.

## Using the Web APIs ##
As mentioned previously, there is a small example process included in this repository. This process shows the basic process of invoking a handful of methods on a few of the available Web API interfaces.

**NOTE:** There is no specfic authentication method exposed by the PAM REST API. Authentication will occur based on HTTP negotiation between the PAM server and Blue Prism. You are only responsible for having a valid credential defined within your Blue Prism environment. Blue Prism will submit that credential automatically when prompted by PAM.

The majority of the PAM methods that require submitting some form of data will do so using the body of the HTTP request. The Web API definitions in this integration do not include defined request bodies. You must refer to the Red Hat documentation for further information related to what PAM expects to receive in the body of each specific request. The Blue Prism Web APIs are designed to accept an input string for the request body, so you build the request body within your process and then pass that string into the method.

For the full list of Process Server REST API endpoints and descriptions, use one of the following resources:
* [Execution Server REST API](https://jbpm.org/learn/documentation.html) on the jBPM Documentation page (static)
* Swagger UI for the Process Server REST API at `http://SERVER:PORT/kie-server/docs` (dynamic, requires running Process Server)

Red Hat's PAM REST API support either JSON or XML format. However, the Web API definitions within Blue Prism have all been designed to default to JSON. Should you desire to use XML instead of JSON, you will need to change the ***content-type*** entry of the **Common Headers** definition of each Web API from ***application/json*** to ***application/xml***.
