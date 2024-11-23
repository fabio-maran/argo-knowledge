# Chapter Overview and Objectives

Embarking on the journey of exploring Argo and its powerful capabilities in Kubernetes workflow management requires a solid foundation in key concepts. This chapter lays the groundwork by focusing on essential concepts that will enhance your comprehension of Argo and its functionalities.

By the end of this chapter, you should be able to:

- Explain key Argo concepts.
- Present the Argo suite’s use cases.
- Identify the role of Kubernetes.
- Install Kubernetes to work with the Argo suite.

## What Is GitOps?

GitOps embodies a set of principles that form the backbone of modern software delivery practices. At its core, GitOps hinges on five key aspects, each contributing to a streamlined and efficient development and deployment process.

## Core Elements

### Declarative configuration
First and foremost is the principle of declarative configuration. This implies a departure from the traditional imperative style of issuing specific commands. Instead, GitOps centers around expressing the desired end state of a system, allowing developers to declare intentions rather than prescribe exact actions. For instance, specifying the desire for three containers for a given application prompts automated agents to adjust the current state accordingly, potentially terminating existing containers to align with the declared configuration.

### Immutable storage
Git, in the context of GitOps, serves as more than just a version-controlled storage solution; it represents immutable storage. While Git is the predominant source control system, the principles of GitOps are adaptable to other version control systems as well. The immutability aspect underscores the idea that once a configuration is committed to Git, it becomes a static reference point, aiding in reproducibility and traceability. It is also often referred to as the source of truth.

### Automation
Automation is a cornerstone of GitOps, emphasizing the importance of eliminating manual interventions post-commit to the version control system. The moment changes are integrated into the VCS, the baton is passed to software agents. 

### Software agents
These agents play a pivotal role in executing the necessary actions to realize the newly declared configuration. The process involves assessing the disparity between the existing system state and the desired state specified in the version control, encapsulating the essence of GitOps' closed-loop nature.

### Closed loop
Closed loop, in the GitOps paradigm, encapsulates the continuous feedback loop between the actual and desired states of a system. It signifies that the automated actions taken by software agents are not arbitrary but are a direct response to the evolving configuration stored in the version control. The closed loop mechanism ensures that the system perpetually converges towards the declared state, fostering consistency and predictability.

## What Is Argo?
Argo is a set of Kubernetes-native tools that enhance the workflow management capabilities of Kubernetes. It includes Argo Continuous Delivery (CD), Argo Workflows for running complex jobs, Argo Events for event-based dependency management, and Argo Rollouts for progressive delivery. These tools are designed to help you automate and manage tasks in a Kubernetes environment, making it easier to deploy, update, and manage applications.

Let’s discuss them in more detail.

## Argo Continuous Delivery (CD)
Argo CD is a declarative, GitOps Continuous Delivery tool for Kubernetes. It helps you apply manifest from repo to cluster, and continuously monitors the repo (GitOps). Typically used for infrastructure and application deployment. It provides blue-green and canary update strategies, integrates with service meshes and ingress controllers to shape traffic, and automates promotion and rollback based on analysis. It is used to safely deploy artifacts into Production.

## Argo Workflows
Argo Workflows, as an extension of the Kubernetes API, introduces a new Workflow CRD, providing companies with a highly adaptable batch resource akin to a Kubernetes Job. This extensibility renders Workflows versatile and applicable across various domains, with a particular spotlight on its efficacy in Machine Learning (ML) and Data pipelines. Leveraging Argo Workflows in these contexts has become a strategic move for numerous companies, unraveling its potential in orchestrating complex processes seamlessly.

At its core, Argo Workflows operate on a unique set of characteristics and use cases. Each step within a workflow manifests as a pod, contributing to the modularity and scalability of the overall process. This design allows for streamlined parallelism and efficient resource utilization. Predominantly, Argo Workflows find their sweet spot in data processing and automation scenarios, exemplified by the fan-out fan-in pattern. This pattern enables the workflow to distribute tasks widely, execute them concurrently, and then consolidate the results, making Argo Workflows a robust choice for scenarios demanding intricate data manipulation and automated processes.

## Argo Events
Argo Events is an event-driven workflow automation framework for Kubernetes that helps you trigger Kubernetes objects, Argo Workflows, serverless workloads, and other processes in response to events from various sources such as webhooks, S3, schedules, messaging queues, GCP PubSub, and more. It supports events from over 20 event sources and allows you to customize business-level constraint logic for workflow automation.

Argo Events is composed of two main components: Triggers and Event Sources. Triggers are responsible for executing actions when an event occurs, while Event Sources are responsible for generating events.

Some of the use cases of Argo Events include automating research workflows, designing a complete CI/CD pipeline, and automating everything by combining Argo Events, Workflows & Pipelines, CD, and Rollouts.

## Argo Rollouts
Argo Rollouts is a progressive delivery controller for Kubernetes. It was born out of necessity due to Kubernetes’ lack of more sophisticated deployment strategies. It helps you apply manifest from repo to cluster, and continuously monitors the repo (GitOps). Typically used for infrastructure and application deployment. It provides blue-green and canary update strategies, integrates with service meshes and ingress controllers to shape traffic, and automates promotion and rollback based on analysis. It is used to safely deploy artifacts into Production.

## Benefits of Using Argo
Using Argo for continuous delivery offers several benefits. We will now explore some of them.

Argo is a popular open source tool that brings the practicality of GitOps to anyone who uses Kubernetes. By enabling GitOps, Argo can enhance the robustness, security, and reliability of Kubernetes environments. This technical practice can be highly beneficial to DevOps teams, improving their efficiency.

Argo is designed from the ground up for a modern containerized environment. Argo CD as an example is equipped with a powerful GUI and CLI, enabling all seniority levels of engineers to work with it and implement highly sophisticated custom solutions. Argo Rollouts on the other hand supports progressive delivery strategies like canary and blue-green deployments, which are difficult to implement in plain Kubernetes.

The automation provided by Argo speeds up the entire process of pushing new features, leading to faster and more frequent deployments. If any issues are detected based on defined metrics, the deployment can be automatically rolled back to the previous working deployment, allowing for faster error resolution.

One of the benefits of using Git and GitOps principles is the built-in auditing, which gives you the benefit of having the entire history of your software tracked over time. Argo makes it easy to specify, schedule, and coordinate the running of complex workflows and applications on Kubernetes.

Argo's integration with other Cloud Native Computing Foundation (CNCF) projects is a significant advantage. It uses or integrates with CNCF projects like gRPC, Prometheus, NATS, Helm, and CloudEvents. This integration allows for seamless interoperability and enhanced functionality within the cloud native ecosystem. For instance, Prometheus can be used for monitoring and alerting purposes, while Helm can help manage Kubernetes applications. NATS can provide a high-performance messaging system, and CloudEvents can offer a standard way to define the format of event data in a consistent way across services, platforms, and systems. Therefore, by using Argo, you can leverage the benefits of these CNCF projects, leading to more robust, scalable, and efficient cloud native applications.

Please note that we will delve deeper into each of these topics in the subsequent chapters.


