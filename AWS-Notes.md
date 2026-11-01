# ☁🚀 AWS — Complete Notes

<p align="center">

**IAM • VPC • EC2 • S3 • RDS • DynamoDB • Lambda • Elastic Beanstalk • Route 53 • CloudFront • API Gateway • SQS • SNS • CloudWatch • CloudFormation**

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazon-aws)
![Cloud Computing](https://img.shields.io/badge/Cloud-Computing-blue?style=for-the-badge)
![DevOps Learning](https://img.shields.io/badge/DevOps-Learning-success?style=for-the-badge)

</p>

---

## 📖 About These Notes

This single file covers **15 core AWS services** in simple English, in a **logical learning order**.

```text
🔐 Security          → IAM
🌐 Networking        → VPC → (later) Route 53, CloudFront, API Gateway
🖥️ Compute           → EC2 → Lambda → Elastic Beanstalk
🪣 Storage           → S3
🗄️ Database          → RDS → DynamoDB
📨 Messaging         → SQS → SNS
🛠️ Management        → CloudWatch → CloudFormation
```

Every service follows the same flow:

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
<summary><b>🌐 PART 3 — VPC — Virtual Private Cloud</b></summary>

- [3.1 🌐 What is VPC?](#31--what-is-vpc)
- [3.2 🤔 Why Do We Use VPC?](#32--why-do-we-use-vpc)
- [3.3 🧰 What Does VPC Provide?](#33--what-does-vpc-provide)
- [3.4 🏠 Default VPC vs Custom VPC](#34--default-vpc-vs-custom-vpc)
- [3.5 📏 CIDR Block](#35--cidr-block)
- [3.6 🧩 Subnet](#36--subnet)
- [3.7 🛣️ Route Table](#37--route-table)
- [3.8 🚪 Internet Gateway (IGW)](#38--internet-gateway-igw)
- [3.9 🔁 NAT Gateway](#39--nat-gateway)
- [3.10 🛡️ Security Group](#310--security-group)
- [3.11 🚧 Network ACL (NACL)](#311--network-acl-nacl)
- [3.12 ⚖️ Security Group vs NACL](#312--security-group-vs-nacl)
- [3.13 🔗 VPC Peering](#313--vpc-peering)
- [3.14 🔌 VPC Endpoints](#314--vpc-endpoints)
- [3.15 🏢 Transit Gateway](#315--transit-gateway)
- [3.16 🔐 VPN and Direct Connect](#316--vpn-and-direct-connect)
- [3.17 📊 VPC Flow Logs](#317--vpc-flow-logs)
- [3.18 🏰 Bastion Host](#318--bastion-host)
- [3.19 🏗️ Real Example: Public + Private Architecture](#319--real-example-public--private-architecture)
- [📌🧠 VPC Quick Revision](#-vpc-quick-revision)
- [🧠⚡ VPC One-Line Memory](#-vpc-one-line-memory)
- [🗺️ VPC Learning Map](#-vpc-learning-map)
- [⭐ VPC Final Memory](#-vpc-final-memory)

</details>

<details>
<summary><b>🖥️ PART 4 — EC2 — Elastic Compute Cloud</b></summary>

- [4.1 🖥️ What is EC2?](#41--what-is-ec2)
- [4.2 🤔 Why Do We Use EC2?](#42--why-do-we-use-ec2)
- [4.3 🧰 What Does EC2 Provide?](#43--what-does-ec2-provide)
- [4.4 🖥️ EC2 Instance](#44--ec2-instance)
- [4.5 📦 AMI](#45--ami)
- [4.6 ⚙️ Instance Type](#46--instance-type)
- [4.7 📋 Launch Template](#47--launch-template)
- [4.8 🔑 Key Pair](#48--key-pair)
- [4.9 🛡️ Security Group](#49--security-group)
- [4.10 💾 EBS](#410--ebs)
- [4.11 📍 Elastic IP](#411--elastic-ip)
- [4.12 ⚖️ Load Balancer](#412--load-balancer)
- [4.13 🎯 Target Group](#413--target-group)
- [4.14 📈 Auto Scaling Group (ASG)](#414--auto-scaling-group-asg)
- [4.15 📌 Placement Groups](#415--placement-groups)
- [4.16 💰 EC2 Pricing Models](#416--ec2-pricing-models)
- [4.17 🏗️ Real Example: Web Server on EC2](#417--real-example-web-server-on-ec2)
- [📌🧠 EC2 Quick Revision](#-ec2-quick-revision)
- [🧠⚡ EC2 One-Line Memory](#-ec2-one-line-memory)
- [🗺️ EC2 Learning Map](#-ec2-learning-map)
- [⭐ EC2 Final Memory](#-ec2-final-memory)

</details>

<details>
<summary><b>🪣 PART 5 — S3 — Simple Storage Service</b></summary>

- [5.1 ☁️ What is S3?](#51--what-is-s3)
- [5.2 🤔 Why Do We Use S3?](#52--why-do-we-use-s3)
- [5.3 🧰 What Does S3 Provide?](#53--what-does-s3-provide)
- [5.4 🧱 S3 Basic Concepts](#54--s3-basic-concepts)
- [5.5 💾 S3 Storage Classes](#55--s3-storage-classes)
- [5.6 🔄 Versioning](#56--versioning)
- [5.7 🔐 S3 Permissions and Security](#57--s3-permissions-and-security)
- [5.8 🔒 Encryption](#58--encryption)
- [5.9 🛡️ S3 Security vs Encryption](#59--s3-security-vs-encryption)
- [5.10 🌐 S3 Static Website Hosting](#510--s3-static-website-hosting)
- [5.11 ♻️ S3 Lifecycle Management](#511--s3-lifecycle-management)
- [5.12 🔄 S3 Replication](#512--s3-replication)
- [5.13 🚀 S3 Transfer Acceleration](#513--s3-transfer-acceleration)
- [5.14 🧩 Multipart Upload](#514--multipart-upload)
- [5.15 🔔 S3 Event Notifications](#515--s3-event-notifications)
- [5.16 💰 S3 Pricing](#516--s3-pricing)
- [📌🧠 S3 Quick Revision](#-s3-quick-revision)
- [🧠⚡ S3 One-Line Memory](#-s3-one-line-memory)
- [🗺️ S3 Learning Map](#-s3-learning-map)
- [⭐ S3 Final Memory](#-s3-final-memory)

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
<summary><b>⚡ PART 7 — DynamoDB — NoSQL Database</b></summary>

- [7.1 ⚡ What is DynamoDB?](#71--what-is-dynamodb)
- [7.2 🤔 Why Do We Use DynamoDB?](#72--why-do-we-use-dynamodb)
- [7.3 🧰 What Does DynamoDB Provide?](#73--what-does-dynamodb-provide)
- [7.4 🧱 DynamoDB Basic Concepts](#74--dynamodb-basic-concepts)
- [7.5 🔑 Primary Key](#75--primary-key)
- [7.6 🔠 Data Types](#76--data-types)
- [7.7 💰 Capacity Modes](#77--capacity-modes)
- [7.8 📖 Read Consistency](#78--read-consistency)
- [7.9 📇 Secondary Indexes](#79--secondary-indexes)
- [7.10 🔍 Reading Data: Query vs Scan](#710--reading-data-query-vs-scan)
- [7.11 🛠️ DynamoDB Operations](#711--dynamodb-operations)
- [7.12 🔄 DynamoDB Streams](#712--dynamodb-streams)
- [7.13 ⏳ TTL (Time To Live)](#713--ttl-time-to-live)
- [7.14 ⚡ DAX (DynamoDB Accelerator)](#714--dax-dynamodb-accelerator)
- [7.15 🌍 Global Tables](#715--global-tables)
- [7.16 🔁 Transactions](#716--transactions)
- [7.17 📸 Backup and Restore](#717--backup-and-restore)
- [7.18 🔒 DynamoDB Security](#718--dynamodb-security)
- [7.19 🆚 DynamoDB vs RDS](#719--dynamodb-vs-rds)
- [7.20 🧠 Data Modeling Tips](#720--data-modeling-tips)
- [7.21 💰 DynamoDB Pricing](#721--dynamodb-pricing)
- [7.22 🏗️ Real Example: Serverless Products API](#722--real-example-serverless-products-api)
- [📌🧠 DynamoDB Quick Revision](#-dynamodb-quick-revision)
- [🧠⚡ DynamoDB One-Line Memory](#-dynamodb-one-line-memory)
- [🗺️ DynamoDB Learning Map](#-dynamodb-learning-map)
- [⭐ DynamoDB Final Memory](#-dynamodb-final-memory)

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
<summary><b>🧭 PART 10 — Route 53 — DNS Service</b></summary>

- [10.1 🧭 What is Route 53?](#101--what-is-route-53)
- [10.2 🤔 Why Do We Use Route 53?](#102--why-do-we-use-route-53)
- [10.3 🧰 What Does Route 53 Provide?](#103--what-does-route-53-provide)
- [10.4 🧠 DNS Basics](#104--dns-basics)
- [10.5 🏷️ Domain Registration](#105--domain-registration)
- [10.6 📂 Hosted Zone](#106--hosted-zone)
- [10.7 📄 DNS Records](#107--dns-records)
- [10.8 ⏱️ TTL](#108--ttl)
- [10.9 🔗 CNAME Record](#109--cname-record)
- [10.10 ⭐ Alias Record](#1010--alias-record)
- [10.11 🔀 Routing Policies](#1011--routing-policies)
- [10.12 ❤️ Health Checks](#1012--health-checks)
- [10.13 🔁 Route 53 Resolver](#1013--route-53-resolver)
- [10.14 💰 Route 53 Pricing](#1014--route-53-pricing)
- [10.15 🏗️ Real Example: Domain to Load Balancer](#1015--real-example-domain-to-load-balancer)
- [📌🧠 Route 53 Quick Revision](#-route-53-quick-revision)
- [🧠⚡ Route 53 One-Line Memory](#-route-53-one-line-memory)
- [🗺️ Route 53 Learning Map](#-route-53-learning-map)
- [⭐ Route 53 Final Memory](#-route-53-final-memory)

</details>

<details>
<summary><b>🌍 PART 11 — CloudFront — Content Delivery Network (CDN)</b></summary>

- [11.1 🌍 What is CloudFront?](#111--what-is-cloudfront)
- [11.2 🤔 Why Do We Use CloudFront?](#112--why-do-we-use-cloudfront)
- [11.3 🧰 What Does CloudFront Provide?](#113--what-does-cloudfront-provide)
- [11.4 📍 CloudFront Infrastructure](#114--cloudfront-infrastructure)
- [11.5 🧱 CloudFront Basic Concepts](#115--cloudfront-basic-concepts)
- [11.6 🎯 Origins](#116--origins)
- [11.7 🔒 Securing the S3 Origin (OAC)](#117--securing-the-s3-origin-oac)
- [11.8 🧭 Cache Behaviors](#118--cache-behaviors)
- [11.9 ⏱️ Caching and TTL](#119--caching-and-ttl)
- [11.10 🔄 Invalidation](#1110--invalidation)
- [11.11 🔒 CloudFront Security](#1111--cloudfront-security)
- [11.12 ⚡ CloudFront Functions and Lambda@Edge](#1112--cloudfront-functions-and-lambdaedge)
- [11.13 🌐 Custom Domain with Route 53](#1113--custom-domain-with-route-53)
- [11.14 💰 Price Classes](#1114--price-classes)
- [11.15 📊 Monitoring and Logging](#1115--monitoring-and-logging)
- [11.16 🆚 CloudFront vs S3 Transfer Acceleration vs Global Accelerator](#1116--cloudfront-vs-s3-transfer-acceleration-vs-global-accelerator)
- [11.17 💰 CloudFront Pricing](#1117--cloudfront-pricing)
- [11.18 🏗️ Real Example: S3 Static Website with CloudFront](#1118--real-example-s3-static-website-with-cloudfront)
- [📌🧠 CloudFront Quick Revision](#-cloudfront-quick-revision)
- [🧠⚡ CloudFront One-Line Memory](#-cloudfront-one-line-memory)
- [🗺️ CloudFront Learning Map](#-cloudfront-learning-map)
- [⭐ CloudFront Final Memory](#-cloudfront-final-memory)

</details>

<details>
<summary><b>🚪 PART 12 — API Gateway — Front Door for APIs</b></summary>

- [12.1 🚪 What is API Gateway?](#121--what-is-api-gateway)
- [12.2 🤔 Why Do We Use API Gateway?](#122--why-do-we-use-api-gateway)
- [12.3 🧰 What Does API Gateway Provide?](#123--what-does-api-gateway-provide)
- [12.4 🗂️ Types of APIs](#124--types-of-apis)
- [12.5 🧱 API Gateway Basic Concepts](#125--api-gateway-basic-concepts)
- [12.6 🔗 Integration Types](#126--integration-types)
- [12.7 🔒 API Security](#127--api-security)
- [12.8 🚦 Throttling](#128--throttling)
- [12.9 💾 Caching](#129--caching)
- [12.10 🏷️ Stages and Deployments](#1210--stages-and-deployments)
- [12.11 🌍 Endpoint Types and Custom Domain](#1211--endpoint-types-and-custom-domain)
- [12.12 🌐 CORS](#1212--cors)
- [12.13 📊 Monitoring and Logging](#1213--monitoring-and-logging)
- [12.14 ⏱️ Important Limits and Facts](#1214--important-limits-and-facts)
- [12.15 💰 API Gateway Pricing](#1215--api-gateway-pricing)
- [12.16 🏗️ Real Example: Serverless REST API](#1216--real-example-serverless-rest-api)
- [📌🧠 API Gateway Quick Revision](#-api-gateway-quick-revision)
- [🧠⚡ API Gateway One-Line Memory](#-api-gateway-one-line-memory)
- [🗺️ API Gateway Learning Map](#-api-gateway-learning-map)
- [⭐ API Gateway Final Memory](#-api-gateway-final-memory)

</details>

<details>
<summary><b>📬 PART 13 — SQS — Simple Queue Service</b></summary>

- [13.1 📬 What is SQS?](#131--what-is-sqs)
- [13.2 🤔 Why Do We Use SQS?](#132--why-do-we-use-sqs)
- [13.3 🧰 What Does SQS Provide?](#133--what-does-sqs-provide)
- [13.4 🧱 SQS Basic Concepts](#134--sqs-basic-concepts)
- [13.5 🗂️ Types of SQS Queues](#135--types-of-sqs-queues)
- [13.6 🔄 Message Lifecycle](#136--message-lifecycle)
- [13.7 ⏱️ Visibility Timeout](#137--visibility-timeout)
- [13.8 🗓️ Message Retention](#138--message-retention)
- [13.9 ⏳ Delay Queue](#139--delay-queue)
- [13.10 📡 Short Polling vs Long Polling](#1310--short-polling-vs-long-polling)
- [13.11 ☠️ Dead-Letter Queue (DLQ)](#1311--dead-letter-queue-dlq)
- [13.12 🔒 SQS Security](#1312--sqs-security)
- [13.13 💻 SQS Commands and Code](#1313--sqs-commands-and-code)
- [13.14 📦 Batch Operations](#1314--batch-operations)
- [13.15 ⚡ SQS with Lambda](#1315--sqs-with-lambda)
- [13.16 📈 SQS with Auto Scaling](#1316--sqs-with-auto-scaling)
- [13.17 🆚 SQS vs SNS](#1317--sqs-vs-sns)
- [13.18 💰 SQS Pricing](#1318--sqs-pricing)
- [13.19 🏗️ Real Example: Order Processing System](#1319--real-example-order-processing-system)
- [📌🧠 SQS Quick Revision](#-sqs-quick-revision)
- [🧠⚡ SQS One-Line Memory](#-sqs-one-line-memory)
- [🗺️ SQS Learning Map](#-sqs-learning-map)
- [⭐ SQS Final Memory](#-sqs-final-memory)

</details>

<details>
<summary><b>📢 PART 14 — SNS — Simple Notification Service</b></summary>

- [14.1 📢 What is SNS?](#141--what-is-sns)
- [14.2 🤔 Why Do We Use SNS?](#142--why-do-we-use-sns)
- [14.3 🧰 What Does SNS Provide?](#143--what-does-sns-provide)
- [14.4 🧱 SNS Basic Concepts](#144--sns-basic-concepts)
- [14.5 🗂️ Types of SNS Topics](#145--types-of-sns-topics)
- [14.6 👥 Subscribers and Protocols](#146--subscribers-and-protocols)
- [14.7 🔀 Fan-Out Pattern (SNS + SQS)](#147--fan-out-pattern-sns--sqs)
- [14.8 🎯 Message Filtering](#148--message-filtering)
- [14.9 💻 SNS Commands and Code](#149--sns-commands-and-code)
- [14.10 🔁 Delivery, Retries and DLQ](#1410--delivery-retries-and-dlq)
- [14.11 🔒 SNS Security](#1411--sns-security)
- [14.12 🔗 SNS Integrations with AWS Services](#1412--sns-integrations-with-aws-services)
- [14.13 📲 SMS and Mobile Push](#1413--sms-and-mobile-push)
- [14.14 🆚 SNS vs SQS](#1414--sns-vs-sqs)
- [14.15 💰 SNS Pricing](#1415--sns-pricing)
- [14.16 🏗️ Real Example: Order Notification System](#1416--real-example-order-notification-system)
- [📌🧠 SNS Quick Revision](#-sns-quick-revision)
- [🧠⚡ SNS One-Line Memory](#-sns-one-line-memory)
- [🗺️ SNS Learning Map](#-sns-learning-map)
- [⭐ SNS Final Memory](#-sns-final-memory)

</details>

<details>
<summary><b>📊 PART 15 — CloudWatch — Monitoring and Logs</b></summary>

- [15.1 📊 What is CloudWatch?](#151--what-is-cloudwatch)
- [15.2 🤔 Why Do We Use CloudWatch?](#152--why-do-we-use-cloudwatch)
- [15.3 🧰 What Does CloudWatch Provide?](#153--what-does-cloudwatch-provide)
- [15.4 📈 CloudWatch Metrics](#154--cloudwatch-metrics)
- [15.5 🚨 CloudWatch Alarms](#155--cloudwatch-alarms)
- [15.6 📝 CloudWatch Logs](#156--cloudwatch-logs)
- [15.7 🤖 CloudWatch Agent](#157--cloudwatch-agent)
- [15.8 📋 CloudWatch Dashboards](#158--cloudwatch-dashboards)
- [15.9 ⏰ EventBridge (CloudWatch Events)](#159--eventbridge-cloudwatch-events)
- [15.10 🧪 Other Useful CloudWatch Features](#1510--other-useful-cloudwatch-features)
- [15.11 ⚖️ CloudWatch vs CloudTrail vs AWS Config](#1511--cloudwatch-vs-cloudtrail-vs-aws-config)
- [15.12 💰 CloudWatch Pricing](#1512--cloudwatch-pricing)
- [15.13 🏗️ Real Example: High CPU Alert + Auto Scaling](#1513--real-example-high-cpu-alert--auto-scaling)
- [📌🧠 CloudWatch Quick Revision](#-cloudwatch-quick-revision)
- [🧠⚡ CloudWatch One-Line Memory](#-cloudwatch-one-line-memory)
- [🗺️ CloudWatch Learning Map](#-cloudwatch-learning-map)
- [⭐ CloudWatch Final Memory](#-cloudwatch-final-memory)

</details>

<details>
<summary><b>🏗️ PART 16 — CloudFormation — Infrastructure as Code</b></summary>

- [16.1 🏗️ What is CloudFormation?](#161--what-is-cloudformation)
- [16.2 🤔 Why Do We Use CloudFormation?](#162--why-do-we-use-cloudformation)
- [16.3 🧰 What Does CloudFormation Provide?](#163--what-does-cloudformation-provide)
- [16.4 🧱 CloudFormation Basic Concepts](#164--cloudformation-basic-concepts)
- [16.5 📝 Template Anatomy](#165--template-anatomy)
- [16.6 🧮 Intrinsic Functions](#166--intrinsic-functions)
- [16.7 💻 Template Examples](#167--template-examples)
- [16.8 📚 Stacks](#168--stacks)
- [16.9 🔄 Change Sets](#169--change-sets)
- [16.10 🛡️ Protecting Resources](#1610--protecting-resources)
- [16.11 🔍 Drift Detection](#1611--drift-detection)
- [16.12 🧩 Nested Stacks and Cross-Stack References](#1612--nested-stacks-and-cross-stack-references)
- [16.13 🌍 StackSets](#1613--stacksets)
- [16.14 ⌨️ CloudFormation CLI Commands](#1614--cloudformation-cli-commands)
- [16.15 🧰 Helper Tools and Related Services](#1615--helper-tools-and-related-services)
- [16.16 📏 Important Limits and Facts](#1616--important-limits-and-facts)
- [16.17 🆚 CloudFormation vs Terraform](#1617--cloudformation-vs-terraform)
- [16.18 💰 CloudFormation Pricing](#1618--cloudformation-pricing)
- [16.19 🏗️ Real Example: Deploy a Web Application Stack](#1619--real-example-deploy-a-web-application-stack)
- [📌🧠 CloudFormation Quick Revision](#-cloudformation-quick-revision)
- [🧠⚡ CloudFormation One-Line Memory](#-cloudformation-one-line-memory)
- [🗺️ CloudFormation Learning Map](#-cloudformation-learning-map)
- [⭐ CloudFormation Final Memory](#-cloudformation-final-memory)

</details>

<details>
<summary><b>🧩 PART 17 — Putting It All Together</b></summary>

- [17.1 🧩 Service Categories — Big Picture](#171--service-categories--big-picture)
- [17.2 ⚖️ Compute Comparison: EC2 vs Lambda vs Elastic Beanstalk](#172--compute-comparison-ec2-vs-lambda-vs-elastic-beanstalk)
- [17.3 🗄️ Database Comparison: RDS vs DynamoDB](#173--database-comparison-rds-vs-dynamodb)
- [17.4 📨 Messaging Comparison: SQS vs SNS](#174--messaging-comparison-sqs-vs-sns)
- [17.5 🌍 Delivery Comparison: Route 53 vs CloudFront vs API Gateway](#175--delivery-comparison-route-53-vs-cloudfront-vs-api-gateway)
- [17.6 📊 Monitoring and Management Comparison](#176--monitoring-and-management-comparison)
- [17.7 🏗️ Architecture A: Traditional 3-Tier Web Application](#177--architecture-a-traditional-3-tier-web-application)
- [17.8 ⚡ Architecture B: Serverless Application](#178--architecture-b-serverless-application)
- [17.9 🔄 Architecture C: Event-Driven and Decoupled](#179--architecture-c-event-driven-and-decoupled)
- [17.10 🏗️ CloudFormation: Building Everything From Code](#1710--cloudformation-building-everything-from-code)
- [17.11 ✅ Production Checklist](#1711--production-checklist)

</details>

- **[📌🧠 Complete AWS Quick Revision](#-complete-aws-quick-revision)**
- **[🧠⚡ Complete AWS One-Line Memory](#-complete-aws-one-line-memory)**
- **[🗺️ Complete AWS Learning Map](#-complete-aws-learning-map)**
- **[⭐ Complete AWS Final Memory](#-complete-aws-final-memory)**
- [☁️ AWS — Build Anything, Scale Everywhere](#-aws--build-anything-scale-everywhere)

---

# ☁ PART 1 — AWS BASICS — Cloud and AWS Introduction

> Start here. Understand what AWS is before learning the services.

---

## 1.1 ☁ What is AWS?

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

### 1.3.1 🏗 IaaS — Infrastructure as a Service

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

### 📊 Where Our 15 Services Fit

| Service                | Type                              |
| ---------------------- | --------------------------------- |
| 🖥️ EC2                | IaaS                              |
| 🌱 Elastic Beanstalk   | PaaS                              |
| ⚡ Lambda              | Serverless (FaaS)                 |
| 🗄️ RDS                | Managed Database Service          |
| ⚡ DynamoDB            | Serverless NoSQL Database         |
| 🪣 S3                  | Managed Storage Service           |
| 🌐 VPC                 | Networking Service                |
| 🧭 Route 53            | DNS / Networking Service          |
| 🌍 CloudFront          | Content Delivery Network (CDN)    |
| 🚪 API Gateway         | Managed API Service (Serverless)  |
| 📬 SQS                 | Managed Message Queue             |
| 📢 SNS                 | Managed Pub/Sub Messaging         |
| 📊 CloudWatch          | Monitoring and Management Service |
| 🏗️ CloudFormation      | Infrastructure as Code Service    |
| 🔐 IAM                 | Security Service                  |

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

| Type                | Meaning                          | Examples (in our notes)                                   |
| ------------------- | -------------------------------- | --------------------------------------------------------- |
| 🌍 Global Service   | Not tied to one Region           | IAM, Route 53, CloudFront                                 |
| 🌏 Regional Service | Works inside one Region          | EC2, S3 (buckets), VPC, RDS, DynamoDB, Lambda, Elastic Beanstalk, API Gateway, SQS, SNS, CloudWatch, CloudFormation |

#### ⚠ Important

> **S3 bucket names are globally unique, but each bucket is created in one Region.**

> **VPC is Regional. Subnet is inside one AZ.**

---

## 1.5 🖥 Ways to Access AWS

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

#### ⚠ Important

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

These notes follow a **logical learning order**: security and network first, then compute and storage, then databases, then delivery and APIs, then messaging, and finally monitoring and automation.

| Part | Service                 | Category          | Simple Meaning                         |
| ---- | ----------------------- | ----------------- | -------------------------------------- |
| 2    | 🔐 **IAM**              | Security          | Controls who can do what               |
| 3    | 🌐 **VPC**              | Networking        | Our private network                    |
| 4    | 🖥️ **EC2**             | Compute           | Virtual servers                        |
| 5    | 🪣 **S3**               | Storage           | Object storage                         |
| 6    | 🗄️ **RDS**             | Database          | Managed relational database            |
| 7    | ⚡ **DynamoDB**         | Database          | Serverless NoSQL database              |
| 8    | ⚡ **Lambda**           | Compute           | Run code without servers               |
| 9    | 🌱 **Elastic Beanstalk**| Compute           | Easy application deployment            |
| 10   | 🧭 **Route 53**         | Networking        | DNS service                            |
| 11   | 🌍 **CloudFront**       | Content Delivery  | CDN — fast content delivery            |
| 12   | 🚪 **API Gateway**      | Networking / API  | Front door for APIs                    |
| 13   | 📬 **SQS**              | Messaging         | Message queue                          |
| 14   | 📢 **SNS**              | Messaging         | Pub/sub notifications                  |
| 15   | 📊 **CloudWatch**       | Management        | Monitoring, logs and alarms            |
| 16   | 🏗️ **CloudFormation**   | Management        | Infrastructure as Code                 |
| 17   | 🧩 **Putting It All Together** | Summary    | Comparisons and full architectures     |

#### 🪜 Suggested Learning Order

```text
1️⃣  IAM               → Learn security first
2️⃣  VPC               → Understand networking
3️⃣  EC2               → Launch servers
4️⃣  S3                → Store files
5️⃣  RDS               → Add a relational database
6️⃣  DynamoDB          → Add a NoSQL database
7️⃣  Lambda            → Run code without servers
8️⃣  Elastic Beanstalk → Deploy applications easily
9️⃣  Route 53          → Connect a domain name
🔟  CloudFront        → Deliver content faster
1️⃣1️⃣ API Gateway       → Build APIs
1️⃣2️⃣ SQS               → Decouple with queues
1️⃣3️⃣ SNS               → Send notifications and fan-out
1️⃣4️⃣ CloudWatch        → Monitor everything
1️⃣5️⃣ CloudFormation    → Build everything from code
```

---

# 🔐 PART 2 — IAM — Identity and Access Management

> **IAM = Controls WHO can access AWS and WHAT they can do**

---

## 2.1 🔐 What is IAM?

> **IAM = Identity and Access Management**

IAM is an AWS service that is used to **securely manage users, groups, roles, and permissions.**

IAM allows us to control **who can access AWS resources and what actions they can perform.**

### We can use IAM to:

- 👤 Create and manage IAM users.
- 👥 Organize users into IAM groups.
- 🔑 Assign permissions using IAM policies.
- 🎭 Create and manage IAM roles
- 🛡️ Control access to AWS resources.

### ⚙️ It Provides components such as:

- 👤 IAM Users
- 👥 IAM Groups
- 🎭 IAM Roles
- 📜 IAM Policies

to securely manage access to AWS resources.

</br>
<p align="center">

![Amazon IAM](https://github.com/samir-shaikh7/My-Notes/blob/main/AWS-Notes/Images/IAM-def.png?raw=true)

</p>

---

#### IAM answers two main questions:

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

#### 🏗 IAM Basic Flow

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

#### ⚠ Important

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

#### ⚠ Important

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

#### 🏗 Example

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

### 2.8.1 🗂 Types of Policies

```text
📜 IAM Policies
│
├── 🏢 AWS Managed Policy
├── 🛠️ Customer Managed Policy
└── 📎 Inline Policy
```

#### 1⃣ 🏢 AWS Managed Policy

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

#### 2⃣ 🛠 Customer Managed Policy

Created and managed by **us**.

- Can be reused by many users, groups and roles
- Gives more exact control

---

#### 3⃣ 📎 Inline Policy

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

### 2.8.2 ⚖ Identity-Based vs Resource-Based Policy

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

## 2.9 ⚖ Policy Evaluation Logic

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

#### ⚠ Important

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

#### ⚙ Settings We Can Control

- 📏 Minimum password length
- 🔤 Must include uppercase, lowercase, numbers, symbols
- ⏳ Password expiry (force change after some days)
- 🔁 Prevent reusing old passwords

> **Password Policy = Rules for strong passwords**

---

## 2.15 🌐 Identity Federation

**Identity Federation** lets users sign in to AWS using an **existing identity** from outside IAM, instead of creating separate IAM users.

#### 🏗 Example

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

## 2.16 🛡 Permissions Boundary and SCP

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

#### ⚠ Important

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

### 2.17.4 🕵 AWS CloudTrail (Related Service)

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

## 2.19 🏗 Real Example: EC2 Accessing S3 Using a Role

### 🎯 Requirement

An application running on **EC2** needs to **read files from an S3 bucket**, without storing access keys on the server.

### 🏗 Architecture

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

## 🗺 IAM Learning Map

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

# 🌐 PART 3 — VPC — Virtual Private Cloud

> **VPC = Our Own Private Network in AWS**

---

## 3.1 🌐 What is VPC?

> **VPC = Virtual Private Cloud**

### 📖 Technical Definition

Amazon VPC is an AWS service that is used create our own **logically isolated private network inside the AWS Cloud**.

VPC allows us to launch, manage and control AWS resources within our own virtual network.

We launch AWS resources like **EC2, RDS and Load Balancers** inside our VPC.

### We can use VPC to:

- 🌐 Create a private network in AWS.
- 📍 Define IP address ranges for our network.
- 🔀 Divide the network into public and private subnets.
- 🔒 Control incoming and outgoing network traffic.
- 🚪 Connect our network to the internet.

### ⚙️ It Provides networking components such as:

- 🌐 Subnets
- 🛣️ Route Tables
- 🌍 Internet Gateway
- 🔄 NAT Gateway
- 🛡️ Security Groups
- 🔐 Network ACLs
- 🔗 VPC Peering

to build and manage AWS network environments.

</br>
<p align="center">

![Amazon S3](https://github.com/samir-shaikh7/My-Notes/blob/main/AWS-Notes/Images/VPC-def.png?raw=true)

</p>

---

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

## 3.2 🤔 Why Do We Use VPC?

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

## 3.3 🧰 What Does VPC Provide?

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

#### ⚠ Important

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

## 3.4 🏠 Default VPC vs Custom VPC

### 3.4.1 🏠 Default VPC

AWS automatically creates a **Default VPC** in every Region for our account.

- ✅ Comes ready to use
- 🧩 Has default subnets (one in each AZ)
- 🚪 Has an Internet Gateway already attached
- 📏 Default CIDR is `172.31.0.0/16`
- 🧪 Good for quick testing

### 3.4.2 🛠 Custom VPC

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

## 3.5 📏 CIDR Block

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

#### ⚠ Important

> Do not use **overlapping CIDR ranges** if you want to connect two VPCs later (VPC Peering will not work).

---

## 3.6 🧩 Subnet

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

#### ⚠ Important

> **One Subnet = One Availability Zone only.**

A subnet cannot stretch across multiple AZs.

### 3.6.1 🌍 Public Subnet

A subnet whose **Route Table has a route to an Internet Gateway**.

Resources here can be reached from the internet (if they have a public IP).

**Used for:**

- 🌐 Web Servers
- ⚖️ Load Balancers
- 🔁 NAT Gateway
- 🏰 Bastion Host

### 3.6.2 🔒 Private Subnet

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

#### ⚠ Important

> A subnet is called **public or private only because of its Route Table**, not because of its name.

### 3.6.3 5⃣ Reserved IP Addresses

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

### 3.6.4 🌍 Auto-assign Public IP

A subnet can be set to **auto-assign a public IPv4 address** to new instances launched in it.

A public subnet needs both:

```text
1. 🛣️ Route to Internet Gateway
2. 📍 Public IP (auto-assigned or Elastic IP) on the instance
```

---

## 3.7 🛣 Route Table

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

## 3.8 🚪 Internet Gateway (IGW)

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

#### ⚠ Important

> If even one of these is missing, internet access will not work.

### 🌍 Egress-Only Internet Gateway

Used for **IPv6** traffic. It allows **outbound only** connections to the internet and blocks incoming connections.

---

## 3.9 🔁 NAT Gateway

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

#### ⚠ Important

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

## 3.10 🛡 Security Group

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

## 3.11 🚧 Network ACL (NACL)

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

#### ⚠ Important

> NACL is **stateless**. If we allow inbound traffic, we must also allow the **outbound response** (usually using ephemeral ports `1024–65535`).

#### 🧠 Simple Meaning

> **NACL = Firewall for the subnet**

---

## 3.12 ⚖ Security Group vs NACL

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

## 3.13 🔗 VPC Peering

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

### ⚠ Peering Is NOT Transitive

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

## 3.14 🔌 VPC Endpoints

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

### 🗂 Types of VPC Endpoints

```text
🔌 VPC Endpoints
│
├── 🚪 Gateway Endpoint
└── 🔗 Interface Endpoint
```

#### 1⃣ Gateway Endpoint

- Supports only **S3** and **DynamoDB**
- Added as a **route in the Route Table**
- **No extra charge**

#### 2⃣ Interface Endpoint (AWS PrivateLink)

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

## 3.15 🏢 Transit Gateway

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

## 3.16 🔐 VPN and Direct Connect

These services connect our **on-premises network (office / data center)** to **AWS VPC**.

### 3.16.1 🔐 Site-to-Site VPN

A **secure, encrypted connection** between our office network and our VPC **over the public internet**.

- ⚡ Quick to setup
- 🔒 Encrypted traffic
- 💰 Cost is lower
- 🌐 Speed depends on the internet

### 3.16.2 ⚡ AWS Direct Connect

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

## 3.17 📊 VPC Flow Logs

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

#### ⚠ Important

> Flow Logs do **NOT** capture the actual content (data) of the packets. They only record **traffic information**.

---

## 3.18 🏰 Bastion Host

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

## 3.19 🏗 Real Example: Public + Private Architecture

This is the most common VPC design.

### 🎯 Requirement

- 🌐 Website should be reachable from the internet
- 🗄️ Database should be **private** and safe

### 🏗 Architecture

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

## 🗺 VPC Learning Map

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

# 🖥 PART 4 — EC2 — Elastic Compute Cloud

> **EC2 = Virtual Server in AWS**

---

## 4.1 🖥 What is EC2?

> **EC2 = Elastic Compute Cloud**

### 📖 Technical Definition

Amazon EC2 is an AWS service that provides **resizable virtual servers in the cloud**.

EC2 allows us to **launch, manage and scale servers on AWS**.

These virtual servers are called **EC2 Instances**.

We can use these **EC2 Instances** to:

* 🌐 Host websites
* ⚙️ Run applications
* 🗄️ Run databases
* 📦 Install software
* 🐳 Run Docker
* 🔧 Run Jenkins

### ⚙️ It Provides

- 💻 Different Instance Types
- 🧠 CPU and Memory Resources
- 💾 Storage Options
- 🌐 Networking Resources

We can select these resources according to our needs.

</br>
<p align="center">

![Amazon S3](https://github.com/samir-shaikh7/My-Notes/blob/main/AWS-Notes/Images/EC2-def.png?raw=true)

</p>

#### 🧠 Easy Memory

> **EC2 = Virtual Server in AWS**

---

## 4.2 🤔 Why Do We Use EC2?

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

## 4.3 🧰 What Does EC2 Provide?

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

## 4.4 🖥 EC2 Instance

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

#### 🖥 EC2 Instance Structure

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

### 4.4.1 🔄 EC2 Instance States

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

## 4.5 📦 AMI

> **AMI = Amazon Machine Image**

An **AMI** is a **pre-configured template** that contains everything required to create an EC2 Instance.

#### 📦 It Contains

- 💿 Operating System
- 📥 Installed Software
- ⚙️ Settings and Configurations

#### 🎯 It Is Used To

- 🚀 Launch new EC2 Instance quickly
- 💾 Backup a configured server

#### ⚠ Important

> **Without AMI, we cannot launch an EC2 Instance.**

### 🗂 Types of AMIs

#### 1⃣ AWS-Provided AMIs

Created and maintained by AWS.

**Examples:**

- Amazon Linux
- Ubuntu
- Windows Server

#### 2⃣ AWS Marketplace AMI

Created by third-party vendors.

**Examples:**

- Jenkins Server
- MongoDB
- WordPress
- Red Hat Enterprise Linux

Some are free, while others require payment.

#### 3⃣ Custom AMI

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

## 4.6 ⚙ Instance Type

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

### 4.6.1 🏷 Instance Families

Different instance families are designed for different workloads.

#### 1⃣ General Purpose (T, M)

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

#### 2⃣ Compute Optimized (C)

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

#### 3⃣ Memory Optimized (R, X)

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

#### 4⃣ Storage Optimized (I, D)

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

#### 5⃣ Accelerated Computing (P, G)

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

## 4.7 📋 Launch Template

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

## 4.8 🔑 Key Pair

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

#### ⚠ Important

> The private key should be protected and should not be shared publicly.

> AWS lets us **download the private key only once** when the key pair is created.

---

## 4.9 🛡 Security Group

A **Security Group** is a virtual firewall that controls **inbound and outbound network traffic** for an EC2 Instance.

### Security Group Provides Two Types of Rules

#### 1⃣ Inbound Rules

Inbound Rules control **incoming traffic**.

#### 2⃣ Outbound Rules

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

#### ⚠ Important

> Do not open unnecessary ports to the entire internet.

For example, SSH port **22** should generally be restricted to trusted source IPs or managed through safer access methods where possible.

#### 🧠 Simple Meaning

> **Security Group = Firewall for the instance**

---

## 4.10 💾 EBS

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

### 4.10.1 💽 EBS Volume

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

### 4.10.2 📊 EBS Volume Types

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

#### 1⃣ gp3 — General Purpose SSD

gp3 is an SSD volume used for most general workloads.

**Used for:**

- 🌐 Web servers
- ⚙️ Application servers
- 📱 General applications

---

#### 2⃣ gp2 — General Purpose SSD

gp2 is an older-generation SSD volume.

- Good for general workloads
- Performance depends partly on volume size
- gp3 is generally preferred for new workloads

---

#### 3⃣ io2 — Provisioned IOPS SSD

io2 is an SSD volume for applications that need **high and consistent I/O performance**.

**Used for:**

- 🗄️ Databases
- ⚡ I/O-intensive applications
- 🔥 Critical applications

---

#### 4⃣ io1 — Provisioned IOPS SSD

io1 is an older SSD volume designed for applications that need provisioned IOPS.

**Used for:**

- 🗄️ High-performance databases
- ⚡ I/O-intensive applications

---

#### 5⃣ st1 — Throughput Optimized HDD

st1 is an HDD volume designed for **high-throughput workloads**.

It is better for large amounts of data processed sequentially.

**Used for:**

- 📦 Big Data
- 🏢 Data warehouses
- 📝 Log processing
- 📈 Large sequential workloads

---

#### 6⃣ sc1 — Cold HDD

sc1 is a low-cost HDD volume for data that is accessed less frequently.

**Used for:**

- 🗃️ Large datasets that are rarely accessed
- 📚 Archives
- 💤 Infrequently accessed data

---

### 4.10.3 🧩 EBS Volume Roles

#### 1⃣ Root Volume

Root Volume contains the **Operating System** of the EC2 Instance.

#### 2⃣ Additional Volume

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

### 4.10.4 📸 EBS Snapshot

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

### 4.10.5 🆚 EBS vs Instance Store

| 💾 EBS                           | ⚡ Instance Store                       |
| -------------------------------- | -------------------------------------- |
| Network-attached persistent disk | Disk physically attached to the host   |
| Data stays after stop            | Data is **lost** when instance stops   |
| Can take snapshots               | No snapshots                           |
| Good for most uses               | Good for temporary data, cache         |

---

## 4.11 📍 Elastic IP

An **Elastic IP Address** is a **static public IPv4 address** that can be associated with AWS resources such as an EC2 Instance.

A normal public IPv4 address may change when an instance is stopped and started, depending on how it is configured.

Elastic IP is useful when a **stable public IPv4 address** is required.

#### 🔄 Public IP vs Elastic IP

```text
🌍 Normal Public IP   → May change after stop/start
📍 Elastic IP         → Stays the same until we release it
```

#### ⚠ Important

> **Public IPv4 addresses (including Elastic IPs) can have a cost.** Release Elastic IPs we do not use.

#### 🧠 Simple Meaning

> **Elastic IP = Static Public IPv4 Address**

---

## 4.12 ⚖ Load Balancer

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

### 4.12.1 🧩 Types of Load Balancers

AWS has **4 main types** of Load Balancers.

#### 1⃣ Application Load Balancer (ALB)

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

#### 2⃣ Network Load Balancer (NLB)

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

#### 3⃣ Gateway Load Balancer (GWLB)

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

#### 4⃣ Classic Load Balancer (CLB)

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

## 4.13 🎯 Target Group

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

## 4.14 📈 Auto Scaling Group (ASG)

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

#### 1⃣ Launch Template

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

#### 2⃣ Minimum Capacity

Minimum number of EC2 Instances that should run.

**Example:**

```text
Minimum Capacity = 2
```

ASG will try to keep at least **2 EC2 Instances** running.

---

#### 3⃣ Desired Capacity

Number of EC2 Instances we normally want to run.

**Example:**

```text
Desired Capacity = 3
```

ASG will normally try to keep **3 EC2 Instances** running.

If one instance becomes unhealthy, ASG can launch a replacement to return to 3.

---

#### 4⃣ Maximum Capacity

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

### 4.14.1 📈 Scaling Policies

A **Scaling Policy** tells the Auto Scaling Group when to add or remove EC2 Instances.

#### 1⃣ Dynamic Scaling

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

#### 2⃣ Scheduled Scaling

Scale at a fixed time.

**Example:**

```text
Every Day

9 AM  → Launch 5 Instances
10 PM → Reduce to 2 Instances
```

---

#### 3⃣ Predictive Scaling

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

## 4.15 📌 Placement Groups

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

### 4.15.1 🔗 Cluster Placement Group

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

### 4.15.2 🧩 Spread Placement Group

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

#### ⚠ Important

> Spread Placement Group has a limit of **7 running instances per Availability Zone**.

#### 🧠 Remember

> **Spread = Keep Instances Separate**

---

### 4.15.3 🗂 Partition Placement Group

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

## 4.16 💰 EC2 Pricing Models

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

### 4.16.1 🟢 On-Demand Instances

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

### 4.16.2 📅 Reserved Instances (RI)

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

#### ⚠ Important

> Reserved Instance does **NOT** mean you reserve a physical EC2 server.

It means you commit to using EC2 for a long time and get a discount.

---

### 4.16.3 💳 Savings Plans

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

#### ⚠ Important

> Savings Plans do not reserve a physical EC2 server.

You make a long-term spending commitment and get a discount on eligible compute usage.

---

### 4.16.4 ⚡ Spot Instances

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

#### ⚠ Important

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

### 4.16.5 🏢 Dedicated Hosts

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

### 4.16.6 🔒 Dedicated Instances

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

## 4.17 🏗 Real Example: Web Server on EC2

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

### 🏗 Architecture

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

## 🗺 EC2 Learning Map

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

# 🪣 PART 5 — S3 — Simple Storage Service

> **S3 = Object Storage in AWS**

---

## 5.1 ☁ What is S3?

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

#### ⚙️ It Provides

- 📈 Scalable Storage
- 🛡️ High Durability
- 🔐 Security Features
- 💰 Different Storage Classes

</br>
<p align="center">

![Amazon S3](https://github.com/samir-shaikh7/My-Notes/blob/main/AWS-Notes/Images/S3-def.png?raw=true)

</p>

#### 🏗 S3 Basic Architecture

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

## 5.2 🤔 Why Do We Use S3?

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

## 5.3 🧰 What Does S3 Provide?

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

## 5.4 🧱 S3 Basic Concepts

### 5.4.1 🪣 S3 Bucket

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

### 5.4.2 📦 S3 Object

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

### 5.4.3 🔑 Object Key

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

### 5.4.4 🛡 S3 Durability and Availability

- 🛡️ S3 Standard is designed for **99.999999999% (11 nines) durability**
- 📋 Data is stored across **multiple Availability Zones** (except One Zone classes)

> **Durability = Data will not be lost**

---

## 5.5 💾 S3 Storage Classes

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

### 5.5.1 🟢 S3 Standard

Used for data that is accessed frequently.

#### Examples

- 🌐 Websites
- 💻 Applications
- 📄 Frequently accessed files

> **Standard = Frequently accessed data**

---

### 5.5.2 🧠 S3 Intelligent-Tiering

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

### 5.5.3 🟡 S3 Standard-IA

**IA = Infrequent Access**

Used for data that is accessed less frequently but needs quick access when required.

#### Examples

- 📊 Old reports
- 💾 Backups
- 📄 Important files that are rarely accessed

> **Standard-IA = Infrequent access + Quick retrieval**

---

### 5.5.4 🟠 S3 One Zone-IA

Used for infrequently accessed data in a **single Availability Zone**.

#### Examples

- 💾 Re-creatable backups
- 📄 Old data
- 🔄 Secondary copies of data
- 🗂️ Temporary data that is rarely accessed

> **One Zone-IA = Infrequent access + Quick retrieval + Stored in one Availability Zone**

---

### 5.5.5 ⚡ S3 Glacier Instant Retrieval

Used for archive data that still needs fast retrieval when required.

#### Examples

- 🏥 Medical records
- 📄 Old documents
- 🗃️ Long-term archives
- 📊 Historical data

> **Glacier Instant Retrieval = Rarely accessed + Instant retrieval**

---

### 5.5.6 🧊 S3 Glacier Flexible Retrieval

Used for archive data where retrieval can take more time.

#### Examples

- 💾 Old backups
- 🗃️ Archived files
- 📦 Long-term data
- 🛡️ Disaster recovery data

> **Glacier Flexible Retrieval = Rarely accessed + Retrieval in minutes to hours**

---

### 5.5.7 ❄ S3 Glacier Deep Archive

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

## 5.6 🔄 Versioning

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

## 5.7 🔐 S3 Permissions and Security

S3 security controls **who can access which bucket or object and what they can do**.

#### 🛡 Common Security Mechanisms

```text
🔐 S3 Security
│
├── 📜 IAM Policy
├── 🪣 Bucket Policy
├── 📋 ACLs
└── 🚫 Block Public Access
```

#### 🛡 S3 Access Control Flow

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

### 5.7.1 📜 IAM Policy

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

### 5.7.2 🪣 Bucket Policy

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

### ⚖ IAM Policy vs Bucket Policy

| 📜 IAM Policy                    | 🪣 Bucket Policy                  |
| -------------------------------- | --------------------------------- |
| Attached to User, Role, or Group | Attached to S3 Bucket             |
| Identity-based policy            | Resource-based policy             |
| Controls what an identity can do | Controls access to an S3 resource |

#### 🧠 Simple Difference

> **IAM Policy → What an identity can do**

> **Bucket Policy → Who can access an S3 resource**

---

### 5.7.3 📋 ACLs

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

### 5.7.4 🚫 Block Public Access

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

#### ⚠ Important

> For a **public static website**, Block Public Access must be turned off for that bucket, and a bucket policy must allow public read.

---

### 5.7.5 🔗 Pre-signed URLs

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

## 5.8 🔒 Encryption

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

### 5.8.1 🔑 SSE-S3

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

### 5.8.2 🔐 SSE-KMS

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

### 5.8.3 🗝 SSE-C

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

### 5.8.4 🔐🔐 DSSE-KMS

**DSSE-KMS = Dual-layer Server-Side Encryption with KMS keys**

S3 applies **two layers of encryption** to the object using KMS keys.

It is used when strict compliance rules need extra protection.

#### 🧠 Remember

> **DSSE-KMS → Two layers of encryption with KMS keys**

---

### 5.8.5 🌐 Encryption in Transit

Data moving between us and S3 can be protected with **HTTPS (SSL/TLS)**.

```text
💾 At Rest     → Data stored in S3 is encrypted (SSE)
🌐 In Transit  → Data moving to S3 is protected (HTTPS)
```

---

## 5.9 🛡 S3 Security vs Encryption

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

## 5.10 🌐 S3 Static Website Hosting

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

#### 🏗 Static Website Architecture

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

#### ⚙ Basic Steps

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

#### ⚠ Important

> S3 static website endpoint uses **HTTP**. For **HTTPS** and a custom domain, use **CloudFront** (and Route 53 for the domain name).

> **Static Website Hosting = Hosting static website files using S3**

---

## 5.11 ♻ S3 Lifecycle Management

**S3 Lifecycle Management** is used to automatically move or delete objects based on rules.

Instead of manually managing old files, S3 does it automatically.

### ♻ Lifecycle Rule

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

#### 🗑 Expiration

Deletes objects automatically after a specified period.

#### ♻ Lifecycle Flow

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

## 5.12 🔄 S3 Replication

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

### 5.12.1 🏠 SRR — Same-Region Replication

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

### 5.12.2 🌍 CRR — Cross-Region Replication

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

### 5.12.3 🔧 Replication Rules

A Replication Rule defines:

- 📦 Which objects should be replicated
- 📍 Where they should be replicated
- 🪣 What destination bucket should be used

Replication can be applied to:

- 📦 All objects
- 📁 Specific objects using prefixes
- 🏷️ Objects with specific tags

---

### 5.12.4 🕒 Versioning Requirement

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

### 5.12.5 📦 Existing Objects vs New Objects

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

### ⚖ CRR vs SRR

| 🌍 CRR                      | 🏠 SRR                    |
| --------------------------- | ------------------------- |
| Cross-Region Replication    | Same-Region Replication   |
| Different AWS Regions       | Same AWS Region           |
| 🛡️ Disaster recovery        | 💾 Backup / data processing|
| Example: Mumbai → Singapore | Example: Mumbai → Mumbai  |

---

## 5.13 🚀 S3 Transfer Acceleration

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

## 5.14 🧩 Multipart Upload

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

## 5.15 🔔 S3 Event Notifications

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

## 5.16 💰 S3 Pricing

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

## 🗺 S3 Learning Map

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

# 🗄 PART 6 — RDS — Relational Database Service

> **RDS = Managed Relational Database in AWS**

---

## 6.1 🗄 What is RDS?

> **RDS = Relational Database Service**

Amazon RDS is a **fully managed database service provided by AWS**.

It is used to **easily create, manage, and run relational databases in the AWS cloud**.

AWS manages most of the database setup and maintenance tasks for us.

### Such as:

- 🖥️ Hardware setup
- 💿 Operating system maintenance
- 📸 Automated backups
- 🔄 Software updates
- 🛡️ Failover (with Multi-AZ)

So we don't need to manage everything manually, We only focus on our **data and application**.

### We can use RDS to:

- 🗄️ Create relational databases
- 📥 Store and retrieve data
- 🔄 Take automated backups
- 📈 Increase database capacity
- 🔒 Manage database security
- 🌍 Improve database availability
- 🔍 Monitor database performance

### ⚙️ RDS supports database engines such as:

- 🐬 MySQL
- 🐘 PostgreSQL
- 🐬 MariaDB
- 🏢 Oracle
- 🪟 Microsoft SQL Server
- ⚡ Amazon Aurora

</br>
<p align="center">

![Amazon RDS](https://github.com/samir-shaikh7/My-Notes/blob/main/AWS-Notes/Images/RDS-def.png?raw=true)

</p>

---

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

#### 🏗 RDS Basic Architecture

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

#### ⚠ Important

> **In RDS, we cannot SSH into the database server or access its operating system.**

AWS manages the OS. We only access the **database** using its endpoint.

---

## 6.4 🧱 RDS Basic Concepts

### 6.4.1 🖥 DB Instance

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

### 6.4.2 🛢 DB Engine

A **DB Engine** is the **database software** that runs on the DB Instance.

Examples: MySQL, PostgreSQL, MariaDB, Oracle, SQL Server.

> **DB Engine = Database Software**

---

### 6.4.3 ⚙ DB Instance Class

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

#### ⚠ Important

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

## 6.5 🛢 Supported Database Engines

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

## 6.6 ⚙ DB Instance Classes

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

### 6.7.3 🕰 Magnetic Storage

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

## 6.8 🛡 Multi-AZ Deployment

**Multi-AZ** is a feature that gives **high availability** to our database.

RDS keeps a **standby copy** of our database in a **different Availability Zone**.

#### 🏗 Multi-AZ Architecture

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

#### ⚠ Important

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

#### 🏗 Read Replica Architecture

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

#### ⚠ Important

> Because replication is **asynchronous**, a Read Replica may be **slightly behind** the Primary (called **replica lag**).

#### 🧠 Simple Meaning

> **Read Replica = Read-only copy to improve read performance**

---

## 6.10 ⚖ Multi-AZ vs Read Replica

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

### 6.11.2 🖐 Manual Snapshots

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

#### ⚠ Important

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

### 6.12.2 🛡 Security Group

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

#### ⚠ Important

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

### 6.12.5 🗝 AWS Secrets Manager

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

#### ⚠ Important

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

#### 🏗 Architecture

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

#### 🏗 Aurora Architecture

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

#### 🌩 Aurora Serverless

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

#### 1⃣ On-Demand

Pay per hour for the DB instance with no long-term commitment.

> **On-Demand = Pay as You Use**

#### 2⃣ Reserved Instances

Commit for **1 or 3 years** and get a **discount** compared to On-Demand.

Best for databases that run **continuously** (like production databases).

> **Reserved = Commit for long time, pay less**

#### 💡 Cost Tips

- Use **small burstable instances** for dev/test
- **Stop** (or delete) test databases when not needed
- Use **Reserved Instances** for production databases
- Delete **old manual snapshots** that are not needed

#### ⚠ Important

> A **stopped** RDS instance is automatically started again after **7 days**.

> **Multi-AZ increases cost**, because we pay for the standby too.

---

## 6.18 🏗 Real Example: EC2 + RDS Architecture

This is the most common real-world use of RDS.

### 🎯 Requirement

- Website should be reachable from the internet
- Database should be **private and safe**
- Database should be **highly available**

### 🏗 Architecture

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

### ⚖ RDS vs Database on EC2

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

## 🗺 RDS Learning Map

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

# ⚡ PART 7 — DynamoDB — NoSQL Database

> **DynamoDB = Fully managed, serverless NoSQL database**

---

## 7.1 ⚡ What is DynamoDB?

> **DynamoDB = Fully managed NoSQL database of AWS**

Amazon DynamoDB is a **fully managed, serverless NoSQL database** that gives **fast and predictable performance (single-digit millisecond)** at any scale.

We do not manage servers, storage or patching. We just **create a table and store data**.

#### 🤔 What is NoSQL?

**NoSQL** means **"Not only SQL"**. These databases do **not use fixed tables with joins** like a relational database. DynamoDB stores data as **items (key-value / document style)**.

#### 📦 DynamoDB Is Used For

- 🎮 Gaming (player data, leaderboards)
- 🛒 Shopping carts and session data
- 📱 Mobile and web app backends
- 🏭 IoT data
- 📊 High-traffic applications with simple access patterns

#### 🏗 DynamoDB Basic Architecture

```text
👤 Application
      │
      ▼
⚡ DynamoDB
      │
      ▼
📋 Table
      │
      ├── 🧾 Item 1  (attributes)
      ├── 🧾 Item 2
      └── 🧾 Item 3
```

#### 🧠 Easy Memory

> **DynamoDB = Serverless NoSQL database with very fast key-based access**

---

## 7.2 🤔 Why Do We Use DynamoDB?

### ❌ Traditional Database Problems

```text
🗄️ Relational Database (single server)

❌ Hard to scale for millions of requests
❌ Need to manage servers, replicas, patching
❌ Performance can slow down as data grows
```

### ✅ With DynamoDB

```text
⚡ DynamoDB

✅ Scales automatically (on-demand capacity)
✅ No servers to manage (serverless)
✅ Consistent low latency (milliseconds)
✅ Built-in high availability across multiple AZs
```

#### ⭐ Main Reasons

- ⚡ **Very fast** response time
- 📈 **Automatic scaling** for huge traffic
- ❌ **No server management**
- 🛡️ **High availability** (data copied across multiple AZs in a Region)
- 🌍 **Global Tables** for multi-Region apps
- 💰 Pay for what we use
- 🔗 Works very well with **Lambda** and **API Gateway**

---

## 7.3 🧰 What Does DynamoDB Provide?

DynamoDB provides:

- 📋 Tables, Items and Attributes
- 🔑 Primary Keys (Partition Key, Sort Key)
- 💰 Capacity Modes (Provisioned and On-Demand)
- 📇 Secondary Indexes (LSI and GSI)
- 🔄 Streams
- ⏳ TTL (automatic item expiry)
- 🌍 Global Tables
- ⚡ DAX (in-memory cache)
- 🔁 Transactions
- 📸 Backups and Point-in-Time Recovery
- 🔒 Encryption and IAM access control

---

## 7.4 🧱 DynamoDB Basic Concepts

```text
⚡ DynamoDB
│
└── 📋 Table
      │
      ├── 🧾 Item 1  → { attribute1, attribute2, ... }
      ├── 🧾 Item 2
      └── 🧾 Item 3
```

### 7.4.1 📖 Simple Definitions

| Concept           | Simple Meaning                                              | Relational DB Similar To |
| ----------------- | ----------------------------------------------------------- | ------------------------ |
| 📋 **Table**      | A collection of items                                       | Table                    |
| 🧾 **Item**       | One record in a table                                       | Row                      |
| 🏷️ **Attribute**  | One piece of data in an item                                | Column                   |
| 🔑 **Primary Key**| Uniquely identifies each item                               | Primary Key              |

#### 💻 Example Table: `Students`

```text
📋 Table: Students   (Primary Key: StudentID)

┌───────────┬─────────┬────────┬─────────────────┐
│ StudentID │ Name    │ City   │ Course          │
├───────────┼─────────┼────────┼─────────────────┤
│ 101       │ Rahul   │ Pune   │ AWS             │
│ 102       │ Sara    │ Delhi  │ Python          │
│ 103       │ Amit    │ Mumbai │ DevOps, Linux   │  ← extra attribute style allowed
└───────────┴─────────┴────────┴─────────────────┘
```

#### ⭐ Important Points

- 🔓 DynamoDB is **schema-less** — except for the **primary key**, items in the same table can have **different attributes**
- 📏 Maximum **item size is 400 KB**
- 🌏 A table belongs to **one Region**

#### 🧠 Remember

> **Table → Items → Attributes**

---

## 7.5 🔑 Primary Key

Every table **must have a primary key**. It uniquely identifies each item.

```text
🔑 Primary Key Types
│
├── 1️⃣ Simple Primary Key     → Partition Key only
└── 2️⃣ Composite Primary Key  → Partition Key + Sort Key
```

### 7.5.1 🔑 Partition Key

- The main key used to **find an item**
- DynamoDB uses the partition key value to decide **where (which partition) the item is stored**
- Must be **unique** when it is the only key

```text
Table: Students
Partition Key: StudentID

StudentID = 101 → Rahul
StudentID = 102 → Sara
```

### 7.5.2 🔑 Partition Key + Sort Key (Composite Key)

- **Partition Key** = groups related items
- **Sort Key** = sorts items inside the same partition
- The **combination** must be unique

```text
Table: Orders
Partition Key: CustomerID
Sort Key:      OrderDate

┌────────────┬────────────┬─────────┐
│ CustomerID │ OrderDate  │ Amount  │
├────────────┼────────────┼─────────┤
│ C1         │ 2026-01-05 │ 500     │
│ C1         │ 2026-02-10 │ 900     │   ← same customer, different dates
│ C2         │ 2026-01-20 │ 300     │
└────────────┴────────────┴─────────┘
```

#### 🎯 Why Use a Sort Key?

- 📚 Get **all orders of one customer** in one query
- 📅 Get orders **within a date range**
- 🔢 Items are stored **in sorted order**

### 7.5.3 ✅ Good Partition Key Choice

```text
✅ High number of different values (high cardinality): UserID, OrderID, DeviceID
❌ Few different values: Gender, Country, Status ("active"/"inactive")
```

#### ⚠ Hot Partition

If **too many requests go to the same partition key value**, that partition gets overloaded (**hot partition**), and requests can be throttled.

> **Choose a partition key that spreads requests evenly.**

#### 🧠 Simple Meaning

> **Partition Key = Where the item is stored and found. Sort Key = Order inside the partition.**

---

## 7.6 🔠 Data Types

```text
🔠 DynamoDB Data Types
│
├── 🔤 Scalar     → String (S), Number (N), Binary (B), Boolean (BOOL), Null (NULL)
├── 📚 Document   → List (L), Map (M)
└── 🗂️ Set        → String Set (SS), Number Set (NS), Binary Set (BS)
```

#### 💻 Example Item (JSON style)

```json
{
  "StudentID": "101",
  "Name": "Rahul",
  "Age": 21,
  "Courses": ["AWS", "Python"],
  "Address": {
    "City": "Pune",
    "Pin": "411001"
  }
}
```

#### ⚠ Key Attribute Types

> The **primary key attributes** must be **String, Number or Binary**.

---

## 7.7 💰 Capacity Modes

DynamoDB has two ways to handle **read and write capacity**.

```text
💰 Capacity Modes
│
├── 📏 Provisioned Mode
└── ⚡ On-Demand Mode
```

### 7.7.1 📏 Provisioned Mode

We **set the number of reads and writes per second** we need.

- 📖 **RCU** = Read Capacity Unit
- ✏️ **WCU** = Write Capacity Unit

#### 📖 Capacity Unit Meaning

| Unit            | Meaning                                                                   |
| --------------- | ------------------------------------------------------------------------- |
| 📖 **1 RCU**    | One **strongly consistent** read/second up to **4 KB**, or two **eventually consistent** reads/second up to 4 KB |
| ✏️ **1 WCU**    | One write/second up to **1 KB**                                           |

#### 🧮 Example Calculation

```text
Requirement: 10 writes per second, each item is 2 KB
→ Each write of 2 KB uses 2 WCU
→ Total = 10 × 2 = 20 WCU

Requirement: 10 strongly consistent reads per second, each item is 8 KB
→ Each read of 8 KB uses 8 / 4 = 2 RCU
→ Total = 10 × 2 = 20 RCU
(For eventually consistent reads, it would be half = 10 RCU)
```

#### ⭐ Key Points

- 📈 Can use **Auto Scaling** to adjust capacity automatically
- 💰 Good when traffic is **predictable**
- ⚠️ If we exceed the capacity → requests are **throttled** (error `ProvisionedThroughputExceededException`)

### 7.7.2 ⚡ On-Demand Mode

DynamoDB **automatically handles any traffic**. We **pay per request**.

- ✅ No capacity planning
- ✅ Scales instantly with traffic
- 💰 Good for **new, unpredictable or spiky** workloads
- 💸 Can cost more than provisioned when traffic is steady and high

### 7.7.3 📊 Provisioned vs On-Demand

| 📏 Provisioned                       | ⚡ On-Demand                              |
| ------------------------------------ | ----------------------------------------- |
| We set RCU and WCU                   | No capacity setting                       |
| Auto Scaling available               | Scales automatically                      |
| Cheaper for steady, predictable load | Good for unpredictable load               |
| Throttling if limit is crossed       | Handles traffic spikes automatically      |
| Pay for provisioned capacity         | Pay per read/write request                |

#### 🧠 Easy Memory

```text
📏 Provisioned = We decide the capacity (cheaper if predictable)
⚡ On-Demand   = AWS decides the capacity (easy, pay per request)
```

---

## 7.8 📖 Read Consistency

When we read data, DynamoDB offers different consistency options.

```text
📖 Read Types
│
├── 🔄 Eventually Consistent Read  (default)
├── ✅ Strongly Consistent Read
└── 🔁 Transactional Read
```

### 7.8.1 🔄 Eventually Consistent Read

- ⚡ Default
- 💰 Uses **half** the read capacity
- ⚠️ May return **slightly old data** just after a write

### 7.8.2 ✅ Strongly Consistent Read

- 🆕 Always returns the **latest data**
- 💰 Uses **full** read capacity
- 🐢 Slightly higher latency
- ⚠️ Not available for **Global Secondary Indexes**

### 7.8.3 📊 Comparison

| 🔄 Eventually Consistent         | ✅ Strongly Consistent             |
| -------------------------------- | ---------------------------------- |
| May be slightly old              | Always latest data                 |
| Lower cost (half RCU)            | Higher cost (full RCU)             |
| Faster                           | Slightly slower                    |
| Default                          | Must be requested                  |

---

## 7.9 📇 Secondary Indexes

By default, we can search **only using the primary key**. A **Secondary Index** lets us **query using other attributes**.

```text
📇 Secondary Indexes
│
├── 🌍 GSI → Global Secondary Index
└── 📍 LSI → Local Secondary Index
```

#### 💻 Example Problem

```text
Table: Students   (Partition Key: StudentID)

❓ We want to find all students from "Pune" (City)
❌ City is not a key → We would need a full scan (slow, costly)
✅ Create a GSI with Partition Key = City
```

### 7.9.1 🌍 Global Secondary Index (GSI)

- 🔑 Has a **different partition key (and optional sort key)** from the table
- ➕ Can be created or deleted **at any time**
- 💰 Has its **own read/write capacity**
- 🔄 Supports **only eventually consistent reads**
- 📦 Default limit: **20 GSIs per table**

### 7.9.2 📍 Local Secondary Index (LSI)

- 🔑 Has the **same partition key** as the table but a **different sort key**
- ⏰ Must be created **when the table is created** (cannot be added later)
- 💰 Uses the **table's capacity**
- ✅ Supports **strongly consistent reads**
- 📦 Maximum **5 LSIs per table**
- 📏 Limits the size of one partition key's data to **10 GB**

### 7.9.3 📊 GSI vs LSI

| 🌍 GSI                                | 📍 LSI                                    |
| ------------------------------------- | ----------------------------------------- |
| Different partition key + sort key    | Same partition key, different sort key    |
| Can be added **any time**             | Only at **table creation**                |
| Own capacity                          | Shares table capacity                     |
| Eventually consistent reads only      | Strong or eventual consistency            |
| Up to 20 (default limit)              | Up to 5                                   |

#### 🧠 Easy Memory

```text
🌍 GSI = Global  → Completely different key, add anytime
📍 LSI = Local   → Same partition key, different sort key, only at creation
```

---

## 7.10 🔍 Reading Data: Query vs Scan

### 7.10.1 🎯 Query

- Finds items using the **partition key** (and optionally a sort key condition)
- ✅ **Fast and efficient**
- 💰 Reads only the needed items

```text
Query: CustomerID = "C1" AND OrderDate between "2026-01-01" and "2026-12-31"
```

### 7.10.2 🔄 Scan

- Reads **every item in the table (or index)**
- 🐢 **Slow and expensive** for big tables
- ⚠️ Avoid in production for large tables

```text
Scan: Give all items where Amount > 500   (checks every item)
```

### 7.10.3 📊 Comparison

| 🎯 Query                         | 🔄 Scan                            |
| -------------------------------- | ---------------------------------- |
| Uses the key                     | Reads the whole table              |
| Fast                             | Slow                               |
| Low cost                         | High cost                          |
| Recommended                      | Use only when needed               |

#### 🧠 Remember

> **Query = Use keys (good). Scan = Check everything (avoid).**

---

## 7.11 🛠 DynamoDB Operations

```text
🛠️ Main Operations
│
├── ➕ PutItem        → Create or replace an item
├── 🔍 GetItem        → Read one item by primary key
├── ✏️ UpdateItem     → Change attributes of an item
├── 🗑️ DeleteItem     → Delete an item
├── 🎯 Query          → Read items with the partition key
├── 🔄 Scan           → Read all items
├── 📦 BatchGetItem   → Read many items in one call
└── 📦 BatchWriteItem → Write/delete many items in one call
```

### 7.11.1 ⌨ AWS CLI Examples

```bash
# Create a table
aws dynamodb create-table \
  --table-name Students \
  --attribute-definitions AttributeName=StudentID,AttributeType=S \
  --key-schema AttributeName=StudentID,KeyType=HASH \
  --billing-mode PAY_PER_REQUEST

# Put an item
aws dynamodb put-item \
  --table-name Students \
  --item '{"StudentID": {"S": "101"}, "Name": {"S": "Rahul"}, "City": {"S": "Pune"}}'

# Get an item
aws dynamodb get-item \
  --table-name Students \
  --key '{"StudentID": {"S": "101"}}'

# Query items
aws dynamodb query \
  --table-name Orders \
  --key-condition-expression "CustomerID = :c" \
  --expression-attribute-values '{":c": {"S": "C1"}}'
```

#### 📖 Understanding It

```text
HASH      = Partition Key
RANGE     = Sort Key
S / N / B = String / Number / Binary
PAY_PER_REQUEST = On-Demand mode
```

### 7.11.2 🐍 Python (boto3) Example

```python
import boto3

dynamodb = boto3.resource("dynamodb", region_name="ap-south-1")
table = dynamodb.Table("Students")

# Put an item
table.put_item(Item={"StudentID": "101", "Name": "Rahul", "City": "Pune"})

# Get an item
response = table.get_item(Key={"StudentID": "101"})
print(response.get("Item"))

# Update an item
table.update_item(
    Key={"StudentID": "101"},
    UpdateExpression="SET City = :c",
    ExpressionAttributeValues={":c": "Mumbai"},
)

# Delete an item
table.delete_item(Key={"StudentID": "101"})
```

---

## 7.12 🔄 DynamoDB Streams

**DynamoDB Streams** records **every change** (insert, update, delete) made to items in a table.

```text
📋 DynamoDB Table
        │ item changes
        ▼
🔄 DynamoDB Stream (change log, kept for 24 hours)
        │
        ▼
⚡ Lambda Function  → reacts to changes
```

#### 🎯 Used For

- 📧 Send a **welcome email** when a new user item is added
- 🔁 **Replicate** data to another system
- 📊 Update **analytics or search indexes**
- 🕵️ **Audit** changes

#### ⭐ Key Points

- ⏱️ Stream records are available for **24 hours**
- 🔗 Commonly used with **Lambda triggers**

---

## 7.13 ⏳ TTL (Time To Live)

**TTL** automatically **deletes items after a set time**.

```text
🧾 Item has attribute:  expiresAt = 1767225600  (a Unix timestamp)
        ↓
⏰ When current time passes expiresAt
        ↓
🗑️ DynamoDB deletes the item automatically (no write cost)
```

#### 🎯 Used For

- 🔐 Session data
- 📝 Temporary tokens or OTPs
- 🧹 Old logs and temporary data

#### ⭐ Key Points

- 🕒 The TTL attribute must be a **Number** with an **epoch time (seconds)**
- ⏳ Deletion happens **within a few days after expiry** (not instantly)
- 💰 TTL deletions **do not consume write capacity**

---

## 7.14 ⚡ DAX (DynamoDB Accelerator)

**DAX** is a **fully managed in-memory cache** for DynamoDB.

```text
📱 Application
      │
      ▼
⚡ DAX Cluster (in-memory cache)
      │ (only on cache miss)
      ▼
📋 DynamoDB Table
```

#### ⭐ Key Points

- ⚡ Response time improves from **milliseconds to microseconds**
- 🔁 **No application logic change** — uses DAX client
- 📈 Good for **read-heavy** and repeated-read workloads
- 💰 Reduces the read load (and cost) on the table
- ⚠️ DAX works with **eventually consistent** reads

> **DAX = Cache in front of DynamoDB for microsecond reads**

---

## 7.15 🌍 Global Tables

**Global Tables** automatically **replicate a DynamoDB table across multiple AWS Regions**.

```text
🌏 Mumbai Region  ◄──── replication ────►  🌎 N. Virginia Region
   📋 Table                                    📋 Table
   (read + write)                              (read + write)
```

#### 🎯 Used For

- 🌍 Users in different parts of the world get **low latency**
- 🛡️ **Disaster recovery** (if one Region fails, another is available)
- ✏️ **Multi-Region, multi-active** (we can write in any Region)

#### ⚠ Requirement

> **DynamoDB Streams must be enabled** for Global Tables (it is managed for us).

---

## 7.16 🔁 Transactions

DynamoDB supports **ACID transactions** across multiple items and tables.

```text
🔁 Transaction
│
├── ✏️ TransactWriteItems → Many writes: ALL succeed or ALL fail
└── 📖 TransactGetItems   → Many reads in one consistent operation
```

#### 💻 Example

```text
Transfer money:
  1. Subtract ₹500 from Account A
  2. Add ₹500 to Account B

✅ Both succeed together
❌ Or both fail (nothing changes)
```

#### ⚠ Important

> Transactions use **more capacity** (about **2×**) than normal reads/writes.

---

## 7.17 📸 Backup and Restore

```text
📸 Backup Options
│
├── 🖐️ On-Demand Backup        → We create a backup when we want
├── ⏪ Point-in-Time Recovery   → Restore to any second in the last 35 days
└── 🌍 AWS Backup               → Central backup management
```

#### ⭐ Key Points

- ⏪ **PITR** must be **enabled** (it is not on by default)
- 📅 PITR keeps **35 days** of history
- 🔁 Restore creates a **new table** (does not overwrite the old one)
- 🚀 Backups do **not use table capacity** and have **no performance impact**

---

## 7.18 🔒 DynamoDB Security

```text
🔐 DynamoDB Security
│
├── 📜 IAM Policies          → Who can access tables and actions
├── 🎯 Fine-grained access   → Control access down to item/attribute level
├── 🔒 Encryption at Rest    → Always enabled (AWS owned / AWS managed / customer managed KMS key)
├── 🌐 Encryption in Transit → HTTPS
└── 🔌 VPC Gateway Endpoint  → Private access from a VPC (no internet needed)
```

#### 💻 Example IAM Policy (Read-Only for One Table)

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "dynamodb:GetItem",
        "dynamodb:Query",
        "dynamodb:Scan"
      ],
      "Resource": "arn:aws:dynamodb:ap-south-1:123456789012:table/Students"
    }
  ]
}
```

#### ⚠ Important

> **DynamoDB does not use database passwords or open ports.** Access is controlled by **IAM**.

---

## 7.19 🆚 DynamoDB vs RDS

| Feature              | ⚡ DynamoDB                        | 🗄️ RDS                              |
| -------------------- | ---------------------------------- | ----------------------------------- |
| Type                 | NoSQL (key-value / document)       | Relational (SQL)                    |
| Schema               | Flexible (only key fixed)          | Fixed schema                        |
| Scaling              | Automatic, almost unlimited        | Scale up the instance / add replicas|
| Servers              | Serverless                         | DB instances (managed by AWS)       |
| Joins                | ❌ No joins                        | ✅ Supports joins                   |
| Query Style          | By key and indexes                 | Complex SQL queries                 |
| Access               | IAM + HTTPS API                    | Database user/password + port       |
| Performance          | Single-digit millisecond           | Depends on instance size and query  |
| Best For             | Simple, high-scale access patterns | Complex queries, relationships      |

#### 🧠 Easy Memory

```text
⚡ DynamoDB = Fast key-based lookups at any scale (NoSQL)
🗄️ RDS      = Complex relationships and SQL queries
```

---

## 7.20 🧠 Data Modeling Tips

- 🎯 Design tables **around how the application will read the data** (access patterns)
- 🔑 Pick a **high-cardinality partition key**
- 📚 Use **sort keys** to group and order related items
- 🚫 Avoid **Scan** on big tables
- 📇 Add **GSIs** for extra query patterns
- 🏷️ Many applications use **one table** for multiple item types (single-table design) — advanced topic

#### ⚠ Important

> **In DynamoDB we plan the queries first, then design the table.** (In SQL we usually design tables first.)

---

## 7.21 💰 DynamoDB Pricing

```text
💰 DynamoDB Cost
│
├── 📖✏️ Read / Write requests (On-Demand) or RCU / WCU (Provisioned)
├── 💾 Data storage (per GB per month)
├── 📇 Global Secondary Indexes (storage + capacity)
├── 🌍 Global Tables (replicated writes)
├── ⚡ DAX nodes (per hour)
├── 📸 Backups / PITR
└── 🌐 Data transfer out
```

- 🎁 There is an **always-free tier** (some storage and capacity)
- 🏷️ **Standard-IA table class** is cheaper for storage when data is rarely accessed

---

## 7.22 🏗 Real Example: Serverless Products API

### 🎯 Requirement

Store and fetch product data for a mobile app using a serverless backend.

### 🏗 Architecture

```text
📱 Mobile App
     │
     ▼
🚪 API Gateway
     │
     ▼
⚡ Lambda
     │
     ▼
⚡ DynamoDB Table: Products
   Partition Key: ProductID
```

### 🪜 Steps to Build It

```text
1. Create table: Products
     → Partition key: ProductID (String)
     → Capacity mode: On-Demand
2. (Optional) Create a GSI on Category for "show products by category"
3. Create a Lambda function with an IAM role allowing
     dynamodb:GetItem, PutItem, Query on the table
4. Write Lambda code using boto3 to read and write items
5. Create an API Gateway route for GET /products/{id} and POST /products
6. Connect the routes to the Lambda function
7. ✅ Test the API
```

#### 💻 Lambda Code Example

```python
import json
import boto3

table = boto3.resource("dynamodb").Table("Products")

def lambda_handler(event, context):
    product_id = event["pathParameters"]["id"]
    response = table.get_item(Key={"ProductID": product_id})
    item = response.get("Item")

    if not item:
        return {"statusCode": 404, "body": json.dumps({"message": "Not found"})}

    return {"statusCode": 200, "body": json.dumps(item, default=str)}
```

> 💡 `default=str` is used because DynamoDB returns numbers as `Decimal`, which JSON cannot convert directly.

---

## 📌🧠 DynamoDB Quick Revision

```text
⚡ DynamoDB
│
├── 🧱 Basics
│   ├── 📋 Table
│   ├── 🧾 Item
│   └── 🏷️ Attribute
│
├── 🔑 Primary Key
│   ├── Partition Key
│   └── Partition Key + Sort Key
│
├── 💰 Capacity Modes
│   ├── 📏 Provisioned (RCU / WCU)
│   └── ⚡ On-Demand
│
├── 📖 Read Types
│   ├── Eventually Consistent
│   ├── Strongly Consistent
│   └── Transactional
│
├── 📇 Indexes
│   ├── 🌍 GSI
│   └── 📍 LSI
│
├── 🔍 Access
│   ├── 🎯 Query
│   └── 🔄 Scan
│
├── ⚙️ Features
│   ├── 🔄 Streams (24 hours)
│   ├── ⏳ TTL
│   ├── ⚡ DAX
│   ├── 🌍 Global Tables
│   └── 🔁 Transactions
│
└── 🔒 Protection
    ├── 📸 Backups + PITR (35 days)
    └── 🔐 IAM + Encryption
```

---

## 🧠⚡ DynamoDB One-Line Memory

| Concept                      | Easy Memory                                         |
| ---------------------------- | --------------------------------------------------- |
| ⚡ **DynamoDB**              | Serverless NoSQL Database                           |
| 📋 **Table**                 | Collection of Items                                 |
| 🧾 **Item**                  | One Record (Like a Row), Max 400 KB                 |
| 🏷️ **Attribute**             | One Piece of Data (Like a Column)                   |
| 🔑 **Partition Key**         | Decides Where an Item Is Stored                     |
| 🔑 **Sort Key**              | Orders Items Inside a Partition                     |
| 📏 **Provisioned Mode**      | We Set RCU and WCU                                  |
| ⚡ **On-Demand Mode**        | Pay Per Request, Auto Scaling                       |
| 📖 **1 RCU**                 | One Strong Read/sec up to 4 KB                      |
| ✏️ **1 WCU**                 | One Write/sec up to 1 KB                            |
| 🌍 **GSI**                   | Different Key, Add Anytime                          |
| 📍 **LSI**                   | Same Partition Key, Only at Table Creation          |
| 🎯 **Query**                 | Use Keys — Fast                                     |
| 🔄 **Scan**                  | Read Everything — Avoid                             |
| 🔄 **Streams**               | Change Log for 24 Hours                             |
| ⏳ **TTL**                   | Auto-Delete Expired Items                           |
| ⚡ **DAX**                   | In-Memory Cache, Microsecond Reads                  |
| 🌍 **Global Tables**         | Multi-Region Replication                            |
| ⏪ **PITR**                  | Restore to Any Second in Last 35 Days               |

---

## 🗺 DynamoDB Learning Map

```text
                          ⚡ DynamoDB
                                │
       ┌────────────────────────┼────────────────────────┐
       │                        │                        │
       ▼                        ▼                        ▼
    DATA MODEL               CAPACITY                 ACCESS
       │                        │                        │
       ├── Table                ├── Provisioned          ├── Query
       ├── Item                 │    (RCU / WCU)         ├── Scan
       ├── Attribute            └── On-Demand            ├── Get / Put / Update
       └── Primary Key                                   └── Batch Operations
            ├── Partition Key
            └── Sort Key
       │
       ▼
    INDEXES
       │
       ├── GSI
       └── LSI
       │
       ▼
   ADVANCED FEATURES
       │
       ├── Streams  → Lambda
       ├── TTL
       ├── DAX
       ├── Global Tables
       └── Transactions
       │
       ▼
   PROTECTION
       │
       ├── Backups / PITR
       ├── IAM Policies
       └── Encryption
```

---

## ⭐ DynamoDB Final Memory

```text
DynamoDB
 │
 ├── What is it?
 │      └── Serverless NoSQL Database
 │
 ├── What is a record called?
 │      └── Item
 │
 ├── What uniquely identifies an item?
 │      └── Primary Key (Partition Key [+ Sort Key])
 │
 ├── How to avoid capacity planning?
 │      └── On-Demand Mode
 │
 ├── How to search by a non-key attribute?
 │      └── Secondary Index (GSI)
 │
 ├── Fast read or slow read?
 │      └── Query (fast), Scan (slow)
 │
 ├── How to react to changes?
 │      └── Streams + Lambda
 │
 ├── How to auto-delete old items?
 │      └── TTL
 │
 ├── How to get microsecond reads?
 │      └── DAX
 │
 ├── How to replicate across Regions?
 │      └── Global Tables
 │
 └── How to restore deleted data?
        └── PITR (35 days) / Backups
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

#### 1⃣ ⏳ Synchronous Invocation

The caller **waits** for the response.

**Examples:** API Gateway, Function URL, Application Load Balancer

```text
👤 User → 🌐 API Gateway → ⚡ Lambda → 📤 Response → 👤 User
```

---

#### 2⃣ 📤 Asynchronous Invocation

The caller sends the event and **does not wait**. Lambda handles retries.

**Examples:** S3, SNS, EventBridge

#### ⭐ Key Points

- 🔁 Lambda **retries twice** if the function fails (total 3 attempts)
- 📮 Failed events can be sent to a **Dead-Letter Queue (DLQ)** or a failure destination

---

#### 3⃣ 📬 Event Source Mapping

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

## 8.9 ⚙ Lambda Configuration

### 8.9.1 🧠 Memory

- Memory can be set from **128 MB to 10,240 MB (10 GB)**
- 🧩 **CPU power increases with memory** (more memory = more CPU)

### 8.9.2 ⏱ Timeout

- Default timeout is **3 seconds**
- Maximum timeout is **15 minutes (900 seconds)**

### 8.9.3 🔐 Environment Variables

Key-value settings available to our code.

```text
DB_HOST = mydb.xxxx.rds.amazonaws.com
STAGE   = production
```

#### ⚠ Important

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

### 8.11.2 🏷 Aliases

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

## 8.13 ⚖ Concurrency

**Concurrency** is the **number of function copies running at the same time**.

```text
📨 100 requests at once
        ↓
⚡ Lambda runs many copies together (scales automatically)
```

### 8.13.1 🗂 Types of Concurrency

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

#### ⚠ Important

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

#### ⚠ Important

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

#### ⚠ Important

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

## 8.18 🏗 Real Example: Auto Thumbnail Creator

### 🎯 Requirement

When a user uploads an image to an S3 bucket, create a smaller thumbnail automatically.

### 🏗 Architecture

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

#### ⚠ Important

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

## 8.19 ⚖ Lambda vs EC2

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

## 🗺 Lambda Learning Map

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

## 9.4 🏗 What Beanstalk Creates for Us

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

#### 🏗 Architecture

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

#### ⚠ Important

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

### 9.5.2 🏗 Relationship

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

### 9.6.2 ⚙ Worker Tier

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

## 9.8 🛠 Supported Platforms

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

### 9.10.1 1⃣ All at Once

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

### 9.10.2 2⃣ Rolling

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

### 9.10.3 3⃣ Rolling with Additional Batch

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

### 9.10.4 4⃣ Immutable

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

### 9.10.5 5⃣ Traffic Splitting

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

### 9.12.1 ⌨ EB CLI Common Commands

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

#### ⚠ Important

> Do **not** put secrets directly in code. Use environment properties with care, or **AWS Secrets Manager**.

---

## 9.14 🎭 IAM Roles in Beanstalk

```text
🎭 Beanstalk Roles
│
├── 🛠️ Service Role     → Lets Beanstalk manage AWS resources for us
└── 🖥️ Instance Profile → Role used by the EC2 instances
```

### 9.14.1 🛠 Service Role

Allows Elastic Beanstalk to **create and manage** AWS resources (like Auto Scaling, Load Balancer, health reporting) on our behalf.

### 9.14.2 🖥 Instance Profile

An IAM role attached to the **EC2 instances** in the environment.

It allows the application to:

- 🪣 Upload logs and versions to S3
- 📊 Send data to CloudWatch
- 🔗 Access other AWS services our app needs (like S3 or DynamoDB)

#### 🧠 Simple Difference

> **Service Role = Permissions for Beanstalk itself. Instance Profile = Permissions for our app's EC2 instances.**

---

## 9.15 🗄 Database with Beanstalk

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

#### ⚠ Important

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

## 9.20 🏗 Real Example: Deploy a Python Flask App

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

#### ⚠ Important

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

### 🏗 What Beanstalk Built for Us

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

## 🗺 Elastic Beanstalk Learning Map

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

# 🧭 PART 10 — Route 53 — DNS Service

> **Route 53 = AWS DNS Service**

---

## 10.1 🧭 What is Route 53?

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

## 10.2 🤔 Why Do We Use Route 53?

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

## 10.3 🧰 What Does Route 53 Provide?

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

## 10.4 🧠 DNS Basics

### 10.4.1 📖 What is DNS?

> **DNS = Domain Name System**

DNS converts a **domain name** into an **IP address**.

```text
www.example.com  ──►  DNS  ──►  203.0.113.10
```

### 10.4.2 🧱 Parts of a Domain Name

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

### 10.4.3 🔄 How DNS Works (Step by Step)

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

## 10.5 🏷 Domain Registration

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

## 10.6 📂 Hosted Zone

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

### 10.6.1 🗂 Types of Hosted Zones

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

#### ⚠ Important

> For a **Private Hosted Zone**, the VPC must have **DNS resolution** and **DNS hostnames** enabled.

> **Hosted Zone = Container of DNS records for a domain**

---

## 10.7 📄 DNS Records

A **DNS Record** tells DNS **what to answer** for a name.

#### 🧱 Parts of a Record

| Part           | Meaning                                  |
| -------------- | ---------------------------------------- |
| 🏷️ Name        | The domain/subdomain (www.example.com)   |
| 🔠 Type        | Record type (A, CNAME ...)               |
| 🎯 Value       | The answer (IP address or name)          |
| ⏱️ TTL         | How long to cache the answer             |
| 🔀 Routing Policy | How Route 53 answers                  |

### 10.7.1 📋 Common Record Types

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

## 10.8 ⏱ TTL

> **TTL = Time To Live**

TTL tells DNS resolvers **how long to cache (remember) a record**.

```text
TTL = 300 seconds
→ Resolvers remember the answer for 5 minutes
```

#### ⚖ High TTL vs Low TTL

| ⏱️ High TTL (like 24 hours)         | ⚡ Low TTL (like 60 seconds)         |
| ----------------------------------- | ------------------------------------ |
| Fewer DNS queries                   | More DNS queries                     |
| Lower cost                          | Higher cost                          |
| Changes take longer to reach users  | Changes reach users faster           |

#### 💡 Tip

> Before changing an important DNS record (like moving to a new server), **lower the TTL first**, then make the change.

#### ⚠ Important

> **Alias records do not have a TTL setting.** Route 53 manages it.

---

## 10.9 🔗 CNAME Record

A **CNAME** points one domain name to **another domain name**.

```text
www.example.com  ──CNAME──►  example.com
```

#### ⚠ Important Rule

> **A CNAME cannot be created for the root (apex) domain** such as `example.com`. It can be created only for subdomains such as `www.example.com`.

---

## 10.10 ⭐ Alias Record

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

### 10.10.1 ⚖ CNAME vs Alias

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

## 10.11 🔀 Routing Policies

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

### 10.11.1 1⃣ Simple Routing

One record with one or more values. No special rules.

```text
www.example.com ──► 203.0.113.10
```

- ✅ Easiest policy
- ❌ Cannot be used with Health Checks (when multiple values are given, a random value is returned to the client)

> **Simple = Basic one-to-one routing**

---

### 10.11.2 2⃣ Weighted Routing

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

### 10.11.3 3⃣ Latency Routing

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

### 10.11.4 4⃣ Failover Routing

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

### 10.11.5 5⃣ Geolocation Routing

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

#### ⚠ Important

> Create a **Default** record, so users from locations we did not define still get an answer.

> **Geolocation = Route by user's country/continent**

---

### 10.11.6 6⃣ Geoproximity Routing

Route based on the **distance** between the user and our resources.

We can use a **bias** value to send **more or less traffic** to a resource.

```text
Bias +   → Resource gets more traffic (bigger area)
Bias -   → Resource gets less traffic (smaller area)
```

> **Geoproximity = Route by distance, adjustable with bias**

---

### 10.11.7 7⃣ Multivalue Answer Routing

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

## 10.12 ❤ Health Checks

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

### 10.12.1 🗂 Types of Health Checks

```text
❤️ Health Checks
│
├── 🌐 Endpoint Health Check
├── 🧮 Calculated Health Check
└── 📈 CloudWatch Alarm Health Check
```

#### 1⃣ 🌐 Endpoint Health Check

Checks a **specific endpoint** (IP address or domain name) using HTTP, HTTPS or TCP.

#### 2⃣ 🧮 Calculated Health Check

Combines the results of **multiple health checks** (AND, OR or "at least X healthy").

#### 3⃣ 📈 CloudWatch Alarm Health Check

Uses the state of a **CloudWatch Alarm**. This is useful for **private resources** that Route 53 checkers cannot reach directly.

#### ⚠ Important

> Route 53 health checkers are on the **public internet**, so they **cannot directly check resources in a private subnet**. Use a **CloudWatch Alarm** health check for those.

#### ⭐ Key Points

- 🔔 Can send notifications using **Amazon SNS**
- ⏱️ We can set the check interval and failure threshold
- 🛠️ The health check path can be like `/health`

> **Health Check = Route 53 checks if our server is alive**

---

## 10.13 🔁 Route 53 Resolver

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

## 10.14 💰 Route 53 Pricing

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

## 10.15 🏗 Real Example: Domain to Load Balancer

### 🎯 Requirement

Open `www.example.com` and reach a website running behind an Application Load Balancer.

### 🏗 Architecture

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

### 🛡 Failover Example (Active-Passive)

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

## 🗺 Route 53 Learning Map

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

# 🌍 PART 11 — CloudFront — Content Delivery Network (CDN)

> **CloudFront = Cache content near users for faster delivery**

---

## 11.1 🌍 What is CloudFront?

> **CloudFront = AWS Content Delivery Network (CDN)**

Amazon CloudFront is a **CDN (Content Delivery Network)** service.

It **delivers our content (web pages, images, videos, APIs) to users with low delay** by **caching copies at AWS Edge Locations** close to the users.

#### 🤔 What is a CDN?

A **CDN** is a **network of servers spread around the world**. It keeps copies of our content near users, so users do not need to reach the original server every time.

#### 🏗 CloudFront Basic Architecture

```text
👤 User (Mumbai)
      │
      ▼
📍 Nearest Edge Location (Mumbai)
      │
      ├── ✅ Content in cache  → Return immediately (fast)
      │
      └── ❌ Not in cache      → Get from Origin, save in cache, then return
                                        │
                                        ▼
                                 🪣 Origin (S3 / ALB / EC2 ...)
                                 (in another Region, e.g. N. Virginia)
```

#### 📦 CloudFront Can Deliver

- 🌐 Static website files (HTML, CSS, JS, images)
- 🎥 Video streaming
- 📥 Software downloads
- 🔌 Dynamic content and APIs

#### 🧠 Easy Memory

> **CloudFront = Keep copies of our content near users for faster delivery**

---

## 11.2 🤔 Why Do We Use CloudFront?

### ❌ Without CloudFront

```text
👤 User in India ──────── long distance ────────► 🖥️ Server in USA

❌ Slow loading (high latency)
❌ Origin server handles every request
❌ Higher load and cost on the origin
```

### ✅ With CloudFront

```text
👤 User in India ──► 📍 Edge Location in India ──(only if needed)──► 🖥️ Origin in USA

✅ Fast loading
✅ Less load on the origin
✅ Better security options
✅ Lower data transfer cost from the origin
```

#### ⭐ Main Reasons

- ⚡ **Faster** content delivery (low latency)
- 🌍 **Global reach** through many edge locations
- 📉 **Reduces load** on the origin server
- 🔒 **Security**: HTTPS, DDoS protection, WAF, signed URLs
- 💰 Often **lower cost** for data transfer
- 📈 Handles **traffic spikes** easily

---

## 11.3 🧰 What Does CloudFront Provide?

CloudFront provides:

- 🌍 Global Edge Locations
- 📦 Distributions
- 🎯 Origins and Origin Groups
- 🧭 Cache Behaviors
- ⏱️ Caching with TTL
- 🔄 Invalidation
- 🔒 HTTPS and Custom SSL Certificates
- 🔑 Signed URLs and Signed Cookies
- 🛡️ AWS WAF and Shield Integration
- ⚡ CloudFront Functions and Lambda@Edge
- 🌐 Geo Restriction
- 📊 Logging and Monitoring

---

## 11.4 📍 CloudFront Infrastructure

```text
📍 CloudFront Network
│
├── 📍 Edge Locations           → Many locations worldwide, closest to users
└── 🏢 Regional Edge Caches     → Bigger caches between edge locations and origin
```

### 11.4.1 📍 Edge Location

The place where content is **cached and delivered to users**.

### 11.4.2 🏢 Regional Edge Cache

A **larger cache layer** between Edge Locations and the Origin.

```text
👤 User
   ↓
📍 Edge Location  (small cache)
   ↓ (miss)
🏢 Regional Edge Cache (bigger cache)
   ↓ (miss)
🪣 Origin
```

#### ⭐ Key Points

- ✅ Fewer requests reach the origin
- 📈 Keeps less-popular content cached longer

---

## 11.5 🧱 CloudFront Basic Concepts

```text
🌍 CloudFront
│
├── 📦 Distribution     → Main CloudFront setup (gets a domain name)
├── 🎯 Origin           → Where the original content is stored
├── 🧭 Cache Behavior   → Rules for different URL paths
├── ⏱️ TTL              → How long content stays in cache
└── 🔄 Invalidation     → Remove content from cache before TTL ends
```

### 11.5.1 📖 Simple Definitions

| Concept             | Simple Meaning                                                        |
| ------------------- | --------------------------------------------------------------------- |
| 📦 Distribution     | The CloudFront configuration; it gets a domain like `d1234abcd.cloudfront.net` |
| 🎯 Origin           | The source of our content (S3 bucket, ALB, EC2, API Gateway, custom server) |
| 🧭 Cache Behavior   | Settings applied to a **URL path pattern** (like `/images/*`)         |
| ⏱️ TTL              | Time to Live — how long an object stays in cache                      |
| ✅ Cache Hit        | Content found in cache → returned fast                                |
| ❌ Cache Miss       | Content not in cache → fetched from the origin                        |
| 🔄 Invalidation     | A request to remove cached objects                                    |

### 11.5.2 📊 Cache Hit vs Cache Miss

```text
✅ Cache HIT
👤 → 📍 Edge (has content) → 👤       (fast, origin not used)

❌ Cache MISS
👤 → 📍 Edge (no content) → 🪣 Origin → 📍 Edge (saves copy) → 👤
```

#### 🧠 Remember

> **Higher Cache Hit ratio = Faster and cheaper**

---

## 11.6 🎯 Origins

An **Origin** is the **place where our original content lives**.

```text
🎯 CloudFront Origins
│
├── 🪣 Amazon S3 bucket
├── ⚖️ Application Load Balancer (ALB)
├── 🖥️ EC2 instance / custom HTTP server
├── 🚪 API Gateway
├── 🌱 Elastic Beanstalk environment
└── 🌐 Any public HTTP/HTTPS server (even outside AWS)
```

### 11.6.1 🪣 S3 Origin

```text
👤 → 📍 CloudFront → 🪣 S3 Bucket (private)
```

- ✅ Best for **static websites and files**
- 🔒 Keep the bucket **private** and allow only CloudFront (using **OAC**)

### 11.6.2 ⚖ ALB / EC2 / Custom Origin

```text
👤 → 📍 CloudFront → ⚖️ Application Load Balancer → 🖥️ EC2 Servers
```

- ✅ Best for **dynamic websites and APIs**

### 11.6.3 🛟 Origin Groups (Failover)

An **Origin Group** has a **primary origin** and a **secondary origin**.

```text
📍 CloudFront
     │
     ├── 🟢 Primary Origin (S3 in Mumbai)
     │        ❌ fails (error codes like 5xx)
     │            ↓
     └── 🟡 Secondary Origin (S3 in Singapore)
```

> **Origin Group = Backup origin for high availability**

---

## 11.7 🔒 Securing the S3 Origin (OAC)

We do **not** want users to open our S3 bucket directly. We want users to go **only through CloudFront**.

```text
❌ User ──► S3 bucket directly  (blocked)

✅ User ──► CloudFront ──► S3 bucket (allowed)
```

### 11.7.1 🛡 Origin Access Control (OAC)

**OAC** lets CloudFront **securely access a private S3 bucket**.

#### 🪜 How It Works

```text
1. 🪣 Keep the S3 bucket PRIVATE (Block Public Access ON)
2. 🌍 Create an OAC and attach it to the CloudFront origin
3. 📜 Add a bucket policy allowing the CloudFront distribution to read objects
4. ✅ Only CloudFront can read the objects
```

#### 💻 Example Bucket Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "Service": "cloudfront.amazonaws.com" },
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-website-bucket/*",
      "Condition": {
        "StringEquals": {
          "AWS:SourceArn": "arn:aws:cloudfront::123456789012:distribution/EDFDVBD6EXAMPLE"
        }
      }
    }
  ]
}
```

#### ⚠ Important

> **OAC is the newer and recommended method.** The older method is **OAI (Origin Access Identity)**.

> **OAC = Private S3 bucket that only CloudFront can read**

---

## 11.8 🧭 Cache Behaviors

A **Cache Behavior** defines **how CloudFront handles requests for a specific URL path**.

```text
🌍 Distribution
│
├── 🧭 /images/*     → Origin: S3 bucket      (cache for 1 day)
├── 🧭 /api/*        → Origin: API Gateway    (no cache)
└── 🧭 Default (*)   → Origin: ALB            (cache 5 minutes)
```

#### 🎯 A Behavior Can Control

- 🎯 Which **origin** to use
- 🔒 **HTTP / HTTPS** rules (redirect HTTP to HTTPS)
- 🔧 Allowed **HTTP methods** (GET, POST ...)
- ⏱️ **Cache TTL** and cache policy
- 🔑 **Restrict viewer access** (signed URLs)
- ⚡ Attached **functions** (CloudFront Functions / Lambda@Edge)
- 🗜️ **Compression**

#### ⭐ Key Points

- 🥇 The **Default behavior** (`*`) is always present
- 🔢 More specific path patterns are matched first

---

## 11.9 ⏱ Caching and TTL

CloudFront keeps objects in cache for a time (TTL).

```text
⏱️ TTL Settings
│
├── 🔽 Minimum TTL   → Shortest time to keep an object
├── 🔸 Default TTL   → Used when origin gives no cache headers (default: 24 hours)
└── 🔼 Maximum TTL   → Longest time to keep an object (default: 1 year)
```

#### 📖 Controlling Cache From the Origin

The origin can send headers like:

```text
Cache-Control: max-age=3600     → Cache for 1 hour
Cache-Control: no-cache         → Do not cache
```

#### 🧭 Cache Key and Policies

The **Cache Key** decides **what makes two requests the "same"** (URL, headers, cookies, query strings).

- ✅ Include **only what is needed** in the cache key → higher hit ratio
- 🧩 Use **Cache Policies** and **Origin Request Policies** to control this

#### 🧠 Simple Meaning

> **TTL = How long CloudFront remembers a file before asking the origin again**

---

## 11.10 🔄 Invalidation

Sometimes we **update a file** but CloudFront still has the **old version** cached.

An **Invalidation** removes objects from edge caches.

```text
📝 We update  /index.html  on the origin
        ↓
🔄 Create Invalidation for /index.html
        ↓
🗑️ Edge locations remove the old copy
        ↓
✅ Next request gets the new file
```

#### 💻 Examples

```text
/index.html        → One file
/images/*          → All files under /images
/*                 → Everything
```

#### ⭐ Key Points

- 💰 A limited number of invalidation paths each month are **free**, extra paths are charged
- ✅ Better approach: use **versioned file names** (like `app.v2.js` or `app.3f2a.js`) instead of invalidating often

```text
❌ Update  style.css          → needs invalidation
✅ Use     style.v2.css       → new name = new cache entry automatically
```

> **Invalidation = Force CloudFront to forget cached files**

---

## 11.11 🔒 CloudFront Security

```text
🔐 CloudFront Security
│
├── 🔒 HTTPS (Viewer and Origin)
├── 🔑 Signed URLs / Signed Cookies
├── 🌐 Geo Restriction
├── 🛡️ AWS WAF
├── 🛡️ AWS Shield (DDoS protection)
├── 🪣 OAC (private S3 origin)
└── 🔐 Field-Level Encryption
```

### 11.11.1 🔒 HTTPS and SSL Certificates

- 🌍 CloudFront provides a default `*.cloudfront.net` certificate
- 🏷️ For our **own domain** (like `www.example.com`), use a certificate from **AWS Certificate Manager (ACM)**

#### ⚠ Important

> **The ACM certificate used with CloudFront must be created in the `us-east-1` (N. Virginia) Region.**

#### 🔁 Viewer Protocol Policy

```text
🔁 Viewer Protocol Policy
│
├── HTTP and HTTPS       → Allow both
├── Redirect HTTP to HTTPS → Recommended
└── HTTPS Only           → Block HTTP
```

### 11.11.2 🔑 Signed URLs and Signed Cookies

Used to give **private content** only to **authorized users** (paid videos, member-only files).

```text
👤 User logs in on our app
        ↓
🔑 App creates a Signed URL (valid for limited time)
        ↓
📍 CloudFront checks the signature
        ↓
✅ Content delivered
```

| 🔗 Signed URL                          | 🍪 Signed Cookie                        |
| -------------------------------------- | --------------------------------------- |
| Access to **one file**                 | Access to **many files**                |
| Link has the signature                 | Signature is stored in a cookie         |
| Good for single downloads              | Good for streaming / whole sections     |

### 11.11.3 🌐 Geo Restriction

Allow or block users **by country**.

```text
✅ Allow List  → Only selected countries can access
❌ Block List  → Selected countries are blocked
```

### 11.11.4 🛡 AWS WAF and Shield

- 🛡️ **AWS WAF** — blocks bad requests (SQL injection, bad IPs, bots)
- 🛡️ **AWS Shield Standard** — free DDoS protection, automatically included for CloudFront

---

## 11.12 ⚡ CloudFront Functions and Lambda@Edge

We can **run code at the edge** to change requests and responses.

```text
👤 Viewer ──► 📍 Edge ──► [Code runs here] ──► 🎯 Origin
```

### 11.12.1 ⚡ CloudFront Functions

- 🪶 Very lightweight JavaScript functions
- ⚡ Extremely fast, runs at **every edge location**
- 🎯 Used for **simple tasks**: URL rewrite, redirects, header changes, simple authorization checks

### 11.12.2 ⚡ Lambda@Edge

- 🧠 More powerful Lambda functions that run at **Regional Edge Caches**
- ⏱️ Can run longer and use more features
- 🎯 Used for **complex logic**: custom authentication, dynamic content changes, calling other services

### 11.12.3 📊 Comparison

| ⚡ CloudFront Functions         | 🧠 Lambda@Edge                          |
| ------------------------------- | --------------------------------------- |
| Very lightweight and very fast  | More powerful, longer running           |
| Runs at edge locations          | Runs at regional edge caches            |
| Simple tasks                    | Complex tasks                           |
| Lower cost                      | Higher cost                             |

---

## 11.13 🌐 Custom Domain with Route 53

By default we get a URL like `d1234abcd.cloudfront.net`. We can use our own domain.

```text
👤 User opens  www.example.com
        ↓
🧭 Route 53  (Alias record → CloudFront distribution)
        ↓
🌍 CloudFront
        ↓
🪣 Origin
```

#### 🪜 Steps

```text
1. Request an ACM certificate in us-east-1 for www.example.com
2. In the distribution, add the Alternate Domain Name (CNAME): www.example.com
3. Attach the ACM certificate
4. In Route 53 → Create an A record (Alias) → target: the CloudFront distribution
5. ✅ Users open https://www.example.com
```

---

## 11.14 💰 Price Classes

CloudFront prices vary by **geographic area**. **Price Classes** let us choose which edge locations to use to save cost.

```text
💰 Price Classes
│
├── 🌍 Price Class All   → All edge locations (best performance)
├── 🌎 Price Class 200   → Most locations (excludes the most expensive)
└── 🌏 Price Class 100   → Only the cheapest regions (lowest cost)
```

> **Lower price class = Lower cost, but some users may get slightly slower delivery**

---

## 11.15 📊 Monitoring and Logging

```text
📊 CloudFront Monitoring
│
├── 📈 CloudWatch Metrics → Requests, BytesDownloaded, 4xx/5xx error rate
├── 📝 Standard Logs      → Detailed request logs sent to S3
├── ⚡ Real-time Logs     → Logs sent to Kinesis Data Streams
└── 🕵️ CloudTrail         → API actions on CloudFront
```

#### 💡 Tip

> Watch the **Cache Hit Ratio** to understand how well caching works.

---

## 11.16 🆚 CloudFront vs S3 Transfer Acceleration vs Global Accelerator

| Service                   | Main Use                                          | Caches Content? |
| ------------------------- | ------------------------------------------------- | --------------- |
| 🌍 **CloudFront**         | Fast delivery of **content** (download)           | ✅ Yes          |
| 🚀 **S3 Transfer Acceleration** | Faster **uploads** to S3 from far away      | ❌ No           |
| 🛰️ **Global Accelerator** | Fast and reliable network path to apps, static IPs| ❌ No           |

#### 🧠 Easy Memory

```text
🌍 CloudFront          = Cache content near users
🚀 Transfer Accel.     = Faster upload to S3
🛰️ Global Accelerator  = Better network path with fixed IP addresses
```

---

## 11.17 💰 CloudFront Pricing

```text
💰 CloudFront Cost
│
├── 📤 Data transfer out to viewers (per GB, varies by region)
├── 📨 Number of HTTP/HTTPS requests
├── 🔄 Invalidation requests (beyond free amount)
├── ⚡ CloudFront Functions / Lambda@Edge usage
└── 📝 Real-time logs and other add-ons
```

- 🎁 There is a **free tier** with monthly free data transfer and requests
- 📥 Data transfer **from AWS origins to CloudFront is free** (no AWS data-out charge for that part)

#### 💡 Cost Tips

- 📈 Increase the **cache hit ratio**
- 🗜️ Enable **compression**
- 💰 Pick a suitable **price class**

---

## 11.18 🏗 Real Example: S3 Static Website with CloudFront

### 🎯 Requirement

Host a fast, secure website at `https://www.example.com` using S3 and CloudFront.

### 🏗 Architecture

```text
👤 User
   │  https://www.example.com
   ▼
🧭 Route 53 (Alias → CloudFront)
   │
   ▼
🌍 CloudFront Distribution  (HTTPS, ACM certificate)
   │  (OAC)
   ▼
🪣 S3 Bucket (private) ── index.html, style.css, images/
```

### 🪜 Steps to Build It

```text
1. Create an S3 bucket and upload website files (keep it PRIVATE)
2. Request an ACM certificate in us-east-1 for www.example.com
3. Create a CloudFront distribution
     → Origin: the S3 bucket
     → Origin access: OAC (create new)
     → Viewer protocol policy: Redirect HTTP to HTTPS
     → Default root object: index.html
     → Alternate domain name: www.example.com
     → Custom SSL certificate: select the ACM certificate
4. Copy the generated bucket policy into the S3 bucket
5. In Route 53 → Create an A record (Alias) → target CloudFront distribution
6. Wait until the distribution status is Deployed
7. ✅ Open https://www.example.com
8. When files change → upload new files and create an invalidation (/*)
```

#### 🧠 Why Is This Better Than Using the S3 Website Endpoint?

```text
🪣 S3 website endpoint only    → HTTP only, single Region, public bucket needed
🌍 S3 + CloudFront             → HTTPS, global speed, private bucket, custom domain
```

---

## 📌🧠 CloudFront Quick Revision

```text
🌍 CloudFront
│
├── 📍 Infrastructure
│   ├── Edge Locations
│   └── Regional Edge Caches
│
├── 🧱 Concepts
│   ├── 📦 Distribution
│   ├── 🎯 Origin / Origin Group
│   ├── 🧭 Cache Behavior
│   ├── ⏱️ TTL
│   └── 🔄 Invalidation
│
├── 🎯 Origins
│   ├── S3 (with OAC)
│   ├── ALB / EC2
│   ├── API Gateway
│   └── Custom HTTP server
│
├── 🔒 Security
│   ├── HTTPS + ACM (us-east-1)
│   ├── Signed URLs / Cookies
│   ├── Geo Restriction
│   ├── WAF + Shield
│   └── OAC
│
├── ⚡ Edge Compute
│   ├── CloudFront Functions
│   └── Lambda@Edge
│
├── 💰 Cost
│   └── Price Classes
│
└── 🌐 Domain
    └── Route 53 Alias
```

---

## 🧠⚡ CloudFront One-Line Memory

| Concept                      | Easy Memory                                         |
| ---------------------------- | --------------------------------------------------- |
| 🌍 **CloudFront**            | AWS CDN — Cache Content Near Users                  |
| 📍 **Edge Location**         | Nearby Server That Delivers Cached Content          |
| 🏢 **Regional Edge Cache**   | Bigger Cache Between Edge and Origin                |
| 📦 **Distribution**          | Main CloudFront Setup (Gets a Domain Name)          |
| 🎯 **Origin**                | Where the Original Content Lives                    |
| 🛟 **Origin Group**          | Primary + Backup Origin                             |
| 🧭 **Cache Behavior**        | Rules for a URL Path                                |
| ✅ **Cache Hit**             | Found in Cache — Fast                               |
| ❌ **Cache Miss**            | Not in Cache — Go to Origin                         |
| ⏱️ **TTL**                   | How Long Content Stays in Cache                     |
| 🔄 **Invalidation**          | Force Removal of Cached Files                       |
| 🛡️ **OAC**                   | Private S3 Bucket Only CloudFront Can Read          |
| 🔑 **Signed URL**            | Temporary Access to Private Content                 |
| 🌐 **Geo Restriction**       | Allow or Block by Country                           |
| 🔒 **ACM Certificate**       | Must Be in us-east-1 for CloudFront                 |
| ⚡ **CloudFront Functions**  | Light and Fast Edge Code                            |
| 🧠 **Lambda@Edge**           | Powerful Edge Code                                  |

---

## 🗺 CloudFront Learning Map

```text
                         🌍 CloudFront
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
 DELIVERY NETWORK           SETUP                    SECURITY
      │                        │                        │
      ├── Edge Locations       ├── Distribution         ├── HTTPS (ACM)
      └── Regional Edge        ├── Origins              ├── OAC
          Cache                │    ├── S3              ├── Signed URL/Cookies
                               │    ├── ALB / EC2       ├── Geo Restriction
                               │    └── API Gateway     └── WAF / Shield
                               ├── Cache Behaviors
                               └── Origin Groups
      │
      ▼
   CACHING
      │
      ├── TTL
      ├── Cache Key / Policies
      └── Invalidation
      │
      ▼
  EDGE COMPUTE
      │
      ├── CloudFront Functions
      └── Lambda@Edge
      │
      ▼
 DOMAIN & COST
      │
      ├── Route 53 Alias
      └── Price Classes
```

---

## ⭐ CloudFront Final Memory

```text
CloudFront
 │
 ├── What is it?
 │      └── CDN (caches content at edge locations)
 │
 ├── What is the main setup called?
 │      └── Distribution
 │
 ├── Where does content come from?
 │      └── Origin (S3, ALB, EC2, API Gateway ...)
 │
 ├── How to keep S3 private but still serve it?
 │      └── OAC
 │
 ├── How long does content stay cached?
 │      └── TTL
 │
 ├── How to remove old content from cache?
 │      └── Invalidation (or use versioned file names)
 │
 ├── How to give private content to selected users?
 │      └── Signed URLs / Signed Cookies
 │
 ├── Where must the ACM certificate be created?
 │      └── us-east-1
 │
 └── How to use our own domain?
        └── Route 53 Alias record
```

---

# 🚪 PART 12 — API Gateway — Front Door for APIs

> **API Gateway = Secure front door that sends API requests to the right backend**

---

## 12.1 🚪 What is API Gateway?

> **API Gateway = Front door for our APIs**

Amazon API Gateway is a **fully managed service** to **create, publish, secure, monitor and manage APIs** at any scale.

It sits **between the client and our backend** and handles requests.

#### 🤔 What is an API?

> **API = Application Programming Interface**

An API is a way for one application to **talk to another application**, usually using **HTTP requests**.

```text
📱 Mobile App  ──► GET /products  ──►  🖥️ Backend  ──►  📦 List of products
```

#### 🏗 API Gateway Basic Architecture

```text
👥 Clients (Web, Mobile, Other Apps)
          │
          ▼
🚪 API Gateway
          │
   ┌──────┼───────────────┐
   ▼      ▼               ▼
⚡ Lambda  🖥️ EC2 / ALB    🔌 Other AWS Services
```

#### 🧠 Easy Memory

> **API Gateway = Secure front door that sends API requests to the right backend**

---

## 12.2 🤔 Why Do We Use API Gateway?

### ❌ Without API Gateway

```text
👥 Clients ──► Directly call backend servers

❌ We must build security, throttling, logging ourselves
❌ Backend is exposed
❌ Hard to manage versions and stages
```

### ✅ With API Gateway

```text
👥 Clients ──► 🚪 API Gateway ──► Backend

✅ Authentication and authorization
✅ Throttling (rate limits)
✅ Caching
✅ Monitoring and logging
✅ Versioning with stages
```

#### ⭐ Main Reasons

- ⚡ Build **serverless APIs** with Lambda quickly
- 🔒 Built-in **security** options
- 🚦 **Throttling** protects the backend from too many requests
- 💾 Optional **caching** for faster responses
- 📊 Built-in **monitoring** with CloudWatch
- 🔢 Manage **different versions and environments** (dev, test, prod)
- 📈 Scales automatically

---

## 12.3 🧰 What Does API Gateway Provide?

API Gateway provides:

- 🌐 REST APIs
- ⚡ HTTP APIs
- 🔌 WebSocket APIs
- 🔗 Integrations with backends
- 🔒 Authorization (IAM, Cognito, Lambda Authorizer)
- 🔑 API Keys and Usage Plans
- 🚦 Throttling
- 💾 Caching
- 🏷️ Stages and Deployments
- 🌍 Custom Domain Names
- 📊 Logging and Monitoring

---

## 12.4 🗂 Types of APIs

```text
🚪 API Gateway API Types
│
├── 🌐 REST API
├── ⚡ HTTP API
└── 🔌 WebSocket API
```

### 12.4.1 🌐 REST API

The **full-featured** option.

- ✅ Request/response validation and transformation
- ✅ API keys and usage plans
- ✅ Caching
- ✅ AWS WAF integration
- ✅ Private APIs (inside a VPC)
- 💰 Higher cost than HTTP API

> **REST API = Feature-rich API**

### 12.4.2 ⚡ HTTP API

A **simpler, cheaper and faster** option for many use cases.

- ✅ Lower cost
- ✅ Lower latency
- ✅ Good for **Lambda** and HTTP backends
- ✅ Supports JWT authorizers, CORS
- ❌ Fewer features than REST API (no API keys, no caching, etc.)

> **HTTP API = Simple, cheap, fast**

### 12.4.3 🔌 WebSocket API

Supports **two-way (real-time) communication** between client and server.

- 💬 Chat applications
- 📈 Live dashboards
- 🎮 Real-time games and notifications

```text
📱 Client ◄══════ persistent connection ══════► 🚪 API Gateway ──► ⚡ Lambda
```

> **WebSocket API = Real-time two-way communication**

### 12.4.4 📊 REST API vs HTTP API

| Feature              | 🌐 REST API                       | ⚡ HTTP API                    |
| -------------------- | --------------------------------- | ------------------------------ |
| Cost                 | Higher                            | Lower                          |
| Latency              | Normal                            | Lower                          |
| API Keys / Usage Plans | ✅ Yes                          | ❌ No                          |
| Caching              | ✅ Yes                            | ❌ No                          |
| Request Validation   | ✅ Yes                            | Limited                        |
| WAF Integration      | ✅ Yes                            | ❌ Not directly                |
| Private API (VPC)    | ✅ Yes                            | ❌ No (uses VPC Link for backends) |
| Best For             | Full control and many features    | Simple, fast, low-cost APIs    |

#### 🧠 Easy Memory

```text
🌐 REST API      = More features
⚡ HTTP API      = Cheaper and simpler
🔌 WebSocket API = Real-time
```

---

## 12.5 🧱 API Gateway Basic Concepts

```text
🚪 API Gateway
│
├── 📍 API               → The whole API
├── 📂 Resource          → A URL path (/products)
├── 🔧 Method            → HTTP action (GET, POST ...)
├── 🔗 Integration       → Where the request goes (Lambda, HTTP ...)
├── 🏷️ Stage             → Environment (dev, test, prod)
└── 🚀 Deployment        → A published snapshot of the API
```

### 12.5.1 📖 Simple Definitions

| Concept          | Simple Meaning                                                    |
| ---------------- | ----------------------------------------------------------------- |
| 📍 API           | The collection of resources and methods                           |
| 📂 Resource      | A path in the URL, like `/products` or `/products/{id}`           |
| 🔧 Method        | The HTTP action on a resource: GET, POST, PUT, DELETE             |
| 🔗 Integration   | The backend that handles the request                              |
| 🏷️ Stage         | A named version/environment of a deployed API (`dev`, `prod`)     |
| 🚀 Deployment    | Publishing the API to a stage so clients can use it               |
| 🌐 Invoke URL    | The URL clients call                                              |

### 12.5.2 🔧 HTTP Methods

| Method   | Action              | Example                    |
| -------- | ------------------- | -------------------------- |
| `GET`    | Read data           | `GET /products`            |
| `POST`   | Create data         | `POST /products`           |
| `PUT`    | Update data         | `PUT /products/101`        |
| `DELETE` | Delete data         | `DELETE /products/101`     |

### 12.5.3 🌐 Invoke URL Format

```text
https://{api-id}.execute-api.{region}.amazonaws.com/{stage}/{resource}

Example:
https://abc123xyz.execute-api.ap-south-1.amazonaws.com/prod/products
```

#### ⚠ Important

> **After changing a REST API, we must DEPLOY it to a stage.** Changes are not live until deployed.

---

## 12.6 🔗 Integration Types

An **Integration** decides **what handles the request** behind API Gateway.

```text
🔗 Integrations
│
├── ⚡ Lambda Function      → Most common (serverless)
├── 🌐 HTTP Endpoint        → Any public HTTP backend
├── 🔌 AWS Service          → DynamoDB, SQS, SNS, S3 ... directly
├── 🔒 VPC Link             → Private resources (ALB/NLB) inside a VPC
└── 🎭 Mock                 → Fixed response without a backend (for testing)
```

### 12.6.1 ⚡ Lambda Integration

```text
👥 Client ──► 🚪 API Gateway ──► ⚡ Lambda ──► 🗄️ DynamoDB / RDS
```

#### 🧬 Proxy vs Non-Proxy

| 🔄 Proxy Integration (Lambda Proxy)             | 🔧 Non-Proxy (Custom) Integration           |
| ----------------------------------------------- | ------------------------------------------- |
| API Gateway passes the **whole request** to Lambda | We **map and transform** request/response |
| Lambda returns the full response format         | More control, more configuration            |
| **Simple and most used**                        | Used when transformation is needed          |

#### 💻 Lambda Proxy Response Format

```python
import json

def lambda_handler(event, context):
    return {
        "statusCode": 200,
        "headers": {"Content-Type": "application/json"},
        "body": json.dumps({"message": "Hello from API Gateway + Lambda"})
    }
```

#### 📖 Understanding It

```text
event       → Contains method, path, headers, query string, body
statusCode  → HTTP status code returned to the client
body        → Response content (must be a string)
```

### 12.6.2 🔒 VPC Link

A **VPC Link** lets API Gateway reach **private resources** (like an internal Application Load Balancer or NLB) inside our VPC.

```text
🚪 API Gateway ──(VPC Link)──► ⚖️ Internal Load Balancer ──► 🖥️ Private EC2
```

---

## 12.7 🔒 API Security

```text
🔐 API Gateway Security
│
├── 🔑 Authentication / Authorization
│   ├── 🎭 IAM Authorization (SigV4)
│   ├── 👤 Amazon Cognito User Pools
│   ├── ⚡ Lambda Authorizer (Custom)
│   └── 🪪 JWT Authorizer (HTTP API)
│
├── 🔑 API Keys + Usage Plans    → Identify and limit clients
├── 📜 Resource Policy           → Allow/deny by IP, VPC, account
├── 🛡️ AWS WAF                   → Protect from web attacks
└── 🔒 HTTPS (TLS)               → Encryption in transit
```

### 12.7.1 🎭 IAM Authorization

- Callers must **sign requests** using AWS credentials (Signature V4)
- Good for **AWS services and internal applications**

### 12.7.2 👤 Cognito User Pool Authorizer

- Users sign in with **Amazon Cognito**
- Client sends the **token** with the request
- API Gateway checks the token
- Good for **web and mobile app users**

### 12.7.3 ⚡ Lambda Authorizer (Custom Authorizer)

- Our own **Lambda function** checks the token or headers
- It returns an **IAM policy** (allow or deny)
- Good for **custom authentication** (third-party tokens, custom logic)

```text
👥 Client (sends token)
     │
     ▼
🚪 API Gateway ──► ⚡ Lambda Authorizer ──► ✅ Allow / ❌ Deny
     │ (if allowed)
     ▼
⚡ Backend Lambda
```

### 12.7.4 🔑 API Keys and Usage Plans

- **API Key** = a string given to a client to identify it
- **Usage Plan** = sets **throttling limits** and **quotas** for API keys

```text
🔑 Client A (Free plan)    → 100 requests/day
🔑 Client B (Premium plan) → 10,000 requests/day
```

#### ⚠ Important

> **API Keys are NOT a strong security method by themselves.** They identify clients and apply limits. Use IAM, Cognito or a Lambda Authorizer for real authorization.

### 12.7.5 🔒 Summary

| Method              | Best For                               |
| ------------------- | -------------------------------------- |
| 🎭 IAM              | AWS users, roles, internal services    |
| 👤 Cognito          | Mobile and web app users               |
| ⚡ Lambda Authorizer| Custom or third-party authentication   |
| 🔑 API Key          | Identify clients and apply usage limits|
| 📜 Resource Policy  | Restrict by IP / VPC / account         |

---

## 12.8 🚦 Throttling

**Throttling** limits the **number of requests** so the backend is protected.

```text
👥 Too many requests
        ↓
🚦 API Gateway throttles
        ↓
❌ Extra requests get  HTTP 429 (Too Many Requests)
```

#### 🧱 Throttling Levels

```text
🚦 Throttling Levels
│
├── 🌍 Account-level limit (per Region)
├── 🏷️ Stage / Method level limits
└── 🔑 Client level (Usage Plans)
```

#### ⭐ Key Points

- ⚡ **Rate** = requests per second (steady)
- 💥 **Burst** = short spike capacity
- 🚦 Exceeding the limit returns **429 Too Many Requests**
- 💡 Default account limits exist and can be increased by request

---

## 12.9 💾 Caching

API Gateway (REST API) can **cache responses** for a time.

```text
👥 Client ──► 🚪 API Gateway
                  │
        ┌─────────┴─────────┐
        ▼                   ▼
   💾 Cache HIT         ❌ Cache MISS
   (Return fast)        (Call backend, store response)
```

#### ⭐ Key Points

- ⏱️ Default **TTL = 300 seconds (5 minutes)**
- ⚡ Faster response and **lower backend load**
- 💰 Cache is a **paid feature** (we pay by cache size per hour)
- 🏷️ Cache is enabled **per stage**

> **Caching = Store responses to reply faster**

---

## 12.10 🏷 Stages and Deployments

A **Stage** is a **named environment** of our API.

```text
🚪 My API
│
├── 🏷️ dev   → https://.../dev/...
├── 🏷️ test  → https://.../test/...
└── 🏷️ prod  → https://.../prod/...
```

#### ⭐ Key Points

- 🚀 Each deployment can be released to a stage
- 🔢 **Stage Variables** = settings that change per stage (like Lambda alias or backend URL)
- 🔙 Easy rollback to a previous deployment
- 🐤 **Canary release** — send a small % of traffic to a new deployment first
- 📊 Each stage can have its own **logging, throttling and caching**

#### 💻 Stage Variable Example

```text
Lambda function:  my-function:${stageVariables.lambdaAlias}

dev  stage → lambdaAlias = DEV
prod stage → lambdaAlias = PROD
```

---

## 12.11 🌍 Endpoint Types and Custom Domain

### 12.11.1 🌍 API Endpoint Types (REST API)

```text
🌍 Endpoint Types
│
├── 🌐 Edge-Optimized  → Requests go through CloudFront edge locations (global users)
├── 🌏 Regional        → Clients in the same Region (we can add our own CloudFront)
└── 🔒 Private         → Only inside a VPC (via interface VPC endpoint)
```

| Type              | Best For                                         |
| ----------------- | ------------------------------------------------ |
| 🌐 Edge-Optimized | Users spread across the world                    |
| 🌏 Regional       | Users in one Region, or when using own CloudFront|
| 🔒 Private        | Internal APIs inside a VPC                       |

### 12.11.2 🏷 Custom Domain Name

Instead of the default URL, we can use our own domain.

```text
❌ https://abc123xyz.execute-api.ap-south-1.amazonaws.com/prod/products
✅ https://api.example.com/products
```

#### 🪜 Steps

```text
1. Get an SSL/TLS certificate from AWS Certificate Manager (ACM)
2. Create a Custom Domain Name in API Gateway
3. Map the domain to our API and stage
4. In Route 53 → Create an Alias record pointing to the API Gateway domain
5. ✅ Clients use https://api.example.com
```

---

## 12.12 🌐 CORS

**CORS = Cross-Origin Resource Sharing**

A browser **blocks** a web page from calling an API on a **different domain** unless the API allows it.

```text
🌐 Website: https://www.example.com
        │ calls
        ▼
🚪 API: https://api.example.com    ← must allow origin www.example.com
```

#### ⭐ Key Points

- ✅ We must **enable CORS** in API Gateway when a browser app calls our API from another domain
- 🔧 CORS sends special headers like `Access-Control-Allow-Origin`
- ⚠️ With Lambda proxy integration, our **Lambda code must also return the CORS headers**

---

## 12.13 📊 Monitoring and Logging

```text
📊 API Gateway Monitoring
│
├── 📈 CloudWatch Metrics → Count, Latency, 4XXError, 5XXError
├── 📝 CloudWatch Logs    → Access logs and execution logs
├── 🔍 AWS X-Ray          → Trace requests through services
└── 🕵️ CloudTrail         → API Gateway management actions
```

| Metric           | Meaning                                     |
| ---------------- | ------------------------------------------- |
| `Count`          | Total number of API calls                   |
| `Latency`        | Total time from request to response         |
| `IntegrationLatency` | Time taken by the backend               |
| `4XXError`       | Client-side errors (bad request, unauthorized) |
| `5XXError`       | Server-side errors                          |

---

## 12.14 ⏱ Important Limits and Facts

| Item                       | Fact                                                |
| -------------------------- | --------------------------------------------------- |
| ⏱️ Integration Timeout     | Default maximum of **29 seconds** for REST APIs     |
| 📏 Payload Size            | About **10 MB** request payload                     |
| 🚦 Throttling              | Account-level default limits (can be increased)     |
| 💾 Cache TTL               | Default 300 seconds                                 |
| 🔢 Status Code             | `429` when throttled                                |

#### ⚠ Important

> **API Gateway waits only a short time (about 29 seconds by default) for the backend.** For long tasks, accept the request and process in the background (use **SQS, Step Functions or async Lambda**).

> 💡 Limits can change. Check AWS documentation for current values.

---

## 12.15 💰 API Gateway Pricing

```text
💰 API Gateway Cost
│
├── 📨 Number of API calls (per million requests)
├── 📦 Data transfer out
├── 💾 Cache size (if caching is enabled)
└── 🔌 WebSocket connection minutes and messages
```

- 🎁 There is a **free tier** for new accounts
- ⚡ **HTTP APIs** are cheaper than **REST APIs**

---

## 12.16 🏗 Real Example: Serverless REST API

### 🎯 Requirement

Build a simple **Products API** without managing any server.

### 🏗 Architecture

```text
📱 Client App
     │ GET/POST /products
     ▼
🚪 API Gateway (Stage: prod)
     │ (Authorizer: Cognito)
     ▼
⚡ Lambda Function
     │
     ▼
🗄️ DynamoDB Table: Products
```

### 🪜 Steps to Build It

```text
1. Create a DynamoDB table: Products (partition key: productId)
2. Create a Lambda function with an execution role (access to the table)
3. Open API Gateway → Create API → HTTP API (or REST API)
4. Add routes:  GET /products   and   POST /products
5. Integrate each route with the Lambda function
6. (Optional) Add an authorizer (Cognito / JWT / Lambda)
7. Deploy to a stage (like prod) — HTTP API can use auto-deploy
8. Test with the Invoke URL:  curl https://<api-id>.execute-api.<region>.amazonaws.com/prod/products ✅
9. (Optional) Add a custom domain with Route 53 + ACM
```

### 🌍 Full Serverless Flow

```text
👤 User
   │
   ▼
🧭 Route 53 (api.example.com)
   │
   ▼
🚪 API Gateway
   │
   ▼
⚡ Lambda
   │
   ▼
🗄️ DynamoDB
   │
   ▼
📊 CloudWatch (logs and metrics)
```

---

## 📌🧠 API Gateway Quick Revision

```text
🚪 API Gateway
│
├── 🗂️ API Types
│   ├── 🌐 REST API
│   ├── ⚡ HTTP API
│   └── 🔌 WebSocket API
│
├── 🧱 Concepts
│   ├── Resource
│   ├── Method
│   ├── Integration
│   ├── Stage
│   └── Deployment
│
├── 🔗 Integrations
│   ├── Lambda (Proxy / Non-proxy)
│   ├── HTTP Endpoint
│   ├── AWS Services
│   ├── VPC Link
│   └── Mock
│
├── 🔒 Security
│   ├── IAM
│   ├── Cognito
│   ├── Lambda Authorizer
│   ├── API Keys + Usage Plans
│   ├── Resource Policy
│   └── WAF
│
├── ⚡ Performance
│   ├── Throttling (429)
│   └── Caching (TTL 300s)
│
├── 🌍 Endpoint Types
│   ├── Edge-Optimized
│   ├── Regional
│   └── Private
│
└── 📊 Monitoring
    ├── CloudWatch
    └── X-Ray
```

---

## 🧠⚡ API Gateway One-Line Memory

| Concept                      | Easy Memory                                       |
| ---------------------------- | ------------------------------------------------- |
| 🚪 **API Gateway**           | Secure Front Door for APIs                        |
| 🌐 **REST API**              | Feature-rich API                                  |
| ⚡ **HTTP API**              | Cheaper, Simpler, Faster                          |
| 🔌 **WebSocket API**         | Real-time Two-way Communication                   |
| 📂 **Resource**              | URL Path (/products)                              |
| 🔧 **Method**                | HTTP Action (GET, POST ...)                       |
| 🔗 **Integration**           | Backend That Handles the Request                  |
| 🏷️ **Stage**                 | Environment of the API (dev, prod)                |
| 🚀 **Deployment**            | Publish API Changes to a Stage                    |
| 🎭 **IAM Auth**              | For AWS Users and Services                        |
| 👤 **Cognito Authorizer**    | For App Users                                     |
| ⚡ **Lambda Authorizer**     | Custom Authentication Logic                       |
| 🔑 **API Key**               | Identify Client and Apply Limits (Not Strong Security) |
| 🚦 **Throttling**            | Limit Requests, Returns 429                       |
| 💾 **Caching**               | Store Responses (Default TTL 5 min)               |
| 🌐 **CORS**                  | Allow Browser Calls From Other Domains            |
| 🔒 **VPC Link**              | Reach Private Resources in a VPC                  |

---

## 🗺 API Gateway Learning Map

```text
                        🚪 API Gateway
                              │
      ┌───────────────────────┼───────────────────────┐
      │                       │                       │
      ▼                       ▼                       ▼
   API TYPES               REQUEST FLOW             SECURITY
      │                       │                       │
      ├── REST API            ├── Resource            ├── IAM
      ├── HTTP API            ├── Method              ├── Cognito
      └── WebSocket API       ├── Integration         ├── Lambda Authorizer
                              │    ├── Lambda         ├── API Keys
                              │    ├── HTTP           ├── Resource Policy
                              │    ├── AWS Service    └── WAF
                              │    └── VPC Link
                              └── Stage / Deployment
      │
      ▼
  PERFORMANCE
      │
      ├── Throttling
      └── Caching
      │
      ▼
  DOMAIN & NETWORK
      │
      ├── Edge / Regional / Private
      ├── Custom Domain (Route 53 + ACM)
      └── CORS
      │
      ▼
  MONITORING
      │
      ├── CloudWatch
      └── X-Ray
```

---

## ⭐ API Gateway Final Memory

```text
API Gateway
 │
 ├── What is it?
 │      └── Front door for APIs
 │
 ├── Which API type is cheapest and simplest?
 │      └── HTTP API
 │
 ├── Which API type for real-time chat?
 │      └── WebSocket API
 │
 ├── Most common backend?
 │      └── Lambda
 │
 ├── How to protect app users' access?
 │      └── Cognito Authorizer
 │
 ├── How to do custom authentication?
 │      └── Lambda Authorizer
 │
 ├── How to limit requests?
 │      └── Throttling / Usage Plans
 │
 ├── How to make responses faster?
 │      └── Caching
 │
 ├── Why do changes not appear?
 │      └── We forgot to Deploy to the stage
 │
 └── Why does the browser block my API call?
        └── CORS not enabled
```

---

# 📬 PART 13 — SQS — Simple Queue Service

> **SQS = A waiting line (queue) for messages between applications**

---

## 13.1 📬 What is SQS?

> **SQS = Simple Queue Service**

Amazon SQS is a **fully managed message queue service**.

A **queue** stores **messages** until another application is ready to process them.

It helps different parts of an application **talk to each other without depending on each other**.

#### 📦 SQS Is Used To

- 🔗 **Decouple** (separate) application parts
- 📥 Store tasks until they can be processed
- 🛡️ Protect a slow backend from sudden traffic
- ⚙️ Run background jobs

#### 🏗 SQS Basic Architecture

```text
📤 Producer                📬 SQS Queue               📥 Consumer
(Sends messages)     ──►   (Stores messages)    ──►   (Processes messages)
```

#### 🏠 Simple Example

```text
🍕 Restaurant

👤 Customer places order  → 🧾 Order slip goes on the rack   → 👨‍🍳 Chef takes slips one by one

Producer  = Customer / Waiter
Queue     = Order rack
Consumer  = Chef
```

#### 🧠 Easy Memory

> **SQS = A waiting line (queue) for messages between applications**

---

## 13.2 🤔 Why Do We Use SQS?

### ❌ Without a Queue (Tightly Coupled)

```text
🌐 Web Server ───directly calls───► ⚙️ Processing Server

If the Processing Server is slow or down:
❌ Web Server waits or fails
❌ Orders can be lost
```

### ✅ With SQS (Loosely Coupled)

```text
🌐 Web Server ──► 📬 SQS Queue ──► ⚙️ Processing Server

✅ Web Server just sends the message and continues
✅ Messages wait safely in the queue
✅ Processing Server works at its own speed
```

#### ⭐ Main Reasons

- 🔗 **Decoupling** — services work independently
- 🛡️ **Buffering** — handles traffic spikes smoothly
- 🔁 **Reliability** — messages are stored safely until processed
- 📈 **Scalability** — add more consumers when the queue grows
- ❌ No servers or software to manage

---

## 13.3 🧰 What Does SQS Provide?

SQS provides:

- 📬 Standard Queues
- 🔢 FIFO Queues
- ⏱️ Visibility Timeout
- 🗓️ Message Retention
- ⏳ Delay Queues
- 📡 Long Polling
- ☠️ Dead-Letter Queues
- 🔒 Encryption
- 🔐 Access Policies
- 📊 CloudWatch Monitoring

---

## 13.4 🧱 SQS Basic Concepts

```text
📬 SQS
│
├── 📤 Producer      → Sends messages to the queue
├── 📬 Queue         → Stores messages
├── 📥 Consumer      → Reads and processes messages
└── 🧾 Message       → The data being sent
```

### 13.4.1 📖 Simple Definitions

| Concept        | Simple Meaning                                               |
| -------------- | ------------------------------------------------------------ |
| 📤 Producer    | The application that **sends** messages                      |
| 📥 Consumer    | The application that **receives and processes** messages     |
| 📬 Queue       | The place where messages wait                                |
| 🧾 Message     | A piece of data (text, JSON, etc.)                           |
| 🔑 Receipt Handle | An ID given when a message is received, used to delete it |
| 🏷️ Message Attributes | Extra metadata sent with a message                    |

### 13.4.2 ⭐ Important Facts

- 🔄 SQS is a **pull-based** service — consumers **ask (poll)** the queue for messages
- 🌏 A queue belongs to **one Region**
- 🧾 A message can contain text such as JSON, XML or plain text
- 📏 Message size is limited (**256 KB** in older documentation; AWS has since increased it to **1 MiB** — check current docs)
- 🗑️ **The consumer must delete the message** after processing, otherwise it will come back

#### 🧠 Remember

> **SQS = Pull model. Consumers poll the queue.**

---

## 13.5 🗂 Types of SQS Queues

```text
📬 SQS Queue Types
│
├── 📬 Standard Queue
└── 🔢 FIFO Queue
```

### 13.5.1 📬 Standard Queue

The **default** queue type.

#### ⭐ Features

- 🚀 **Almost unlimited throughput** (very high number of messages per second)
- 📨 **At-least-once delivery** — a message is delivered at least once, but **sometimes more than once** (duplicates possible)
- 🔀 **Best-effort ordering** — messages may arrive in a different order

```text
Sent:      1 → 2 → 3 → 4
Received:  1 → 3 → 2 → 4   (order may change)
```

#### ✅ Use When

- High throughput is needed
- Order is not important
- The application can handle duplicate messages (idempotent processing)

> **Standard = Very fast, may have duplicates, order not guaranteed**

---

### 13.5.2 🔢 FIFO Queue

**FIFO = First-In, First-Out**

#### ⭐ Features

- 🔢 **Order is preserved** (first message sent is first message received)
- 1️⃣ **Exactly-once processing** — no duplicates (duplicates are removed)
- 🏷️ Queue name must **end with `.fifo`** (example: `orders.fifo`)
- 📉 Lower throughput than Standard (higher limits are possible with batching and high-throughput mode)

```text
Sent:      1 → 2 → 3 → 4
Received:  1 → 2 → 3 → 4   (same order)
```

#### 🧩 FIFO Terms

| Term                       | Meaning                                                    |
| -------------------------- | ---------------------------------------------------------- |
| 🏷️ Message Group ID        | Messages in the same group are processed **in order**      |
| 🔑 Message Deduplication ID| Used to avoid duplicate messages (within a 5-minute window)|

#### ✅ Use When

- Order is very important (bank transactions, order updates)
- Duplicates are not acceptable

> **FIFO = Strict order, no duplicates, lower throughput**

---

### 13.5.3 📊 Standard vs FIFO

| 📬 Standard Queue                  | 🔢 FIFO Queue                           |
| ---------------------------------- | --------------------------------------- |
| Almost unlimited throughput        | Limited throughput (higher with batching/high-throughput mode) |
| At-least-once delivery             | Exactly-once processing                 |
| Best-effort ordering               | Strict ordering                         |
| Duplicates possible                | No duplicates                           |
| Any queue name                     | Name must end with `.fifo`              |
| Best for speed and scale           | Best for order and accuracy             |

#### 🧠 Easy Memory

```text
📬 Standard = Fast, may repeat, order not fixed
🔢 FIFO     = Ordered, no repeat
```

---

## 13.6 🔄 Message Lifecycle

```text
1. 📤 Producer sends a message to the queue
          ↓
2. 📬 Message is stored in the queue (redundantly across AZs)
          ↓
3. 📥 Consumer polls the queue and receives the message
          ↓
4. ⏱️ Message becomes invisible (Visibility Timeout starts)
          ↓
5. ⚙️ Consumer processes the message
          ↓
6. 🗑️ Consumer deletes the message from the queue
          ↓
7. ✅ Done
```

#### ⚠ Important

> **If the consumer does not delete the message before the Visibility Timeout ends, the message becomes visible again and can be processed again.**

---

## 13.7 ⏱ Visibility Timeout

When a consumer **receives** a message, SQS **hides** it from other consumers for a time. This time is the **Visibility Timeout**.

#### 🏗 How It Works

```text
📬 Queue: [Message A]
        │
        ▼
📥 Consumer 1 receives Message A
        │
        ▼
🙈 Message A is hidden (Visibility Timeout = 30 seconds)
        │
        ├── ✅ Consumer 1 finishes and deletes it → Gone forever
        │
        └── ❌ Consumer 1 crashes (no delete)
                    ↓
            👀 After 30 seconds → Message A visible again
                    ↓
            📥 Another consumer can process it
```

#### ⭐ Key Points

- ⏱️ **Default: 30 seconds**
- 📏 Range: **0 seconds to 12 hours**
- 🔧 Set it **longer than the time our consumer needs** to process one message
- ⏳ A consumer can **extend** the timeout while still processing

#### 🧠 Simple Meaning

> **Visibility Timeout = Time during which a received message is hidden from others**

---

## 13.8 🗓 Message Retention

How long SQS **keeps a message** if it is not deleted.

- 🗓️ **Default: 4 days**
- 📏 Range: **1 minute to 14 days**

After the retention period, SQS **deletes the message automatically**.

---

## 13.9 ⏳ Delay Queue

A **Delay Queue** hides new messages from consumers for some time after they are sent.

```text
📤 Message sent
        ↓
⏳ Delay (example: 60 seconds)  → Not visible yet
        ↓
👀 Message becomes visible
        ↓
📥 Consumer can receive it
```

- ⏱️ Delay range: **0 seconds to 15 minutes**
- 🎯 Used when we want to process a message **a little later**
- 💡 We can also delay **individual messages** (message timer) in Standard queues

---

## 13.10 📡 Short Polling vs Long Polling

Consumers **poll** (ask) the queue for messages.

### 13.10.1 ⚡ Short Polling

- Returns **immediately**, even if the queue is empty
- Checks only a **subset** of SQS servers, so it may return empty results even when messages exist
- ❌ More empty responses = more API calls = more cost

### 13.10.2 📡 Long Polling

- Waits for messages to arrive (up to **20 seconds**) before returning
- Checks **all** SQS servers
- ✅ Fewer empty responses
- ✅ **Lower cost**
- ✅ **Recommended** in most cases

#### ⚙ How to Enable

```text
ReceiveMessageWaitTimeSeconds = 1 to 20   (on the queue)
or
WaitTimeSeconds = 1 to 20                 (in the ReceiveMessage call)
```

#### 📊 Comparison

| ⚡ Short Polling                | 📡 Long Polling                    |
| ------------------------------- | ---------------------------------- |
| Returns immediately             | Waits up to 20 seconds             |
| Many empty responses            | Fewer empty responses              |
| Higher cost                     | Lower cost                         |
| Wait time = 0                   | Wait time = 1 to 20 seconds        |

#### 🧠 Remember

> **Use Long Polling to reduce cost and empty responses.**

---

## 13.11 ☠ Dead-Letter Queue (DLQ)

A **Dead-Letter Queue** is a **separate queue** where SQS sends messages that **fail processing again and again**.

#### 🏗 How It Works

```text
📬 Main Queue
      │
      ▼
📥 Consumer tries to process
      │
   ❌ Fails (message returns to the queue)
      │
   ❌ Fails again ... (count reaches maxReceiveCount)
      │
      ▼
☠️ Dead-Letter Queue  (message is moved here)
```

#### ⭐ Key Points

- 🔢 **maxReceiveCount** = how many times a message can be received before it moves to the DLQ
- 🔍 We can inspect DLQ messages to find the bug
- 🏷️ A FIFO queue needs a FIFO DLQ, and a Standard queue needs a Standard DLQ
- ⏳ Set DLQ **retention longer** than the main queue

#### 🧠 Simple Meaning

> **DLQ = Parking place for messages that keep failing**

---

## 13.12 🔒 SQS Security

```text
🔐 SQS Security
│
├── 🔐 Access Control
│   ├── 📜 IAM Policy          → What an identity can do with the queue
│   └── 📬 Queue Access Policy → Who can use this queue (also cross-account)
│
├── 🔒 Encryption at Rest
│   ├── 🔑 SSE-SQS (SQS-managed keys)
│   └── 🔐 SSE-KMS (KMS keys)
│
└── 🌐 Encryption in Transit → HTTPS
```

#### 💻 Example: Queue Policy Allowing SNS to Send Messages

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "Service": "sns.amazonaws.com" },
      "Action": "sqs:SendMessage",
      "Resource": "arn:aws:sqs:ap-south-1:123456789012:my-queue",
      "Condition": {
        "ArnEquals": { "aws:SourceArn": "arn:aws:sns:ap-south-1:123456789012:my-topic" }
      }
    }
  ]
}
```

#### ⭐ Key Points

- 🔒 Server-side encryption protects stored messages
- 🌐 For private access from a VPC, use a **VPC Interface Endpoint** for SQS

---

## 13.13 💻 SQS Commands and Code

### 13.13.1 ⌨ AWS CLI Examples

```bash
# Create a queue
aws sqs create-queue --queue-name my-queue

# Send a message
aws sqs send-message \
  --queue-url https://sqs.ap-south-1.amazonaws.com/123456789012/my-queue \
  --message-body "Order #1001 received"

# Receive messages (long polling)
aws sqs receive-message \
  --queue-url https://sqs.ap-south-1.amazonaws.com/123456789012/my-queue \
  --wait-time-seconds 20 \
  --max-number-of-messages 10

# Delete a message after processing
aws sqs delete-message \
  --queue-url https://sqs.ap-south-1.amazonaws.com/123456789012/my-queue \
  --receipt-handle "<receipt-handle>"
```

### 13.13.2 🐍 Python (boto3) Example

```python
import boto3

sqs = boto3.client("sqs", region_name="ap-south-1")
queue_url = "https://sqs.ap-south-1.amazonaws.com/123456789012/my-queue"

# Send a message
sqs.send_message(QueueUrl=queue_url, MessageBody="Order #1001 received")

# Receive and process messages
response = sqs.receive_message(
    QueueUrl=queue_url,
    MaxNumberOfMessages=10,
    WaitTimeSeconds=20,
)

for msg in response.get("Messages", []):
    print("Processing:", msg["Body"])
    # ... do the work here ...
    sqs.delete_message(QueueUrl=queue_url, ReceiptHandle=msg["ReceiptHandle"])
```

#### 📖 Understanding It

```text
send_message     → Producer puts a message in the queue
receive_message  → Consumer pulls messages (long polling = WaitTimeSeconds 20)
delete_message   → Consumer removes the message after successful processing
```

---

## 13.14 📦 Batch Operations

SQS lets us **send, receive and delete up to 10 messages in one call**.

- ✅ Fewer API calls
- 💰 Lower cost
- 🚀 Better performance

---

## 13.15 ⚡ SQS with Lambda

Lambda can **read messages from SQS automatically** (Event Source Mapping).

```text
📬 SQS Queue ──(Lambda polls the queue)──► ⚡ Lambda (batch of messages)
```

#### ⭐ Key Points

- 📦 Lambda receives messages in **batches**
- ✅ If the function succeeds, Lambda **deletes the messages**
- ❌ If the function fails, messages return to the queue after the Visibility Timeout
- ⏱️ Set the queue **Visibility Timeout longer than the Lambda timeout** (AWS recommends at least 6 times the function timeout)
- ☠️ Use a **DLQ** on the SQS queue for failed messages

---

## 13.16 📈 SQS with Auto Scaling

We can scale consumers based on **queue length**.

```text
📬 Queue grows (many messages waiting)
        ↓
📊 CloudWatch Metric: ApproximateNumberOfMessagesVisible
        ↓
🚨 Alarm triggers
        ↓
📈 Auto Scaling adds more consumer EC2 instances
        ↓
📉 Queue shrinks → instances are removed
```

#### 💡 Tip

> A better metric is **backlog per instance** (queue length ÷ number of running instances).

---

## 13.17 🆚 SQS vs SNS

| 📬 SQS                              | 📢 SNS                                 |
| ----------------------------------- | -------------------------------------- |
| **Queue** (message storage)         | **Pub/Sub** (message broadcast)        |
| **Pull** — consumers poll           | **Push** — SNS sends to subscribers    |
| One message is processed by **one consumer** | One message goes to **many subscribers** |
| Messages are **stored** until deleted | Messages are **not stored** (delivered immediately) |
| Used for decoupling and buffering   | Used for notifications and fan-out     |

#### 🧠 Easy Memory

```text
📬 SQS = Mailbox (messages wait for pickup)
📢 SNS = Loudspeaker (message is announced to everyone)
```

---

## 13.18 💰 SQS Pricing

```text
💰 SQS Cost
│
├── 📨 Number of requests (send, receive, delete ...)
├── 📦 Large messages (billed as multiple requests)
└── 🌐 Data transfer out
```

- 🎁 SQS has a **free tier** (a number of requests per month)
- 💡 Use **batching** and **long polling** to reduce cost

---

## 13.19 🏗 Real Example: Order Processing System

### 🎯 Requirement

An online shop should **accept orders quickly**, even during a sale when thousands of orders come at the same time. The orders should be processed safely in the background.

### 🏗 Architecture

```text
👥 Customers
     │
     ▼
🌐 Web / API Server
     │ send order message
     ▼
📬 SQS Queue (orders-queue) ───► ☠️ DLQ (orders-dlq)
     │
     ▼
⚙️ Worker Servers (Auto Scaling) or ⚡ Lambda
     │
     ▼
🗄️ Database (RDS / DynamoDB)
```

### 🪜 Steps to Build It

```text
1. Create SQS queue: orders-queue
2. Create DLQ: orders-dlq and attach it (maxReceiveCount = 3)
3. Set Long Polling (20 seconds) and Visibility Timeout
4. Web server sends each new order as a message
5. Workers (or Lambda) read messages, process orders and delete them
6. Create CloudWatch alarm on queue length to scale workers
7. ✅ Orders are never lost, even if workers are slow
```

#### ✅ Benefits

```text
🛡️ Web server stays fast during traffic spikes
🔁 Failed orders are retried automatically
☠️ Bad messages go to DLQ for checking
📈 Workers scale with the queue size
```

---

## 📌🧠 SQS Quick Revision

```text
📬 SQS
│
├── 🧱 Basics
│   ├── 📤 Producer
│   ├── 📬 Queue
│   ├── 📥 Consumer
│   └── 🧾 Message
│
├── 🗂️ Queue Types
│   ├── 📬 Standard
│   └── 🔢 FIFO
│
├── ⚙️ Settings
│   ├── ⏱️ Visibility Timeout
│   ├── 🗓️ Retention
│   ├── ⏳ Delay Queue
│   └── 📡 Long Polling
│
├── ☠️ Failure Handling
│   └── Dead-Letter Queue
│
├── 🔒 Security
│   ├── IAM Policy / Queue Policy
│   └── SSE-SQS / SSE-KMS
│
└── 🔗 Integrations
    ├── ⚡ Lambda
    ├── 📈 Auto Scaling
    └── 📢 SNS Fan-out
```

---

## 🧠⚡ SQS One-Line Memory

| Concept                    | Easy Memory                                      |
| -------------------------- | ------------------------------------------------ |
| 📬 **SQS**                 | Message Queue Service                            |
| 📤 **Producer**            | Sends Messages                                   |
| 📥 **Consumer**            | Receives and Processes Messages                  |
| 📬 **Standard Queue**      | Fast, At-least-once, Order Not Fixed             |
| 🔢 **FIFO Queue**          | Ordered, Exactly-once, Name Ends with .fifo      |
| ⏱️ **Visibility Timeout**  | Time a Received Message Stays Hidden (Default 30s)|
| 🗓️ **Retention**           | How Long Messages Are Kept (Default 4 Days, Max 14)|
| ⏳ **Delay Queue**         | Hide New Messages for 0 to 15 Minutes            |
| 📡 **Long Polling**        | Wait Up to 20 Seconds, Saves Cost                |
| ☠️ **Dead-Letter Queue**   | Parking Place for Failed Messages                |
| 🔄 **Pull Model**          | Consumers Ask the Queue for Messages             |
| 🗑️ **Delete Message**      | Consumer Must Delete After Processing            |

---

## 🗺 SQS Learning Map

```text
                           📬 Amazon SQS
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
        ▼                        ▼                        ▼
     QUEUE TYPES              SETTINGS                RELIABILITY
        │                        │                        │
        ├── Standard             ├── Visibility Timeout   ├── Dead-Letter Queue
        └── FIFO                 ├── Retention            └── Retry via Visibility Timeout
                                 ├── Delay Queue
                                 └── Long Polling
        │
        ▼
    SECURITY
        │
        ├── IAM / Queue Policy
        └── Encryption
        │
        ▼
  INTEGRATIONS
        │
        ├── Lambda
        ├── Auto Scaling
        └── SNS (Fan-out)
```

---

## ⭐ SQS Final Memory

```text
SQS
 │
 ├── What is it?
 │      └── Message Queue
 │
 ├── Push or Pull?
 │      └── Pull (consumers poll)
 │
 ├── Need strict order?
 │      └── FIFO Queue
 │
 ├── Need maximum speed?
 │      └── Standard Queue
 │
 ├── How to avoid processing twice at the same time?
 │      └── Visibility Timeout
 │
 ├── How to reduce empty responses and cost?
 │      └── Long Polling
 │
 ├── Where do failing messages go?
 │      └── Dead-Letter Queue
 │
 └── Who deletes a processed message?
        └── The Consumer
```

---

# 📢 PART 14 — SNS — Simple Notification Service

> **SNS = Send one message, many receive it (Push + Fan-out)**

---

## 14.1 📢 What is SNS?

> **SNS = Simple Notification Service**

Amazon SNS is a **fully managed publish/subscribe (pub/sub) messaging service**.

A **publisher** sends a message to a **topic**, and SNS **delivers a copy of that message to all subscribers** of that topic.

#### 📦 SNS Is Used To

- 📧 Send email notifications
- 📱 Send SMS text messages
- 📲 Send mobile push notifications
- 🔔 Send alerts from AWS services (like CloudWatch alarms)
- 🔀 **Fan-out** one message to many services (SQS, Lambda, HTTP endpoints)

#### 🏗 SNS Basic Architecture

```text
📤 Publisher
     │
     ▼
📢 SNS Topic
     │
     ├──► 📧 Email Subscriber
     ├──► 📱 SMS Subscriber
     ├──► ⚡ Lambda Subscriber
     ├──► 📬 SQS Subscriber
     └──► 🌐 HTTP/HTTPS Endpoint
```

#### 🏠 Simple Example

```text
📺 YouTube Channel

Channel Owner     = Publisher
Channel           = Topic
Subscribers       = People who get a notification when a new video is posted
```

#### 🧠 Easy Memory

> **SNS = Send one message, many receive it (Push + Fan-out)**

---

## 14.2 🤔 Why Do We Use SNS?

### ❌ Without SNS

```text
⚙️ Application must send the message to each system one by one

⚙️ App ──► 📧 Email system
⚙️ App ──► 📱 SMS system
⚙️ App ──► 📊 Analytics service
⚙️ App ──► 📦 Inventory service

(More code, more connections, hard to add new receivers)
```

### ✅ With SNS

```text
⚙️ App ──► 📢 SNS Topic ──┬──► 📧 Email
                          ├──► 📱 SMS
                          ├──► 📊 Analytics (Lambda)
                          └──► 📦 Inventory (SQS)

(App sends ONE message. New subscribers can be added anytime.)
```

#### ⭐ Main Reasons

- 🔀 One message reaches many receivers
- 🔗 Publisher and subscribers are **loosely coupled**
- ⚡ Messages are **pushed** immediately
- 🔌 Supports many subscriber types
- ❌ No servers to manage

---

## 14.3 🧰 What Does SNS Provide?

SNS provides:

- 📢 Topics (Standard and FIFO)
- 👥 Subscriptions
- 📤 Message Publishing
- 🎯 Message Filtering
- 🔁 Delivery Retries
- ☠️ Dead-Letter Queues for subscriptions
- 🔒 Encryption
- 🔐 Access Policies
- 📲 Mobile Push and SMS
- 📊 Delivery Status Logging

---

## 14.4 🧱 SNS Basic Concepts

```text
📢 SNS
│
├── 📤 Publisher     → Sends messages to a topic
├── 📢 Topic         → Channel for messages
├── 👥 Subscriber    → Receives messages from the topic
└── 🧾 Message       → The data being sent
```

### 14.4.1 📖 Simple Definitions

| Concept          | Simple Meaning                                                   |
| ---------------- | ---------------------------------------------------------------- |
| 📤 Publisher     | The service or application that **sends** a message              |
| 📢 Topic         | A named channel that **groups subscribers**                      |
| 👥 Subscription  | A link between a topic and a subscriber (endpoint)               |
| 🎯 Endpoint      | The destination (email address, phone number, Lambda ARN, URL...)|
| 🧾 Message       | The content sent through the topic                               |
| 🏷️ Message Attributes | Extra metadata used for filtering                           |

### 14.4.2 ⭐ Important Facts

- 🚀 SNS is a **push-based** service — SNS sends messages to subscribers
- 💨 SNS **does not store** messages for later pickup (it delivers them right away, with retries)
- 🌏 A topic belongs to **one Region**
- 📏 Message size is limited (**256 KB** in older documentation; AWS has since increased it to **1 MB** — check current docs)

#### 🧠 Remember

> **SNS = Push model. SNS pushes messages to subscribers.**

---

## 14.5 🗂 Types of SNS Topics

```text
📢 SNS Topic Types
│
├── 📢 Standard Topic
└── 🔢 FIFO Topic
```

### 14.5.1 📢 Standard Topic

The **default** topic type.

- 🚀 Very high throughput
- 📨 **At-least-once** delivery (duplicates possible)
- 🔀 **Best-effort ordering**
- 👥 Supports many subscriber types

> **Standard Topic = Fast, flexible, many protocols**

### 14.5.2 🔢 FIFO Topic

- 🔢 **Strict message ordering**
- 1️⃣ **Message deduplication**
- 🏷️ Topic name must **end with `.fifo`**
- 📬 Used with **SQS queues** as subscribers

> **FIFO Topic = Ordered and no duplicates (used with SQS)**

### 14.5.3 📊 Standard vs FIFO

| 📢 Standard Topic             | 🔢 FIFO Topic                            |
| ----------------------------- | ---------------------------------------- |
| Highest throughput            | Lower throughput                         |
| At-least-once delivery        | Exactly-once style delivery (dedup)      |
| Best-effort ordering          | Strict ordering                          |
| Many subscriber types         | Limited subscriber types (mainly SQS)    |
| Name can be anything          | Name must end with `.fifo`               |

---

## 14.6 👥 Subscribers and Protocols

SNS can deliver messages to many types of endpoints.

```text
👥 SNS Subscriber Types
│
├── 📧 Email / Email-JSON
├── 📱 SMS (text message)
├── 📲 Mobile Push Notifications (Apple, Google, Amazon devices)
├── 🌐 HTTP / HTTPS endpoint (webhook)
├── ⚡ AWS Lambda
├── 📬 Amazon SQS
└── 🔥 Amazon Data Firehose
```

#### 📊 Quick Idea

| Subscriber       | Use                                              |
| ---------------- | ------------------------------------------------ |
| 📧 Email         | Alerts to people (admins, team)                  |
| 📱 SMS           | Text alerts to phone numbers                     |
| 📲 Mobile Push   | App notifications on user devices                |
| 🌐 HTTP/HTTPS    | Send data to a web application                   |
| ⚡ Lambda        | Run code when a message arrives                  |
| 📬 SQS           | Store messages for later processing              |
| 🔥 Firehose      | Send data to S3, Redshift, etc.                  |

### 14.6.1 📧 Email Subscription Needs Confirmation

```text
1. 👤 We add an email address as a subscriber
          ↓
2. 📧 SNS sends a confirmation email
          ↓
3. 🖱️ The person clicks "Confirm subscription"
          ↓
4. ✅ Messages are now delivered
```

#### ⚠ Important

> **The subscription stays "Pending confirmation" until the email owner confirms it.**

---

## 14.7 🔀 Fan-Out Pattern (SNS + SQS)

**Fan-out** means **one message is delivered to many places** at the same time.

SNS + SQS is a very popular pattern.

```text
                      📤 Order Service
                             │
                             ▼
                    📢 SNS Topic: new-order
                             │
        ┌────────────────────┼────────────────────┐
        ▼                    ▼                    ▼
  📬 SQS: inventory    📬 SQS: email        ⚡ Lambda: analytics
        │                    │                    │
        ▼                    ▼                    ▼
  📦 Inventory         📧 Send email        📊 Save report
     Service              to customer
```

#### ⭐ Why Use SQS Behind SNS?

- 💾 SQS **stores** the message safely if the consumer is slow or down
- 🔁 Each consumer processes at its **own speed**
- 🧩 Each service has its **own queue**
- ➕ We can add a new consumer without changing the publisher

#### 🧠 Remember

> **SNS = Broadcast. SQS = Store. Together = Reliable fan-out.**

---

## 14.8 🎯 Message Filtering

By default, every subscriber gets **every message**.

With a **Filter Policy**, a subscriber receives **only the messages it needs**.

#### 🏗 Example

```text
📢 Topic: orders
   │
   │ Message attribute: type = "electronics"
   ▼
┌───────────────────────┬───────────────────────┐
▼                       ▼                       ▼
📬 Queue A              📬 Queue B              📬 Queue C
Filter: electronics     Filter: clothes         No filter
✅ Receives             ❌ Does not receive     ✅ Receives all
```

#### 💻 Example Filter Policy

```json
{
  "type": ["electronics"]
}
```

#### ⭐ Key Points

- 🏷️ Filter policy is attached to the **subscription** (not the topic)
- 🎯 Can filter on **message attributes** (or on message body, depending on the policy scope)
- ✅ Reduces the need for extra code and extra topics

> **Filtering = Each subscriber gets only the messages it wants**

---

## 14.9 💻 SNS Commands and Code

### 14.9.1 ⌨ AWS CLI Examples

```bash
# Create a topic
aws sns create-topic --name my-alerts

# Subscribe an email address
aws sns subscribe \
  --topic-arn arn:aws:sns:ap-south-1:123456789012:my-alerts \
  --protocol email \
  --notification-endpoint you@example.com

# Publish a message
aws sns publish \
  --topic-arn arn:aws:sns:ap-south-1:123456789012:my-alerts \
  --subject "Server Alert" \
  --message "CPU is above 70% on web-server-1"
```

### 14.9.2 🐍 Python (boto3) Example

```python
import boto3

sns = boto3.client("sns", region_name="ap-south-1")
topic_arn = "arn:aws:sns:ap-south-1:123456789012:my-alerts"

sns.publish(
    TopicArn=topic_arn,
    Subject="Server Alert",
    Message="CPU is above 70% on web-server-1",
)
```

---

## 14.10 🔁 Delivery, Retries and DLQ

SNS tries to deliver each message and **retries if delivery fails**.

#### 🔄 Delivery Flow

```text
📢 SNS Topic
     │
     ▼
📤 Delivery attempt to subscriber
     │
 ┌───┴───┐
 ▼       ▼
✅ Success   ❌ Failure
             │
             ▼
        🔁 Retry (based on the delivery policy)
             │
             ▼
   ☠️ After all retries fail → Dead-Letter Queue (if configured)
```

#### ⭐ Key Points

- 🔁 Retry behavior depends on the **protocol** (SQS and Lambda have strong delivery retries)
- ☠️ We can attach a **Dead-Letter Queue (SQS)** to a **subscription** to keep undelivered messages
- 📊 We can enable **delivery status logging** to CloudWatch Logs

---

## 14.11 🔒 SNS Security

```text
🔐 SNS Security
│
├── 🔐 Access Control
│   ├── 📜 IAM Policy         → What an identity can do
│   └── 📢 Topic Access Policy → Who can publish/subscribe (also cross-account)
│
├── 🔒 Encryption at Rest → SSE using AWS KMS
└── 🌐 Encryption in Transit → HTTPS
```

#### 💻 Example: Allow CloudWatch to Publish to a Topic

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "Service": "cloudwatch.amazonaws.com" },
      "Action": "sns:Publish",
      "Resource": "arn:aws:sns:ap-south-1:123456789012:my-alerts"
    }
  ]
}
```

#### ⚠ Important

> If the topic is encrypted with a KMS key, the **publishing service must also have permission to use that key**.

---

## 14.12 🔗 SNS Integrations with AWS Services

SNS works closely with many AWS services.

```text
🔗 SNS Integrations
│
├── 📊 CloudWatch Alarms     → Send alerts to a topic
├── 🪣 S3 Event Notifications → Notify when an object is created
├── 📈 Auto Scaling           → Notify on instance launch/terminate
├── 🗄️ RDS Events             → Notify on failover, backups
├── ⏰ EventBridge            → Send events to a topic
└── 🌱 Elastic Beanstalk      → Notify on environment events
```

#### 💻 Example: CloudWatch Alarm → SNS → Email

```text
📊 CloudWatch Alarm (CPU > 70%)
         │
         ▼
📢 SNS Topic: my-alerts
         │
         ▼
📧 Email to the DevOps team
```

---

## 14.13 📲 SMS and Mobile Push

### 14.13.1 📱 SMS

SNS can send **text messages** to phone numbers.

- 🌍 Supports many countries
- 💰 Charged **per SMS** (price depends on the country)
- 📏 Has spending limits and sandbox rules for new accounts
- ⚠️ Some countries require **sender registration** rules (check AWS documentation)

### 14.13.2 📲 Mobile Push Notifications

SNS can send push messages to mobile apps through services like:

- 🍎 Apple Push Notification Service (APNs)
- 🤖 Firebase Cloud Messaging (FCM, for Android)

```text
📢 SNS ──► 📲 Push Service (APNs / FCM) ──► 📱 User's Phone
```

---

## 14.14 🆚 SNS vs SQS

| 📢 SNS                                 | 📬 SQS                                   |
| -------------------------------------- | ---------------------------------------- |
| **Pub/Sub** (broadcast)                | **Queue** (storage)                      |
| **Push** — SNS sends to subscribers    | **Pull** — consumers poll the queue      |
| One message → **many subscribers**     | One message → **one consumer**           |
| Messages are **not stored** for pickup | Messages are **stored** until deleted    |
| Used for notifications and fan-out     | Used for decoupling and buffering        |

#### 🧠 Easy Memory

```text
📢 SNS = Loudspeaker (announce to everyone)
📬 SQS = Mailbox (wait for pickup)
```

---

## 14.15 💰 SNS Pricing

```text
💰 SNS Cost
│
├── 📨 Number of requests / published messages
├── 📤 Deliveries to some endpoints (HTTP, SMS, email, mobile push)
├── 📱 SMS messages (price depends on country)
└── 🌐 Data transfer out
```

- 🎁 SNS has a **free tier** (some requests and email deliveries per month)
- 💡 Delivery to **SQS and Lambda** is usually very cheap or covered by free amounts

---

## 14.16 🏗 Real Example: Order Notification System

### 🎯 Requirement

When a customer places an order:

- 📧 Send a **confirmation email** to the customer
- 📦 Update **inventory**
- 📊 Save data for **analytics**

### 🏗 Architecture

```text
👤 Customer places order
        │
        ▼
🌐 Order API (API Gateway + Lambda)
        │ publish
        ▼
📢 SNS Topic: new-order
        │
 ┌──────┼───────────────┐
 ▼      ▼               ▼
📧     📬 SQS           ⚡ Lambda
Email  (inventory)      (analytics)
```

### 🪜 Steps to Build It

```text
1. Create the SNS topic: new-order
2. Create SQS queue: inventory-queue
3. Subscribe inventory-queue to the topic
     → Add queue policy allowing SNS to send messages
4. Subscribe a Lambda function (analytics)
5. Subscribe an email address (confirm it)
6. Publish a test message to the topic
7. ✅ Check email, queue message and Lambda logs
```

### 🚨 Another Example: Alerts

```text
📊 CloudWatch Alarm ──► 📢 SNS Topic: ops-alerts ──┬──► 📧 Email (DevOps team)
                                                   └──► 📱 SMS (On-call engineer)
```

---

## 📌🧠 SNS Quick Revision

```text
📢 SNS
│
├── 🧱 Basics
│   ├── 📤 Publisher
│   ├── 📢 Topic
│   ├── 👥 Subscriber
│   └── 🧾 Message
│
├── 🗂️ Topic Types
│   ├── 📢 Standard
│   └── 🔢 FIFO
│
├── 👥 Subscriber Types
│   ├── Email / SMS
│   ├── Mobile Push
│   ├── HTTP/HTTPS
│   ├── Lambda
│   ├── SQS
│   └── Firehose
│
├── 🔀 Patterns
│   ├── Fan-out (SNS + SQS)
│   └── Message Filtering
│
├── 🔁 Reliability
│   ├── Retries
│   └── Subscription DLQ
│
└── 🔒 Security
    ├── IAM / Topic Policy
    └── Encryption (KMS)
```

---

## 🧠⚡ SNS One-Line Memory

| Concept                     | Easy Memory                                      |
| --------------------------- | ------------------------------------------------ |
| 📢 **SNS**                  | Publish/Subscribe Notification Service           |
| 📤 **Publisher**            | Sends a Message to a Topic                       |
| 📢 **Topic**                | Channel That Groups Subscribers                  |
| 👥 **Subscriber**           | Receives Messages from a Topic                   |
| 🚀 **Push Model**           | SNS Sends Messages to Subscribers                |
| 💨 **No Storage**           | SNS Does Not Keep Messages for Later Pickup      |
| 📢 **Standard Topic**       | Fast, Many Protocols, Best-effort Order          |
| 🔢 **FIFO Topic**           | Ordered, No Duplicates, Used with SQS            |
| 🔀 **Fan-out**              | One Message to Many Places (SNS + SQS)           |
| 🎯 **Filter Policy**        | Subscriber Gets Only the Messages It Wants       |
| ☠️ **DLQ**                  | Keeps Messages That Could Not Be Delivered       |
| 📧 **Email Subscription**   | Needs Confirmation by the Email Owner            |

---

## 🗺 SNS Learning Map

```text
                           📢 Amazon SNS
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
        ▼                        ▼                        ▼
      TOPICS                SUBSCRIBERS               FEATURES
        │                        │                        │
        ├── Standard             ├── Email / SMS          ├── Fan-out
        └── FIFO                 ├── Mobile Push          ├── Message Filtering
                                 ├── HTTP/HTTPS           ├── Retries
                                 ├── Lambda               └── Dead-Letter Queue
                                 ├── SQS
                                 └── Firehose
        │
        ▼
    SECURITY
        │
        ├── IAM / Topic Policy
        └── Encryption
        │
        ▼
  INTEGRATIONS
        │
        ├── CloudWatch Alarms
        ├── S3 Events
        ├── Auto Scaling
        └── EventBridge
```

---

## ⭐ SNS Final Memory

```text
SNS
 │
 ├── What is it?
 │      └── Pub/Sub Notification Service
 │
 ├── Push or Pull?
 │      └── Push
 │
 ├── Where do publishers send messages?
 │      └── To a Topic
 │
 ├── Who receives them?
 │      └── Subscribers (Email, SMS, Lambda, SQS ...)
 │
 ├── How to send one message to many services?
 │      └── Fan-out (SNS + SQS)
 │
 ├── How to send only needed messages to a subscriber?
 │      └── Filter Policy
 │
 ├── Need ordering and no duplicates?
 │      └── FIFO Topic (with SQS)
 │
 └── Common alert path?
        └── CloudWatch Alarm → SNS → Email
```

---

# 📊 PART 15 — CloudWatch — Monitoring and Logs

> **CloudWatch = Eyes and alarm bell of our AWS account**

---

## 15.1 📊 What is CloudWatch?

> **CloudWatch = Monitoring and Observability Service of AWS**

Amazon CloudWatch is a service that **collects, shows and acts on data** (metrics, logs and events) from our AWS resources and applications.

It helps us answer questions like:

- ❓ Is my server healthy?
- ❓ Is the CPU too high?
- ❓ Did my Lambda function fail?
- ❓ What error came in my application log?

#### 📦 CloudWatch Can Monitor

- 🖥️ EC2 instances
- 🗄️ RDS databases
- ⚡ Lambda functions
- 🪣 S3 buckets
- ⚖️ Load Balancers
- 📱 Our own applications (custom metrics and logs)

#### 🏗 CloudWatch Basic Idea

```text
☁️ AWS Resources / Applications
        │
        │ send data
        ▼
📊 CloudWatch
   ├── 📈 Metrics   (numbers over time)
   ├── 📝 Logs      (text records)
   ├── 🚨 Alarms    (alerts and actions)
   └── 📋 Dashboards (graphs in one place)
```

#### 🧠 Easy Memory

> **CloudWatch = Eyes and Alarm Bell of our AWS account**

---

## 15.2 🤔 Why Do We Use CloudWatch?

### ❌ Without Monitoring

```text
💥 Server becomes slow
        ↓
😴 Nobody notices
        ↓
👥 Users face problems
        ↓
📞 Customers complain first
```

### ✅ With CloudWatch

```text
📈 CloudWatch watches CPU, memory, errors
        ↓
🚨 Alarm triggers when value is too high
        ↓
📧 Team gets notified (SNS)
        ↓
🔧 Problem fixed quickly (or Auto Scaling adds servers)
```

#### ⭐ Main Reasons

- 👀 See the health and performance of resources
- 🚨 Get alerts before users complain
- 📈 Trigger **Auto Scaling** automatically
- 📝 Store and search application logs
- 🛠️ Troubleshoot problems faster
- 💰 Find unused or underused resources

---

## 15.3 🧰 What Does CloudWatch Provide?

CloudWatch provides:

- 📈 Metrics
- 📝 Logs
- 🚨 Alarms
- 📋 Dashboards
- 🔎 Logs Insights (query logs)
- ⏰ EventBridge (events and schedules)
- 🧪 Synthetics (test websites and APIs)
- 🤖 CloudWatch Agent (collect memory, disk and logs from servers)

---

## 15.4 📈 CloudWatch Metrics

A **Metric** is a **number measured over time**.

#### 💻 Examples

```text
📈 EC2 CPUUtilization      → 45%
📈 RDS DatabaseConnections → 120
📈 Lambda Errors           → 3
📈 ALB RequestCount        → 5000
```

### 15.4.1 🧱 Metric Terms

```text
📈 Metric
│
├── 📦 Namespace   → Group of metrics (example: AWS/EC2)
├── 🏷️ Metric Name → Name of the value (example: CPUUtilization)
├── 🔖 Dimension   → Extra detail to identify (example: InstanceId)
├── 🕒 Timestamp   → Time of the data
├── 🔢 Value       → The measured number
└── 📏 Unit        → Percent, Bytes, Count, Seconds ...
```

#### 📖 Simple Definitions

| Term          | Simple Meaning                                           |
| ------------- | -------------------------------------------------------- |
| 📦 Namespace  | A container (group) for metrics, like `AWS/EC2`          |
| 🏷️ Metric Name| What we measure, like `CPUUtilization`                   |
| 🔖 Dimension  | A name-value pair to pick a specific resource (`InstanceId=i-123`) |
| 🕒 Datapoint  | One measured value at one time                           |
| ⏱️ Period     | Time length used to group datapoints (like 60 seconds)   |
| 📊 Statistic  | Average, Sum, Minimum, Maximum, SampleCount              |

### 15.4.2 📦 Default (Built-in) Metrics

AWS services send metrics to CloudWatch **automatically**.

| Service    | Example Metrics                                               |
| ---------- | ------------------------------------------------------------- |
| 🖥️ EC2     | CPUUtilization, NetworkIn/Out, DiskReadOps, StatusCheckFailed |
| 🗄️ RDS     | CPUUtilization, FreeStorageSpace, DatabaseConnections         |
| ⚡ Lambda  | Invocations, Errors, Duration, Throttles                      |
| ⚖️ ALB     | RequestCount, TargetResponseTime, HTTPCode_Target_5XX_Count   |
| 🪣 S3      | BucketSizeBytes, NumberOfObjects (daily storage metrics)      |

#### ⚠ Important

> **EC2 does NOT send memory (RAM) usage and disk space usage by default.** To get these, install the **CloudWatch Agent** on the instance.

### 15.4.3 ⏱ Basic vs Detailed Monitoring (EC2)

| 🟢 Basic Monitoring              | 🔵 Detailed Monitoring            |
| -------------------------------- | --------------------------------- |
| Data every **5 minutes**         | Data every **1 minute**           |
| Free                             | Extra cost                        |
| Default for EC2                  | Must be enabled                   |

### 15.4.4 🛠 Custom Metrics

We can send **our own metrics** to CloudWatch (for example, number of logged-in users, memory usage, queue length).

```text
📱 Our Application / Script
        │ PutMetricData (API / CLI / SDK)
        ▼
📊 CloudWatch Custom Metric
```

#### 💻 CLI Example

```bash
aws cloudwatch put-metric-data \
  --namespace "MyApp" \
  --metric-name "ActiveUsers" \
  --value 150 \
  --unit Count
```

#### ⭐ Key Points

- 🚀 **Standard resolution** = data at 1-minute level
- ⚡ **High resolution** = data down to **1 second**

### 15.4.5 🗓 Metric Retention

CloudWatch keeps metric data for a long time, and older data is stored at lower detail.

| Data Detail         | Kept For          |
| ------------------- | ----------------- |
| Under 60 seconds    | 3 hours           |
| 1 minute            | 15 days           |
| 5 minutes           | 63 days           |
| 1 hour              | 455 days (15 months) |

#### 🧠 Simple Meaning

> **Metric = A number tracked over time**

---

## 15.5 🚨 CloudWatch Alarms

A **CloudWatch Alarm** watches **one metric** and takes an **action** when the metric crosses a limit (threshold).

#### 🏗 How an Alarm Works

```text
📈 Metric (CPUUtilization)
        │
        ▼
🚨 Alarm  (Threshold: CPU > 70% for 5 minutes)
        │
        ▼
 ┌──────┴──────┐
 ▼             ▼
📧 SNS      📈 Auto Scaling
(Notify)    (Add servers)
```

### 15.5.1 🚦 Alarm States

```text
🚦 Alarm States
│
├── 🟢 OK                    → Metric is within the limit
├── 🔴 ALARM                 → Metric crossed the limit
└── ⚪ INSUFFICIENT_DATA     → Not enough data to decide
```

### 15.5.2 🧱 Alarm Settings

| Setting                | Meaning                                          |
| ---------------------- | ------------------------------------------------ |
| 📈 Metric              | What to watch (like CPUUtilization)              |
| 📏 Threshold           | The limit (like 70%)                             |
| ⏱️ Period              | Length of each time window (like 5 minutes)      |
| 🔁 Evaluation Periods  | How many periods to check                        |
| 🎯 Datapoints to Alarm | How many bad datapoints cause the ALARM state    |
| ⚙️ Condition           | Greater than, less than, etc.                    |

#### 💻 Example

```text
Alarm: High-CPU
Metric:    CPUUtilization
Condition: > 70%
Period:    5 minutes
Result:    If CPU stays above 70% for 5 minutes → ALARM
```

### 15.5.3 🎯 Alarm Actions

When the alarm changes state, it can:

```text
🎯 Alarm Actions
│
├── 📧 Send notification          → SNS topic (email, SMS, Lambda)
├── 📈 Auto Scaling action        → Add or remove instances
├── 🖥️ EC2 action                 → Stop, Terminate, Reboot, Recover instance
└── 🛠️ Systems Manager action     → Create OpsItem / Incident
```

### 15.5.4 🧩 Composite Alarm

A **Composite Alarm** combines **multiple alarms** using AND / OR rules.

```text
🚨 Alarm A (CPU high)  AND  🚨 Alarm B (Memory high)  →  🚨 Composite Alarm
```

It helps reduce **alert noise**.

#### 🧠 Simple Meaning

> **Alarm = Watch a metric, then act when it crosses a limit**

---

## 15.6 📝 CloudWatch Logs

**CloudWatch Logs** stores and lets us search **log files** from our applications and AWS services.

#### 🏗 Log Structure

```text
📝 CloudWatch Logs
│
└── 📁 Log Group           → Collection of log streams (like one app)
      │
      ├── 📄 Log Stream 1  → Logs from one source (one server/function)
      ├── 📄 Log Stream 2
      └── 📄 Log Stream 3
            └── 🧾 Log Events (individual log lines)
```

#### 📖 Simple Definitions

| Term            | Simple Meaning                                           |
| --------------- | -------------------------------------------------------- |
| 📁 Log Group    | A group of logs that share the same settings (retention, access) |
| 📄 Log Stream   | A sequence of log events from one source                 |
| 🧾 Log Event    | One log line with a timestamp                            |
| 🗓️ Retention    | How long to keep logs (1 day to forever)                 |

### 15.6.1 📤 Where Logs Come From

```text
📤 Log Sources
│
├── ⚡ Lambda          → Logs sent automatically
├── 🖥️ EC2             → Using the CloudWatch Agent
├── 🌐 API Gateway     → Access and execution logs
├── 🗄️ RDS             → Error, slow query and general logs (if enabled)
├── 🌐 VPC Flow Logs   → Network traffic logs
└── 📱 Our Application → Using SDK or agent
```

### 15.6.2 🗓 Retention

- By default, log groups are kept **forever (never expire)**
- We should set a **retention period** (like 7, 30, 90 days) to save cost

#### ⚠ Important

> **Logs stored forever can become expensive.** Always set a retention period.

### 15.6.3 🔍 Metric Filters

A **Metric Filter** looks for a **pattern** in logs and **turns it into a metric**.

```text
📝 Log: "ERROR: Database connection failed"
        ↓
🔍 Metric Filter (pattern: ERROR)
        ↓
📈 Metric: ErrorCount
        ↓
🚨 Alarm when ErrorCount > 5
```

### 15.6.4 📡 Subscription Filters

A **Subscription Filter** sends log data **in real time** to another service.

```text
📝 Log Group ──► 🔍 Subscription Filter ──► ⚡ Lambda / 🔥 Firehose / 🌊 Kinesis
```

### 15.6.5 🔎 Logs Insights

**CloudWatch Logs Insights** lets us **search and analyze logs using queries**.

#### 💻 Example Query

```text
fields @timestamp, @message
| filter @message like /ERROR/
| sort @timestamp desc
| limit 20
```

This shows the latest 20 error lines.

### 15.6.6 📦 Export Logs

Logs can be **exported to S3** for long-term storage.

#### 🧠 Simple Meaning

> **CloudWatch Logs = Central place to store and search logs**

---

## 15.7 🤖 CloudWatch Agent

The **CloudWatch Agent** is software we install on **EC2 instances or on-premises servers**.

#### 🎯 It Collects

- 🧠 **Memory** usage
- 💾 **Disk** space usage
- 📊 More system-level metrics
- 📝 **Log files** from the server (like `/var/log/messages`, application logs)

#### 🏗 How It Works

```text
🖥️ EC2 Instance
   └── 🤖 CloudWatch Agent
          ├── 📈 Sends memory/disk metrics ──► CloudWatch Metrics
          └── 📝 Sends log files           ──► CloudWatch Logs
```

#### 🪜 Steps

```text
1. Attach an IAM Role to EC2 (with CloudWatchAgentServerPolicy)
2. Install the CloudWatch Agent
3. Create the agent configuration (which metrics and logs to send)
4. Start the agent
5. ✅ View data in CloudWatch
```

#### ⚠ Important

> The agent needs **IAM permissions**. Use an **IAM Role** for EC2 instead of access keys.

---

## 15.8 📋 CloudWatch Dashboards

A **Dashboard** is a **customizable page** with graphs and numbers from different metrics.

```text
📋 My-App Dashboard
├── 📈 EC2 CPU graph
├── 📈 RDS connections graph
├── 📈 ALB request count graph
└── 🚨 Alarm status widget
```

#### ⭐ Key Points

- 🌍 Can show metrics from **different Regions and accounts**
- 🖱️ Can be created from the console or code
- 👀 Useful for **one-screen view** of the whole application

> **Dashboard = Our control panel with graphs**

---

## 15.9 ⏰ EventBridge (CloudWatch Events)

**Amazon EventBridge** (earlier called **CloudWatch Events**) lets us **react to events** or **run things on a schedule**.

```text
⏰ EventBridge
│
├── 📅 Schedule Rule  → Run at a time (cron or rate)
└── 🔔 Event Rule     → React to an AWS event
```

#### 💻 Examples

```text
📅 Every day at 9 AM       → Trigger Lambda to stop Dev servers
🔔 EC2 instance stopped    → Send SNS notification
🔔 S3 object created       → Trigger Lambda
```

#### 🏗 Flow

```text
🔔 Event (EC2 state change, schedule, etc.)
        ↓
📏 Rule (event pattern)
        ↓
🎯 Target (Lambda, SNS, SQS, Step Functions ...)
```

#### 📖 Schedule Expressions

```text
rate(5 minutes)             → Every 5 minutes
cron(0 9 * * ? *)           → Every day at 9:00 AM (UTC)
```

> **EventBridge = Event router and scheduler**

---

## 15.10 🧪 Other Useful CloudWatch Features

```text
🧪 More Features
│
├── 🧪 Synthetics        → Canaries that test our website/API on a schedule
├── 📦 Container Insights → Metrics for ECS, EKS containers
├── ⚡ Lambda Insights    → Detailed Lambda performance data
├── 🤖 Anomaly Detection  → Uses ML to find unusual metric patterns
└── 🔍 X-Ray (related)    → Trace requests across services
```

---

## 15.11 ⚖ CloudWatch vs CloudTrail vs AWS Config

These three are often confused.

| Service           | Main Question                         | Easy Memory                    |
| ----------------- | ------------------------------------- | ------------------------------ |
| 📊 **CloudWatch** | How is my resource **performing**?    | Performance and monitoring     |
| 🕵️ **CloudTrail** | **Who did what** in my account?       | API activity / audit log       |
| 🗂️ **AWS Config** | How did my resource **configuration change**? | Configuration history  |

#### 💻 Example

```text
EC2 server is slow            → CloudWatch (CPU metrics)
Someone deleted a bucket      → CloudTrail (who and when)
Security Group rules changed  → AWS Config (what changed)
```

#### 🧠 Easy Memory

```text
📊 CloudWatch = PERFORMANCE
🕵️ CloudTrail = WHO DID IT
🗂️ Config     = WHAT CHANGED
```

---

## 15.12 💰 CloudWatch Pricing

```text
💰 CloudWatch Cost
│
├── 📈 Custom Metrics (per metric per month)
├── 🔬 Detailed Monitoring (EC2)
├── 🚨 Alarms (per alarm per month)
├── 📝 Logs → Data ingestion + Storage
├── 🔎 Logs Insights queries (per GB scanned)
├── 📋 Dashboards (beyond the free ones)
└── 🧪 Synthetics canaries
```

- 🎁 There is a **free tier** (some metrics, alarms, logs and dashboards)
- ✅ Default metrics from AWS services are **free**

#### 💡 Cost Tips

- 🗓️ Set **log retention** for every log group
- 🧹 Delete unused alarms and dashboards
- 📏 Avoid sending too many custom metrics

---

## 15.13 🏗 Real Example: High CPU Alert + Auto Scaling

### 🎯 Requirement

- If EC2 CPU goes above 70%, **send an email** to the team.
- Also **add more servers** automatically.

### 🏗 Architecture

```text
🖥️ EC2 Instances (Auto Scaling Group)
        │ CPUUtilization
        ▼
📈 CloudWatch Metric
        │
        ▼
🚨 Alarm: CPU > 70% for 5 minutes
        │
   ┌────┴─────────────┐
   ▼                  ▼
📢 SNS Topic       📈 Auto Scaling Policy
   │                  │
   ▼                  ▼
📧 Email to team   ➕ Add 2 instances
```

### 🪜 Steps to Build It

```text
1. Create an SNS topic and subscribe our email (confirm the email)
2. Open CloudWatch → Alarms → Create Alarm
3. Select metric: EC2 → Per-Instance (or ASG) → CPUUtilization
4. Condition: Greater than 70 for 5 minutes
5. Action: Send notification to the SNS topic
6. (Optional) Action: Attach the Auto Scaling policy
7. Create the alarm
8. Test by generating CPU load on the instance
9. ✅ Check the email and the alarm state
```

### 🛑 Another Example: Auto-Recover Instance

```text
🖥️ EC2 → Metric: StatusCheckFailed_System
        ↓
🚨 Alarm (value > 0)
        ↓
🔁 EC2 Action: Recover instance
```

---

## 📌🧠 CloudWatch Quick Revision

```text
📊 CloudWatch
│
├── 📈 Metrics
│   ├── Default Metrics
│   ├── Custom Metrics
│   ├── Basic (5 min) vs Detailed (1 min)
│   └── Namespace, Dimension, Period
│
├── 🚨 Alarms
│   ├── OK / ALARM / INSUFFICIENT_DATA
│   ├── Threshold, Period, Evaluation Periods
│   ├── Actions → SNS, Auto Scaling, EC2
│   └── Composite Alarms
│
├── 📝 Logs
│   ├── Log Group / Log Stream
│   ├── Retention
│   ├── Metric Filters
│   ├── Subscription Filters
│   └── Logs Insights
│
├── 🤖 CloudWatch Agent
│   ├── Memory and Disk metrics
│   └── Server log files
│
├── 📋 Dashboards
│
├── ⏰ EventBridge
│   ├── Schedule Rules
│   └── Event Rules
│
└── 🔗 Related
    ├── CloudTrail → Who did it
    └── Config → What changed
```

---

## 🧠⚡ CloudWatch One-Line Memory

| Concept                     | Easy Memory                                      |
| --------------------------- | ------------------------------------------------ |
| 📊 **CloudWatch**           | Monitoring Service of AWS                        |
| 📈 **Metric**               | A Number Tracked Over Time                       |
| 📦 **Namespace**            | Group of Metrics (AWS/EC2)                       |
| 🔖 **Dimension**            | Detail to Pick a Specific Resource               |
| 🛠️ **Custom Metric**        | Our Own Metric Sent to CloudWatch                |
| 🚨 **Alarm**                | Watches a Metric and Takes Action                |
| 🚦 **Alarm States**         | OK, ALARM, INSUFFICIENT_DATA                     |
| 📝 **Log Group**            | Collection of Log Streams                        |
| 📄 **Log Stream**           | Logs From One Source                             |
| 🔍 **Metric Filter**        | Turns Log Patterns Into Metrics                  |
| 🔎 **Logs Insights**        | Search Logs Using Queries                        |
| 🤖 **CloudWatch Agent**     | Collects Memory, Disk and Log Files              |
| 📋 **Dashboard**            | One-Screen View of Graphs                        |
| ⏰ **EventBridge**          | Event Router and Scheduler                       |
| 🕵️ **CloudTrail**           | Who Did What                                     |
| 🗂️ **AWS Config**           | What Changed                                     |

---

## 🗺 CloudWatch Learning Map

```text
                        📊 CloudWatch
                              │
      ┌───────────────────────┼───────────────────────┐
      │                       │                       │
      ▼                       ▼                       ▼
   COLLECT                  WATCH                    ACT
      │                       │                       │
      ├── Metrics             ├── Dashboards          ├── Alarms
      ├── Logs                ├── Logs Insights       │    ├── SNS
      └── CloudWatch Agent    └── Synthetics          │    ├── Auto Scaling
                                                      │    └── EC2 Actions
                                                      └── EventBridge
                                                           ├── Schedule
                                                           └── Event Rules
```

---

## ⭐ CloudWatch Final Memory

```text
CloudWatch
 │
 ├── What is it?
 │      └── Monitoring Service
 │
 ├── How do we measure things?
 │      └── Metrics
 │
 ├── How do we get alerts?
 │      └── Alarms → SNS
 │
 ├── Where do we store logs?
 │      └── CloudWatch Logs
 │
 ├── How do we get memory and disk usage from EC2?
 │      └── CloudWatch Agent
 │
 ├── How do we see everything on one screen?
 │      └── Dashboards
 │
 ├── How do we run something on a schedule?
 │      └── EventBridge
 │
 └── Who did it / What changed?
        └── CloudTrail / Config
```

---

# 🏗 PART 16 — CloudFormation — Infrastructure as Code

> **CloudFormation = Write a template once, build the same infrastructure again and again**

---

## 16.1 🏗 What is CloudFormation?

> **CloudFormation = Infrastructure as Code (IaC) service of AWS**

AWS CloudFormation lets us **describe our AWS resources in a text file (template)**, and AWS **creates and manages those resources for us automatically**.

Instead of clicking in the console again and again, we **write the infrastructure as code**.

#### 🤔 What is Infrastructure as Code (IaC)?

> **IaC = Managing infrastructure using code files instead of manual clicks**

```text
📝 Code file (Template)
        ↓
☁️ CloudFormation reads it
        ↓
🏗️ Creates EC2, VPC, S3, RDS ... exactly as written
```

#### 📦 CloudFormation Can Create

- 🌐 VPC, Subnets, Gateways
- 🖥️ EC2 instances and Auto Scaling
- 🪣 S3 buckets
- 🗄️ RDS and DynamoDB
- ⚡ Lambda functions
- 🔐 IAM roles
- …almost every AWS service

#### 🏗 Basic Architecture

```text
📝 Template (YAML / JSON)
        │
        ▼
🏗️ CloudFormation
        │
        ▼
📚 Stack  ──► 🖥️ EC2   🪣 S3   🗄️ RDS   🌐 VPC   ⚡ Lambda ...
```

#### 🧠 Easy Memory

> **CloudFormation = Write a template once, build the same infrastructure again and again**

---

## 16.2 🤔 Why Do We Use CloudFormation?

### ❌ Manual Setup (Console Clicking)

```text
🖱️ Click, click, click in the console
        ↓
😵 Hard to remember every step
        ↓
🐛 Mistakes happen
        ↓
🔁 Hard to repeat the same setup (dev, test, prod)
```

### ✅ With CloudFormation

```text
📝 Write a template
        ↓
🚀 Create a stack
        ↓
🔁 Reuse the same template for dev, test and prod
        ↓
🧹 Delete the stack to remove everything cleanly
```

#### ⭐ Main Reasons

- 🔁 **Repeatable** — same result every time
- 📝 **Version control** — store templates in Git
- ⚡ **Fast** — build full environments in minutes
- 🐛 **Fewer mistakes** — no manual steps
- 🧹 **Easy cleanup** — delete the stack, all resources are removed
- 💰 **CloudFormation is free** — we pay only for the resources created
- 🔍 **Track changes** — see what will change before updating

---

## 16.3 🧰 What Does CloudFormation Provide?

CloudFormation provides:

- 📝 Templates (YAML / JSON)
- 📚 Stacks
- 🔄 Change Sets
- 🌍 StackSets (multi-account / multi-Region)
- 🔍 Drift Detection
- 🧩 Nested Stacks
- 🔁 Automatic Rollback
- 🛡️ Stack Policies and Termination Protection
- 🔗 Cross-Stack References (Exports / Imports)

---

## 16.4 🧱 CloudFormation Basic Concepts

```text
🏗️ CloudFormation
│
├── 📝 Template     → The blueprint (file)
├── 📚 Stack        → Group of resources created from a template
├── 🧩 Resource     → One AWS service item (EC2, S3 ...)
├── 🔄 Change Set   → Preview of changes before updating
└── 🌍 StackSet     → Deploy a stack to many accounts/Regions
```

### 16.4.1 📖 Simple Definitions

| Concept          | Simple Meaning                                                      |
| ---------------- | ------------------------------------------------------------------- |
| 📝 **Template**  | A JSON or YAML file that describes the resources we want            |
| 📚 **Stack**     | The running result of a template — all resources managed as **one unit** |
| 🧩 **Resource**  | An AWS item defined in the template (like an S3 bucket)             |
| 🔄 **Change Set**| A preview of what will change when we update a stack                |
| 🌍 **StackSet**  | Create stacks in many accounts and Regions with one operation       |
| 🔍 **Drift**     | When real resources are changed manually and no longer match the template |

### 16.4.2 🏗 Relationship

```text
📝 Template: web-app.yaml
        │
        ├──► 📚 Stack: web-app-dev     (Dev environment)
        ├──► 📚 Stack: web-app-test    (Test environment)
        └──► 📚 Stack: web-app-prod    (Prod environment)
```

#### 🧠 Remember

> **One Template can create many Stacks. One Stack manages all its resources together.**

---

## 16.5 📝 Template Anatomy

A CloudFormation template has **sections**.

```text
📝 Template Sections
│
├── 🔢 AWSTemplateFormatVersion  → Template version (optional)
├── 📄 Description               → Text describing the template (optional)
├── 🏷️ Metadata                  → Extra information (optional)
├── 🎛️ Parameters                → Input values given at stack creation (optional)
├── 🗺️ Mappings                  → Lookup tables (optional)
├── ❓ Conditions                → If/else logic (optional)
├── 🔄 Transform                 → Macros like AWS::Serverless (optional)
├── 🧩 Resources                 → The AWS resources (REQUIRED)
└── 📤 Outputs                   → Values to show/export after creation (optional)
```

#### ⚠ Important

> **Only the `Resources` section is required.** All other sections are optional.

### 16.5.1 🎛 Parameters

**Parameters** let us **pass values into the template** when creating the stack, so the same template can be reused.

```yaml
Parameters:
  InstanceType:
    Type: String
    Default: t3.micro
    AllowedValues:
      - t3.micro
      - t3.small
    Description: EC2 instance size
```

#### 🎯 Used For

- 🖥️ Instance type (small for dev, large for prod)
- 🏷️ Names, environment names
- 🔑 Key pair names

### 16.5.2 🧩 Resources

The **main section**. Each resource has a **logical ID**, a **Type** and **Properties**.

```yaml
Resources:
  MyBucket:                      # Logical ID (our own name)
    Type: AWS::S3::Bucket        # Resource Type
    Properties:                  # Settings of the resource
      VersioningConfiguration:
        Status: Enabled
```

#### 📖 Understanding It

```text
Logical ID  → Name used inside the template (MyBucket)
Type        → Which AWS resource (AWS::S3::Bucket)
Properties  → Configuration of that resource
```

#### 🔠 Resource Type Format

```text
AWS::<Service>::<Resource>

AWS::EC2::Instance
AWS::S3::Bucket
AWS::IAM::Role
AWS::Lambda::Function
AWS::DynamoDB::Table
```

### 16.5.3 📤 Outputs

**Outputs** show **useful values** after the stack is created (and can be exported for other stacks).

```yaml
Outputs:
  BucketArn:
    Description: ARN of the bucket
    Value: !GetAtt MyBucket.Arn
```

### 16.5.4 🗺 Mappings

A **lookup table** inside the template.

```yaml
Mappings:
  RegionMap:
    ap-south-1:
      AMI: ami-0aaa1111bbb2222cc
    us-east-1:
      AMI: ami-0ddd3333eee4444ff
```

Used with `!FindInMap`. (The AMI IDs above are only examples.)

### 16.5.5 ❓ Conditions

Create resources **only when a condition is true**.

```yaml
Conditions:
  IsProd: !Equals [!Ref Environment, prod]

Resources:
  ProdOnlyBucket:
    Type: AWS::S3::Bucket
    Condition: IsProd
```

---

## 16.6 🧮 Intrinsic Functions

**Intrinsic Functions** are built-in functions used **inside templates**.

| Function              | Short Form  | What It Does                                          |
| --------------------- | ----------- | ----------------------------------------------------- |
| `Fn::Ref`             | `!Ref`      | Returns a parameter value or a resource's main ID     |
| `Fn::GetAtt`          | `!GetAtt`   | Returns an attribute of a resource (like ARN, DNS name)|
| `Fn::Sub`             | `!Sub`      | Replaces variables inside a string                    |
| `Fn::Join`            | `!Join`     | Joins values into one string                          |
| `Fn::FindInMap`       | `!FindInMap`| Reads a value from a Mapping                          |
| `Fn::If`              | `!If`       | Chooses a value using a condition                     |
| `Fn::ImportValue`     | `!ImportValue` | Imports an exported value from another stack       |
| `Fn::Select`          | `!Select`   | Picks one item from a list                            |
| `Fn::GetAZs`          | `!GetAZs`   | Returns the Availability Zones of a Region            |

#### 💻 Examples

```yaml
# !Ref → value of a parameter
InstanceType: !Ref InstanceType

# !GetAtt → an attribute of a resource
Value: !GetAtt MyBucket.Arn

# !Sub → replace variables in a string
BucketName: !Sub "my-app-${AWS::AccountId}-${AWS::Region}"

# !Join → join pieces
Value: !Join ["-", [app, !Ref Environment, bucket]]
```

#### 🧠 Easy Memory

```text
!Ref     = Give me the ID / parameter value
!GetAtt  = Give me a specific attribute (ARN, DNS name ...)
!Sub     = Put variables inside a string
```

### 16.6.1 🌐 Pseudo Parameters

Built-in values available in every template.

| Pseudo Parameter      | Value                                   |
| --------------------- | --------------------------------------- |
| `AWS::Region`         | The Region where the stack is created   |
| `AWS::AccountId`      | The AWS account ID                      |
| `AWS::StackName`      | The name of the stack                   |
| `AWS::StackId`        | The ID of the stack                     |

---

## 16.7 💻 Template Examples

### 16.7.1 🪣 Example 1: Simple S3 Bucket

```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: Create an S3 bucket with versioning

Parameters:
  BucketName:
    Type: String
    Description: A globally unique bucket name

Resources:
  MyBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Ref BucketName
      VersioningConfiguration:
        Status: Enabled

Outputs:
  BucketArn:
    Description: ARN of the bucket
    Value: !GetAtt MyBucket.Arn
```

### 16.7.2 🖥 Example 2: EC2 Instance with Security Group

```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: EC2 web server with a security group

Parameters:
  InstanceType:
    Type: String
    Default: t3.micro
    AllowedValues: [t3.micro, t3.small]

  LatestAmiId:
    Type: AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>
    Default: /aws/service/ami-amazon-linux-latest/al2023-ami-kernel-default-x86_64

Resources:
  WebSecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow HTTP
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0

  WebServer:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: !Ref InstanceType
      ImageId: !Ref LatestAmiId
      SecurityGroupIds:
        - !GetAtt WebSecurityGroup.GroupId
      UserData:
        Fn::Base64: |
          #!/bin/bash
          dnf install -y httpd
          systemctl enable --now httpd
          echo "Hello from CloudFormation" > /var/www/html/index.html
      Tags:
        - Key: Name
          Value: !Sub "${AWS::StackName}-web"

Outputs:
  InstanceId:
    Description: ID of the web server
    Value: !Ref WebServer
  PublicIP:
    Description: Public IP address
    Value: !GetAtt WebServer.PublicIp
```

#### 📖 Understanding It

```text
Parameters   → InstanceType and the latest Amazon Linux AMI (read from SSM Parameter Store)
Resources    → A Security Group and an EC2 instance that uses it
!Ref / !GetAtt → Connect resources together
Outputs      → Shows the instance ID and public IP after creation
```

#### ⚠ Important

> **CloudFormation figures out the order by itself.** The Security Group is created first because the EC2 instance depends on it (through `!GetAtt`).

### 16.7.3 🗄 Example 3: DynamoDB Table

```yaml
Resources:
  StudentsTable:
    Type: AWS::DynamoDB::Table
    Properties:
      TableName: Students
      BillingMode: PAY_PER_REQUEST
      AttributeDefinitions:
        - AttributeName: StudentID
          AttributeType: S
      KeySchema:
        - AttributeName: StudentID
          KeyType: HASH
```

---

## 16.8 📚 Stacks

A **Stack** is a **collection of AWS resources** created and managed from **one template**.

#### 🔄 Stack Lifecycle

```text
📝 Template
     │
     ▼
🚀 Create Stack  ──► 🏗️ Resources are created
     │
     ▼
✏️ Update Stack  ──► Resources are changed (using the updated template)
     │
     ▼
🗑️ Delete Stack  ──► All resources of the stack are deleted
```

### 16.8.1 🚦 Common Stack Statuses

| Status                    | Meaning                                              |
| ------------------------- | ---------------------------------------------------- |
| `CREATE_IN_PROGRESS`      | Stack is being created                               |
| `CREATE_COMPLETE`         | ✅ Stack created successfully                        |
| `CREATE_FAILED`           | ❌ A resource failed to create                       |
| `ROLLBACK_IN_PROGRESS`    | Creation failed, AWS is removing created resources   |
| `ROLLBACK_COMPLETE`       | Rollback finished (stack must be deleted and recreated) |
| `UPDATE_COMPLETE`         | ✅ Update finished successfully                      |
| `UPDATE_ROLLBACK_COMPLETE`| Update failed and old state was restored             |
| `DELETE_COMPLETE`         | Stack deleted                                        |

### 16.8.2 🔁 Automatic Rollback

If **creating a stack fails**, CloudFormation **rolls back** by default — it **deletes the resources it already created**.

```text
🚀 Create Stack
     │
     ├── ✅ Resource 1 created
     ├── ✅ Resource 2 created
     └── ❌ Resource 3 fails
              ↓
     🔁 Rollback: Resource 1 and 2 are deleted
```

#### 💡 Tip

> For debugging, we can choose **"Preserve successfully provisioned resources"** (disable rollback) to inspect what was created.

---

## 16.9 🔄 Change Sets

A **Change Set** is a **preview of the changes** CloudFormation will make **before we update a stack**.

```text
📝 Updated Template
        ↓
🔄 Create Change Set
        ↓
👀 Review: what will be Added / Modified / Removed
        ↓
✅ Execute  (or ❌ Cancel)
```

#### 🎯 Why Use It?

- 👀 See the impact before changing production
- ⚠️ Avoid surprise **replacements** (resource deleted and recreated)

#### ⚠ Update Behaviors

| Behavior                  | Meaning                                                      |
| ------------------------- | ------------------------------------------------------------ |
| 🟢 **No interruption**    | Resource updated with no downtime                            |
| 🟡 **Some interruption**  | Resource may be briefly unavailable                          |
| 🔴 **Replacement**        | Old resource is deleted and a **new one is created** (data may be lost!) |

> **Always check a Change Set to see if any resource will be "Replaced".**

---

## 16.10 🛡 Protecting Resources

### 16.10.1 🗑 DeletionPolicy

Controls **what happens to a resource when the stack is deleted**.

```text
🗑️ DeletionPolicy
│
├── Delete   → Resource is deleted (default for most)
├── Retain   → Resource is kept
└── Snapshot → Take a snapshot, then delete (for RDS, EBS ...)
```

#### 💻 Example

```yaml
Resources:
  ImportantBucket:
    Type: AWS::S3::Bucket
    DeletionPolicy: Retain

  Database:
    Type: AWS::RDS::DBInstance
    DeletionPolicy: Snapshot
    # ... properties
```

#### ⚠ Important

> **An S3 bucket that is not empty cannot be deleted by CloudFormation.** Empty it first, or the stack deletion will fail.

### 16.10.2 🔒 Termination Protection

When enabled, the stack **cannot be deleted by mistake**.

### 16.10.3 📜 Stack Policy

A **JSON policy** that **prevents updates** to selected resources in a stack (protects critical resources during updates).

---

## 16.11 🔍 Drift Detection

**Drift** happens when someone **changes a resource manually** (console/CLI) so it **no longer matches the template**.

```text
📝 Template says: Security Group allows port 80 only
👤 Someone adds port 22 manually in the console
        ↓
🔍 Drift Detection → Reports: "DRIFTED"
```

#### 🎯 Used For

- 🕵️ Finding manual changes
- 📋 Keeping infrastructure consistent with code

#### 💡 Best Practice

> **Do not change CloudFormation-managed resources manually.** Change the template and update the stack.

---

## 16.12 🧩 Nested Stacks and Cross-Stack References

### 16.12.1 🧩 Nested Stacks

A template can **include other templates** as resources (`AWS::CloudFormation::Stack`).

```text
📚 Parent Stack
   ├── 📚 Nested Stack: Network (VPC, Subnets)
   ├── 📚 Nested Stack: Security (IAM, Security Groups)
   └── 📚 Nested Stack: App (EC2, ASG, ALB)
```

#### 🎯 Used For

- 📦 Reusing common templates
- 🧹 Keeping big templates small and organized
- 📏 Working around template and resource limits

### 16.12.2 🔗 Cross-Stack References (Export / Import)

One stack **exports** a value, another stack **imports** it.

```text
📚 Network Stack                 📚 App Stack
   Outputs:                         Resources:
     VpcId  ──── Export ────►          Uses  !ImportValue  NetworkVpcId
```

```yaml
# Network stack
Outputs:
  VpcId:
    Value: !Ref MyVPC
    Export:
      Name: NetworkVpcId

# App stack
VpcId: !ImportValue NetworkVpcId
```

#### ⚠ Important

> **A stack cannot be deleted while another stack imports its exported value.**

### 16.12.3 🆚 Nested Stacks vs Cross-Stack References

| 🧩 Nested Stacks                          | 🔗 Cross-Stack References                  |
| ----------------------------------------- | ------------------------------------------ |
| Reuse a template inside another           | Share values between independent stacks    |
| Parent controls child lifecycle           | Stacks are managed separately              |
| Good for reusable components              | Good for shared layers (network, security) |

---

## 16.13 🌍 StackSets

A **StackSet** lets us **deploy the same stack to multiple AWS accounts and Regions** with one operation.

```text
🌍 StackSet (one template)
   ├──► ☁️ Account A — Mumbai
   ├──► ☁️ Account A — Singapore
   ├──► ☁️ Account B — Mumbai
   └──► ☁️ Account C — N. Virginia
```

#### 🎯 Used For

- 🏢 Company-wide **IAM roles and security settings**
- 📊 Turning on **logging/monitoring** in all accounts
- 🛡️ Applying **standard guardrails**

> **StackSet = One template → many accounts and Regions**

---

## 16.14 ⌨ CloudFormation CLI Commands

| Command                                      | What It Does                                |
| -------------------------------------------- | ------------------------------------------- |
| `aws cloudformation validate-template`       | Check the template syntax                   |
| `aws cloudformation create-stack`            | Create a stack                              |
| `aws cloudformation describe-stacks`         | Show stack details and outputs              |
| `aws cloudformation describe-stack-events`   | Show events (useful for errors)             |
| `aws cloudformation update-stack`            | Update a stack                              |
| `aws cloudformation deploy`                  | Create or update a stack (easy command)     |
| `aws cloudformation delete-stack`            | Delete a stack and its resources            |
| `aws cloudformation create-change-set`       | Preview changes                             |

#### 💻 Example Commands

```bash
# Check the template
aws cloudformation validate-template --template-body file://web.yaml

# Create a stack
aws cloudformation create-stack \
  --stack-name web-dev \
  --template-body file://web.yaml \
  --parameters ParameterKey=InstanceType,ParameterValue=t3.micro \
  --capabilities CAPABILITY_NAMED_IAM

# Easy way: create or update
aws cloudformation deploy \
  --stack-name web-dev \
  --template-file web.yaml \
  --capabilities CAPABILITY_NAMED_IAM

# See outputs
aws cloudformation describe-stacks --stack-name web-dev

# Delete everything
aws cloudformation delete-stack --stack-name web-dev
```

#### ⚠ Important

> If the template creates **IAM resources**, we must acknowledge it with `--capabilities CAPABILITY_IAM` (or `CAPABILITY_NAMED_IAM`).

---

## 16.15 🧰 Helper Tools and Related Services

```text
🧰 Related Tools
│
├── 🎨 Infrastructure Composer → Visual drawing of templates
├── ⚡ AWS SAM                 → Simplified templates for serverless apps (Lambda, API Gateway, DynamoDB)
├── 🧰 AWS CDK                 → Write infrastructure using Python, TypeScript, Java ... (generates CloudFormation)
├── 🔧 cfn-init / helper scripts → Install software on EC2 from the template
└── 📥 IaC Generator / Import  → Bring existing resources under CloudFormation
```

#### 🧠 Easy Memory

```text
📝 CloudFormation = Write templates (YAML/JSON)
⚡ SAM            = Shortcut templates for serverless
🧰 CDK            = Write infrastructure in a programming language
```

---

## 16.16 📏 Important Limits and Facts

| Item                         | Fact                                                  |
| ---------------------------- | ----------------------------------------------------- |
| 📝 Template Formats          | JSON or YAML                                          |
| 🧩 Resources per Template    | Up to 500 resources per stack                         |
| 📏 Template Size             | About 1 MB when uploaded from S3 (smaller limit for direct upload) |
| 💰 Cost of CloudFormation    | Free (pay only for created resources)                 |
| 🌏 Stack Scope               | A stack belongs to one Region and one account         |

> 💡 Limits can change. Check AWS documentation for current values.

---

## 16.17 🆚 CloudFormation vs Terraform

Both are **Infrastructure as Code** tools.

| Feature            | 🏗️ CloudFormation                    | 🌍 Terraform                               |
| ------------------ | ------------------------------------ | ------------------------------------------ |
| Made by            | AWS                                  | HashiCorp                                  |
| Works with         | **AWS only**                         | **Many clouds** (AWS, Azure, GCP ...)      |
| Language           | JSON / YAML                          | HCL (HashiCorp Configuration Language)     |
| State Management   | AWS manages the state                | We manage the **state file**               |
| Cost               | Free                                 | Open source (paid versions available)      |
| New AWS features   | Usually supported early              | Provider updates needed                    |

#### 🧠 Easy Memory

```text
🏗️ CloudFormation = AWS-only IaC, AWS manages state
🌍 Terraform       = Multi-cloud IaC, we manage state
```

---

## 16.18 💰 CloudFormation Pricing

```text
💰 CloudFormation Cost
│
├── 🏗️ CloudFormation itself → FREE for AWS resource types
└── 💳 Resources it creates  → Normal AWS charges (EC2, RDS, NAT Gateway ...)
```

#### 💡 Cost Tips

- 🧹 **Delete test stacks** when finished to stop charges
- 🧪 Use small instance types for dev stacks

---

## 16.19 🏗 Real Example: Deploy a Web Application Stack

### 🎯 Requirement

Create the same **web environment** for **dev** and **prod** without manual clicking.

### 🏗 What the Template Builds

```text
📝 web-app.yaml
        │
        ▼
📚 Stack
   ├── 🌐 VPC + Subnets + Internet Gateway
   ├── 🛡️ Security Groups
   ├── 🎭 IAM Role + Instance Profile
   ├── 🖥️ EC2 Launch Template + Auto Scaling Group
   ├── ⚖️ Application Load Balancer + Target Group
   └── 🗄️ RDS Database (DeletionPolicy: Snapshot)
```

### 🪜 Steps

```text
1. Write the template (use Parameters for Environment and InstanceType)
2. Validate it:   aws cloudformation validate-template ...
3. Create the dev stack:
     aws cloudformation deploy --stack-name app-dev ... Environment=dev InstanceType=t3.micro
4. Test the application using the ALB DNS name from Outputs
5. Create the prod stack from the same template:
     aws cloudformation deploy --stack-name app-prod ... Environment=prod InstanceType=m5.large
6. To change something → update the template → create a Change Set → execute
7. When finished with dev → aws cloudformation delete-stack --stack-name app-dev
8. ✅ Everything is removed cleanly
```

### ✅ Benefits

```text
🔁 Same template for dev and prod
📝 Template is stored in Git (version control)
👀 Change Sets show changes before applying
🧹 One command deletes the whole environment
```

---

## 📌🧠 CloudFormation Quick Revision

```text
🏗️ CloudFormation
│
├── 🧱 Basics
│   ├── 📝 Template (YAML / JSON)
│   ├── 📚 Stack
│   └── 🧩 Resources
│
├── 📝 Template Sections
│   ├── Parameters
│   ├── Mappings
│   ├── Conditions
│   ├── Resources (required)
│   └── Outputs
│
├── 🧮 Functions
│   ├── !Ref
│   ├── !GetAtt
│   ├── !Sub
│   ├── !Join
│   └── !ImportValue
│
├── 🔄 Changes
│   ├── Update Stack
│   ├── Change Set
│   └── Rollback
│
├── 🛡️ Protection
│   ├── DeletionPolicy (Delete / Retain / Snapshot)
│   ├── Termination Protection
│   └── Stack Policy
│
├── 🔍 Drift Detection
│
├── 🧩 Reuse
│   ├── Nested Stacks
│   ├── Export / Import
│   └── 🌍 StackSets
│
└── 🧰 Related
    ├── SAM
    ├── CDK
    └── Terraform (alternative)
```

---

## 🧠⚡ CloudFormation One-Line Memory

| Concept                      | Easy Memory                                         |
| ---------------------------- | --------------------------------------------------- |
| 🏗️ **CloudFormation**        | Infrastructure as Code Service of AWS               |
| 📝 **Template**              | The Blueprint (YAML or JSON)                        |
| 📚 **Stack**                 | Resources Created From a Template, Managed Together |
| 🧩 **Resources**             | The Only Required Section                           |
| 🎛️ **Parameters**            | Inputs to Reuse a Template                          |
| 📤 **Outputs**               | Values Shown (or Exported) After Creation           |
| 🔗 **!Ref**                  | Give Me the ID or Parameter Value                   |
| 🔗 **!GetAtt**               | Give Me an Attribute (ARN, DNS ...)                 |
| 🔗 **!Sub**                  | Put Variables Inside a String                       |
| 🔄 **Change Set**            | Preview Before Updating                             |
| 🔁 **Rollback**              | Undo Resources if Creation Fails                    |
| 🔍 **Drift**                 | Manual Change That Does Not Match the Template      |
| 🗑️ **DeletionPolicy**        | Delete, Retain or Snapshot on Stack Deletion        |
| 🧩 **Nested Stack**          | Template Inside a Template                          |
| 🌍 **StackSet**              | One Template to Many Accounts and Regions           |
| 💰 **Pricing**               | Free, Pay for the Created Resources                 |

---

## 🗺 CloudFormation Learning Map

```text
                        🏗️ CloudFormation
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
   TEMPLATE                  STACK                  CHANGE CONTROL
      │                        │                        │
      ├── Parameters           ├── Create               ├── Change Sets
      ├── Mappings             ├── Update               ├── Rollback
      ├── Conditions           ├── Delete               ├── Drift Detection
      ├── Resources            └── Status               └── Stack Policy
      ├── Outputs
      └── Functions
           ├── !Ref
           ├── !GetAtt
           └── !Sub
      │
      ▼
   REUSE & SCALE
      │
      ├── Nested Stacks
      ├── Export / Import
      └── StackSets
      │
      ▼
   RELATED TOOLS
      │
      ├── SAM
      ├── CDK
      └── Terraform
```

---

## ⭐ CloudFormation Final Memory

```text
CloudFormation
 │
 ├── What is it?
 │      └── Infrastructure as Code (AWS)
 │
 ├── What do we write?
 │      └── Template (YAML / JSON)
 │
 ├── What does AWS create from it?
 │      └── Stack
 │
 ├── Which section is required?
 │      └── Resources
 │
 ├── How to reuse a template for dev and prod?
 │      └── Parameters
 │
 ├── How to preview changes?
 │      └── Change Set
 │
 ├── What if creation fails?
 │      └── Automatic Rollback
 │
 ├── How to find manual changes?
 │      └── Drift Detection
 │
 ├── How to keep a resource when the stack is deleted?
 │      └── DeletionPolicy: Retain
 │
 └── How to deploy to many accounts and Regions?
        └── StackSets
```

---

# 🧩 PART 17 — Putting It All Together

> Comparisons, full architectures and a production checklist using all the services.

---

## 17.1 🧩 Service Categories — Big Picture

```text
☁️ AWS Services in These Notes
│
├── 🔐 Security
│   └── IAM
│
├── 🌐 Networking and Content Delivery
│   ├── VPC
│   ├── Route 53
│   ├── CloudFront
│   └── API Gateway
│
├── 🖥️ Compute
│   ├── EC2
│   ├── Lambda
│   └── Elastic Beanstalk
│
├── 🪣 Storage
│   └── S3
│
├── 🗄️ Database
│   ├── RDS
│   └── DynamoDB
│
├── 📨 Application Integration (Messaging)
│   ├── SQS
│   └── SNS
│
└── 🛠️ Management and Governance
    ├── CloudWatch
    └── CloudFormation
```

#### 📊 One Table for All Services

| Service                | Category        | What It Does (Simple)                         |
| ---------------------- | --------------- | --------------------------------------------- |
| 🔐 **IAM**             | Security        | Controls who can do what                      |
| 🌐 **VPC**             | Networking      | Our own private network                       |
| 🧭 **Route 53**        | Networking      | DNS — domain name to IP                       |
| 🌍 **CloudFront**      | Networking / CDN| Caches content near users                     |
| 🚪 **API Gateway**     | Networking / API| Front door for APIs                           |
| 🖥️ **EC2**             | Compute         | Virtual servers                               |
| ⚡ **Lambda**          | Compute         | Run code without servers                      |
| 🌱 **Elastic Beanstalk**| Compute (PaaS) | Upload code, AWS builds the environment       |
| 🪣 **S3**              | Storage         | Object storage                                |
| 🗄️ **RDS**             | Database        | Managed relational (SQL) database             |
| ⚡ **DynamoDB**        | Database        | Serverless NoSQL database                     |
| 📬 **SQS**             | Messaging       | Message queue (pull)                          |
| 📢 **SNS**             | Messaging       | Pub/sub notifications (push)                  |
| 📊 **CloudWatch**      | Management      | Monitoring, logs and alarms                   |
| 🏗️ **CloudFormation**  | Management      | Infrastructure as Code                        |

---

## 17.2 ⚖ Compute Comparison: EC2 vs Lambda vs Elastic Beanstalk

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

## 17.3 🗄 Database Comparison: RDS vs DynamoDB

| Feature              | 🗄️ RDS                              | ⚡ DynamoDB                         |
| -------------------- | ----------------------------------- | ---------------------------------- |
| Type                 | Relational (SQL)                    | NoSQL (key-value / document)       |
| Schema               | Fixed                               | Flexible (only key fixed)          |
| Servers              | DB instances (AWS-managed)          | Serverless                         |
| Scaling              | Scale up + read replicas            | Automatic, almost unlimited        |
| Joins                | ✅ Yes                              | ❌ No                              |
| Access               | User/password + port                | IAM + HTTPS API                    |
| Best for             | Complex queries, relationships      | Simple, huge-scale lookups         |

---

## 17.4 📨 Messaging Comparison: SQS vs SNS

| Feature                  | 📬 SQS                              | 📢 SNS                                 |
| ------------------------ | ----------------------------------- | -------------------------------------- |
| Model                    | Queue                               | Publish / Subscribe                    |
| Delivery                 | **Pull** (consumer polls)           | **Push** (SNS sends)                   |
| Receivers                | One consumer processes each message | Many subscribers get each message      |
| Stores messages?         | ✅ Yes (up to 14 days)              | ❌ No (delivers immediately)           |
| Best for                 | Decoupling and buffering            | Notifications and fan-out              |

#### 🧠 Easy Memory

```text
📬 SQS = Mailbox      (store and pick up)
📢 SNS = Loudspeaker  (announce to everyone)
📢 + 📬 = Fan-out     (SNS sends to many SQS queues)
```

---

## 17.5 🌍 Delivery Comparison: Route 53 vs CloudFront vs API Gateway

| Service            | Main Job                                          |
| ------------------ | ------------------------------------------------- |
| 🧭 **Route 53**    | Turns a **domain name** into the right address    |
| 🌍 **CloudFront**  | **Caches and delivers content** from edge locations |
| 🚪 **API Gateway** | Receives **API requests** and sends them to a backend |

```text
👤 User
   ↓
🧭 Route 53       → "Where is www.example.com?"
   ↓
🌍 CloudFront     → "Here is the cached page / forward to origin"
   ↓
🚪 API Gateway    → "Handle this API call"
   ↓
⚡ Lambda / 🖥️ EC2 → "Do the work"
```

---

## 17.6 📊 Monitoring and Management Comparison

| Service              | Question It Answers                          |
| -------------------- | -------------------------------------------- |
| 📊 **CloudWatch**    | How is my resource **performing**? (metrics, logs, alarms) |
| 🕵️ **CloudTrail**    | **Who did what** in my account?              |
| 🗂️ **AWS Config**    | **What changed** in my configuration?        |
| 🏗️ **CloudFormation**| Build and manage resources **from code**     |

---

## 17.7 🏗 Architecture A: Traditional 3-Tier Web Application

This design uses **servers (EC2)** and a **relational database (RDS)**.

```text
                           👤 User
                             │
                             ▼
                    🧭 Route 53 (DNS)
                             │
                             ▼
                    🌍 CloudFront (CDN)  ◄──── 🪣 S3 (images, static files)
                             │
                             ▼
┌───────────────────────── 🌐 VPC ──────────────────────────────┐
│                            │                                   │
│   ┌─────────── 🌍 Public Subnets ───────────────────────┐      │
│   │        ⚖️ Application Load Balancer                  │      │
│   └──────────────────────┬──────────────────────────────┘      │
│                          │                                     │
│   ┌─────────── 🔒 Private Subnets ──────────────────────┐      │
│   │   🖥️ EC2 (Auto Scaling Group)  ◄── 🎭 IAM Role       │      │
│   │              │                                       │      │
│   │              ▼                                       │      │
│   │   🗄️ RDS (Multi-AZ)                                  │      │
│   └──────────────────────────────────────────────────────┘      │
└─────────────────────────────────────────────────────────────────┘
                             │
                             ▼
              📊 CloudWatch (metrics, logs, alarms)
                             │
                             ▼
              📢 SNS ──► 📧 Email alert to the team
```

#### 📖 Story of One Request

```text
1. 👤 User opens www.example.com
2. 🧭 Route 53 points to the CloudFront distribution
3. 🌍 CloudFront returns cached files, or forwards the request to the Load Balancer
4. ⚖️ Load Balancer sends the request to a healthy EC2 server
5. 🖥️ EC2 reads/writes data in 🗄️ RDS (private subnet)
6. 🖥️ EC2 uses its 🎭 IAM Role to read files from 🪣 S3
7. 📊 CloudWatch watches CPU and errors
8. 🚨 If CPU is high → alarm → 📈 Auto Scaling adds servers + 📢 SNS emails the team
```

> 🌱 **Elastic Beanstalk** can create and manage the Load Balancer, Auto Scaling and EC2 part of this design for us.

---

## 17.8 ⚡ Architecture B: Serverless Application

This design has **no servers to manage**.

```text
                     👤 User
                        │
          ┌─────────────┴─────────────┐
          ▼                           ▼
   🧭 Route 53                 🧭 Route 53
   (www.example.com)           (api.example.com)
          │                           │
          ▼                           ▼
   🌍 CloudFront              🚪 API Gateway
          │                           │ (Cognito / IAM authorizer)
          ▼                           ▼
   🪣 S3 (private,            ⚡ Lambda Function
      static website)                 │
                                      ▼
                              ⚡ DynamoDB Table
                                      │
                                      ▼
                         🔄 DynamoDB Stream ──► ⚡ Lambda (reacts to changes)

   📊 CloudWatch → Logs and metrics for Lambda, API Gateway and DynamoDB
```

#### 📖 Story of One Request

```text
1. 👤 User opens the website → 🌍 CloudFront serves the files from 🪣 S3
2. 📱 The web app calls api.example.com
3. 🚪 API Gateway checks the user's token (authorizer)
4. ⚡ Lambda runs the business logic
5. ⚡ DynamoDB stores or returns the data
6. 📊 CloudWatch records logs and metrics
7. 🔐 IAM roles control what each Lambda can access
```

#### ✅ Benefits

```text
💰 Pay only for use (no idle cost)
📈 Scales automatically
🛠️ No server patching
```

---

## 17.9 🔄 Architecture C: Event-Driven and Decoupled

This design uses **messaging** to connect services safely.

```text
👤 Customer places an order
        │
        ▼
🚪 API Gateway ──► ⚡ Lambda (Order Service)
                         │ publish
                         ▼
                  📢 SNS Topic: new-order
                         │
      ┌──────────────────┼───────────────────┐
      ▼                  ▼                   ▼
 📬 SQS: inventory   📬 SQS: payment      📧 Email
      │                  │               (confirmation)
      ▼                  ▼
 ⚡ Lambda           🖥️ Worker (EC2 ASG)
 (update stock)      (process payment)
      │                  │
      ▼                  ▼
 ⚡ DynamoDB         🗄️ RDS

 ☠️ Each SQS queue has a Dead-Letter Queue for failed messages
 📊 CloudWatch alarm on queue length → scales the workers
```

#### ⭐ Why This Design Is Good

```text
🔗 Services are loosely coupled (one failure does not stop everything)
🛡️ SQS buffers traffic spikes
🔀 SNS fan-out sends one event to many services
☠️ DLQ keeps failed messages for checking
📈 Workers scale with the queue length
```

---

## 17.10 🏗 CloudFormation: Building Everything From Code

Any of the architectures above can be **created from a CloudFormation template**.

```text
📝 template.yaml
        │
        ▼
🏗️ CloudFormation Stack
   ├── 🔐 IAM Roles
   ├── 🌐 VPC, Subnets, Gateways
   ├── 🖥️ EC2 / ⚡ Lambda / 🌱 Beanstalk
   ├── 🗄️ RDS / ⚡ DynamoDB
   ├── 🪣 S3 / 🌍 CloudFront
   ├── 🚪 API Gateway
   ├── 📬 SQS / 📢 SNS
   ├── 📊 CloudWatch Alarms
   └── 🧭 Route 53 Records
```

#### ✅ Benefits

```text
🔁 Same setup for dev, test and prod
📝 Templates stored in Git
🧹 Delete the stack → everything is cleaned up
```

---

## 17.11 ✅ Production Checklist

```text
✅ Security
├── 🔐 Use IAM roles (not access keys) for EC2 and Lambda
├── 📲 Enable MFA on the root user and admins
├── 🔒 Keep databases in private subnets
├── 🛡️ Use Security Groups with least privilege
└── 🔒 Enable encryption (S3, RDS, DynamoDB, SQS, SNS)

✅ Reliability
├── 🛡️ Use Multi-AZ for RDS
├── 📈 Use Auto Scaling and Load Balancers
├── ☠️ Use Dead-Letter Queues
└── 📸 Enable backups (RDS, DynamoDB PITR, S3 versioning)

✅ Monitoring
├── 📊 CloudWatch alarms on key metrics
├── 📝 Set log retention
└── 📢 Alerts through SNS

✅ Cost
├── 🗑️ Delete unused resources
├── 🔁 Watch NAT Gateways, Load Balancers, Elastic IPs
├── 💰 Use lifecycle rules and right-sized instances
└── 🔔 Set a billing alarm / budget

✅ Operations
├── 🏗️ Use CloudFormation for repeatable infrastructure
└── 🕵️ Turn on CloudTrail
```

---

# 📌🧠 Complete AWS Quick Revision

```text
☁️ AWS
│
├── 🔐 IAM
│   ├── User, Group, Role, Policy
│   ├── MFA, Least Privilege
│   └── Explicit Deny > Allow > Default Deny
│
├── 🌐 VPC
│   ├── CIDR, Subnet (Public / Private), Route Table
│   ├── Internet Gateway, NAT Gateway
│   └── Security Group, NACL, Peering, Endpoints
│
├── 🖥️ EC2
│   ├── AMI, Instance Type, Key Pair, Security Group
│   ├── EBS, Elastic IP
│   ├── Load Balancer, Target Group, Auto Scaling
│   └── Pricing: On-Demand, Reserved, Savings Plans, Spot
│
├── 🪣 S3
│   ├── Bucket, Object, Key, Storage Classes
│   ├── Versioning, Lifecycle, Replication
│   └── Security and Encryption
│
├── 🗄️ RDS
│   ├── Engines, Instance Class, Endpoint
│   ├── Multi-AZ, Read Replica
│   └── Backups, Snapshots, Encryption
│
├── ⚡ DynamoDB
│   ├── Table, Item, Partition Key, Sort Key
│   ├── Provisioned vs On-Demand
│   ├── GSI, LSI, Query vs Scan
│   └── Streams, TTL, DAX, Global Tables
│
├── ⚡ Lambda
│   ├── Function, Trigger, Event
│   ├── Execution Role
│   └── 15 min limit, Cold Start, Concurrency
│
├── 🌱 Elastic Beanstalk
│   ├── Application, Version, Environment
│   ├── Web Tier, Worker Tier
│   └── Deployment Policies
│
├── 🧭 Route 53
│   ├── Hosted Zone, Records, Alias
│   ├── Routing Policies
│   └── Health Checks
│
├── 🌍 CloudFront
│   ├── Distribution, Origin, Edge Location
│   ├── TTL, Invalidation
│   └── OAC, Signed URLs, ACM (us-east-1)
│
├── 🚪 API Gateway
│   ├── REST, HTTP, WebSocket APIs
│   ├── Stage, Deployment, Integration
│   └── Authorizers, Throttling, Caching
│
├── 📬 SQS
│   ├── Standard vs FIFO
│   ├── Visibility Timeout, Long Polling
│   └── Dead-Letter Queue
│
├── 📢 SNS
│   ├── Topic, Publisher, Subscriber
│   ├── Fan-out, Filter Policy
│   └── Standard vs FIFO Topic
│
├── 📊 CloudWatch
│   ├── Metrics, Alarms, Logs
│   ├── CloudWatch Agent, Dashboards
│   └── EventBridge
│
└── 🏗️ CloudFormation
    ├── Template, Stack, Parameters, Outputs
    ├── Change Set, Rollback, Drift
    └── Nested Stacks, StackSets
```

---

# 🧠⚡ Complete AWS One-Line Memory

| Service                  | Easy Memory                                         |
| ------------------------ | --------------------------------------------------- |
| ☁️ **AWS**               | Rent IT services and pay as you use                 |
| 🔐 **IAM**               | Controls Who Can Do What                            |
| 🌐 **VPC**               | Our Own Private Network                             |
| 🚪 **Internet Gateway**  | Gate of VPC to the Internet                         |
| 🔁 **NAT Gateway**       | Private Servers Go Out, Nobody Comes In             |
| 🛡️ **Security Group**    | Firewall for Instance (Stateful)                    |
| 🚧 **NACL**              | Firewall for Subnet (Stateless)                     |
| 🖥️ **EC2**               | Virtual Server                                      |
| 📦 **AMI**               | Server Template                                     |
| 💾 **EBS**               | Persistent Disk for EC2                             |
| ⚖️ **Load Balancer**     | Distributes Traffic                                 |
| 📈 **Auto Scaling**      | Automatically Adjusts Number of Servers             |
| 🪣 **S3**                | Object Storage                                      |
| 🗄️ **RDS**               | Managed Relational Database                         |
| 🛡️ **Multi-AZ**          | Standby Copy for Failover                           |
| 📖 **Read Replica**      | Read-Only Copy for Speed                            |
| ⚡ **DynamoDB**          | Serverless NoSQL Database                           |
| 🔑 **Partition Key**     | Decides Where a DynamoDB Item Is Stored             |
| ⚡ **Lambda**            | Run Code Without Servers (Max 15 Minutes)           |
| 🔔 **Trigger**           | Event That Starts a Lambda Function                 |
| 🌱 **Elastic Beanstalk** | Upload Code, AWS Builds the Environment             |
| 🧭 **Route 53**          | DNS Service (Name → IP)                             |
| 🔗 **Alias Record**      | Point Root Domain to AWS Resource                   |
| ❤️ **Health Check**      | Checks if Server is Healthy                         |
| 🌍 **CloudFront**        | CDN — Cache Content Near Users                      |
| 🛡️ **OAC**               | Private S3 Bucket That Only CloudFront Can Read     |
| 🚪 **API Gateway**       | Secure Front Door for APIs                          |
| 🚦 **Throttling**        | Limit Requests (Returns 429)                        |
| 📬 **SQS**               | Message Queue (Pull Model)                          |
| ⏱️ **Visibility Timeout**| Time a Received Message Stays Hidden                |
| ☠️ **Dead-Letter Queue** | Parking Place for Failed Messages                   |
| 📢 **SNS**               | Pub/Sub Notifications (Push Model)                  |
| 🔀 **Fan-out**           | One Message to Many Places (SNS + SQS)              |
| 📊 **CloudWatch**        | Monitoring: Metrics, Logs, Alarms                   |
| 🚨 **Alarm**             | Watches a Metric and Takes Action                   |
| 🕵️ **CloudTrail**        | Who Did What                                        |
| 🏗️ **CloudFormation**    | Infrastructure as Code                              |
| 📚 **Stack**             | Resources Created From One Template                 |
| 🔄 **Change Set**        | Preview Before Updating a Stack                     |

---

# 🗺 Complete AWS Learning Map

```text
                                  ☁️ AWS
                                    │
   ┌───────────┬──────────┬─────────┼──────────┬───────────┬───────────┐
   │           │          │         │          │           │           │
   ▼           ▼          ▼         ▼          ▼           ▼           ▼
SECURITY   NETWORKING  COMPUTE   STORAGE   DATABASE   MESSAGING  MANAGEMENT
   │           │          │         │          │           │           │
   └── IAM     ├── VPC    ├── EC2   └── S3     ├── RDS     ├── SQS     ├── CloudWatch
               ├── Route  ├── Lambda           └── Dynamo  └── SNS     └── CloudFormation
               │    53    └── Elastic              DB
               ├── Cloud       Beanstalk
               │   Front
               └── API
                   Gateway
```

### 🪜 Suggested Learning Order (Same as the Order of These Notes)

```text
1️⃣  IAM               → Learn security first
2️⃣  VPC               → Understand networking
3️⃣  EC2               → Launch servers
4️⃣  S3                → Store files
5️⃣  RDS               → Add a relational database
6️⃣  DynamoDB          → Add a NoSQL database
7️⃣  Lambda            → Run code without servers
8️⃣  Elastic Beanstalk → Deploy applications easily
9️⃣  Route 53          → Connect a domain name
🔟  CloudFront        → Deliver content faster
1️⃣1️⃣ API Gateway       → Build APIs
1️⃣2️⃣ SQS               → Decouple with queues
1️⃣3️⃣ SNS               → Send notifications and fan-out
1️⃣4️⃣ CloudWatch        → Monitor everything
1️⃣5️⃣ CloudFormation    → Build everything from code
```

---

# ⭐ Complete AWS Final Memory

```text
AWS
 │
 ├── How to control access?
 │      └── IAM
 │
 ├── How to build a private network?
 │      └── VPC
 │
 ├── How to run a server?
 │      └── EC2
 │
 ├── How to store files?
 │      └── S3
 │
 ├── How to store relational (SQL) data?
 │      └── RDS
 │
 ├── How to store NoSQL data at huge scale?
 │      └── DynamoDB
 │
 ├── How to run code without servers?
 │      └── Lambda
 │
 ├── How to deploy an app easily?
 │      └── Elastic Beanstalk
 │
 ├── How to connect a domain name?
 │      └── Route 53
 │
 ├── How to deliver content faster worldwide?
 │      └── CloudFront
 │
 ├── How to create and protect APIs?
 │      └── API Gateway
 │
 ├── How to decouple services with a queue?
 │      └── SQS
 │
 ├── How to send notifications to many receivers?
 │      └── SNS
 │
 ├── How to monitor and get alerts?
 │      └── CloudWatch
 │
 └── How to build all infrastructure from code?
        └── CloudFormation
```

---

<p align="center">

## ☁ AWS — Build Anything, Scale Everywhere

**Learn → Practice → Build → Deploy → Automate**

</p>
