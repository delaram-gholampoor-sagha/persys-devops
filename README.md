# persys-CI/CD
**DevOps as a service platform!**
<br>
**i am working on a public version that soon will be released here! read [Updates](#Updates)**
<br>
**!!THIS PROJECT IS UNDER ACTIVE DEVELOPMENT DO NOT USE IN PRODUCTION!!**
<!-- TOC -->
* **[Architecture](#Architecture)**
* **[Updates](#Updates)**
* **[Contributions](#Contributions)**
* **[Open Source]()**
* **[Goals!](#Goals!)**
* **[Project RoadMap]()**
* **[Community](#community)**
* **[Services Description]()**
* **[Documentation](#Documentation)**
* **[CNCF](#CNCF)**
<!-- TOC -->

# Architecture
* **this is the system design that i came up with, a high level mind map to look at.**
* feel free to open an ISSUE mentioning any problems or ideas you might have!

  ![](arch.png)

Open Source DevOps as a Service platform written in Golang with a rust CLI client and next.js frontend,
this project provides tooling needed to take complete control over your CI/CD and Development Environment needs such as :
service discovery , datacenter aware API gateway, multi-environment deployments (Cloud Providers, Local Kubernetes cluster) , traffic monitoring , automatic rollbacks , end-to-end testing , monitoring and health checks using Grafana and Prometheus, services catalogue , and much more!

# how it works!
**refer to [how-it-works.md](https://github.com/miladhzzzz/persys-cicd/docs/how-it-works.md) for a better understanding of how this software works!**

# Updates
* **[8/12/2022] this whole thing is written by me so there's a lot to work on, i'll really appreciate any help!**
* **[10/3/2022] getting my hands on the hardware and infrastructures needed for developing this project has costs please consider donating to us!**
* **[12/24/2022] I'm actively trying to build a community so please at lease give us a star or contribute to our cause!**
* **[12/30/2022] currently the project has hard coded personal / sensitive data in it i'll release the first working version soon to our open source repository which is : https://github.com/miladhzzzz/persys-cicd**
* **[1/12/2023]  achieved first working version on my local environment cleanup is coming along good!**
* **[1/12/2023]  refactoring code to meet a modern microservice architecture boilerplate**
* **[1/12/2023]  changed the architecture! also working on a linear design that will be available soon!**

# Contributions
**we are looking for contributors in fields of expertise listed below:**
<br>
* DevOps Engineers
* UI/UX Designer
* Frontend react, next.js engineer
* Golang developers
* Rust developers
* Cloud network engineers
* Datacenter Architectures and designers
* Software test specialist
* Project managers

**please refer to community section and consider joining us**
[Community](#community)
# Open Source Tech We Use
* [Backstage](https://github.com/backstage/backstage)
* [apache kafka](https://github.com/obsidiandynamics/kafdrop)
* [gRPC](https://github.com/grpc)
* [Git]()
* [Rust (Programming Language)]()
* [Terraform]()
* [Kubernetes]()
* [Go (Programming Language)]()
* [OpenTelemtry](https://github.com/opentelemtry)
* [Watermill](https://github.com/watermill)
* [Mongodb](https://github.com/mongodb)
* [Signoz](https://github.com/signoz)
* [Kafdrop](https://github.com/obsidiandynamics/kafdrop)
* [Ceph](https://github.com/ceph)
* [Github](https://github.com)

# Goals!
**This project really started because of my own pain to setup a development environment for one of my projects.
to give you a little bit of detail i needed apache kafka , mongodb cluster , backstage, prometheus , grafana, signoz ,etc ...
plus i wanted to have a CI/CD pipeline so i can automate my software development at home!
well considering i currently am living in Tehran/Iran internet connection is a disaster and due to sanctions i cant even access ghcr.io or registry.docker.com
so i was looking for a platform to give me everything i need from required dbs , message brokers etc... in a very simplistic manner,
and i found None! so i started making myself the developer platform that i desired! LOL
in summary the goal of this project is** :
* giving you everything you need for developing your project
* automatic git management on webhooks and starting the build proccess that way
* service discovery and api gateway
* monitorning
* service catalogue (Developer Portal)
* automatic builds and end-to-end testing
* deployment to test environment on kubernetes
* multi-environment deployments and management of my service in different places like (Cloud Service Providers, Local environment)
  <br>
  and of course what i have in mind is a platform like https://dev.azure.com but actually having kubernetes as a service in our platform is going to make everything easy!

# Project Road Map
* Q1 2023 : Clean UP the code repository for and rebase to public repository.
* Q1 2023 : Build our Community to help develop, manage , market our product.
* Q1 2023 : Test First Working version!
* Q2 2023 : Submit project to CNCF sandbox projects and integrate our community with the world!
* Q2 2023 : Hopefully we can get our hands on Infrastructure needed to launch our Hosted version of our software.
* Q3 2023 : Grow our Community and hire people to help!
* Q4 2023 : Release the software for on premise use (hosting it yourself).
* Q4 2023 : World Dominance :D.

# community
**Our primary goal in this project as we discussed before is to build a community of iranian highly skilled
specialists to help each other and junior developers in a way that we can write great software that is maintained by
community contributions.**
<br>
and of course integrating our community with the world of Open Source!
<br>
we can find a lot of great software that is written by millions of Open Source contributors accross the globe in https://github.com/readme
<br>
you can join "your" community and start contributing in various projects! please visit our slack or discord (will be updated soon) to ask around and have a dialogue with others!
<br>
https://join.slack.com/t/persys-cicd/shared_invite/zt-1lje1wst0-E0TjKMIXGe1FGLex1uQoxg


# Services Description
* [api-gateway](https://github.com/miladhzzzz/persys-cicd) : a pretty basic api gateway that talks to the whole system and handles authorization, notification, user management (clients send http rest calls and we generate gRPC calls to microservices and use kafka to check on jobs)
* [ci-service](https://github.com/miladhzzzz/persys-cicd) : obviously does ci server stuff build your code test it and push it to a private and/or multiple repositories.
* [clients/cli](https://github.com/miladhzzzz/persys-cicd) : a cli interactive shell written in rust that communicates with api-gateway.
* [events-manager](https://github.com/miladhzzzz/persys-cicd) : events manager is responsible for aggregating events throughout the whole system with kafka
* [shipper](https://github.com/miladhzzzz/persys-cicd) : shipper deploys your code to different types of environments (Cloud, On-Prem , etc...) getting your environment from cloud-mgmt.
* [theye](https://github.com/miladhzzzz/persys-cicd) : theye will keep an on "EYE" on system state and try to get desired state of the whole system talking to cloud-mgmt and ci-service , shipper.
* [cloud-mgmt](https://github.com/miladhzzzz/persys-cicd) : this is a datacenter-cloud inter-connect fabric that will be responsible for kubernetes-as-a-service on persys-cloud or your cloud-provider.

# Documentation
**the documentation will be located at https://github.com/miladhzzzz/persys-cicd/docs**
* [getting-started.md](https://github.com/miladhzzzz/persys-cicd/docs/getting-started.md)
* [how-it-works.md](https://github.com/miladhzzzz/persys-cicd/docs/how-it-works.md)
* [install.md](https://github.com/miladhzzzz/persys-cicd/install.md)
* [architecture.md](https://github.com/miladhzzzz/persys-cicd/architecture.md)
* [contributions.md](https://github.com/miladhzzzz/persys-cicd/contributions.md)

# Cloud Native Computing Foundation
<br>
this project is currently in the sandbox waiting list of Cloud Native Computing Foundation, and as we mentioned above we are using and supporting a lot of CNCF technologies
<br>
so, thank you 

[CNCF](https://github.com/miladhzzzz/persys-cicd) <3

![](cncf-ambassador.png)