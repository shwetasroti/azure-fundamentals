# AZ-900

# Understand cloud concepts (15-20%)

## Describe the benefits and considerations of using cloud services

| term | description |
|---|---|
| high availability | Occurs when multiple resources are deployed so that a system is available 99.99% of the time. For example, Azure creates availability sets for VMs to ensure that workloads are available almost all of the time. |
| scalability | Occurs when you can increase the number of VMs as more inbound requests arrives. This represents manual horizontal scaling. |
| elasticity | Occurs when your App Services web app automatically requests more computing resources during a sudden spike in traffic. It allows you to add and remove resources as needed. |
| agility | The ability to rapidly develop, test and launch software applications that drive business growth. Cloud Agility allows them to focus on other issues such as security, monitoring and analysis, instead of provisioning and maintaining the resources. |
| fault tolerance | Occurs when a state-wide power outage in a region does not affect the ability of users to access data that was deployed to a datacenter in that state. Redundancy is built into the Azure architecture so that if a region fails, a paired region at least 300 miles away takes over. |
| disaster recovery | Occurs when you are able to retrieve data after it was lost due to some type of event. |
| economies of scale | Economies of scale is the ability to do things more efficiently or at a lower-cost per unit when operating at a larger scale (e.g. the ability to acquire hardware at a lower cost than if a single user or smaller business were purchasing it, cloud providers can also make deals with local governments and utilities to get tax savings, lower pricing on power, cooling, and high-speed network connectivity between sites). |

---

| term | description |
|---|---|
| Capital Expenditure (CapEx) | CapEx is the spending of money on physical infrastructure up front, and then deducting that expense from your tax bill over time. CapEx is an upfront cost, which has a value that reduces over time.|
| Operational Expenditure (OpEx) | OpEx is spending money on services or products now and being billed for them now. You can deduct this expense from your tax bill in the same year. |

* _understand the consumption-based model_ - With OpEx, there is no upfront cost, you pay for a service or product as you use it.

## Describe the differences between Infrastructure-as-a-Service (IaaS), Platform-as-a-Service (PaaS) and Software-as-a-Service (SaaS)

* _describe Infrastructure-as-a-Service (IaaS)_ - IaaS quickly scales up and down with demand, letting you pay only for what you use. It helps you avoid the expense and complexity of buying and managing your own physical servers and other datacenter infrastructure. Each resource is offered as a separate service component, and you only need to rent a particular one for as long as you need it. A cloud computing service provider, such as Azure, manages the infrastructure, while you purchase, install, configure, and manage your own software—operating systems, middleware, and applications.
* _describe Platform-as-a-Service (PaaS)_ - PaaS is designed to support the complete web application lifecycle: building, testing, deploying, managing, and updating. PaaS allows you to avoid the expense and complexity of buying and managing software licenses, the underlying application infrastructure and middleware, container orchestrators such as Kubernetes, or the development tools and other resources. You manage the applications and services you develop, and the cloud service provider typically manages everything else.
* _describe Software-as-a-Service (SaaS)_ - Software as a service (SaaS) allows users to connect to and use cloud-based apps over the Internet. Common examples are email, calendaring, and office tools (such as Microsoft Office 365). SaaS provides a complete software solution that you purchase on a pay-as-you-go basis from a cloud service provider. You rent the use of an app for your organization, and your users connect to it over the Internet, usually with a web browser. All of the underlying infrastructure, middleware, app software, and app data are located in the service provider’s data center. The service provider manages the hardware and software, and with the appropriate service agreement, will ensure the availability and the security of the app and your data as well. SaaS allows your organization to get quickly up and running with an app at minimal upfront cost.
* _compare and contrast the three different service type_

---

|Management responsibilities| IaaS | PaaS | SaaS |
|--|--|--|--|
| Applications | X | X | |
| Data | X | X | |
| Runtime | X | | |
| Middleware | X | | |
| OS | X | | |
| Virtualization | | | |
| Servers | | | |
| Storage | | | |
| Networking | | | |

---

| | User | Cloud Provider |
|---|---|---|
|IaaS | Purchase, installation, configuration, and management of their own software operating systems, middleware, and applications. | Responsible for ensuring that the underlying cloud infrastructure (such as virtual machines, storage, and networking) is available for the user. |
|PaaS | Responsible for the development of their own applications. | Responsible for operating system management, and network and service configuration. |
|SaaS | Users just use the application software; they are not responsible for any maintenance or management of that software. | The cloud provider is responsible for the provision, management, and maintenance of the application software. |

---

## Describe the differences between public, private and hybrid cloud models

* _describe public cloud_ - The solution is managed by a provider. MOst solutions are based on a multi-tenant model with the solution run in a shared environment with customer data partitioned to provide data security. MSFT Azure is an example of a public cloud.
* _describe private cloud_ - An organization builds and maintains its own solution, either in its datacenter or hosted as dedicated resources by a solution provider. Services and infrastructure are hosted on a private network dedicated to that organization only. Government agencies and financial institutions often use the private cloud model. A private cloud requires access to be limited to one tenant A private cloud's services and infrastructure are maintained on a private network. A company can implement its own private cloud, but it is more common to subscribe to a private cloud hosted and managed by a third-party provider.
* _describe hybrid cloud_ - This combines features of public and private clouds. This provides a way to save costs by sharing less-secure solutions needs in a public cloud and keeping high-risk, high-value resources internal to the network. A hybrid cloud provides support for a feature known as cloud bursting, where internal resources meet most needs but cloud-based resources can be added to help support peak use times.
* _compare and contrast the three different cloud models_

---

| | Advantages | Disadvantages |
|---|---|---|
| Public | + High Scalability/Agility <br/>+ PAYG (No CapEx, OpEx model)<br/>+ Minimal technical knowledge required<br/>+ Lower costs — no need to purchase hardware or software, and you pay only for the service you use.<br/>+ No maintenance — your service provider provides the maintenance.<br/>+ Near-unlimited scalability — on-demand resources are available to meet your business needs.<br/>+ High reliability — a vast network of servers ensures against failure.| - May not be able to meet specific security requirements | - May not be able to meet specific compliance requirements<br/>- You don't own the hardware and may not be able to manage them as you wish |
| Private | + You have complete control<br/>+ Can meet strict security and compliance requirements <br/>+ More flexibility — your organization can customize its cloud environment to meet specific business needs.<br/>+ Improved security — resources are not shared with others, so higher levels of control and security are possible.<br/>+ High scalability — private clouds still afford the scalability and efficiency of a public cloud.| - Upfront CapEx costs<br/>- Owning equipment limits agility to scale<br/>- Requires high technical knowledge |
| Hybrid | + Advantages of both Public and Private<br/>+ Control — your organization can maintain a private infrastructure for sensitive assets.<br/>+ Flexibility — you can take advantage of additional resources in the public cloud when you need them.<br/>+ Cost-effectiveness — with the ability to scale to the public cloud, you pay for extra computing power only when needed.<br/>+ Ease — transitioning to the cloud doesn’t have to be overwhelming because you can migrate gradually — phasing in workloads over time.| - Can be more expensive than selecting one deployment model<br/>- Can be more complicated to set up and manage|

---
---

# Understand core Azure services (30-35%)

## Understand the core Azure architectural components

| term | description |
|---|---|
| Regions | A region is a geographical area on the planet containing at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network.|
| Availability Zones | Availability Zone is an isolated location inside of an Azure Region that has its own independent power source, network, and cooling. The physical and logical separation of Availability Zones within an Azure region protects applications and data from zone-level failures. Availability Zone data transfer pricing is based on Availability Zones.|
| Resource Groups | Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for resources deployed on Azure.|
| Azure Resource Manager | Azure Resource Manager is the interface for managing and organizing cloud resources. Think of Resource Manager as a way to deploy cloud resources.|
| benefits and usage of core Azure architectural components | |

## Describe some of the core products available in Azure

| Compute | |
|---|---|
| Virtual Machines | Windows or Linux virtual machines (VMs) hosted in Azure |
| Virtual Machine Scale Sets | Scaling for Windows or Linux VMs hosted in Azure |
| App Service | PaaS offerings to build, deploy, and scale enterprise-grade web, mobile, and API apps. |
| Azure Functions | An event-driven, serverless compute service |
| Azure Container Instances (ACI) | Run Docker containers on-demand in a managed, serverless Azure environment |
| Azure Kubernetes Service (AKS) | to deploy and manage containerized applications |

| Networking | |
|---|---|
| Virtual Network | Connects VMs to incoming Virtual Private Network (VPN) connections |
| Load Balancer | Balances inbound and outbound connections to applications or service endpoints. An Open System Interonnection (OSI) layer 4 load balancer that routes traffic based on source adn destination IP addres adn port but does not support routing based on URL. It can be configured to support incoming Internet traffic and internal VM traffic. |
| VPN Gateway | Accesses Azure Virtual Networks through high-performance VPN gateways. Azure VPN Gateway enables you to establish secure, cross-premises connectivity between your virtual network within Azure and on-premises IT infrastructure. |
| Application Gateway | Optimizes app server farm delivery while increasing application security. A web load balancer that supports traffic balancing across multiple Application Zones. It acts as an Open System Interonnection (OSI) level 7 load balancer and lets you route traffic to a server pool based on the incoming URL. Application Gateway can scale automatically based on changing demands. |
| Content Delivery Network | Delivers high-bandwidth content to customers globally. CDN caches information on point-of-presence edge servers, providing for efficient delivery and minimizing latency. It helps to minimize the load on web content servers but does not provide load balancing. |

| Feature | Description | When to use |
|---|---|---|
| Azure Files | Access is provided to other VMs, as well as on-prem, through use of the Server Message Block (SMB) protocol, REST, and native client libraries. Provides an SMB interface, client libraries, and a REST interface that allows access from anywhere to stored files. | You want to "lift and shift" an application to the cloud which already uses the native file system APIs to share data between it and other applications running in Azure. You want to store development and debugging tools that need to be accessed from many virtual machines. |
| Azure Blobs | Designed for storing very large quantities of unstructured data. Outside access to application data is supported, but data is stored and accessed as block blobs. Provides client libraries and a REST interface that allows unstructured data to be stored and accessed at a massive scale in block blobs. Also supports Azure Data Lake Storage Gen2 for enterprise big data analytics solutions. | You want your application to support streaming and random access scenarios. You want to be able to access application data from anywhere. You want to build an enterprise data lake on Azure and perform big data analytics. |
| Azure Disks | Stores data as a virtual hard disk (VHD) that is available to the VM to which the disk is attached. This storage product does not provide any outside access. Provides client libraries and a REST interface that allows data to be persistently stored and accessed from an attached virtual hard disk. | You want to lift and shift applications that use native file system APIs to read and write data to persistent disks. You want to store data that is not required to be accessed from outside the virtual machine to which the disk is attached. |
| Archive Storage | This is provided as a low-cost storage option for data that is rarely accessed. | You want to store logs that you don't need quick access to. |

| Databases | |
|---|---|
| CosmosDB | Globally distributed database that supports NoSQL options |
| Azure Database for MySQL | A relational database service powered by the MySQL community edition. It's a fully managed database as a service offering that can handle mission-critical workloads with predictable performance and dynamic scalability. |
| Azure Database for PostgreSQL | A relational database service based on the open-source Postgres database engine. It's a fully managed database-as-a-service offering that can handle mission-critical workloads with predictable performance, security, high availability, and dynamic scalability. It's available in two deployment options, as a single server and as a Hyperscale (Citus) cluster. The Hyperscale (Citus) option horizontally scales queries across multiple machines using sharding, and serves applications that require greater scale and performance. |
| Azure SQL Database | Fully managed relational database with auto-scale, integral intelligence, and robust security |
| Azure Database Migration Service | Migrates your databases to the cloud with no application code changes |

* _describe the Azure Marketplace and its usage scenarios_ - The Marketplace allows customers to find, try, purchase, and provision applications and services from hundreds of leading service providers, all certified to run on Azure. Azure Marketplace is a service on Azure that helps connect end users with Microsoft partners, independent software vendors (ISVs), and start-ups that are offering their solutions and services, which are optimized to run on Azure.

## Describe some of the solutions available on Azure

### Internet of Things (IoT)

| term | description |
|---|---|
| IoT Hub | A PaaS solution that requires you to write code to connect to IoT devices.|
| IoT Central | A global IoT SaaS solution which provides the means to connect to, monitor, and manage IoT resources. IoT Central is a SaaS solution that does not require any development experience. An application is completely hosted by MSFT, which eliminates the need for you to manage an IoT application.|

### Big Data and Analytics

| term | description |
|---|---|
| SQL Data Warehouse | Run analytics at a massive scale using a cloud-based Enterprise Data Warehouse (EDW) that leverages massive parallel processing (MPP) to run complex queries quickly across petabytes of data. |
| HDInsight | An open-source enterprise-level analytics service that provides for fast and cost-effective processing of massive amounts of data. HDInsight can be used to analyze streaming or historic data. Scenarios for using HDInsight include extract, transform, and load (ETL) batch processing, interactive queries on data warehouses, and processing streams of Internet of Things (IOT) data. HDInsight is a managed Hadoop service that allows you to process batches in Hadoop clusters by using R, Python, SQL, Scala, and Java.|
| Data Lake Analytics | An on-demand analytics service that is optimized for processing data in Data Lake Store. You use U-SQL to process batches. Integrates with Azure Data Lake Store, Azure Storage blobs, Azure SQL Database, and Azure Synapse. Pricing model is per-job.|
| Azure Databricks | An Apache Spark-based analytics platform. You can think of it as "Spark as a service." It's the easiest way to use Spark on the Azure platform. It manages the Spark cluster for you.|

### Artificial Intelligence (AI)

| term | description |
|---|---|
| Azure Machine Learning Service | A data science solution that enables computers to predict outcomes and trends without being explicitly programmed. It is a cloud service to train, deploy, automate, and manage machine learning models. It is designed to let you start training on a local computer and then scale out to the cloud. Machine learning models created in Machine Learning Studio cannot be deployed or managed by Azure Machine Learning Service.|
| Azure Machine Learning Studio | Gives you a collaborative drag-and-drop visual workspace to work with machine learning solutions without the need to write any code. It allows you to use built-in algorithms, not write custom algorithms. You can build, test, and deploy predictive analytics solutions on your data. Machine Learning Studio solutions are managed in Machine Learning Studio and are only deployed as web services. This makes the model you create accessible to others.|

### Serverless computing

| term | description |
|---|---|
| Azure Functions | Provides a solution for building highly reliable and secure serverless apps suppporting multiple programming languages. You can build apps using simple serverless functions with the ability to scale as needed to meet demand. It enables you to focus on building apps without the concerns for server resources.|
| Logic Apps | A cloud service designed to help you automate and orchestrate tasks, workflows, and business processes. Logic Apps is a serverless solution that lets you connect and coordinate systems and applications.| 
| Event Grid | Allows you to easily build applications with event-based architectures. It's a fully-managed, intelligent event routing service that uses a publish-subscribe model for uniform event consumption. |

### DevOps solutions

| term | description |
|---|---|
| Azure DevOps | provides version control, reporting, requirements management, project management, automated builds, lab management, testing and release management capabilities. It covers the entire application lifecycle, and enables DevOps capabilities. |
| Azure DevTest Labs | Creates labs consisting of pre-configured bases or Azure Resource Manager templates. These have all the necessary tools and software that you can use to create environments. You can create environments in a few minutes, as opposed to hours or days. |

* _describe the benefits and outcomes of using Azure solutions_

## Understand Azure management tools

| term | description |
|---|---|
| Azure Portal | Azure CLI is a cross-platform command-line program that connects to Azure and executes administrative commands on Azure resources. Cross-platform means that it can be run on Windows, Linux, or macOS. |
| Azure Powershell | Azure PowerShell is a module that you add to Windows PowerShell or PowerShell Core that enables you to connect to your Azure subscription and manage resources. |
| Azure CLI | The Azure command-line interface (CLI) is Microsoft's cross-platform command-line experience for managing Azure resources. The Azure CLI is designed to be easy to learn and get started with, but powerful enough to be a great tool for building custom automation to use Azure resources.
| Cloud Shell | Azure Cloud Shell is an interactive, authenticated, browser-accessible shell for managing Azure resources. It provides the flexibility of choosing the shell experience that best suits the way you work, either Bash or PowerShell. |
| Azure Advisor | Advisor is a personalized cloud consultant that helps you follow best practices to optimize your Azure deployments. It analyzes your resource configuration and usage telemetry and then recommends solutions that can help you improve the cost effectiveness, performance, high availability, and security of your Azure resources. |

# Understand security, privacy, compliance, and trust (25-30%)

## Understand securing network connectivity in Azure

| term | description |
|---|---|
| Network Security Groups (NSG) | NSGs operate at layers 3 & 4, and provide a list of allowed and denied communication to and from network interfaces and subnets. NSGs are fully customizable, and give you the ability to fully lock down network communication to and from your virtual machines. By using NSGs, you can isolate applications between environments, tiers, and services. |
| Application Security Groups (ASG) | An application security group is a logical collection of virtual machines (NICs). You join virtual machines to the application security group, and then use the application security group as a source or destination in NSG rules. |
| User Defined Routes (UDR) | Azure routes traffic between all subnets within a virtual network, by default. You can create your own routes to override Azure's default routing. The ability to create custom routes is helpful if, for example, you want to route traffic between subnets through a network virtual appliance (NVA). |
| Azure Firewall | Azure Firewall is a managed, cloud-based, network security service that protects your Azure Virtual Network resources. It is a fully stateful firewall as a service with built-in high availability and unrestricted cloud scalability. Azure Firewall provides inbound protection for non-HTTP/S protocols. Examples of non-HTTP/S protocols include: Remote Desktop Protocol (RDP), Secure Shell (SSH), and File Transfer Protocol (FTP). It also provides outbound, network-level protection for all ports and protocols, and application-level protection for outbound HTTP/S. |
| Azure DDoS Protection | DDoS Protection leverages the scale and elasticity of Microsoft’s global network to bring DDoS mitigation capacity to every Azure region. The Azure DDoS Protection service protects your Azure applications by scrubbing traffic at the Azure network edge before it can impact your service's availability. Within a few minutes of attack detection, you are notified using Azure Monitor metrics. |

## Describe core Azure Identity services

| term | description |
|---|---|
| Authentication (Who are you?) | The process of establishing the identity of a person or service looking to access a resource. It involves the act of challenging a party for legitimate credentials, and provides the basis for creating a security principal for identity and access control use. It establishes if they are who they say they are. |
| Authorization (What are you allowed to do?) | The process of establishing what level of access an authenticated person or service has. It specifies what data they're allowed to access and what they can do with it. |
| Azure Active Directory | Azure AD is a cloud-based identity service. It has built in support for synchronizing with your existing on-premises Active Directory or can be used stand-alone. This means that all your applications, whether on-premises, in the cloud (including Office 365), or even mobile can share the same credentials. Administrators and developers can control access to internal and external data and applications using centralized rules and policies configured in Azure AD. To manage resources in Azure AD, such as users, groups, and domains, there are several Azure AD administrator roles. |
| Azure Multi-Factor Authentication | Multi-factor authentication (MFA) provides additional security for your identities by requiring two or more elements for full authentication. These elements fall into three categories: <br/>  - Something you know<br/>  - Something you possess<br/>  - Something you are |

| authentication type | supports MFA | supports SSPR |
|---|---|---|
| Password | yes | yes |
| SMS |  yes | yes |
| Voice Call | yes | yes |
| App Passwords | sometimes | no |
| MSFT Authenticator | yes | yes |
| OATH Hardware token | Public Preview | yes |
| Security Questions | no | yes |
| Email address | no | yes |

## Describe security tools and features of Azure

| term | description |
|---|---|
| Azure Security Center | Security Center is a monitoring service that provides threat protection across all of your services both in Azure, and on-premises. Available in two tiers, Free (limited to assessments and recommendations only); Standard (full suite of security-related services including continious monitoring, threat detection and just-in-time access control)<br/>_Usage scenarios:_<br/>&bull; Incident Response (Detect, Assess, Diagnose)<br/>&bull; Implement Recommendations |
| Key Vault | Azure Key Vault is a secret store: a centralized cloud service for storing application secrets. Key Vault helps you control your applications' secrets by keeping them in a single central location and providing secure access, permissions control, and access logging.
| Azure Information Protection (AIP) | Azure Information Protection (sometimes referred to as AIP) is a cloud-based solution that helps an organization to classify and optionally, protect its documents and emails by applying labels. Labels can be applied automatically by administrators who define rules and conditions, manually by users, or a combination where users are given recommendations. The protection technology uses Azure Rights Management (RMS). This protection technology uses encryption, identity, and authorization policies. Similarly to the labels that are applied, protection that is applied by using Rights Management stays with the documents and emails, independently of the location—inside or outside your organization, networks, file servers, and applications. This information protection solution keeps you in control of your data, even when it is shared with other people.
| Azure Advanced Threat Protection (ATP) | Azure Advanced Threat Protection (ATP) is a cloud-based security solution that leverages your on-premises Active Directory signals to identify, detect, and investigate advanced threats, compromised identities, and malicious insider actions directed at your organization. Azure ATP enables SecOp analysts and security professionals struggling to detect advanced attacks in hybrid environments to:<br/>&bull; Monitor users, entity behavior, and activities with learning-based analytics<br/>&bull; Protect user identities and credentials stored in Active Directory<br/>&bull; Provide clear incident information on a simple timeline for fast triage<br/>&bull; Identify and investigate suspicious user activities and advanced attacks throughout the kill chain - Azure ATP identifies these advanced threats at the source throughout the entire cyber-attack kill chain:<br/>&bull;*Reconnaissance* - Identify rogue users and attackers’ attempts to gain information. Attackers are searching for information about user names, users’ group membership, IP addresses assigned to devices, resources, and more, using a variety of methods.<br/>&bull; *Compromised credentials* - Identify attempts to compromise user credentials using brute force attacks, failed authentications, user group membership changes, and other methods.<br/>&bull; *Lateral movements* - Detect attempts to move laterally inside the network to gain further control of sensitive users, utilizing methods such as Pass the Ticket, Pass the Hash, Overpass the Hash and more.<br/>&bull; *Domain dominance* - Highlighting attacker behavior if domain dominance is achieved, through remote code execution on the domain controller, and methods such as DC Shadow, malicious domain controller replication, Golden Ticket activities, and more. |

## Describe Azure governance methodologies

* _describe policies and initiatives with Azure Policy_ - Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources, so those resources stay compliant with your corporate standards and service level agreements. Azure Policy meets this need by evaluating your resources for non-compliance with assigned policies. All data stored by Azure Policy is encrypted at rest.
  * *policies* - Every policy definition has conditions under which it's enforced. And, it has a defined effect that takes place if the conditions are met. To implement these policy definitions (both built-in and custom definitions), you'll need to assign them. You can assign any of these policies through the Azure portal, PowerShell, or Azure CLI. A policy assignment is a policy definition that has been assigned to take place within a specific scope. This scope could range from a management group to a resource group.
  * *initiatives* - A collection of policy definitions that are tailored towards achieving a singular overarching goal. Initiative definitions simplify managing and assigning policy definitions. They simplify by grouping a set of policies as one single item. For example, you could create an initiative titled Enable Monitoring in Azure Security Center, with a goal to monitor all the available security recommendations in your Azure Security Center. Like a policy assignment, an initiative assignment is an initiative definition assigned to a specific scope. Initiative assignments reduce the need to make several initiative definitions for each scope. This scope could also range from a management group to a resource group. Each initiative is assignable to different scopes. One initiative can be assigned to both subscriptionA and subscriptionB.
* _describe Role-Based Access Control (RBAC)_ - Azure RBAC is a newer authorization system that provides fine-grained access management to Azure resources. RBAC includes many built-in roles, can be assigned at different scopes, and allows you to create your own custom roles. The way you control access to resources using RBAC is to create role assignments. This is a key concept to understand – it’s how permissions are enforced. A role assignment consists of three elements: security principal, role definition, and scope.
* _describe Locks_ - As an administrator, you may need to lock a subscription, resource group, or resource to prevent other users in your organization from accidentally deleting or modifying critical resources. You can set the lock level to CanNotDelete or ReadOnly. In the portal, the locks are called Delete and Read-only respectively.
* _describe Azure Advisor security assistance_ - Azure Advisor provides you with a consistent, consolidated view of recommendations for all your Azure resources. It integrates with Azure Security Center to bring you security recommendations. You can get security recommendations from the Security tab on the Advisor dashboard. Security Center helps you prevent, detect, and respond to threats with increased visibility into and control over the security of your Azure resources. It periodically analyzes the security state of your Azure resources. When Security Center identifies potential security vulnerabilities, it creates recommendations. The recommendations guide you through the process of configuring the controls you need.
* _describe Azure Blueprints_ - Simplify largescale Azure deployments by packaging key environment artifacts, such as Azure Resource Manager templates, role-based access controls, and policies, in a single blueprint definition. Easily apply the blueprint to new subscriptions and environments, and fine-tune control and management through versioning.

## Understand monitoring and reporting options in Azure

* _describe Azure Monitor_ - Azure Monitor maximizes the availability and performance of your applications and services by delivering a comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments. It helps you understand how your applications are performing and proactively identifies issues affecting them and the resources they depend on. Just a few examples of what you can do with Azure Monitor include:
  * Detect and diagnose issues across applications and dependencies with Application Insights.
  * Correlate infrastructure issues with Azure Monitor for VMs and Azure Monitor for Containers.
  * Drill into your monitoring data with Log Analytics for troubleshooting and deep diagnostics.
  * Support operations at scale with smart alerts and automated actions.
  * Create visualizations with Azure dashboards and workbooks.
* _describe Azure Service Health_ - Service Health provides you with a customizable dashboard which tracks the health of your Azure services in the regions where you use them. In this dashboard, you can track active events like ongoing service issues, upcoming planned maintenance, or relevant health advisories. When events become inactive, they get placed in your health history for up to 90 days. Finally, you can use the Service Health dashboard to create and manage service health alerts which proactively notify you when service issues are affecting you. Service Health tracks three types of health events that may impact your resources:
  * Service issues - Problems in the Azure services that affect you right now.
  * Planned maintenance - Upcoming maintenance that can affect the availability of your services in the future.
  * Health advisories - Changes in Azure services that require your attention. Examples include when Azure features are deprecated or if you exceed a usage quota.
* _understand the use cases and benefits of Azure Monitor and Azure Service Health_ - Service Health integrates with Azure Monitor to alert you via emails, text messages, and webhook notifications when your business-critical resources are impacted. Set up an activity log alert for the appropriate service health event. Route that alert to the appropriate people in your organization using Action Groups.

## Understand privacy, compliance and data protection standards in Azure

| term | description |
|---|---|
| GDPR | A regulation enforced by a government agency. It is controlled by the European Union (EU).|
| ISO | International Standard Organization (ISO) is a standards-based non-regulatory agency, based in Geneva, Switzerland.|
| NIST | A standards-based non-regulatory agency based in the US. NIST stands for National Institute of Standards and Technology.|
| Microsoft Privacy Statement | The Microsoft privacy statement explains what personal data Microsoft processes, how Microsoft processes it, and for what purposes. |
| Trust center | Trust Center is a website resource containing information and details about how Microsoft implements and supports security, privacy, compliance, and transparency in all Microsoft cloud products and services. The Trust Center is an important part of the Microsoft Trusted Cloud Initiative, and provides support and resources for the legal and compliance community. |
| Service Trust Portal | The Service Trust Portal (STP) hosts the Compliance Manager service, and is the Microsoft public site for publishing audit reports and other compliance-related information relevant to Microsoft’s cloud services. |
| Compliance Manager | Allows you to determine whether or not your services meet industry standards. Compliance Manager is a workflow within Service Trust Portal. It allows you to view a compliance score to determine how well you comply with industry standards. |
| Azure Government cloud services | Uses a physically isolated instance of Azure, but it is not because of strict government data privacy requirements. Azure Government is separate to keep government services and data separate from non-government services and data. Azure Government's datacenters are only based in the US. |
| Azure China cloud services | Maintain compliance with Chinese laws and regulations when you use Azure China cloud computing services. This physically isolated instance of Azure requires that you have an account separate from an Azure global account—the Azure China pricing is distinct. |
| Azure Germany services | Azure Germany uses a physically isolated instance of Azure to meet strict government data privacy requirements. Germany uses a dedicated trustee of customer data. A local company controls access to customer data, unless the customer grants others access to the data. |

# Understand Azure pricing and support (20-25%)

## Understand Azure subscriptions

* _describe an Azure subscription_ - An Azure subscription is a logical container used to provision resources in Microsoft Azure. It holds the details of all your resources like virtual machines, databases, etc.
* _understand the uses and options with Azure subscriptions such access control and offer types_ - Azure offers free and paid subscription options to suit different needs and requirements. The most commonly used subscriptions are:
  * Free: An Azure free subscription includes a $200 credit to spend on any service for the first 30 days, free access to the most popular Azure products for 12 months, and access to more than 25 products that are always free.
  * Pay-As-You-Go: A Pay-As-You-Go (PAYG) subscription charges you monthly for the services you used in that billing period. This subscription type is appropriate for a wide range of users, from individuals to small businesses, and many large organizations as well.
  * Enterprise Agreement: An Enterprise Agreement (EA) provides flexibility to buy cloud services and software licenses under one agreement, with discounts for new licenses and Software Assurance. It's targeted at enterprise-scale organizations.
  * Student: An Azure for Students subscription includes $100 in Azure credits to be used within the first 12 months plus select free services without requiring a credit card at sign-up. You must verify your student status through your organizational email address.

  * Every Azure Subscription Includes
    * Free access to billing and subscription support
    * Azure products and services documentation
    * Online self-help documentation
    * Community support forums

  * Purchasing Options for Azure Products and Services
    * Enterprise: Enterprise customers sign an Enterprise Agreement (EA) with Azure that commits them to spend a negotiated amount on Azure services, which they typically pay annually. Enterprise customers also have access to customized Azure pricing.
    * Web direct: Direct Web customers pay general public prices for Azure resources, and their monthly billing and payments occur through the Azure website.
    * Cloud Solution Provider: Cloud Solution Provider (CSP) typically are Microsoft partner companies that a customer hires to build solutions on top of Azure. Payment and billing for Azure usage occur through the customer's CSP.

* _understand subscription management using Management groups_

## Understand planning and management of costs

* _understand options for purchasing Azure products and services_
* _understand options around Azure Free account_ -  An Azure free subscription includes a $200 credit to spend on any service for the first 30 days, free access to the most popular Azure products for 12 months, and access to more than 25 products that are always free.
* _understand the factors affecting costs:_
  * Resource Type: Costs are resource-specific, so the usage that a meter tracks and the number of meters associated with a resource depend on the resource type.
  * Service: Azure usage rates and billing periods can differ between Enterprise, Web Direct, and Cloud Solution Provider (CSP) customers. Some subscription types also include usage allowances, which affect costs.
  * Location: Azure has datacenters all over the world. Usage costs vary between locations that offer particular Azure products, services, and resources based on popularity, demand, and local infrastructure costs.
  * Ingress and egress traffic -
    * Following Availability Zone data transfer is charged:
      * Data transfer, ingress and egress, from a VNet resource deployed in an Availability Zone to another resource in different Availability Zone in the same VNET
    * Following Availability Zone data transfer is NOT charged:
      * Data transfer between VNet resources located in same Availability Zone
      * Data transfer between a VNet resource and a Public IP address in the same Azure Region
      * Data transfer between VNet resources located in peered VNets across Availability Zones. This data transfer will be charges as per VNet peering rates.
* _understand Zones for billing purposes_ - A zone is a geographical grouping of Azure regions used to determine billing based on data trasnsfers. Billing applies to both incoming and outgoing data and varies by zone. Microsoft has defined four zones for this purpose, simply referrd to as Zone 1, Zone 2, Zone 3, and DE Zone 1. Data transfers between zones and regions in a zone are billed. Data transfers between zones in the same region are not charged. Zones do not impact any other billing factors.
  * A sub-region is the lowest level geo-location that you may select to deploy your applications and associated data. For data transfers (except CDN), the following regions correspond to Zone 1, Zone 2, Zone 3, and DE Zone 1.

| zone | regions |
|---|---|
| Zone 1 | Canada Central, Canada East, North Europe, West Europe, France Central, France South, Switzerland North, Switzerland West, UK South, UK West, Central US, East US, East US 2, US Gov Arizona, US Gov Iowa, US Gov Texas, US Gov Virginia, North Central US, South Central US, West US, West US 2, West Central US |
| Zone 2 | East Asia, Southeast Asia, Australia Central, Australia Central 2, Australia East, Australia Southeast, Central India, Japan East, Japan West, Korea Central, Korea South, South India, West India |
| Zone 3 | Brazil South, South Africa North, South Africa West, UAE Central, UAE North |
| DE Zone 1 | Germany Central, Germany Northeast |

* _understand the Pricing calculator_ - The Azure pricing calculator is a free web-based tool that allows you to input Azure services and modify properties and options of the services. It outputs the costs per service and total cost for the full estimate.
* _understand the Total Cost of Ownership (TCO) Calculator_ - If you are starting to migrate to the cloud, a useful tool you can use to predict your cost savings is the Total Cost of Ownership (TCO) calculator. TCO helps you estimate cost savings realized by mirating to Azure.
* _understand best practices for minimizing Azure costs_:
  * *performing cost analysis* -
  * *creating spending limits and quotas* - Spending limit in Azure exists to prevent spending over your credit amount. All new customers who sign up for the trial or offers that includes credits over multiple months have the spending limit turned on by default. The spending limit is $0. It can’t be changed. The spending limit isn’t available for subscription types such as Pay-As-You-Go subscriptions and commitment plans.
  * *using tags to identify cost owners* - You can use tags to group your billing data. For example, if you're running multiple VMs for different organizations, use the tags to group usage by cost center. You can also use tags to categorize costs by runtime environment, such as the billing usage for VMs running in the production environment. When exporting billing data or accessing it through billing APIs, tags are included in that data and can be used to further slice your data from a cost perspective.
  * *using Azure reservations* - Reserved instances are purchased in one-year or three-year terms, with payment required for the full term up front. After it's purchased, Microsoft matches up the reservation to running instances and decrements the hours from your reservation. Reservations can be purchased through the Azure portal. And because reserved instances are a compute discount, they are available for both Windows and Linux VMs.
  * *using Azure Advisor recommendations* - Does not allow you to determine whether or not your services meet industry standards but rather provides recommendations on high availability, cost, security, and performance. It analyzes theservices that you deploy and tries to find ways to improve the usage of those services.
* _describe Azure Cost Management_ - Azure Cost Management is another free, built-in Azure tool that can be used to gain greater insights into where your cloud money is going. You can see historical breakdowns of what services you are spending your money on and how it is tracking against budgets that you have set. You can set budgets, schedule reports, and analyze your cost areas.

## Understand the support options available with Azure

| | BASIC | DEVELOPER | STANDARD | PROFESSIONAL DIRECT | PREMIER
|---| ---|---|---|---|---|
| Scope | Available to all Microsoft Azure accounts | Microsoft Azure: Trial and non-production environments | Microsoft Azure: Production workload environments | Microsoft Azure: Business-critical dependence | All Microsoft Products, including Azure: Substantial dependence across multiple products |
| Customer<br/>Service, Self-Help and Communities | 24x7 access to billing and subscription support, online self-help, documentation, whitepapers, and support forums | 24x7 access to billing and subscription support, online self-help, documentation, whitepapers, and support forums | 24x7 access to billing and subscription support, online self-help, documentation, whitepapers, and support forums | 24x7 access to billing and subscription support, online self-help, documentation, whitepapers, and support forums | 24x7 access to billing and subscription support, online self-help, documentation, whitepapers, and support forums
| Best<br/>Practices | Access to full set of Azure Advisor recs | Access to full set of Azure Advisor recs | Access to full set of Azure Advisor recs | Access to full set of Azure Advisor recs | Access to full set of Azure Advisor recs
| Health Status<br/>and Notifications | Access to personalized Service Health Dashboard & Health API | Access to personalized Service Health Dashboard & Health API | Access to personalized Service Health Dashboard & Health API | Access to personalized Service Health Dashboard & Health API | Access to personalized Service Health Dashboard & Health API
| Technical<br/>Support | Not available | Business hours access1 to Support Engineers via email | 24x7 access to Support Engineers via email and phone | 24x7 access to Support Engineers via email and phone | 24x7 access to Support Engineers via email and phone
| Who Can<br/>Open Cases | Not available | Unlimited contacts / unlimited cases | Unlimited contacts / unlimited cases | Unlimited contacts / unlimited cases | Unlimited contacts / unlimited cases
| Third-Party<br/>Software Support | Not available | Interoperability & configuration guidance and troubleshooting | Interoperability & configuration guidance and troubleshooting | Interoperability & configuration guidance and troubleshooting | Interoperability & configuration guidance and troubleshooting
|Case Severity/<br/>Response Times | Not available | Minimal business impact (Sev C): <8 business hours1 | Minimal business impact (Sev C): <8 business hours1 Moderate business impact (Sev B): <4 hours Critical business impact (Sev A): <1 hour |  Minimal business impact (Sev C): <4 business hours1 Moderate business impact (Sev B): <2 hours Critical business impact (Sev A): <1 hour |  Minimal business impact (Sev C): <4 business hours1 Moderate business impact (Sev B): <2 hours Critical business impact (Sev A): <1 hour <15 minutes (with Azure Rapid Response or Azure Event Management)
| Architecture<br/>Support | Not available | General guidance | General guidance | Architectural guidance based on best practice delivered by ProDirect Delivery Manager | Customer specific architectural support such as design reviews, performance tuning, configuration and implementation assistance delivered by Microsoft Azure technical specialists. |
| Operations<br/>Support | Not available | Not available | Not available | Onboarding services, service reviews, Azure Advisor consultations | Technical account manager-led service reviews and reporting |
| Training | Not available | Not available | Not available | Azure Engineering-led web seminars | Azure Engineering-led web seminars, on-demand training |
| Proactive<br/>Guidance | Not available | Not available | Not available | ProDirect Delivery Manager | Designated Technical Account Manager |
| Launch<br/>Support | Not available | Not available | Not available | Not available | Azure Event Management (available for additional fee) |
| Pricing | Not available | $29/mo | $100/mo | $1,000/mo | Contact us |

* _understand how to open a support ticket_ - Submit a support request from the Azure Portal. Simply select "Support" from the menu bar or open the "Help + support" hub.
* _understand available support channels outside of support plan channels_ - Available Support Channels outside of Support Plan Channels
  * Azure Knowledge Center
  * Microsoft Developer Network (MSDN) Forums
  * Stack Overflow
  * Server Fault
  * Azure Feedback Forums
  * Twitter
* _describe the Knowledge Center_ - The Azure Knowledge Center is a searchable database that contains answers to common support questions, from a community of Azure experts, developers, customers, and users. You can browse through all responses within the Azure Knowledge Center. Find specific solutions by entering keyword search terms into the text-entry field and further refine your search results by selecting products or tags from the lists provided by two dropdown lists.

## Describe Azure Service Level Agreements (SLAs)

* _describe a Service Level Agreement (SLA)_ - Formal documents called Service-Level Agreements (SLAs) capture the specific terms that define the performance standards that apply to Azure. SLAs describe Microsoft's commitment to providing Azure customers with specific performance standards. There are SLAs for individual Azure products and services. SLAs also specify what happens if a service or product fails to perform to a governing SLA's specification. Note: Azure does not provide SLAs for most services under the Free or Shared tiers.
* _understand Composite SLAs_ - When combining SLAs across different service offerings, the resultant SLA is a called a Composite SLA. The resulting composite SLA can provide higher or lower uptime values, depending on your application architecture.
* _understand how to determine an appropriate SLA for an application_ - There are three key characteristics of SLAs for Azure products and services:
  * Performance Targets
  * Uptime and Connectivity Guarantees
  * Service credits (percentage of the applicable monthly service fees credited to you if a service fails to meet uptime guarantee)

## Understand service lifecycle in Azure

| term | description |
|---|---|
| Public | This means that an Azure feature is available to all Azure customers for evaluation purposes. These previews can be turned on through the preview features page as detailed below.|
| Private | This means that an Azure feature is available to *specific* Azure customers for evaluation purposes. This is typically by invite only and issued directly by the product team responsible for the feature or service.|
| General Availability (GA) | Once a feature has been evaluated and tested successfully, it might be released to customers as part of Azure's default product set. This release is referred to as General Availability (GA). |

* _understand how to monitor feature updates and product changes_ - The Azure portal "What's New" link on the ? help menu provides a list of recent updates you can periodically check to see what's changed in Azure. Alternatively, you can use the Azure Updates page (https://azure.microsoft.com/updates/).
