## Overview of Tackle

Your containerization and journey to Kubernetes might be easier if you have a green field. But what if it's the complete opposite? What if you have hundreds of legacy applications alongside their dependencies for dozens of business services? The open-source [Tackle](https://www.konveyor.io/tackle) tool, as part of the [Konveyor](https://www.konveyor.io) project, helps you assess your application portfolio to get recommendations in your journey to Kubernetes. This blog talks about the tools that make up Tackle and how they help streamline the modernization and migration of your application portfolio to Kubernetes.   

## How Tackle fits into the overall Konveyor landscape

Tackle is one of the projects under the larger Konveyor umbrella community. Let's use the following diagram to discuss how Tackle fits in and what problems is it addressing.

![Konveyor Projects](assets/konveyor-projects.jpg)

At first, we assess our application portfolio with [Tackle Pathfinder](https://github.com/konveyor/tackle-pathfinder) - a tool that is used to come up with the migration strategy to follow with each application or application type. For the refactor strategy, we can also use Tackle to detect what needs to be changed for all the applications assessed by Tackle Pathfinder to run on the target environment and provide guidelines and some degree of automation on how to perform these changes. 

Once your applications are assessed by Tackle, they can be rehosted using [Crane](https://www.konveyor.io/crane) or [Forklift](https://forklift.konveyor.io/), replatformed using [Move2Kube](https://move2kube.konveyor.io/), and/or refactored using other tools that are part of the Tackle project.   

## How Tackle components come together to help you assess applications to migrate to Kubernetes

Tackle comprises three key pillars:

- Application Inventory
- Pathfinder
- Controls
 
The Controls component is a bit different from the first two as it is used to store master data for the Application Inventory and Pathfinder. This blog will highlight Pathfinder and Application Inventory since Tackle users will not interact with the Controls component directly. 

[Tackle Application Inventory](https://github.com/konveyor/tackle-application-inventory) allows users to maintain their portfolio of applications, link them to the business services that they support, define their interdependencies, and use an extensible tagging model to add metadata to describe and categorize them in multiple dimensions. The Application Inventory is the vehicle by which an application can be selected for assessment by Pathfinder.

[Tackle Pathfinder](https://github.com/konveyor/tackle-pathfinder) is a questionnaire-based tool that assesses the suitability of applications for modernization in order to be deployed in Containers on an enterprise Kubernetes platform. Through interaction with the questionnaire, and review process, the system is enriched with application knowledge which is exposed via a collection of reports. The reports provide information about applications’ suitability for Kubernetes, highlight associated risks, and generate an adoption plan informed by the applications’ prioritization, business criticality, and dependencies.

Both Application Inventory and Pathfinder tools are accessible from a common [Tackle UI](https://github.com/konveyor/tackle-ui/).

Besides the above two tools, there are [Tackle DiVA](https://github.com/konveyor/tackle-diva), [Tackle Test Generator](https://github.com/konveyor/tackle-test-generator-cli), and [Tackle Container Advisor](https://github.com/konveyor/tackle-container-advisor) which you can learn more about from the links under the resources section. 

## How to get involved with the Tackle project

Ready to give Tackle a try? Start [here](https://www.konveyor.io/tackle).

Have a question or just would like to say "hi"? Join the [Tackle Mailing List](https://groups.google.com/g/tackle-dev) or join the #konveyor channel on slack.k8s.io

## Resources

- [Tackle Containerization Advisor (TCA) for Legacy Applications](https://www.youtube.com/watch?v=VapEooROERw)

- [Data-centric Application Analysis with Open-source Tool Tackle-DiVA](https://www.youtube.com/watch?v=UJi1tGFMw2M)
- [Migrate and Modernize your Application Portfolio to Kubernetes with Tackle](https://www.youtube.com/watch?v=S8ISWz87rlk)
- [Tackle-test: An Automatic Unit-level Test Case Generator](https://www.youtube.com/watch?v=qThqTFh2PM4)
