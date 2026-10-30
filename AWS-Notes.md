# ☁️🚀 AWS — Complete Notes

<p align="center">

**IAM • EC2 • S3 • VPC • RDS • Route 53 • Lambda • Elastic Beanstalk**

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazon-aws)
![Cloud Computing](https://img.shields.io/badge/Cloud-Computing-blue?style=for-the-badge)
![DevOps Learning](https://img.shields.io/badge/DevOps-Learning-success?style=for-the-badge)

</p>

---

## 📖 About These Notes

This single file covers **8 core AWS services** in simple English.

Every service has the same flow:

```text
1. 📖 Definition and Simple Meaning
2. 🤔 Why do we use it?
3. 🧱 Concepts and sub-topics
4. 💻 Examples and diagrams
5. 🏗️ Real example
6. 📌 Quick Revision + 🧠 One-Line Memory + 🗺️ Learning Map + ⭐ Final Memory
```

## 📚 Table of Contents

> Click a part to open its list of topics.

<details>
<summary><b>☁️ PART 1 — AWS BASICS — Cloud and AWS Introduction</b></summary>

- [1.1 ☁️ What is AWS?](#11--what-is-aws)
- [1.2 🤔 Why Do We Use AWS?](#12--why-do-we-use-aws)
- [1.3 🧩 Cloud Service Models](#13--cloud-service-models)
- [1.4 🌍 AWS Global Infrastructure](#14--aws-global-infrastructure)
- [1.5 🖥️ Ways to Access AWS](#15--ways-to-access-aws)
- [1.6 🤝 Shared Responsibility Model](#16--shared-responsibility-model)
- [1.7 💰 AWS Pricing Basics](#17--aws-pricing-basics)
- [1.8 📚 Services Covered in These Notes](#18--services-covered-in-these-notes)

</details>

<details>
<summary><b>🔐 PART 2 — IAM — Identity and Access Management</b></summary>

- [2.1 🔐 What is IAM?](#21--what-is-iam)
- [2.2 🤔 Why Do We Use IAM?](#22--why-do-we-use-iam)
- [2.3 🧰 What Does IAM Provide?](#23--what-does-iam-provide)
- [2.4 🧱 IAM Basic Concepts](#24--iam-basic-concepts)
- [2.5 👑 Root User](#25--root-user)
- [2.6 👤 IAM User](#26--iam-user)
- [2.7 👥 IAM Group](#27--iam-group)
- [2.8 📜 IAM Policy](#28--iam-policy)
- [2.9 ⚖️ Policy Evaluation Logic](#29--policy-evaluation-logic)
- [2.10 🎭 IAM Role](#210--iam-role)
- [2.11 📊 IAM User vs Group vs Role](#211--iam-user-vs-group-vs-role)
- [2.12 🔑 Access Keys](#212--access-keys)
- [2.13 📲 MFA](#213--mfa)
- [2.14 🔒 Password Policy](#214--password-policy)
- [2.15 🌐 Identity Federation](#215--identity-federation)
- [2.16 🛡️ Permissions Boundary and SCP](#216--permissions-boundary-and-scp)
- [2.17 📊 IAM Monitoring and Reports](#217--iam-monitoring-and-reports)
- [2.18 ✅ IAM Best Practices](#218--iam-best-practices)
- [2.19 🏗️ Real Example: EC2 Accessing S3 Using a Role](#219--real-example-ec2-accessing-s3-using-a-role)
- [📌🧠 IAM Quick Revision](#-iam-quick-revision)
- [🧠⚡ IAM One-Line Memory](#-iam-one-line-memory)
- [🗺️ IAM Learning Map](#-iam-learning-map)
- [⭐ IAM Final Memory](#-iam-final-memory)

</details>

<details>
<summary><b>🖥️ PART 3 — EC2 — Elastic Compute Cloud</b></summary>

- [3.1 🖥️ What is EC2?](#31--what-is-ec2)
- [3.2 🤔 Why Do We Use EC2?](#32--why-do-we-use-ec2)
- [3.3 🧰 What Does EC2 Provide?](#33--what-does-ec2-provide)
- [3.4 🖥️ EC2 Instance](#34--ec2-instance)
- [3.5 📦 AMI](#35--ami)
- [3.6 ⚙️ Instance Type](#36--instance-type)
- [3.7 📋 Launch Template](#37--launch-template)
- [3.8 🔑 Key Pair](#38--key-pair)
- [3.9 🛡️ Security Group](#39--security-group)
- [3.10 💾 EBS](#310--ebs)
- [3.11 📍 Elastic IP](#311--elastic-ip)
- [3.12 ⚖️ Load Balancer](#312--load-balancer)
- [3.13 🎯 Target Group](#313--target-group)
- [3.14 📈 Auto Scaling Group (ASG)](#314--auto-scaling-group-asg)
- [3.15 📌 Placement Groups](#315--placement-groups)
- [3.16 💰 EC2 Pricing Models](#316--ec2-pricing-models)
- [3.17 🏗️ Real Example: Web Server on EC2](#317--real-example-web-server-on-ec2)
- [📌🧠 EC2 Quick Revision](#-ec2-quick-revision)
- [🧠⚡ EC2 One-Line Memory](#-ec2-one-line-memory)
- [🗺️ EC2 Learning Map](#-ec2-learning-map)
- [⭐ EC2 Final Memory](#-ec2-final-memory)

</details>

<details>
<summary><b>🪣 PART 4 — S3 — Simple Storage Service</b></summary>

- [4.1 ☁️ What is S3?](#41--what-is-s3)
- [4.2 🤔 Why Do We Use S3?](#42--why-do-we-use-s3)
- [4.3 🧰 What Does S3 Provide?](#43--what-does-s3-provide)
- [4.4 🧱 S3 Basic Concepts](#44--s3-basic-concepts)
- [4.5 💾 S3 Storage Classes](#45--s3-storage-classes)
- [4.6 🔄 Versioning](#46--versioning)
- [4.7 🔐 S3 Permissions and Security](#47--s3-permissions-and-security)
- [4.8 🔒 Encryption](#48--encryption)
- [4.9 🛡️ S3 Security vs Encryption](#49--s3-security-vs-encryption)
- [4.10 🌐 S3 Static Website Hosting](#410--s3-static-website-hosting)
- [4.11 ♻️ S3 Lifecycle Management](#411--s3-lifecycle-management)
- [4.12 🔄 S3 Replication](#412--s3-replication)
- [4.13 🚀 S3 Transfer Acceleration](#413--s3-transfer-acceleration)
- [4.14 🧩 Multipart Upload](#414--multipart-upload)
- [4.15 🔔 S3 Event Notifications](#415--s3-event-notifications)
- [4.16 💰 S3 Pricing](#416--s3-pricing)
- [📌🧠 S3 Quick Revision](#-s3-quick-revision)
- [🧠⚡ S3 One-Line Memory](#-s3-one-line-memory)
- [🗺️ S3 Learning Map](#-s3-learning-map)
- [⭐ S3 Final Memory](#-s3-final-memory)

</details>

<details>
<summary><b>🌐 PART 5 — VPC — Virtual Private Cloud</b></summary>

- [5.1 🌐 What is VPC?](#51--what-is-vpc)
- [5.2 🤔 Why Do We Use VPC?](#52--why-do-we-use-vpc)
- [5.3 🧰 What Does VPC Provide?](#53--what-does-vpc-provide)
- [5.4 🏠 Default VPC vs Custom VPC](#54--default-vpc-vs-custom-vpc)
- [5.5 📏 CIDR Block](#55--cidr-block)
- [5.6 🧩 Subnet](#56--subnet)
- [5.7 🛣️ Route Table](#57--route-table)
- [5.8 🚪 Internet Gateway (IGW)](#58--internet-gateway-igw)
- [5.9 🔁 NAT Gateway](#59--nat-gateway)
- [5.10 🛡️ Security Group](#510--security-group)
- [5.11 🚧 Network ACL (NACL)](#511--network-acl-nacl)
- [5.12 ⚖️ Security Group vs NACL](#512--security-group-vs-nacl)
- [5.13 🔗 VPC Peering](#513--vpc-peering)
- [5.14 🔌 VPC Endpoints](#514--vpc-endpoints)
- [5.15 🏢 Transit Gateway](#515--transit-gateway)
- [5.16 🔐 VPN and Direct Connect](#516--vpn-and-direct-connect)
- [5.17 📊 VPC Flow Logs](#517--vpc-flow-logs)
- [5.18 🏰 Bastion Host](#518--bastion-host)
- [5.19 🏗️ Real Example: Public + Private Architecture](#519--real-example-public--private-architecture)
- [📌🧠 VPC Quick Revision](#-vpc-quick-revision)
- [🧠⚡ VPC One-Line Memory](#-vpc-one-line-memory)
- [🗺️ VPC Learning Map](#-vpc-learning-map)
- [⭐ VPC Final Memory](#-vpc-final-memory)

</details>

<details>
<summary><b>🗄️ PART 6 — RDS — Relational Database Service</b></summary>

- [6.1 🗄️ What is RDS?](#61--what-is-rds)
- [6.2 🤔 Why Do We Use RDS?](#62--why-do-we-use-rds)
- [6.3 🧰 What Does RDS Provide?](#63--what-does-rds-provide)
- [6.4 🧱 RDS Basic Concepts](#64--rds-basic-concepts)
- [6.5 🛢️ Supported Database Engines](#65--supported-database-engines)
- [6.6 ⚙️ DB Instance Classes](#66--db-instance-classes)
- [6.7 💾 RDS Storage](#67--rds-storage)
- [6.8 🛡️ Multi-AZ Deployment](#68--multi-az-deployment)
- [6.9 📖 Read Replicas](#69--read-replicas)
- [6.10 ⚖️ Multi-AZ vs Read Replica](#610--multi-az-vs-read-replica)
- [6.11 📸 Backups and Snapshots](#611--backups-and-snapshots)
- [6.12 🔐 RDS Security](#612--rds-security)
- [6.13 🔒 Encryption](#613--encryption)
- [6.14 📊 Monitoring](#614--monitoring)
- [6.15 🔌 RDS Proxy](#615--rds-proxy)
- [6.16 🌟 Amazon Aurora](#616--amazon-aurora)
- [6.17 💰 RDS Pricing](#617--rds-pricing)
- [6.18 🏗️ Real Example: EC2 + RDS Architecture](#618--real-example-ec2--rds-architecture)
- [📌🧠 RDS Quick Revision](#-rds-quick-revision)
- [🧠⚡ RDS One-Line Memory](#-rds-one-line-memory)
- [🗺️ RDS Learning Map](#-rds-learning-map)
- [⭐ RDS Final Memory](#-rds-final-memory)

</details>

<details>
<summary><b>🧭 PART 7 — Route 53 — DNS Service</b></summary>

- [7.1 🧭 What is Route 53?](#71--what-is-route-53)
- [7.2 🤔 Why Do We Use Route 53?](#72--why-do-we-use-route-53)
- [7.3 🧰 What Does Route 53 Provide?](#73--what-does-route-53-provide)
- [7.4 🧠 DNS Basics](#74--dns-basics)
- [7.5 🏷️ Domain Registration](#75--domain-registration)
- [7.6 📂 Hosted Zone](#76--hosted-zone)
- [7.7 📄 DNS Records](#77--dns-records)
- [7.8 ⏱️ TTL](#78--ttl)
- [7.9 🔗 CNAME Record](#79--cname-record)
- [7.10 ⭐ Alias Record](#710--alias-record)
- [7.11 🔀 Routing Policies](#711--routing-policies)
- [7.12 ❤️ Health Checks](#712--health-checks)
- [7.13 🔁 Route 53 Resolver](#713--route-53-resolver)
- [7.14 💰 Route 53 Pricing](#714--route-53-pricing)
- [7.15 🏗️ Real Example: Domain to Load Balancer](#715--real-example-domain-to-load-balancer)
- [📌🧠 Route 53 Quick Revision](#-route-53-quick-revision)
- [🧠⚡ Route 53 One-Line Memory](#-route-53-one-line-memory)
- [🗺️ Route 53 Learning Map](#-route-53-learning-map)
- [⭐ Route 53 Final Memory](#-route-53-final-memory)

</details>

<details>
<summary><b>⚡ PART 8 — Lambda — Serverless Compute</b></summary>

- [8.1 ⚡ What is Lambda?](#81--what-is-lambda)
- [8.2 🤔 Why Do We Use Lambda?](#82--why-do-we-use-lambda)
- [8.3 🧰 What Does Lambda Provide?](#83--what-does-lambda-provide)
- [8.4 🧠 What is Serverless?](#84--what-is-serverless)
- [8.5 🧱 Lambda Basic Concepts](#85--lambda-basic-concepts)
- [8.6 🔄 How Lambda Works](#86--how-lambda-works)
- [8.7 💻 Lambda Code Examples](#87--lambda-code-examples)
- [8.8 🔔 Triggers and Invocation Types](#88--triggers-and-invocation-types)
- [8.9 ⚙️ Lambda Configuration](#89--lambda-configuration)
- [8.10 🎭 Execution Role and Permissions](#810--execution-role-and-permissions)
- [8.11 🔢 Versions and Aliases](#811--versions-and-aliases)
- [8.12 🥶 Cold Start](#812--cold-start)
- [8.13 ⚖️ Concurrency](#813--concurrency)
- [8.14 🌐 Lambda in a VPC](#814--lambda-in-a-vpc)
- [8.15 ⭐ Important Limits and Facts](#815--important-limits-and-facts)
- [8.16 📊 Monitoring Lambda](#816--monitoring-lambda)
- [8.17 💰 Lambda Pricing](#817--lambda-pricing)
- [8.18 🏗️ Real Example: Auto Thumbnail Creator](#818--real-example-auto-thumbnail-creator)
- [8.19 ⚖️ Lambda vs EC2](#819--lambda-vs-ec2)
- [📌🧠 Lambda Quick Revision](#-lambda-quick-revision)
- [🧠⚡ Lambda One-Line Memory](#-lambda-one-line-memory)
- [🗺️ Lambda Learning Map](#-lambda-learning-map)
- [⭐ Lambda Final Memory](#-lambda-final-memory)

</details>

<details>
<summary><b>🌱 PART 9 — Elastic Beanstalk — Easy Application Deployment</b></summary>

- [9.1 🌱 What is Elastic Beanstalk?](#91--what-is-elastic-beanstalk)
- [9.2 🤔 Why Do We Use Elastic Beanstalk?](#92--why-do-we-use-elastic-beanstalk)
- [9.3 🧰 What Does Elastic Beanstalk Provide?](#93--what-does-elastic-beanstalk-provide)
- [9.4 🏗️ What Beanstalk Creates for Us](#94--what-beanstalk-creates-for-us)
- [9.5 🧱 Basic Concepts](#95--basic-concepts)
- [9.6 🧩 Environment Tiers](#96--environment-tiers)
- [9.7 🌍 Environment Types](#97--environment-types)
- [9.8 🛠️ Supported Platforms](#98--supported-platforms)
- [9.9 🔄 How Deployment Works](#99--how-deployment-works)
- [9.10 🚀 Deployment Policies](#910--deployment-policies)
- [9.11 🔵🟢 Blue/Green Deployment](#911--bluegreen-deployment)
- [9.12 🧰 Ways to Deploy](#912--ways-to-deploy)
- [9.13 📁 Configuration Files](#913--configuration-files)
- [9.14 🎭 IAM Roles in Beanstalk](#914--iam-roles-in-beanstalk)
- [9.15 🗄️ Database with Beanstalk](#915--database-with-beanstalk)
- [9.16 📊 Monitoring and Health](#916--monitoring-and-health)
- [9.17 🔄 Managed Updates](#917--managed-updates)
- [9.18 💰 Elastic Beanstalk Pricing](#918--elastic-beanstalk-pricing)
- [9.19 ✅ Best For and Not Ideal For](#919--best-for-and-not-ideal-for)
- [9.20 🏗️ Real Example: Deploy a Python Flask App](#920--real-example-deploy-a-python-flask-app)
- [📌🧠 Elastic Beanstalk Quick Revision](#-elastic-beanstalk-quick-revision)
- [🧠⚡ Elastic Beanstalk One-Line Memory](#-elastic-beanstalk-one-line-memory)
- [🗺️ Elastic Beanstalk Learning Map](#-elastic-beanstalk-learning-map)
- [⭐ Elastic Beanstalk Final Memory](#-elastic-beanstalk-final-memory)

</details>

<details>
<summary><b>🧩 PART 10 — Putting It All Together</b></summary>

- [10.1 ⚖️ EC2 vs Lambda vs Elastic Beanstalk](#101--ec2-vs-lambda-vs-elastic-beanstalk)
- [10.2 🏗️ How All Services Work Together](#102--how-all-services-work-together)

</details>

- **[📌🧠 Complete AWS Quick Revision](#-complete-aws-quick-revision)**
- **[🧠⚡ Complete AWS One-Line Memory](#-complete-aws-one-line-memory)**
- **[🗺️ Complete AWS Learning Map](#-complete-aws-learning-map)**
- **[⭐ Complete AWS Final Memory](#-complete-aws-final-memory)**
- [☁️ AWS — Build Anything, Scale Everywhere](#-aws--build-anything-scale-everywhere)

---

# ☁️ PART 1 — AWS BASICS — Cloud and AWS Introduction

> Start here. Understand what AWS is before learning the services.

---

## 1.1 ☁️ What is AWS?

> **AWS = Amazon Web Services**

AWS is a cloud platform provided by Amazon.

It gives us **computing power, storage, databases, networking and many other services over the internet**.

We do not buy hardware. We **rent services** and **pay only for what we use**.

#### 📦 AWS Can Provide

- 🖥️ Servers
- 🪣 Storage
- 🗄️ Databases
- 🌐 Networking
- 🔐 Security
- ⚡ Serverless computing
- 🤖 AI and Machine Learning

#### 🧠 Easy Memory

> **AWS = Rent IT services on the internet and pay as you use**

---

## 1.2 🤔 Why Do We Use AWS?

### ❌ Traditional IT (On-Premises)

```text
🖥️ Buy Physical Servers
        ↓
🏢 Setup Data Center
        ↓
🔌 Power, Cooling, Network
        ↓
🛠️ Maintain Hardware
        ↓
📦 Run Applications
```

### ✅ With AWS

```text
☁️ AWS
 ↓
🖱️ Create Services in Minutes
 ↓
⚙️ Choose Size and Configuration
 ↓
📈 Scale Up or Down When Needed
 ↓
💰 Pay Only for Usage
```

#### ⭐ Main Reasons

- ❌ No need to buy and maintain physical hardware
- ⚡ Create resources in minutes
- 📈 Easy to scale up and down
- 💰 Pay-as-you-go pricing
- 🌍 Use services in many parts of the world
- 🛡️ Strong security tools
- 🔄 Backup and disaster recovery options

---

## 1.3 🧩 Cloud Service Models

Cloud services are mainly divided into 3 models.

```text
☁️ Cloud Models
│
├── 🏗️ IaaS  → Infrastructure as a Service
├── 🧰 PaaS  → Platform as a Service
└── 📱 SaaS  → Software as a Service
```

### 1.3.1 🏗️ IaaS — Infrastructure as a Service

We get **basic infrastructure** (servers, storage, network). We manage the OS and applications.

**Example:** Amazon EC2

> **IaaS = We rent the hardware, we manage the rest**

### 1.3.2 🧰 PaaS — Platform as a Service

We get a **ready platform**. We only manage our **code and data**.

**Example:** AWS Elastic Beanstalk

> **PaaS = Upload code, platform handles the servers**

### 1.3.3 📱 SaaS — Software as a Service

We use a **complete software** over the internet.

**Examples:** Gmail, Microsoft 365

> **SaaS = Just use the software**

### 1.3.4 ⚡ Serverless

We write only **code (functions)**. AWS runs it when needed.

**Example:** AWS Lambda

> **Serverless = No server management at all**

### 📊 Where Our 8 Services Fit

| Service                | Type                          |
| ---------------------- | ----------------------------- |
| 🖥️ EC2                | IaaS                          |
| 🌱 Elastic Beanstalk   | PaaS                          |
| ⚡ Lambda              | Serverless (FaaS)             |
| 🗄️ RDS                | Managed Database Service      |
| 🪣 S3                  | Managed Storage Service       |
| 🌐 VPC                 | Networking Service            |
| 🧭 Route 53            | DNS / Networking Service      |
| 🔐 IAM                 | Security Service              |

---

## 1.4 🌍 AWS Global Infrastructure

```text
🌍 AWS Global Infrastructure
│
├── 🌏 Region
│     └── 🏢 Availability Zones (AZ)
│
└── 📍 Edge Locations
```

### 1.4.1 🌏 Region

A **Region** is a **geographic area** where AWS has data centers.

**Examples:**

```text
ap-south-1      → Mumbai
ap-southeast-1  → Singapore
us-east-1       → N. Virginia
```

#### 💡 Why Regions Matter

- 📍 Choose a Region **close to users** for lower delay
- 📋 Some data must stay in a specific country (compliance)
- 💰 Prices can be different in different Regions
- 🧩 Some services are available only in some Regions

---

### 1.4.2 🏢 Availability Zone (AZ)

An **Availability Zone** is **one or more data centers** inside a Region.

Each Region has multiple AZs.

```text
🌏 Region: Mumbai (ap-south-1)
│
├── 🏢 AZ: ap-south-1a
├── 🏢 AZ: ap-south-1b
└── 🏢 AZ: ap-south-1c
```

#### ⭐ Key Points

- AZs are **separate** from each other (power, network, location)
- AZs in a Region are connected with fast, low-latency links
- Using **more than one AZ** gives **high availability**

> **AZ = Separate data center group inside a Region**

---

### 1.4.3 📍 Edge Location

An **Edge Location** is a site used to **deliver content faster to users**.

It is used by services such as **CloudFront** (CDN) and **Route 53**.

> **Edge Location = Nearby delivery point for faster content**

---

### 1.4.4 🌐 Global vs Regional Services

| Type               | Meaning                          | Examples (in our notes)        |
| ------------------ | -------------------------------- | ------------------------------ |
| 🌍 Global Service  | Not tied to one Region           | IAM, Route 53                  |
| 🌏 Regional Service| Works inside one Region          | EC2, S3 (buckets), VPC, RDS, Lambda, Elastic Beanstalk |

#### ⚠️ Important

> **S3 bucket names are globally unique, but each bucket is created in one Region.**

> **VPC is Regional. Subnet is inside one AZ.**

---

## 1.5 🖥️ Ways to Access AWS

```text
🖥️ Access AWS
│
├── 🌐 AWS Management Console   → Web browser (click and use)
├── ⌨️ AWS CLI                  → Command line
└── 💻 AWS SDK / API            → From code (Python, Java, Node.js ...)
```

| Method        | Used For                              |
| ------------- | ------------------------------------- |
| 🌐 Console    | Learning, quick tasks, visual setup   |
| ⌨️ CLI        | Scripts and automation                |
| 💻 SDK / API  | Application code                      |

#### ⚠️ Important

> All three methods use **IAM** to check permissions.

---

## 1.6 🤝 Shared Responsibility Model

AWS and the customer **share** the security work.

```text
🤝 Shared Responsibility
│
├── ☁️ AWS Responsibility  → Security OF the cloud
│     ├── Physical data centers
│     ├── Hardware
│     └── Core network and virtualization
│
└── 👤 Customer Responsibility → Security IN the cloud
      ├── Our data
      ├── IAM users and permissions
      ├── Security Groups and firewall rules
      └── Our operating system and applications (on EC2)
```

#### 🧠 Easy Memory

```text
AWS      = Security OF the cloud
Customer = Security IN the cloud
```

#### 💡 Example

| Service    | AWS Manages                     | We Manage                           |
| ---------- | ------------------------------- | ----------------------------------- |
| 🖥️ EC2    | Hardware, virtualization        | OS, patches, apps, firewall         |
| 🗄️ RDS    | Hardware, OS, database patching | Data, users, security groups        |
| ⚡ Lambda  | Servers, OS, runtime            | Our code and permissions            |

---

## 1.7 💰 AWS Pricing Basics

```text
💰 AWS Pricing Ideas
│
├── 💳 Pay as You Go         → Pay only for what you use
├── 📅 Save When You Commit  → Reserved / Savings Plans give discounts
├── 📈 Pay Less at Higher Use → Volume-based discounts
└── 🎁 Free Tier             → Limited free usage for new learners
```

#### 💡 Cost Safety Tips

- 🗑️ Delete resources you are not using
- ⏹️ Stop EC2 instances when not needed
- 🔔 Set a **billing alarm / budget**
- 🔁 NAT Gateways, Load Balancers and Elastic IPs can cost money if left running

---

## 1.8 📚 Services Covered in These Notes

| #  | Service                 | Category   | Simple Meaning                         |
| -- | ----------------------- | ---------- | -------------------------------------- |
| 2  | 🔐 **IAM**              | Security   | Controls who can do what               |
| 3  | 🖥️ **EC2**             | Compute    | Virtual servers                        |
| 4  | 🪣 **S3**               | Storage    | Object storage                         |
| 5  | 🌐 **VPC**              | Networking | Our private network                    |
| 6  | 🗄️ **RDS**             | Database   | Managed relational database            |
| 7  | 🧭 **Route 53**         | Networking | DNS service                            |
| 8  | ⚡ **Lambda**           | Compute    | Run code without servers               |
| 9  | 🌱 **Elastic Beanstalk**| Compute    | Easy application deployment            |

#### 🪜 Suggested Learning Order

```text
1️⃣ IAM               → Learn security first
2️⃣ VPC               → Understand networking
3️⃣ EC2               → Launch servers
4️⃣ S3                → Store files
5️⃣ RDS               → Add a database
6️⃣ Route 53          → Connect a domain
7️⃣ Lambda            → Serverless tasks
8️⃣ Elastic Beanstalk → Easy deployments
```

---

# 🔐 PART 2 — IAM — Identity and Access Management

> **IAM = Controls WHO can access AWS and WHAT they can do**

---

## 2.1 🔐 What is IAM?

> **IAM = Identity and Access Management**

AWS IAM is a service that helps us **control who can access our AWS account and what they can do**.

IAM answers two main questions:

```text
👤 WHO are you?              → Authentication
🔑 WHAT can you do?          → Authorization
```

#### 🧠 Authentication vs Authorization

| 🔍 Authentication        | 🔑 Authorization               |
| ------------------------ | ------------------------------ |
| Who are you?             | What are you allowed to do?    |
| Login with user/password | Permissions given by policies  |
| Example: Sign in         | Example: Can read S3 bucket    |

#### 🏗️ IAM Basic Flow

```text
👤 User / Application / Service
            │
            ▼
      🔍 Authentication
      (Who are you?)
            │
            ▼
      📜 Authorization
      (What can you do?)
            │
            ▼
   ☁️ AWS Services (S3, EC2, RDS ...)
```

#### 🧠 Easy Memory

> **IAM = Security Guard of our AWS Account**

#### ⚠️ Important

> **IAM is a global service.** It is not tied to one Region.

> **IAM is free.** We do not pay for IAM itself.

---

## 2.2 🤔 Why Do We Use IAM?

Suppose a company has an AWS account and many people work on it.

### ❌ Without IAM Control

```text
🔑 Everyone Uses the Same Root Login
            ↓
⚠️ Everyone Has Full Access
            ↓
💥 One Mistake Can Delete Everything
```

### ✅ With IAM

```text
☁️ AWS Account
 ↓
👤 Create Separate Users
 ↓
👥 Put Them in Groups
 ↓
📜 Give Only Required Permissions
 ↓
🛡️ Safe and Controlled Access
```

#### ⭐ Main Reasons

- 🔑 Do not share one login with everyone
- 📜 Give each person only the permissions they need
- 🛡️ Protect the AWS account from mistakes and misuse
- 🎭 Give AWS services (like EC2) access to other services safely
- 📲 Add extra security using MFA
- 📊 Track who did what in the account

---

## 2.3 🧰 What Does IAM Provide?

IAM provides:

- 👤 Users
- 👥 Groups
- 🎭 Roles
- 📜 Policies
- 🔑 Access Keys
- 📲 MFA
- 🔒 Password Policy
- 🌐 Identity Federation
- 📊 Credential Reports and Access Advisor

---

## 2.4 🧱 IAM Basic Concepts

```text
🔐 IAM
│
├── 👑 Root User
├── 👤 IAM User
├── 👥 IAM Group
├── 🎭 IAM Role
└── 📜 IAM Policy
```

### 2.4.1 🧩 Main Parts in Simple Words

| Concept        | Simple Meaning                                      |
| -------------- | --------------------------------------------------- |
| 👑 Root User   | The owner of the AWS account (full access)          |
| 👤 IAM User    | A person or application with its own login          |
| 👥 IAM Group   | A collection of users                               |
| 🎭 IAM Role    | A set of permissions that can be assumed temporarily|
| 📜 IAM Policy  | A document that says Allow or Deny                  |

### 2.4.2 🔗 How They Connect

```text
        📜 Policy
   (Allow / Deny Rules)
            │
   ┌────────┼────────┐
   ▼        ▼        ▼
 👤 User  👥 Group  🎭 Role
```

#### 🧠 Remember

> **Policy = Permissions. User, Group and Role = Who gets the permissions.**

---

## 2.5 👑 Root User

The **Root User** is created when we first create the AWS account.

It uses the **email address** we used to sign up.

#### ⭐ Key Points

- Has **complete access** to everything in the account
- Cannot be restricted by normal IAM policies
- Some tasks can only be done by the root user (like closing the account)

#### ⚠️ Important

> **Do not use the root user for daily work.**

#### ✅ Root User Best Practices

```text
1. 📲 Enable MFA on the root user
2. 🔒 Use a strong and unique password
3. 🚫 Do not create access keys for the root user
4. 👤 Create an IAM user (or admin user) for daily work
5. 🗄️ Use root only for tasks that need root
```

#### 🧠 Simple Meaning

> **Root User = Owner with unlimited power. Keep it locked.**

---

## 2.6 👤 IAM User

An **IAM User** is an identity created inside our AWS account for **one person or one application**.

Each user has its own credentials.

#### 🔐 User Credentials

```text
👤 IAM User
│
├── 🌐 Console Access
│     └── Username + Password (+ MFA)
│
└── 💻 Programmatic Access
      └── Access Key ID + Secret Access Key
```

#### ⭐ Key Points

- A new IAM user has **no permissions by default**
- We must attach policies (directly or through a group)
- One user should be used by **one person** (do not share)

#### 🚫 Default Deny

```text
👤 New IAM User
        ↓
❌ No Permissions
        ↓
📜 Attach Policy
        ↓
✅ User Gets Permissions
```

#### 🧠 Simple Meaning

> **IAM User = A person or app with its own login in AWS**

---

## 2.7 👥 IAM Group

An **IAM Group** is a **collection of IAM users**.

Instead of giving permissions to each user one by one, we give permissions to the group.

#### 🏗️ Example

```text
👥 Developers Group  ──► 📜 Developer Policy
   ├── 👤 Rahul
   ├── 👤 Sara
   └── 👤 Amit

👥 Admins Group      ──► 📜 Admin Policy
   └── 👤 Priya
```

#### ⭐ Key Points

- A group contains **only users** (a group cannot contain another group)
- A user can be in **more than one group**
- Policies attached to the group apply to **all users in it**
- A group is **not an identity for login** (we cannot sign in as a group)

#### 🧠 Simple Meaning

> **IAM Group = Manage permissions for many users together**

---

## 2.8 📜 IAM Policy

An **IAM Policy** is a **JSON document** that defines **permissions**.

It tells AWS **who can do what on which resource**.

#### 🧱 Important Elements

| Element     | Meaning                                         |
| ----------- | ----------------------------------------------- |
| `Version`   | Policy language version                         |
| `Statement` | The main permission rules                       |
| `Effect`    | `Allow` or `Deny`                               |
| `Action`    | What can be done (example: `s3:GetObject`)      |
| `Resource`  | On which resource (example: a bucket ARN)       |
| `Principal` | Who gets access (used in resource-based policies)|
| `Condition` | Optional extra conditions (like IP address)     |

#### 💻 Example IAM Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:PutObject"
      ],
      "Resource": "arn:aws:s3:::my-bucket/*"
    }
  ]
}
```

#### 📖 Understanding It

```text
Effect   → Allow
Action   → Read and Upload objects
Resource → All objects in my-bucket
```

> This policy allows reading and uploading objects in `my-bucket`.

---

### 2.8.1 🗂️ Types of Policies

```text
📜 IAM Policies
│
├── 🏢 AWS Managed Policy
├── 🛠️ Customer Managed Policy
└── 📎 Inline Policy
```

#### 1️⃣ 🏢 AWS Managed Policy

Created and managed by **AWS**.

**Examples:**

```text
AdministratorAccess
AmazonS3ReadOnlyAccess
AmazonEC2FullAccess
```

- Ready to use
- AWS updates them when needed

---

#### 2️⃣ 🛠️ Customer Managed Policy

Created and managed by **us**.

- Can be reused by many users, groups and roles
- Gives more exact control

---

#### 3️⃣ 📎 Inline Policy

A policy added **directly inside** one user, group or role.

- Belongs to only that one identity
- Deleted when that identity is deleted

#### 📊 Comparison

| 🏢 AWS Managed       | 🛠️ Customer Managed       | 📎 Inline                  |
| -------------------- | ------------------------- | -------------------------- |
| Created by AWS       | Created by us             | Created inside one identity|
| Reusable             | Reusable                  | Not reusable               |
| AWS updates it       | We update it              | We update it               |
| Quick to use         | Exact control             | One-to-one permission      |

---

### 2.8.2 ⚖️ Identity-Based vs Resource-Based Policy

#### 👤 Identity-Based Policy

Attached to an **identity** (User, Group, Role).

It says: **"This identity can do these actions."**

#### 🪣 Resource-Based Policy

Attached to a **resource** (like an S3 bucket).

It says: **"These identities can access this resource."**

```text
👤 Identity-Based          🪣 Resource-Based
User ──► Policy             Bucket ──► Policy
"What can I do?"            "Who can access me?"
```

#### 🧠 Easy Memory

> **Identity-Based = Attached to who. Resource-Based = Attached to what.**

---

## 2.9 ⚖️ Policy Evaluation Logic

When someone makes a request, AWS checks all policies and decides **Allow or Deny**.

#### 📏 Three Simple Rules

```text
1️⃣ By default, everything is DENIED  (Implicit Deny)

2️⃣ An Allow in a policy gives permission

3️⃣ An explicit Deny ALWAYS wins over Allow
```

#### 🔄 Decision Flow

```text
📨 Request
    │
    ▼
❓ Is there an explicit Deny?
    │
    ├── Yes ──► ❌ DENY
    │
    └── No
         │
         ▼
   ❓ Is there an Allow?
         │
         ├── Yes ──► ✅ ALLOW
         │
         └── No  ──► ❌ DENY (Default)
```

#### 💻 Example

```text
Policy 1 → Allow s3:*  (all S3 actions)
Policy 2 → Deny  s3:DeleteObject

Result:
✅ User can read and upload
❌ User cannot delete (Explicit Deny wins)
```

#### 🧠 Remember

> **Explicit Deny > Allow > Default Deny**

---

## 2.10 🎭 IAM Role

An **IAM Role** is an identity with **permissions** that can be **assumed (used) by someone or something** who needs it.

A role does **not** have its own password or permanent access keys.

When someone assumes a role, AWS gives them **temporary security credentials**.

#### 🎯 Why Do We Need Roles?

Suppose an **EC2 instance** needs to read files from **S3**.

##### ❌ Wrong Way

```text
🖥️ EC2
 └── 🔑 Access Key stored inside the server
        ⚠️ Risky! Keys can leak.
```

##### ✅ Right Way

```text
🖥️ EC2
 └── 🎭 IAM Role attached
        ↓
   🔑 Temporary credentials (given automatically)
        ↓
   🪣 S3 Access
```

#### ⭐ Key Points

- Gives **temporary credentials** that expire automatically
- No need to store access keys in code or servers
- Can be assumed by **AWS services, users, or other AWS accounts**
- Credentials are provided through **AWS STS (Security Token Service)**

#### 🧩 A Role Has Two Parts

```text
🎭 IAM Role
│
├── 🤝 Trust Policy
│      └── WHO can assume this role?
│
└── 📜 Permissions Policy
       └── WHAT can this role do?
```

#### 🤝 Example Trust Policy (EC2 can assume this role)

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "ec2.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

#### 📖 Understanding It

```text
Principal → EC2 service
Action    → sts:AssumeRole
Meaning   → "EC2 is allowed to use this role"
```

---

### 2.10.1 🎯 Common Uses of Roles

```text
🎭 Role Use Cases
│
├── 🖥️ EC2 Role         → EC2 accesses S3, RDS, etc.
├── ⚡ Lambda Role       → Lambda accesses DynamoDB, S3, etc.
├── 🌍 Cross-Account     → Access resources in another AWS account
└── 🌐 Federated Access  → External users sign in and get a role
```

#### 💡 Instance Profile

An **Instance Profile** is a container used to pass an IAM Role to an EC2 instance.

When we attach a role to EC2 from the console, AWS handles this for us.

#### 🧠 Simple Meaning

> **IAM Role = Temporary permissions given to a service or a person**

---

## 2.11 📊 IAM User vs Group vs Role

| Feature           | 👤 User                  | 👥 Group              | 🎭 Role                       |
| ----------------- | ------------------------ | --------------------- | ----------------------------- |
| What is it?       | Person or app identity   | Collection of users   | Temporary permission identity |
| Has login?        | Yes (password / keys)    | No                    | No (uses temporary credentials)|
| Credentials       | Long-term                | None                  | Temporary                     |
| Used by           | One person / one app     | Many users together   | AWS services, users, other accounts|
| Main purpose      | Identify a person        | Manage many users     | Give temporary access         |

#### 🧠 Easy Memory

```text
👤 User   = Person with an ID card
👥 Group  = Team of people
🎭 Role   = A temporary uniform anyone allowed can wear
```

---

## 2.12 🔑 Access Keys

**Access Keys** are used for **programmatic access** to AWS (using AWS CLI, SDK or API).

#### 🔐 Access Key Has Two Parts

```text
🔑 Access Key
│
├── 🆔 Access Key ID       (like a username)
└── 🤫 Secret Access Key   (like a password)
```

#### ⭐ Key Points

- The **Secret Access Key is shown only once** when created
- A user can have **maximum 2 access keys**
- We can **deactivate**, **rotate** or **delete** keys

#### ⚠️ Important

> **Never hard-code access keys in your code or upload them to GitHub.**

> **Never share the Secret Access Key.**

#### ✅ Better Options

```text
🖥️ Running on EC2 / Lambda?  → Use an IAM Role
💻 Using CLI on your laptop? → Use IAM Identity Center or short-term credentials if possible
```

#### 🧠 Simple Meaning

> **Access Keys = Login credentials for CLI, SDK and API**

---

## 2.13 📲 MFA

**MFA = Multi-Factor Authentication**

MFA adds an **extra layer of security** on top of the password.

#### 🔐 How It Works

```text
🔒 Password        (Something you KNOW)
        +
📱 MFA Code        (Something you HAVE)
        ↓
✅ Access Granted
```

Even if someone steals the password, they cannot log in without the MFA code.

#### 📱 Types of MFA Devices

- 📱 Authenticator app (virtual MFA) on a phone
- 🔑 Hardware security key (like FIDO security keys)
- 🔢 Hardware TOTP token

#### ✅ Where to Enable MFA

- 👑 **Root user** (must do)
- 👤 IAM users with console access, especially admins

#### 🧠 Simple Meaning

> **MFA = Password + One more proof**

---

## 2.14 🔒 Password Policy

A **Password Policy** sets the rules for IAM user passwords.

#### ⚙️ Settings We Can Control

- 📏 Minimum password length
- 🔤 Must include uppercase, lowercase, numbers, symbols
- ⏳ Password expiry (force change after some days)
- 🔁 Prevent reusing old passwords

> **Password Policy = Rules for strong passwords**

---

## 2.15 🌐 Identity Federation

**Identity Federation** lets users sign in to AWS using an **existing identity** from outside IAM, instead of creating separate IAM users.

#### 🏗️ Example

```text
🏢 Company Login (Active Directory / Google / Okta)
                  ↓
        🌐 Federation / SSO
                  ↓
          🎭 IAM Role Permissions
                  ↓
              ☁️ AWS Access
```

#### ⭐ Benefits

- 👤 No need to create IAM users for every employee
- 🔑 Users use one login for many apps (Single Sign-On)
- 🛡️ Easier user management

#### 💡 AWS IAM Identity Center

**AWS IAM Identity Center** is the AWS service for managing **SSO access** to multiple AWS accounts and applications from one place.

> **Federation = Use outside login to get AWS access**

---

## 2.16 🛡️ Permissions Boundary and SCP

These are advanced features that **limit the maximum permissions**.

### 2.16.1 🚧 Permissions Boundary

A **Permissions Boundary** sets the **maximum permissions** that a user or role can have.

```text
📜 Policy says  → Allow S3, EC2, RDS
🚧 Boundary says → Only S3 and EC2

✅ Final Permissions = S3 and EC2  (Common part only)
```

> **Permissions Boundary = Upper limit of permissions for a user/role**

---

### 2.16.2 🏢 SCP (Service Control Policy)

An **SCP** is used in **AWS Organizations** to set permission limits for **whole AWS accounts**.

```text
🏢 AWS Organization
│
├── 🛡️ SCP: Deny use of certain services
│
├── ☁️ Account A  (affected by SCP)
└── ☁️ Account B  (affected by SCP)
```

#### ⚠️ Important

> An SCP **does not give permissions**. It only **limits** what permissions can be used.

> **SCP = Guardrails for AWS accounts**

---

## 2.17 📊 IAM Monitoring and Reports

IAM gives tools to **review and audit** access.

```text
📊 IAM Reports
│
├── 📄 Credential Report
├── 🔎 Access Advisor
└── 🧭 IAM Access Analyzer
```

### 2.17.1 📄 Credential Report

A report listing **all IAM users** and the status of their credentials (passwords, access keys, MFA, last used).

### 2.17.2 🔎 Access Advisor

Shows **which services a user or role can access** and **when they last used them**.

Helps us remove unused permissions.

### 2.17.3 🧭 IAM Access Analyzer

Helps find **resources shared with outside accounts or the public**, and helps review permissions.

### 2.17.4 🕵️ AWS CloudTrail (Related Service)

**CloudTrail** records **API calls and actions** made in the account (who did what and when).

> **IAM = Who can do it. CloudTrail = Who actually did it.**

---

## 2.18 ✅ IAM Best Practices

```text
✅ IAM Best Practices
│
├── 1️⃣ 🔒 Lock away the root user
├── 2️⃣ 📲 Enable MFA
├── 3️⃣ 👤 Create individual IAM users (no sharing)
├── 4️⃣ 👥 Use groups to manage permissions
├── 5️⃣ 🎯 Give least privilege
├── 6️⃣ 🎭 Use roles for AWS services (not access keys)
├── 7️⃣ 🔄 Rotate credentials regularly
├── 8️⃣ 🗑️ Remove unused users, keys and permissions
└── 9️⃣ 📊 Monitor using CloudTrail and reports
```

### 🎯 Least Privilege

> **Give only the permissions that are needed, nothing more.**

#### 💻 Example

```text
❌ Bad  → Give AdministratorAccess to a developer who only reads S3
✅ Good → Give only S3 read permission on the required bucket
```

---

## 2.19 🏗️ Real Example: EC2 Accessing S3 Using a Role

### 🎯 Requirement

An application running on **EC2** needs to **read files from an S3 bucket**, without storing access keys on the server.

### 🏗️ Architecture

```text
┌──────────────┐        ┌──────────────┐        ┌──────────────┐
│  🖥️ EC2       │        │  🎭 IAM Role  │        │  🪣 S3 Bucket │
│  Application │ ─────► │  (Temporary  │ ─────► │  my-bucket   │
│              │ assumes│  credentials)│ access │              │
└──────────────┘        └──────────────┘        └──────────────┘
```

### 🪜 Steps to Build It

```text
1. Go to IAM → Roles → Create Role
2. Select trusted entity → AWS Service → EC2
3. Attach permission policy (for example: AmazonS3ReadOnlyAccess)
4. Give the role a name (example: EC2-S3-ReadRole)
5. Launch EC2 → Attach the IAM Role to the instance
6. Connect to EC2 and test: aws s3 ls
7. ✅ EC2 can read S3 without any access keys
```

### ✅ Why This Is Better

| ❌ Using Access Keys on EC2   | ✅ Using IAM Role               |
| ----------------------------- | ------------------------------- |
| Keys stored on server         | No keys stored                  |
| Keys can leak                 | Credentials are temporary       |
| Manual rotation needed        | Automatic rotation              |
| Risky                         | Secure and recommended          |

---

## 📌🧠 IAM Quick Revision

```text
🔐 IAM
│
├── 🧱 Identities
│   ├── 👑 Root User
│   ├── 👤 IAM User
│   ├── 👥 IAM Group
│   └── 🎭 IAM Role
│
├── 📜 Policies
│   ├── 🏢 AWS Managed
│   ├── 🛠️ Customer Managed
│   ├── 📎 Inline
│   ├── 👤 Identity-Based
│   └── 🪣 Resource-Based
│
├── 🔑 Credentials
│   ├── 🔒 Password
│   ├── 🔑 Access Keys
│   └── 📲 MFA
│
├── 🌐 Access Types
│   ├── 🎭 Roles (Temporary)
│   └── 🌐 Federation / SSO
│
├── 🛡️ Limits
│   ├── 🚧 Permissions Boundary
│   └── 🏢 SCP
│
└── 📊 Monitoring
    ├── 📄 Credential Report
    ├── 🔎 Access Advisor
    └── 🕵️ CloudTrail
```

---

## 🧠⚡ IAM One-Line Memory

| Concept                    | Easy Memory                                      |
| -------------------------- | ------------------------------------------------ |
| 🔐 **IAM**                 | Controls Who Can Do What in AWS                  |
| 👑 **Root User**           | Owner with Unlimited Power (Keep Locked)         |
| 👤 **IAM User**            | Person or App with Own Login                     |
| 👥 **IAM Group**           | Collection of Users                              |
| 🎭 **IAM Role**            | Temporary Permissions for Services or People     |
| 📜 **IAM Policy**          | JSON Document of Allow / Deny Rules              |
| 🏢 **AWS Managed Policy**  | Policy Created by AWS                            |
| 🛠️ **Customer Managed**    | Policy Created by Us (Reusable)                  |
| 📎 **Inline Policy**       | Policy Inside One Identity Only                  |
| 🤝 **Trust Policy**        | Who Can Assume the Role                          |
| 🔑 **Access Keys**         | Credentials for CLI, SDK and API                 |
| 📲 **MFA**                 | Password + One More Proof                        |
| 🌐 **Federation**          | Use Outside Login to Access AWS                  |
| 🚧 **Permissions Boundary**| Upper Limit for a User or Role                   |
| 🏢 **SCP**                 | Guardrails for Whole AWS Accounts                |
| 🎯 **Least Privilege**     | Give Only What Is Needed                         |

---

## 🗺️ IAM Learning Map

```text
                          🔐 AWS IAM
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
  IDENTITIES               PERMISSIONS              CREDENTIALS
      │                        │                        │
      ├── Root User            ├── Policies             ├── Password
      ├── IAM User             │    ├── AWS Managed     ├── Access Keys
      ├── IAM Group            │    ├── Customer Mgd    ├── MFA
      └── IAM Role             │    └── Inline          └── Temporary (STS)
                               └── Policy Evaluation
      │
      ▼
  EXTENDED ACCESS
      │
      ├── Roles (EC2, Lambda, Cross-Account)
      └── Federation / SSO
      │
      ▼
   LIMITS
      │
      ├── Permissions Boundary
      └── SCP
      │
      ▼
   MONITORING
      │
      ├── Credential Report
      ├── Access Advisor
      ├── Access Analyzer
      └── CloudTrail
```

---

## ⭐ IAM Final Memory

```text
IAM
 │
 ├── What is it?
 │      └── Controls Who Can Do What in AWS
 │
 ├── Who is the owner?
 │      └── Root User (Lock it with MFA)
 │
 ├── Who is a person or app?
 │      └── IAM User
 │
 ├── How to manage many users?
 │      └── IAM Group
 │
 ├── How to give temporary access?
 │      └── IAM Role
 │
 ├── Where are permissions written?
 │      └── IAM Policy (JSON)
 │
 ├── What wins in a conflict?
 │      └── Explicit Deny
 │
 ├── How to secure login?
 │      └── MFA
 │
 ├── How should EC2 access S3?
 │      └── IAM Role (not Access Keys)
 │
 ├── How much permission to give?
 │      └── Least Privilege
 │
 └── How to limit permissions?
        └── Permissions Boundary / SCP
```

---

# 🖥️ PART 3 — EC2 — Elastic Compute Cloud

> **EC2 = Virtual Server in AWS**

---

## 3.1 🖥️ What is EC2?

> **EC2 = Elastic Compute Cloud**

### 📖 Technical Definition

Amazon EC2 is an AWS service that provides **resizable virtual servers in the cloud**.

EC2 allows us to **launch, manage and scale servers on AWS**.

We can use these virtual computers to:

- 🌐 Host websites
- ⚙️ Run applications
- 🗄️ Run databases
- 📦 Install software
- 🐳 Run Docker
- 🔧 Run Jenkins

#### 🧠 Easy Memory

> **EC2 = Virtual Server in AWS**

---

## 3.2 🤔 Why Do We Use EC2?

If a company wants to run an application, it needs **computing resources**.

### ❌ Traditionally

```text
🖥️ Buy Physical Server
        ↓
💿 Install OS
        ↓
🔧 Configure Hardware
        ↓
🚀 Deploy Application
```

### ✅ With AWS EC2

```text
☁️ AWS
 ↓
🖥️ Create EC2 Instance
 ↓
💿 Select OS
 ↓
⚙️ Configure Resources
 ↓
🚀 Deploy Application
```

#### ⭐ Main Reasons

- ❌ No need to buy physical servers
- ⚡ Quickly create servers
- ⚙️ Choose different CPU and memory configurations
- 📈 Scale infrastructure when required
- 💰 Pay for the resources used according to the pricing model

---

## 3.3 🧰 What Does EC2 Provide?

EC2 provides:

- 🖥️ Virtual servers (instances)
- ⚙️ Different instance types
- 💿 Operating system choices through AMIs
- 🧠 CPU and memory resources
- 💾 Storage options
- 🌐 Networking
- 🛡️ Security Groups
- 🔑 Key pairs
- 📍 Elastic IP options
- 📈 Auto Scaling integration
- 📊 Monitoring through CloudWatch

---

## 3.4 🖥️ EC2 Instance

An **EC2 Instance** is a **virtual server running in AWS, created from an AMI**.

It provides compute resources such as:

- 🧠 CPU
- 🧩 RAM
- 💾 Storage
- 🌐 Networking

#### 🎯 Simple Definition

> **EC2 Instance = A Virtual Server in the AWS Cloud**

It is used to:

- 🌐 Host websites
- ⚙️ Run applications

#### 🖥️ EC2 Instance Structure

```text
🖥️ EC2 Instance
├── 🧠 CPU
├── 🧩 Memory
├── 💿 Operating System
├── 💾 Storage
└── 🌐 Network
```

We can connect to the instance and install software just like on a physical server.

---

### 3.4.1 🔄 EC2 Instance States

An instance moves through different states.

```text
🔄 EC2 Instance States
│
├── 🟡 Pending      → Starting up
├── 🟢 Running      → Working, we are charged for compute
├── 🟠 Stopping     → Going to stop
├── 🔴 Stopped      → Shut down, EBS data stays, no compute charge
├── ⏳ Shutting-down → Going to terminate
└── ⚫ Terminated   → Deleted permanently
```

#### 📊 Stop vs Terminate

| ⏹️ Stop                                   | 🗑️ Terminate                       |
| ----------------------------------------- | ---------------------------------- |
| Instance can be started again             | Instance is **deleted permanently**|
| EBS volume data stays                     | Root volume is deleted by default  |
| No compute charge, EBS storage is charged | No more charges for the instance   |

#### 🧠 Remember

> **Stop = Can start again. Terminate = Gone forever.**

---

## 3.5 📦 AMI

> **AMI = Amazon Machine Image**

An **AMI** is a **pre-configured template** that contains everything required to create an EC2 Instance.

#### 📦 It Contains

- 💿 Operating System
- 📥 Installed Software
- ⚙️ Settings and Configurations

#### 🎯 It Is Used To

- 🚀 Launch new EC2 Instance quickly
- 💾 Backup a configured server

#### ⚠️ Important

> **Without AMI, we cannot launch an EC2 Instance.**

### 🗂️ Types of AMIs

#### 1️⃣ AWS-Provided AMIs

Created and maintained by AWS.

**Examples:**

- Amazon Linux
- Ubuntu
- Windows Server

#### 2️⃣ AWS Marketplace AMI

Created by third-party vendors.

**Examples:**

- Jenkins Server
- MongoDB
- WordPress
- Red Hat Enterprise Linux

Some are free, while others require payment.

#### 3️⃣ Custom AMI

Created by the User.

**Example:**

```text
Ubuntu
   ↓
Nginx installed
   ↓
Java installed
   ↓
Our application deployed
   ↓
Save this setup as an AMI
```

We save this setup as an AMI and reuse it whenever needed.

### 🚀 Example

```text
📦 AMI
 ↓
🚀 Launch
 ↓
🖥️ EC2 Instance
```

#### 🧠 Simple Meaning

> **AMI = Template for an EC2 server**

---

## 3.6 ⚙️ Instance Type

**Instance Type** gives the **Compute Power / Resources** to an EC2 Instance, such as:

- 🧠 CPU
- 🧩 RAM
- 🌐 Network performance

It helps us choose the right amount of power for our workload.

#### Instance Type Defines

- CPU
- Memory
- Network performance
- Other hardware capabilities

#### 💻 Examples

```text
t3.micro
m5.large
```

#### 📖 Understanding the Name

```text
m5.large
│ │  │
│ │  └── Size  (nano, micro, small, medium, large, xlarge ...)
│ └───── Generation (5th generation)
└─────── Family (m = general purpose)
```

---

### 3.6.1 🏷️ Instance Families

Different instance families are designed for different workloads.

#### 1️⃣ General Purpose (T, M)

Used for:

- 🌐 Websites
- 📱 Small/medium applications
- 🖥️ General-purpose servers

**Examples:**

```text
t3
t4g
m7i
```

#### 🧠 Remember

> **General Purpose = Balanced CPU + RAM**

---

#### 2️⃣ Compute Optimized (C)

Best for:

- 🎮 Gaming
- ⚡ High-performance web servers

**Examples:**

```text
c5.large
c7i
```

#### 🧠 Remember

> **Compute Optimized = More CPU Power**

---

#### 3️⃣ Memory Optimized (R, X)

Used when applications require **large amounts of RAM**.

Best for:

- 🗄️ Large databases
- 🐬 MySQL
- 📊 Data processing

**Examples:**

```text
r5.large
r5i.large
```

#### 🧠 Remember

> **Memory Optimized = More RAM**

---

#### 4️⃣ Storage Optimized (I, D)

Used for applications requiring:

- ⚡ High storage performance
- 💾 Large local storage

Best for:

- 📦 Big Data
- 🏢 Data Warehouses

**Examples:**

```text
i3.large
d2.large
```

#### 🧠 Remember

> **Storage Optimized = High storage performance/capacity**

---

#### 5️⃣ Accelerated Computing (P, G)

Best for:

- 🤖 AI
- 🧠 Machine Learning
- 🔬 Deep Learning
- 🎨 Graphics
- 🎬 Video Rendering

#### 🧠 Remember

> **Accelerated Computing = GPU / special hardware power for AI, ML and graphics**

---

### 📊 Instance Family Summary

| Family                   | Letters | Best For                      | Easy Memory               |
| ------------------------ | ------- | ----------------------------- | ------------------------- |
| 🟢 General Purpose       | T, M    | Websites, small apps          | Balanced CPU + RAM        |
| ⚡ Compute Optimized     | C       | High-performance servers      | More CPU                  |
| 🧠 Memory Optimized      | R, X    | Large databases               | More RAM                  |
| 💾 Storage Optimized     | I, D    | Big data, data warehouses     | High storage performance  |
| 🚀 Accelerated Computing | P, G    | AI, ML, graphics              | GPU power                 |

---

## 3.7 📋 Launch Template

A **Launch Template** is a saved **Blueprint** that contains all the configurations required to launch an EC2 Instance.

Instead of entering the same EC2 settings every time, we can create a **Launch Template** and reuse it.

Launch Templates are commonly used with **EC2 Auto Scaling Groups**.

A Launch Template is a **Reusable Template** that contains EC2 Launch Settings such as:

- 📦 AMI
- ⚙️ Instance Type
- 🔑 Key Pair
- 🛡️ Security Group
- 💾 Storage
- 📝 User Data

#### 📝 What is User Data?

**User Data** is a script that runs **automatically when the instance starts for the first time**.

**Example:**

```bash
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "Hello from EC2" > /var/www/html/index.html
```

This installs a web server automatically at launch.

#### 🧠 Simple Meaning

> **Launch Template = Reusable blueprint to launch EC2**

---

## 3.8 🔑 Key Pair

A **Key Pair** is used to securely connect to EC2 Instances.

It allows secure login without using a password.

A Key Pair is a combination of:

- 🔓 Public Key
- 🔐 Private Key

#### 🔐 How It Works

```text
🔓 Public Key
    ↓
Stored by AWS on EC2 Instance

🔐 Private Key
    ↓
Downloaded and kept securely by User
```

#### 🧠 Easy Memory

```text
Public Key  = Lock
Private Key = Key of that Lock
```

For Linux EC2 Instances, SSH commonly uses a private key.

#### Example

```text
🔐 Private Key
     ↓
    SSH
     ↓
🐧 Linux EC2
```

#### 💻 SSH Command Example

```bash
chmod 400 my-key.pem
ssh -i my-key.pem ec2-user@<public-ip-address>
```

#### ⚠️ Important

> The private key should be protected and should not be shared publicly.

> AWS lets us **download the private key only once** when the key pair is created.

---

## 3.9 🛡️ Security Group

A **Security Group** is a virtual firewall that controls **inbound and outbound network traffic** for an EC2 Instance.

### Security Group Provides Two Types of Rules

#### 1️⃣ Inbound Rules

Inbound Rules control **incoming traffic**.

#### 2️⃣ Outbound Rules

Outbound Rules control **outgoing traffic**.

Security Groups use rules based on:

- Protocols
- Ports
- Source/Destination

### 🔄 Security Groups Are Stateful

Security Groups are **stateful**.

This means if an **Inbound Request** is allowed, the response is automatically allowed.

We don't need to create a separate outbound rule for the response.

#### Example

```text
🌍 Internet
   ↓
🛡️ Security Group
   ↓
🖥️ EC2
```

### 🔐 Example Inbound Rules

| Protocol   | Port | Purpose                    |
| ---------- | ---: | -------------------------- |
| SSH        |   22 | Linux administration       |
| HTTP       |   80 | Web traffic                |
| HTTPS      |  443 | Secure web traffic         |
| Custom TCP | 8080 | Application such as Tomcat |
| RDP        | 3389 | Windows remote desktop     |

#### ⭐ Key Points

- ✅ Only **Allow** rules (no Deny rules)
- 🚫 All inbound traffic is **denied by default**
- ✅ All outbound traffic is **allowed by default**
- 🔗 One instance can have **multiple** Security Groups
- 🔗 One Security Group can be attached to **multiple** instances

#### ⚠️ Important

> Do not open unnecessary ports to the entire internet.

For example, SSH port **22** should generally be restricted to trusted source IPs or managed through safer access methods where possible.

#### 🧠 Simple Meaning

> **Security Group = Firewall for the instance**

---

## 3.10 💾 EBS

> **EBS = Elastic Block Store**

EBS is a **block-level storage service provided by AWS for EC2 Instances**.

EBS is like a **hard disk** that we attach to an EC2 Instance to store data, such as:

- 💿 Operating system
- 📦 Applications
- 📄 Files

It provides **persistent storage** for EC2 Instances, which means it can remain available even when an EC2 Instance is stopped.

#### Example

```text
🖥️ EC2
 ↓
💾 EBS Volume
 ↓
📄 Data
```

### EBS Can Be Used For

- 💿 Operating system
- 📦 Application data
- 🗄️ Database storage
- 📄 Persistent files

#### 🧠 Simple Meaning

> **EBS = Persistent disk storage for EC2**

---

### 3.10.1 💽 EBS Volume

An **EBS Volume** is like a **Hard Disk / SSD for EC2 Instance**.

```text
🖥️ EC2 is a Computer
        +
💾 EBS Volume is the Hard Disk of that Computer
```

#### ⭐ Key Points

- 📍 An EBS volume is created in **one Availability Zone**
- 🔗 It can be attached to an EC2 instance in the **same AZ**
- 📸 We can take **snapshots** (backups) of it

---

### 3.10.2 📊 EBS Volume Types

EBS Volumes are mainly divided into **2 categories: SSD and HDD**.

```text
💾 EBS Volume Types
│
├── ⚡ SSD
│   ├── gp3
│   ├── gp2
│   ├── io2
│   └── io1
│
└── 🕰️ HDD
    ├── st1
    └── sc1
```

#### 1️⃣ gp3 — General Purpose SSD

gp3 is an SSD volume used for most general workloads.

**Used for:**

- 🌐 Web servers
- ⚙️ Application servers
- 📱 General applications

---

#### 2️⃣ gp2 — General Purpose SSD

gp2 is an older-generation SSD volume.

- Good for general workloads
- Performance depends partly on volume size
- gp3 is generally preferred for new workloads

---

#### 3️⃣ io2 — Provisioned IOPS SSD

io2 is an SSD volume for applications that need **high and consistent I/O performance**.

**Used for:**

- 🗄️ Databases
- ⚡ I/O-intensive applications
- 🔥 Critical applications

---

#### 4️⃣ io1 — Provisioned IOPS SSD

io1 is an older SSD volume designed for applications that need provisioned IOPS.

**Used for:**

- 🗄️ High-performance databases
- ⚡ I/O-intensive applications

---

#### 5️⃣ st1 — Throughput Optimized HDD

st1 is an HDD volume designed for **high-throughput workloads**.

It is better for large amounts of data processed sequentially.

**Used for:**

- 📦 Big Data
- 🏢 Data warehouses
- 📝 Log processing
- 📈 Large sequential workloads

---

#### 6️⃣ sc1 — Cold HDD

sc1 is a low-cost HDD volume for data that is accessed less frequently.

**Used for:**

- 🗃️ Large datasets that are rarely accessed
- 📚 Archives
- 💤 Infrequently accessed data

---

### 3.10.3 🧩 EBS Volume Roles

#### 1️⃣ Root Volume

Root Volume contains the **Operating System** of the EC2 Instance.

#### 2️⃣ Additional Volume

We can attach extra volumes to our EC2 Instance for **extra storage**.

#### Example

```text
🖥️ EC2
│
├── 💿 Root Volume
│    └── OS
│
├── 💾 Additional Volume 1
│    └── Application Data
│
└── 💾 Additional Volume 2
     └── Database / Logs / Files
```

---

### 3.10.4 📸 EBS Snapshot

An **EBS Snapshot** is a **backup/copy of an EBS Volume**.

It can be used to:

- ♻️ Restore data
- 🆕 Create a new EBS Volume

#### Used For

- 💾 Backup EBS data
- 🛟 Recover data if something goes wrong
- 🆕 Create a new EBS Volume from a snapshot
- 📋 Keep a copy of your data for future use

#### 🧠 Simple Meaning

> **EBS Snapshot = Backup of an EBS Volume**

---

### 3.10.5 🆚 EBS vs Instance Store

| 💾 EBS                           | ⚡ Instance Store                       |
| -------------------------------- | -------------------------------------- |
| Network-attached persistent disk | Disk physically attached to the host   |
| Data stays after stop            | Data is **lost** when instance stops   |
| Can take snapshots               | No snapshots                           |
| Good for most uses               | Good for temporary data, cache         |

---

## 3.11 📍 Elastic IP

An **Elastic IP Address** is a **static public IPv4 address** that can be associated with AWS resources such as an EC2 Instance.

A normal public IPv4 address may change when an instance is stopped and started, depending on how it is configured.

Elastic IP is useful when a **stable public IPv4 address** is required.

#### 🔄 Public IP vs Elastic IP

```text
🌍 Normal Public IP   → May change after stop/start
📍 Elastic IP         → Stays the same until we release it
```

#### ⚠️ Important

> **Public IPv4 addresses (including Elastic IPs) can have a cost.** Release Elastic IPs we do not use.

#### 🧠 Simple Meaning

> **Elastic IP = Static Public IPv4 Address**

---

## 3.12 ⚖️ Load Balancer

A **Load Balancer** is an AWS service that automatically distributes incoming traffic across multiple EC2 Instances and IP addresses.

### ⭐ Load Balancer Improves

- ✅ Availability
- 📈 Scalability
- 🛡️ Fault Tolerance
- ⚖️ Traffic Distribution

A Load Balancer is like a **Traffic Controller**.

Instead of sending all users to one EC2 Instance, it distributes users to multiple EC2 Instances.

This prevents one server from becoming overloaded.

#### Example

```text
👥 Users
  ↓
⚖️ Load Balancer
  ↓
 ┌──────┼──────┐
 ↓      ↓      ↓
EC2    EC2    EC2
```

This helps improve availability and distribute traffic.

#### Used For

- 🌐 Websites
- 📱 Web Applications
- 🔥 High Traffic Applications

---

### 3.12.1 🧩 Types of Load Balancers

AWS has **4 main types** of Load Balancers.

#### 1️⃣ Application Load Balancer (ALB)

Works at the **Application Layer (Layer 7)**.

Used for:

- HTTP
- HTTPS

Can send traffic based on:

- URL Path
- Host Name
- Other application-level rules

Commonly used for:

- Web Applications
- Websites

---

#### 2️⃣ Network Load Balancer (NLB)

Works at the **Transport Layer (Layer 4)**.

Used for:

- TCP
- UDP
- TLS

Provides:

- ⚡ Very high performance
- ⏱️ Low latency

Used when applications need fast network connections.

Can provide **static IP addresses**.

---

#### 3️⃣ Gateway Load Balancer (GWLB)

Works mainly at **Layer 3**.

It is used for **network security**.

It works with:

- 🔥 Firewall
- 🔍 IDS
- 🛡️ IPS

Used to deploy and manage network security appliances.

Helps distribute traffic to devices such as:

- Firewalls
- Intrusion detection systems

---

#### 4️⃣ Classic Load Balancer (CLB)

The **older generation** of AWS Load Balancer.

Supports basic:

- HTTP
- HTTPS
- TCP

AWS generally recommends using **ALB or NLB** for new applications.

---

### 📊 Load Balancer Comparison

| Load Balancer | Main Use                        |
| ------------- | ------------------------------- |
| **ALB**       | Web applications                |
| **NLB**       | Fast network traffic            |
| **GWLB**      | Firewalls & security appliances |
| **CLB**       | Older/basic applications        |

---

## 3.13 🎯 Target Group

A **Target Group** is a collection of EC2 Instances where a Load Balancer sends incoming user requests.

It also checks whether the servers are:

- ✅ Healthy
- ❌ Unhealthy

Target Group is used to run applications across multiple Availability Zones.

It supports **Blue-Green deployments**.

It improves application availability.

### 📊 Target Group Components

| Component         | Description                      |
| ----------------- | -------------------------------- |
| Target            | Resource receiving traffic       |
| Target Type       | Instance, IP, Lambda, etc.       |
| Protocol          | HTTP, HTTPS, TCP, etc.           |
| Port              | Port on which application runs   |
| Health Check      | Checks whether target is healthy |
| Health Check Path | Endpoint such as `/health`       |

#### Example

```text
                 👥 Users
                    ↓
             ⚖️ Application
             Load Balancer
                    ↓
              🎯 Target Group
           ┌────────┼────────┐
           ↓        ↓        ↓
        EC2-1     EC2-2     EC2-3
        Healthy   Healthy   Unhealthy
```

#### 🧠 Simple Meaning

> **Target Group = Group of servers that receive traffic from the Load Balancer**

---

## 3.14 📈 Auto Scaling Group (ASG)

**Auto Scaling** is an AWS service that automatically launches or terminates EC2 Instances based on:

- 📜 Defined policies
- 📊 Workload demand
- ❤️ Health conditions

It helps our application:

- 👥 Handle more users
- 💰 Save cost when traffic is low
- ✅ Maintain availability

AWS automatically **increases or decreases EC2 Instances**.

### 🧩 Main Components of ASG

#### 1️⃣ Launch Template

A Launch Template contains the configuration that AWS uses to launch new EC2 Instances.

It can contain:

- AMI
- Instance Type
- Key Pair
- Security Group
- Storage
- Network Settings
- IAM Role
- User Data

---

#### 2️⃣ Minimum Capacity

Minimum number of EC2 Instances that should run.

**Example:**

```text
Minimum Capacity = 2
```

ASG will try to keep at least **2 EC2 Instances** running.

---

#### 3️⃣ Desired Capacity

Number of EC2 Instances we normally want to run.

**Example:**

```text
Desired Capacity = 3
```

ASG will normally try to keep **3 EC2 Instances** running.

If one instance becomes unhealthy, ASG can launch a replacement to return to 3.

---

#### 4️⃣ Maximum Capacity

Maximum number of EC2 Instances that can run.

**Example:**

```text
Maximum Capacity = 5
```

ASG will not increase the number of instances above **5**, even when scaling is triggered.

#### 📊 Capacity Summary

```text
Min     Desired     Max
 2   ◄─────  3  ─────►  5
```

---

### 3.14.1 📈 Scaling Policies

A **Scaling Policy** tells the Auto Scaling Group when to add or remove EC2 Instances.

#### 1️⃣ Dynamic Scaling

Automatically increases or decreases instances based on metrics like CPU utilization.

**Example:**

```text
CPU > 70%
    ↓
Add 2 Instances

CPU < 30%
    ↓
Remove 1 Instance
```

---

#### 2️⃣ Scheduled Scaling

Scale at a fixed time.

**Example:**

```text
Every Day

9 AM  → Launch 5 Instances
10 PM → Reduce to 2 Instances
```

---

#### 3️⃣ Predictive Scaling

Predictive Scaling uses **past data** to predict future traffic and starts EC2 Instances before the traffic increases.

**Example:**

```text
Every day at 8:00 PM
        ↓
Shopping Website receives heavy traffic
        ↓
AWS learns this pattern
        ↓
Starts launching additional EC2 Instances
        ↓
Application is ready before 8:00 PM
```

#### Another Example

```text
Low Traffic
    ↓
2 EC2 Instances

High Traffic
    ↓
5 EC2 Instances
```

This helps with:

- ✅ Availability
- 📈 Scalability
- 💰 Cost Management

#### ASG Structure

```text
                 📈 Auto Scaling Group
                        │
           ┌────────────┼────────────┐
           ▼            ▼            ▼
         EC2-1        EC2-2        EC2-3
```

#### 🧠 Simple Meaning

> **ASG = Automatically adds or removes EC2 servers**

---

## 3.15 📌 Placement Groups

An **EC2 Placement Group** is an AWS feature that allows you to control the **physical placement of EC2 Instances within AWS infrastructure**.

A Placement Group is a way of telling AWS:

> **"How should I physically place my EC2 servers so that they communicate better or remain isolated from each other?"**

It helps optimize instances for specific requirements such as:

- ⚡ Low Network Latency
- 🚀 High Network Throughput
- ✅ High Availability

AWS provides **3 main types** of Placement Groups:

```text
📌 Placement Groups
│
├── 🔗 Cluster
├── 🧩 Spread
└── 🗂️ Partition
```

---

### 3.15.1 🔗 Cluster Placement Group

Instances are placed **close together in the same Availability Zone**.

#### 🎯 Main Purpose

- ⚡ High Performance Computing
- ⏱️ Low Latency Communication

#### Diagram

```text
             Availability Zone
        ┌─────────────────────────┐
        │                         │
        │   EC2-1  EC2-2  EC2-3   │
        │    ●──────●──────●      │
        │                         │
        │   EC2-4  EC2-5  EC2-6   │
        │    ●──────●──────●      │
        │                         │
        └─────────────────────────┘
```

#### Use When

- Applications need very low latency
- Big Data processing
- Instances need high network throughput

#### Example

We have **10 EC2 Instances** processing a large scientific calculation.

They continuously communicate with each other.

We want them to communicate as fast as possible.

```text
→ We Use Cluster Placement Group
```

#### 🧠 Remember

> **Cluster = Keep Instances Close**

---

### 3.15.2 🧩 Spread Placement Group

Each EC2 Instance is placed on **different physical hardware**.

#### 🎯 Main Purpose

- ✅ High Availability
- 🛡️ Failure Isolation

#### Example

```text
              Availability Zone
     ┌─────────────────────────────────┐
     │                                 │
     │  Hardware 1    Hardware 2       │
     │  ┌─────────┐   ┌─────────┐      │
     │  │  EC2-1  │   │  EC2-2  │      │
     │  └─────────┘   └─────────┘      │
     │                                 │
     │  Hardware 3    Hardware 4       │
     │  ┌─────────┐   ┌─────────┐      │
     │  │  EC2-3  │   │  EC2-4  │      │
     │  └─────────┘   └─────────┘      │
     │                                 │
     └─────────────────────────────────┘
```

#### If Hardware 1 Fails

```text
EC2-1 → ✗
EC2-2 → ✓
EC2-3 → ✓
EC2-4 → ✓
```

Application can continue running.

#### ⚠️ Important

> Spread Placement Group has a limit of **7 running instances per Availability Zone**.

#### 🧠 Remember

> **Spread = Keep Instances Separate**

---

### 3.15.3 🗂️ Partition Placement Group

Instances are divided into **different partitions**.

Each partition has its own hardware.

#### 🎯 Main Purpose

- 🌐 Large Distributed Applications
- 🛡️ Failure Isolation

#### Example

```text
                 Availability Zone
┌─────────────────────────────────────────────────────┐
│                                                     │
│  Partition 1       Partition 2       Partition 3    │
│ ┌──────────────┐  ┌──────────────┐  ┌──────────────┐│
│ │  Hardware 1  │  │  Hardware 2  │  │  Hardware 3  ││
│ │              │  │              │  │              ││
│ │    EC2-1     │  │    EC2-3     │  │    EC2-5     ││
│ │    EC2-2     │  │    EC2-4     │  │    EC2-6     ││
│ └──────────────┘  └──────────────┘  └──────────────┘│
│                                                     │
└─────────────────────────────────────────────────────┘
```

If Hardware 1 fails:

> **Only Partition 1 is affected.**

Partition 2 and 3 can continue running.

#### Use Partition Placement Group When

- We have many EC2 Instances
- We want to separate instances into groups
- We want hardware failure to affect only one partition

#### 🧠 Remember

> **Partition = Groups of instances on separate hardware**

---

### 📊 Placement Groups — Quick Summary

```text
🔗 Cluster
→ Instances close together
→ Low latency + High throughput

🧩 Spread
→ Instances separated
→ High availability + Failure isolation

🗂️ Partition
→ Instances divided into partitions
→ Large distributed applications + Failure isolation
```

---

## 3.16 💰 EC2 Pricing Models

An **EC2 Pricing Model** means the different ways AWS charges you for using EC2 Instances.

### 💰 Main EC2 Pricing Models

```text
💰 EC2 Pricing Models
│
├── 1. 🟢 On-Demand Instances
├── 2. 📅 Reserved Instances
├── 3. 💳 Savings Plans
├── 4. ⚡ Spot Instances
├── 5. 🏢 Dedicated Hosts
└── 6. 🔒 Dedicated Instances
```

---

### 3.16.1 🟢 On-Demand Instances

On-Demand means we pay for EC2 compute capacity as we use it, without making a long-term commitment.

#### How It Works

```text
🚀 Launch EC2
    ↓
🖥️ Use EC2
    ↓
💰 Pay for Usage
    ↓
⏹️ Stop / Terminate
    ↓
✅ Stop Paying for Compute
```

#### Example

Suppose:

```text
EC2 Price = $0.10/hour
You run it for = 10 hours

Cost = $1
```

#### 🧠 Simple Meaning

> **On-Demand = Pay as You Use**

---

### 3.16.2 📅 Reserved Instances (RI)

Reserved Instance (RI) is a pricing option in AWS where we commit to using an EC2 Instance for a long time, usually **1 year or 3 years**.

In return, AWS gives a **discount compared to On-Demand pricing**.

#### How It Works

```text
📝 Commit for 1 or 3 Years
          ↓
     🎁 Get a Discount
          ↓
💰 Use EC2 at Lower Cost
```

#### Example

```text
On-Demand
$100/month

Reserved Instance
$60/month
```

We save money because we agree to use the EC2 Instance for a longer period.

#### Best For

Applications that run continuously for a long time, such as:

- 🌐 Production Web Server
- 🗄️ Database Server
- ⚙️ Backend Server

#### ⚠️ Important

> Reserved Instance does **NOT** mean you reserve a physical EC2 server.

It means you commit to using EC2 for a long time and get a discount.

---

### 3.16.3 💳 Savings Plans

Savings Plans are a way to get a discount on AWS compute costs when you commit to using a certain amount of compute for **1 year or 3 years**.

Instead of committing to one specific EC2 Instance, you commit to a certain **amount of usage per hour**.

#### How It Works

```text
📝 Commit to $5/hour for 1 Year
             ↓
       ⚙️ Use AWS Compute
             ↓
         🎁 Get Discount
```

#### Example

Suppose you commit to:

```text
$5/hour for 1 year
```

You can use eligible compute resources, and AWS gives you discounted prices for the usage covered by your commitment.

### Main Types

```text
💳 Savings Plans
│
├── Compute Savings Plans
└── EC2 Instance Savings Plans
```

#### I. Compute Savings Plans

More flexible.

Your commitment can be used for eligible compute services, such as:

- EC2
- Lambda
- Fargate

You have more freedom to change your compute resources.

#### II. EC2 Instance Savings Plans

Less flexible, but usually gives a bigger discount.

It applies to a specific EC2 Instance family in a specific AWS Region.

You can still change the size of the instance within that family.

#### Best For

Savings Plans are best for:

- Long-term workloads
- Production applications
- Applications with predictable compute usage

#### ⚠️ Important

> Savings Plans do not reserve a physical EC2 server.

You make a long-term spending commitment and get a discount on eligible compute usage.

---

### 3.16.4 ⚡ Spot Instances

Spot Instances allow you to use unused EC2 capacity from AWS at a **very low price**.

When AWS has extra EC2 capacity available, you can use it at a much cheaper price than On-Demand.

#### How It Works

```text
💤 AWS has unused EC2 capacity
          ↓
     ⚡ Spot Instance
          ↓
      💰 Very low price
```

#### Example

Suppose an EC2 Instance costs:

```text
On-Demand → $100
Spot       → $30
```

The Spot price can be much lower than On-Demand.

The exact price can change depending on:

- Instance Type
- Region
- Available AWS Capacity

#### ⚠️ Important

The main disadvantage of Spot Instances is that AWS can **stop or interrupt your instance** when AWS needs the capacity back.

So, you should use Spot Instances only for workloads that can handle interruptions.

#### Interruption

```text
⚡ Spot Instance Running
        ↓
AWS Needs the Capacity
        ↓
❌ Instance May Be Interrupted
```

#### ✅ Best For

Spot Instances are good for workloads that can be stopped and started again, such as:

- 📦 Batch processing
- 📊 Big Data processing
- 🔬 Data analysis
- 🔧 CI/CD workloads
- 🧪 Testing
- 🔄 Stateless applications

#### ❌ Not Ideal For

Spot Instances are not a good choice for workloads that cannot be interrupted, such as:

- Critical production servers
- Long-running databases
- Important applications that cannot tolerate downtime

#### 🧠 Simple Way to Remember

> **Spot Instance = Very cheap EC2, but AWS can interrupt it.**

---

### 3.16.5 🏢 Dedicated Hosts

A **Dedicated Host** is a **complete physical server dedicated to your AWS account**.

This means the physical server is **not shared with other AWS customers**.

#### How It Works

```text
AWS Physical Server
┌─────────────────────────────┐
│                             │
│       YOUR AWS ACCOUNT      │
│                             │
│    EC2   EC2   EC2   EC2    │
│                             │
└─────────────────────────────┘
```

All the EC2 Instances running on this host belong to your AWS account.

#### Why Use Dedicated Hosts?

Dedicated Hosts are mainly used when you need:

- Dedicated physical hardware
- Compliance requirements
- Existing software licenses tied to a physical server
- More control and visibility over the physical host

#### 💰 Cost

Dedicated Hosts are generally more expensive than normal EC2 Instances that use shared hardware.

#### 🧠 Simple Way to Remember

> **Dedicated Host = A complete physical server dedicated to your AWS account.**

---

### 3.16.6 🔒 Dedicated Instances

Dedicated Instances are EC2 Instances that run on **physical hardware dedicated to your AWS account**.

This means your EC2 Instance's physical hardware is **not shared with other AWS customers**.

#### How It Works

```text
Dedicated Instance
        ↓
Dedicated Hardware for Your Account
        ↓
AWS Manages the Physical Server
```

---

### 🔍 Dedicated Instance vs Dedicated Host

The main difference is **control**.

#### Dedicated Instance

> You get dedicated hardware, but AWS manages the physical host. You don't get control or detailed visibility of that host.

#### Dedicated Host

> You get a whole physical server and have more visibility and control over the host.

#### 🧠 Simple Way to Remember

```text
Dedicated Instance
        ↓
Dedicated Hardware
        ↓
AWS Manages Physical Host


Dedicated Host
        ↓
Entire Physical Server
        ↓
More Visibility + Control
```

---

### 📊 Pricing Models Comparison

| Model              | Commitment        | Cost           | Best For                          |
| ------------------ | ----------------- | -------------- | --------------------------------- |
| 🟢 On-Demand       | None              | Normal price   | Short or unpredictable workloads  |
| 📅 Reserved        | 1 or 3 years      | Discount       | Steady 24/7 workloads             |
| 💳 Savings Plans   | 1 or 3 years ($/hr)| Discount      | Flexible long-term compute usage  |
| ⚡ Spot            | None              | Very low       | Interruptible workloads           |
| 🏢 Dedicated Host  | Optional          | High           | Licensing, compliance             |
| 🔒 Dedicated Instance| Optional        | High           | Dedicated hardware, AWS-managed   |

---

## 3.17 🏗️ Real Example: Web Server on EC2

### 🎯 Requirement

Host a simple website on a Linux EC2 instance.

### 🪜 Steps to Build It

```text
1. Open EC2 → Launch Instance
2. Choose AMI           → Amazon Linux
3. Choose Instance Type → t3.micro
4. Choose Key Pair      → Create or select one
5. Network Settings     → Select VPC and Public Subnet
6. Security Group       → Allow SSH (22) from My IP, HTTP (80) from anywhere
7. Storage              → Default EBS gp3 root volume
8. Advanced → User Data → Add the web server install script
9. Launch Instance
10. Open the Public IP in a browser ✅
```

### 🏗️ Architecture

```text
🌍 Internet
     │
     ▼
🚪 Internet Gateway
     │
     ▼
┌──────── 🌐 VPC ─────────┐
│  ┌── 🌍 Public Subnet ──┐│
│  │   🖥️ EC2 Instance    ││
│  │   🛡️ Security Group  ││
│  │   💾 EBS Volume      ││
│  └──────────────────────┘│
└──────────────────────────┘
```

---

## 📌🧠 EC2 Quick Revision

```text
🖥️ EC2
│
├── 🖥️ Instance
│   ├── 📦 AMI
│   ├── ⚙️ Instance Type
│   ├── 🔑 Key Pair
│   └── 🛡️ Security Group
│
├── 💾 Storage
│   └── EBS
│       ├── Root Volume
│       ├── Additional Volume
│       └── Snapshot
│
├── 🌐 Networking
│   ├── 📍 Elastic IP
│   ├── ⚖️ Load Balancer
│   └── 🎯 Target Group
│
├── 📈 Scaling
│   ├── 📋 Launch Template
│   └── 📈 Auto Scaling Group
│
├── 📌 Placement Groups
│   ├── Cluster
│   ├── Spread
│   └── Partition
│
└── 💰 Pricing Models
    ├── On-Demand
    ├── Reserved Instances
    ├── Savings Plans
    ├── Spot Instances
    ├── Dedicated Hosts
    └── Dedicated Instances
```

---

## 🧠⚡ EC2 One-Line Memory

| Concept                | Easy Memory                     |
| ---------------------- | ------------------------------- |
| 🖥️ **EC2**            | Virtual Server                  |
| 📦 **AMI**             | Server Template                 |
| ⚙️ **Instance Type**   | Compute Power                   |
| 📋 **Launch Template** | Reusable Launch Configuration   |
| 🔑 **Key Pair**        | Secure Login                    |
| 🛡️ **Security Group** | Virtual Firewall                |
| 💾 **EBS**             | Persistent Disk                 |
| 📸 **Snapshot**        | EBS Backup                      |
| 📍 **Elastic IP**      | Static Public IPv4              |
| ⚖️ **Load Balancer**   | Distributes Traffic             |
| 🎯 **Target Group**    | Group of Targets                |
| 📈 **ASG**             | Automatically Adjusts Instances |
| 📌 **Placement Group** | Controls Physical Placement     |
| 💰 **Pricing Models**  | Different Ways to Pay           |

---

## 🗺️ EC2 Learning Map

```text
                         ☁️ AWS EC2
                              │
       ┌──────────────────────┼──────────────────────┐
       │                      │                      │
       ▼                      ▼                      ▼
    COMPUTE                STORAGE               NETWORKING
       │                      │                      │
       │                      │                      ├── Security Group
       │                      ├── EBS                ├── Elastic IP
       │                      │   ├── Volume         ├── Load Balancer
       │                      │   └── Snapshot       └── Target Group
       │                      │
       └── Instance Type      │
                              │
                              ▼
                           LAUNCH
                              │
                              ├── AMI
                              ├── Key Pair
                              └── Launch Template
                              │
                              ▼
                           SCALING
                              │
                              └── Auto Scaling Group
                              │
                              ▼
                          PLACEMENT
                              │
                              ├── Cluster
                              ├── Spread
                              └── Partition
                              │
                              ▼
                           PRICING
                              │
                              ├── On-Demand
                              ├── Reserved Instances
                              ├── Savings Plans
                              ├── Spot
                              ├── Dedicated Host
                              └── Dedicated Instance
```

---

## ⭐ EC2 Final Memory

```text
EC2
 │
 ├── What is it?
 │      └── Virtual Server
 │
 ├── What creates it?
 │      └── AMI
 │
 ├── How powerful?
 │      └── Instance Type
 │
 ├── How to launch repeatedly?
 │      └── Launch Template
 │
 ├── How to connect?
 │      └── Key Pair
 │
 ├── How to secure?
 │      └── Security Group
 │
 ├── Where to store data?
 │      └── EBS
 │
 ├── How to distribute traffic?
 │      └── Load Balancer
 │
 ├── Which servers receive traffic?
 │      └── Target Group
 │
 ├── How to scale?
 │      └── Auto Scaling Group
 │
 ├── How to place instances?
 │      └── Placement Groups
 │
 └── How to pay?
        └── Pricing Models
```

---

# 🪣 PART 4 — S3 — Simple Storage Service

> **S3 = Object Storage in AWS**

---

## 4.1 ☁️ What is S3?

> **S3 = Simple Storage Service**

Amazon S3 is a secure object storage service provided by AWS.

It is used to **store and retrieve any amount of data from anywhere over the internet**.

S3 stores data as **Objects inside Buckets**.

#### 📦 S3 Can Store

- 🖼️ Images
- 🎥 Videos
- 📄 Documents
- 💾 Backup files
- 🌐 Static website files
- 📝 Log files
- 📦 Application files

#### 🏗️ S3 Basic Architecture

```text
👤 User / Application
        │
        ▼
    ☁️ AWS S3
        │
        ▼
    🪣 Bucket
        │
        ▼
    📦 Object
```

#### 🧠 Easy Memory

> **S3 = Object Storage in AWS**

---

## 4.2 🤔 Why Do We Use S3?

Suppose a company has files that need to be stored.

### ❌ Traditional Storage

```text
🖥️ Buy Storage Server
        ↓
⚙️ Install Storage
        ↓
🔧 Manage Hardware
        ↓
📦 Store Files
```

### ✅ With S3

```text
☁️ AWS
 ↓
🪣 Create S3 Bucket
 ↓
📦 Upload Objects
 ↓
💾 Store Data
```

#### ⭐ Main Reasons

- ❌ No need to manage physical storage hardware
- 📈 Highly scalable storage
- 📦 Store large amounts of data
- 🛡️ High durability
- 🌍 Access data from anywhere
- 💾 Different storage classes for different needs
- 🔄 Backup and disaster recovery
- 🌐 Static website hosting

---

## 4.3 🧰 What Does S3 Provide?

S3 provides:

- 🪣 Buckets
- 📦 Objects
- 🔑 Object Keys
- 💾 Storage Classes
- 🔄 Versioning
- ♻️ Lifecycle Rules
- 🔒 Encryption
- 🛡️ Access Control
- 🔄 Replication
- 🔔 Event Notifications
- 🌐 Static Website Hosting

---

## 4.4 🧱 S3 Basic Concepts

### 4.4.1 🪣 S3 Bucket

A **Bucket** is a container used to store objects in S3.

> **Bucket = Container for S3 Objects**

#### 🧩 Core Relationship

```text
☁️ S3
 │
 └── 🪣 Bucket
       │
       ├── 📄 Object
       ├── 🖼️ Object
       └── 📦 Object
```

#### Example

```text
my-website-bucket
│
├── 📄 index.html
├── 🎨 style.css
├── 🖼️ logo.png
└── 📁 images/
    ├── 🖼️ image1.jpg
    └── 🖼️ image2.jpg
```

#### 💡 Important

Before uploading an object to S3, we normally create a bucket.

#### ⭐ Bucket Rules

- 🌍 Bucket names must be **globally unique** (across all AWS accounts)
- 🌏 A bucket is created in **one Region**
- 🔤 Names use lowercase letters, numbers and hyphens
- 📏 Name length is 3 to 63 characters

---

### 4.4.2 📦 S3 Object

An **Object** is the actual data stored inside an S3 bucket.

Every file stored in S3 is called an **Object**.

#### Examples

```text
🖼️ photo.jpg
🎥 video.mp4
📄 resume.pdf
🌐 index.html
📦 backup.zip
```

An object consists mainly of:

```text
📦 Object
│
├── 📄 Data
├── 🔑 Key
└── 📝 Metadata
```

#### 🧠 Simple Meaning

> **Object = File stored in S3**

#### ⭐ Object Facts

- 📏 One object can be up to **5 TB**
- 📤 A single upload (PUT) can be up to **5 GB**. For larger files, use **Multipart Upload**

---

### 4.4.3 🔑 Object Key

An **Object Key** is the name of the Object.

It is used to identify an object inside an S3 bucket.

#### Example

```text
🪣 Bucket
│
├── 📄 index.html
├── 📁 images/logo.png
└── 📁 documents/resume.pdf
```

#### 🧠 Important

S3 does not have traditional folders like a normal file system.

What looks like a folder is actually part of the **object key**.

#### Example

```text
images/logo.png
│      │
│      └── 📄 Object name
│
└── 📁 Prefix
```

---

### 4.4.4 🛡️ S3 Durability and Availability

- 🛡️ S3 Standard is designed for **99.999999999% (11 nines) durability**
- 📋 Data is stored across **multiple Availability Zones** (except One Zone classes)

> **Durability = Data will not be lost**

---

## 4.5 💾 S3 Storage Classes

Different data has different access requirements.

For example:

- 🔥 Some data is accessed frequently.
- 💤 Some data is rarely accessed.
- 🧊 Some data is only kept for backup/archive.

S3 provides different **Storage Classes**.

#### 📊 Storage Classes

```text
💾 S3 Storage Classes
│
├── 🟢 S3 Standard
├── 🧠 S3 Intelligent-Tiering
├── 🟡 S3 Standard-IA
├── 🟠 S3 One Zone-IA
├── ⚡ S3 Glacier Instant Retrieval
├── 🧊 S3 Glacier Flexible Retrieval
└── ❄️ S3 Glacier Deep Archive
```

### 4.5.1 🟢 S3 Standard

Used for data that is accessed frequently.

#### Examples

- 🌐 Websites
- 💻 Applications
- 📄 Frequently accessed files

> **Standard = Frequently accessed data**

---

### 4.5.2 🧠 S3 Intelligent-Tiering

Used when the access pattern is unknown or changes over time.

AWS automatically moves objects between access tiers based on how often they are accessed.

```text
🔄 Changing Access Pattern
          ↓
🧠 Intelligent-Tiering
          ↓
🤖 AWS Automatically Changes Tier
          ↓
💰 Helps Reduce Storage Cost
```

> **Intelligent-Tiering = Changing or unknown access**

---

### 4.5.3 🟡 S3 Standard-IA

**IA = Infrequent Access**

Used for data that is accessed less frequently but needs quick access when required.

#### Examples

- 📊 Old reports
- 💾 Backups
- 📄 Important files that are rarely accessed

> **Standard-IA = Infrequent access + Quick retrieval**

---

### 4.5.4 🟠 S3 One Zone-IA

Used for infrequently accessed data in a **single Availability Zone**.

#### Examples

- 💾 Re-creatable backups
- 📄 Old data
- 🔄 Secondary copies of data
- 🗂️ Temporary data that is rarely accessed

> **One Zone-IA = Infrequent access + Quick retrieval + Stored in one Availability Zone**

---

### 4.5.5 ⚡ S3 Glacier Instant Retrieval

Used for archive data that still needs fast retrieval when required.

#### Examples

- 🏥 Medical records
- 📄 Old documents
- 🗃️ Long-term archives
- 📊 Historical data

> **Glacier Instant Retrieval = Rarely accessed + Instant retrieval**

---

### 4.5.6 🧊 S3 Glacier Flexible Retrieval

Used for archive data where retrieval can take more time.

#### Examples

- 💾 Old backups
- 🗃️ Archived files
- 📦 Long-term data
- 🛡️ Disaster recovery data

> **Glacier Flexible Retrieval = Rarely accessed + Retrieval in minutes to hours**

---

### 4.5.7 ❄️ S3 Glacier Deep Archive

Used for data that is very rarely accessed and needs to be stored for a long time at very low cost.

#### Examples

- 💾 Long-term backups
- 🗃️ Old archives
- 📜 Historical records

> **Glacier Deep Archive = Very rarely accessed + Lowest storage cost + Long retrieval time**

---

### 🧠 Easy Storage Class Memory

```text
🔥 Frequently Used
       ↓
🟢 S3 Standard

🤔 Unknown / Changing Access
       ↓
🧠 Intelligent-Tiering

💤 Infrequent Access
       ↓
🟡 Standard-IA
🟠 One Zone-IA

🧊 Archive
       ↓
⚡ Glacier Instant Retrieval
🧊 Glacier Flexible Retrieval
❄️ Glacier Deep Archive
```

---

## 4.6 🔄 Versioning

**S3 Versioning** is a feature that keeps multiple versions of an object.

It helps protect data from accidental deletion or overwriting.

#### 🎯 Used To

- ♻️ Recover accidentally deleted objects
- ⏪ Recover previous versions
- 🛡️ Protect against accidental overwrites
- 📚 Maintain multiple versions of data

#### Example

```text
📄 File
│
├── 🕐 Version 1
├── 🕑 Version 2
└── 🕒 Version 3
```

Suppose:

```text
website.zip
```

is uploaded.

Later, another `website.zip` is uploaded.

With versioning enabled:

```text
📦 website.zip
│
├── 🕐 Version 1
└── 🕑 Version 2
```

#### ⭐ Key Points

- 🔄 Versioning is **disabled by default**
- ▶️ Once enabled, it can only be **suspended**, not fully turned off
- 🗑️ A delete on a versioned bucket adds a **delete marker** (old versions stay)

#### 🧠 Simple Meaning

> **Versioning = Keep previous versions of objects**

---

## 4.7 🔐 S3 Permissions and Security

S3 security controls **who can access which bucket or object and what they can do**.

#### 🛡️ Common Security Mechanisms

```text
🔐 S3 Security
│
├── 📜 IAM Policy
├── 🪣 Bucket Policy
├── 📋 ACLs
└── 🚫 Block Public Access
```

#### 🛡️ S3 Access Control Flow

```text
👤 Identity / Service
        │
        ▼
   📜 IAM Policy
        │
        ▼
    🪣 S3 Bucket
        │
        ▼
 📦 Bucket / Object
        │
        ▼
  ✅ Allow / ❌ Deny
```

### 4.7.1 📜 IAM Policy

An **IAM Policy** gives permissions to an IAM User, Group, or Role to access S3.

#### Important Elements

| Element    | Meaning               |
| ---------- | --------------------- |
| `Effect`   | Says Allow or Deny    |
| `Action`   | Says what you can do  |
| `Resource` | Says where you can do it |

#### Example IAM Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:PutObject",
        "s3:DeleteObject"
      ],
      "Resource": "arn:aws:s3:::my-bucket/*"
    }
  ]
}
```

#### Permission Examples

```text
📖 s3:GetObject      → Read Object
⬆️ s3:PutObject      → Upload Object
🗑️ s3:DeleteObject   → Delete Object
```

#### Flow

```text
👤 IAM User / Role
        ↓
📜 IAM Policy
        ↓
🪣 S3 Permissions
        ↓
📖 Read / ✏️ Write / 🗑️ Delete
```

---

### 4.7.2 🪣 Bucket Policy

A **Bucket Policy** is a resource-based policy attached directly to an S3 bucket.

It controls who can access the S3 bucket and what actions they can perform.

Bucket policies are written in **JSON format**.

#### Example Bucket Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::123456789012:user/John"
      },
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-bucket/*"
    }
  ]
}
```

#### Bucket Policy Controls

- 👤 Who can access?
- ⚙️ What actions are allowed?
- 📦 Which resources?

#### Common Uses

- 🪣 Control access to a specific S3 bucket
- 👤 Give S3 access to specific AWS users or services
- 🌍 Allow users from another AWS account to access the bucket
- 📦 Control who can access objects in the bucket

---

### ⚖️ IAM Policy vs Bucket Policy

| 📜 IAM Policy                    | 🪣 Bucket Policy                  |
| -------------------------------- | --------------------------------- |
| Attached to User, Role, or Group | Attached to S3 Bucket             |
| Identity-based policy            | Resource-based policy             |
| Controls what an identity can do | Controls access to an S3 resource |

#### 🧠 Simple Difference

> **IAM Policy → What an identity can do**

> **Bucket Policy → Who can access an S3 resource**

---

### 4.7.3 📋 ACLs

**ACL = Access Control List**

S3 ACL is used to control access to S3 buckets and objects.

It controls:

- 👤 Who can access
- ⚙️ What they can do

ACL is an **older access control mechanism** in S3.

ACLs can control access to:

- 🪣 Buckets
- 📦 Objects

> 💡 For most modern S3 use cases, IAM policies and bucket policies are preferred.

---

### 4.7.4 🚫 Block Public Access

**Block Public Access** is used to prevent public access to S3 buckets and objects.

It helps protect data from accidental public exposure.

#### 🔐 For Private Data

Keep **Block Public Access enabled**, unless there is a specific requirement to make data public.

```text
🚫 Block Public Access
        ↓
🛡️ Helps Prevent Public Access
        ↓
🔒 Protects Data From Accidental Exposure
```

#### ⚠️ Important

> For a **public static website**, Block Public Access must be turned off for that bucket, and a bucket policy must allow public read.

---

### 4.7.5 🔗 Pre-signed URLs

A **Pre-signed URL** gives **temporary access** to a private object.

```text
👤 Owner creates pre-signed URL
        ↓
🔗 URL valid for limited time
        ↓
👥 Anyone with the URL can access that object until it expires
```

> **Pre-signed URL = Temporary link to a private object**

---

## 4.8 🔒 Encryption

S3 supports encryption to protect data.

#### 🔐 Encryption Flow

```text
📄 Data
   │
   ▼
🔒 Encryption
   │
   ▼
☁️ S3
   │
   ├── 🔑 SSE-S3
   ├── 🔐 SSE-KMS
   ├── 🔐🔐 DSSE-KMS
   └── 🗝️ SSE-C
```

#### Main Server-Side Encryption Options

```text
🔒 S3 Encryption
│
├── 🔑 SSE-S3
├── 🔐 SSE-KMS
├── 🔐🔐 DSSE-KMS
└── 🗝️ SSE-C
```

> **SSE = Server-Side Encryption**

#### ⭐ Default Encryption

S3 now encrypts new objects by default using **SSE-S3**.

### 4.8.1 🔑 SSE-S3

AWS manages the encryption keys.

S3 automatically encrypts objects when stored.

It is a simple option for most use cases.

```text
👤 You
 ↓
⬆️ Upload File
 ↓
☁️ S3
 ↓
🔒 AWS Encrypts File
```

#### 🧠 Remember

> **SSE-S3 → S3 manages encryption keys**

---

### 4.8.2 🔐 SSE-KMS

Encryption uses **AWS KMS keys**.

It gives us more control over encryption keys.

```text
☁️ S3
 ↓
🔐 AWS KMS
 ↓
🔑 Encryption Key
```

Useful when we need more control over encryption keys and auditing.

#### 🧠 Remember

> **SSE-KMS → KMS manages the encryption key**

---

### 4.8.3 🗝️ SSE-C

**SSE-C = Server-Side Encryption with Customer-Provided Keys**

We provide the encryption key.

S3 performs the encryption/decryption.

We are responsible for managing the key.

```text
👤 Customer
    ↓
🔑 Encryption Key
    ↓
☁️ S3
```

#### 🧠 Remember

> **SSE-C → Customer provides the key**

---

### 4.8.4 🔐🔐 DSSE-KMS

**DSSE-KMS = Dual-layer Server-Side Encryption with KMS keys**

S3 applies **two layers of encryption** to the object using KMS keys.

It is used when strict compliance rules need extra protection.

#### 🧠 Remember

> **DSSE-KMS → Two layers of encryption with KMS keys**

---

### 4.8.5 🌐 Encryption in Transit

Data moving between us and S3 can be protected with **HTTPS (SSL/TLS)**.

```text
💾 At Rest     → Data stored in S3 is encrypted (SSE)
🌐 In Transit  → Data moving to S3 is protected (HTTPS)
```

---

## 4.9 🛡️ S3 Security vs Encryption

| 🛡️ Security                    | 🔒 Encryption                                  |
| ------------------------------ | ---------------------------------------------- |
| Controls access                | Protects data                                  |
| IAM Policy                     | SSE-S3                                         |
| Bucket Policy                  | SSE-KMS                                        |
| ACL                            | DSSE-KMS                                       |
| Block Public Access            | SSE-C                                          |
| Answers **"Who can access?"**  | Answers **"Can someone read the stored data?"**|

#### 🧠 Easy Memory

```text
🛡️ Security
     ↓
👤 WHO can access?

🔒 Encryption
     ↓
📄 Protects stored data
```

---

## 4.10 🌐 S3 Static Website Hosting

S3 can host **static websites**.

A static website mainly contains:

- 📄 HTML
- 🎨 CSS
- ⚙️ JavaScript
- 🖼️ Images

These files can be uploaded to an S3 bucket and served as a website.

#### 🌐 Static Website Examples

- 👨‍💻 Portfolio
- 🏢 Company landing page
- 📚 Documentation
- 🛍️ Product landing page
- 🏪 Simple business website

#### 🏗️ Static Website Architecture

```text
👤 Visitor
    │
    ▼
🌐 Website Request
    │
    ▼
🪣 S3 Bucket
    │
    ├── 📄 index.html
    ├── 🎨 style.css
    ├── ⚙️ script.js
    └── 🖼️ images/
```

#### ⚙️ Basic Steps

1. 🪣 Create an S3 bucket
2. 📤 Upload website files
3. ⚙️ Enable Static Website Hosting
4. 🔧 Configure required website settings (index document, error document)
5. 🔓 Allow public read access (turn off Block Public Access + bucket policy)
6. 🌐 Access the website using the S3 website endpoint

#### 💻 Example Bucket Policy for Public Website

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-website-bucket/*"
    }
  ]
}
```

#### ⚠️ Important

> S3 static website endpoint uses **HTTP**. For **HTTPS** and a custom domain, use **CloudFront** (and Route 53 for the domain name).

> **Static Website Hosting = Hosting static website files using S3**

---

## 4.11 ♻️ S3 Lifecycle Management

**S3 Lifecycle Management** is used to automatically move or delete objects based on rules.

Instead of manually managing old files, S3 does it automatically.

### ♻️ Lifecycle Rule

A Lifecycle Rule tells S3 what to do with objects when certain conditions are met.

#### Two Main Lifecycle Actions

```text
♻️ Lifecycle
│
├── 🔄 Transition
│
└── 🗑️ Expiration
```

#### 🔄 Transition

Moves an object to another storage class.

#### 🗑️ Expiration

Deletes objects automatically after a specified period.

#### ♻️ Lifecycle Flow

```text
📦 Object Uploaded
        │
        ▼
      ⏳ Time
        │
        ▼
🔄 Transition
        │
        ▼
💾 Cheaper Storage Class
        │
        ▼
      ⏳ More Time
        │
        ▼
🗑️ Expiration
```

#### Example

```text
📦 Object Uploaded
       ↓
    ⏳ 30 Days
       ↓
💾 Move to Standard-IA
       ↓
    ⏳ 90 Days
       ↓
🧊 Move to Glacier
       ↓
   ⏳ 365 Days
       ↓
🗑️ Delete
```

#### Lifecycle Can Be Used To

- 💰 Move objects to cheaper storage classes
- 🗑️ Delete old objects
- 💵 Manage storage costs
- 🧊 Automatically archive data

#### 🧠 Simple Meaning

> **Lifecycle = Automatically manage object storage over time**

---

## 4.12 🔄 S3 Replication

**S3 Replication** automatically copies objects from one S3 bucket to another S3 bucket.

#### 🔄 Replication Architecture

```text
🪣 Source Bucket
       │
       │ 🔄 Replication Rule
       ▼
🪣 Destination Bucket
```

#### 🎯 Useful For

- 🌍 Keeping data closer to users
- 💾 Backup
- 🛡️ Disaster recovery
- 🔁 Data redundancy
- 📋 Compliance

### 🔄 Types of S3 Replication

```text
🔄 S3 Replication
│
├── 🏠 SRR
│   └── Same-Region Replication
│
└── 🌍 CRR
    └── Cross-Region Replication
```

### 4.12.1 🏠 SRR — Same-Region Replication

> **SRR = Same-Region Replication**

Objects are replicated/copied between S3 buckets in the **same AWS Region**.

```text
🇮🇳 Mumbai Region
│
├── 🪣 Source Bucket
│        │
│        │ 🔄 SRR
│        ▼
└── 🪣 Destination Bucket
```

#### Use Cases

- 💾 Backup
- 🔬 Separating production and test data

#### 🧠 Remember

> **SRR = Same Region**

---

### 4.12.2 🌍 CRR — Cross-Region Replication

> **CRR = Cross-Region Replication**

Copies objects from a bucket in one AWS Region to another AWS Region.

```text
🇮🇳 Mumbai Region
      │
      ▼
🪣 Source S3 Bucket
      │
      │ 🔄 CRR
      ▼
🇸🇬 Singapore Region
      │
      ▼
🪣 Destination S3 Bucket
```

#### Use Cases

- 🛡️ Disaster recovery
- 🌍 Reduce latency for users in another Region

#### 🧠 Remember

> **CRR = Different Regions**

---

### 4.12.3 🔧 Replication Rules

A Replication Rule defines:

- 📦 Which objects should be replicated
- 📍 Where they should be replicated
- 🪣 What destination bucket should be used

Replication can be applied to:

- 📦 All objects
- 📁 Specific objects using prefixes
- 🏷️ Objects with specific tags

---

### 4.12.4 🕒 Versioning Requirement

S3 Versioning must be enabled on **both the source and destination buckets** for S3 live replication.

```text
🪣 Source Bucket
Versioning → ✅ ON
       ↓
🔄 Replication
       ↓
🪣 Destination Bucket
Versioning → ✅ ON
```

---

### 4.12.5 📦 Existing Objects vs New Objects

By default, S3 live replication is designed for **new and updated objects** after replication is configured.

For objects that already exist, you can use **S3 Batch Replication**.

```text
🆕 New Objects
     ↓
🔄 Live Replication

📦 Existing Objects
     ↓
⚙️ Batch Replication
```

#### 💻 Example

```text
👤 User uploads photo.jpg
        ↓
🪣 Source Bucket
        ↓
🔄 Replication Rule
        ↓
🪣 Destination Bucket (photo.jpg copied automatically)
```

---

### ⚖️ CRR vs SRR

| 🌍 CRR                      | 🏠 SRR                    |
| --------------------------- | ------------------------- |
| Cross-Region Replication    | Same-Region Replication   |
| Different AWS Regions       | Same AWS Region           |
| 🛡️ Disaster recovery        | 💾 Backup / data processing|
| Example: Mumbai → Singapore | Example: Mumbai → Mumbai  |

---

## 4.13 🚀 S3 Transfer Acceleration

**S3 Transfer Acceleration** helps speed up uploads and downloads to S3 by using AWS edge locations.

#### 🚀 Transfer Flow

```text
👤 User
   │
   ▼
📍 Nearest AWS Edge Location
   │
   ▼
🌐 AWS Network
   │
   ▼
🪣 S3 Bucket
```

It is useful when users are geographically far from the S3 bucket's Region.

#### 🧠 Simple Meaning

> **Transfer Acceleration = Faster long-distance S3 transfers**

---

## 4.14 🧩 Multipart Upload

**Multipart Upload** allows a large object to be uploaded in multiple parts.

#### 🧩 Multipart Upload Flow

```text
📦 Large File
     │
     ▼
┌────────┬────────┬────────┬────────┐
│ Part 1 │ Part 2 │ Part 3 │ Part 4 │
└────────┴────────┴────────┴────────┘
     │
     ▼
☁️ S3
     │
     ▼
📦 Complete Object
```

#### ⭐ Benefits

- ⚡ Faster uploads
- 🔀 Upload parts in parallel
- 🔁 Retry only failed parts
- 📦 Useful for large files

#### 💡 When to Use

- Recommended for files larger than **100 MB**
- Required for files larger than **5 GB**

#### 🧠 Simple Meaning

> **Multipart Upload = Upload large file in smaller parts**

---

## 4.15 🔔 S3 Event Notifications

**S3 Event Notifications** send a message when something happens in a bucket.

#### 🔔 Example Events

- 📤 Object created (uploaded)
- 🗑️ Object deleted
- ♻️ Object restored

#### 🎯 Can Send Events To

```text
🔔 S3 Event
   │
   ├── ⚡ Lambda
   ├── 📬 SQS Queue
   ├── 📢 SNS Topic
   └── ⏰ EventBridge
```

#### 💻 Example

```text
👤 Upload photo.jpg
        ↓
🪣 S3 Bucket
        ↓ (Event)
⚡ Lambda → Creates a thumbnail
```

> **Event Notification = S3 tells another service "something happened"**

---

## 4.16 💰 S3 Pricing

```text
💰 S3 Cost
│
├── 💾 Storage (per GB per month, depends on storage class)
├── 📨 Requests (PUT, GET, LIST ...)
├── 🌐 Data Transfer Out to the internet
├── 🔄 Replication
└── 🚀 Extra features (Transfer Acceleration, retrieval fees for IA/Glacier)
```

#### 💡 Cost Tips

- 💾 Use **Lifecycle rules** to move old data to cheaper classes
- 🗑️ Delete old versions and incomplete multipart uploads
- 🧠 Use **Intelligent-Tiering** if access pattern is unknown

---

## 📌🧠 S3 Quick Revision

```text
☁️ S3
│
├── 🧱 Basics
│   ├── 🪣 Bucket
│   ├── 📦 Object
│   └── 🔑 Object Key
│
├── 💾 Storage
│   └── Storage Classes
│       ├── 🟢 Standard
│       ├── 🧠 Intelligent-Tiering
│       ├── 🟡 Standard-IA
│       ├── 🟠 One Zone-IA
│       └── 🧊 Glacier
│
├── 🔐 Security
│   ├── 📜 IAM Policy
│   ├── 🪣 Bucket Policy
│   ├── 📋 ACL
│   └── 🚫 Block Public Access
│
├── 🔒 Encryption
│   ├── 🔑 SSE-S3
│   ├── 🔐 SSE-KMS
│   ├── 🔐🔐 DSSE-KMS
│   └── 🗝️ SSE-C
│
├── 🛠️ Management
│   ├── 🔄 Versioning
│   └── ♻️ Lifecycle
│
├── 🔄 Replication
│   ├── 🏠 SRR
│   └── 🌍 CRR
│
└── 🚀 Performance
    ├── ⚡ Transfer Acceleration
    └── 🧩 Multipart Upload
```

---

## 🧠⚡ S3 One-Line Memory

| Concept                    | Easy Memory                                   |
| -------------------------- | --------------------------------------------- |
| ☁️ **S3**                  | Object Storage                                |
| 🪣 **Bucket**              | Container for Objects                         |
| 📦 **Object**              | File stored in S3                             |
| 🔑 **Object Key**          | Object Name / Identifier                      |
| 💾 **Storage Class**       | Storage based on access needs                 |
| 🔄 **Versioning**          | Keeps previous object versions                |
| 📜 **IAM Policy**          | Identity permissions                          |
| 🪣 **Bucket Policy**       | Bucket resource permissions                   |
| 📋 **ACL**                 | Older access control                          |
| 🚫 **Block Public Access** | Helps prevent public access                   |
| 🔒 **Encryption**          | Protects stored data                          |
| 🌐 **Static Website**      | Hosts static website files                    |
| ♻️ **Lifecycle**           | Automatically manages objects over time       |
| 🔄 **Replication**         | Copies objects to another bucket              |
| 🚀 **Transfer Acceleration**| Faster long-distance transfers               |
| 🧩 **Multipart Upload**    | Upload large file in smaller parts            |
| 🔔 **Event Notification**  | S3 tells another service something happened   |

---

## 🗺️ S3 Learning Map

```text
                          ☁️ AWS S3
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
    BASICS                  STORAGE                  SECURITY
      │                        │                        │
      ├── Bucket               └── Storage Classes      ├── IAM Policy
      ├── Object                                        ├── Bucket Policy
      └── Object Key                                    ├── ACL
                                                        ├── Block Public Access
      │                                                 └── Encryption
      ▼
  MANAGEMENT
      │
      ├── Versioning
      ├── Lifecycle
      └── Replication (SRR / CRR)
      │
      ▼
  PERFORMANCE
      │
      ├── Transfer Acceleration
      └── Multipart Upload
      │
      ▼
   FEATURES
      │
      ├── Static Website Hosting
      └── Event Notifications
```

---

## ⭐ S3 Final Memory

```text
S3
 │
 ├── What is it?
 │      └── Object Storage
 │
 ├── Where do files live?
 │      └── Bucket
 │
 ├── What is a file called?
 │      └── Object
 │
 ├── How to save cost?
 │      └── Storage Classes + Lifecycle
 │
 ├── How to keep old versions?
 │      └── Versioning
 │
 ├── Who can access?
 │      └── IAM Policy + Bucket Policy
 │
 ├── How to protect stored data?
 │      └── Encryption
 │
 ├── How to copy to another bucket?
 │      └── Replication (SRR / CRR)
 │
 ├── How to host a website?
 │      └── Static Website Hosting
 │
 └── How to upload large files?
        └── Multipart Upload
```

---

# 🌐 PART 5 — VPC — Virtual Private Cloud

> **VPC = Our Own Private Network in AWS**

---

## 5.1 🌐 What is VPC?

> **VPC = Virtual Private Cloud**

### 📖 Technical Definition

Amazon VPC is an AWS service that lets us create our own **logically isolated private network inside the AWS Cloud**.

We control the network, such as:

- 🌐 IP address range
- 🧩 Subnets
- 🛣️ Route tables
- 🚪 Gateways
- 🛡️ Security rules

We launch AWS resources like **EC2, RDS and Load Balancers** inside our VPC.

#### 🧠 Easy Memory

> **VPC = Our Own Private Network in AWS**

#### 🏠 Simple Example

```text
☁️ AWS Cloud = A Big City

🌐 VPC       = Our Own Gated Society in that City

🧩 Subnet    = Different Blocks inside the Society

🚪 Gate      = Internet Gateway
```

---

## 5.2 🤔 Why Do We Use VPC?

If a company wants to run applications on AWS, it needs a **secure and controlled network**.

### ❌ Traditionally

```text
🖥️ Buy Routers and Switches
         ↓
🔌 Setup Cables
         ↓
🔢 Configure IP Addresses
         ↓
🔥 Setup Firewall
         ↓
🖥️ Connect Servers
```

### ✅ With AWS VPC

```text
☁️ AWS
 ↓
🌐 Create VPC
 ↓
🧩 Create Subnets
 ↓
🚪 Attach Gateway
 ↓
🛡️ Configure Routes and Security
 ↓
🖥️ Launch Resources
```

#### ⭐ Main Reasons

- ❌ No need to buy physical network devices
- 🔒 Our network is isolated from other AWS customers
- 🎛️ Full control over IP range, subnets and routing
- 🗄️ Keep important resources (like databases) private
- 🛡️ Control incoming and outgoing traffic

---

## 5.3 🧰 What Does VPC Provide?

VPC provides:

- 🌐 Private IP address range (CIDR)
- 🧩 Subnets
- 🛣️ Route Tables
- 🚪 Internet Gateway
- 🔁 NAT Gateway
- 🛡️ Security Groups
- 🚧 Network ACLs
- 🔗 VPC Peering
- 🔌 VPC Endpoints
- 📊 Flow Logs for traffic monitoring

#### ⚠️ Important

> **A VPC belongs to one AWS Region, but it spans all Availability Zones in that Region.**

> **A Subnet belongs to only one Availability Zone.**

```text
🌏 Region
│
└── 🌐 VPC
     │
     ├── 🏢 Availability Zone A
     │       └── 🧩 Subnet 1
     │
     └── 🏢 Availability Zone B
             └── 🧩 Subnet 2
```

---

## 5.4 🏠 Default VPC vs Custom VPC

### 5.4.1 🏠 Default VPC

AWS automatically creates a **Default VPC** in every Region for our account.

- ✅ Comes ready to use
- 🧩 Has default subnets (one in each AZ)
- 🚪 Has an Internet Gateway already attached
- 📏 Default CIDR is `172.31.0.0/16`
- 🧪 Good for quick testing

### 5.4.2 🛠️ Custom VPC

A VPC that **we create ourselves**.

- 📏 We choose the CIDR block
- 🧩 We create our own subnets
- 🎛️ We control routing and security
- 🏭 Best for real projects and production

### 📊 Comparison

| Feature         | 🏠 Default VPC     | 🛠️ Custom VPC          |
| --------------- | ------------------ | ---------------------- |
| Created by      | AWS automatically  | Us                     |
| CIDR            | 172.31.0.0/16      | We choose              |
| Subnets         | Already created    | We create              |
| Internet access | Ready to use       | We must configure      |
| Best for        | Quick testing      | Production / Projects  |

---

## 5.5 📏 CIDR Block

> **CIDR = Classless Inter-Domain Routing**

A **CIDR Block** is the **range of IP addresses** of our VPC.

When we create a VPC, we must give it a CIDR block.

#### 💻 Example

```text
10.0.0.0/16
```

This has two parts:

```text
10.0.0.0   → Starting IP address
/16        → Size of the network
```

### 📏 Allowed VPC Size

```text
Largest  VPC → /16  (65,536 IPs)
Smallest VPC → /28  (16 IPs)
```

### 🔢 Quick Idea of Sizes

| CIDR  | Total IPs |
| ----- | --------: |
| /16   |    65,536 |
| /20   |     4,096 |
| /24   |       256 |
| /28   |        16 |

#### 🧠 Easy Memory

```text
Smaller number after /  = Bigger network
Bigger number after /   = Smaller network
```

### 🏠 Private IP Ranges Used in VPC

AWS recommends using these private ranges:

```text
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```

#### ⚠️ Important

> Do not use **overlapping CIDR ranges** if you want to connect two VPCs later (VPC Peering will not work).

---

## 5.6 🧩 Subnet

A **Subnet** is a **smaller part (range of IPs) of a VPC**.

We divide our VPC into subnets to organize and secure our resources.

```text
🌐 VPC  10.0.0.0/16
│
├── 🧩 Subnet 1  10.0.1.0/24
├── 🧩 Subnet 2  10.0.2.0/24
└── 🧩 Subnet 3  10.0.3.0/24
```

#### 🧠 Simple Meaning

> **Subnet = A small section of the VPC network**

#### ⚠️ Important

> **One Subnet = One Availability Zone only.**

A subnet cannot stretch across multiple AZs.

### 5.6.1 🌍 Public Subnet

A subnet whose **Route Table has a route to an Internet Gateway**.

Resources here can be reached from the internet (if they have a public IP).

**Used for:**

- 🌐 Web Servers
- ⚖️ Load Balancers
- 🔁 NAT Gateway
- 🏰 Bastion Host

### 5.6.2 🔒 Private Subnet

A subnet that **does NOT have a direct route to an Internet Gateway**.

Resources here are not directly reachable from the internet.

**Used for:**

- 🗄️ Databases
- ⚙️ Backend Servers
- 🏢 Internal Applications

### 🧠 Remember

```text
🌍 Public Subnet  = Route to Internet Gateway
🔒 Private Subnet = No route to Internet Gateway
```

#### ⚠️ Important

> A subnet is called **public or private only because of its Route Table**, not because of its name.

### 5.6.3 5️⃣ Reserved IP Addresses

AWS reserves **5 IP addresses** in every subnet. We cannot use them.

Example for subnet `10.0.1.0/24`:

| IP Address   | Use                                  |
| ------------ | ------------------------------------ |
| 10.0.1.0     | Network address                      |
| 10.0.1.1     | VPC Router                           |
| 10.0.1.2     | DNS server                           |
| 10.0.1.3     | Reserved for future use              |
| 10.0.1.255   | Network broadcast address (reserved) |

So a `/24` subnet has 256 IPs, but only **251 usable** IPs.

### 5.6.4 🌍 Auto-assign Public IP

A subnet can be set to **auto-assign a public IPv4 address** to new instances launched in it.

A public subnet needs both:

```text
1. 🛣️ Route to Internet Gateway
2. 📍 Public IP (auto-assigned or Elastic IP) on the instance
```

---

## 5.7 🛣️ Route Table

A **Route Table** is a set of rules (called **routes**) that decides **where network traffic goes**.

It works like a **GPS / Road Map** for the network.

#### 💻 Example Route Table

| Destination | Target   |
| ----------- | -------- |
| 10.0.0.0/16 | local    |
| 0.0.0.0/0   | igw-xxxx |

### 📖 Understanding It

```text
10.0.0.0/16  → local
(Traffic inside the VPC stays inside the VPC)

0.0.0.0/0    → Internet Gateway
(All other traffic goes to the internet)
```

#### 🧠 Easy Memory

```text
0.0.0.0/0 = All IP addresses (Anywhere)
```

### 📌 Important Points

- 📋 Every VPC has a **Main Route Table**
- 🏠 Every route table has a **local route** by default (cannot be deleted)
- 🔗 Every subnet must be associated with a route table
- 🧩 One route table can be used by many subnets
- 1️⃣ A subnet can be associated with only one route table at a time

### 🧩 Public vs Private Route Table

```text
🌍 Public Route Table
├── 10.0.0.0/16 → local
└── 0.0.0.0/0   → Internet Gateway

🔒 Private Route Table
├── 10.0.0.0/16 → local
└── 0.0.0.0/0   → NAT Gateway   (if internet access is needed)
```

#### 🧠 Simple Meaning

> **Route Table = Road map that tells traffic where to go**

---

## 5.8 🚪 Internet Gateway (IGW)

An **Internet Gateway** is an AWS component that **connects our VPC to the internet**.

It allows:

- 🌐 Resources in the VPC to reach the internet
- 👥 Internet users to reach our public resources

#### 🧠 Simple Meaning

> **IGW = The main gate of our VPC to the internet**

### ⭐ Key Points

- 1️⃣ One VPC can have **only one** Internet Gateway attached
- ✅ It is **highly available and scalable** (managed by AWS)
- 💰 There is **no extra charge** for the IGW itself

#### Example

```text
🌍 Internet
   ↓
🚪 Internet Gateway
   ↓
🛣️ Route Table
   ↓
🌍 Public Subnet
   ↓
🖥️ EC2
```

### ✅ What Is Needed for Internet Access?

For an EC2 instance to be reachable from the internet, we need **all of these**:

```text
1. 🚪 Internet Gateway attached to VPC
2. 🛣️ Route to IGW in the subnet's Route Table
3. 📍 Public IP / Elastic IP on the instance
4. 🛡️ Security Group (and NACL) allowing the traffic
```

#### ⚠️ Important

> If even one of these is missing, internet access will not work.

### 🌍 Egress-Only Internet Gateway

Used for **IPv6** traffic. It allows **outbound only** connections to the internet and blocks incoming connections.

---

## 5.9 🔁 NAT Gateway

> **NAT = Network Address Translation**

A **NAT Gateway** allows resources in a **private subnet** to **access the internet**, but the internet **cannot start a connection** to them.

#### 🧠 Simple Meaning

> **NAT Gateway = Private servers can go out, but nobody can come in**

### 🎯 Why Do We Need It?

Private servers (like a backend or database) sometimes need internet access for:

- 🔄 Software updates
- 📦 Downloading packages
- 🌐 Calling external APIs

But we do not want the internet to reach them directly.

#### Example

```text
🖥️ Private EC2
     ↓
🛣️ Private Route Table
     ↓
🔁 NAT Gateway  (in Public Subnet)
     ↓
🚪 Internet Gateway
     ↓
🌍 Internet
```

### ⭐ Key Points

- 🌍 NAT Gateway is created in a **Public Subnet**
- 📍 It needs an **Elastic IP** (for a public NAT Gateway)
- 🛣️ The Private Route Table points `0.0.0.0/0` to the NAT Gateway
- ➡️ It is **outbound only** (allows outgoing, blocks new incoming connections)
- 🏢 It is created in **one AZ** — for high availability, create one NAT Gateway in each AZ
- 💰 It is **a paid service** (charged per hour and per GB of data)

#### ⚠️ Important

> **NAT Gateway must be in a Public Subnet**, otherwise it cannot reach the Internet Gateway.

### 🧠 IGW vs NAT Gateway

| Feature          | 🚪 Internet Gateway     | 🔁 NAT Gateway               |
| ---------------- | ----------------------- | ---------------------------- |
| Used for         | Public subnets          | Private subnets              |
| Traffic          | Inbound + Outbound      | Outbound only                |
| Placed in        | Attached to VPC         | Inside a Public Subnet       |
| Needs Elastic IP | No                      | Yes (public NAT Gateway)     |
| Cost             | No extra charge         | Paid                         |

---

## 5.10 🛡️ Security Group

A **Security Group** is a virtual firewall that controls **inbound and outbound traffic** for resources like **EC2 Instances**.

It works at the **instance level** (network interface level).

### ⭐ Key Points

- 🔄 **Stateful** — if inbound traffic is allowed, the response is automatically allowed
- ✅ Only **Allow rules** (we cannot write Deny rules)
- 🚫 All traffic is **denied by default** (inbound)
- ✅ By default, all **outbound** traffic is allowed
- 📋 Rules are based on Protocol, Port and Source/Destination
- 🔎 All rules are checked together before deciding

#### 🔐 Example Inbound Rules

| Protocol   | Port | Source    | Purpose                  |
| ---------- | ---: | --------- | ------------------------ |
| SSH        |   22 | My IP     | Admin access             |
| HTTP       |   80 | 0.0.0.0/0 | Web traffic              |
| HTTPS      |  443 | 0.0.0.0/0 | Secure web traffic       |
| MySQL      | 3306 | Web SG    | Database from web server |

#### 💡 Tip

A Security Group can use **another Security Group as the source**.

```text
Database SG
→ Allow 3306 only from Web Server SG
```

This means only our web servers can talk to the database.

#### 🧠 Simple Meaning

> **Security Group = Firewall for the instance**

---

## 5.11 🚧 Network ACL (NACL)

> **NACL = Network Access Control List**

A **NACL** is a firewall that controls **inbound and outbound traffic at the subnet level**.

### ⭐ Key Points

- 🧩 Works at the **Subnet level**
- 🔁 **Stateless** — return traffic must be allowed separately
- ✅❌ Supports both **Allow and Deny** rules
- 🔢 Rules have **rule numbers** and are checked **in order (lowest number first)**
- 🎯 The first matching rule is applied
- 🔗 Every subnet must be associated with one NACL
- 🧩 One NACL can be used for many subnets

### 📋 Default vs Custom NACL

```text
🏠 Default NACL
→ Allows all inbound and outbound traffic

🛠️ Custom NACL
→ Denies all traffic until we add Allow rules
```

#### 💻 Example Rules

| Rule # | Type | Port | Source           | Action |
| -----: | ---- | ---: | ---------------- | ------ |
|    100 | HTTP |   80 | 0.0.0.0/0        | ALLOW  |
|    110 | SSH  |   22 | 203.0.113.5/32   | ALLOW  |
|    120 | All  |  All | 198.51.100.7/32  | DENY   |
|      * | All  |  All | 0.0.0.0/0        | DENY   |

The last rule `*` is the default rule that denies everything not matched.

#### ⚠️ Important

> NACL is **stateless**. If we allow inbound traffic, we must also allow the **outbound response** (usually using ephemeral ports `1024–65535`).

#### 🧠 Simple Meaning

> **NACL = Firewall for the subnet**

---

## 5.12 ⚖️ Security Group vs NACL

| Feature          | 🛡️ Security Group                | 🚧 NACL                        |
| ---------------- | -------------------------------- | ------------------------------ |
| Works at         | Instance level                   | Subnet level                   |
| State            | **Stateful**                     | **Stateless**                  |
| Rule types       | Allow only                       | Allow and Deny                 |
| Rule evaluation  | All rules checked together       | Rules checked in number order  |
| Default behavior | Deny all inbound, allow outbound | Default NACL allows all        |
| Applies to       | Only instances using that SG     | All resources in the subnet    |

### 🧠 Easy Memory

```text
🛡️ Security Group = Guard at the Room Door  (instance)

🚧 NACL           = Guard at the Building Gate  (subnet)
```

### 🔄 Traffic Flow

```text
🌍 Internet
   ↓
🚪 Internet Gateway
   ↓
🛣️ Route Table
   ↓
🚧 NACL           (Subnet level)
   ↓
🛡️ Security Group (Instance level)
   ↓
🖥️ EC2
```

---

## 5.13 🔗 VPC Peering

**VPC Peering** is a **private network connection between two VPCs**, so resources can communicate using **private IP addresses**.

#### 🧠 Simple Meaning

> **VPC Peering = Direct private link between two VPCs**

#### Example

```text
🌐 VPC A  ◄──── Peering Connection ────►  🌐 VPC B
10.0.0.0/16                              10.1.0.0/16
```

### ⭐ Key Points

- 🔒 Traffic stays on the **AWS private network** (not on the public internet)
- 🌍 Works between VPCs in the **same Region, different Regions, or different AWS accounts**
- 📏 CIDR blocks of the two VPCs **must NOT overlap**
- 🛣️ We must **update Route Tables** on both sides
- 🛡️ We must allow the traffic in **Security Groups / NACLs**

### ⚠️ Peering Is NOT Transitive

```text
VPC A ◄────► VPC B ◄────► VPC C

A can talk to B   ✅
B can talk to C   ✅
A can talk to C   ❌  (Not automatically)
```

If A needs to talk to C, we need to create a **separate peering between A and C**.

#### 🧠 Remember

> **VPC Peering = One-to-one connection, Not Transitive**

When there are many VPCs, peering becomes difficult to manage. We then use **Transit Gateway**.

---

## 5.14 🔌 VPC Endpoints

A **VPC Endpoint** allows our VPC to connect to **AWS services privately**, without using the Internet Gateway, NAT Gateway or public internet.

#### 🧠 Simple Meaning

> **VPC Endpoint = Private path from our VPC to AWS services**

#### 🎯 Why Use It?

Suppose a private EC2 wants to access **S3**.

```text
❌ Without Endpoint
Private EC2 → NAT Gateway → Internet Gateway → S3
(Costs money and goes through internet path)

✅ With Endpoint
Private EC2 → VPC Endpoint → S3
(Private, secure, and no NAT needed)
```

### 🗂️ Types of VPC Endpoints

```text
🔌 VPC Endpoints
│
├── 🚪 Gateway Endpoint
└── 🔗 Interface Endpoint
```

#### 1️⃣ Gateway Endpoint

- Supports only **S3** and **DynamoDB**
- Added as a **route in the Route Table**
- **No extra charge**

#### 2️⃣ Interface Endpoint (AWS PrivateLink)

- Creates a **network interface (ENI) with a private IP** in our subnet
- Supports many AWS services (such as SQS, SNS, CloudWatch, etc.) and other PrivateLink services
- **Paid service** (charged per hour and per GB)

### 📊 Comparison

| Feature       | 🚪 Gateway Endpoint   | 🔗 Interface Endpoint    |
| ------------- | --------------------- | ------------------------ |
| Supported     | S3, DynamoDB          | Many AWS services        |
| How it works  | Route in Route Table  | ENI with private IP      |
| Cost          | Free                  | Paid                     |

---

## 5.15 🏢 Transit Gateway

A **Transit Gateway (TGW)** is a **central hub** that connects **many VPCs and on-premises networks** together.

Instead of creating many peering connections, every network connects to the Transit Gateway.

#### 🧠 Simple Meaning

> **Transit Gateway = Central Hub connecting many networks**

### ❌ Without Transit Gateway (Peering)

```text
VPC A ──── VPC B
  │ ╲      ╱ │
  │   ╲  ╱   │
  │   ╱  ╲   │
  │ ╱      ╲ │
VPC C ──── VPC D

(Many connections — hard to manage)
```

### ✅ With Transit Gateway

```text
        VPC A
          │
VPC D ── Transit ── VPC B
         Gateway
          │
        VPC C
```

### ⭐ Key Points

- 🕸️ Works as a **Hub-and-Spoke** model
- 🔢 Reduces the number of connections
- 🧰 Easier to manage when we have many VPCs
- 🔐 Can also connect **VPN** and **Direct Connect** to AWS

---

## 5.16 🔐 VPN and Direct Connect

These services connect our **on-premises network (office / data center)** to **AWS VPC**.

### 5.16.1 🔐 Site-to-Site VPN

A **secure, encrypted connection** between our office network and our VPC **over the public internet**.

- ⚡ Quick to setup
- 🔒 Encrypted traffic
- 💰 Cost is lower
- 🌐 Speed depends on the internet

### 5.16.2 ⚡ AWS Direct Connect

A **dedicated private network connection** from our office/data center to AWS.

- 🚫 Does **not** use the public internet
- 📶 More stable and consistent network performance
- 🚀 Higher speed
- ⏳ Takes more time and cost to setup

### 📊 Comparison

| Feature        | 🔐 Site-to-Site VPN   | ⚡ Direct Connect            |
| -------------- | --------------------- | ---------------------------- |
| Connection     | Over the internet     | Dedicated private line       |
| Setup          | Quick                 | Takes longer                 |
| Cost           | Lower                 | Higher                       |
| Performance    | Depends on internet   | Stable and consistent        |

#### 🧠 Easy Memory

```text
🔐 VPN            = Secure tunnel over the internet
⚡ Direct Connect = Own private cable to AWS
```

---

## 5.17 📊 VPC Flow Logs

**VPC Flow Logs** capture **information about the IP traffic going to and from network interfaces** in our VPC.

#### 🎯 Used For

- 🛠️ Troubleshooting connectivity issues
- 🔍 Security monitoring
- 🕵️ Finding who is accessing our resources
- ✅❌ Checking whether traffic is accepted or rejected

### 📍 Flow Logs Can Be Created At

- 🌐 VPC level
- 🧩 Subnet level
- 🔌 Network Interface (ENI) level

### 📤 Flow Logs Can Be Sent To

- 📈 Amazon CloudWatch Logs
- 🪣 Amazon S3
- 🔥 Amazon Data Firehose

#### 💻 A Flow Log Record Shows

- Source IP and Destination IP
- Source Port and Destination Port
- Protocol
- Action — **ACCEPT** or **REJECT**

#### ⚠️ Important

> Flow Logs do **NOT** capture the actual content (data) of the packets. They only record **traffic information**.

---

## 5.18 🏰 Bastion Host

A **Bastion Host** is a small EC2 instance in a **Public Subnet** used as a **secure entry point** to reach servers in **Private Subnets**.

```text
👨‍💻 Admin
    ↓ SSH
🏰 Bastion Host  (Public Subnet)
    ↓ SSH
🖥️ Private EC2   (Private Subnet)
```

#### ⭐ Key Points

- 🔐 Allow SSH to the bastion **only from our trusted IP**
- 🛡️ Private servers allow SSH **only from the bastion's Security Group**
- 💡 A safer modern option is **AWS Systems Manager Session Manager** (no open SSH port needed)

> **Bastion Host = Secure jump server to reach private servers**

---

## 5.19 🏗️ Real Example: Public + Private Architecture

This is the most common VPC design.

### 🎯 Requirement

- 🌐 Website should be reachable from the internet
- 🗄️ Database should be **private** and safe

### 🏗️ Architecture

```text
                        🌍 Internet
                           │
                           ▼
                  🚪 Internet Gateway
                           │
┌──────────────────────── 🌐 VPC 10.0.0.0/16 ──────────────────────┐
│                          │                                       │
│   ┌──────────────── 🌍 Public Subnet 10.0.1.0/24 ────────────┐   │
│   │   🖥️ Web Server (EC2)             🔁 NAT Gateway         │   │
│   └──────────────────────────────────────────────────────────┘   │
│                          │                                       │
│                          ▼                                       │
│   ┌──────────────── 🔒 Private Subnet 10.0.2.0/24 ───────────┐   │
│   │   🗄️ Database (RDS / EC2)                                │   │
│   └──────────────────────────────────────────────────────────┘   │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 🪜 Steps to Build It

```text
1. Create VPC            → 10.0.0.0/16
2. Create Public Subnet  → 10.0.1.0/24
3. Create Private Subnet → 10.0.2.0/24
4. Create Internet Gateway and attach to VPC
5. Create Public Route Table  → 0.0.0.0/0 → IGW
6. Associate Public Route Table with Public Subnet
7. Create NAT Gateway in Public Subnet (with Elastic IP)
8. Create Private Route Table → 0.0.0.0/0 → NAT Gateway
9. Associate Private Route Table with Private Subnet
10. Create Security Groups (Web SG, DB SG)
11. Launch EC2 / RDS in the correct subnets
```

### 🔐 Security Group Setup

```text
Web SG
├── Allow HTTP  80  from 0.0.0.0/0
├── Allow HTTPS 443 from 0.0.0.0/0
└── Allow SSH   22  from My IP

DB SG
└── Allow MySQL 3306 from Web SG only
```

---

## 📌🧠 VPC Quick Revision

```text
🌐 VPC
│
├── 🔢 IP Addressing
│   └── 📏 CIDR Block
│
├── 🧩 Network Layout
│   ├── Subnet
│   │   ├── 🌍 Public Subnet
│   │   └── 🔒 Private Subnet
│   └── 🛣️ Route Table
│
├── 🚪 Gateways
│   ├── Internet Gateway
│   └── NAT Gateway
│
├── 🛡️ Security
│   ├── Security Group
│   └── Network ACL
│
├── 🔗 Connectivity
│   ├── VPC Peering
│   ├── VPC Endpoints
│   ├── Transit Gateway
│   ├── Site-to-Site VPN
│   └── Direct Connect
│
└── 📊 Monitoring
    └── VPC Flow Logs
```

---

## 🧠⚡ VPC One-Line Memory

| Concept                    | Easy Memory                             |
| -------------------------- | --------------------------------------- |
| 🌐 **VPC**                 | Our Own Private Network in AWS          |
| 📏 **CIDR Block**          | IP Address Range of the VPC             |
| 🧩 **Subnet**              | Small Section of the VPC (One AZ)       |
| 🌍 **Public Subnet**       | Has Route to Internet Gateway           |
| 🔒 **Private Subnet**      | No Direct Route to Internet             |
| 🛣️ **Route Table**         | Decides Where Traffic Goes              |
| 🚪 **Internet Gateway**    | Gate of VPC to the Internet             |
| 🔁 **NAT Gateway**         | Private Servers Go Out, No One Comes In |
| 🛡️ **Security Group**      | Firewall for Instance (Stateful)        |
| 🚧 **NACL**                | Firewall for Subnet (Stateless)         |
| 🔗 **VPC Peering**         | Private Link Between 2 VPCs             |
| 🔌 **VPC Endpoint**        | Private Path to AWS Services            |
| 🏢 **Transit Gateway**     | Central Hub for Many Networks           |
| 🔐 **VPN**                 | Secure Tunnel Over Internet             |
| ⚡ **Direct Connect**      | Private Dedicated Line to AWS           |
| 📊 **Flow Logs**           | Records of Network Traffic              |
| 🏰 **Bastion Host**        | Secure Jump Server                      |

---

## 🗺️ VPC Learning Map

```text
                          ☁️ AWS VPC
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        ▼                      ▼                      ▼
    ADDRESSING              ROUTING                SECURITY
        │                      │                      │
        └── CIDR Block         ├── Route Table        ├── Security Group
                               ├── Internet Gateway   └── NACL
                               └── NAT Gateway
                               │
                               ▼
                           SUBNETS
                               │
                               ├── Public Subnet
                               └── Private Subnet
                               │
                               ▼
                         CONNECTIVITY
                               │
                               ├── VPC Peering
                               ├── VPC Endpoints
                               ├── Transit Gateway
                               ├── VPN
                               └── Direct Connect
                               │
                               ▼
                          MONITORING
                               │
                               └── VPC Flow Logs
```

---

## ⭐ VPC Final Memory

```text
VPC
 │
 ├── What is it?
 │      └── Our Private Network in AWS
 │
 ├── How big is the network?
 │      └── CIDR Block
 │
 ├── How to divide it?
 │      └── Subnets
 │
 ├── How does traffic find its way?
 │      └── Route Table
 │
 ├── How to connect to the internet?
 │      └── Internet Gateway
 │
 ├── How can private servers go online?
 │      └── NAT Gateway
 │
 ├── How to secure the instance?
 │      └── Security Group
 │
 ├── How to secure the subnet?
 │      └── NACL
 │
 ├── How to connect two VPCs?
 │      └── VPC Peering
 │
 ├── How to reach AWS services privately?
 │      └── VPC Endpoints
 │
 ├── How to connect many VPCs?
 │      └── Transit Gateway
 │
 ├── How to connect office to AWS?
 │      └── VPN / Direct Connect
 │
 └── How to monitor traffic?
        └── VPC Flow Logs
```

---

# 🗄️ PART 6 — RDS — Relational Database Service

> **RDS = Managed Relational Database in AWS**

---

## 6.1 🗄️ What is RDS?

> **RDS = Relational Database Service**

Amazon RDS is an AWS service that makes it easy to **set up, run and scale a relational database in the cloud**.

AWS manages the routine database work for us, such as:

- 🖥️ Hardware setup
- 💿 Operating system patching
- 📸 Backups
- 🔄 Software updates
- 🛡️ Failover (with Multi-AZ)

We only focus on our **data and application**.

#### 📋 What is a Relational Database?

A relational database stores data in **tables (rows and columns)**.

```text
📋 Students Table
┌────┬─────────┬────────┐
│ ID │ Name    │ City   │
├────┼─────────┼────────┤
│ 1  │ Rahul   │ Pune   │
│ 2  │ Sara    │ Delhi  │
└────┴─────────┴────────┘
```

We use **SQL** to work with this data.

#### 🏗️ RDS Basic Architecture

```text
👤 User / Application
        │
        ▼
    🗄️ RDS Endpoint
        │
        ▼
  🖥️ DB Instance
        │
        ▼
   💾 EBS Storage
```

#### 🧠 Easy Memory

> **RDS = Managed Relational Database in AWS**

---

## 6.2 🤔 Why Do We Use RDS?

Suppose a company needs a database for its application.

### ❌ Traditionally (Self-Managed Database)

```text
🖥️ Buy Physical Server
        ↓
💿 Install Operating System
        ↓
🛢️ Install Database Software
        ↓
🔧 Configure and Tune Database
        ↓
📸 Setup Backups Manually
        ↓
🔄 Do Patching and Updates
        ↓
📦 Store Data
```

### ✅ With RDS

```text
☁️ AWS
 ↓
🗄️ Create RDS Database
 ↓
⚙️ Select Engine and Instance Class
 ↓
🔐 Configure Security
 ↓
📦 Connect Application and Store Data
```

#### ⭐ Main Reasons

- ❌ No need to install and manage database software on servers
- 📸 Automated backups
- 🔄 Easy software patching
- 🛡️ High availability with Multi-AZ
- 📈 Easy to scale (instance size and storage)
- 📖 Read Replicas for better read performance
- 🔒 Encryption support
- 📊 Monitoring with CloudWatch

---

## 6.3 🧰 What Does RDS Provide?

RDS provides:

- 🖥️ DB Instances
- 🛢️ Multiple Database Engines
- ⚙️ Different Instance Classes
- 💾 Storage Options
- 🛡️ Multi-AZ High Availability
- 📖 Read Replicas
- 📸 Automated Backups and Snapshots
- 🔒 Encryption
- 🔐 Network Security (VPC, Security Groups)
- 📊 Monitoring (CloudWatch, Performance Insights)
- 🔄 Automatic Maintenance and Patching

#### ⚠️ Important

> **In RDS, we cannot SSH into the database server or access its operating system.**

AWS manages the OS. We only access the **database** using its endpoint.

---

## 6.4 🧱 RDS Basic Concepts

### 6.4.1 🖥️ DB Instance

A **DB Instance** is the **database server running in AWS**.

It runs a database engine and has its own CPU, memory and storage.

```text
🗄️ DB Instance
├── 🛢️ Database Engine (MySQL, PostgreSQL ...)
├── 🧠 CPU and Memory (Instance Class)
├── 💾 Storage
└── 🌐 Network
```

> **DB Instance = Database Server in RDS**

---

### 6.4.2 🛢️ DB Engine

A **DB Engine** is the **database software** that runs on the DB Instance.

Examples: MySQL, PostgreSQL, MariaDB, Oracle, SQL Server.

> **DB Engine = Database Software**

---

### 6.4.3 ⚙️ DB Instance Class

The **DB Instance Class** decides the **compute power** (CPU and RAM) of the DB Instance.

Examples:

```text
db.t3.micro
db.m5.large
db.r5.large
```

> **DB Instance Class = Power of the Database Server**

---

### 6.4.4 🌐 Endpoint

An **Endpoint** is the **address (DNS name)** used by our application to connect to the database.

#### Example

```text
mydb.abc123xyz.ap-south-1.rds.amazonaws.com
```

Our application connects to this endpoint with a port (for example, MySQL uses `3306`).

#### 💡 Important

Always connect using the **endpoint name**, not an IP address. During failover, AWS changes the target behind the endpoint automatically.

> **Endpoint = Connection Address of the Database**

---

### 6.4.5 🧩 DB Subnet Group

A **DB Subnet Group** is a collection of **subnets** in a VPC where RDS can place the DB Instance.

```text
🌐 VPC
│
└── 🧩 DB Subnet Group
      ├── 🔒 Private Subnet (AZ-a)
      └── 🔒 Private Subnet (AZ-b)
```

#### ⚠️ Important

> A DB Subnet Group must have subnets in **at least 2 Availability Zones**.

> **DB Subnet Group = Subnets where RDS can run**

---

### 6.4.6 🔧 Parameter Group

A **Parameter Group** is a collection of **database engine settings** (configuration values).

Instead of editing a config file on a server, we change settings using a Parameter Group.

#### Example Settings

- Maximum connections
- Character set
- Time zone

> **Parameter Group = Database Configuration Settings**

---

### 6.4.7 🧰 Option Group

An **Option Group** is used to enable **extra features** for some database engines (for example, Oracle and SQL Server).

> **Option Group = Extra Database Features**

---

## 6.5 🛢️ Supported Database Engines

RDS supports multiple database engines.

```text
🛢️ RDS Engines
│
├── 🌟 Amazon Aurora (MySQL and PostgreSQL compatible)
├── 🐬 MySQL
├── 🐘 PostgreSQL
├── 🦭 MariaDB
├── 🔶 Oracle
├── 🪟 Microsoft SQL Server
└── 🏢 IBM Db2
```

#### 📊 Quick Idea

| Engine         | Type                                  |
| -------------- | ------------------------------------- |
| Aurora         | AWS-built, MySQL/PostgreSQL compatible|
| MySQL          | Popular open source                   |
| PostgreSQL     | Open source, advanced features        |
| MariaDB        | Open source, MySQL-like               |
| Oracle         | Commercial (license needed)           |
| SQL Server     | Commercial (Microsoft)                |
| Db2            | Commercial (IBM)                      |

#### 🧠 Remember

> **Open Source Engines = No license fee** (MySQL, PostgreSQL, MariaDB)

> **Commercial Engines = License needed** (Oracle, SQL Server, Db2)

---

## 6.6 ⚙️ DB Instance Classes

Different applications need different power.

RDS provides different **Instance Class families**.

```text
⚙️ DB Instance Classes
│
├── 🟢 Standard (m)
├── 🧠 Memory Optimized (r, x)
└── 💡 Burstable (t)
```

### 6.6.1 🟢 Standard Classes (m)

Balanced CPU and memory.

**Used for:** General database workloads.

**Examples:**

```text
db.m5.large
db.m6g.large
```

> **Standard = Balanced CPU + RAM**

---

### 6.6.2 🧠 Memory Optimized Classes (r, x)

More memory for each CPU.

**Used for:** Large databases and memory-heavy workloads.

**Examples:**

```text
db.r5.large
db.r6g.large
```

> **Memory Optimized = More RAM**

---

### 6.6.3 💡 Burstable Classes (t)

Gives a **baseline CPU performance** and can **burst** to higher performance when needed.

**Used for:** Development, testing, small websites and low-traffic apps.

**Examples:**

```text
db.t3.micro
db.t3.medium
```

> **Burstable = Low cost, good for dev/test**

---

## 6.7 💾 RDS Storage

RDS uses **EBS volumes** to store database data.

#### 📊 Storage Types

```text
💾 RDS Storage
│
├── 🟢 General Purpose SSD (gp2 / gp3)
├── ⚡ Provisioned IOPS SSD (io1 / io2)
└── 🕰️ Magnetic (Old / legacy)
```

### 6.7.1 🟢 General Purpose SSD (gp2 / gp3)

Good for most workloads.

**Used for:** Small and medium databases, dev/test, general applications.

> **General Purpose SSD = Default choice for most databases**

---

### 6.7.2 ⚡ Provisioned IOPS SSD (io1 / io2)

For applications needing **fast and consistent I/O performance**.

**Used for:** Production databases, I/O-heavy applications.

> **Provisioned IOPS = High and consistent performance**

---

### 6.7.3 🕰️ Magnetic Storage

An **older** storage type kept for backward compatibility.

AWS recommends using SSD storage for new databases.

---

### 6.7.4 📈 Storage Auto Scaling

**Storage Auto Scaling** automatically increases the storage when the database is running out of space.

```text
💾 Storage Almost Full
        ↓
📈 RDS Increases Storage Automatically
        ↓
✅ No Downtime for Storage Increase
```

We set a **maximum storage limit**, and RDS will not grow beyond it.

> **Storage Auto Scaling = Storage grows automatically**

---

## 6.8 🛡️ Multi-AZ Deployment

**Multi-AZ** is a feature that gives **high availability** to our database.

RDS keeps a **standby copy** of our database in a **different Availability Zone**.

#### 🏗️ Multi-AZ Architecture

```text
              📱 Application
                    │
                    ▼
            🌐 RDS Endpoint
                    │
        ┌───────────┴───────────┐
        ▼                       ▼
┌────────────────┐     ┌────────────────┐
│ 🖥️ Primary DB  │ ──► │ 💤 Standby DB  │
│   (AZ-a)       │ Sync│   (AZ-b)       │
└────────────────┘     └────────────────┘
```

#### ⭐ How It Works

- Data is copied **synchronously** from Primary to Standby
- If the Primary fails, RDS **automatically fails over** to the Standby
- The **same endpoint** is used, so the application does not need changes

#### 🔄 Failover Example

```text
❌ Primary DB Fails
        ↓
🔄 RDS Detects Failure
        ↓
✅ Standby Becomes New Primary
        ↓
📱 Application Keeps Using Same Endpoint
```

#### ❓ When Does Failover Happen?

- Primary DB instance fails
- Availability Zone has an issue
- Instance type is changed
- Software patching (maintenance)

#### ⚠️ Important

> **In a normal Multi-AZ DB Instance deployment, the standby is NOT used for reading or traffic.** It is only for failover.

> Multi-AZ is for **High Availability**, not for **performance**.

#### 🧠 Simple Meaning

> **Multi-AZ = Standby copy in another AZ for automatic failover**

#### 💡 Extra Note

RDS also has **Multi-AZ DB Cluster** deployment (for MySQL and PostgreSQL), where the standby instances can also be used to **read data**. For basic learning, remember the Multi-AZ DB Instance concept first.

---

## 6.9 📖 Read Replicas

A **Read Replica** is a **read-only copy** of our main database.

It is used to **reduce the load** on the main database by sending read queries to the replica.

#### 🏗️ Read Replica Architecture

```text
              📱 Application
              │            │
         ✏️ Write      📖 Read
              │            │
              ▼            ▼
     ┌──────────────┐   ┌────────────────┐
     │ 🖥️ Primary DB │──►│ 📖 Read Replica│
     └──────────────┘   └────────────────┘
                Async Replication
```

#### ⭐ Key Points

- Data is copied **asynchronously** from the Primary to the Replica
- Replicas are **read-only** (SELECT queries)
- A Read Replica has its **own endpoint**
- We can create **multiple Read Replicas**
- Replicas can be in the **same Region or a different Region**
- A Read Replica can be **promoted** to become a standalone database

#### 🎯 Used For

- 📈 Improving read performance
- 📊 Reports and analytics queries
- 🌍 Serving users in another Region
- 🛡️ Disaster recovery (by promoting a replica)

#### ⚠️ Important

> Because replication is **asynchronous**, a Read Replica may be **slightly behind** the Primary (called **replica lag**).

#### 🧠 Simple Meaning

> **Read Replica = Read-only copy to improve read performance**

---

## 6.10 ⚖️ Multi-AZ vs Read Replica

This is a very common confusion.

| 🛡️ Multi-AZ                      | 📖 Read Replica                     |
| -------------------------------- | ----------------------------------- |
| Used for **High Availability**   | Used for **Read Performance**       |
| **Synchronous** replication      | **Asynchronous** replication        |
| Standby is not used for reading (in Multi-AZ DB Instance) | Can be used for reading |
| **Automatic failover**           | Manual promotion needed             |
| Same endpoint after failover     | Has its own separate endpoint       |
| Within the same Region (different AZ) | Same Region or different Region |

#### 🧠 Easy Memory

```text
🛡️ Multi-AZ
     ↓
Failure protection (Backup server ready)

📖 Read Replica
     ↓
Speed (More servers to read from)
```

---

## 6.11 📸 Backups and Snapshots

RDS gives two ways to back up our database.

```text
📸 RDS Backups
│
├── 🤖 Automated Backups
└── 🖐️ Manual Snapshots
```

### 6.11.1 🤖 Automated Backups

RDS automatically takes **daily backups** and stores **transaction logs**.

#### ⭐ Key Points

- Retention period can be set from **1 to 35 days**
- Allows **Point-in-Time Recovery (PITR)**
- Taken during a **backup window**
- Automated backups are **deleted when the DB instance is deleted** (unless we choose otherwise)

#### ⏪ Point-in-Time Recovery

We can restore the database to **any specific time** within the retention period.

```text
🕐 10:00 AM  → Database OK
🕑 11:30 AM  → Someone deletes important data ❌
🕒 11:35 AM  → Restore to 11:29 AM ✅
```

> **PITR = Restore database to a specific time**

---

### 6.11.2 🖐️ Manual Snapshots

A **Manual Snapshot** is a backup that **we create ourselves**.

#### ⭐ Key Points

- We take it whenever we want
- It is **kept until we delete it**
- It stays even after the DB instance is deleted
- Can be **copied** to another Region
- Can be **shared** with other AWS accounts

> **Manual Snapshot = Backup we take and keep as long as we want**

---

### 📊 Automated Backup vs Manual Snapshot

| 🤖 Automated Backup             | 🖐️ Manual Snapshot             |
| ------------------------------- | ------------------------------ |
| Taken automatically by RDS      | Taken by us                    |
| Retention: 1 to 35 days         | Kept until we delete it        |
| Supports Point-in-Time Recovery | Restores to snapshot time only |
| Deleted with the DB instance (by default) | Stays after DB deletion |

---

### 6.11.3 🔁 Restoring a Database

#### ⚠️ Important

> **Restoring a backup or snapshot always creates a NEW DB instance** (with a new endpoint). It does not overwrite the existing one.

```text
📸 Snapshot / Backup
        ↓
🔁 Restore
        ↓
🆕 New DB Instance (New Endpoint)
```

---

## 6.12 🔐 RDS Security

RDS security has many layers.

```text
🔐 RDS Security
│
├── 🌐 VPC (Network Isolation)
├── 🧩 Private Subnets
├── 🛡️ Security Groups
├── 👤 Database Users and Passwords
├── 📜 IAM
├── 🗝️ AWS Secrets Manager
└── 🔒 Encryption
```

### 6.12.1 🌐 VPC and Private Subnet

RDS runs inside a **VPC**.

For safety, we place the database in a **Private Subnet** so the internet cannot reach it directly.

> **Best Practice: Keep databases in private subnets.**

---

### 6.12.2 🛡️ Security Group

A Security Group controls **who can connect** to the database.

#### 🔐 Example Inbound Rule

| Type          | Port | Source        | Purpose                     |
| ------------- | ---: | ------------- | --------------------------- |
| MySQL/Aurora  | 3306 | Web Server SG | Only web servers can connect|

#### 📌 Common Database Ports

| Engine      | Default Port |
| ----------- | -----------: |
| MySQL       |         3306 |
| MariaDB     |         3306 |
| PostgreSQL  |         5432 |
| Oracle      |         1521 |
| SQL Server  |         1433 |

#### ⚠️ Important

> Do **not** open the database port to `0.0.0.0/0` (the entire internet).

---

### 6.12.3 🌍 Public Accessibility

RDS has a setting called **Publicly Accessible**.

```text
Publicly Accessible = No   → Only reachable from inside the VPC (Recommended)
Publicly Accessible = Yes  → Gets a public IP and can be reached from the internet
```

#### 💡 Tip

Keep it **No** for production databases.

---

### 6.12.4 📜 IAM

IAM controls **who can manage RDS** (create, delete, modify databases).

IAM can also be used for **IAM Database Authentication**, so users can log in with a temporary token instead of a password (supported for some engines).

---

### 6.12.5 🗝️ AWS Secrets Manager

Instead of storing the database password inside application code, we can store it in **AWS Secrets Manager**.

It can also **rotate passwords automatically**.

> **Never hard-code database passwords in your code.**

---

## 6.13 🔒 Encryption

RDS supports encryption to protect data.

```text
🔒 RDS Encryption
│
├── 💾 Encryption at Rest
└── 🌐 Encryption in Transit
```

### 6.13.1 💾 Encryption at Rest

Protects data **stored on disk**, including:

- Database storage
- Automated backups
- Snapshots
- Read Replicas

RDS uses **AWS KMS** keys for this.

#### ⚠️ Important

> **Encryption at rest is selected when the DB instance is created.** We cannot directly turn it on for an existing unencrypted DB instance.

#### 🔁 How to Encrypt an Existing Unencrypted Database

```text
🗄️ Unencrypted DB
        ↓
📸 Take Snapshot
        ↓
📋 Copy Snapshot with Encryption Enabled
        ↓
🔁 Restore from Encrypted Snapshot
        ↓
🔒 New Encrypted DB
```

---

### 6.13.2 🌐 Encryption in Transit

Protects data **while it travels** between the application and the database.

It uses **SSL/TLS**.

#### 🧠 Easy Memory

```text
💾 At Rest     → Data stored on disk is protected
🌐 In Transit  → Data moving on the network is protected
```

---

## 6.14 📊 Monitoring

RDS provides different tools to monitor database health and performance.

```text
📊 RDS Monitoring
│
├── 📈 CloudWatch Metrics
├── 🔬 Enhanced Monitoring
├── 🚀 Performance Insights
└── 🔔 RDS Events
```

### 6.14.1 📈 CloudWatch Metrics

Basic metrics collected automatically.

**Examples:**

- CPU Utilization
- Database Connections
- Free Storage Space
- Read/Write IOPS
- Replica Lag

---

### 6.14.2 🔬 Enhanced Monitoring

Gives **detailed operating system level metrics** (like memory and process information) of the DB instance.

---

### 6.14.3 🚀 Performance Insights

Helps us **find performance problems** in the database, such as slow queries.

> **Performance Insights = Find what is slowing the database**

---

### 6.14.4 🔔 RDS Events

RDS sends notifications for events such as:

- Failover
- Backup completed
- Low storage
- Maintenance

These can be sent using **Amazon SNS**.

---

## 6.15 🔌 RDS Proxy

**RDS Proxy** is a managed service that sits **between the application and the database**.

It **pools and shares database connections**.

#### 🏗️ Architecture

```text
📱 Application (Many Connections)
          │
          ▼
    🔌 RDS Proxy
   (Connection Pool)
          │
          ▼
    🗄️ RDS Database
   (Fewer Connections)
```

#### ⭐ Benefits

- 🔌 Reduces load caused by many connections
- ⚡ Faster and smoother failover handling
- 🔐 Can use IAM authentication and Secrets Manager
- 📈 Useful for applications such as **AWS Lambda** that open many short connections

> **RDS Proxy = Connection pool in front of RDS**

---

## 6.16 🌟 Amazon Aurora

**Amazon Aurora** is a database engine **built by AWS** and available through RDS.

It is **compatible with MySQL and PostgreSQL**.

#### ⭐ Key Points

- Designed for **high performance and availability**
- Data is stored in a **cluster volume** that is automatically copied across **3 Availability Zones** (6 copies of data)
- Storage **grows automatically**
- Supports up to **15 Aurora Replicas**
- Faster failover than normal RDS engines

#### 🏗️ Aurora Architecture

```text
              📱 Application
              │            │
         ✏️ Writer       📖 Reader
          Endpoint       Endpoint
              │            │
              ▼            ▼
      ┌──────────┐   ┌──────────────────┐
      │ ✏️ Writer │   │ 📖 Aurora Replicas│
      │ Instance │   │ (up to 15)       │
      └────┬─────┘   └────────┬─────────┘
           └────────┬─────────┘
                    ▼
        💾 Shared Cluster Storage
      (6 copies across 3 AZs)
```

#### 🌩️ Aurora Serverless

**Aurora Serverless** automatically **adjusts database capacity** based on application demand.

Useful for **unpredictable or changing workloads**.

#### 📊 RDS (MySQL) vs Aurora

| 🐬 RDS MySQL / PostgreSQL        | 🌟 Aurora                              |
| -------------------------------- | -------------------------------------- |
| Standard open source engine on RDS | AWS-built, MySQL/PostgreSQL compatible |
| Uses EBS storage for each instance | Shared cluster storage                 |
| Up to 15 Read Replicas (supported engines) | Up to 15 Aurora Replicas       |
| Normal cost                      | Usually higher cost, higher performance|

#### 🧠 Simple Meaning

> **Aurora = AWS-built high-performance database, compatible with MySQL/PostgreSQL**

---

## 6.17 💰 RDS Pricing

RDS charges mainly depend on:

```text
💰 RDS Cost
│
├── 🖥️ DB Instance (per hour, depends on instance class)
├── 💾 Storage (per GB per month)
├── ⚡ Provisioned IOPS (if used)
├── 📸 Backup Storage (beyond free amount)
├── 🌐 Data Transfer Out
└── 🛡️ Multi-AZ (extra standby cost)
```

### 💳 Pricing Options

#### 1️⃣ On-Demand

Pay per hour for the DB instance with no long-term commitment.

> **On-Demand = Pay as You Use**

#### 2️⃣ Reserved Instances

Commit for **1 or 3 years** and get a **discount** compared to On-Demand.

Best for databases that run **continuously** (like production databases).

> **Reserved = Commit for long time, pay less**

#### 💡 Cost Tips

- Use **small burstable instances** for dev/test
- **Stop** (or delete) test databases when not needed
- Use **Reserved Instances** for production databases
- Delete **old manual snapshots** that are not needed

#### ⚠️ Important

> A **stopped** RDS instance is automatically started again after **7 days**.

> **Multi-AZ increases cost**, because we pay for the standby too.

---

## 6.18 🏗️ Real Example: EC2 + RDS Architecture

This is the most common real-world use of RDS.

### 🎯 Requirement

- Website should be reachable from the internet
- Database should be **private and safe**
- Database should be **highly available**

### 🏗️ Architecture

```text
                        🌍 Internet
                           │
                           ▼
                  🚪 Internet Gateway
                           │
┌──────────────────────── 🌐 VPC ──────────────────────────────┐
│                          │                                    │
│   ┌──────────── 🌍 Public Subnet ──────────────────────┐      │
│   │            🖥️ Web Server (EC2)                      │      │
│   └─────────────────────┬──────────────────────────────┘      │
│                         │ Port 3306                           │
│                         ▼                                     │
│   ┌──────────── 🔒 Private Subnets ────────────────────┐      │
│   │                                                    │      │
│   │   AZ-a: 🗄️ RDS Primary ───► AZ-b: 💤 RDS Standby   │      │
│   │                                                    │      │
│   └────────────────────────────────────────────────────┘      │
└───────────────────────────────────────────────────────────────┘
```

### 🪜 Steps to Build It

```text
1. Create VPC with Public and Private Subnets (2 AZs)
2. Create Security Group for Web Server (Web SG)
3. Create Security Group for Database (DB SG)
     → Allow port 3306 only from Web SG
4. Create DB Subnet Group using Private Subnets
5. Create RDS Database
     → Choose Engine and Instance Class
     → Enable Multi-AZ
     → Publicly Accessible = No
     → Select DB Subnet Group and DB SG
     → Enable Automated Backups and Encryption
6. Launch EC2 Web Server in Public Subnet
7. Connect EC2 to RDS using the RDS Endpoint
```

### 🔐 Security Group Setup

```text
Web SG
├── Allow HTTP  80  from 0.0.0.0/0
├── Allow HTTPS 443 from 0.0.0.0/0
└── Allow SSH   22  from My IP

DB SG
└── Allow MySQL 3306 from Web SG only
```

---

### ⚖️ RDS vs Database on EC2

| 🗄️ RDS (Managed)                   | 🖥️ Database on EC2 (Self-Managed)  |
| ---------------------------------- | ---------------------------------- |
| AWS manages OS and patching        | We manage OS and patching          |
| Automated backups                  | We set up backups ourselves        |
| Easy Multi-AZ and Read Replicas    | We set up replication ourselves    |
| No OS access                       | Full OS access                     |
| Less work                          | More control, more work            |

#### 🧠 Easy Memory

```text
🗄️ RDS          = Less work, AWS manages it
🖥️ DB on EC2    = More control, we manage everything
```

---

## 📌🧠 RDS Quick Revision

```text
🗄️ RDS
│
├── 🧱 Basics
│   ├── 🖥️ DB Instance
│   ├── 🛢️ DB Engine
│   ├── ⚙️ Instance Class
│   ├── 🌐 Endpoint
│   ├── 🧩 DB Subnet Group
│   └── 🔧 Parameter Group
│
├── 🛢️ Engines
│   ├── 🌟 Aurora
│   ├── 🐬 MySQL
│   ├── 🐘 PostgreSQL
│   ├── 🦭 MariaDB
│   ├── 🔶 Oracle
│   └── 🪟 SQL Server
│
├── 💾 Storage
│   ├── 🟢 General Purpose SSD
│   ├── ⚡ Provisioned IOPS
│   └── 📈 Storage Auto Scaling
│
├── 🛡️ High Availability and Scaling
│   ├── 🛡️ Multi-AZ
│   └── 📖 Read Replicas
│
├── 📸 Backup
│   ├── 🤖 Automated Backups
│   └── 🖐️ Manual Snapshots
│
├── 🔐 Security
│   ├── 🌐 VPC / Private Subnet
│   ├── 🛡️ Security Group
│   ├── 🗝️ Secrets Manager
│   └── 🔒 Encryption
│
├── 📊 Monitoring
│   ├── 📈 CloudWatch
│   └── 🚀 Performance Insights
│
└── 🔌 Extra
    └── RDS Proxy
```

---

## 🧠⚡ RDS One-Line Memory

| Concept                    | Easy Memory                                   |
| -------------------------- | --------------------------------------------- |
| 🗄️ **RDS**                | Managed Relational Database                   |
| 🖥️ **DB Instance**        | Database Server in RDS                        |
| 🛢️ **DB Engine**          | Database Software                             |
| ⚙️ **Instance Class**      | Power of the Database Server                  |
| 🌐 **Endpoint**            | Connection Address of the Database            |
| 🧩 **DB Subnet Group**     | Subnets where RDS can run                     |
| 🔧 **Parameter Group**     | Database Configuration Settings               |
| 🟢 **gp2 / gp3**           | General Purpose SSD                           |
| ⚡ **Provisioned IOPS**    | High and Consistent Performance               |
| 📈 **Storage Auto Scaling**| Storage Grows Automatically                   |
| 🛡️ **Multi-AZ**           | Standby in Another AZ for Failover            |
| 📖 **Read Replica**        | Read-Only Copy for Better Read Performance    |
| 🤖 **Automated Backup**    | Daily Backup, 1 to 35 Days, PITR              |
| 🖐️ **Manual Snapshot**    | Backup Kept Until We Delete It                |
| 🔐 **Security Group**      | Controls Who Can Connect                      |
| 🔒 **Encryption**          | Protects Stored and Moving Data               |
| 🔌 **RDS Proxy**           | Connection Pool in Front of RDS               |
| 🌟 **Aurora**              | AWS-Built High-Performance Database           |

---

## 🗺️ RDS Learning Map

```text
                          ☁️ AWS RDS
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
   DATABASE                 AVAILABILITY             SECURITY
      │                        │                        │
      ├── DB Instance          ├── Multi-AZ             ├── VPC
      ├── DB Engine            ├── Read Replica         ├── Security Group
      ├── Instance Class       └── Backups              ├── Encryption
      └── Storage                  ├── Automated        └── Secrets Manager
                                   └── Snapshots
      │
      ▼
  PERFORMANCE
      │
      ├── Read Replicas
      ├── RDS Proxy
      ├── Performance Insights
      └── Aurora
      │
      ▼
   MONITORING
      │
      ├── CloudWatch
      ├── Enhanced Monitoring
      └── RDS Events
      │
      ▼
    PRICING
      │
      ├── On-Demand
      └── Reserved Instances
```

---

## ⭐ RDS Final Memory

```text
RDS
 │
 ├── What is it?
 │      └── Managed Relational Database
 │
 ├── What runs the database?
 │      └── DB Instance
 │
 ├── Which database software?
 │      └── DB Engine
 │
 ├── How powerful?
 │      └── Instance Class
 │
 ├── How to connect?
 │      └── Endpoint
 │
 ├── Where does it run?
 │      └── DB Subnet Group (Private Subnets)
 │
 ├── How to avoid downtime?
 │      └── Multi-AZ
 │
 ├── How to improve read speed?
 │      └── Read Replica
 │
 ├── How to take backups?
 │      └── Automated Backups + Manual Snapshots
 │
 ├── How to secure it?
 │      └── Security Group + Encryption + Secrets Manager
 │
 ├── How to reduce connection load?
 │      └── RDS Proxy
 │
 └── Which AWS-built engine?
        └── Aurora
```

---

# 🧭 PART 7 — Route 53 — DNS Service

> **Route 53 = AWS DNS Service**

---

## 7.1 🧭 What is Route 53?

> **Route 53 = AWS DNS Service**

Amazon Route 53 is a **highly available and scalable DNS (Domain Name System) service**.

It helps users reach our application using a **domain name** (like `www.example.com`) instead of an IP address.

Route 53 does three main jobs:

```text
🧭 Route 53
│
├── 🏷️ Domain Registration   → Buy and manage domain names
├── 🔀 DNS Routing           → Convert domain names to IP addresses
└── ❤️ Health Checks         → Check if our servers are healthy
```

#### 💡 Why the Name "53"?

DNS uses **port 53**.

#### ⭐ Key Facts

- 🌍 Route 53 is a **global service**
- ✅ Highly available (AWS offers a 100% availability SLA for Route 53 DNS)
- 🔗 Works closely with AWS services like **ELB, CloudFront, S3, EC2 and API Gateway**

#### 🧠 Easy Memory

> **Route 53 = Phonebook of the internet + smart traffic director**

---

## 7.2 🤔 Why Do We Use Route 53?

Computers talk using **IP addresses**. Humans remember **names**.

### ❌ Without DNS

```text
👤 User must remember → 203.0.113.10
```

### ✅ With Route 53

```text
👤 User types → www.example.com
        ↓
🧭 Route 53 finds the IP
        ↓
🖥️ Browser connects to the server
```

#### ⭐ Main Reasons

- 🏷️ Use easy-to-remember domain names
- 🔀 Route users to the best server
- ❤️ Automatically avoid unhealthy servers
- 🌍 Send users to the nearest Region
- 🔗 Easily connect domain names to AWS resources
- 🔒 Create private DNS names inside a VPC

---

## 7.3 🧰 What Does Route 53 Provide?

Route 53 provides:

- 🏷️ Domain Registration
- 📂 Hosted Zones
- 📄 DNS Records
- 🔗 Alias Records
- 🔀 Routing Policies
- ❤️ Health Checks
- 🔒 Private DNS for VPCs
- 🔁 Route 53 Resolver (hybrid DNS)

---

## 7.4 🧠 DNS Basics

### 7.4.1 📖 What is DNS?

> **DNS = Domain Name System**

DNS converts a **domain name** into an **IP address**.

```text
www.example.com  ──►  DNS  ──►  203.0.113.10
```

### 7.4.2 🧱 Parts of a Domain Name

```text
        www.blog.example.com.
         │   │     │     │ │
         │   │     │     │ └── . Root
         │   │     │     └──── com  → Top-Level Domain (TLD)
         │   │     └────────── example → Second-Level Domain
         │   └──────────────── blog → Subdomain
         └──────────────────── www  → Subdomain / Host
```

#### 📖 Simple Definitions

| Term                  | Meaning                                      |
| --------------------- | -------------------------------------------- |
| 🌐 Domain Name        | Human-friendly name (example.com)            |
| 🔝 TLD                | Last part (.com, .org, .in)                  |
| 🧩 Subdomain          | Prefix before the domain (www, blog, api)    |
| 🔤 FQDN               | Full name (www.example.com.)                 |
| 🧭 Name Server        | Server that answers DNS questions            |
| 🏷️ Registrar          | Company where we buy the domain              |

### 7.4.3 🔄 How DNS Works (Step by Step)

```text
1. 👤 User types www.example.com in browser
          ↓
2. 💻 Browser asks the DNS Resolver (usually from the ISP)
          ↓
3. 🔝 Resolver asks the Root Server    → "Who knows .com?"
          ↓
4. 🏷️ Resolver asks the TLD Server     → "Who knows example.com?"
          ↓
5. 🧭 Resolver asks the Authoritative Name Server (Route 53)
          ↓
6. 🌐 Route 53 returns the IP address
          ↓
7. 💾 Resolver saves it in cache (for the TTL time)
          ↓
8. 🖥️ Browser connects to the server using the IP
```

#### 🧠 Remember

> **Route 53 acts as the Authoritative DNS** — the place that holds the final answer for our domain.

---

## 7.5 🏷️ Domain Registration

Route 53 can **register (buy) domain names**.

#### 🪜 Steps

```text
1. Open Route 53 → Registered Domains
2. Search for the domain name
3. Choose the domain and pay the yearly fee
4. Route 53 automatically creates a Hosted Zone for it
```

#### ⭐ Key Points

- 💰 The yearly price depends on the TLD (.com, .in, .org ...)
- 🔁 We can also **transfer** a domain from another registrar
- 🌍 We can buy a domain from **another registrar** (like GoDaddy) and still use Route 53 for DNS

#### 🔁 Using a Domain Bought Elsewhere

```text
1. Create a Hosted Zone in Route 53
2. Copy the 4 NS (Name Server) values of the Hosted Zone
3. Go to the registrar and replace the domain's name servers
   with the Route 53 name servers
4. ✅ Now Route 53 controls the DNS records
```

#### 🧠 Simple Meaning

> **Registrar = Where we buy the name. DNS service = Where we manage its records.**

---

## 7.6 📂 Hosted Zone

A **Hosted Zone** is a **container that holds all DNS records** for one domain.

```text
📂 Hosted Zone: example.com
│
├── 📄 A Record      → example.com      → 203.0.113.10
├── 📄 CNAME Record  → www.example.com  → example.com
├── 📄 MX Record     → Mail servers
├── 📄 NS Record     → Route 53 name servers
└── 📄 SOA Record    → Start of Authority information
```

When we create a Hosted Zone, Route 53 automatically creates **NS** and **SOA** records.

### 7.6.1 🗂️ Types of Hosted Zones

```text
📂 Hosted Zones
│
├── 🌍 Public Hosted Zone
└── 🔒 Private Hosted Zone
```

#### 🌍 Public Hosted Zone

- Answers DNS queries from the **internet**
- Used for public websites and apps
- Example: `www.example.com`

#### 🔒 Private Hosted Zone

- Answers DNS queries only **inside one or more VPCs**
- Used for internal names
- Example: `db.internal.example.com`

#### 📊 Comparison

| 🌍 Public Hosted Zone              | 🔒 Private Hosted Zone                  |
| ---------------------------------- | --------------------------------------- |
| For **internet** traffic           | For traffic inside **VPCs**             |
| Anyone on the internet can resolve | Only resources in the VPC can resolve   |
| Example: `www.example.com`         | Example: `db.internal.example.com`      |

#### ⚠️ Important

> For a **Private Hosted Zone**, the VPC must have **DNS resolution** and **DNS hostnames** enabled.

> **Hosted Zone = Container of DNS records for a domain**

---

## 7.7 📄 DNS Records

A **DNS Record** tells DNS **what to answer** for a name.

#### 🧱 Parts of a Record

| Part           | Meaning                                  |
| -------------- | ---------------------------------------- |
| 🏷️ Name        | The domain/subdomain (www.example.com)   |
| 🔠 Type        | Record type (A, CNAME ...)               |
| 🎯 Value       | The answer (IP address or name)          |
| ⏱️ TTL         | How long to cache the answer             |
| 🔀 Routing Policy | How Route 53 answers                  |

### 7.7.1 📋 Common Record Types

| Record    | Full Form / Meaning     | Used For                                      |
| --------- | ----------------------- | --------------------------------------------- |
| **A**     | Address                 | Domain → IPv4 address                         |
| **AAAA**  | IPv6 Address            | Domain → IPv6 address                         |
| **CNAME** | Canonical Name          | Domain → Another domain name                  |
| **NS**    | Name Server             | Shows which servers manage the domain         |
| **MX**    | Mail Exchange           | Email servers for the domain                  |
| **TXT**   | Text                    | Verification and security information         |
| **SOA**   | Start of Authority      | Basic information about the zone              |
| **PTR**   | Pointer                 | IP address → Domain name (reverse lookup)     |
| **SRV**   | Service                 | Location of a specific service                |
| **CAA**   | Certification Authority Authorization | Which CAs can issue certificates |

#### 💻 Examples

```text
A      example.com        → 203.0.113.10
AAAA   example.com        → 2001:db8::1
CNAME  www.example.com    → example.com
MX     example.com        → 10 mail.example.com
TXT    example.com        → "v=spf1 include:_spf.example.com ~all"
```

#### 🧠 Easy Memory

```text
A     = Name → IPv4
AAAA  = Name → IPv6
CNAME = Name → Another Name
MX    = Mail servers
NS    = Name servers
TXT   = Text / verification
```

---

## 7.8 ⏱️ TTL

> **TTL = Time To Live**

TTL tells DNS resolvers **how long to cache (remember) a record**.

```text
TTL = 300 seconds
→ Resolvers remember the answer for 5 minutes
```

#### ⚖️ High TTL vs Low TTL

| ⏱️ High TTL (like 24 hours)         | ⚡ Low TTL (like 60 seconds)         |
| ----------------------------------- | ------------------------------------ |
| Fewer DNS queries                   | More DNS queries                     |
| Lower cost                          | Higher cost                          |
| Changes take longer to reach users  | Changes reach users faster           |

#### 💡 Tip

> Before changing an important DNS record (like moving to a new server), **lower the TTL first**, then make the change.

#### ⚠️ Important

> **Alias records do not have a TTL setting.** Route 53 manages it.

---

## 7.9 🔗 CNAME Record

A **CNAME** points one domain name to **another domain name**.

```text
www.example.com  ──CNAME──►  example.com
```

#### ⚠️ Important Rule

> **A CNAME cannot be created for the root (apex) domain** such as `example.com`. It can be created only for subdomains such as `www.example.com`.

---

## 7.10 ⭐ Alias Record

An **Alias Record** is a **special Route 53 record type** that points a domain name to **selected AWS resources**.

#### 🎯 Alias Can Point To

- ⚖️ Elastic Load Balancer (ALB, NLB)
- 🌐 CloudFront distribution
- 🌱 Elastic Beanstalk environment
- 🪣 S3 static website endpoint
- 🚪 API Gateway
- 🌍 Global Accelerator
- 🔌 VPC Interface Endpoints
- 📄 Another record in the same hosted zone

#### ❌ Alias Cannot Point To

- 🖥️ An EC2 instance's DNS name

#### ⭐ Key Points

- ✅ Can be used for the **root domain** (`example.com`)
- 💰 DNS queries to Alias records pointing to AWS resources are **free**
- 🔠 Works as **A** or **AAAA** record type
- ❤️ Can use **Evaluate Target Health** (checks target health automatically)

### 7.10.1 ⚖️ CNAME vs Alias

| 🔗 CNAME                                         | ⭐ Alias                                       |
| ------------------------------------------------ | --------------------------------------------- |
| Points to any domain name                        | Points to selected AWS resources              |
| **Cannot** be used for root domain               | **Can** be used for root domain               |
| Route 53 charges for queries                     | Queries to AWS resources are free             |
| Standard DNS record type                         | Route 53-specific feature                     |
| TTL can be set                                   | TTL is managed by Route 53                    |

#### 🧠 Remember

> **Root domain pointing to a Load Balancer? Use Alias.**

---

## 7.11 🔀 Routing Policies

A **Routing Policy** decides **how Route 53 answers DNS queries**.

```text
🔀 Routing Policies
│
├── 1️⃣ Simple
├── 2️⃣ Weighted
├── 3️⃣ Latency
├── 4️⃣ Failover
├── 5️⃣ Geolocation
├── 6️⃣ Geoproximity
└── 7️⃣ Multivalue Answer
```

### 7.11.1 1️⃣ Simple Routing

One record with one or more values. No special rules.

```text
www.example.com ──► 203.0.113.10
```

- ✅ Easiest policy
- ❌ Cannot be used with Health Checks (when multiple values are given, a random value is returned to the client)

> **Simple = Basic one-to-one routing**

---

### 7.11.2 2️⃣ Weighted Routing

Send traffic in **percentages** using weights.

```text
🧭 Route 53
   ├── 70% → 🖥️ Server A (weight 70)
   ├── 20% → 🖥️ Server B (weight 20)
   └── 10% → 🖥️ Server C (weight 10)
```

#### 🎯 Used For

- 🧪 Testing a new version with a small amount of traffic
- 📦 Gradually moving traffic to a new server
- ⚖️ Load distribution

#### ⭐ Key Points

- Weight `0` = no traffic to that record
- Can be used with Health Checks

> **Weighted = Split traffic by percentage**

---

### 7.11.3 3️⃣ Latency Routing

Send the user to the **AWS Region with the lowest network delay**.

```text
🇮🇳 User in India   → 🌏 Mumbai Region
🇺🇸 User in USA     → 🌎 N. Virginia Region
🇪🇺 User in Europe  → 🌍 Ireland Region
```

#### 🎯 Used For

- ⚡ Fast response for global users
- 🌍 Apps running in multiple Regions

> **Latency = Send to the fastest Region**

---

### 7.11.4 4️⃣ Failover Routing

Uses an **Active-Passive** setup with **Health Checks**.

```text
🟢 Primary Server (Healthy)   → Gets all traffic

🔴 Primary Server (Failed)
        ↓
🟡 Secondary Server           → Takes over traffic
```

#### ⭐ Key Points

- Needs a **Health Check on the Primary** record
- Secondary can be another server, region, or a static S3 website with a "We will be back soon" page

> **Failover = Backup site takes over when main site fails**

---

### 7.11.5 5️⃣ Geolocation Routing

Route based on the **user's location** (country, continent or default).

```text
🇮🇳 India users  → Indian website
🇫🇷 France users → French-language website
🌍 Everyone else → Default website
```

#### 🎯 Used For

- 🌐 Language-based content
- 📋 Local laws and compliance
- 💰 Region-based pricing

#### ⚠️ Important

> Create a **Default** record, so users from locations we did not define still get an answer.

> **Geolocation = Route by user's country/continent**

---

### 7.11.6 6️⃣ Geoproximity Routing

Route based on the **distance** between the user and our resources.

We can use a **bias** value to send **more or less traffic** to a resource.

```text
Bias +   → Resource gets more traffic (bigger area)
Bias -   → Resource gets less traffic (smaller area)
```

> **Geoproximity = Route by distance, adjustable with bias**

---

### 7.11.7 7️⃣ Multivalue Answer Routing

Returns **multiple healthy values** (up to 8) for one query.

```text
🧭 Route 53 → returns:
   ├── 203.0.113.10  ✅
   ├── 203.0.113.11  ✅
   └── 203.0.113.12  ✅   (unhealthy ones are not returned)
```

#### ⭐ Key Points

- Can use Health Checks (only healthy values are returned)
- It is **not a replacement for a Load Balancer**, but gives simple client-side balancing

> **Multivalue = Multiple healthy answers**

---

### 📊 Routing Policy Quick Comparison

| Policy        | Easy Memory                      | Health Checks? |
| ------------- | -------------------------------- | -------------- |
| Simple        | One basic answer                 | ❌ No          |
| Weighted      | Percentage split                 | ✅ Yes         |
| Latency       | Fastest Region                   | ✅ Yes         |
| Failover      | Backup when primary fails        | ✅ Yes         |
| Geolocation   | By user's country                | ✅ Yes         |
| Geoproximity  | By distance (with bias)          | ✅ Yes         |
| Multivalue    | Many healthy answers             | ✅ Yes         |

---

## 7.12 ❤️ Health Checks

Route 53 can **check if a server or endpoint is healthy**.

```text
🧭 Route 53 Health Checkers (from many locations)
        │
        ▼
🖥️ Web Server (/health)
        │
   ┌────┴────┐
   ▼         ▼
✅ Healthy  ❌ Unhealthy
```

If a resource is unhealthy, Route 53 **stops sending traffic** to it (with policies like Failover, Weighted, Latency and Multivalue).

### 7.12.1 🗂️ Types of Health Checks

```text
❤️ Health Checks
│
├── 🌐 Endpoint Health Check
├── 🧮 Calculated Health Check
└── 📈 CloudWatch Alarm Health Check
```

#### 1️⃣ 🌐 Endpoint Health Check

Checks a **specific endpoint** (IP address or domain name) using HTTP, HTTPS or TCP.

#### 2️⃣ 🧮 Calculated Health Check

Combines the results of **multiple health checks** (AND, OR or "at least X healthy").

#### 3️⃣ 📈 CloudWatch Alarm Health Check

Uses the state of a **CloudWatch Alarm**. This is useful for **private resources** that Route 53 checkers cannot reach directly.

#### ⚠️ Important

> Route 53 health checkers are on the **public internet**, so they **cannot directly check resources in a private subnet**. Use a **CloudWatch Alarm** health check for those.

#### ⭐ Key Points

- 🔔 Can send notifications using **Amazon SNS**
- ⏱️ We can set the check interval and failure threshold
- 🛠️ The health check path can be like `/health`

> **Health Check = Route 53 checks if our server is alive**

---

## 7.13 🔁 Route 53 Resolver

**Route 53 Resolver** answers DNS queries for resources **inside our VPC**.

It is also used for **hybrid DNS** (VPC + on-premises network).

```text
🔁 Route 53 Resolver
│
├── ⬅️ Inbound Endpoint   → On-premises → can resolve AWS (VPC) names
└── ➡️ Outbound Endpoint  → VPC → can resolve on-premises names
```

#### 🧠 Simple Meaning

> **Resolver = DNS bridge between VPC and on-premises network**

---

## 7.14 💰 Route 53 Pricing

```text
💰 Route 53 Cost
│
├── 🏷️ Domain registration (yearly fee, depends on TLD)
├── 📂 Hosted Zone (monthly fee per hosted zone)
├── 🔍 DNS Queries (per million queries)
└── ❤️ Health Checks (monthly fee per health check)
```

#### 💡 Tips

- 🔗 Alias queries to AWS resources are **free**
- 🗑️ Delete unused Hosted Zones and Health Checks

---

## 7.15 🏗️ Real Example: Domain to Load Balancer

### 🎯 Requirement

Open `www.example.com` and reach a website running behind an Application Load Balancer.

### 🏗️ Architecture

```text
👤 User
   │  www.example.com
   ▼
🧭 Route 53 (Hosted Zone: example.com)
   │  Alias A record → ALB
   ▼
⚖️ Application Load Balancer
   │
   ├── 🖥️ EC2-1
   └── 🖥️ EC2-2
```

### 🪜 Steps to Build It

```text
1. Register the domain (or use an existing one)
2. Create a Public Hosted Zone for example.com
3. Create the Application Load Balancer and EC2 servers
4. In the Hosted Zone → Create Record
     Name  → www
     Type  → A
     Alias → ON
     Target → Application Load Balancer
5. Open www.example.com in the browser ✅
```

### 🛡️ Failover Example (Active-Passive)

```text
🧭 Route 53
   │
   ├── 🟢 Primary   → Main ALB (with Health Check)
   └── 🟡 Secondary → S3 static "maintenance" website

If Primary becomes unhealthy → Users are sent to Secondary
```

---

## 📌🧠 Route 53 Quick Revision

```text
🧭 Route 53
│
├── 🏷️ Domain Registration
│
├── 📂 Hosted Zones
│   ├── 🌍 Public
│   └── 🔒 Private
│
├── 📄 Records
│   ├── A, AAAA, CNAME, NS, MX, TXT
│   ├── ⏱️ TTL
│   └── ⭐ Alias
│
├── 🔀 Routing Policies
│   ├── Simple
│   ├── Weighted
│   ├── Latency
│   ├── Failover
│   ├── Geolocation
│   ├── Geoproximity
│   └── Multivalue Answer
│
├── ❤️ Health Checks
│   ├── Endpoint
│   ├── Calculated
│   └── CloudWatch Alarm
│
└── 🔁 Route 53 Resolver
```

---

## 🧠⚡ Route 53 One-Line Memory

| Concept                  | Easy Memory                                   |
| ------------------------ | --------------------------------------------- |
| 🧭 **Route 53**          | DNS Service of AWS                            |
| 🔢 **DNS**               | Converts Name → IP Address                    |
| 🏷️ **Registrar**         | Place Where We Buy a Domain                   |
| 📂 **Hosted Zone**       | Container of DNS Records                      |
| 🌍 **Public Zone**       | For Internet Users                            |
| 🔒 **Private Zone**      | For Names Inside a VPC                        |
| 📄 **A Record**          | Name → IPv4                                   |
| 📄 **CNAME**             | Name → Another Name (Not for Root Domain)     |
| ⭐ **Alias**             | Name → AWS Resource (Works for Root Domain)   |
| ⏱️ **TTL**               | How Long DNS Answer is Cached                 |
| 🔀 **Simple**            | One Basic Answer                              |
| ⚖️ **Weighted**          | Percentage Split                              |
| ⚡ **Latency**           | Fastest Region                                |
| 🛟 **Failover**          | Backup Takes Over                             |
| 📍 **Geolocation**       | By User's Country                             |
| 📏 **Geoproximity**      | By Distance with Bias                         |
| 🎲 **Multivalue**        | Many Healthy Answers                          |
| ❤️ **Health Check**      | Checks If Server Is Alive                     |

---

## 🗺️ Route 53 Learning Map

```text
                         🧭 Route 53
                              │
       ┌──────────────────────┼──────────────────────┐
       │                      │                      │
       ▼                      ▼                      ▼
    DOMAIN                  DNS                  AVAILABILITY
       │                      │                      │
       └── Registration       ├── Hosted Zones       ├── Health Checks
                              │    ├── Public        └── Failover
                              │    └── Private
                              ├── Records
                              │    ├── A / AAAA
                              │    ├── CNAME
                              │    ├── Alias
                              │    └── MX / NS / TXT
                              │
                              ▼
                       ROUTING POLICIES
                              │
                              ├── Simple
                              ├── Weighted
                              ├── Latency
                              ├── Failover
                              ├── Geolocation
                              ├── Geoproximity
                              └── Multivalue
                              │
                              ▼
                          HYBRID DNS
                              │
                              └── Route 53 Resolver
```

---

## ⭐ Route 53 Final Memory

```text
Route 53
 │
 ├── What is it?
 │      └── DNS Service of AWS
 │
 ├── Where do we buy a domain?
 │      └── Domain Registration
 │
 ├── Where are DNS records stored?
 │      └── Hosted Zone
 │
 ├── How to point root domain to a Load Balancer?
 │      └── Alias Record
 │
 ├── How to split traffic by percentage?
 │      └── Weighted Routing
 │
 ├── How to send users to the fastest Region?
 │      └── Latency Routing
 │
 ├── How to use a backup site?
 │      └── Failover Routing + Health Check
 │
 ├── How to route by country?
 │      └── Geolocation Routing
 │
 └── How to check if a server is alive?
        └── Health Check
```

---

# ⚡ PART 8 — Lambda — Serverless Compute

> **Lambda = Run code without managing servers**

---

## 8.1 ⚡ What is Lambda?

> **Lambda = Run code without managing servers (Serverless)**

AWS Lambda is a **serverless compute service**.

We **upload our code**, and AWS runs it **only when needed**.

There is **no server to create, patch or manage**.

#### 📦 Lambda Can Be Used To

- 🖼️ Process files uploaded to S3
- 🌐 Build backend for APIs
- ⏰ Run scheduled jobs (like a cron job)
- 📬 Process messages from queues
- 🔔 Respond to events from AWS services
- 🔄 Automate AWS tasks

#### 🧠 Easy Memory

> **Lambda = Just write code, AWS runs it when an event happens**

---

## 8.2 🤔 Why Do We Use Lambda?

### ❌ Traditional (EC2)

```text
🖥️ Create Server
      ↓
💿 Install Runtime
      ↓
🚀 Deploy Code
      ↓
🛠️ Patch and Maintain Server
      ↓
💰 Pay Even When Idle
```

### ✅ With Lambda

```text
📝 Upload Code
      ↓
🔔 Event Happens
      ↓
⚡ Lambda Runs Code
      ↓
💰 Pay Only for Run Time
```

#### ⭐ Main Reasons

- ❌ No server management
- 📈 **Automatic scaling** (from 1 to thousands of requests)
- 💰 Pay only when code runs (no charge when idle)
- ⚡ Quick to build small event-driven apps
- 🔗 Easy integration with many AWS services

---

## 8.3 🧰 What Does Lambda Provide?

Lambda provides:

- 📝 Functions
- 🔔 Triggers
- 🏃 Multiple Runtimes
- 🎭 Execution Roles
- 🧠 Memory and Timeout Settings
- 🔐 Environment Variables
- 📚 Layers
- 🔢 Versions and Aliases
- ⚖️ Concurrency Controls
- 📊 Monitoring with CloudWatch
- 🔗 Function URLs

---

## 8.4 🧠 What is Serverless?

> **Serverless does NOT mean "no servers".** Servers still exist, but **AWS manages them**. We only write code.

```text
🖥️ EC2          → We manage the server
🌱 Beanstalk    → AWS manages most of the server setup
⚡ Lambda       → AWS manages everything, we write only code
```

#### ⭐ Serverless Features

- 🚫 No server management
- 📈 Auto scaling
- 💰 Pay per use
- 🛡️ Built-in high availability

---

## 8.5 🧱 Lambda Basic Concepts

```text
⚡ Lambda
│
├── 📝 Function         → Our code
├── 🔢 Handler          → Entry point of the code
├── 🏃 Runtime          → Language environment
├── 🔔 Trigger          → What starts the function
├── 🧪 Event            → Input data given to the function
├── 🧾 Context          → Information about the invocation
├── 🎭 Execution Role   → Permissions of the function
├── 🧠 Memory           → Memory given to the function
└── ⏱️ Timeout          → Maximum run time
```

### 8.5.1 📖 Simple Definitions

| Concept             | Simple Meaning                                              |
| ------------------- | ----------------------------------------------------------- |
| 📝 Function         | The code we write and upload                                |
| 🔢 Handler          | The function name AWS calls first (like `lambda_function.lambda_handler`) |
| 🏃 Runtime          | The language environment (Python, Node.js, Java ...)        |
| 🔔 Trigger          | The event source that starts the function                   |
| 🧪 Event            | The input data (JSON) given to the function                 |
| 🧾 Context          | Extra info (request ID, remaining time) about the run       |
| 🎭 Execution Role   | IAM role that allows the function to use AWS services       |

### 8.5.2 🏃 Supported Runtimes

- 🐍 Python
- 🟢 Node.js
- ☕ Java
- 🟣 .NET
- 💎 Ruby
- 🐹 Go (via custom/provided runtime)
- 📦 Container images
- 🔧 Custom runtime

#### 💡 Note

> Runtime versions are updated by AWS over time. Always check the current supported versions in AWS documentation.

---

## 8.6 🔄 How Lambda Works

```text
🔔 Event Source (S3, API Gateway, EventBridge ...)
              │
              ▼
        ⚡ Lambda Service
              │
              ▼
   🧱 Execution Environment Created
   (Runtime + Our Code)
              │
              ▼
      ▶️ Handler Runs
              │
              ▼
   📤 Result / Side Effects
   (Response, write to S3, update DB ...)
              │
              ▼
   💤 Environment Reused or Removed
```

#### 🧠 Simple Flow

```text
Event → Lambda runs code → Result → Stops (no charge until next event)
```

---

## 8.7 💻 Lambda Code Examples

### 8.7.1 👋 Simple Python Function

```python
import json

def lambda_handler(event, context):
    name = event.get("name", "World")
    return {
        "statusCode": 200,
        "body": json.dumps({"message": f"Hello, {name}!"})
    }
```

#### 📖 Understanding It

```text
lambda_handler → Entry point (the Handler)
event          → Input data (JSON converted to a Python dictionary)
context        → Information about the invocation
return         → The response
```

### 8.7.2 🪣 Python Function for an S3 Event

```python
def lambda_handler(event, context):
    for record in event["Records"]:
        bucket = record["s3"]["bucket"]["name"]
        key = record["s3"]["object"]["key"]
        print(f"New file uploaded: {key} in bucket: {bucket}")
    return {"status": "done"}
```

This function runs every time a file is uploaded to the S3 bucket.

---

## 8.8 🔔 Triggers and Invocation Types

### 8.8.1 🔔 Common Triggers

```text
🔔 Lambda Triggers
│
├── 🪣 S3              → File uploaded or deleted
├── 🌐 API Gateway     → HTTP request
├── ⏰ EventBridge     → Schedule (cron) or events
├── 📬 SQS             → Message in queue
├── 📢 SNS             → Notification
├── 🗃️ DynamoDB        → Table data changed (Streams)
├── 📊 CloudWatch Logs → Log events
└── 🔗 Function URL    → Direct HTTPS endpoint for the function
```

#### 💻 Example: Image Thumbnail

```text
👤 User uploads photo.jpg
          ↓
🪣 S3 Bucket
          ↓ (Trigger)
⚡ Lambda Function
          ↓
🖼️ Creates thumbnail
          ↓
🪣 S3 Bucket (thumbnails)
```

### 8.8.2 🔁 Invocation Types

```text
🔁 Lambda Invocation Types
│
├── ⏳ Synchronous      → Caller waits for the result
├── 📤 Asynchronous     → Caller does not wait
└── 📬 Event Source Mapping → Lambda reads from a queue/stream
```

#### 1️⃣ ⏳ Synchronous Invocation

The caller **waits** for the response.

**Examples:** API Gateway, Function URL, Application Load Balancer

```text
👤 User → 🌐 API Gateway → ⚡ Lambda → 📤 Response → 👤 User
```

---

#### 2️⃣ 📤 Asynchronous Invocation

The caller sends the event and **does not wait**. Lambda handles retries.

**Examples:** S3, SNS, EventBridge

#### ⭐ Key Points

- 🔁 Lambda **retries twice** if the function fails (total 3 attempts)
- 📮 Failed events can be sent to a **Dead-Letter Queue (DLQ)** or a failure destination

---

#### 3️⃣ 📬 Event Source Mapping

Lambda **polls (reads) from a source** and calls our function with batches of records.

**Examples:** SQS, Kinesis, DynamoDB Streams

```text
📬 SQS Queue ──(Lambda polls)──► ⚡ Lambda (batch of messages)
```

#### 📊 Comparison

| Type             | Who Waits?        | Examples                    |
| ---------------- | ----------------- | --------------------------- |
| ⏳ Synchronous   | Caller waits      | API Gateway, ALB            |
| 📤 Asynchronous  | Caller does not wait | S3, SNS, EventBridge     |
| 📬 Event Source Mapping | Lambda polls | SQS, Kinesis, DynamoDB Streams |

---

## 8.9 ⚙️ Lambda Configuration

### 8.9.1 🧠 Memory

- Memory can be set from **128 MB to 10,240 MB (10 GB)**
- 🧩 **CPU power increases with memory** (more memory = more CPU)

### 8.9.2 ⏱️ Timeout

- Default timeout is **3 seconds**
- Maximum timeout is **15 minutes (900 seconds)**

### 8.9.3 🔐 Environment Variables

Key-value settings available to our code.

```text
DB_HOST = mydb.xxxx.rds.amazonaws.com
STAGE   = production
```

#### ⚠️ Important

> Do **not** store passwords in plain environment variables. Use **AWS Secrets Manager** or **Systems Manager Parameter Store**.

### 8.9.4 💾 Ephemeral Storage (`/tmp`)

- Each function has temporary disk space at `/tmp`
- Default **512 MB**, configurable up to **10,240 MB**
- Data in `/tmp` is **temporary** (not guaranteed to stay)

### 8.9.5 📚 Layers

A **Layer** is a ZIP package of **libraries or shared code** that can be used by many functions.

```text
📚 Layer (pandas, requests ...)
      ↑ used by
⚡ Function A    ⚡ Function B    ⚡ Function C
```

- ✅ Keeps function package small
- ♻️ Reuse the same libraries in many functions

### 8.9.6 📦 Deployment Package

```text
📦 Ways to Deploy Code
│
├── 🗜️ ZIP file         → Small packages
└── 🐳 Container Image   → Larger packages (up to 10 GB)
```

---

## 8.10 🎭 Execution Role and Permissions

Lambda uses **two types of permissions**.

```text
🔐 Lambda Permissions
│
├── 🎭 Execution Role          → What the function can DO
└── 🔓 Resource-based Policy   → WHO can invoke the function
```

### 8.10.1 🎭 Execution Role

An **IAM Role** that gives the function permission to use other AWS services.

#### 💻 Example

If the function must read from S3 and write logs:

```text
🎭 Execution Role
├── 📜 AmazonS3ReadOnlyAccess
└── 📜 AWSLambdaBasicExecutionRole  (allows writing logs to CloudWatch)
```

### 8.10.2 🔓 Resource-based Policy

Decides **which service or account can invoke** (call) the function.

**Example:** Allowing S3 to invoke our function.

#### 🧠 Simple Difference

> **Execution Role = What Lambda can access. Resource-based Policy = Who can call Lambda.**

---

## 8.11 🔢 Versions and Aliases

### 8.11.1 🔢 Versions

When we publish a function, Lambda creates a **numbered version**.

```text
⚡ my-function
│
├── $LATEST   → Working copy (changes)
├── Version 1 → Fixed (cannot be changed)
├── Version 2 → Fixed
└── Version 3 → Fixed
```

- 🔒 Published versions are **immutable** (cannot be changed)

### 8.11.2 🏷️ Aliases

An **Alias** is a **name that points to a version**.

```text
🏷️ PROD  ──► Version 2
🏷️ DEV   ──► $LATEST
```

- 🔁 Easy rollback (point the alias to an older version)
- ⚖️ Aliases can **split traffic** between two versions (like 90% / 10%)

```text
🏷️ PROD
   ├── 90% → Version 2
   └── 10% → Version 3  (testing)
```

> **Alias = A name pointing to a version**

---

## 8.12 🥶 Cold Start

When a Lambda function has not run for some time, AWS must **prepare a new execution environment** first.

This causes a small delay called a **Cold Start**.

```text
🥶 Cold Start
   → New environment created
   → Code and runtime loaded
   → Slight delay

🔥 Warm Start
   → Existing environment reused
   → Faster
```

#### 💡 Ways to Reduce Cold Start

- 🧠 Use enough memory
- 📦 Keep the package small
- 🔥 Use **Provisioned Concurrency**
- ⚡ Initialize heavy things (like DB connections) outside the handler so they can be reused

---

## 8.13 ⚖️ Concurrency

**Concurrency** is the **number of function copies running at the same time**.

```text
📨 100 requests at once
        ↓
⚡ Lambda runs many copies together (scales automatically)
```

### 8.13.1 🗂️ Types of Concurrency

```text
⚖️ Concurrency
│
├── 🔒 Reserved Concurrency
└── 🔥 Provisioned Concurrency
```

#### 🔒 Reserved Concurrency

- Keeps a **fixed amount** of concurrency for one function
- Also acts as a **limit** (the function cannot go above it)
- Protects other functions from being starved

#### 🔥 Provisioned Concurrency

- Keeps a number of environments **always ready (warm)**
- Reduces **cold start**
- Costs extra

#### ⚠️ Important

> There is a default **account-level concurrency limit per Region** (it can be increased by requesting AWS).

---

## 8.14 🌐 Lambda in a VPC

By default, Lambda runs **outside our VPC** in an AWS-managed network.

If the function needs to access **private resources** (like RDS in a private subnet), we can attach it to our **VPC**.

```text
⚡ Lambda (attached to VPC private subnet)
        │
        ▼
🗄️ RDS in Private Subnet
```

#### ⚠️ Important

> A Lambda function in a VPC has **no internet access by default**. To reach the internet or AWS services, use a **NAT Gateway** (in a public subnet) or **VPC Endpoints**.

```text
⚡ Lambda (Private Subnet)
        ↓
🔁 NAT Gateway (Public Subnet)
        ↓
🚪 Internet Gateway
        ↓
🌍 Internet
```

---

## 8.15 ⭐ Important Limits and Facts

| Item                       | Fact                                                 |
| -------------------------- | ---------------------------------------------------- |
| ⏱️ Maximum Timeout         | **15 minutes**                                       |
| ⏱️ Default Timeout         | 3 seconds                                            |
| 🧠 Memory                  | 128 MB up to 10,240 MB (10 GB)                       |
| 💾 `/tmp` Storage          | 512 MB default, up to 10,240 MB                      |
| 📦 ZIP Package             | 50 MB zipped (direct upload), 250 MB unzipped        |
| 🐳 Container Image         | Up to 10 GB                                          |
| 📨 Payload (synchronous)   | 6 MB request and response                            |
| 💰 Billing                 | Requests + run time (in milliseconds) × memory       |
| 🔄 Stateless               | No data kept between runs. Use S3, DynamoDB, RDS     |

#### ⚠️ Important

> **Lambda is not good for tasks running longer than 15 minutes.** Use EC2, ECS or other services for long jobs.

> **Lambda functions are stateless.** Store data outside Lambda.

> 💡 Limits can change over time. Check AWS documentation for current values.

---

## 8.16 📊 Monitoring Lambda

```text
📊 Lambda Monitoring
│
├── 📈 CloudWatch Metrics → Invocations, Errors, Duration, Throttles
├── 📝 CloudWatch Logs    → Output of print/log statements
└── 🔍 AWS X-Ray          → Trace requests across services
```

- 📝 Each function automatically gets a **CloudWatch Log Group**
- 🖨️ Anything we `print()` appears in CloudWatch Logs
- 🔔 We can create **CloudWatch Alarms** on errors

---

## 8.17 💰 Lambda Pricing

```text
💰 Lambda Cost
│
├── 📨 Number of Requests
├── ⏱️ Duration × Memory (billed in milliseconds)
└── 🔥 Provisioned Concurrency (if used)
```

- ✅ No charge when the function is **not running**
- 🎁 Includes a **free tier**

#### ✅ Best For

- ⚡ Event-driven tasks
- ⏱️ Short tasks
- 🤖 Automation and scheduled jobs
- 🌐 Backend for APIs
- 📁 File and data processing

#### ❌ Not Ideal For

- ⏳ Tasks longer than 15 minutes
- 🖥️ Applications needing a full server or OS control
- 🔌 Applications needing constant long-lived connections

---

## 8.18 🏗️ Real Example: Auto Thumbnail Creator

### 🎯 Requirement

When a user uploads an image to an S3 bucket, create a smaller thumbnail automatically.

### 🏗️ Architecture

```text
👤 User
   │ uploads photo.jpg
   ▼
🪣 S3 Bucket: uploads
   │ (S3 Event Notification)
   ▼
⚡ Lambda Function
   │ (resizes image)
   ▼
🪣 S3 Bucket: thumbnails
```

### 🪜 Steps to Build It

```text
1. Create two S3 buckets: uploads and thumbnails
2. Create an IAM Role for Lambda
     → Read from uploads, write to thumbnails, write logs
3. Create the Lambda function (choose runtime and the Role)
4. Write the code that reads the image, resizes it and saves it
5. Add a Trigger → S3 → bucket: uploads → Event: Object Created
6. Upload a test image
7. ✅ Check the thumbnails bucket and CloudWatch Logs
```

#### ⚠️ Important

> **Never use the same bucket for input and output with the same trigger.** The new thumbnail upload would trigger the function again and create an **infinite loop**.

### ⏰ Another Example: Scheduled Job

```text
⏰ EventBridge Rule (every day at 9 AM)
          ↓
⚡ Lambda Function
          ↓
🛑 Stop all Dev EC2 instances to save cost
```

---

## 8.19 ⚖️ Lambda vs EC2

| Feature             | ⚡ Lambda                        | 🖥️ EC2                          |
| ------------------- | -------------------------------- | ------------------------------- |
| Server management   | None                             | We manage                       |
| Scaling             | Automatic                        | We set up Auto Scaling          |
| Billing             | Per request + duration           | Per second/hour while running   |
| Max run time        | 15 minutes                       | No limit                        |
| Idle cost           | None                             | Pay while running               |
| Best for            | Short, event-driven tasks        | Long-running, custom apps       |

---

## 📌🧠 Lambda Quick Revision

```text
⚡ Lambda
│
├── 🧱 Basics
│   ├── 📝 Function
│   ├── 🔢 Handler
│   ├── 🏃 Runtime
│   ├── 🔔 Trigger
│   └── 🧪 Event
│
├── 🔁 Invocation
│   ├── ⏳ Synchronous
│   ├── 📤 Asynchronous
│   └── 📬 Event Source Mapping
│
├── ⚙️ Configuration
│   ├── 🧠 Memory
│   ├── ⏱️ Timeout
│   ├── 🔐 Environment Variables
│   ├── 💾 /tmp Storage
│   └── 📚 Layers
│
├── 🔐 Security
│   ├── 🎭 Execution Role
│   └── 🔓 Resource-based Policy
│
├── 🔢 Release Management
│   ├── Versions
│   └── Aliases
│
├── ⚖️ Performance
│   ├── 🥶 Cold Start
│   ├── 🔒 Reserved Concurrency
│   └── 🔥 Provisioned Concurrency
│
└── 📊 Monitoring
    ├── CloudWatch Metrics
    ├── CloudWatch Logs
    └── X-Ray
```

---

## 🧠⚡ Lambda One-Line Memory

| Concept                       | Easy Memory                                   |
| ----------------------------- | --------------------------------------------- |
| ⚡ **Lambda**                 | Run Code Without Servers                      |
| 📝 **Function**               | The Code We Upload                            |
| 🔢 **Handler**                | Entry Point of the Code                       |
| 🏃 **Runtime**                | Language Environment                          |
| 🔔 **Trigger**                | Event That Starts the Function                |
| 🧪 **Event**                  | Input Data (JSON) for the Function            |
| 🎭 **Execution Role**         | What the Function Can Access                  |
| 🔓 **Resource-based Policy**  | Who Can Call the Function                     |
| ⏱️ **Timeout**                | Maximum 15 Minutes                            |
| 🧠 **Memory**                 | 128 MB to 10 GB (More Memory = More CPU)      |
| 📚 **Layer**                  | Shared Libraries for Functions                |
| 🔢 **Version**                | Fixed Copy of the Function                    |
| 🏷️ **Alias**                  | Name Pointing to a Version                    |
| 🥶 **Cold Start**             | Small Delay When a New Environment Starts     |
| 🔥 **Provisioned Concurrency**| Keeps Functions Warm                          |
| 🔒 **Reserved Concurrency**   | Guaranteed and Limited Capacity               |
| 💰 **Pricing**                | Requests + Duration, No Idle Charge           |

---

## 🗺️ Lambda Learning Map

```text
                          ⚡ AWS Lambda
                                │
      ┌─────────────────────────┼─────────────────────────┐
      │                         │                         │
      ▼                         ▼                         ▼
   CODE                      TRIGGERS                 PERMISSIONS
      │                         │                         │
      ├── Function              ├── S3                    ├── Execution Role
      ├── Handler               ├── API Gateway           └── Resource Policy
      ├── Runtime               ├── EventBridge
      └── Layers                ├── SQS / SNS
                                └── DynamoDB
      │
      ▼
  CONFIGURATION
      │
      ├── Memory
      ├── Timeout
      ├── Env Variables
      └── VPC Settings
      │
      ▼
  RELEASE & SCALE
      │
      ├── Versions / Aliases
      ├── Concurrency
      └── Cold Start
      │
      ▼
  MONITORING
      │
      ├── CloudWatch Logs
      ├── CloudWatch Metrics
      └── X-Ray
```

---

## ⭐ Lambda Final Memory

```text
Lambda
 │
 ├── What is it?
 │      └── Run Code Without Servers
 │
 ├── What do we upload?
 │      └── Function Code
 │
 ├── What starts it?
 │      └── Trigger / Event
 │
 ├── What are its permissions?
 │      └── Execution Role
 │
 ├── How long can it run?
 │      └── Maximum 15 Minutes
 │
 ├── Does it keep data?
 │      └── No (Stateless)
 │
 ├── What is the startup delay?
 │      └── Cold Start
 │
 ├── How to keep it warm?
 │      └── Provisioned Concurrency
 │
 └── How do we pay?
        └── Requests + Duration
```

---

# 🌱 PART 9 — Elastic Beanstalk — Easy Application Deployment

> **Elastic Beanstalk = Upload code, AWS builds and runs the environment**

---

## 9.1 🌱 What is Elastic Beanstalk?

> **Elastic Beanstalk = Easy way to deploy applications (PaaS)**

AWS Elastic Beanstalk lets us **upload our application code**, and AWS **automatically creates and manages the infrastructure** to run it.

We do not need to set up EC2, Load Balancer, Auto Scaling and monitoring one by one.

#### 📦 Beanstalk Can Run

- 🌐 Websites
- 🔌 REST APIs
- 📱 Web applications
- ⚙️ Background worker applications

#### 🧠 What is PaaS?

> **PaaS = Platform as a Service.** We bring only the **code**. The platform handles servers and setup.

#### 🧠 Easy Memory

> **Elastic Beanstalk = Upload code, AWS builds and runs the environment**

---

## 9.2 🤔 Why Do We Use Elastic Beanstalk?

### ❌ Without Beanstalk

```text
🖥️ Create EC2
      ↓
🛡️ Create Security Group
      ↓
⚖️ Create Load Balancer
      ↓
📈 Create Auto Scaling Group
      ↓
📊 Setup Monitoring
      ↓
🚀 Deploy Code
```

### ✅ With Beanstalk

```text
📝 Upload Application Code
          ↓
🌱 Elastic Beanstalk
          ↓
☁️ AWS Creates Everything Automatically
          ↓
🚀 Application is Running
```

#### ⭐ Main Reasons

- ⚡ Fast deployment
- ❌ No need to set up infrastructure manually
- 📈 Automatic scaling
- ⚖️ Automatic load balancing
- 📊 Built-in health monitoring
- 🔄 Easy version updates
- 🎛️ We still keep control of the AWS resources

---

## 9.3 🧰 What Does Elastic Beanstalk Provide?

Elastic Beanstalk provides:

- 🖥️ Automatic EC2 provisioning
- ⚖️ Load Balancer setup
- 📈 Auto Scaling setup
- 🛡️ Security Group setup
- 🧰 Ready platforms (Python, Java, Node.js ...)
- 🚀 Deployment policies
- 📊 Health monitoring
- 📝 Logs
- 🔄 Managed platform updates
- ⌨️ EB CLI for command-line deployment

---

## 9.4 🏗️ What Beanstalk Creates for Us

```text
🌱 Elastic Beanstalk Environment
│
├── 🖥️ EC2 Instances
├── 📈 Auto Scaling Group
├── ⚖️ Load Balancer
├── 🛡️ Security Groups
├── 📊 CloudWatch Monitoring
├── 🪣 S3 Bucket (stores application versions and logs)
└── 🗄️ (Optional) RDS Database
```

#### 🏗️ Architecture

```text
              👤 Users
                 │
                 ▼
         ⚖️ Load Balancer
                 │
        ┌────────┼────────┐
        ▼        ▼        ▼
     🖥️ EC2    🖥️ EC2    🖥️ EC2
        └────────┼────────┘
                 │
        📈 Auto Scaling Group
```

#### ⚠️ Important

> **Beanstalk itself is free.** We pay only for the AWS resources it creates (EC2, Load Balancer, etc.).

> **We still have control.** We can open the created resources and change settings.

---

## 9.5 🧱 Basic Concepts

```text
🌱 Elastic Beanstalk
│
├── 📱 Application          → Our app (a logical container)
├── 📦 Application Version  → A specific uploaded code version
├── 🌍 Environment          → The running set of AWS resources
├── 🧩 Environment Tier     → Web Server or Worker
├── 🧰 Platform             → OS + Language runtime
└── ⚙️ Configuration        → Settings of the environment
```

### 9.5.1 📖 Simple Definitions

| Concept                  | Simple Meaning                                                     |
| ------------------------ | ------------------------------------------------------------------ |
| 📱 Application           | Folder-like container for our app, versions and environments       |
| 📦 Application Version   | One uploaded version of our code (v1, v2 ...), stored in S3        |
| 🌍 Environment           | The AWS resources running one version of our app                   |
| 🧩 Environment Tier      | The type of work (web requests or background jobs)                 |
| 🧰 Platform              | The runtime setup (language + OS + web server)                     |
| ⚙️ Configuration         | Settings like instance type, scaling, environment variables        |

### 9.5.2 🏗️ Relationship

```text
📱 Application: my-app
│
├── 📦 Version v1
├── 📦 Version v2
│
├── 🌍 Environment: Dev   → running v2
└── 🌍 Environment: Prod  → running v1
```

#### 🧠 Remember

> **One Application can have many Versions and many Environments. One Environment runs one Version at a time.**

---

## 9.6 🧩 Environment Tiers

```text
🌍 Environment Tiers
│
├── 🌐 Web Server Tier   → Handles HTTP requests (websites, APIs)
└── ⚙️ Worker Tier       → Handles background jobs from an SQS queue
```

### 9.6.1 🌐 Web Server Tier

- Serves **web requests** from users
- Uses a **Load Balancer** and Auto Scaling
- **Examples:** Website, REST API

### 9.6.2 ⚙️ Worker Tier

- Processes **background tasks**
- Uses an **Amazon SQS queue**
- A daemon on each instance reads messages from SQS and sends them to our app
- **Examples:** Sending emails, generating reports, processing images

```text
🌐 Web Tier ──► 📬 SQS Queue ──► ⚙️ Worker Tier
(Receives request)   (Stores job)   (Processes job)
```

### 📊 Comparison

| 🌐 Web Server Tier           | ⚙️ Worker Tier                    |
| ---------------------------- | --------------------------------- |
| Serves web requests          | Processes background tasks        |
| Uses a Load Balancer         | Uses an **SQS Queue**             |
| Example: Website, REST API   | Example: Sending emails, reports  |

---

## 9.7 🌍 Environment Types

```text
🌍 Environment Types
│
├── ⚖️ Load Balanced (Auto Scaling)  → Many instances + Load Balancer
└── 1️⃣ Single Instance               → One instance only (no Load Balancer)
```

| ⚖️ Load Balanced Environment      | 1️⃣ Single Instance Environment      |
| --------------------------------- | ----------------------------------- |
| Multiple EC2 instances            | One EC2 instance                    |
| Load Balancer + Auto Scaling      | No Load Balancer                    |
| Good for production               | Good for development and testing    |
| Higher cost                       | Lower cost                          |

---

## 9.8 🛠️ Supported Platforms

Beanstalk supports many platforms, such as:

- ☕ Java (Tomcat / Java SE)
- 🟣 .NET (on Windows and .NET on Linux)
- 🐘 PHP
- 🟢 Node.js
- 🐍 Python
- 💎 Ruby
- 🐹 Go
- 🐳 Docker

#### 💡 Note

> Platform versions change often. Always choose a **currently supported** platform version when creating an environment.

---

## 9.9 🔄 How Deployment Works

```text
1. 📝 Write the application code
          ↓
2. 🗜️ Package it (ZIP file or use EB CLI)
          ↓
3. 🌱 Upload to Elastic Beanstalk
          ↓
4. 📦 Beanstalk stores it as an Application Version (in S3)
          ↓
5. 🌍 Beanstalk creates the Environment
   (EC2, Load Balancer, Auto Scaling, Security Group ...)
          ↓
6. 🚀 Application is deployed on the instances
          ↓
7. 🔗 We get an environment URL
          ↓
8. 📊 Beanstalk monitors health
```

---

## 9.10 🚀 Deployment Policies

A **Deployment Policy** decides **how a new version is released** to the instances.

```text
🚀 Deployment Policies
│
├── 1️⃣ All at Once
├── 2️⃣ Rolling
├── 3️⃣ Rolling with Additional Batch
├── 4️⃣ Immutable
└── 5️⃣ Traffic Splitting
```

### 9.10.1 1️⃣ All at Once

Deploys the new version to **all instances at the same time**.

```text
🖥️🖥️🖥️🖥️ (v1)  ──►  🖥️🖥️🖥️🖥️ (v2)   all together
```

- ⚡ Fastest
- ⚠️ **Downtime is possible** (all instances update together)
- 🔙 Rollback needs a redeploy
- 🎯 Good for **development and testing**

> **All at Once = Fast but risky**

---

### 9.10.2 2️⃣ Rolling

Deploys in **small batches**, one batch at a time.

```text
Batch 1:  🖥️(v2) 🖥️(v1) 🖥️(v1) 🖥️(v1)
Batch 2:  🖥️(v2) 🖥️(v2) 🖥️(v1) 🖥️(v1)
Batch 3:  🖥️(v2) 🖥️(v2) 🖥️(v2) 🖥️(v1)
Batch 4:  🖥️(v2) 🖥️(v2) 🖥️(v2) 🖥️(v2)
```

- ✅ No full downtime
- ⚠️ **Capacity is reduced** during deployment (a batch is out of service)
- ⚠️ Two versions run together for some time

> **Rolling = Update batch by batch**

---

### 9.10.3 3️⃣ Rolling with Additional Batch

Launches **extra new instances first**, then does the rolling update.

```text
➕ Launch an extra batch of new instances (v2)
        ↓
🔄 Roll out v2 batch by batch on old instances
        ↓
➖ Remove the extra batch at the end
```

- ✅ **Full capacity is kept** during deployment
- 💰 Slightly higher cost for a short time
- 🏭 Good for production

> **Rolling + Additional Batch = Rolling without losing capacity**

---

### 9.10.4 4️⃣ Immutable

Launches **a new set of instances** with the new version in a temporary Auto Scaling group. If healthy, they replace the old instances.

```text
🖥️🖥️🖥️ (v1, old)       🆕 🖥️🖥️🖥️ (v2, new)
                  ↓ new instances pass health checks
✅ New instances join the main group, old ones are terminated
```

- ✅ **Safest** option
- 🔙 **Fast and easy rollback** (just terminate the new instances)
- 💰 Needs double capacity for a short time
- ⏳ Slower than other methods

> **Immutable = New servers, safest**

---

### 9.10.5 5️⃣ Traffic Splitting

Sends a **small percentage of traffic** to the new version first (canary testing), and watches health.

```text
👥 Traffic
   ├── 90% → 🖥️ v1 (old)
   └── 10% → 🖥️ v2 (new, being tested)
```

- ✅ Safe testing with real traffic
- 🔙 Easy rollback
- ⚠️ Works with **Application Load Balancer** environments

> **Traffic Splitting = Test new version on a small % of users**

---

### 9.10.6 📊 Deployment Policy Comparison

| Policy                          | How It Works                                       | Downtime?            | Rollback          |
| ------------------------------- | -------------------------------------------------- | -------------------- | ----------------- |
| **All at Once**                 | All instances at the same time                     | ⚠️ Possible          | Redeploy          |
| **Rolling**                     | Batch by batch                                     | ❌ No (reduced capacity) | Redeploy      |
| **Rolling + Additional Batch**  | Extra batch first, then roll                       | ❌ No (full capacity)| Redeploy          |
| **Immutable**                   | New instances replace old ones                     | ❌ No                | ✅ Fast           |
| **Traffic Splitting**           | Small % of traffic to new version first            | ❌ No                | ✅ Fast           |

#### 🧠 Easy Memory

```text
All at Once  = Fast but risky
Rolling      = Batch by batch
Rolling + AB = Batch by batch, full capacity
Immutable    = New servers, safest
Traffic Split= Test on small % of users
```

---

## 9.11 🔵🟢 Blue/Green Deployment

Blue/Green is **not a built-in deployment policy**. We do it by creating **two environments** and **swapping their URLs**.

```text
🔵 Blue Environment  (Old Version)  ◄── Users
🟢 Green Environment (New Version)       (test here first)

        🔁 Swap Environment URLs

🟢 Green Environment (New Version)  ◄── Users
🔵 Blue Environment  (Old Version)       (kept for quick rollback)
```

#### 🪜 Steps

```text
1. Clone the current environment (Blue) → create Green
2. Deploy the new version to Green
3. Test Green using its own URL
4. Beanstalk → Swap Environment URLs
5. ✅ Users now reach Green
6. If something goes wrong, swap back to Blue
```

#### ⭐ Key Points

- ✅ Almost zero downtime
- 🔙 Very easy rollback
- 💰 Double resources while both environments exist

> **Blue/Green = Swap URLs for safe release**

---

## 9.12 🧰 Ways to Deploy

```text
🧰 Deployment Methods
│
├── 🖥️ AWS Management Console   → Upload a ZIP file
├── ⌨️ EB CLI                   → Command line tool
└── 🔄 CI/CD Pipeline           → CodePipeline, Jenkins, GitHub Actions
```

### 9.12.1 ⌨️ EB CLI Common Commands

| Command        | What It Does                                       |
| -------------- | -------------------------------------------------- |
| `eb init`      | Set up the application in our project folder       |
| `eb create`    | Create a new environment                           |
| `eb deploy`    | Deploy the current code to the environment         |
| `eb status`    | Show environment status                            |
| `eb health`    | Show instance health                               |
| `eb logs`      | Get logs from the environment                      |
| `eb open`      | Open the application URL in the browser            |
| `eb ssh`       | Connect to an instance using SSH                   |
| `eb terminate` | Delete the environment                             |

#### 💻 Example Flow

```bash
eb init -p python-3.11 my-app --region ap-south-1
eb create my-app-env
eb deploy
eb open
```

> 💡 Use a **currently supported** platform version in the `-p` option.

---

## 9.13 📁 Configuration Files

### 9.13.1 📂 `.ebextensions`

A folder in our code where we put **configuration files** (`.config` files, YAML or JSON) to customize the environment.

```text
📁 my-app/
├── 📄 application.py
├── 📄 requirements.txt
└── 📁 .ebextensions/
    └── 📄 01_settings.config
```

#### 💻 Example

```yaml
option_settings:
  aws:elasticbeanstalk:application:environment:
    APP_STAGE: production
```

#### 🎯 Can Be Used To

- 📦 Install packages
- ⚙️ Change environment settings
- 🔐 Set environment properties
- 🛠️ Run custom commands

### 9.13.2 🔐 Environment Properties

**Environment Properties** are key-value settings (like environment variables) available to our application.

```text
DB_HOST = mydb.xxxx.rds.amazonaws.com
STAGE   = production
```

#### ⚠️ Important

> Do **not** put secrets directly in code. Use environment properties with care, or **AWS Secrets Manager**.

---

## 9.14 🎭 IAM Roles in Beanstalk

```text
🎭 Beanstalk Roles
│
├── 🛠️ Service Role     → Lets Beanstalk manage AWS resources for us
└── 🖥️ Instance Profile → Role used by the EC2 instances
```

### 9.14.1 🛠️ Service Role

Allows Elastic Beanstalk to **create and manage** AWS resources (like Auto Scaling, Load Balancer, health reporting) on our behalf.

### 9.14.2 🖥️ Instance Profile

An IAM role attached to the **EC2 instances** in the environment.

It allows the application to:

- 🪣 Upload logs and versions to S3
- 📊 Send data to CloudWatch
- 🔗 Access other AWS services our app needs (like S3 or DynamoDB)

#### 🧠 Simple Difference

> **Service Role = Permissions for Beanstalk itself. Instance Profile = Permissions for our app's EC2 instances.**

---

## 9.15 🗄️ Database with Beanstalk

We can add an **RDS database** in two ways.

```text
🗄️ Database Options
│
├── 🔗 Coupled     → RDS created inside the Beanstalk environment
└── 🔓 Decoupled   → RDS created separately, outside Beanstalk
```

### 9.15.1 🔗 Coupled Database

The database is created **inside the environment**.

- ✅ Quick for development and testing
- ❌ If the environment is **deleted, the database is deleted too**

### 9.15.2 🔓 Decoupled Database (Recommended for Production)

Create **RDS separately** and connect the application to it using the **endpoint** (via environment properties).

```text
🌱 Beanstalk Environment ───► 🗄️ RDS (separate)
   (can be deleted/recreated)    (data stays safe)
```

#### ⚠️ Important

> **For production, keep the database outside Beanstalk (decoupled).**

---

## 9.16 📊 Monitoring and Health

Beanstalk monitors the health of our environment.

### 9.16.1 🚦 Health Colors

| Color        | Meaning                                    |
| ------------ | ------------------------------------------ |
| 🟢 **Green** | OK — the environment is healthy            |
| 🟡 **Yellow**| Warning — some problem detected            |
| 🔴 **Red**   | Degraded or severe — serious problem      |
| ⚪ **Grey**  | Unknown — no data or an update in progress |

### 9.16.2 📈 Monitoring Tools

```text
📊 Monitoring
│
├── 🚦 Health Dashboard    → Overall environment health
├── 📈 CloudWatch Metrics  → CPU, network, request counts
├── 📝 Logs                → Request and application logs
└── 🔔 Events              → Messages about environment changes
```

#### 💡 Enhanced Health Reporting

Gives more **detailed health information** about instances and the application.

---

## 9.17 🔄 Managed Updates

**Managed Platform Updates** let Beanstalk automatically **update the platform version** (OS, runtime, web server) of our environment during a maintenance window.

- 🛠️ Keeps the platform patched and secure
- ⏰ Runs in a **weekly maintenance window** we choose

---

## 9.18 💰 Elastic Beanstalk Pricing

```text
💰 Beanstalk Cost
│
├── 🌱 Elastic Beanstalk itself → FREE
└── 💳 Underlying resources we use
      ├── 🖥️ EC2 instances
      ├── ⚖️ Load Balancer
      ├── 🪣 S3 storage
      ├── 🗄️ RDS (if used)
      └── 📊 CloudWatch
```

#### 💡 Cost Tips

- 🧪 Use **Single Instance** environments for dev/test
- 🗑️ **Terminate** environments you are not using
- 🧹 Delete old application versions

---

## 9.19 ✅ Best For and Not Ideal For

#### ✅ Best For

- 👨‍💻 Developers who want to deploy fast without managing infrastructure
- 🌐 Standard web applications and APIs
- 🚀 Quick setups for small and medium projects
- 🧪 Learning AWS deployment

#### ❌ Not Ideal For

- 🎛️ Very complex infrastructure with special custom needs
- ⚡ Small event-driven tasks (use Lambda)
- 🖥️ Full OS-level control for everything (use EC2)

---

## 9.20 🏗️ Real Example: Deploy a Python Flask App

### 🎯 Requirement

Deploy a small Flask web application using Elastic Beanstalk.

### 📁 Project Files

```text
📁 flask-app/
├── 📄 application.py
└── 📄 requirements.txt
```

#### 📄 `application.py`

```python
from flask import Flask

application = Flask(__name__)

@application.route("/")
def home():
    return "Hello from Elastic Beanstalk!"

if __name__ == "__main__":
    application.run()
```

#### 📄 `requirements.txt`

```text
Flask
```

#### ⚠️ Important

> Beanstalk's Python platform looks for a callable named **`application`** in `application.py` by default. That is why the Flask object is named `application`.

### 🪜 Steps to Deploy (Console)

```text
1. Zip the files (application.py and requirements.txt at the top level of the ZIP)
2. Open Elastic Beanstalk → Create Application
3. Environment tier → Web server environment
4. Platform → Python (choose a supported version)
5. Application code → Upload your ZIP file
6. Choose a preset (Single instance for testing)
7. Create environment
8. Wait until the health becomes 🟢 Green
9. Open the environment URL ✅
```

### 🪜 Steps to Deploy (EB CLI)

```bash
cd flask-app
eb init -p python-3.11 flask-app --region ap-south-1
eb create flask-env
eb open
```

To deploy changes later:

```bash
eb deploy
```

To delete everything and stop charges:

```bash
eb terminate flask-env
```

### 🏗️ What Beanstalk Built for Us

```text
🌱 Environment: flask-env
├── 🖥️ EC2 instance (runs our Flask app)
├── 🛡️ Security Group
├── 🎭 Instance Profile
├── 🪣 S3 bucket (application versions)
└── 📊 CloudWatch monitoring
```

---

## 📌🧠 Elastic Beanstalk Quick Revision

```text
🌱 Elastic Beanstalk
│
├── 🧱 Basics
│   ├── 📱 Application
│   ├── 📦 Application Version
│   ├── 🌍 Environment
│   └── 🧰 Platform
│
├── 🧩 Tiers
│   ├── 🌐 Web Server Tier
│   └── ⚙️ Worker Tier (SQS)
│
├── 🌍 Environment Types
│   ├── ⚖️ Load Balanced
│   └── 1️⃣ Single Instance
│
├── 🚀 Deployment Policies
│   ├── All at Once
│   ├── Rolling
│   ├── Rolling with Additional Batch
│   ├── Immutable
│   ├── Traffic Splitting
│   └── 🔵🟢 Blue/Green (swap URLs)
│
├── 🧰 Tools
│   ├── Console
│   ├── EB CLI
│   └── .ebextensions
│
├── 🎭 Roles
│   ├── Service Role
│   └── Instance Profile
│
└── 🗄️ Database
    ├── Coupled
    └── Decoupled (recommended)
```

---

## 🧠⚡ Elastic Beanstalk One-Line Memory

| Concept                    | Easy Memory                                      |
| -------------------------- | ------------------------------------------------ |
| 🌱 **Elastic Beanstalk**   | Upload Code, AWS Builds the Environment          |
| 🧰 **PaaS**                | We Bring Code, Platform Handles Servers          |
| 📱 **Application**         | Container for Versions and Environments          |
| 📦 **Application Version** | One Uploaded Code Version                        |
| 🌍 **Environment**         | Running Set of AWS Resources                     |
| 🌐 **Web Server Tier**     | Handles HTTP Requests                            |
| ⚙️ **Worker Tier**         | Handles Background Jobs from SQS                 |
| ⚡ **All at Once**         | Fast but Risky                                   |
| 🔄 **Rolling**             | Batch by Batch                                   |
| 🛡️ **Immutable**           | New Servers, Safest                              |
| 🔵🟢 **Blue/Green**        | Swap URLs for Safe Release                       |
| 📂 **.ebextensions**       | Custom Configuration Files                       |
| 🛠️ **Service Role**        | Permissions for Beanstalk Itself                 |
| 🖥️ **Instance Profile**    | Permissions for Our EC2 Instances                |
| 🔓 **Decoupled DB**        | Keep RDS Outside Beanstalk for Production        |
| 💰 **Pricing**             | Beanstalk Free, Pay for Resources                |

---

## 🗺️ Elastic Beanstalk Learning Map

```text
                       🌱 Elastic Beanstalk
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
   CONCEPTS                DEPLOYMENT               OPERATIONS
      │                        │                        │
      ├── Application          ├── Console              ├── Health Monitoring
      ├── Version              ├── EB CLI               ├── Logs
      ├── Environment          ├── CI/CD                ├── Managed Updates
      ├── Platform             └── Policies             └── Scaling
      └── Tiers                    ├── All at Once
                                   ├── Rolling
      │                            ├── Immutable
      ▼                            ├── Traffic Splitting
   SECURITY                        └── Blue/Green
      │
      ├── Service Role
      └── Instance Profile
      │
      ▼
   DATABASE
      │
      ├── Coupled
      └── Decoupled (RDS)
```

---

## ⭐ Elastic Beanstalk Final Memory

```text
Elastic Beanstalk
 │
 ├── What is it?
 │      └── Easy deployment service (PaaS)
 │
 ├── What do we provide?
 │      └── Only our code
 │
 ├── What does AWS create?
 │      └── EC2, Load Balancer, Auto Scaling, Monitoring
 │
 ├── What is the running setup called?
 │      └── Environment
 │
 ├── Which tier serves websites?
 │      └── Web Server Tier
 │
 ├── Which tier does background jobs?
 │      └── Worker Tier (SQS)
 │
 ├── Safest deployment policy?
 │      └── Immutable
 │
 ├── How to do Blue/Green?
 │      └── Swap Environment URLs
 │
 ├── Where should production DB live?
 │      └── Outside Beanstalk (RDS, decoupled)
 │
 └── What do we pay for?
        └── Only the resources Beanstalk creates
```

---

# 🧩 PART 10 — Putting It All Together

> How the services compare and work together in one real application.

---

## 10.1 ⚖️ EC2 vs Lambda vs Elastic Beanstalk

| Feature            | 🖥️ EC2                    | ⚡ Lambda                      | 🌱 Elastic Beanstalk           |
| ------------------ | ------------------------- | ----------------------------- | ------------------------------ |
| Type               | IaaS (Virtual Server)     | Serverless (FaaS)             | PaaS                           |
| We manage          | OS, software, scaling     | Only code                     | Only code (and some settings)  |
| Control            | Full control              | Least control                 | Medium control                 |
| Runs               | Continuously              | Only when triggered           | Continuously                   |
| Max run time       | No limit                  | 15 minutes                    | No limit                       |
| Billing            | Per second/hour of usage  | Per request + duration        | Pay for resources created      |
| Best for           | Custom, long-running apps | Event-driven short tasks      | Quick web app deployment       |

#### 🧠 Easy Memory

```text
🖥️ EC2               = Full control, more work
🌱 Elastic Beanstalk = Upload code, AWS sets up servers
⚡ Lambda            = Just a function, no servers
```

---

## 10.2 🏗️ How All Services Work Together

A typical real-world web application uses **all these services together**.

```text
                         👤 User
                           │
                           ▼
                  🧭 Route 53 (DNS)
                  www.example.com
                           │
                           ▼
┌─────────────────────── 🌐 VPC ───────────────────────────────┐
│                          │                                    │
│   ┌──────────── 🌍 Public Subnets ──────────────────────┐     │
│   │   ⚖️ Load Balancer                                   │     │
│   │        │                                             │     │
│   │   🖥️ EC2 (Auto Scaling Group)  ◄── 🎭 IAM Role       │     │
│   │   (or 🌱 Elastic Beanstalk manages these)            │     │
│   └──────────────────────┬───────────────────────────────┘     │
│                          │                                    │
│   ┌──────────── 🔒 Private Subnets ─────────────────────┐     │
│   │   🗄️ RDS (Multi-AZ)                                  │     │
│   └──────────────────────────────────────────────────────┘     │
│                                                               │
└───────────────────────────────────────────────────────────────┘
         │                                  │
         ▼                                  ▼
   🪣 S3 (images, static files)    ⚡ Lambda (background tasks,
                                    triggered by S3 uploads)
```

#### 📖 Story of One Request

```text
1. 👤 User opens www.example.com
2. 🧭 Route 53 returns the Load Balancer address
3. ⚖️ Load Balancer sends the request to a healthy EC2 server
4. 🖥️ EC2 reads/writes data in 🗄️ RDS (private subnet)
5. 🖥️ EC2 uses its 🎭 IAM Role to store images in 🪣 S3
6. ⚡ Lambda is triggered by the S3 upload and creates a thumbnail
7. 🔐 IAM controls permissions at every step
```

#### 🧩 Role of Each Service

| Service              | Role in the Architecture                 |
| -------------------- | ---------------------------------------- |
| 🔐 IAM               | Permissions and security for everything  |
| 🌐 VPC               | The private network for all resources    |
| 🖥️ EC2               | Runs the application                     |
| 🌱 Elastic Beanstalk | Easy way to deploy and manage the app    |
| 🪣 S3                | Stores files and static content          |
| 🗄️ RDS               | Stores application data                  |
| 🧭 Route 53          | Connects the domain name to the app      |
| ⚡ Lambda            | Runs small event-driven tasks            |

---

# 📌🧠 Complete AWS Quick Revision

```text
☁️ AWS
│
├── 🔐 IAM
│   ├── User, Group, Role, Policy
│   └── MFA, Least Privilege
│
├── 🖥️ EC2
│   ├── AMI, Instance Type, Key Pair, Security Group
│   ├── EBS, Elastic IP
│   ├── Load Balancer, Target Group, Auto Scaling
│   └── Pricing: On-Demand, Reserved, Savings Plans, Spot
│
├── 🪣 S3
│   ├── Bucket, Object, Key
│   ├── Storage Classes
│   ├── Versioning, Lifecycle, Replication
│   └── Security and Encryption
│
├── 🌐 VPC
│   ├── CIDR, Subnet, Route Table
│   ├── Internet Gateway, NAT Gateway
│   └── Security Group, NACL, Peering, Endpoints
│
├── 🗄️ RDS
│   ├── Engines, Instance Class, Endpoint
│   ├── Multi-AZ, Read Replica
│   └── Backups, Snapshots, Encryption
│
├── 🧭 Route 53
│   ├── Hosted Zone, Records, Alias
│   ├── Routing Policies
│   └── Health Checks
│
├── ⚡ Lambda
│   ├── Function, Trigger, Event
│   ├── Execution Role
│   └── 15 min limit, Cold Start
│
└── 🌱 Elastic Beanstalk
    ├── Application, Version, Environment
    ├── Web Tier, Worker Tier
    └── Deployment Policies
```

---

# 🧠⚡ Complete AWS One-Line Memory

| Service                  | Easy Memory                                   |
| ------------------------ | --------------------------------------------- |
| ☁️ **AWS**               | Rent IT services and pay as you use           |
| 🔐 **IAM**               | Controls Who Can Do What                      |
| 🖥️ **EC2**               | Virtual Server                                |
| 📦 **AMI**               | Server Template                               |
| 💾 **EBS**               | Persistent Disk for EC2                       |
| ⚖️ **Load Balancer**     | Distributes Traffic                           |
| 📈 **Auto Scaling**      | Automatically Adjusts Number of Servers       |
| 🪣 **S3**                | Object Storage                                |
| 🌐 **VPC**               | Our Own Private Network                       |
| 🚪 **Internet Gateway**  | Gate of VPC to the Internet                   |
| 🔁 **NAT Gateway**       | Private Servers Go Out, Nobody Comes In       |
| 🛡️ **Security Group**    | Firewall for Instance (Stateful)              |
| 🚧 **NACL**              | Firewall for Subnet (Stateless)               |
| 🗄️ **RDS**               | Managed Relational Database                   |
| 🛡️ **Multi-AZ**          | Standby Copy for Failover                     |
| 📖 **Read Replica**      | Read-Only Copy for Speed                      |
| 🧭 **Route 53**          | DNS Service (Name → IP)                       |
| 🔗 **Alias Record**      | Point Root Domain to AWS Resource             |
| ❤️ **Health Check**      | Checks if Server is Healthy                   |
| ⚡ **Lambda**            | Run Code Without Servers (Max 15 Minutes)     |
| 🔔 **Trigger**           | Event That Starts a Lambda Function           |
| 🌱 **Elastic Beanstalk** | Upload Code, AWS Builds the Environment       |
| 🌍 **Environment**       | Running Set of Resources for Our App          |

---

# 🗺️ Complete AWS Learning Map

```text
                              ☁️ AWS
                                │
     ┌──────────────┬───────────┼────────────┬──────────────┐
     │              │           │            │              │
     ▼              ▼           ▼            ▼              ▼
  SECURITY       COMPUTE     STORAGE     NETWORKING      DATABASE
     │              │           │            │              │
     └── IAM        ├── EC2     └── S3       ├── VPC        └── RDS
                    ├── Lambda               └── Route 53
                    └── Elastic
                        Beanstalk
```

### 🪜 Suggested Learning Order

```text
1️⃣ IAM              → Learn security first
2️⃣ VPC              → Understand networking
3️⃣ EC2              → Launch servers
4️⃣ S3               → Store files
5️⃣ RDS              → Add a database
6️⃣ Route 53         → Connect a domain
7️⃣ Lambda           → Serverless tasks
8️⃣ Elastic Beanstalk → Easy deployments
```

---

# ⭐ Complete AWS Final Memory

```text
AWS
 │
 ├── How to control access?
 │      └── IAM
 │
 ├── How to run a server?
 │      └── EC2
 │
 ├── How to store files?
 │      └── S3
 │
 ├── How to build a private network?
 │      └── VPC
 │
 ├── How to store relational data?
 │      └── RDS
 │
 ├── How to connect a domain name?
 │      └── Route 53
 │
 ├── How to run code without servers?
 │      └── Lambda
 │
 └── How to deploy an app easily?
        └── Elastic Beanstalk
```

---

<p align="center">

## ☁️ AWS — Build Anything, Scale Everywhere

**Learn → Practice → Build → Deploy → Automate**

</p>
