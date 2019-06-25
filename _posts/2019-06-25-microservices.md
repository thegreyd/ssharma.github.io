---
layout: post
title: "Microservices Part 1"
date: '2019-06-25'
categories: engineering
---

My notes as I read through Sam Newman's excellent [Building Microservices](https://samnewman.io/books/building_microservices/) book.

![Architecture diagram](https://dzone.com/storage/temp/5302608-1.png)

<!-- more -->

Microservices are small services working together (usually known as Microservice architecture) to enable functionality in software. They allow organizations to deliver software faster, embrace new technologies while giving more freedom to react and respond to changes (agile). The opposite of Microservices architecture is a Monolith, and it can be looked as a solution to the problems with Monolithic architecture.

A Monolith by definition a big application with a big codebase. It does many different things. It is deployed as a single unit, therefore any change to any part requires a re-deploy. It is very inflexible since it is a slow moving giant (think in terms of refactoring). 

Microservices in contrast are
- **Small and Focused on doing one thing well** - A good metric on how small is it can be rewritten in 2 weeks.
- **Autonomous** - Microservices are independent. All communiation between services happen through the network using their APIs. With clearly defined external APIs, the internal implentation is not tightly coupled to other applications. This independence allows them to be deployed, tested, developed, changed without affecting other apps (unless there is a change in the API).

## Key benefits
- **Technology Heterogeneity** - Choose any technology inside the service since they are decoupled. Freedom to choose the best tool for the job.
- **Resilience** - Failure is contained within a service, and does not affect other systems (unlike a Monolith)
- **Scaling** - Any service can be independently scaled up and down according to usage.
- **Independently deployable**
- **Allows for Reuse** - Decomposition allows for reuse of common features
- **Team Ownership** - Smaller teams working on smaller codebases are more productive.
- **Maintainable** - Easy to replace, rewrite, refactor

Sam notes this about microservies and SOA

> "_The microservice approach has emerged from real-world use, taking our better understanding of systems and architecture to do SOA well. So you should instead think of microservices as a specific approach for SOA in the same way that XP or Scrum are specific approaches for Agile software development._"

Other software decompositional techniques like shared libraries, modules are not as effective as microservices.

Sam goes in length to deconstruct and explain why software architects are not really architects, but they should be thought as Town Planners. Software organically evolves over time unlike a building, but very much like a city. Instead of architect we should think evolutionary architect (I'm not sure if it helps that much). He talks about how to come up and align goals(business), principles(architecture) and practices(implentation). He explains why it's a good idea to standardize engineering practices and technology inside your organization.

Like a town planner, the most interesting piece for an evolutionary architect is how different systems interacts with each other. Internal implementations can take care of themselves. Getting interfaces, and service boundaries right is the most important.

> "_When starting out however keep a new system on the more monolithic side; getting service boundaries wrong can be costly, so waiting for things to stabilize as you get to grips with a new domain is sensible._"
