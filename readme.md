# Azure AZ-900: Microsoft Azure Fundamentals Exam Prep 2023

## Describe cloud concepts (25-30%)
## Describe cloud computing
-- define cloud computing: some computer

-- describe the shared responsibility model

<img width="1356" alt="shared-responsibility-model" src="https://github.com/ju4nmoreno/Azure-notes/assets/11647634/ad37e65b-b697-43cc-999f-893c11caa40d">

-- define cloud models, including public, private, and hybrid
- <b>Public:</b> "the public cloud is defined a computing services offered by third-partproviders over the public Internet, making them available to anyone who wants to use or purchase them".
- <b>Private:</b> "The private cloud is defined as computing services offered either over the Internet or a private internal network and only to select users instead of general public."
- <b>Hybrid:</b> "A hybrid cloud... is a computing environment that combines a private cloud with a public cloud."

-- identify appropriate use cases for each cloud model

-- describe the consumption-based model

-- compare cloud pricing model

### Describe the benefits of using cloud services
-- describe the benefits of high availability and predictability
- <b>High Availability (HA):</b> 
    - Ability of a system to remain operational to users during planned or unplanned outages.
        - Operating System scurity patches
        - Application updates
        - Hardware replacement
        - Migrating to a new hosting provider
    - Unplanned Outages
        - Hardware faile
        - Network disruptions
        - Power outages
        - Natural disasters
        - Cyber attacks
        - Software bugs
        - Poor scalisg /architecture design
    - Methods to Mitigate Planned Outagse
        - Gradual deployment strategy
            - 1-10-100-etc
        - Testing and monitoring of deployment
        - Easy rollback plan
        - Small deployments
        - Frequent deployments
        - Automation
    - Methods to Mitigate Unplanned Outages
        - Every single core component has redundancy
        - Use Azure's built-in features for availability
            - Availability Sets
            - Availability Zones
            - Cross-Region Load Balancing / Front Door
        - Constant health monitoring / probes
        - Automation
    - Methods to Mitigate Unplanned Outages
        - Strong security practices
        - be geographically distributed
        - Have a disaster recovery plan
        - Test that disaster recovery plan / fire drills!
        - Load Testing
    - High-Availability Is...
        - A conscious effort to avoid the obvious sources of downtime

- <b>Scalability</b>
    - The ability of a system ot accommodate increasing demand by adding or removing resurces as needed
    - E-commerce websites have Black Friday
    - School registration are busy in September
    - Tax systems are busy in April

- <b>The $1M Question...</b>
    - Can you epand the capacity of a sistem very easily, by adding more servers?
    - Or will it be a massive undertaking to do that?

- <b>Vertical Scaling</b>
    - Also called "scaling up" or "scaling down"
    - Adding more resources to single servers
    - Icrease the amount of memory, the number of CPUs
    - Azure - 96 vCPUs, 384 GB memory
    - (Does not improve availability)

- <b>Horizontal Scaling</b>
    - Also called "scaling out" or "scaling in"
    - adding more servers to a system
    - No limits to scaling
    - Additional complexities for lead balancing
    - (Can improve availability)

- <b>Horizontal Scaling</b>
    - Adding more resources to a system adds to cost
    - Reducing resources can reduce cost
    - Having a scalable system allows for a system to be perfectly sized
    - This optimizes the cost by reducing wasted computing resources

- <b>Elasticity</b>
    - The ability of a system to quickly and easily scale up or down the amount of resources that a system uses in response to  changing demand

- <b>Quickly and Easily</b>
    - Has to involve some sort of Automation
    - Often called "autoscaling" in cloud computing
    - The system monitors some metric (such as CPU utilization) to determine how busy a system is
    - Adds resources when it exceeds a limit for being busy
    - Remove resorces when it falls below a limit for not busy

- <b>Why Is It Needed</b>
    - More efficient and cost-effective use of resources
    - Minimizes computing "waste" - resources paid for and not used
    - Self-hosted systems tend to have a large precentage of "over-provisioned" resources for anticipated future growth

- <b>Save Here, Spend there</b>
    - Aloso have the potential to have a maximum capacity higher than you could afford if you had a static provisioning of resources

- <b>All Three Relating to High Quality Service</b>
    - Availability
        - The ability of a system to be accessible and usable by usres when they need it
    - Reliability
        The ability of a system t preform its intended function witout interruption asd with a high degree of accuray
    - Predictability

- <b>Reminder: Availability</b>
    - The ability of a system to be accessible and usable by usres when they need it

- describe the benefits of reliability and predictability in the cloud
- describe the benefits of manageability in the cloud
- describe the benefits of security and governace in the cloud
- describe the benefits of manageability in the cloud

### Describe cloud service types
- describe infrastructure as a service (IaaS)
    - These are the essential services of technology
        - Computing
        - Storage
        - Networking
    - Generally have "real world" equivalents in your own data center
    - Cloud replacement of real world things
- describe platform as a service (PaaS)
    - Cloud service providers have an opportunity to provide more than just the "basic" infrastructure
- describe software as a service (SaaS)
- identify appropriate use cases for each cloud service (IaaS, PaaS, SaaS)


-------
### Descriibe Azure compute and networking services
- compare compute types, including container instances, virtual machines (VMs), and functions
- describe VM options, including Azure Virtual Machine, Azure Virtual Machine Scale Sets, availability sets, and Azure Virtual Desktop
- describe resources required for vitual machines
- describe application hosting options, including the web Apps feature of Azure App Service. containers, and vitual machines
- describe virtual metworking, incuding the purpose of Azure Virtual Networks, Azure virtual subnets, peering, Azure DNS, Azure VPN Gateway, and Azure ExpressRoute
- define public and private endpoints

#### Getting Deep into the Technical
- Compute services ("Executing code" in the cloud)
    - Virtual Machines (VM)
        - Infrastructure as a service - IaaS
        - Take an Existing machine from your environment into the cloud - a copy
        - Windows or Linux operating systems - several of each
        - A "slice" of a physical machine shared with other customers
        - Full control over it, as if it was your machine
    - VM Scale Sets (VMSS)
        - Elasticity
        - Two or more virtual machines running the exact same code
        - with a "load balancer" in front to direct traffict randomly to one of the machines
        - Able to add more machines as demand grows (autoscaling)
        - Able to reduce machines as demand slows
        - Can handle up to 100 VMs in a single scale set
        - Can be configured to increase that to 1000 VMs in a single scale set
        - If you need more, you can create more scalesets
    - App services (Web apps)
        - A new paradigm for running code in the cloud
        - Give your code and configuration to Azure, and they will run it
        - Promise of performance but no access to hardware
        - Platform as a Service (PaaS)
    - Azure Container Instances (ACI)
        - Another paradigm for running code in the cloud
        - Containers contain everything the app needs to run in a "container image"
        - Fastest and easiest to deploy
        - <b>Azure Container Instance (ACI)</b> - single instance, quickest way to deploy a container
    - Azure Kubernetes Services (AKS)
        - <b>Azure Kubernetes Service (AKS)</b> - runs on a cluster of servers, enterprise-grade
    - Windows Virtual Desktop
        - Desktop version of Windows that runs in the cloud
        - You software installed, your files - available from anywhere
        - Can even see your dektop on iOS and Android, or from any web browser
        - Runs on Azure
- Networking services
    - Connectivity Services
        - <b>Virtual Network</b> - emulating a physical network
        - Microsoft Global Network already exists, so a vitual network is just software configuration
        - <b>Subnet</b> - a subdivision of a virtual network, that you control, that has its own secury rules
        - <b>Virtual Private Network (VPN)</b> - connecting two netjorks as if they were on the same network, uses a Network Gateway
        - <b>ExpessRoute</b> - high-speed private connection to Azure
        - <b>DNS Services</b> - domain name resolution
    - Protection Services
        - <b>DDos Protection</b> - Distrubited Denial of Service attack protection
        - <b>Azure Firewall</b>
        - <b>Network Security Groups</b>
        - <b>Private Link</b>
    - Delivery Services
        - <b>Load Balancer</b> - destribute traffice evenly between multiple backend servers
        - <b>Application Gateway</b> - higher-level of load balancer with an optional firewall
        - <b>Content Delivery Network (CDN)</b> - stores common static files on the edge, closer to the users for (preceived) improved performance
        - <b>Azure Front Door Service</b> - a load balancer, CDN and firewall all-in-one
    - Monitoring Services
        - <b>Network Watcher</b>
        - <b>ExpressRoute Monitor</b>
        - <b>Azure Monitor</b>
- Storage services
- Database services
