# Create serverless applications

## Identify the technology options
Business processses in software are often called **workflows**, Azure offers different technologies to build
these workflows:
- [Logic Apps](https://azure.microsoft.com/en-us/services/logic-apps/)
- [Microsoft Power Automate](https://flow.microsoft.com/en-us/)
- [WebJobs](https://docs.microsoft.com/en-us/azure/app-service/webjobs-create)
- [Azure Functions](https://azure.microsoft.com/en-us/services/functions/)
### Similarities
- They can accept **inputs**
- They can run **actions**
- They can have **conditions**
- They can produce **outputs**
- They can be **triggered** by an external event or run on a **schedule**

## Design-first Technologies
### Logic Apps
It's possible to create a flow diagram, this is called a **design-first** approach.
Automate, orchestrate and integrate components of a distributed application. This thing looks a lot like AWS Step Functions to me.
Over 200 connectors are included with Logic Apps, a connector is a component that proved an interface to an external service, e.g. Twitter.
If your favourite service does not have a pre-existing connector, you can define your own.

### Power Automate
It's possible to create a flow diagram, this is called a **design-first** approach.
This thing lets you create workflows without any knowledge of development or IT experience.
There are 4 types of flow:
- Automated: triggered from some event, e.g. a tweet
- Button: triggered from a button, no shit
- Scheduled: runs on a schedule, also..no shit
- Business process: a flow that models a business process, e.g. stock ordering
Under the hood, *Power Automate* is built on *Logic Apps*, this means that *Power Automate* supports the same
set of connectors.

### Design-first Technologies Compared
|       | Power Automate | Logic Apps            |
|-------|----------------|-----------------------|
| Users | Analysts       | Developers            |
| Tools | GUI Only       | Code editing possible |

## Code-first Technologies
### WebJobs
*Azure App Service* is a service for web applications, backends, api's.. This service looks like AWS Elastic Beanstalk on steroids.
*WebJobs* are a part this service and can be used to run a program or script automatically.
There are 2 kinds of WebJobs:
- Continuous: runs in a loop to for example check a shared folder for new content
- Triggred: runs when manually started or on schedule
WebJobs can be written in Shell languages like *bash* or *PowerShell* are a full blown programming language
like *Java* or *Python*
#### WebJob SDK
Reduces the amount of code needed to interact with the *Azure App Service*. Only supported for C#, so it's a no from me.

### Azure Functions
Basically AWS Lambda, but for Azure.
Types of triggers: HttpTrigger, TimerTrigger, BlobTrigger, CosmosDbTrigger. All are pretty self-explanatory, and seem to be a one-on-one equivalent of their AWS counterpart.

### Code-first Technologies Compared
This is like comparing Beanstalk and Lambda. Azure Functions are fully managed by Azure, WebJobs require some attention for scaling, *but* you can make use of the host system.
