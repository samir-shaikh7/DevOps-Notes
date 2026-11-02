# 🚀🛠️ DevOps — Complete Notes

<p align="center">

**Git & GitHub • Maven • Jenkins • SonarQube • Nexus • Docker • Kubernetes • Terraform • Ansible • Prometheus • Grafana**

![DevOps](https://img.shields.io/badge/DevOps-Complete%20Notes-blue?style=for-the-badge)
![CI/CD](https://img.shields.io/badge/CI%2FCD-Automation-green?style=for-the-badge)
![Containers](https://img.shields.io/badge/Docker-Kubernetes-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![IaC](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Learning](https://img.shields.io/badge/DevOps-Learning-success?style=for-the-badge)

</p>

---

## 📖 About These Notes

This single file covers **11 core DevOps tools**, in a **logical learning order** (the same order a real project follows).

```text
🌿 Source Code      → Git & GitHub
📦 Build            → Maven
⚙️ CI/CD            → Jenkins
🔍 Code Quality     → SonarQube
🗄️ Artifacts        → Nexus Repository
🐳 Containers       → Docker → Kubernetes
🏗️ Infrastructure   → Terraform → Ansible (create, then configure)
📊 Monitoring       → Prometheus → Grafana
```

The notes follow this flow for every tool:

```text
1. 📖 Definition and Simple Meaning
2. 🤔 Why do we use it?
3. 🧱 Concepts and sub-topics
4. 💻 Commands, examples and diagrams
5. 🏗️ Real example
6. 📌 Quick Revision + 🧠 One-Line Memory + 🗺️ Learning Map + ⭐ Final Memory
```

### 🔄 Complete DevOps Pipeline

```text
Developer
   ↓
Git & GitHub  (store code)
   ↓
Jenkins  (pipeline starts)
   ↓
Maven  (build and test)
   ↓
SonarQube  (quality gate)
   ↓
Nexus  (store artifact)
   ↓
Docker  (build image)
   ↓
Kubernetes  (deploy and scale)
   ↑                    ↑
Terraform           Ansible
(create servers)    (configure servers)
   ↓
Prometheus  (collect metrics)
   ↓
Grafana  (dashboards and alerts)
```

## 📚 Table of Contents

> Click a part to open its list of topics.

<details>
<summary><b>🌿 PART 1 — Git & GitHub — Version Control and Collaboration</b></summary>

- [1.1 🧭 Git & GitHub Fundamentals](#11--git--github-fundamentals)
- [1.2 📦 Git Repository & Working Areas](#12--git-repository--working-areas)
- [1.3 🛠️ Basic Git Commands](#13--basic-git-commands)
- [1.4 🌐 Git Remote & Remote Commands](#14--git-remote--remote-commands)
- [1.5 🌿 Git Branching & HEAD](#15--git-branching--head)
- [1.6 🔀 Branch Integration](#16--branch-integration)
- [1.7 🤝 GitHub Collaboration](#17--github-collaboration)
- [1.8 🚫 `.gitignore`](#18--gitignore)
- [1.9 ↩️ Git History, Undoing Changes & Recovery](#19--git-history-undoing-changes--recovery)
- [1.10 ⚡ Advanced Git Operations](#110--advanced-git-operations)
- [1.11 🔐 GitHub Authentication](#111--github-authentication)
- [1.12 🏷️ Git Tags](#112--git-tags)
- [1.13 ☁️ Git in DevOps](#113--git-in-devops)
- [1.14 🧪 Basic Git Practical](#114--basic-git-practical)
- [1.15 🌍 Real-World Git Workflow](#115--real-world-git-workflow)
- [1.16 ⭐ Advantages & Limitations](#116--advantages--limitations)
- [1.17 ⚡ Quick Revision](#117--quick-revision)
- [📋 Git Command Cheat Sheet](#-git-command-cheat-sheet)
- [⭐ Final Memory](#-final-memory)

</details>

<details>
<summary><b>📦 PART 2 — Maven — Build and Dependency Management</b></summary>

- [2.1 📦 What is Maven?](#21--what-is-maven)
- [2.2 🤔 Why Do We Use Maven?](#22--why-do-we-use-maven)
- [2.3 🧰 What Does Maven Provide?](#23--what-does-maven-provide)
- [2.4 ⚙️ Installation and Setup](#24--installation-and-setup)
- [2.5 📁 Standard Project Structure](#25--standard-project-structure)
- [2.6 📄 pom.xml (Project Object Model)](#26--pomxml-project-object-model)
- [2.7 🏷️ Maven Coordinates (GAV)](#27--maven-coordinates-gav)
- [2.8 🔁 Build Lifecycle](#28--build-lifecycle)
- [2.9 🧩 Plugins and Goals](#29--plugins-and-goals)
- [2.10 📚 Dependencies and Scopes](#210--dependencies-and-scopes)
- [2.11 🌐 Maven Repositories](#211--maven-repositories)
- [2.12 🛠️ settings.xml](#212--settingsxml)
- [2.13 💻 Common Maven Commands](#213--common-maven-commands)
- [2.14 📦 Packaging Types](#214--packaging-types)
- [2.15 🏗️ Multi-Module Projects](#215--multi-module-projects)
- [2.16 🔗 Maven in CI/CD (Jenkins)](#216--maven-in-cicd-jenkins)
- [2.17 🏗️ Real Example: Build and Store a Java App](#217--real-example-build-and-store-a-java-app)
- [2.18 🧯 Troubleshooting](#218--troubleshooting)
- [2.19 📌 Maven Quick Revision](#219--maven-quick-revision)
- [2.20 🧠⚡ Maven One-Line Memory](#220--maven-one-line-memory)
- [2.21 🗺️ Maven Learning Map](#221--maven-learning-map)
- [2.22 ⭐ Maven Final Memory](#222--maven-final-memory)

</details>

<details>
<summary><b>⚙️ PART 3 — Jenkins — CI/CD Automation</b></summary>

- [3.1 ⚙️ Jenkins Fundamentals](#31--jenkins-fundamentals)
- [3.2 ⚙️ CI/CD with Jenkins](#32--cicd-with-jenkins)
- [3.3 🧱 Jenkins Architecture](#33--jenkins-architecture)
- [3.4 ⚙️ Jenkins Installation & Setup](#34--jenkins-installation--setup)
- [3.5 ⏱️ Jenkins UI & Jobs](#35--jenkins-ui--jobs)
- [3.6 🧩 Jenkins Plugins](#36--jenkins-plugins)
- [3.7 🐙 Jenkins + Git / GitHub](#37--jenkins--git--github)
- [🐙 Jenkins + GitHub](#-jenkins--github)
- [3.8 🔔 Jenkins Triggers](#38--jenkins-triggers)
- [3.9 🔗 Jenkins Pipeline Fundamentals](#39--jenkins-pipeline-fundamentals)
- [3.10 🔗 Declarative Pipeline](#310--declarative-pipeline)
- [3.11 📝 Jenkinsfile Advanced Syntax](#311--jenkinsfile-advanced-syntax)
- [3.12 ⚖️ Declarative vs Scripted Pipeline](#312--declarative-vs-scripted-pipeline)
- [3.13 🔤 Jenkins Environment Variables](#313--jenkins-environment-variables)
- [3.14 🔤 Jenkins Parameters](#314--jenkins-parameters)
- [3.15 🔑 Jenkins Credentials](#315--jenkins-credentials)
- [3.16 📦 Jenkins + Maven](#316--jenkins--maven)
- [3.17 📦 Jenkins Artifacts](#317--jenkins-artifacts)
- [3.18 🔗 Jenkins Pipeline from SCM](#318--jenkins-pipeline-from-scm)
- [3.19 🔗 Multibranch Pipeline](#319--multibranch-pipeline)
- [3.20 ⚙️ Jenkins Shared Libraries](#320--jenkins-shared-libraries)
- [3.21 🔐 Jenkins Security](#321--jenkins-security)
- [3.22 ⚙️ Jenkins Failure Handling](#322--jenkins-failure-handling)
- [3.23 ⚙️ Jenkins Administration](#323--jenkins-administration)
- [3.24 🧯 Jenkins Troubleshooting](#324--jenkins-troubleshooting)
- [3.25 🔄 Complete Jenkins CI/CD Workflow](#325--complete-jenkins-cicd-workflow)
- [3.26 🧪 Jenkins Practical Commands](#326--jenkins-practical-commands)
- [3.27 📌 Quick Revision](#327--quick-revision)

</details>

<details>
<summary><b>🔍 PART 4 — SonarQube — Code Quality and Security</b></summary>

- [4.1 🔍 What is SonarQube?](#41--what-is-sonarqube)
- [4.2 🤔 Why Do We Use SonarQube?](#42--why-do-we-use-sonarqube)
- [4.3 🧰 What Does SonarQube Provide?](#43--what-does-sonarqube-provide)
- [4.4 🧱 SonarQube Architecture](#44--sonarqube-architecture)
- [4.5 ⚙️ Installation (Docker Method)](#45--installation-docker-method)
- [4.6 📁 Projects, Tokens and Keys](#46--projects-tokens-and-keys)
- [4.7 🔬 Sonar Scanner](#47--sonar-scanner)
- [4.8 📊 Issue Types and Severity](#48--issue-types-and-severity)
- [4.9 🚦 Quality Gate](#49--quality-gate)
- [4.10 📏 Quality Profiles and Rules](#410--quality-profiles-and-rules)
- [4.11 🆕 New Code vs Overall Code](#411--new-code-vs-overall-code)
- [4.12 🔗 SonarQube with Jenkins](#412--sonarqube-with-jenkins)
- [4.13 🏗️ Real Example: Quality Check Before Deploy](#413--real-example-quality-check-before-deploy)
- [4.14 🧯 Troubleshooting](#414--troubleshooting)
- [4.15 📌 SonarQube Quick Revision](#415--sonarqube-quick-revision)
- [4.16 🧠⚡ SonarQube One-Line Memory](#416--sonarqube-one-line-memory)
- [4.17 🗺️ SonarQube Learning Map](#417--sonarqube-learning-map)
- [4.18 ⭐ SonarQube Final Memory](#418--sonarqube-final-memory)

</details>

<details>
<summary><b>🗄️ PART 5 — Nexus Repository — Artifact Repository Manager</b></summary>

- [5.1 🗄️ What is Nexus Repository?](#51--what-is-nexus-repository)
- [5.2 🤔 Why Do We Use Nexus?](#52--why-do-we-use-nexus)
- [5.3 🧰 What Does Nexus Provide?](#53--what-does-nexus-provide)
- [5.4 🧱 Repository Types](#54--repository-types)
- [5.5 🧬 Repository Formats](#55--repository-formats)
- [5.6 🔁 Release vs Snapshot](#56--release-vs-snapshot)
- [5.7 ⚙️ Installation (Docker Method)](#57--installation-docker-method)
- [5.8 👥 Users, Roles and Privileges](#58--users-roles-and-privileges)
- [5.9 📤 Uploading Artifacts with Maven](#59--uploading-artifacts-with-maven)
- [5.10 📥 Downloading Dependencies from Nexus](#510--downloading-dependencies-from-nexus)
- [5.11 🐳 Docker Registry in Nexus](#511--docker-registry-in-nexus)
- [5.12 🧹 Cleanup Policies and Storage](#512--cleanup-policies-and-storage)
- [5.13 🔗 Nexus in CI/CD](#513--nexus-in-cicd)
- [5.14 🏗️ Real Example: Store and Reuse a Build](#514--real-example-store-and-reuse-a-build)
- [5.15 🧯 Troubleshooting](#515--troubleshooting)
- [5.16 📌 Nexus Quick Revision](#516--nexus-quick-revision)
- [5.17 🧠⚡ Nexus One-Line Memory](#517--nexus-one-line-memory)
- [5.18 🗺️ Nexus Learning Map](#518--nexus-learning-map)
- [5.19 ⭐ Nexus Final Memory](#519--nexus-final-memory)

</details>

<details>
<summary><b>🐳 PART 6 — Docker — Containers</b></summary>

- [6.1 📖 What is Docker?](#61--what-is-docker)
- [6.2 🤔 Why Do We Use Docker?](#62--why-do-we-use-docker)
- [6.3 ⚙️ What Does Docker Provide?](#63--what-does-docker-provide)
- [6.4 ⚙️ What Does Docker Do?](#64--what-does-docker-do)
- [6.5 📖 What is a Container?](#65--what-is-a-container)
- [6.6 📖 What is a Docker Image?](#66--what-is-a-docker-image)
- [6.7 ⚖️ Image vs Container](#67--image-vs-container)
- [6.8 📖 What is Dockerfile?](#68--what-is-dockerfile)
- [6.9 🐳 Docker Engine](#69--docker-engine)
- [6.10 🧱 Docker Architecture](#610--docker-architecture)
- [6.11 🐳 Docker Client / Docker CLI](#611--docker-client--docker-cli)
- [6.12 🗄️ Docker Registry](#612--docker-registry)
- [6.13 🐳 Docker Hub](#613--docker-hub)
- [6.14 💾 Docker Volume](#614--docker-volume)
- [6.15 🌐 Docker Network](#615--docker-network)
- [6.16 🧩 Docker Compose](#616--docker-compose)
- [6.17 🐳 Docker in DevOps](#617--docker-in-devops)
- [6.18 🐳 Docker + Jenkins](#618--docker--jenkins)
- [6.19 🐳 Docker + Kubernetes](#619--docker--kubernetes)
- [6.20 🐳 Docker + AWS](#620--docker--aws)
- [6.21 🔁 Docker Image Lifecycle](#621--docker-image-lifecycle)
- [6.22 💻 Important Docker Commands](#622--important-docker-commands)
- [6.23 💻 Important Dockerfile Example](#623--important-dockerfile-example)
- [6.24 🧪 Basic Docker Practical](#624--basic-docker-practical)
- [6.25 🌍 Real-World Example](#625--real-world-example)
- [6.26 ⭐ Advantages of Docker](#626--advantages-of-docker)
- [6.27 ⭐ Disadvantages of Docker](#627--disadvantages-of-docker)
- [6.28 ⚖️ Docker vs Virtual Machine](#628--docker-vs-virtual-machine)
- [6.29 ⚖️ Dockerfile vs Image vs Container](#629--dockerfile-vs-image-vs-container)
- [6.30 ⚖️ Docker vs Kubernetes](#630--docker-vs-kubernetes)
- [6.31 📌 Quick Revision](#631--quick-revision)
- [6.32 🐳 Docker in DevOps Ecosystem](#632--docker-in-devops-ecosystem)
- [6.33 📌 Docker Quick Revision & Cheat Sheet](#633--docker-quick-revision--cheat-sheet)
- [6.34 🧠 Super Memory Map](#634--super-memory-map)
- [🏆 Docker Super Memory](#-docker-super-memory)

</details>

<details>
<summary><b>☸️ PART 7 — Kubernetes — Container Orchestration</b></summary>

- [7.1 ☸️ Kubernetes Fundamentals](#71--kubernetes-fundamentals)
- [7.2 🧱 Kubernetes Architecture](#72--kubernetes-architecture)
- [7.3 ☸️ Kubernetes Objects and Workloads](#73--kubernetes-objects-and-workloads)
- [7.4 🌐 Kubernetes Networking](#74--kubernetes-networking)
- [7.5 💾 Kubernetes Storage](#75--kubernetes-storage)
- [7.6 🔧 Configuration and Security](#76--configuration-and-security)
- [7.7 ❤️ Health Checks and Probes](#77--health-checks-and-probes)
- [7.8 📅 Scheduling and Scaling](#78--scheduling-and-scaling)
- [7.9 🧪 Practical kubectl Commands](#79--practical-kubectl-commands)
- [7.10 🧪 Complete Practical: Deploy an Application](#710--complete-practical-deploy-an-application)
- [7.11 🧯 Troubleshooting](#711--troubleshooting)
- [7.12 ⚖️ Important Comparisons](#712--important-comparisons)
- [7.13 ⚡ Final Revision: How Everything Connects](#713--final-revision-how-everything-connects)

</details>

<details>
<summary><b>🏗️ PART 8 — Terraform — Infrastructure as Code</b></summary>

- [8.1 📖 What is Terraform?](#81--what-is-terraform)
- [8.2 🤔 Why Do We Use Terraform?](#82--why-do-we-use-terraform)
- [8.3 📖 What is Infrastructure as Code (IaC)?](#83--what-is-infrastructure-as-code-iac)
- [8.4 ⚙️ What Does Terraform Do?](#84--what-does-terraform-do)
- [8.5 🏗️ How Terraform Works](#85--how-terraform-works)
- [8.6 📖 What is HCL?](#86--what-is-hcl)
- [8.7 🔧 Terraform Configuration Files](#87--terraform-configuration-files)
- [8.8 🧰 Terraform Provider](#88--terraform-provider)
- [8.9 🧱 Terraform Resource](#89--terraform-resource)
- [8.10 🔤 Terraform Variable](#810--terraform-variable)
- [8.11 📤 Terraform Output](#811--terraform-output)
- [8.12 📒 Terraform State](#812--terraform-state)
- [8.13 🌐 Terraform Remote State](#813--terraform-remote-state)
- [8.14 🗄️ Terraform Backend](#814--terraform-backend)
- [8.15 📒 State Locking](#815--state-locking)
- [8.16 💻 Terraform State Commands](#816--terraform-state-commands)
- [8.17 🔌 Terraform Data Source](#817--terraform-data-source)
- [8.18 🧱 Terraform Module](#818--terraform-module)
- [8.19 🗄️ Terraform Registry](#819--terraform-registry)
- [8.20 🏗️ Terraform Functions](#820--terraform-functions)
- [8.21 🔀 Conditional Expressions](#821--conditional-expressions)
- [8.22 🏗️ Terraform count](#822--terraform-count)
- [8.23 🏗️ Terraform for_each](#823--terraform-for_each)
- [8.24 🏗️ Terraform Dependency](#824--terraform-dependency)
- [8.25 📌 depends_on](#825--depends_on)
- [8.26 🏗️ Terraform Idempotency](#826--terraform-idempotency)
- [8.27 🏗️ Terraform Drift](#827--terraform-drift)
- [8.28 🏗️ Terraform Locals](#828--terraform-locals)
- [8.29 🔁 Terraform Lifecycle Rules](#829--terraform-lifecycle-rules)
- [8.30 🏗️ Terraform Dynamic Block](#830--terraform-dynamic-block)
- [8.31 🏗️ Terraform Workspace](#831--terraform-workspace)
- [8.32 🏗️ Terraform Import](#832--terraform-import)
- [8.33 🏗️ Terraform Provisioner](#833--terraform-provisioner)
- [8.34 🏗️ Terraform with AWS](#834--terraform-with-aws)
- [8.35 🐙 Terraform with Git/GitHub](#835--terraform-with-gitgithub)
- [8.36 🏗️ Terraform with Jenkins](#836--terraform-with-jenkins)
- [8.37 🐳 Terraform with Docker](#837--terraform-with-docker)
- [8.38 ☸️ Terraform with Kubernetes](#838--terraform-with-kubernetes)
- [8.39 💻 Important Terraform Commands](#839--important-terraform-commands)
- [8.40 🧪 Basic Terraform Practical — Create EC2](#840--basic-terraform-practical--create-ec2)
- [8.41 🌍 Real-World DevOps Example](#841--real-world-devops-example)
- [8.42 ⚖️ Terraform vs AWS Console](#842--terraform-vs-aws-console)
- [8.43 ⚖️ Terraform vs Ansible](#843--terraform-vs-ansible)
- [8.44 ⚖️ Terraform vs Jenkins](#844--terraform-vs-jenkins)
- [8.45 ⚖️ Terraform vs CloudFormation](#845--terraform-vs-cloudformation)
- [8.46 📌 Quick Revision](#846--quick-revision)
- [⚡ Terraform Core Workflow](#-terraform-core-workflow)
- [📌 Final Revision](#-final-revision)

</details>

<details>
<summary><b>🅰️ PART 9 — Ansible — Configuration Management</b></summary>

- [9.1 🅰️ What is Ansible?](#91--what-is-ansible)
- [9.2 🤔 Why Do We Use Ansible?](#92--why-do-we-use-ansible)
- [9.3 🧰 What Does Ansible Provide?](#93--what-does-ansible-provide)
- [9.4 🧱 Ansible Architecture](#94--ansible-architecture)
- [9.5 ⚙️ Installation and First Test](#95--installation-and-first-test)
- [9.6 📋 Inventory](#96--inventory)
- [9.7 💻 Ad-Hoc Commands](#97--ad-hoc-commands)
- [9.8 📜 Playbook](#98--playbook)
- [9.9 🧩 Common Modules](#99--common-modules)
- [9.10 🔁 Idempotency](#910--idempotency)
- [9.11 🔤 Variables, Facts and Conditions](#911--variables-facts-and-conditions)
- [9.12 🔔 Handlers](#912--handlers)
- [9.13 📄 Templates (Jinja2)](#913--templates-jinja2)
- [9.14 🧱 Roles](#914--roles)
- [9.15 🔐 Ansible Vault](#915--ansible-vault)
- [9.16 🔗 Ansible in CI/CD and DevOps](#916--ansible-in-cicd-and-devops)
- [9.17 ⚖️ Ansible vs Terraform](#917--ansible-vs-terraform)
- [9.18 🏗️ Real Example: Deploy a Web App on 3 Servers](#918--real-example-deploy-a-web-app-on-3-servers)
- [9.19 🧯 Troubleshooting](#919--troubleshooting)
- [9.20 📌 Ansible Quick Revision](#920--ansible-quick-revision)
- [9.21 🧠⚡ Ansible One-Line Memory](#921--ansible-one-line-memory)
- [9.22 🗺️ Ansible Learning Map](#922--ansible-learning-map)
- [9.23 ⭐ Ansible Final Memory](#923--ansible-final-memory)

</details>

<details>
<summary><b>🔥 PART 10 — Prometheus — Monitoring and Alerting</b></summary>

- [10.1 🔥 What is Prometheus?](#101--what-is-prometheus)
- [10.2 🤔 Why Do We Use Prometheus?](#102--why-do-we-use-prometheus)
- [10.3 🧰 What Does Prometheus Provide?](#103--what-does-prometheus-provide)
- [10.4 🧱 Prometheus Architecture](#104--prometheus-architecture)
- [10.5 📊 Metric Types](#105--metric-types)
- [10.6 ⚙️ Installation and Configuration](#106--installation-and-configuration)
- [10.7 🔌 Exporters](#107--exporters)
- [10.8 🔎 PromQL Basics](#108--promql-basics)
- [10.9 🚨 Alerting](#109--alerting)
- [10.10 ☸️ Prometheus in Kubernetes](#1010--prometheus-in-kubernetes)
- [10.11 💾 Storage and Retention](#1011--storage-and-retention)
- [10.12 ⚖️ Pull vs Push Model](#1012--pull-vs-push-model)
- [10.13 🔗 Prometheus in DevOps](#1013--prometheus-in-devops)
- [10.14 🏗️ Real Example: Monitor 2 Web Servers](#1014--real-example-monitor-2-web-servers)
- [10.15 🧯 Troubleshooting](#1015--troubleshooting)
- [10.16 📌 Prometheus Quick Revision](#1016--prometheus-quick-revision)
- [10.17 🧠⚡ Prometheus One-Line Memory](#1017--prometheus-one-line-memory)
- [10.18 🗺️ Prometheus Learning Map](#1018--prometheus-learning-map)
- [10.19 ⭐ Prometheus Final Memory](#1019--prometheus-final-memory)

</details>

<details>
<summary><b>📊 PART 11 — Grafana — Dashboards and Visualization</b></summary>

- [11.1 📊 What is Grafana?](#111--what-is-grafana)
- [11.2 🤔 Why Do We Use Grafana?](#112--why-do-we-use-grafana)
- [11.3 🧰 What Does Grafana Provide?](#113--what-does-grafana-provide)
- [11.4 🧱 Grafana Architecture](#114--grafana-architecture)
- [11.5 ⚙️ Installation](#115--installation)
- [11.6 🔌 Data Sources](#116--data-sources)
- [11.7 🧩 Dashboards and Panels](#117--dashboards-and-panels)
- [11.8 🔁 Variables and Templating](#118--variables-and-templating)
- [11.9 📥 Importing Ready-Made Dashboards](#119--importing-ready-made-dashboards)
- [11.10 🚨 Grafana Alerting](#1110--grafana-alerting)
- [11.11 👥 Users, Teams and Permissions](#1111--users-teams-and-permissions)
- [11.12 🧾 Provisioning (Config as Code)](#1112--provisioning-config-as-code)
- [11.13 🔗 Grafana in DevOps](#1113--grafana-in-devops)
- [11.14 ☸️ Grafana in Kubernetes](#1114--grafana-in-kubernetes)
- [11.15 🏗️ Real Example: Server Monitoring Dashboard](#1115--real-example-server-monitoring-dashboard)
- [11.16 🧯 Troubleshooting](#1116--troubleshooting)
- [11.17 📌 Grafana Quick Revision](#1117--grafana-quick-revision)
- [11.18 🧠⚡ Grafana One-Line Memory](#1118--grafana-one-line-memory)
- [11.19 🗺️ Grafana Learning Map](#1119--grafana-learning-map)
- [11.20 ⭐ Grafana Final Memory](#1120--grafana-final-memory)

</details>

---

# 🌿 PART 1 — Git & GitHub — Version Control and Collaboration

> **Git tracks code changes. GitHub shares and manages the code with the team.**
<a name="topic-1"></a>

---

## 1.1 🧭 Git & GitHub Fundamentals


### 📖 What is Git?

#### 🧠 Technical Definition

Git is a **distributed version control system (VCS)**. It is used to track changes in source code, manage different versions of files, and collaborate with other developers.

#### 💡 Simple Definition

**Git helps developers save, track, and manage changes in their code.**

#### ⚙️ What Does Git Do?

Git mainly tracks the changes made to project files.

For example:

```text
Developer
    ↓
Modify Code
    ↓
Git detects changes
    ↓
Stage Changes
    ↓
Commit Changes
    ↓
Version Saved

```

Git allows us to know:

- What changed
- When it changed
- Which version contains the change
- What the previous version looked like
- Which changes should be included in a commit

#### 🤔 Why Do We Use Git?

Without Git, developers may create files like:

```text
project-final
project-final-new
project-final-new-2
project-final-latest
project-final-latest-real

```

This becomes difficult to manage.

With Git, we can properly maintain the history of our project.

Git helps us:

- Track code changes
- Maintain different versions
- Go back to an older version
- Create branches
- Merge changes
- Work with multiple developers
- Maintain project history
- Manage changes safely

#### 📦 What Does Git Provide?

Git provides several features that help us manage a project:

| Feature             | Purpose                               |
| ------------------- | ------------------------------------- |
| Version Control     | Track different versions              |
| Commit History      | See previous commits                  |
| Branches            | Work on different features separately |
| Merging             | Combine changes                       |
| Local Repository    | Store Git history locally             |
| Staging Area        | Prepare changes before commit         |
| Remote Repository   | Work with remote repositories         |
| Change Tracking     | Know what changed                     |
| Conflict Management | Handle conflicting changes            |

#### 🌍 Real-World Example

Suppose you are developing an application.

You create Version 1:

```text
Login Page

```

Later you add:

```text
Payment Page

```

Then:

```text
Version 1
   ↓
Version 2
   ↓
Version 3

```

If the payment feature causes a problem, Git helps you inspect the previous versions and understand what changed.

#### 🧠 Easy Memory

**Git = Version Control**


---

### 📖 What is GitHub?

#### 🧠 Technical Definition

GitHub is a **cloud-based platform** used to store, manage, and share Git repositories online.

#### 💡 Simple Definition

**GitHub is a platform used to store and manage our code online.**

GitHub allows developers to:

- Store repositories online
- Push and pull code
- Collaborate with developers
- Review code changes
- Use branches and Pull Requests
- Keep a remote copy of their code
- Track issues and tasks
- Integrate CI/CD tools

#### 🤔 Why Do We Use GitHub?

Git works locally on our computer.

But when multiple developers need to share and collaborate on the same project, we need a remote platform.

GitHub provides that platform.

```text
Developer A
      ↓
   GitHub
      ↑
Developer B

```

#### 🧠 Easy Memory

```text
Git
 ↓
Version Control Tool

GitHub
 ↓
Online Platform

```


---

### 💻 Git vs GitHub

| Git                                           | GitHub                                   |
| --------------------------------------------- | ---------------------------------------- |
| Version control system                        | Cloud-based development platform         |
| Runs locally on our computer                  | Hosted online                            |
| Tracks code changes                           | Hosts Git repositories                   |
| Used through Git commands                     | Provides Git plus collaboration features |
| Can work without internet for many operations | Mainly used online                       |
| Maintains local Git history                   | Provides remote repository hosting       |

#### 🧠 Easy Memory

```text
Git
 ↓
Track Code Changes

GitHub
 ↓
Store + Share + Collaborate

```

---

## 1.2 📦 Git Repository & Working Areas


### 📖 What is a Git Repository?

A **Git repository** is a location where Git stores project files and keeps track of their changes.

A repository can be:

- Local
- Remote

---

### 📁 Local Repository

A local repository is stored on our computer.

```text
Developer Computer
       ↓
Local Git Repository

```

We use the local repository to:

- Save commits
- Maintain project history
- Create branches
- Merge changes
- Work without internet for many Git operations

---

### 🌐 Remote Repository

A remote repository is stored on a remote platform such as GitHub.

```text
Local Repository
       ↓
     GitHub
       ↓
Remote Repository

```

The remote repository is mainly used for:

- Sharing code
- Collaboration
- Backup/remote copy
- Pull Requests
- Code reviews

---

### 📊 Local vs Remote Repository

| Local Repository                      | Remote Repository                  |
| ------------------------------------- | ---------------------------------- |
| Stored on our computer                | Stored on remote server/platform   |
| Used for local development            | Used for sharing and collaboration |
| Managed using Git                     | Commonly hosted on GitHub          |
| Many operations work without internet | Usually accessed through internet  |

#### 🧠 Easy Memory

```text
Local
→ My Computer

Remote
→ GitHub / Remote Server

```

---

### 💻 Git Working Areas

Git mainly works with three important areas:

```text
Working Directory
       ↓
Staging Area
       ↓
Local Repository

```

Understanding these areas is very important because many Git commands are based on moving changes between them.

---

### 🔹 Working Directory

The **Working Directory** is the area where we actually work on our project files.

Suppose our project contains:

```text
index.html
style.css
script.js

```

If we modify `index.html`, the change first exists in the **Working Directory**.

We can check the change using:

```bash
git status

```

#### 💡 Simple Meaning

**Working Directory = Where we actually modify files**

---

### 🏷️ Staging Area

The **Staging Area** is an intermediate area where we select the changes that we want to include in our next commit.

Suppose we changed:

```text
index.html
style.css
script.js

```

But we only want to commit `index.html`.

We can use:

```bash
git add index.html

```

Now only `index.html` is staged.

#### 🤔 Why Do We Need the Staging Area?

It gives us control over what goes into the next commit.

Without staging, it would be harder to select specific changes for a commit.

#### 🔄 Flow

```text
Working Directory
       │
       │ git add
       ↓
Staging Area

```

#### 💡 Simple Meaning

**Staging Area = Changes prepared for the next commit**

---

### 📁 Local Repository

The Local Repository stores committed versions and project history.

We move changes from the Staging Area to the Local Repository using:

```bash
git commit -m "Updated homepage"

```

After the commit, Git creates a record of those changes in the repository history.

We can view the history using:

```bash
git log

```

#### 🔄 Flow

```text
Staging Area
       │
       │ git commit
       ↓
Local Repository

```

#### 💡 Simple Meaning

**Local Repository = Where committed project history is stored**

---

### 🔄 Complete Working Area Flow

```text
Working Directory
       │
       │ git add
       ↓
Staging Area
       │
       │ git commit
       ↓
Local Repository

```

#### 🧠 Easy Memory

```text
Working Directory
= Where I work

Staging Area
= What I want to commit

Local Repository
= What I have committed

```

---

### 💻 Git Basic Workflow

The basic Git workflow is:

```text
Create / Modify Files
        ↓
    git status
        ↓
      git add
        ↓
  Staging Area
        ↓
    git commit
        ↓
Local Repository
        ↓
     git push
        ↓
      GitHub

```

#### 🪜 What Happens at Each Step?

| Step             | What Happens                 |
| ---------------- | ---------------------------- |
| Modify files     | We make changes              |
| `git status`     | Check what changed           |
| `git add`        | Select changes for commit    |
| Staging Area     | Changes are prepared         |
| `git commit`     | Save a version locally       |
| Local Repository | Commit is stored in history  |
| `git push`       | Send local commits to remote |
| GitHub           | Remote copy is updated       |

#### 🧠 Easy Memory

**Modify → Add → Commit → Push**

---

<a name="topic-3"></a>

---

## 1.3 🛠️ Basic Git Commands


### 💻 `git status`

Command:

```bash
git status

```

`git status` shows the current state of the **Working Directory** and **Staging Area**.

It can show:

- Modified files
- Untracked files
- Staged files
- Current branch information

#### 💻 Example

Suppose we create:

```text
index.html

```

and have not added it yet.

`git status` can show that the file is untracked.

After:

```bash
git add index.html

```

the status changes because the file is now staged.

#### 🤔 Why Do We Use It?

Before running other Git commands, `git status` helps us understand the current state of the repository.

#### 💡 Simple Meaning

**`git status` = Check what is happening in my repository**


---

### 💻 `git add`

Command:

```bash
git add filename

```

`git add` moves changes from the **Working Directory** to the **Staging Area**.

Example:

```bash
git add index.html

```

To stage multiple changes:

```bash
git add .

```

#### 🤔 Why Do We Use `git add`?

Suppose three files are changed:

```text
index.html
style.css
script.js

```

But we only want to include:

```text
index.html

```

in our next commit.

We can use:

```bash
git add index.html

```

Now only that file is staged.

#### ⚙️ How It Works

```text
Working Directory
       │
       │ git add
       ↓
Staging Area
       │
       │ git commit
       ↓
Local Repository

```

#### ⚠️ Important Point

`git add` **does not create a commit**.

It only prepares selected changes for the next commit.

#### 💡 Simple Meaning

**`git add` = Prepare changes for commit**


---

### 💻 `git commit`

Command:

```bash
git commit -m "Add login page"

```

`git commit` creates a **snapshot** of the staged changes in the local repository.

Think of a commit as a saved version of the project.

```text
Staging Area
      ↓
git commit
      ↓
Local Repository

```

#### 🤔 Why Do We Use Commit?

A commit gives us a point in project history.

For example:

```text
Commit 1
→ Added login page

Commit 2
→ Added payment page

Commit 3
→ Fixed login bug

```

We can later inspect these commits using `git log`.

#### 💡 Simple Meaning

**Commit = Save a version in Git history**


---

### 💻 `git log`

Command:

```bash
git log

```

`git log` shows the commit history.

Example:

```text
Commit 3
Commit 2
Commit 1

```

For a shorter output:

```bash
git log --oneline

```

#### 🤔 Why Do We Use It?

It helps us understand:

- Previous commits
- Commit messages
- Commit history
- How the project changed over time

#### 💡 Simple Meaning

**`git log` = See commit history**

---

### 💻 `git diff`

Command:

```bash
git diff

```

`git diff` shows changes that have **not yet been staged**.

For example:

```text
Old Code
   ↓
New Code

```

It helps us review our changes before adding them to the staging area.

#### 💡 Simple Meaning

**`git diff` = See what changed**

---

<a name="topic-4"></a>

---

## 1.4 🌐 Git Remote & Remote Commands


### 📖 What is Git Remote?

A **Git Remote** is a reference to a remote Git repository located outside our local computer.

For example:

```text
Local Repository
       ↓
     Remote
       ↓
GitHub Repository

```

The remote tells Git where it can send and get code.

---

### 📖 What is `origin`?

`origin` is the **common name given to a remote repository**.

For example:

```text
origin → https://github.com/user/project.git

```

When we run:

```bash
git push origin main

```

it means:

> Send my local `main` branch commits to the remote named `origin`.

#### 🧠 Easy Memory

**Remote = Reference to another Git repository**

**origin = Common name of the remote**

---

### 💻 `git remote`

To check configured remotes:

```bash
git remote

```

To see remote URLs:

```bash
git remote -v

```

Example:

```text
origin  https://github.com/user/project.git (fetch)
origin  https://github.com/user/project.git (push)

```

#### 📤 Fetch and Push

```text
fetch
→ Where Git gets remote changes from

push
→ Where Git sends local commits

```

---

### 💻 `git clone`

Command:

```bash
git clone https://github.com/user/project.git

```

`git clone` creates a local copy of a remote repository.

```text
GitHub Repository
       ↓
   git clone
       ↓
Local Computer

```

#### ⚙️ What Does Clone Give Us?

When we clone a repository, we get a local copy that we can work with using Git.

#### 🌍 Real-World Example

Suppose your company already has a project on GitHub.

Instead of creating the project from zero, you clone it:

```bash
git clone <repository-url>

```

Now you have the project on your computer.

#### 💡 Simple Meaning

**Clone = Copy a remote repository to your computer**


---

### 💻 `git push`

Command:

```bash
git push origin main

```

`git push` uploads our local commits to the remote repository.

```text
Local Repository
       ↓
    git push
       ↓
GitHub Repository

```

#### ⚖️ Important Difference

```text
git commit
     ↓
Save changes locally

git push
     ↓
Send local commits to remote

```

#### 💡 Simple Meaning

**Push = Send local commits to remote**


---

### 💻 `git fetch`

Command:

```bash
git fetch

```

`git fetch` downloads remote changes but **does not automatically integrate them into the current branch**.

It is useful when we want to first check what has changed on the remote repository.

#### 💻 Example

Suppose another developer pushed changes to GitHub.

You can run:

```bash
git fetch origin

```

Git downloads information about those changes.

You can then inspect the changes before deciding how to integrate them.

#### 💡 Simple Meaning

**Fetch = Get remote changes without integrating them**

---

### 💻 `git pull`

Command:

```bash
git pull

```

`git pull` gets changes from the remote repository and integrates them into the current local branch.

At a high level:

```text
Remote Repository
       ↓
     git pull
       ↓
Local Branch

```

#### 💡 Simple Meaning

**Pull = Get remote changes + integrate them**

---

### 💻 Git Fetch vs Git Pull

#### 💻 `git fetch`

```text
Remote
  ↓
Fetch
  ↓
Local Git information

```

It does not automatically integrate the changes into the current branch.

#### 💻 `git pull`

```text
Remote
  ↓
Pull
  ↓
Get changes
  ↓
Integrate

```

#### ⚖️ Comparison

| `git fetch`                                  | `git pull`                                |
| -------------------------------------------- | ----------------------------------------- |
| Downloads remote changes                     | Gets remote changes and integrates them   |
| Does not automatically update current branch | Integrates changes into current branch    |
| Gives more control                           | More convenient                           |
| Useful for checking changes first            | Useful when we want latest remote changes |

#### 🧠 Easy Memory

**fetch → Get**

**pull → Get + Integrate**

---

<a name="topic-5"></a>

---

## 1.5 🌿 Git Branching & HEAD


### 📖 What is a Git Branch?

A **branch is a separate line of development** in a Git repository.

Example:

```text
main
 │
 ├── feature-login
 │
 └── feature-payment

```

Developers can work on features without directly changing the main branch.

#### 🌍 Real-World Example

Suppose:

```text
main

```

contains production code.

You want to create a login feature.

Instead of changing `main` directly:

```text
main
 ↓
feature-login

```

You work on `feature-login`.

After development, testing, and review, the changes can be merged into `main`.

#### 🤔 Why Do We Use Branches?

Branches help us:

- Develop features separately
- Fix bugs separately
- Protect the main code
- Allow multiple developers to work independently
- Review changes before merging

#### 🔄 Branch Workflow

```text
main
  ↓
feature-login
  ↓
Development
  ↓
Testing
  ↓
Pull Request
  ↓
Code Review
  ↓
Merge
  ↓
main

```

#### 💡 Simple Meaning

**Branch = Separate line of development**

#### 🧠 Easy Memory

```text
main
→ Stable Code

feature branch
→ New Work

```


---

### 💻 Important Branch Commands

#### 🌿 List Branches

```bash
git branch

```

#### 🌿 Create Branch

```bash
git branch feature-login

```

#### 🌿 Switch Branch

```bash
git switch feature-login

```

#### 🔹 Create and Switch

```bash
git switch -c feature-login

```

#### 🌿 Delete Branch

```bash
git branch -d feature-login

```

#### 🌿 Merge Branch

First switch to the target branch:

```bash
git switch main

```

Then:

```bash
git merge feature-login

```

---

### 📖 What is Git HEAD?

`HEAD` is a reference that tells Git **where we are currently working**.

In normal branch-based work:

```text
HEAD
 ↓
main
 ↓
Latest Commit

```

If we switch to another branch:

```text
HEAD
 ↓
feature-login
 ↓
Latest Commit

```

#### 💡 Simple Meaning

**HEAD = Current location in Git**

---

### 📊 HEAD vs Branch vs Commit

#### 💾 Commit

A commit is a **saved snapshot** of the project.

```text
Commit A
   ↓
Commit B
   ↓
Commit C

```

#### 🌿 Branch

A branch is a **movable reference pointing to a commit**.

```text
main
 ↓
Commit C

```

#### 📍 HEAD

HEAD tells Git **which branch or commit we are currently on**.

```text
HEAD
 ↓
main
 ↓
Commit C

```

#### 🧠 Easy Memory

```text
Commit → Saved Snapshot

Branch → Pointer to a Commit

HEAD → Current Location

```

---

<a name="topic-6"></a>

---

## 1.6 🔀 Branch Integration


### 💻 Git Merge

`git merge` combines changes from one branch into another branch.

Example:

```text
feature-login
      ↓
    Merge
      ↓
    main

```

The changes from `feature-login` are combined into `main`.

#### 🌍 Real-World Example

Suppose a developer finishes the login feature on:

```text
feature-login

```

After testing and review, we want those changes in:

```text
main

```

First switch to the target branch:

```bash
git switch main

```

Then:

```bash
git merge feature-login

```

#### 💡 Simple Meaning

**Merge = Combine branch changes**

#### 🧠 Easy Memory

**Feature Branch → Merge → Main**

---

### 🔀 Merge Conflict

A **merge conflict** happens when Git cannot automatically combine changes from different branches.

This commonly happens when different developers modify the same part of a file.

#### 💻 Example

Developer A:

```text
Hello Sam

```

changes it to:

```text
Hello Samir

```

Developer B changes the same line to:

```text
Hello Developer

```

When Git tries to merge both changes, it may not know which version should be used.

That creates a merge conflict.

#### ⚔️ Conflict Flow

```text
Developer A
    ↓
Change File

Developer B
    ↓
Change Same Part

       ↓

Git Merge
       ↓
Conflict
       ↓
Manual Resolution

```

#### 🔹 How Do We Resolve It?

Basic flow:

```text
Merge
  ↓
Conflict
  ↓
Open the File
  ↓
Resolve the Conflict
  ↓
git add
  ↓
git commit

```

We manually decide which code should remain.

Then we stage the resolved file and complete the merge.

#### 💡 Simple Meaning

**Merge Conflict = Git cannot decide which change to keep**


---

### 💻 Git Rebase

Command:

```bash
git rebase main

```

`git rebase` moves or reapplies commits from one branch on top of another branch.

#### 🤔 Why Do We Use Rebase?

Suppose the `main` branch has moved forward while our feature branch is based on an older version.

Rebase takes our feature commits and places them on top of the latest base.

#### 🔀 Before Rebase

```text
        C1 ── C2   feature
       /
A ── B
       \
        D ── E     main

```

#### 🔀 After Rebase

```text
A ── B ── D ── E
                \
                 C1' ── C2'

```

The feature commits are reapplied on top of the latest base.

#### 💡 Simple Meaning

**Rebase = Move your branch changes onto a new base**

#### ⚠️ Important

Rebase can **rewrite commit history**.

Because of this, it should be used carefully on branches that are already shared with other developers.


---

### 📊 Merge vs Rebase

| Merge                             | Rebase                                      |
| --------------------------------- | ------------------------------------------- |
| Combines branch histories         | Replays commits on a new base               |
| Preserves existing history        | Rewrites commit history                     |
| Can create a merge commit         | Usually avoids a merge commit               |
| Commonly used for shared branches | Should be used carefully on shared branches |

#### 🧠 Easy Memory

**Merge → Combine**

**Rebase → Reapply on new base**

---

<a name="topic-7"></a>

---

## 1.7 🤝 GitHub Collaboration


### 🐙 GitHub Repository

A **GitHub repository** is the remote location where a project and its Git history can be hosted.

It can contain:

```text
Source Code
Git History
README
.gitignore
Configuration Files
Build Files

```

Example:

```text
my-project/
│
├── src/
├── README.md
├── .gitignore
└── pom.xml

```

#### 💡 Simple Explanation

Think of a GitHub repository as an **online project repository managed using Git**.

---

### ⚙️ What Does GitHub Provide?

GitHub provides features such as:

- Git repository hosting
- Remote repositories
- Pull Requests
- Issues
- Code Reviews
- Branch protection
- Actions / CI/CD
- Collaboration
- Access control
- Project management features

---

### ⚙️ What Does GitHub Do?

GitHub provides a central platform where developers collaborate.

Example:

```text
Developer A
     ↓
   GitHub
     ↑
Developer B

```

Developers can:

- Push code
- Pull code
- Review code
- Create Pull Requests
- Discuss changes
- Manage issues
- Trigger CI/CD pipelines

---

### 📥 Pull Request

A **Pull Request (PR)** is a request to merge changes from one branch into another branch.

Example:

```text
feature-login
      ↓
Pull Request
      ↓
Code Review
      ↓
Approved
      ↓
Merge
      ↓
main

```

#### 🤔 Why Do We Use Pull Requests?

Pull Requests are commonly used for:

- Code review
- Discussion
- Testing
- Collaboration
- Controlled merging

#### 🌍 Real-World Workflow

```text
Developer
    ↓
Feature Branch
    ↓
Changes
    ↓
Push to GitHub
    ↓
Pull Request
    ↓
Code Review
    ↓
Testing
    ↓
Approval
    ↓
Merge

```

#### 💡 Simple Meaning

**Pull Request = Request to merge reviewed changes**


---

### 🐙 GitHub Issues

Issues are used to track:

- Bugs
- Tasks
- Feature requests
- Work items

Example:

```text
Issue #25
"Login button is not working"

```

A developer can work on the issue and submit a Pull Request to fix it.

#### 💡 Simple Meaning

**Issue = Track a task or problem**

---

### 📊 Fork vs Clone

#### 🍴 Fork

A **fork** creates your own copy of someone else's GitHub repository under your GitHub account.

```text
Original GitHub Repository
          ↓
        Fork
          ↓
Your GitHub Repository

```

A fork is commonly used when you want to contribute to a repository where you do not have direct write access.

#### 📥 Clone

`git clone` copies a repository from a remote location to your local computer.

```text
GitHub Repository
       ↓
    git clone
       ↓
Local Computer

```

#### ⚖️ Difference

| Fork                                          | Clone                           |
| --------------------------------------------- | ------------------------------- |
| Creates a copy on GitHub                      | Creates a copy on your computer |
| GitHub-level operation                        | Git-level operation             |
| Useful for contributing to another repository | Useful for working locally      |
| Creates your own GitHub repository            | Creates a local Git repository  |

#### 🧠 Easy Memory

```text
Fork
GitHub → Your GitHub Account

Clone
GitHub → Your Computer

```

---

<a name="topic-8"></a>

---

## 1.8 🚫 `.gitignore`


### 📖 What is `.gitignore`?

`.gitignore` tells Git **which files or directories should not be tracked**.

Example:

```text
node_modules/
.env
*.log
target/

```

#### 🤔 Why Is `.gitignore` Important?

We should avoid committing:

- Secrets
- Passwords
- API keys
- Temporary files
- Build files
- Large unnecessary directories

For example:

```text
.env

```

may contain sensitive environment variables and should normally not be committed.

#### 💻 Example

```text
project/
│
├── src/
├── .env
├── node_modules/
├── README.md
└── .gitignore

```

`.gitignore` can tell Git not to track:

```text
.env
node_modules/

```

#### 💡 Simple Meaning

**`.gitignore` = Tell Git what not to track**

---

## 1.9 ↩️ Git History, Undoing Changes & Recovery


### 💻 Git Log

Command:

```bash
git log

```

Shows commit history.

Example:

```text
Commit 3
Commit 2
Commit 1

```

Short format:

```bash
git log --oneline

```

#### 🤔 Why Do We Use It?

It helps us inspect:

- Commit history
- Previous versions
- Commit messages
- Changes made over time

#### 💡 Simple Meaning

**`git log` = View commit history**

---

### 💻 Git Diff

Command:

```bash
git diff

```

Shows changes that have not yet been staged.

```text
Old Code
   ↓
New Code

```

#### 💡 Simple Meaning

**`git diff` = See what changed**

---

### 💻 Git Reset

`git reset` can move the current branch reference and/or change the staging state depending on the option used.

A common example:

```bash
git reset HEAD filename

```

This removes the file from the staging area while keeping the file changes in the Working Directory.

#### ⚠️ Important

`git reset` has different modes and can affect commit history, so use it carefully.

#### 💡 Simple Meaning

**Reset = Reset Git state**

---

### 💻 Git Restore

`git restore` is used to restore files in the Working Directory or Staging Area.

#### 🏷️ Discard Unstaged Changes

```bash
git restore filename

```

This can discard unstaged changes in a file and restore it to the version from the latest commit.

#### 🏷️ Unstage a File

```bash
git restore --staged filename

```

This removes the file from the Staging Area while keeping the changes in the Working Directory.

#### 💡 Simple Meaning

**Restore = Restore file changes / unstage files**

---

### 💻 Git Revert

Command:

```bash
git revert <commit-id>

```

`git revert` creates a **new commit** that reverses the changes introduced by an earlier commit.

Example:

```text
Commit A
   ↓
Commit B
   ↓
Commit C
   ↓
git revert B
   ↓
New Commit

```

The original history remains, and a new commit is created to undo the earlier change.

This is commonly preferred for changes that have already been shared with other developers.

#### 💡 Simple Meaning

**Revert = Undo a previous commit by creating a new commit**

---

### 📊 Reset vs Restore vs Revert

| Command       | Main Purpose                                                  |
| ------------- | ------------------------------------------------------------- |
| `git reset`   | Reset/move Git state and staging or history depending on mode |
| `git restore` | Restore file changes or unstage files                         |
| `git revert`  | Undo a previous commit by creating a new commit               |

#### 🧠 Easy Memory

```text
reset
→ Reset Git state

restore
→ Restore files

revert
→ Undo using a new commit

```

---

### 💻 Git Stash

`git stash` temporarily saves our **uncommitted changes** so we can work on something else without creating an unwanted commit.

Command:

```bash
git stash

```

After stashing, the Working Directory becomes clean.

Later, we can bring the changes back:

```bash
git stash pop

```

#### 🌍 Example Scenario

Suppose we are working on:

```text
feature-login

```

We have unfinished changes.

Suddenly, we need to switch to another branch to fix an urgent bug.

Instead of creating an unwanted commit:

```text
Uncommitted Changes
        ↓
    git stash
        ↓
Switch Branch
        ↓
Fix Bug
        ↓
Return to Branch
        ↓
git stash pop

```

#### 🛠️ Other Commands

View stashes:

```bash
git stash list

```

Apply a stash:

```bash
git stash apply

```

#### ⚖️ `apply` vs `pop`

```text
git stash apply
→ Apply changes but keep stash

git stash pop
→ Apply changes and remove stash

```

#### 💡 Simple Meaning

**stash = Temporarily keep unfinished changes**


---

### 💻 Git Reflog

Command:

```bash
git reflog

```

Git reflog records movements of **HEAD and branch references** in the local repository.

It can help us find commits that are no longer reachable through the current branch history.

Example:

```text
HEAD@{0}
HEAD@{1}
HEAD@{2}
HEAD@{3}

```

Suppose we accidentally reset our branch:

```bash
git reset --hard

```

We may be able to find the previous commit using:

```bash
git reflog

```

Then we can use the appropriate Git command to recover it.

#### 💡 Simple Meaning

**reflog = Record of where HEAD/branches were**

#### ⚠️ Important

Reflog is primarily a **local recovery mechanism**.

---

## 1.10 ⚡ Advanced Git Operations


### 💻 Git Cherry-Pick

Command:

```bash
git cherry-pick <commit-id>

```

`git cherry-pick` applies the changes introduced by a **specific commit** onto the current branch.

#### 💻 Example

Suppose:

```text
main
 │
 ├── A
 ├── B
 └── C

feature
 │
 ├── A
 ├── B
 └── D

```

Suppose we want only the change from commit `D` on another branch.

We can cherry-pick it:

```text
Commit D
   ↓
cherry-pick
   ↓
Other Branch

```

#### 🤔 Why Do We Use Cherry-Pick?

Sometimes we do not want to merge an entire branch.

We only need one specific change.

In that case, cherry-pick can apply that particular commit.

#### 💡 Simple Meaning

**Cherry-pick = Take one specific commit and apply it to another branch**

#### 🧠 Easy Memory

**Cherry-pick → Pick one commit**

---

## 1.11 🔐 GitHub Authentication


To work with GitHub repositories securely, common authentication methods include:

- HTTPS with appropriate credentials/token mechanisms
- SSH keys

### 🔹 HTTPS

HTTPS uses an HTTPS-based remote URL and appropriate authentication mechanisms.

### 🔑 SSH

SSH uses SSH keys for authentication.

Example SSH remote:

```text
git@github.com:user/project.git

```

SSH allows authenticated Git operations without repeatedly entering a password.

#### 💡 Simple Difference

```text
HTTPS
→ HTTPS-based authentication

SSH
→ SSH key-based authentication

```

---

## 1.12 🏷️ Git Tags


A **tag** is a reference used to mark a specific point in Git history.

Tags are commonly used for releases.

Example:

```text
v1.0
v2.0
v2.1

```

#### 🤔 Why Do We Use Tags?

Suppose our application reaches a stable release:

```text
Version 1.0

```

We can mark that commit with:

```text
v1.0

```

Later:

```text
v2.0

```

This makes important release points easy to identify.

#### 🏷️ Create a Tag

```bash
git tag v1.0

```

#### 🏷️ Create an Annotated Tag

```bash
git tag -a v1.0 -m "Version 1.0"

```

#### 🏷️ Push a Tag

```bash
git push origin v1.0

```

#### 💡 Simple Meaning

**Tag = Mark a specific version/release**

#### 🧠 Easy Memory

```text
v1.0 → First Release
v2.0 → Second Release

```

---

## 1.13 ☁️ Git in DevOps


### 🚀 Why is Git Important in DevOps?

Git is one of the important tools in DevOps because source code needs to be **version controlled** before it can be automatically built, tested, and deployed.

Typical flow:

```text
Developer
    ↓
Git
    ↓
GitHub
    ↓
Jenkins
    ↓
Maven
    ↓
Test
    ↓
Docker
    ↓
Deployment

```

Git acts as the **source code management stage** of the DevOps process.

---

### 💻 Git + Jenkins

Jenkins can monitor or be triggered by changes in a GitHub repository.

Example:

```text
Developer
    ↓
git push
    ↓
GitHub
    ↓
Webhook
    ↓
Jenkins
    ↓
Pipeline

```

Jenkins can then:

- Checkout code
- Build the application
- Run tests
- Perform code analysis
- Build Docker images
- Deploy the application

#### 💡 Simple Explanation

Developer pushes code to GitHub.

GitHub can notify Jenkins using a webhook.

Jenkins starts the pipeline.

#### 🧠 Easy Memory

**GitHub stores the code → Jenkins automates the pipeline**

---

### 💻 Git + Maven

Git stores the Java source code.

Maven builds the Java application.

Typical flow:

```text
GitHub
   ↓
Jenkins
   ↓
Maven
   ↓
Compile
   ↓
Test
   ↓
JAR/WAR

```

#### 🧠 Easy Memory

```text
Git → Source Code

Maven → Java Build

```

---

### 💻 Git + Docker

Git stores application source code and Docker-related files such as:

```text
Dockerfile

```

A CI/CD pipeline can use the Git repository to build a Docker image.

Typical flow:

```text
GitHub
   ↓
Jenkins
   ↓
Dockerfile
   ↓
Docker Build
   ↓
Docker Image

```

#### 🧠 Easy Memory

```text
Git
→ Source Code

Docker
→ Container Image

```

---

### 🌿 Complete Git DevOps Flow

A typical Java DevOps workflow can look like:

```text
Developer
    ↓
Git
    ↓
GitHub
    ↓
Pull Request
    ↓
Code Review
    ↓
Merge
    ↓
Jenkins
    ↓
Maven
    ↓
Tests
    ↓
Docker
    ↓
Container Registry
    ↓
Deployment

```

#### 🔄 What Happens?

**Developer**

Writes and modifies application code.

↓

**Git**

Tracks the changes and maintains version history.

↓

**GitHub**

Stores the remote repository and supports collaboration.

↓

**Pull Request**

Allows code review and controlled merging.

↓

**Jenkins**

Runs the CI/CD pipeline.

↓

**Maven**

Builds the Java application.

↓

**Tests**

Checks whether the application works correctly.

↓

**Docker**

Builds a container image.

↓

**Container Registry**

Stores the Docker image.

↓

**Deployment**

Deploys the application to the target environment.

---

<a name="topic-14"></a>

---

## 1.14 🧪 Basic Git Practical


### 🎯 Goal

Create a local Git repository, commit code, and push it to GitHub.

---

### 🌿 Step 1 — Check Git

```bash
git --version

```

This checks whether Git is installed.

---

### 🔧 Step 2 — Configure Git

```bash
git config --global user.name "Name"
git config --global user.email "email@example.com"

```

This sets the name and email Git will use for commits.

---

### 🪜 Step 3 — Create Project

```bash
mkdir my-project
cd my-project

```

---

### 🌿 Step 4 — Initialize Git

```bash
git init

```

This creates a Git repository in the project directory.

---

### 🪜 Step 5 — Create a File

```bash
echo "Hello DevOps" > README.md

```

---

### 🪜 Step 6 — Check Status

```bash
git status

```

You should see the new file as untracked.

---

### 🏷️ Step 7 — Stage the File

```bash
git add README.md

```

Now the file is in the staging area.

---

### 💾 Step 8 — Commit

```bash
git commit -m "Initial commit"

```

Now the change is saved in the local Git history.

---

### 🐙 Step 9 — Connect GitHub Repository

Create a repository on GitHub and add it as a remote:

```bash
git remote add origin <repository-url>

```

---

### 📤 Step 10 — Push

```bash
git push -u origin main

```

Now the local code is available in the GitHub repository.

#### 🔄 Complete Practical Flow

```text
Create Project
      ↓
git init
      ↓
Create File
      ↓
git status
      ↓
git add
      ↓
git commit
      ↓
git remote add origin
      ↓
git push
      ↓
GitHub

```

---

<a name="topic-15"></a>

---

## 1.15 🌍 Real-World Git Workflow


Suppose five developers are working on a Java application.

The source code is stored in GitHub.

```text
Developer A ─┐
Developer B ─┤
Developer C ─┼──→ GitHub
Developer D ─┤
Developer E ─┘

```

Each developer works on a separate branch:

```text
main
│
├── feature-login
├── feature-payment
├── bugfix-cart
└── feature-profile

```

#### 👨‍💻 Developer Workflow

A developer can:

```text
Clone Repository
      ↓
Create Feature Branch
      ↓
Make Changes
      ↓
git status
      ↓
git add
      ↓
git commit
      ↓
git push
      ↓
Create Pull Request

```

Then:

```text
Pull Request
      ↓
Code Review
      ↓
Testing
      ↓
Approval
      ↓
Merge
      ↓
main

```

After merge:

```text
GitHub
   ↓
Webhook
   ↓
Jenkins
   ↓
Maven
   ↓
Test
   ↓
Docker
   ↓
Deployment

```

#### 🌍 Complete Real-World Picture

```text
Developer
    ↓
Feature Branch
    ↓
Code Changes
    ↓
git add
    ↓
git commit
    ↓
git push
    ↓
GitHub
    ↓
Pull Request
    ↓
Code Review
    ↓
Testing
    ↓
Merge
    ↓
Jenkins
    ↓
Maven
    ↓
Docker
    ↓
Deployment

```

This is how Git and GitHub become an important part of a DevOps CI/CD workflow.

---

<a name="topic-16"></a>

---

## 1.16 ⭐ Advantages & Limitations


### ✅ Advantages of Git

#### 🔢 Version Control

Git tracks changes to files and maintains project history.

#### 🔹 Distributed

Developers have a complete repository history locally.

#### 🌿 Branching

Developers can work on features independently.

#### 🧪 Collaboration

Multiple developers can work on the same project.

#### 🔹 History

We can see previous commits and changes.

#### 🔹 Offline Work

Many Git operations work without an internet connection because the repository is local.

---

### ✅ Advantages of GitHub

#### 🌐 Remote Repository Hosting

GitHub stores Git repositories online.

#### 🧪 Collaboration

Multiple developers can work together.

#### 📥 Pull Requests

Supports structured code review and merging.

#### 🔹 Issues

Helps track bugs and tasks.

#### 🔹 CI/CD Integration

Can integrate with Jenkins and GitHub Actions.

#### 🔑 Access Control

Organizations can manage repository permissions.

---

### ⚠️ Limitations of Git

- Can be confusing for beginners
- Merge conflicts require manual resolution
- Large repositories can become difficult to manage if not designed properly

---

### ⚠️ Limitations of GitHub

- Depends on remote network access for many collaboration operations
- Public repositories require careful handling of sensitive information
- Repository permissions must be configured correctly

---

<a name="topic-17"></a>

---

## 1.17 ⚡ Quick Revision


### 🌿 Git

**Git = Version Control Tool**

Tracks and manages code changes.

---

### 🐙 GitHub

**GitHub = Git Repository Hosting + Collaboration Platform**

---

### 📁 Repository

**Repository = Project Files + Git History**

---

### 🔹 Working Areas

```text
Working Directory
      ↓
Staging Area
      ↓
Local Repository

```

---

### 🔄 Basic Workflow

```text
Modify
  ↓
git status
  ↓
git add
  ↓
git commit
  ↓
git push
  ↓
GitHub

```

---

### 🔄 Branch Workflow

```text
main
 ↓
feature-branch
 ↓
Development
 ↓
Pull Request
 ↓
Code Review
 ↓
Merge
 ↓
main

```

---

### 🔄 Remote Workflow

```text
GitHub
   ↓
git clone
   ↓
Local Repository

```

```text
Local Repository
   ↓
git push
   ↓
GitHub

```

```text
GitHub
   ↓
git fetch / git pull
   ↓
Local Repository

```

---

### ⚖️ Important Differences

#### 💻 Git vs GitHub

```text
Git
→ Version Control Tool

GitHub
→ Online Collaboration Platform

```

#### ⚖️ Add vs Commit

```text
git add
→ Working Directory → Staging Area

git commit
→ Staging Area → Local Repository

```

#### ⚖️ Commit vs Push

```text
git commit
→ Save Locally

git push
→ Send to Remote

```

#### ⚖️ Fetch vs Pull

```text
git fetch
→ Get remote changes

git pull
→ Get + Integrate

```

#### 📊 Merge vs Rebase

```text
Merge
→ Combine histories

Rebase
→ Reapply commits on new base

```

#### 📊 Reset vs Restore vs Revert

```text
reset
→ Reset Git state

restore
→ Restore files / unstage

revert
→ Undo using a new commit

```

#### 📊 Fork vs Clone

```text
Fork
→ GitHub → Your GitHub Account

Clone
→ GitHub → Your Computer

```

---

<a name="git-command-cheat-sheet"></a>

---

## 📋 Git Command Cheat Sheet


```bash
# Check Git
git --version

# Configure Git
git config --global user.name "Name"
git config --global user.email "email@example.com"

# Create repository
git init

# Check status
git status

# Stage changes
git add .
git add filename

# Commit changes
git commit -m "Commit message"

# View history
git log
git log --oneline

# View changes
git diff

# Create branch
git branch feature-login

# List branches
git branch

# Switch branch
git switch feature-login

# Create and switch
git switch -c feature-login

# Delete branch
git branch -d feature-login

# Merge
git switch main
git merge feature-login

# Rebase
git rebase main

# Cherry-pick
git cherry-pick <commit-id>

# Stash
git stash
git stash list
git stash apply
git stash pop

# Remote
git remote
git remote -v

# Clone
git clone <repository-url>

# Push
git push origin main

# Fetch
git fetch origin

# Pull
git pull origin main

# Reset
git reset HEAD filename

# Restore
git restore filename
git restore --staged filename

# Revert
git revert <commit-id>

# Reflog
git reflog

# Tags
git tag v1.0
git tag -a v1.0 -m "Version 1.0"
git push origin v1.0

```

---

<a name="final-memory"></a>

---

## ⭐ Final Memory


```text
Git
 ↓
Tracks Code Changes
 ↓
Branch
 ↓
Commit
 ↓
Push
 ↓
GitHub
 ↓
Pull Request
 ↓
Code Review
 ↓
Merge
 ↓
Jenkins
 ↓
Maven
 ↓
Docker
 ↓
Deployment

```

**Git tracks and manages code changes.**

**GitHub hosts Git repositories and enables collaboration.**

**Git + GitHub → Source Code Management in DevOps.**


---

# 📦 PART 2 — Maven — Build and Dependency Management

> **Maven = Builds the Java project and manages its libraries**

---

## 2.1 📦 What is Maven?


> **Maven = Build Automation and Dependency Management Tool**

Maven is a tool mainly used for **Java projects**. It **builds the project, runs tests, creates the package (`.jar` / `.war`) and downloads the required libraries automatically.**

Everything is described in one file called **`pom.xml`**.

### 📦 We can use Maven to:

- 🔨 Compile the source code.
- 🧪 Run unit tests.
- 📦 Create `.jar` / `.war` packages.
- 📚 Download and manage libraries (dependencies).
- 🚀 Upload artifacts to a repository such as Nexus.

### ⚙️ It Provides components such as:

- 📄 `pom.xml` (project description)
- 🔁 Build Lifecycle
- 🧩 Plugins and Goals
- 🌐 Repositories (Local, Central, Remote)

to build and manage Java projects in a standard way.

#### 🏗 Maven Basic Flow

```text
💻 Source Code (.java) + 📄 pom.xml
            │
            ▼
        📦 Maven
   (compile → test → package)
            │
            ▼
   🎁 Artifact (.jar / .war)
```

#### 🧠 Easy Memory

> **Maven = Java Project Manager and Builder**

#### ⚠ Important

> **Maven needs Java (JDK) installed first.**

> **Maven downloads libraries from the internet only once and keeps them in `~/.m2`.**

---

## 2.2 🤔 Why Do We Use Maven?


Suppose a Java team builds an application with many libraries.

### ❌ Without Maven

```text
📥 Download Every .jar Manually
            ↓
⌨️ Write Long javac Commands
            ↓
🧩 Different Steps on Every Machine
            ↓
💥 "It Works on My Machine" Problems
```

### ✅ With Maven

```text
📄 Write pom.xml Once
 ↓
📚 Libraries Download Automatically
 ↓
🔁 Same Build Steps Everywhere
 ↓
✅ One Command: mvn clean package
```

#### ⭐ Main Reasons

- 📚 Libraries (and their dependencies) are downloaded automatically
- 🔁 Same build steps on every machine and in Jenkins
- 📁 Standard project structure for every project
- 🧩 Plugins add testing, packaging and code analysis
- 🚀 Easy to connect with Jenkins, SonarQube and Nexus

---

## 2.3 🧰 What Does Maven Provide?


Maven provides:

- 📄 `pom.xml` Project Description
- 📚 Dependency Management
- 🔁 Build Lifecycle (validate → compile → test → package → install → deploy)
- 🧩 Plugins and Goals
- 📁 Standard Project Structure
- 🌐 Repositories (Local, Central, Remote)
- 🏗️ Multi-Module Project Support

| 🧰 Feature | 💡 Meaning |
| --- | --- |
| 📚 Dependency Management | Downloads libraries and their dependencies automatically |
| 🔁 Build Lifecycle | Fixed steps from validate to deploy |
| 🧩 Plugins | Extra work like compiling, testing, packaging |
| 📁 Standard Structure | Same folder layout for all projects |
| 🌐 Repositories | Places to store and download artifacts |
| 🏗️ Multi-Module | Build many related projects together |

---

## 2.4 ⚙️ Installation and Setup


Maven needs **Java (JDK)** first.

```bash
java -version            # check JDK
sudo apt install maven -y   # Ubuntu / Debian
mvn -version             # check Maven
```

Important locations:

| Item | Location |
| --- | --- |
| Local repository | `~/.m2/repository` |
| User settings | `~/.m2/settings.xml` |
| Global settings | `<MAVEN_HOME>/conf/settings.xml` |

---

## 2.5 📁 Standard Project Structure


```text
my-app/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/          → application code
│   │   └── resources/     → config files
│   └── test/
│       ├── java/          → unit tests
│       └── resources/
└── target/                → build output (created by Maven)
```

Create a sample project:

```bash
mvn archetype:generate -DgroupId=com.example -DartifactId=my-app \
    -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

---

## 2.6 📄 pom.xml (Project Object Model)


`pom.xml` is the **heart of Maven**. It describes the project, dependencies and build settings.

```xml
<project>
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.example</groupId>
  <artifactId>my-app</artifactId>
  <version>1.0.0</version>
  <packaging>jar</packaging>

  <properties>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
  </properties>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.13.2</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
```

---

## 2.7 🏷️ Maven Coordinates (GAV)


Every artifact is identified by **three values**:

| Part | Meaning | Example |
| --- | --- | --- |
| `groupId` | Organization / company | `com.example` |
| `artifactId` | Project / module name | `my-app` |
| `version` | Version number | `1.0.0` |

```text
com.example : my-app : 1.0.0      ← unique address of the artifact
```

`1.0.0-SNAPSHOT` means a **development version** that can change. A version without `SNAPSHOT` is a **release**.

---

## 2.8 🔁 Build Lifecycle


Maven has **3 built-in lifecycles**: `clean`, `default` (build), `site`.

Main phases of the **default** lifecycle:

```text
validate → compile → test → package → verify → install → deploy
```

| Phase | What happens |
| --- | --- |
| `validate` | Check that the project is correct |
| `compile` | Compile source code |
| `test` | Run unit tests |
| `package` | Create `.jar` / `.war` in `target/` |
| `verify` | Run checks on the package |
| `install` | Copy artifact to **local** repository (`~/.m2`) |
| `deploy` | Upload artifact to a **remote** repository (e.g. Nexus) |

> 🧠 Running a phase runs **all earlier phases** too. `mvn package` runs validate, compile, test and package.

---

## 2.9 🧩 Plugins and Goals


- 🧩 A **plugin** is a group of tasks. A **goal** is one task of a plugin.
- 🧩 Phases are connected to plugin goals.

```text
Phase: compile  →  Plugin: maven-compiler-plugin  →  Goal: compile
Phase: test     →  Plugin: maven-surefire-plugin  →  Goal: test
Phase: package  →  Plugin: maven-jar-plugin       →  Goal: jar
```

Run a goal directly: `mvn compiler:compile` (format `plugin:goal`).

---

## 2.10 📚 Dependencies and Scopes


A dependency is a library the project needs. Maven also downloads **transitive dependencies** (dependencies of dependencies).

| Scope | Available in | Example |
| --- | --- | --- |
| `compile` (default) | Compile, test, runtime | Spring, Apache Commons |
| `provided` | Compile and test only (server gives it at runtime) | Servlet API |
| `runtime` | Test and runtime only | JDBC driver |
| `test` | Test only | JUnit |

Useful commands:

```bash
mvn dependency:tree      # show all dependencies
mvn dependency:resolve   # download dependencies
```

---

## 2.11 🌐 Maven Repositories


```text
Local Repository (~/.m2)  →  Central Repository (Maven Central)  →  Remote / Private Repository (Nexus)
```

| Type | Meaning |
| --- | --- |
| 🏠 Local | Folder on your machine; Maven checks here first |
| 🌍 Central | Public repository by Maven community |
| 🏢 Remote / Private | Company repository such as **Nexus** or Artifactory |

Flow: Maven looks in **Local → Central / Remote**. Found libraries are saved to Local.

---

## 2.12 🛠️ settings.xml


Used for **machine-level** settings, not project settings.

Common uses:

- 🗄️ Repository **mirror** (use Nexus instead of Maven Central)
- 🗄️ **Credentials** for deploying to Nexus
- ⚙️ Proxy settings

```xml
<settings>
  <servers>
    <server>
      <id>nexus-releases</id>
      <username>deploy-user</username>
      <password>${env.NEXUS_PASSWORD}</password>
    </server>
  </servers>

  <mirrors>
    <mirror>
      <id>nexus</id>
      <mirrorOf>*</mirrorOf>
      <url>http://nexus.example.com:8081/repository/maven-public/</url>
    </mirror>
  </mirrors>
</settings>
```

> ⚠️ Do not store plain-text passwords in Git. Use environment variables or Jenkins credentials.

---

## 2.13 💻 Common Maven Commands


| Command | Use |
| --- | --- |
| `mvn clean` | Delete the `target/` folder |
| `mvn compile` | Compile the code |
| `mvn test` | Run unit tests |
| `mvn package` | Create `.jar` / `.war` |
| `mvn install` | Put the artifact in local repository |
| `mvn deploy` | Upload the artifact to remote repository |
| `mvn clean package` | Clean, then build (most common) |
| `mvn clean install -DskipTests` | Build without running tests |
| `mvn -v` | Show Maven and Java version |

---

## 2.14 📦 Packaging Types


| Packaging | Output | Use |
| --- | --- | --- |
| `jar` | `.jar` | Libraries, Spring Boot apps |
| `war` | `.war` | Web apps for Tomcat / JBoss |
| `pom` | No file | Parent or multi-module projects |
| `ear` | `.ear` | Enterprise Java apps |

---

## 2.15 🏗️ Multi-Module Projects


A **parent pom** (`packaging: pom`) builds many **child modules** together.

```text
parent/
├── pom.xml          (packaging = pom, lists modules)
├── common/pom.xml
├── service/pom.xml
└── web/pom.xml
```

```xml
<modules>
  <module>common</module>
  <module>service</module>
  <module>web</module>
</modules>
```

---

## 2.16 🔗 Maven in CI/CD (Jenkins)


```text
Developer → Git → Jenkins → mvn clean package → SonarQube → mvn deploy → Nexus → Docker → Deploy
```

Example Jenkins stage:

```groovy
stage('Build') {
  steps {
    sh 'mvn clean package -DskipTests'
  }
}
stage('Unit Test') {
  steps {
    sh 'mvn test'
  }
}
```

Maven produces the **artifact**. Nexus **stores** it. SonarQube **checks** its quality.

---

## 2.17 🏗️ Real Example: Build and Store a Java App


### 🎯 Requirement

A team wants to **build a Java application automatically, check it, and store the final jar** so it can be deployed.

### 🏗 Architecture

```text
┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐
│ 🌿 GitHub │───►│ ⚙️ Jenkins│───►│ 📦 Maven  │───►│ 🔍 Sonar  │───►│ 🗄️ Nexus  │
│  (code)  │    │(pipeline)│    │ (build)  │    │ (quality)│    │(artifact)│
└──────────┘    └──────────┘    └──────────┘    └──────────┘    └──────────┘
```

### 🪜 Steps to Build It

```text
1. Developer pushes code to GitHub
2. Jenkins pulls the code
3. mvn clean package   → creates target/my-app-1.0.0.jar
4. mvn sonar:sonar     → code quality check
5. mvn deploy          → artifact goes to Nexus
6. Docker image is built using the jar
7. ✅ Same jar can be used in every environment
```

### ✅ Why This Is Better

| ❌ Manual Build | ✅ Maven Build |
| --- | --- |
| Different steps on each machine | Same steps everywhere |
| Manual library download | Automatic dependency download |
| Hard to repeat | One command |
| Easy to make mistakes | Repeatable and safe |

---

## 2.18 🧯 Troubleshooting


| Problem | Reason / Fix |
| --- | --- |
| `JAVA_HOME is not set` | Set `JAVA_HOME` to the JDK path |
| `Could not resolve dependencies` | Check internet, mirror URL, dependency version |
| `Compilation failure` | Java version mismatch or syntax error |
| `401 Unauthorized` on deploy | Wrong credentials; server `id` must match pom `distributionManagement` id |
| Old dependency used | Run `mvn clean install -U` (force update) |

---

## 2.19 📌 Maven Quick Revision


- 📦 Maven = **build + dependency management** tool for Java
- 📄 `pom.xml` = project description file
- 📦 GAV = `groupId : artifactId : version`
- 📦 Lifecycle: `validate → compile → test → package → verify → install → deploy`
- 🏢 `install` → local repo, `deploy` → remote repo
- 🗄️ Repositories: Local → Central → Remote (Nexus)
- 🔑 `settings.xml` = credentials, mirrors, proxy
- 🔨 Scopes: `compile`, `provided`, `runtime`, `test`

---

## 2.20 🧠⚡ Maven One-Line Memory


| Topic | Easy Memory |
| --- | --- |
| 📦 **Maven** | Build and dependency manager for Java |
| 📄 **pom.xml** | Project blueprint |
| 🏷️ **GAV** | Address of an artifact |
| 🔁 **Lifecycle** | Fixed ordered build steps |
| 🧩 **Plugin** | Does the real work of a phase |
| 🏠 **Local Repo** | Cache in `~/.m2` |
| 🏢 **Nexus** | Company storage for artifacts |

---

## 2.21 🗺️ Maven Learning Map


```text
Maven
 ├── Basics        → What, Why, Install
 ├── pom.xml       → GAV, Properties, Dependencies
 ├── Lifecycle     → clean, default, site
 ├── Plugins       → compiler, surefire, jar
 ├── Repositories  → Local, Central, Remote
 ├── Settings      → mirrors, credentials
 └── CI/CD         → Jenkins + SonarQube + Nexus
```

---

## 2.22 ⭐ Maven Final Memory


```text
How to build a Java project?              → mvn clean package
How to manage libraries?                  → <dependencies> in pom.xml
Where are libraries stored on my machine? → ~/.m2/repository
How to share the artifact with the team?  → mvn deploy to Nexus
```

> **Maven builds the Java project and manages its libraries using pom.xml.**


---

# ⚙️ PART 3 — Jenkins — CI/CD Automation

> **Jenkins = Automates Build → Test → Deploy (CI/CD)**

---

## 3.1 ⚙️ Jenkins Fundamentals


### 📖 What is Jenkins?

### 📌 Technical Definition

**Jenkins is an open-source automation server used to automate software development and delivery processes such as building, testing, and deploying applications.**

Jenkins is mainly used to implement **CI/CD in DevOps**.

Jenkins helps us automatically perform repetitive tasks whenever developers make changes to the code.

Jenkins is a tool that automatically:

- 🔨 Builds applications
- 🧪 Tests applications
- 📦 Packages applications
- 🚀 Deploys applications

Jenkins also connects different tools and automates the flow between them.

#### 🧠 Easy Memory

> **Jenkins = Automation Server + CI/CD**

---

---

### 🤔 Why Do We Use Jenkins?

In a software project, developers frequently make changes to the application.

Every time we perform build, testing, and deployment manually, it takes time and can cause mistakes.

**Jenkins automates these tasks.**

### ❌ Without Jenkins

```text
Developer
    ↓
Push Code
    ↓
Manually Build
    ↓
Manually Test
    ↓
Manually Deploy
```

### ✅ With Jenkins

```text
Developer
    ↓
GitHub
    ↓
Jenkins
    ↓
Build
    ↓
Test
    ↓
Package
    ↓
Deploy
```

### 🌟 Main Benefits

- Reduces manual work
- Saves time
- Reduces human errors
- Automates repetitive tasks
- Provides faster software delivery
- Helps implement CI/CD

#### 🧠 Easy Memory

> **Jenkins = Less Manual Work + Faster Delivery**

---

---

### ⚙️ Jenkins Features

Jenkins is an open-source automation server that can **Automate**:

- **build**
- **test**
- **package**
- **deployment activities**

and can connect **different tools**.

### ⚙️ Jenkins Use Cases

- Automating builds
- Running tests
- Packaging applications
- Triggering deployments
- Orchestrating CI/CD workflows
- Integrating source control and build tools

### ⭐ Advantages

- Reduces manual work
- Saves time
- Reduces human errors
- Automates repetitive tasks
- Supports CI/CD

### 🧪 Disadvantages / Practical Limitations

- Jenkins requires administration and maintenance
- Plugins add dependencies and can introduce compatibility/maintenance concerns
- Builds, workspaces, logs, and artifacts can consume significant disk space
- Security and permissions must be configured carefully

### ⚙️ Important Jenkins Terminology

See **Section 28 — Quick Revision** for the final terminology table and memory map.

---

## 3.2 ⚙️ CI/CD with Jenkins


CI/CD in Jenkins

### 📌 What is CI/CD?

CI/CD means automatically taking code from a developer's commit and:

```text
Build
  ↓
Test
  ↓
Check Quality
  ↓
Deliver / Deploy
```

CI/CD is the automatic process of building, testing, and deploying an application.

Jenkins is an automation tool that can implement a **CI/CD pipeline**.

---

### 🔵 CI — Continuous Integration

#### 🧠 Definition

**Continuous Integration** means developers frequently merge their code into a shared repository, and the code is automatically built and tested.

#### 💻 Example

```text
Developer
    ↓
Push Code
    ↓
GitHub
    ↓
Jenkins
    ↓
Build + Test
```

#### 🧠 Easy Memory

> **CI = Build + Test**

---

### 🟠 CD — Continuous Delivery

#### 🧠 Definition

**Continuous Delivery** means the application is automatically built, tested, and prepared for release.

It can require a **manual approval** before deployment.

```text
Build
  ↓
Test
  ↓
Package
  ↓
Prepare for Release
  ↓
Manual Approval
```

#### 🧠 Easy Memory

> **Continuous Delivery = Build + Test + Prepare for Release**

---

### 🟢 CD — Continuous Deployment

#### 🧠 Definition

**Continuous Deployment** means the application is automatically deployed to the target environment after successful testing.

No manual approval is required.

```text
Build
  ↓
Test
  ↓
Package
  ↓
Automatically Deploy
```

#### 🧠 Easy Memory

> **Continuous Deployment = Build + Test + Automatically Deploy**

---

### 📊 Simple Difference

| Concept | Flow |
|---|---|
| **CI** | Build + Test |
| **Continuous Delivery** | Build + Test + Prepare for Release |
| **Continuous Deployment** | Build + Test + Automatically Deploy |

#### 💡 Remember

```text
CI = Continuous Integration

CD = Continuous Delivery

CD = Continuous Deployment
```

---

---

---

## 3.3 🧱 Jenkins Architecture


Jenkins Architecture

### 📌 Jenkins Architecture

Jenkins can use a **Controller-Agent architecture** to manage and distribute build workloads.

```text
                    Jenkins Controller
                           │
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
          Agent 1       Agent 2       Agent 3
          Java Build    Testing       Other Work
```

#### 🧠 Easy Memory

> **Controller = Manages + Coordinates**
> 
> **Agent = Executes Tasks**

### 🔹 Controller

The **Jenkins Controller** is the central component that manages Jobs and Pipelines, schedules work, manages configuration, and assigns work to Agents.

### 🔹 Agent

A **Jenkins Agent** is a machine that executes tasks assigned by the Controller. Agents help distribute workloads.

### 🖥️ Node

A **Node** is a machine that Jenkins can use to execute work. The Controller and Agents are part of the Jenkins node model.

### 🔹 Executor

An **Executor** is a slot that allows a Jenkins node to run a build or task. A node can have multiple executors depending on its configuration and capacity.

### 🧪 Labels

A **Label** identifies agents with particular capabilities. A Pipeline can request an agent using a label.

Example:

```groovy
agent {
    label 'linux-agent'
}
```

### 🔑 SSH Agent Connection

A common setup is to connect a Jenkins Controller to a remote Agent using SSH credentials.

```text
Controller
   │
   │ SSH
   ↓
Agent
```

#### 🔄 Typical Flow

```text
1. Create SSH key pair
        ↓
2. Add public key to Agent
        ↓
3. Store private key in Jenkins Credentials
        ↓
4. Create Agent/Node in Jenkins
        ↓
5. Configure IP + credentials + label
        ↓
6. Pipeline selects the label
```


---

---

## 3.4 ⚙️ Jenkins Installation & Setup


Jenkins Installation & Setup

### 📌 Installation Environment

Jenkins can be installed on **Ubuntu/Linux**. A common practical setup uses an Ubuntu server.

#### 🔧 Main Setup Concepts

- Ubuntu/Linux
- Java
- Jenkins package
- Port `8080`
- Security Group / firewall access
- Jenkins service
- Initial administrator password

#### 💻 Basic Service Commands

```bash
sudo systemctl status jenkins
sudo systemctl start jenkins
sudo systemctl stop jenkins
sudo systemctl restart jenkins
```

#### 🔧 Initial Setup Flow

```text
Ubuntu
  ↓
Java
  ↓
Jenkins Installation
  ↓
Start Jenkins Service
  ↓
Port 8080
  ↓
Initial Password
  ↓
Unlock Jenkins
  ↓
Install Required Plugins
  ↓
Create Admin User
```

> AWS/EC2 concepts are covered separately.

---

---

## 3.5 ⏱️ Jenkins UI & Jobs


Jenkins Job

### 📌 Definition

A **Jenkins Job** is a task configured in Jenkins that tells Jenkins what work to perform.

A Jenkins Job is a task that Jenkins performs, such as:

- Building an application
- Testing an application
- Deploying an application

Jenkins Jobs are used to automate repetitive tasks.

### ⏱️ A Job Can

- Get code from Git/GitHub
- Build an application
- Run tests
- Run shell commands
- Create JAR/WAR files
- Create Docker images
- Deploy applications

---

### 📋 Types of Jenkins Jobs

#### 🔹 1. Freestyle Project

A simple job configured through the Jenkins UI.

#### 🔗 2. Pipeline

A CI/CD process defined as code using a `Jenkinsfile`.

#### 🔗 3. Multibranch Pipeline

Automatically manages pipelines for multiple Git branches.

---

### 💡 Example

Suppose we create a Job called:

```text
Java-Application-Build
```

It can perform:

```text
Get Code
   ↓
Build
   ↓
Test
   ↓
Create JAR
```

#### 🧠 Remember

```text
Jenkins = Automation Server

Job = Task given to Jenkins
```

---

---

Jenkins Build, Workspace & Console Output

### 🔨 Build

A **Jenkins Build** is an execution of a Jenkins Job or Pipeline.

A build may perform:

- Code checkout
- Compilation
- Testing
- Packaging
- Deployment

#### 💡 Simple Difference

```text
Job   = Task / Configuration
Build = Execution of that Job
```

### 📁 Workspace

The **Jenkins Workspace** is the working directory where Jenkins checks out source code and performs build/test operations for a Job.

```text
Jenkins
   ↓
Checkout Code
   ↓
Workspace
   ↓
Build
   ↓
Test
```

### 🖥️ Console Output

Console Output shows the logs produced while a build is running. It is one of the first places to inspect when a build fails.


---

---

## 3.6 🧩 Jenkins Plugins


Jenkins Plugin

### 📌 Definition

A **Jenkins Plugin** adds extra functionality to Jenkins and allows Jenkins to integrate with other tools.

### 💻 Examples

- Git Plugin
- Docker Plugin
- Kubernetes Plugin
- Maven-related plugins
- Cloud-related plugins

#### 💡 Simple Meaning

> **Plugin = Extra functionality for Jenkins**

Plugins allow Jenkins to work with many tools used in DevOps.

#### 🧠 Easy Memory

```text
Plugin
   ↓
Extra Functionality
   ↓
More Tool Integrations
```

---

---

### ⚙️ Plugin Installation / Update

Plugins are managed from Jenkins administration. Typical administration tasks include installing required plugins, updating plugins, reviewing dependencies, and removing unused plugins carefully.

### 🧩 Plugin Dependencies

A plugin can depend on other plugins. Dependency compatibility should be considered before updates or removals.

### 🧩 Common Jenkins Plugin Categories

- Source-control integration
- Pipeline functionality
- Credentials/security integration
- Build-tool integration
- Agent/node connectivity

---

## 3.7 🐙 Jenkins + Git / GitHub


### 🔹 SCM

**SCM (Source Code Management)** is the source-control system Jenkins uses to obtain application code. Git and GitHub are common examples.

Jenkins + Git

Jenkins can connect to Git repositories to get application source code.

### 🔄 Basic Flow

```text
Git Repository
      ↓
   Jenkins
      ↓
Get Latest Code
      ↓
    Build
```

#### 🧠 Remember

```text
Git
 ↓
Stores Code

Jenkins
 ↓
Automates Build / Test / Deploy
```


---

## 🐙 Jenkins + GitHub


GitHub is used to store and manage source code.

Jenkins can automatically get code from GitHub and start a Pipeline when changes are pushed.

### 🔄 Flow

```text
Developer
    ↓
Push Code
    ↓
GitHub
    ↓
Webhook
    ↓
Jenkins
    ↓
Build → Test → Deploy
```

#### 🧠 Remember

```text
GitHub → Stores source code

Jenkins → Automates the software delivery process
```

---

---

### 📁 Repository

The repository contains the application source code and can also contain the `Jenkinsfile`.

### 🔹 Checkout

**Checkout** means Jenkins retrieves the required source code into the build workspace.

### 📜 Jenkinsfile from Git

A Jenkinsfile can be stored in the Git repository so the Pipeline definition is version controlled. The detailed **Pipeline from SCM** concept is covered again in Section 18.

---

## 3.8 🔔 Jenkins Triggers


Jenkins Triggers

### 📌 Definition

A **Trigger** is an event or condition that starts a Jenkins Job or Pipeline.

---

### 🔔 1️⃣ Manual Trigger

A user starts the Job by clicking:

```text
Build Now
```

---

### 🔔 2️⃣ Webhook

GitHub can notify Jenkins when new code is pushed.

```text
Developer
    ↓
Push Code
    ↓
GitHub
    ↓
Webhook
    ↓
Jenkins
    ↓
Pipeline Starts
```

---

### 🔹 3️⃣ Schedule

A Job can run at a specific time.

Example:

```text
Every night
    ↓
Jenkins Job
```

---

### 🔹 4️⃣ Polling

Jenkins periodically checks the source repository for changes.

#### 🧠 Easy Memory

> **Trigger = What starts the Job/Pipeline?**

---

---

### 🔹 Poll SCM

With **Poll SCM**, Jenkins periodically checks the source repository for changes and can start a build when changes are detected.

---

## 3.9 🔗 Jenkins Pipeline Fundamentals


Jenkins Pipeline

### 📌 Definition

A **Jenkins Pipeline** is a series of automated steps used to automate the software delivery process, such as building, testing, and deploying an application.

It helps us automate the complete process.

A Jenkins Pipeline is used to:

- Build an application
- Test an application
- Package an application
- Deploy an application

The pipeline is usually written as code in a `Jenkinsfile`.

---

### 🔗 A Pipeline Can Contain

```text
Build
  ↓
Test
  ↓
Package
  ↓
Deploy
```

---

### ❓ Why Use Pipeline?

Pipeline helps us define the complete CI/CD workflow in an organized way.

#### 💻 Example

```text
Pipeline
   │
   ├── Build Stage
   │      └── Maven Build
   │
   ├── Test Stage
   │      └── Run Tests
   │
   └── Deploy Stage
          └── Deploy Application
```

#### 🧠 Easy Memory

> **Pipeline = Complete CI/CD Workflow**

---

---

### ⚙️ Groovy Basics for Jenkins

Jenkins Pipeline uses Groovy-based syntax. Common constructs include blocks such as `pipeline {}`, `stage {}`, `steps {}`, `node {}`, `try/catch`, variables, strings, and function calls.

> Here we focus on the Groovy syntax needed to read and write Jenkins Pipelines.

### 🏷️ Stage

### 📌 Definition

A **Stage** is a major section of a Jenkins Pipeline.

### 🏷️ Common Stages

```text
Build
Test
Package
Deploy
```

#### 💻 Example

```text
Pipeline
   ↓
Build Stage
   ↓
Test Stage
   ↓
Deploy Stage
```

Stages make the pipeline easier to understand and manage.

#### 🧠 Easy Memory

> **Stage = Major Section of a Pipeline**


---
### 🪜 Step

### 📌 Definition

A **Step** is an individual command or action performed inside a Stage.

#### 💻 Example 1

```text
Stage: Build
       ↓
Step: mvn clean package
```

#### 💻 Example 2

```text
Stage: Deploy
       ↓
Step: Run deployment command
```

### 🧠 Easy Difference

```text
Pipeline → Complete workflow

Stage    → Major section

Step     → Individual action
```

#### ⭐ Final Memory

> **Jenkins Pipeline = Pipeline → Stages → Steps**

---

---

---

## 3.10 🔗 Declarative Pipeline


### 📖 What is Declarative Pipeline?

A **Declarative Pipeline** uses a structured Pipeline syntax with `pipeline {}`, `agent`, `stages`, `stage`, and `steps` as its main structure.

#### 🧱 Basic Structure

```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
    }
}
```

#### 🏷️ Multiple Stages

```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps { echo 'Build' }
        }
        stage('Test') {
            steps { echo 'Test' }
        }
        stage('Package') {
            steps { echo 'Package' }
        }
    }
}
```

#### 🏷️ Stage View

The Pipeline stage view is used to understand the execution of individual stages and their status.

#### 🧠 Easy Memory

> **Declarative Pipeline = Structured Jenkins Pipeline syntax**

---

## 3.11 📝 Jenkinsfile Advanced Syntax


Jenkinsfile Advanced Syntax

This section extends the basic Jenkinsfile concepts with the Jenkins Pipeline constructs commonly used in real projects.

### 🔹 14.1 `agent`

Defines where the Pipeline or a stage runs.

```groovy
agent any
```

or:

```groovy
agent { label 'linux-agent' }
```

### 🌍 14.2 `environment`

Defines environment variables available to Pipeline steps.

```groovy
environment {
    APP_NAME = 'my-app'
}
```

### 🔤 14.3 `parameters`

Defines values that can be supplied when starting a build.

```groovy
parameters {
    string(name: 'VERSION', defaultValue: '1.0')
}
```

### 🔹 14.4 `options`

Controls Pipeline behavior and execution options.

Example use cases include build retention and timeouts.

### 🔹 14.5 `tools`

Declares tools that Jenkins should make available to the Pipeline when the relevant tool installations are configured.

### 🔹 14.6 `when`

Controls whether a stage should execute based on a condition.

```groovy
when {
    branch 'main'
}
```

### 📥 14.7 `input`

Pauses a Pipeline and waits for human input/approval before continuing.

### 🔹 14.8 `post`

Runs actions after a Pipeline or stage completes. Common conditions include:

- `always`
- `success`
- `failure`
- `unstable`

Example:

```groovy
post {
    always {
        echo 'Pipeline finished'
    }

    success {
        echo 'Build successful'
    }

    failure {
        echo 'Build failed'
    }
}
```

### 🔹 14.9 `timeout`

Stops execution when it exceeds a defined time limit.

### 🔹 14.10 `retry`

Retries a block when a step fails.

```groovy
retry(3) {
    sh 'some-command'
}
```

### 🔹 14.11 `parallel`

Runs independent branches concurrently.

```text
                 Pipeline
                    │
          ┌─────────┴─────────┐
          ↓                   ↓
       Unit Test          Security Test
          ↓                   ↓
          └─────────┬─────────┘
                    ↓
                  Deploy
```


---

---

## 3.12 ⚖️ Declarative vs Scripted Pipeline


Declarative vs Scripted Pipeline

### 🔗 Declarative Pipeline

Declarative Pipeline uses a structured syntax for defining the Pipeline. It is generally easier to read and is the primary style used in the notes.

```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
    }
}
```

### 🔗 Scripted Pipeline

Scripted Pipeline uses Groovy scripting more directly and provides greater programming flexibility.

```groovy
node {
    stage('Build') {
        echo 'Building...'
    }
}
```

### 💡 Simple Difference

| Declarative | Scripted |
|---|---|
| Structured syntax | More code-oriented |
| Easier to read | More flexible |
| Uses `pipeline {}` | Commonly uses `node {}` |
| Good default for many teams | Useful for complex Groovy logic |


---

---

## 3.13 🔤 Jenkins Environment Variables


Environment Variables

Environment variables allow values to be reused during Pipeline execution.

### 🔤 Jenkins Built-in Variables

Jenkins exposes predefined environment information to builds. A common way to access environment variables in Pipeline is through `env`.

Example:

```groovy
echo "Build number: ${env.BUILD_NUMBER}"
```

### 🔤 Custom Variables

```groovy
environment {
    APP_NAME = 'notes-app'
    ENV_NAME = 'production'
}
```

Then use them in steps:

```groovy
echo "Deploying ${env.APP_NAME}"
```


---

---

## 3.14 🔤 Jenkins Parameters


Parameterized Builds

A **Parameterized Build** allows a user to provide input when starting a Jenkins build.

### 🔤 Common Parameter Types

- String
- Choice
- Boolean
- Password/secret-oriented parameters where appropriate

#### 💻 Example

```groovy
parameters {
    string(name: 'VERSION', defaultValue: '1.0')
    choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'])
    booleanParam(name: 'RUN_TESTS', defaultValue: true)
}
```

The values can be accessed using `params`.

```groovy
echo "Version: ${params.VERSION}"
echo "Environment: ${params.ENVIRONMENT}"
```

#### 🔄 Flow

```text
User
  ↓
Build with Parameters
  ↓
Enter Values
  ↓
Jenkins Pipeline
  ↓
Use params.*
```


---

---

## 3.15 🔑 Jenkins Credentials


Jenkins Credentials

### 📌 Definition

**Jenkins Credentials** are used to securely store authentication information in Jenkins.

Examples include:

- Username/passwords
- API tokens
- SSH keys
- Secret text

Instead of writing passwords or tokens directly in the Jenkinsfile, we store them securely in **Jenkins Credentials** and use them when required.

#### 🔐 Concept

```text
Jenkinsfile
username = ?
password = ?
       ❌
       ↓
Jenkins Credentials
       ↓
Use When Required
```

#### 🧠 Easy Memory

> **Credentials = Secure Authentication Information**

---

---

### 🔑 Credentials ID

A **Credentials ID** identifies a stored Jenkins credential so a Pipeline/job can reference the required credential without hard-coding the secret itself.

### 🔑 Credential Binding / `withCredentials`

Credentials should be stored securely and used only when required. In Pipeline practice, credentials can be bound for a specific block rather than writing secrets directly in the Jenkinsfile.

```groovy
withCredentials([usernamePassword(
    credentialsId: 'app-creds',
    usernameVariable: 'USER',
    passwordVariable: 'PASS'
)]) {
    sh 'some-command'
}
```

---

## 3.16 📦 Jenkins + Maven


Jenkins + Maven

### 📌 Maven

Maven is a build and dependency management tool commonly used for Java applications.

Jenkins can execute Maven commands.

#### 💻 Example

```bash
mvn clean package
```

### 🔄 Flow

```text
GitHub
   ↓
Jenkins
   ↓
Maven
   ↓
Build
   ↓
Test
   ↓
JAR / WAR
```

#### 🧠 Remember

```text
Jenkins → Automation

Maven → Java Build
```

---

---

### 🔨 Build / Test / Package

A typical Maven-driven Jenkins flow is:

```text
Build
  ↓
Test
  ↓
Package
  ↓
JAR / WAR
```

### 🔹 JAR and WAR

- **JAR** — common Java application/package output
- **WAR** — Java web application archive

---

## 3.17 📦 Jenkins Artifacts


Jenkins Artifacts

### 📦 What is an Artifact?

An **artifact** is a build output produced by the build process, such as a JAR, WAR, ZIP, or another generated file.

```text
Source Code
    ↓
Build
    ↓
Test
    ↓
Package
    ↓
Artifact
```

### 📦 `archiveArtifacts`

Jenkins can archive selected build outputs so they can be accessed from the build record.

Example:

```groovy
post {
    success {
        archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    }
}
```

### ⚖️ Artifact vs Source Code

| Source Code | Artifact |
|---|---|
| Human-written application code | Generated build output |
| Input to the build | Output of the build |
| Example: `.java` files | Example: `.jar` / `.war` |

---

---

## 3.18 🔗 Jenkins Pipeline from SCM


Pipeline from SCM

A **Pipeline from SCM** loads the Jenkinsfile from a source-control repository rather than storing the entire Pipeline definition only in the Jenkins UI.

```text
Git Repository
     │
     ├── Application Code
     └── Jenkinsfile
             ↓
          Jenkins
             ↓
          Pipeline
```

#### 🤔 Why Use It?

- Pipeline definition is version controlled
- Jenkinsfile stays with application code
- Changes can be reviewed through source control
- Supports Pipeline as Code

---

---

## 3.19 🔗 Multibranch Pipeline


Multibranch Pipeline

A **Multibranch Pipeline** automatically discovers branches in a repository and can create Pipeline jobs for branches that contain a Jenkinsfile.

#### 🔹 Concept

```text
Git Repository
│
├── main
│    └── Jenkinsfile
│
├── develop
│    └── Jenkinsfile
│
└── feature/login
     └── Jenkinsfile
```

Jenkins can manage the Pipeline for each discovered branch.

#### 🤔 Why Use It?

- Branch-specific Pipelines
- Better CI for feature branches
- Jenkinsfile remains with the branch code
- Useful for Git-based development workflows


---

### 🌿 Branch Discovery

A Multibranch Pipeline discovers repository branches and can create/manage branch-specific Pipeline jobs when the relevant branch contains a Jenkinsfile.

### 🌿 Feature / Main / Develop Branches

```text
Repository
├── main
│   └── Jenkinsfile
├── develop
│   └── Jenkinsfile
└── feature/login
    └── Jenkinsfile
```

---

## 3.20 ⚙️ Jenkins Shared Libraries


Shared Libraries

**Jenkins Shared Libraries** provide reusable Pipeline code so teams do not repeat the same Groovy logic across many Jenkinsfiles.

### 🤔 Why Shared Libraries?

They help apply the **DRY (Don't Repeat Yourself)** principle.

### 🧱 Common Structure

```text
shared-library-repo/
│
├── vars/
│   ├── buildApp.groovy
│   └── deployApp.groovy
│
└── src/
```

A shared function can be called from Jenkinsfiles after the library is configured.

Example concept:

```groovy
@Library('my-shared-library') _

buildApp()
```


---

---

## 3.21 🔐 Jenkins Security


Jenkins Security

### 🔐 Authentication

Authentication answers:

> **Who are you?**

### 🔹 Authorization

Authorization answers:

> **What are you allowed to do?**

### 🔐 RBAC

**Role-Based Access Control (RBAC)** gives users permissions according to assigned roles.

Example:

```text
Admin
 ├── Manage Jenkins
 ├── Manage Jobs
 └── Manage Users

Developer
 ├── Build Jobs
 └── View Jobs

Viewer
 └── View Jobs
```

### 🔹 Least Privilege

Users should receive only the permissions required for their responsibilities.


---

### 🔹 User Management

Jenkins security also includes managing users and assigning the permissions required for their responsibilities.

---

## 3.22 ⚙️ Jenkins Failure Handling


Failure Handling

Real Jenkins Pipelines must handle failures safely and predictably.

### 🔹 `try / catch`

Used in scripted Groovy logic to catch exceptions and handle them.

```groovy
try {
    sh 'some-command'
} catch (err) {
    echo "Command failed"
}
```

### 🧯 `error`

Explicitly marks a Pipeline as failed.

### 🧯 `catchError`

Allows a Pipeline to catch an error and control the resulting build/stage status rather than immediately stopping all processing.

### 🔹 `retry`

Useful for transient failures:

```groovy
retry(3) {
    sh 'some-command'
}
```

### 🔹 `timeout`

Prevents a Pipeline from waiting forever.

#### 🔹 Failure Strategy

```text
Step
 ↓
Fails
 ↓
Can we retry? ── Yes → retry
 ↓ No
Handle / Mark Failure
 ↓
post { failure { ... } }
```


---

---

## 3.23 ⚙️ Jenkins Administration


Jenkins Administration

Jenkins administration includes maintaining the Jenkins Controller, jobs, plugins, storage, logs, and configuration.

### 📥 Important Areas

#### 🌐 Service Management

```bash
sudo systemctl status jenkins
sudo systemctl restart jenkins
```

#### 📜 Logs

Logs help identify service startup, plugin, configuration, and runtime problems.

#### 🧩 Plugin Management

- Install plugins
- Update plugins
- Review dependencies
- Remove unused plugins carefully

#### 🔹 Disk Space

Jenkins can consume significant storage through builds, workspaces, logs, and archived artifacts.

#### 🔨 Build Cleanup

Old builds can be removed using appropriate build retention policies.

#### 🗂️ Workspace Cleanup

Unused workspaces can consume disk space and sometimes cause stale-file problems.

#### 🔹 Backup / Restore

A Jenkins backup strategy should protect important Jenkins configuration and job data.

#### ⚖️ Restart vs Reload

- **Restart:** restarts the Jenkins service/process.
- **Reload:** reloads configuration without performing a full service restart where supported.

---

---

## 3.24 🧯 Jenkins Troubleshooting


Jenkins Troubleshooting


### 🌐 1. Jenkins Service Not Starting

Check:

```bash
sudo systemctl status jenkins
sudo journalctl -u jenkins
```

Check Java compatibility, configuration, permissions, and logs.

### 🔹 2. Agent Offline

Check:

- Agent connectivity
- SSH credentials
- Network/security rules
- Java/runtime availability
- Agent logs
- Label configuration

### 🌿 3. Git Checkout Failure

Check:

- Repository URL
- Credentials
- Network access
- Branch name
- Git installation/configuration

### 🔐 4. Permission Denied

Check file ownership, permissions, user identity, and whether the Jenkins process has access to the required resource.

### 🧯 5. Credentials Error

Check:

- Credential ID
- Credential type
- Credential scope
- Whether the Pipeline references the correct ID

### 🔔 6. Webhook Not Triggering

Check:

```text
GitHub
  ↓
Webhook Configuration
  ↓
Payload URL
  ↓
Network Reachability
  ↓
Jenkins Job Trigger Configuration
  ↓
Build
```

### 🔗 7. Pipeline Failure

Start with **Console Output**, identify the failing stage/step, then inspect the command and environment.

### 🔹 8. Disk Full

Check disk usage and clean unnecessary builds/workspaces/artifacts according to the retention policy.

#### 🧠 Troubleshooting Rule

> **First identify WHERE it failed → then identify WHY → then fix the root cause.**

---

---

## 3.25 🔄 Complete Jenkins CI/CD Workflow


Complete Jenkins CI/CD Workflow

This is the Jenkins-focused view of a typical workflow. Tool-specific details are intentionally kept outside this README.

```text
Developer
    ↓
Git Repository
    ↓
Webhook / Trigger
    ↓
Jenkins Controller
    ↓
Select Agent
    ↓
Checkout Code
    ↓
Build
    ↓
Test
    ↓
Package
    ↓
Create Artifact
    ↓
Post Actions / Notifications
    ↓
Deployment Trigger
```

### ⚙️ Jenkins Responsibilities

```text
Trigger
   ↓
Orchestrate
   ↓
Execute Steps
   ↓
Track Status
   ↓
Show Logs
   ↓
Store Build Information
```

#### 🧠 Big Picture

> **Jenkins is the automation/orchestration layer.**

Docker, Kubernetes, AWS, registries, security scanners, and deployment platforms are external tools that Jenkins can invoke or integrate with.

---

---

## 3.26 🧪 Jenkins Practical Commands


Important Jenkins Commands

### ⚙️ ▶️ Start Jenkins

```bash
sudo systemctl start jenkins
```

**Purpose:** Start Jenkins service.

---

### ⏹️ Stop Jenkins

```bash
sudo systemctl stop jenkins
```

**Purpose:** Stop Jenkins service.

---

### 🔄 Restart Jenkins

```bash
sudo systemctl restart jenkins
```

**Purpose:** Restart Jenkins service.

---

### 🔍 Check Jenkins Status

```bash
sudo systemctl status jenkins
```

**Purpose:** Check Jenkins service status.

---

### 🚀 Enable Jenkins at Boot

```bash
sudo systemctl enable jenkins
```

**Purpose:** Start Jenkins automatically when the system boots.

---

### ☕ Maven Build

```bash
mvn clean package
```

**Purpose:** Build a Java application using Maven.

It can:

```text
Clean
  ↓
Compile
  ↓
Test
  ↓
Package
```

#### 🧠 Quick Command Memory

| Command | Purpose |
|---|---|
| `sudo systemctl start jenkins` | Start Jenkins |
| `sudo systemctl stop jenkins` | Stop Jenkins |
| `sudo systemctl restart jenkins` | Restart Jenkins |
| `sudo systemctl status jenkins` | Check Jenkins status |
| `sudo systemctl enable jenkins` | Start Jenkins automatically at boot |
| `mvn clean package` | Maven build |

---

---

---

---

## 3.27 📌 Quick Revision


Important Jenkins Terms

| Term | Meaning |
|---|---|
| **Jenkins** | Automation Server |
| **Job** | Task configured in Jenkins |
| **Pipeline** | Complete CI/CD workflow |
| **Stage** | Major section of Pipeline |
| **Step** | Individual action |
| **Jenkinsfile** | Pipeline as Code |
| **Controller** | Manages Jenkins |
| **Agent** | Executes tasks |
| **Plugin** | Adds functionality |
| **Workspace** | Working directory |
| **Trigger** | Starts a Job/Pipeline |
| **Build** | Build process / execution |
| **Artifact** | Output produced by a build |
| **Webhook** | Sends event notification to Jenkins |

#### 🧠 Remember


---

---

### 💻 Important Commands

See **Section 26 — Jenkins Practical Commands**.

### 📝 Important Jenkinsfile Syntax

```text
pipeline      → Pipeline definition
agent         → Where it runs
stages        → Major sections
stage         → One stage
steps         → Actions
environment   → Variables
parameters    → User input
options       → Pipeline behavior
tools         → Configured tools
when          → Condition
input         → Human input/approval
post          → After execution
timeout       → Time limit
retry         → Retry failed block
parallel      → Concurrent execution
```

### ⚖️ Important Differences

```text
Job      = Task / configuration
Build    = Execution
Stage    = Major section
Step     = Individual action
Agent    = Executes work
Controller = Manages / coordinates
Workspace = Working directory
Artifact = Build output
Trigger  = Starts Job/Pipeline
```


---

---

### 🌳 Final Jenkins Study Tree

```text
JENKINS
│
├── 1. Jenkins Fundamentals
├── 2. CI/CD with Jenkins
├── 3. Jenkins Architecture
├── 4. Jenkins Installation & Setup
├── 5. Jenkins UI & Jobs
├── 6. Jenkins Plugins
├── 7. Jenkins + Git / GitHub
├── 8. Jenkins Triggers
├── 9. Jenkins Pipeline Fundamentals
├── 10. Declarative Pipeline
├── 11. Jenkinsfile Advanced Syntax
├── 12. Declarative vs Scripted Pipeline
├── 13. Jenkins Environment Variables
├── 14. Jenkins Parameters
├── 15. Jenkins Credentials
├── 16. Jenkins + Maven
├── 17. Jenkins Artifacts
├── 18. Jenkins Pipeline from SCM
├── 19. Multibranch Pipeline
├── 20. Jenkins Shared Libraries
├── 21. Jenkins Security
├── 22. Jenkins Failure Handling
├── 23. Jenkins Administration
├── 24. Jenkins Troubleshooting
├── 25. Complete Jenkins CI/CD Workflow
├── 26. Jenkins Practical Commands
└── 27. Quick Revision
```


---

# 🔍 PART 4 — SonarQube — Code Quality and Security

> **SonarQube = Checks Code Quality and Security Before Release**

---

## 4.1 🔍 What is SonarQube?


> **SonarQube = Code Quality and Security Inspection Platform**

SonarQube **reads your source code (without running it) and finds problems** such as bugs, security weaknesses, bad code and missing tests. This is called **static code analysis**.

### 🔍 We can use SonarQube to:

- 🐞 Find bugs before release.
- 🔐 Find security vulnerabilities.
- 🧹 Find code smells (hard-to-maintain code).
- 📋 Find duplicated code.
- 🧪 Check how much code is covered by tests.
- 🚦 Stop bad code using a Quality Gate.

### ⚙️ It Provides components such as:

- 🔬 Sonar Scanner
- 🖥️ SonarQube Server (dashboard)
- 🗄️ Database
- 🚦 Quality Gate

to check and report code quality.

#### 🏗 SonarQube Basic Flow

```text
💻 Source Code
      │
      ▼
🔬 Sonar Scanner
      │
      ▼
🖥️ SonarQube Server
      │
      ▼
📊 Report + 🚦 Quality Gate (✅ Pass / ❌ Fail)
```

#### 🧠 Easy Memory

> **SonarQube = Teacher Who Checks Your Code Homework**

#### ⚠ Important

> **SonarQube analyzes code, it does not run it.**

> **A failed Quality Gate should stop the pipeline.**

---

## 4.2 🤔 Why Do We Use SonarQube?


Suppose many developers push code every day.

### ❌ Without SonarQube

```text
💻 Code Goes Straight to Production
            ↓
🐞 Bugs and Security Holes Are Found by Users
            ↓
💸 Fixing Costs More Time and Money
```

### ✅ With SonarQube

```text
💻 Developer Pushes Code
 ↓
🔍 SonarQube Checks It Automatically
 ↓
🚦 Quality Gate Pass / Fail
 ↓
✅ Only Good Code Moves Forward
```

#### ⭐ Main Reasons

- 🐞 Find bugs and security problems early
- 🧹 Keep code clean and easy to maintain
- 🚦 Block bad code with a Quality Gate
- 📊 Track quality over time with a dashboard
- 🌍 Works with many languages (Java, Python, JavaScript, C#, Go ...)
- ⚙️ Easy to add inside a Jenkins pipeline

---

## 4.3 🧰 What Does SonarQube Provide?


SonarQube provides:

- 🐞 Bug Detection
- 🔐 Vulnerability Detection
- 🔥 Security Hotspots
- 🧹 Code Smells
- 📋 Duplication Check
- 🧪 Coverage Report
- 🚦 Quality Gate
- 📏 Quality Profiles and Rules

| 🧰 Feature | 💡 Meaning |
| --- | --- |
| 🐞 Bug | Code that can fail at runtime |
| 🔐 Vulnerability | Security weakness that can be attacked |
| 🔥 Security Hotspot | Sensitive code that needs manual review |
| 🧹 Code Smell | Code that works but is hard to maintain |
| 📋 Duplication | Copy-pasted code |
| 🧪 Coverage | Percentage of code tested |
| 🚦 Quality Gate | Pass / Fail rule for a project |

---

## 4.4 🧱 SonarQube Architecture


```text
┌──────────────┐     ┌──────────────────┐     ┌────────────────┐
│ Sonar Scanner│ ──► │ SonarQube Server │ ──► │   Database     │
│ (on CI node) │     │  (Web + Compute  │     │ (PostgreSQL)   │
└──────────────┘     │   + Search)      │     └────────────────┘
                     └──────────────────┘
                              ▲
                              │ Browser (Dashboard)
```

| Component | Role |
| --- | --- |
| **Scanner** | Analyzes code and sends the result to the server |
| **Server** | Processes results, shows dashboard, applies Quality Gate |
| **Database** | Stores analysis history and settings |

---

## 4.5 ⚙️ Installation (Docker Method)


```bash
docker run -d --name sonarqube -p 9000:9000 sonarqube:community
```

- 🖥️ Open `http://<server-ip>:9000`
- 🔒 Default login: `admin` / `admin` (you must change the password on first login)
- 🔹 Production setup should use an **external PostgreSQL database**

> ⚠️ Server needs enough memory. On Linux, `vm.max_map_count` must be at least `524288`.

---

## 4.6 📁 Projects, Tokens and Keys


- 🔍 **Project** = one codebase analyzed in SonarQube
- 🔑 **Project Key** = unique ID of the project
- 🔒 **Token** = secure replacement of a password for scanners / CI tools

Create a token: `My Account → Security → Generate Token`.

---

## 4.7 🔬 Sonar Scanner


Scanner is the client that analyzes the code.

`sonar-project.properties` (generic projects):

```properties
sonar.projectKey=my-app
sonar.projectName=My App
sonar.sources=src
sonar.host.url=http://sonar.example.com:9000
sonar.token=<token>
```

Run:

```bash
sonar-scanner
```

For **Maven** projects:

```bash
mvn clean verify sonar:sonar \
  -Dsonar.projectKey=my-app \
  -Dsonar.host.url=http://sonar.example.com:9000 \
  -Dsonar.token=$SONAR_TOKEN
```

---

## 4.8 📊 Issue Types and Severity


| Type | Meaning |
| --- | --- |
| 🐞 Bug | Probably a mistake that can break the app |
| 🔐 Vulnerability | Security risk that can be attacked |
| 🔥 Security Hotspot | Needs a human to decide if it is safe |
| 🧹 Code Smell | Maintainability problem |

Severity levels: **Blocker, Critical, Major, Minor, Info** (newer versions also show impact on Security / Reliability / Maintainability).

---

## 4.9 🚦 Quality Gate


A **Quality Gate** is a set of conditions. If the code does not meet them, the gate **fails**.

Example conditions (on new code):

- 🧪 Coverage ≥ 80%
- 📋 Duplicated lines < 3%
- 🐞 No new Bugs
- 🔐 No new Vulnerabilities

```text
Analysis → Quality Gate → ✅ Passed → continue pipeline
                       └→ ❌ Failed → stop pipeline
```

---

## 4.10 📏 Quality Profiles and Rules


- ⚠️ **Rule** = one check (e.g. "do not leave unused variables")
- 🚦 **Quality Profile** = a group of rules for one language
- 🔍 Each language has a default profile (e.g. "Sonar way")

---

## 4.11 🆕 New Code vs Overall Code


- 🔢 **New Code** = code changed recently (since last version / N days)
- 🔹 **Overall Code** = the whole project

Best practice: use the Quality Gate on **New Code** ("Clean as You Code"), so old issues do not block new work.

---

## 4.12 🔗 SonarQube with Jenkins


```text
Git → Jenkins → Build → Test → SonarQube Analysis → Quality Gate → Package → Deploy
```

Setup:

1. Install **SonarQube Scanner** plugin in Jenkins
2. Add the Sonar token in **Jenkins Credentials**
3. Add the server in `Manage Jenkins → System → SonarQube servers`
4. Use `withSonarQubeEnv` in the pipeline

```groovy
stage('SonarQube Analysis') {
  steps {
    withSonarQubeEnv('sonar-server') {
      sh 'mvn clean verify sonar:sonar'
    }
  }
}
stage('Quality Gate') {
  steps {
    timeout(time: 5, unit: 'MINUTES') {
      waitForQualityGate abortPipeline: true
    }
  }
}
```

> The server calls back Jenkins using a **webhook** when the analysis is done. Configure it in `SonarQube → Administration → Webhooks`.

---

## 4.13 🏗️ Real Example: Quality Check Before Deploy


### 🎯 Requirement

The team wants **only good-quality, tested code** to reach production.

### 🏗 Architecture

```text
┌──────────┐   ┌──────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────┐
│ 🌿 GitHub │──►│ ⚙️ Jenkins│──►│ 🔬 Scanner    │──►│ 🔍 SonarQube  │──►│ 🚦 Quality│
│  (code)  │   │ (build)  │   │ (analysis)   │   │  (server)    │   │   Gate   │
└──────────┘   └──────────┘   └──────────────┘   └──────────────┘   └──────────┘
```

### 🪜 Steps to Build It

```text
1. Developer pushes code to GitHub
2. Jenkins builds with Maven and runs unit tests
3. Sonar Scanner sends the result to SonarQube
4. ❌ Quality Gate fails (coverage 55% < 80%)
5. Pipeline stops, developer gets a failure message
6. Developer adds tests and fixes issues, pushes again
7. ✅ Quality Gate passes → artifact goes to Nexus → deployed
```

### ✅ Why This Is Better

| ❌ No Code Check | ✅ With SonarQube |
| --- | --- |
| Bugs found in production | Bugs found before release |
| Security holes unknown | Vulnerabilities reported |
| Quality depends on person | Same rules for everyone |
| No history | Dashboard shows trend |

---

## 4.14 🧯 Troubleshooting


| Problem | Reason / Fix |
| --- | --- |
| Server stops at startup | Low memory or `vm.max_map_count` too low |
| `Not authorized` | Wrong or expired token |
| Coverage shows 0% | Coverage report path not given to Sonar (e.g. JaCoCo) |
| Pipeline waits forever at Quality Gate | Webhook to Jenkins not configured |
| Wrong `projectKey` | Key must match the project in SonarQube |

---

## 4.15 📌 SonarQube Quick Revision


- 🔍 SonarQube = **static code analysis** and quality platform
- 🧪 Finds **Bugs, Vulnerabilities, Hotspots, Code Smells, Duplications, Coverage gaps**
- 🖥️ **Scanner** analyzes → **Server** shows result → **Database** stores it
- 🚦 **Quality Gate** decides pass / fail
- 🔑 **Token** is used for authentication in CI
- ⚙️ Works best with Jenkins using `withSonarQubeEnv` + `waitForQualityGate`

---

## 4.16 🧠⚡ SonarQube One-Line Memory


| Topic | Easy Memory |
| --- | --- |
| 🔍 **SonarQube** | Code quality and security checker |
| 🔬 **Scanner** | Reads the code and sends the report |
| 🚦 **Quality Gate** | Pass / Fail rule for code |
| 🐞 **Bug** | Can break the app |
| 🔐 **Vulnerability** | Can be attacked |
| 🧹 **Code Smell** | Hard-to-maintain code |
| 🔑 **Token** | Password for scanners |

---

## 4.17 🗺️ SonarQube Learning Map


```text
SonarQube
 ├── Basics        → What, Why, Architecture
 ├── Setup         → Docker, Database, Token
 ├── Analysis      → Scanner, Maven, sonar-project.properties
 ├── Results       → Bugs, Vulnerabilities, Smells, Coverage
 ├── Control       → Rules, Quality Profile, Quality Gate
 └── CI/CD         → Jenkins, Webhook, Pipeline stage
```

---

## 4.18 ⭐ SonarQube Final Memory


```text
How to check code quality automatically?   → SonarQube
How to analyze a project?                  → Sonar Scanner / mvn sonar:sonar
How to stop bad code from going further?   → Quality Gate
How to connect with Jenkins?               → withSonarQubeEnv + waitForQualityGate
```

> **SonarQube checks code quality and security, and the Quality Gate decides whether the code is good enough to move forward.**


---

# 🗄️ PART 5 — Nexus Repository — Artifact Repository Manager

> **Nexus = Warehouse for Build Artifacts and Dependencies**

---

## 5.1 🗄️ What is Nexus Repository?


> **Nexus = Repository Manager for Build Artifacts**

Nexus Repository (by Sonatype) is a tool that **stores, organizes and serves artifacts and dependencies** such as Maven jars, npm packages, Docker images and more.

### 🔹 We can use Nexus to:

- 📦 Store our own build artifacts (`.jar`, `.war`, `.zip`).
- 🔄 Cache libraries from the internet (proxy).
- 🐳 Keep a private Docker registry.
- 🔐 Control who can read or upload.
- 🧹 Delete old artifacts automatically.

### ⚙️ It Provides components such as:

- 🏠 Hosted Repositories
- 🔄 Proxy Repositories
- 🔗 Group Repositories
- 👥 Users, Roles and Privileges

to store and share artifacts safely.

#### 🏗 Nexus Basic Flow

```text
⚙️ Jenkins / 📦 Maven
        │ upload
        ▼
   🗄️ Nexus Repository
        │ download
        ▼
👩‍💻 Developers / 🚀 Deployment Servers
```

#### 🧠 Easy Memory

> **Nexus = Company Warehouse for Artifacts**

#### ⚠ Important

> **A Release version cannot be overwritten. A Snapshot version can be updated.**

---

## 5.2 🤔 Why Do We Use Nexus?


Suppose many projects build artifacts and need many libraries.

### ❌ Without Nexus

```text
📁 Artifacts Kept on Random Servers / Laptops
            ↓
🌍 Every Build Downloads from the Internet
            ↓
🐌 Slow Builds + ❓ No Version Control of Artifacts
```

### ✅ With Nexus

```text
🗄️ One Trusted Place for All Artifacts
 ↓
🔄 Libraries Cached Locally (Fast Builds)
 ↓
🔐 Access Control + Version History
 ↓
✅ Same Artifact in Every Environment
```

#### ⭐ Main Reasons

- 🏢 Keep one trusted place for all artifacts
- ⚡ Faster builds because libraries are cached
- 🔒 Keep private company artifacts private
- 🕓 Keep every version for rollback
- 🔐 Control who can read and upload
- 🌐 Builds keep working even if Maven Central is slow

---

## 5.3 🧰 What Does Nexus Provide?


Nexus provides:

- 📦 Artifact Storage
- 🔄 Proxy of Remote Repositories
- 🔗 Group Repositories
- 🐳 Docker Registry
- 🔐 Security (Users, Roles, Privileges)
- 🧹 Cleanup Policies
- 🔎 Search and Browse

| 🧰 Feature | 💡 Meaning |
| --- | --- |
| 📦 Artifact storage | Store jar, war, zip, npm, docker, pypi etc. |
| 🔄 Proxy | Cache from remote repositories (e.g. Maven Central) |
| 🔗 Group | One URL for many repositories |
| 🔐 Security | Users, roles, privileges |
| 🧹 Cleanup policies | Delete old artifacts automatically |
| 🔎 Search | Find artifacts in the UI |

---

## 5.4 🧱 Repository Types


| Type | Meaning | Example |
| --- | --- | --- |
| 🏠 **Hosted** | Stores **your own** artifacts | `maven-releases`, `maven-snapshots` |
| 🔄 **Proxy** | Cache of a **remote** repository | `maven-central` |
| 🔗 **Group** | **Combines** hosted + proxy under one URL | `maven-public` |

```text
maven-public (group)
 ├── maven-releases   (hosted)
 ├── maven-snapshots  (hosted)
 └── maven-central    (proxy → repo1.maven.org)
```

---

## 5.5 🧬 Repository Formats


Nexus supports many formats: **Maven2, npm, Docker, PyPI, NuGet, Raw, APT, Yum, Helm** and others.

| Format | Used for |
| --- | --- |
| Maven2 | Java artifacts |
| Docker | Container images |
| npm | JavaScript packages |
| Raw | Any file (zip, scripts) |

---

## 5.6 🔁 Release vs Snapshot


| Policy | Meaning |
| --- | --- |
| **Release** | Final version, cannot be overwritten (e.g. `1.0.0`) |
| **Snapshot** | Development version, can be updated (e.g. `1.0.0-SNAPSHOT`) |

Maven decides the repository from the **version name** in `pom.xml`.

---

## 5.7 ⚙️ Installation (Docker Method)


```bash
docker run -d --name nexus -p 8081:8081 sonatype/nexus3
```

- 🖥️ Open `http://<server-ip>:8081`
- 🗄️ Admin password for first login: `docker exec nexus cat /nexus-data/admin.password`
- 🗄️ Keep data in a **volume** (`/nexus-data`) so it is not lost

```bash
docker run -d --name nexus -p 8081:8081 -v nexus-data:/nexus-data sonatype/nexus3
```

---

## 5.8 👥 Users, Roles and Privileges


```text
Privilege → Role → User
```

- 🔐 **Privilege** = one permission (read, add, edit, delete)
- 🧱 **Role** = group of privileges
- 🧱 **User** = person or tool with roles

Best practice: create a separate **deployment user** for Jenkins instead of using `admin`.

---

## 5.9 📤 Uploading Artifacts with Maven


In `pom.xml`:

```xml
<distributionManagement>
  <repository>
    <id>nexus-releases</id>
    <url>http://nexus.example.com:8081/repository/maven-releases/</url>
  </repository>
  <snapshotRepository>
    <id>nexus-snapshots</id>
    <url>http://nexus.example.com:8081/repository/maven-snapshots/</url>
  </snapshotRepository>
</distributionManagement>
```

In `~/.m2/settings.xml` (the `id` must match):

```xml
<servers>
  <server>
    <id>nexus-releases</id>
    <username>deploy-user</username>
    <password>${env.NEXUS_PASSWORD}</password>
  </server>
  <server>
    <id>nexus-snapshots</id>
    <username>deploy-user</username>
    <password>${env.NEXUS_PASSWORD}</password>
  </server>
</servers>
```

Deploy:

```bash
mvn clean deploy
```

---

## 5.10 📥 Downloading Dependencies from Nexus


Use Nexus as a **mirror** in `settings.xml`:

```xml
<mirrors>
  <mirror>
    <id>nexus</id>
    <mirrorOf>*</mirrorOf>
    <url>http://nexus.example.com:8081/repository/maven-public/</url>
  </mirror>
</mirrors>
```

Now all dependency requests go to Nexus first. Nexus downloads from Maven Central only once and caches it.

---

## 5.11 🐳 Docker Registry in Nexus


Nexus can work as a **private Docker registry**.

```bash
docker login nexus.example.com:8082
docker tag my-app:1.0 nexus.example.com:8082/my-app:1.0
docker push nexus.example.com:8082/my-app:1.0
docker pull nexus.example.com:8082/my-app:1.0
```

> A Docker hosted repository needs its **own HTTP/HTTPS port** (e.g. 8082).

---

## 5.12 🧹 Cleanup Policies and Storage


Old snapshots can fill the disk.

- 🧹 Create a **Cleanup Policy** (e.g. delete components not downloaded for 30 days)
- 🏢 Attach it to a repository
- 💾 Run the **Compact blob store** task to free disk space

Blob Store = the place on disk where Nexus keeps files.

---

## 5.13 🔗 Nexus in CI/CD


```text
Git → Jenkins → Maven Build → SonarQube → mvn deploy → Nexus → Docker Build → Kubernetes
```

```groovy
stage('Publish to Nexus') {
  steps {
    withCredentials([string(credentialsId: 'nexus-pass', variable: 'NEXUS_PASSWORD')]) {
      sh 'mvn deploy -DskipTests'
    }
  }
}
```

---

## 5.14 🏗️ Real Example: Store and Reuse a Build


### 🎯 Requirement

The team wants to **build once and deploy the same artifact to Test, Stage and Prod**, and be able to roll back.

### 🏗 Architecture

```text
┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐
│ ⚙️ Jenkins│───►│ 📦 Maven  │───►│ 🗄️ Nexus  │───►│ 🚀 Deploy │
│(pipeline)│    │ (build)  │    │(artifact)│    │ Test/Prod│
└──────────┘    └──────────┘    └──────────┘    └──────────┘
```

### 🪜 Steps to Build It

```text
1. Jenkins builds my-app-1.0.0.jar
2. mvn deploy uploads it to maven-releases in Nexus
3. Ansible / Docker job downloads the same jar from Nexus
4. Same artifact goes to Test, Stage and Prod (no rebuild)
5. ❌ If Prod fails, version 0.9.0 is taken again from Nexus
6. ✅ Rollback is quick and safe
```

### ✅ Why This Is Better

| ❌ Rebuild for Each Environment | ✅ One Artifact from Nexus |
| --- | --- |
| Builds can differ | Exactly the same file everywhere |
| Hard to roll back | Old versions always available |
| Slow | Fast |
| Hard to audit | Version history is kept |

---

## 5.15 🧯 Troubleshooting


| Problem | Reason / Fix |
| --- | --- |
| `401 Unauthorized` | Wrong credentials, or `server id` does not match pom |
| `403 Forbidden` / `400 Bad Request` on redeploy | Release repo does not allow overwrite; change the version |
| Snapshot goes to release repo (or opposite) | Version name does not match the repository policy |
| Disk full | Add cleanup policy and compact blob store |
| Docker push fails | HTTP connector port missing or insecure registry not allowed |

---

## 5.16 📌 Nexus Quick Revision


- 🗄️ Nexus = **repository manager** for artifacts
- 🖥️ Types: **Hosted** (own), **Proxy** (cache), **Group** (combined URL)
- 🏷️ **Release** = fixed version, **Snapshot** = changing version
- 📦 Maven uploads using `distributionManagement` + `settings.xml` credentials
- 🗄️ Use Nexus as a **mirror** to speed up and secure builds
- 🐳 Can also be a **Docker registry**, npm and PyPI repository
- 🧹 Use cleanup policies to save disk

---

## 5.17 🧠⚡ Nexus One-Line Memory


| Topic | Easy Memory |
| --- | --- |
| 🗄️ **Nexus** | Warehouse for artifacts |
| 🏠 **Hosted** | Our own artifacts |
| 🔄 **Proxy** | Cache of remote repo |
| 🔗 **Group** | One URL for many repos |
| 🔁 **Release** | Final, cannot change |
| 📸 **Snapshot** | Development, can change |
| 🧹 **Cleanup Policy** | Delete old artifacts |

---

## 5.18 🗺️ Nexus Learning Map


```text
Nexus
 ├── Basics        → What, Why
 ├── Repositories  → Hosted, Proxy, Group
 ├── Formats       → Maven, Docker, npm, Raw
 ├── Security      → Users, Roles, Privileges
 ├── Usage         → mvn deploy, mirror, docker push
 ├── Maintenance   → Cleanup, Blob Store
 └── CI/CD         → Jenkins → Nexus → Deploy
```

---

## 5.19 ⭐ Nexus Final Memory


```text
Where to store build artifacts?            → Nexus
How to speed up dependency download?       → Proxy / mirror in Nexus
How to keep a private Docker registry?     → Docker hosted repo in Nexus
How to avoid rebuilding for each env?      → Promote the same artifact from Nexus
```

> **Nexus stores and manages artifacts so every environment uses the same trusted build.**


---

# 🐳 PART 6 — Docker — Containers

> **Docker = Package the App and Its Dependencies into a Container**

---

## 6.1 📖 What is Docker?


### 📌 Technical Definition

Docker is an **open-source containerization platform** that is used to **package, deploy, and run applications** along with their dependencies in isolated containers.

Docker is mainly used in DevOps to implement **consistent application deployment.**

### 💡 Simple Definition

Docker packages an application and everything it needs into a container, so the application can run consistently on different machines.

### 🧠 Easy Example

#### ❌ Without Docker

```text
Application
    ↓
Needs Java
    ↓
Needs Libraries
    ↓
Needs Configuration
    ↓
Needs Dependencies
    ↓
"Works on my machine"
```

#### ✅ With Docker

```text
Application
     +
Dependencies
     +
Libraries
     +
Configuration
        ↓
   Docker Image
        ↓
     Container
```


---

## 6.2 🤔 Why Do We Use Docker?


An application may work on a developer's laptop but fail on another server because the environment is different.

Docker helps solve this problem by packaging the application with its required environment.

### ❌ Without Docker

```text
Developer Machine
       ↓
Application Works
       ↓
Production Server
       ↓
Different Environment
       ↓
Application May Fail
```

### ✅ With Docker

```text
Application + Dependencies
          ↓
      Docker Image
          ↓
       Container
          ↓
    Dev / Test / Production
```

### 🌟 Main Benefits

- ✅ Consistent application environment
- ⚡ Faster application deployment
- 🪶 Lightweight compared to virtual machines
- 📦 Easy to package and distribute applications
- 📈 Helps scale applications
- 🔄 Useful in CI/CD
- ☁️ Works well with cloud and Kubernetes

#### 🧠 Easy Memory

> **Docker = Same application environment across different machines**

---

## 6.3 ⚙️ What Does Docker Provide?


Docker provides important components such as:

- ⚙️ Docker Engine
- 🖼️ Docker Images
- 📦 Docker Containers
- 📄 Dockerfile
- 🗄️ Docker Registry
- 🌐 Docker Hub
- 💾 Docker Volumes
- 🌐 Docker Networks
- 🧩 Docker Compose

These components work together to **build, run, store, connect, and manage containers.**

#### 🧠 Easy Memory

> **Docker provides the components needed to build, run, store, connect, and manage containers.**

---

## 6.4 ⚙️ What Does Docker Do?


Docker allows us to:

- 📦 Package applications
- 🖼️ Build Docker images
- ▶️ Run applications in containers
- 📤 Share images
- ⏹️ Start and stop containers
- ⚙️ Manage application environments
- 🔗 Connect containers
- 💾 Store persistent data
- 🚀 Deploy applications consistently

### 🔄 Basic Flow

```text
Application
    ↓
Dockerfile
    ↓
Docker Image
    ↓
Docker Container
    ↓
Running Application
```

#### 🧠 Remember

> **Dockerfile → Image → Container → Application**

---

## 6.5 📖 What is a Container?


### 📌 Definition

A **Docker Container** is a **running instance of a Docker Image.**

A container is a **lightweight** and **isolated environment** used to **run an application and its dependencies**.

Containers are created from Docker images and share the host operating system's kernel, which makes them lightweight and faster to start than virtual machines.

### 📦 Example

```text
Docker Host
│
├── Container 1 → Java App
│
├── Container 2 → MySQL
│
└── Container 3 → Nginx
```

Each container has its own isolated:

- Processes
- Filesystem view
- Networking
- Configuration

### 🔄 Container Lifecycle

```text
Created
   ↓
Running
   ↓
Stopped
   ↓
Started
   ↓
Removed
```

### ⚠️ Important

```text
Container Stop
      ↓
Container still exists
```

```text
Container Remove
      ↓
Container is deleted
```

### 💡 Simple Meaning

> **Container = A place where an application runs with everything it needs.**

---

## 6.6 📖 What is a Docker Image?


### 📌 Definition

A **Docker Image** is a **read-only template** used to create **Docker Containers.**

A Docker Image contains:

- Application code
- Dependencies
- Libraries
- Required files

### 🔄 Flow

```text
Docker Image
     ↓
Create Container
     ↓
Running Application
```

### 💡 Simple Meaning

> **Image = Blueprint**

> **Container = Running instance of that blueprint**

---

## 6.7 ⚖️ Image vs Container


| Docker Image | Docker Container |
|---|---|
| Template / Blueprint | Running instance |
| Used to create containers | Runs the application |
| Read-only | Has a writable container layer |
| Can be stored in a registry | Runs on Docker Engine |

### 🧠 Easy Memory

```text
IMAGE
  ↓
CONTAINER
  ↓
APPLICATION RUNNING
```

#### ⭐ Golden Rule

> **Image = Blueprint**  
> **Container = Running Instance**

---

## 6.8 📖 What is Dockerfile?


### 📌 Definition

A **Dockerfile** is a **text file** that contains set of instructions used to **build a Docker Image automatically.**

### 🧪 Example

```dockerfile
FROM eclipse-temurin:17

WORKDIR /app

COPY app.jar app.jar

CMD ["java", "-jar", "app.jar"]
```

### 🔄 Flow

```text
Dockerfile
    ↓
docker build
    ↓
Docker Image
    ↓
docker run
    ↓
Container
```

### ⚙️ Common Dockerfile Instructions

| Instruction | Purpose |
|---|---|
| `FROM` | Defines the base image |
| `WORKDIR` | Sets the working directory |
| `COPY` | Copies files into the image |
| `RUN` | Runs a command while building the image |
| `EXPOSE` | Documents a port used by the application |
| `CMD` | Default command when the container starts |
| `ENTRYPOINT` | Defines the main executable for the container |

#### 🧠 Easy Memory

```text
FROM
  ↓
WORKDIR
  ↓
COPY
  ↓
RUN
  ↓
EXPOSE
  ↓
CMD
  ↓
ENTRYPOINT
```

> **Dockerfile = Instructions used to build an Image**

---

## 6.9 🐳 Docker Engine


### 📌 Definition

**Docker Engine is the core part of Docker that allows us to build and run containers.**

It Communicate with Docker clients through an API.

### ⚙️ It Manages

- 🖼️ Images
- 📦 Containers
- 🌐 Networks
- 💾 Volumes

It includes the components needed to:

- Build images
- Run containers
- Manage containers
- Manage networks
- Manage volumes

### 🔄 Basic Flow

```text
Docker CLI
    ↓
Docker Engine
    ↓
Containers
```


---

## 6.10 🧱 Docker Architecture


Docker follows a **client-server architecture**.

The Docker Client / CLI communicates with the Docker Engine through the Docker API.

The Docker Engine performs operations such as building, running, and managing containers.

### 🏗️ Architecture

```text
             User
               ↓
          Docker CLI
               ↓
         Docker Engine
          ┌────┼────┬────┐
          ↓    ↓    ↓    ↓
       Images Containers Networks Volumes
```

#### 🧠 Easy Memory

> **CLI → Engine → Docker Resources**

---

## 6.11 🐳 Docker Client / Docker CLI


### 📌 Definition

The **Docker Client** is a **Command Line Interface (CLI)** that is used to communicate with Docker by sending commands through the **Docker API** to build, run, and manage containers.

### 💻 Common Commands

```bash
docker build
docker run
docker ps
docker stop
docker pull
```

The CLI sends commands to the Docker Engine.

### 🔄 Flow

```text
Docker CLI
     ↓
Docker Engine
     ↓
Docker Resources
```


---

## 6.12 🗄️ Docker Registry


### 📌 Definition

A **Docker Registry** is a **place** where **Docker Images** are **stored** and **distributed.**

We can:

- 📤 Push images to a registry
- 📥 Pull images from a registry

### 🌐 Examples

- Docker Hub
- Amazon ECR
- GitHub Container Registry
- Private Registries

### 🔄 Basic Flow

```text
Docker Image
     ↓
    Push
     ↓
Docker Registry
     ↓
    Pull
     ↓
Another Server
```

#### 🧠 Easy Memory

> **Registry = Storage and distribution place for Docker Images**

---

## 6.13 🐳 Docker Hub


### 📌 Definition

**Docker Hub is a cloud-based container registry service.**

We can use Docker Hub to:

- 🔎 Find public images
- 📥 Download images
- 📦 Store images
- 📤 Share images

### 💻 Example

```bash
docker pull nginx
```

This downloads the Nginx image from a configured registry, commonly Docker Hub.

#### 🧠 Easy Memory

> **Docker Hub = Public place to find, store, and share Docker Images**

---

## 6.14 💾 Docker Volume


### 📌 Definition

A **Docker Volume is used to store data outside the container, so the data can remain even when the container is deleted.**

### ❓ Why Do We Need Volumes?

Containers are often temporary.

If a container is removed, data stored only inside the container may be lost.

### 🔄 Example

```text
Container
    ↓
Application
    ↓
Volume
    ↓
Persistent Data
```

Volumes are commonly used for:

- Databases
- Applications requiring persistent data

---

### 💾 Types of Docker Storage

Docker mainly provides:

1. **Docker Volume**
2. **Bind Mount**
3. **tmpfs Mount**

---

### 💾 1️⃣ Docker Volume

Managed by Docker.

#### 💾 Create a volume

```bash
docker volume create myvolume
```

#### 💾 Use the volume

```bash
docker run -v myvolume:/data nginx
```

#### 🧠 Remember

> **Volume → Managed by Docker**

---

### 🔹 2️⃣ Bind Mount

A bind mount maps a specific directory from the host machine into the container.

```bash
docker run -v /home/user/data:/data nginx
```

```text
Host Directory
(/home/user/data)
       ↓
    Container
       ↓
      /data
```

#### 🧠 Remember

> **Bind Mount → Host Directory**

---

### 🔹 3️⃣ tmpfs Mount

A tmpfs mount stores data temporarily in the host's memory.

Data is removed when the container stops.

```text
tmpfs
  ↓
Host Memory
  ↓
Container
```

#### 🧠 Remember

> **tmpfs → Temporary memory storage**

---

### 📊 Simple Difference

| Storage Type | Meaning |
|---|---|
| **Volume** | Managed by Docker |
| **Bind Mount** | Host directory |
| **tmpfs** | Temporary memory storage |

---

## 6.15 🌐 Docker Network


### 📌 Definition

**Docker Networking allows containers to communicate with each other and with external systems.**

Docker provides different network drivers such as:

- Bridge
- Host
- None

### 🔗 Example

```text
Frontend Container
        ↓
   Docker Network
        ↓
Backend Container
        ↓
Database Container
```

Containers can communicate using Docker networks.

---

### 🌐 Network Types

#### 🔹 1️⃣ Bridge

Default network for containers on a single Docker Host.

#### 🔹 2️⃣ Host

Containers share the host's network stack.

#### 🔹 3️⃣ None

Container has no network connectivity.

---

### 💻 Important Network Commands

#### 🌐 List Networks

```bash
docker network ls
```

#### 🌐 Create Network

```bash
docker network create mynetwork
```

#### 📦 Connect Container

```bash
docker network connect mynetwork myapp
```

#### 📦 Disconnect Container

```bash
docker network disconnect mynetwork myapp
```

---

### 🌐 Custom Bridge Network

Custom bridge networks allow containers to communicate with each other using container/service names.

```text
Backend Container
       ↓
   mynetwork
       ↓
Database Container
```

Backend can connect to the database using:

```text
DB_HOST=mysql
```

instead of using the container IP.

#### 🧠 Easy Memory

> **Network → Allows containers to communicate.**

---

## 6.16 🧩 Docker Compose


### 📌 Definition

**Docker Compose is a tool used to define and run multi-container applications using a YAML configuration file.**

With a single YAML file, we can configure:

- Services
- Networks
- Volumes
- Environment variables
- Images
- Build
- Ports
- Dependencies
- Restart policies

### 🏗️ Example

```text
             Docker Compose
                  │
          ┌───────┼───────┐
          ↓       ↓       ↓
        Web      App      DB
```

For example:

```text
Frontend
Backend
Database
```

can be managed together.

### 💻 Important Compose Commands

#### 🌐 Start Services

```bash
docker compose up
```

#### 🔹 Start in Background

```bash
docker compose up -d
```

#### 🌐 Stop and Remove Services

```bash
docker compose down
```

#### 🌐 List Services

```bash
docker compose ps
```

#### 📜 View Logs

```bash
docker compose logs
```

#### 🌐 Build Services

```bash
docker compose build
```

### 🔗 Service Communication

Services can communicate using their service names.

Example:

```text
Backend → mysql:3306
```

#### 🧠 Easy Memory

> **Docker Compose = Manage multiple containers together using a YAML file.**

---

## 6.17 🐳 Docker in DevOps


Docker is widely used in DevOps because it makes application packaging and deployment more consistent.

### 🔄 Typical Workflow

```text
Developer
    ↓
GitHub
    ↓
Jenkins
    ↓
Build Application
    ↓
Docker Build
    ↓
Docker Image
    ↓
Container Registry
    ↓
Docker / Kubernetes
    ↓
Application Running
```

#### ⭐ Key Point

> **Docker helps DevOps teams package applications consistently and integrate container deployment into CI/CD pipelines.**

---

## 6.18 🐳 Docker + Jenkins


Jenkins can automate Docker operations.

### 🔄 Example

```text
Developer
    ↓
GitHub
    ↓
Jenkins
    ↓
Build Application
    ↓
Docker Build
    ↓
Docker Image
    ↓
Push Image
    ↓
Deploy
```

#### 🧠 Remember

```text
Jenkins → Automates CI/CD

Docker → Packages and runs applications in containers
```

---

## 6.19 🐳 Docker + Kubernetes


Docker and Kubernetes are often used together in container-based environments.

### 🔄 Workflow

```text
Developer
    ↓
Jenkins
    ↓
Docker Image
    ↓
Container Registry
    ↓
Kubernetes
    ↓
Containers
    ↓
Application
```

### 🎯 Roles

```text
Docker
→ Builds / packages container images

Kubernetes
→ Manages containerized applications
```

#### 🧠 Easy Memory

> **Docker → Builds/packages containers**

> **Kubernetes → Manages container workloads**

---

## 6.20 🐳 Docker + AWS


Docker can be used to run containerized applications on AWS.

### ☁️ AWS Container Services

- Amazon ECR
- Amazon ECS
- Amazon EKS

### 🔄 Example

```text
Developer
    ↓
Docker Build
    ↓
Docker Image
    ↓
Amazon ECR
    ↓
ECS / EKS
    ↓
Application
```

#### 🧠 Easy Memory

```text
ECR
→ Stores Images

ECS / EKS
→ Run and manage containers
```

---

## 6.21 🔁 Docker Image Lifecycle


A common Docker Image workflow is:

```text
Dockerfile
    ↓
docker build
    ↓
Docker Image
    ↓
docker tag
    ↓
docker push
    ↓
Container Registry
    ↓
docker pull
    ↓
docker run
    ↓
Container
```

### 🧠 Easy Memory

> **Build → Tag → Push → Pull → Run**

---

## 6.22 💻 Important Docker Commands


### 🔍 Check Docker Version

```bash
docker --version
```

**Purpose:** Shows the Docker version.

---

### 📥 Download an Image

```bash
docker pull nginx
```

**Purpose:** Downloads an image from a container registry.

---

### 🖼️ List Images

```bash
docker images
```

**Purpose:** Shows locally available Docker images.

---

### 🔨 Build an Image

```bash
docker build -t myapp:1.0 .
```

**Purpose:** Builds an image from a Dockerfile.

---

### 📦 ▶️ Run a Container

```bash
docker run -d --name myapp -p 8080:8080 myapp:1.0
```

**Purpose:** Creates and starts a container.

#### 📥 Important Flags

| Flag | Meaning |
|---|---|
| `-d` | Runs in background |
| `--name` | Gives the container a name |
| `-p` | Maps host port to container port |

---

### 📋 List Running Containers

```bash
docker ps
```

**Purpose:** Shows running containers.

---

### 📋 List All Containers

```bash
docker ps -a
```

**Purpose:** Shows running and stopped containers.

---

### ⏹️ Stop a Container

```bash
docker stop myapp
```

**Purpose:** Stops a running container.

---

### 📦 ▶️ Start a Container

```bash
docker start myapp
```

**Purpose:** Starts an existing stopped container.

---

### 🗑️ Remove a Container

```bash
docker rm myapp
```

**Purpose:** Removes a stopped container.

---

### 🗑️ Remove an Image

```bash
docker rmi myapp:1.0
```

**Purpose:** Removes a Docker image.

---

### 📜 View Container Logs

```bash
docker logs myapp
```

**Purpose:** Shows container logs.

---

### 💻 Execute a Command Inside a Container

```bash
docker exec -it myapp bash
```

**Purpose:** Opens a shell inside the running container when the image provides `bash`.

---

## 6.23 💻 Important Dockerfile Example


```dockerfile
FROM eclipse-temurin:17

WORKDIR /app

COPY app.jar app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]
```

### 🔎 Explanation

#### 🔹 `FROM`

Selects the base image.

#### 🔹 `WORKDIR`

Sets the working directory.

#### 🔹 `COPY`

Copies the application file into the image.

#### 🔹 `EXPOSE`

Documents the application port.

#### 🔹 `CMD`

Starts the application.

---

### 🔄 Complete Flow

```text
Dockerfile
    ↓
docker build
    ↓
Docker Image
    ↓
docker run
    ↓
Container
```

#### 🧠 Easy Memory

```text
FROM → WORKDIR → COPY → EXPOSE → CMD
```

---

## 6.24 🧪 Basic Docker Practical


### 🎯 Goal

Containerize a simple Java application.

Suppose we have:

```text
app.jar
```

---

### 🪜 Step 1 — Create Application

Our Java application produces:

```text
app.jar
```

---

### 📄 Step 2 — Create Dockerfile

```dockerfile
FROM eclipse-temurin:17

WORKDIR /app

COPY app.jar app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]
```

---

### 🖼️ Step 3 — Build Image

```bash
docker build -t myapp:1.0 .
```

#### 🔹 Result

```text
Dockerfile
    ↓
Docker Image
```

---

### 📦 Step 4 — Run Container

```bash
docker run -d --name myapp -p 8080:8080 myapp:1.0
```

#### 🔹 Result

```text
Docker Image
     ↓
Container
     ↓
Java Application Running
```

---

### 📦 Step 5 — Check Container

```bash
docker ps
```

---

### 📜 Step 6 — Check Logs

```bash
docker logs myapp
```

---

### 📦 Step 7 — Stop Container

```bash
docker stop myapp
```

---

### 📦 Step 8 — Remove Container

```bash
docker rm myapp
```

#### 🧠 Practical Flow

```text
Build
  ↓
Run
  ↓
Check
  ↓
Logs
  ↓
Stop
  ↓
Remove
```

---

## 6.25 🌍 Real-World Example


Suppose a company has a Java application.

The developer's machine has:

- Java
- Libraries
- Application code
- Required configuration

The company wants the same application to run consistently in testing and production.

### 📦 Create Docker Image

```text
Java Application
      +
Dependencies
      +
Configuration
      ↓
Docker Image
      ↓
Container
```

The image can then be pushed to a registry:

```text
Docker Image
      ↓
Amazon ECR
      ↓
AWS ECS / EKS
      ↓
Application Running
```

#### 🧠 Real-World Understanding

> **Build once → Store the image → Deploy the same image across environments.**

---

## 6.26 ⭐ Advantages of Docker


### 🔹 1️⃣ Consistency

The application runs in a consistent environment.

### 🔹 2️⃣ Lightweight

Containers generally use fewer resources than full virtual machines.

### 🔹 3️⃣ Fast Startup

Containers can start quickly.

### 🔹 4️⃣ Portability

The same image can be used across different environments that support the required container runtime.

### 🚀 5️⃣ Easy Deployment

Applications can be packaged and deployed easily.

### 🧪 6️⃣ Scalability

Multiple container instances can be created when needed.

### 🔹 7️⃣ CI/CD Support

Docker works well with CI/CD pipelines.

#### ⭐ Easy Memory

```text
Consistency
+
Lightweight
+
Fast Startup
+
Portability
+
Easy Deployment
+
Scalability
+
CI/CD
```

---

## 6.27 ⭐ Disadvantages of Docker


### 🔐 1️⃣ Security

Containers share the host kernel, so proper security configuration is important.

### 🔹 2️⃣ Data Persistence

Container storage is not automatically suitable for persistent data.

Volumes or external storage are often needed.

### 🌐 3️⃣ Networking Complexity

Networking can become more complex when many containers are used.

### 🔹 4️⃣ Management at Scale

Managing many containers manually becomes difficult.

Tools such as Kubernetes can help.

### 🔹 5️⃣ Learning Curve

There are several concepts to learn:

- Images
- Containers
- Networks
- Volumes
- Registries
- Dockerfiles

#### 🧠 Remember

> **Docker is powerful, but security, persistence, networking, and management need proper attention.**

---

## 6.28 ⚖️ Docker vs Virtual Machine


| Feature | Docker Container | Virtual Machine |
|---|---|---|
| Kernel | Shares host kernel | Has its own guest OS |
| Weight | Lightweight | Heavier |
| Startup Time | Usually starts faster | Usually starts slower |
| Resource Usage | Uses fewer resources | Uses more resources |
| Packaging | Packages application and dependencies | Includes a full operating system |
| Isolation | Process/filesystem/network isolation | Full OS-level isolation |
| Best Use | Containerized applications | When full OS isolation is needed |

### 🖥️ Virtual Machines

```text
Host Machine
│
├── VM
│    ├── Guest OS
│    └── App
│
└── VM
     ├── Guest OS
     └── App
```

### 📦 Containers

```text
Host Machine
│
└── Docker Engine
     │
     ├── Container → App
     │
     └── Container → App
```

#### 🧠 Easy Memory

> **VM → Full Guest OS**

> **Container → Shares Host Kernel**

---

## 6.29 ⚖️ Dockerfile vs Image vs Container


### 📄 Dockerfile

Instructions used to build an Image.

### 🖼️ Image

Blueprint / template used to create Containers.

### 📦 Container

Running instance of an Image.

### 🔄 Flow

```text
Dockerfile
     ↓
docker build
     ↓
Image
     ↓
docker run
     ↓
Container
     ↓
Application Running
```

#### 🧠 Easy Memory

> **Dockerfile → Image → Container → Application**

---

## 6.30 ⚖️ Docker vs Kubernetes


### 🐳 Docker

Used to:

- Build images
- Run containers
- Manage containers

### ☸️ Kubernetes

Used to:

- Deploy containers
- Scale applications
- Manage container workloads
- Handle service discovery
- Perform rolling updates

### 📊 Simple Comparison

| | Docker | Kubernetes |
|---|---|---|
| Type | Container Platform | Container Orchestration Platform |
| Main Focus | Build & Run Containers | Manage Container Workloads |
| Scale | Mainly single-host/container operations | Multi-host / large-scale workloads |
| Use Cases | Development, DevOps, small applications | Production, large-scale, microservices |

#### 🧠 Easy Difference

> **Docker → Builds and runs containers**

> **Kubernetes → Manages container workloads**

---


---


---

## 6.31 📌 Quick Revision


### 🐳 Docker

> **Docker = Containerization Platform**

---

### 🔄 Main Flow

```text
Application
    ↓
Dockerfile
    ↓
Docker Image
    ↓
Docker Container
    ↓
Running Application
```

---

### ⚙️ Important Concepts

```text
Docker Engine
→ Runs and manages containers

Image
→ Template / Blueprint

Container
→ Running instance of an Image

Dockerfile
→ Instructions to build an Image

Registry
→ Stores and distributes Images

Docker Hub
→ Public container registry

Volume
→ Persistent data storage

Network
→ Container communication

Compose
→ Runs multiple containers together
```

---

### 💻 Important Commands

```bash
docker pull
docker images
docker build
docker run
docker ps
docker ps -a
docker stop
docker start
docker rm
docker rmi
docker logs
docker exec
```

---

### 🔗 Important Integrations

```text
Jenkins
   ↓
Docker Build
   ↓
Docker Image
   ↓
Registry
   ↓
Kubernetes / AWS
```

---

## 6.32 🐳 Docker in DevOps Ecosystem


### 🌐 Complete Ecosystem

```text
Developer
    ↓
GitHub
    ↓
Jenkins
    ↓
Build & Test
    ↓
Docker Build
    ↓
Docker Image
    ↓
Container Registry
    ↓
Kubernetes / Docker
    ↓
Application
    ↓
Running 🚀
```

### 🧠 Key Point

> **Docker helps DevOps teams package applications consistently and integrate container deployment into CI/CD pipelines.**

---

## 6.33 📌 Docker Quick Revision & Cheat Sheet


### ⭐ Docker in One Line

> **Docker is an open-source platform that packages applications and their dependencies into containers so they can run consistently anywhere.**

---

### 🧩 Core Concepts

```text
Dockerfile
    ↓
Image
    ↓
Container
    ↓
Running Application
```

#### 🔹 Remember

```text
Dockerfile → Instructions

Image → Blueprint / Template (Read-only)

Container → Running instance (Writable layer)
```

---

### ❓ Why Do We Use Docker?

- ✅ Consistent environment
- ✅ Solves "Works on my machine"
- ✅ Faster deployment
- ✅ Lightweight vs VMs
- ✅ Easy packaging and distribution
- ✅ Helps with scaling
- ✅ Works well with CI/CD
- ✅ Cloud & Kubernetes ready

---

### ⚙️ What Does Docker Provide?

- Docker Engine
- Docker Images
- Docker Containers
- Dockerfile
- Docker Registry
- Docker Hub
- Docker Volumes
- Docker Networks
- Docker Compose

---

### 🔄 What Does Docker Do?

- Package applications
- Build images
- Run containers
- Share images
- Start / stop containers
- Manage environments
- Connect containers
- Store persistent data
- Deploy consistently

---

### 🖼️ Image vs Container

| Image | Container |
|---|---|
| Template / Blueprint | Running instance |
| Used to create containers | Runs application |
| Read-only | Writable layer |
| Stored in registry | Runs on Docker Engine |
| Does not run by itself | Runs / can be stopped |

---

### 🏗️ Docker Architecture

```text
Docker CLI
    ↓
Docker Engine
    ↓
┌─────────┬────────────┬──────────┬─────────┐
│ Images  │ Containers │ Networks │ Volumes │
└─────────┴────────────┴──────────┴─────────┘
```

---

### 💾 Docker Storage

#### 💾 1. Volume

```text
Managed by Docker
```

#### 🔹 2. Bind Mount

```text
Host Directory
```

#### 🔹 3. tmpfs

```text
Temporary Memory
```

---

### 🌐 Docker Networks

#### 🔹 Bridge

```text
Default network
```

#### 🔹 Host

```text
Shares host network stack
```

#### 🔹 None

```text
No network connectivity
```

#### 🔹 Custom Bridge

```text
Container
    ↓
Custom Network
    ↓
Container
```

Service/container names can be used for communication.

Example:

```text
DB_HOST=mysql
```

---

### 🧩 Docker Compose

Compose file can define:

- Services
- Images
- Build
- Ports
- Volumes
- Networks
- Environment Variables
- Dependencies
- Restart Policies

#### 💻 Important Commands

```bash
docker compose up
docker compose up -d
docker compose down
docker compose ps
docker compose logs
docker compose build
```

---

### 🔄 Docker Image Lifecycle

```text
1. Dockerfile
       ↓
2. docker build
       ↓
3. Docker Image
       ↓
4. docker tag
       ↓
5. docker push
       ↓
6. Registry
       ↓
7. docker pull
       ↓
8. docker run
       ↓
9. Container
```

#### 🧠 Memory

> **Build → Tag → Push → Pull → Run**

---

### 🔗 Docker Ecosystem

#### ⚙️ 1. With Jenkins

```text
Code
 ↓
Jenkins
 ↓
Build
 ↓
Docker Image
 ↓
Registry
 ↓
Deploy
```

#### ☸️ 2. With Kubernetes

```text
Docker Image
 ↓
Registry
 ↓
Kubernetes
 ↓
Pods / Containers
```

#### ☁️ 3. With AWS

```text
Docker Image
 ↓
Amazon ECR
 ↓
ECS / EKS
 ↓
Application
```

---

### ⚖️ Advantages

```text
1. Consistency
2. Lightweight
3. Fast Startup
4. Portability
5. Easy Deployment
6. Scalability
7. CI/CD Support
```

### ⚠️ Disadvantages

```text
1. Security
2. Data Persistence
3. Networking Complexity
4. Management at Scale
5. Learning Curve
```

---


---

## 6.34 🧠 Super Memory Map


```text
                 🐳 DOCKER
                    │
                    ↓
               Dockerfile
               (Instructions)
                    │
                    ↓
                 BUILD
                    │
                    ↓
               Docker Image
                (Blueprint)
                    │
                    ↓
                  RUN
                    │
                    ↓
              Docker Container
             (Running Instance)
                    │
                    ↓
            Application Running
                    │
          ┌─────────┼─────────┐
          ↓         ↓         ↓
       Volume     Network   Compose
          │         │         │
          └─────────┼─────────┘
                    ↓
              Container Registry
                    │
          ┌─────────┼─────────┐
          ↓         ↓         ↓
       Docker Hub  ECR   Private Registry
                    │
                    ↓
                CI/CD
                    │
                 Jenkins
                    │
                    ↓
              Docker Image
                    │
                    ↓
             Kubernetes / AWS
                    │
                    ↓
              Application 🚀
```

---

## 🏆 Docker Super Memory


```text
Dockerfile
    ↓
Build
    ↓
Image
    ↓
Run
    ↓
Container
    ↓
Registry
    ↓
Compose / CI-CD
    ↓
Kubernetes
    ↓
Cloud
    ↓
Application Running
```

#### ⭐ Final Memory Line

> **Docker packages an application and its dependencies into a container so it can run consistently across different environments.**


---

# ☸️ PART 7 — Kubernetes — Container Orchestration

> **Kubernetes = Run, Scale and Heal Containers Automatically**

---

## 7.1 ☸️ Kubernetes Fundamentals


### 📌 What Is Kubernetes?

Kubernetes (K8s) is an open-source container orchestration platform used to deploy, scale, and manage containerized applications.

It automates tasks such as starting containers, replacing failed application instances, distributing workloads across nodes, and managing application networking.

💡 **Example:**
Suppose an application needs 3 replicas. Kubernetes manages these replicas and works to maintaine required number if one fails.


### ❓ Why Do We Use Kubernetes?

Managing containers manually becomes difficult when an application runs many containers across multiple servers.

Kubernetes helps with:

1. Automated Deployment – Deploys applications.
2. Scaling – Increases or decreases application replicas.
3. Self-Healing – Helps recover from failures.
4. Networking – Enables communication between applications.
5. Load Distribution – Distributes traffic across eligible Pods.
6. Rolling Updates – Updates applications gradually.
7. Rollbacks – Returns a Deployment to a previous revision.
8. Resource Management – Manages CPU and memory allocation.
9. Storage Management – Connects applications to storage.
10. Configuration Management – Manages application settings and secrets.

💡 **Example:**
Suppose an application needs 3 replicas. We specify replicas: 3 in a Deployment. If a Pod fails, Kubernetes works to restore the required number of replicas.


### 🌟 Kubernetes Features and Benefits

#### 🩹 Self-Healing
Restarts failed containers and replaces failed Pods when required.

#### 📈 Scaling
Kubernetes allows us to increase or decrease application replicas manually or automatically using autoscalers.

#### 🌐 Service Discovery
Kubernetes DNS allows applications to discover and communicate with Services using their names.

#### ⚖️ Load Distribution
Services provide stable endpoints and distribute eligible traffic across backend Pods.

#### 🔄 Rolling Updates
Deployments can gradually replace old application replicas with new ones.

#### ↩️ Rollbacks
Deployments allow us to return to a previous revision when an update causes problems.

#### 💾 Storage Management
Kubernetes supports application storage through Volumes, PersistentVolumes (PVs), PersistentVolumeClaims (PVCs), and StorageClasses.

#### 📊 Resource Management
CPU and memory requests and limits help manage workload resources.

#### ⚙️ Configuration Management
ConfigMaps and Secrets allow configuration to be separated from container images.

#### 📝 Declarative Management
Users describe the desired state, and Kubernetes continuously works to reconcile the actual state with it.


### 📚 Important Kubernetes Terminology

**Cluster:**
A group of machines that work together to run and manage applications using Kubernetes.

**Node:**
A machine in a Kubernetes cluster.

**Control Plane:**
The components that manage the cluster and its desired state.

**Worker Node:**
A node that runs application workloads.

**Pod:**
The smallest deployable unit in Kubernetes. It contains one or more containers.

**Container:**
A running instance of an application packaged with its dependencies.

**Manifest:**
A YAML or JSON file that defines Kubernetes resources and their configuration.

**Controller:**
A component that checks the current state and works to match it with the desired state.

**Namespace:**
A logical grouping of Kubernetes resources.

### 🔀 Declarative vs Imperative Management

#### 📜 Declarative

We define what we want in a YAML file. Kubernetes works to make the cluster match it.

💡 **Example:**

```bash
kubectl apply -f deployment.yaml
```

🔧 **Use Case:**
Managing applications using YAML files stored in Git.

#### 🔹 Imperative

We directly tell Kubernetes what action to perform using a command.

💡 **Example:**

```bash
kubectl create deployment nginx --image=nginx:stable
```

🔧 **Use Case:**
Use Case: Quick testing, learning, and creating resources directly.


---

## 7.2 🧱 Kubernetes Architecture


### 📌 Architecture Overview

A Kubernetes cluster has two major parts:

1. Control Plane – Manages the cluster.
2. Worker Nodes – Run applications inside Pods.

Simplified architecture:

```text
Administrator
      |
      v
   kubectl
      |
      v
  API Server
      |
      +------ etcd
      |
      +------ Scheduler
      |
      +------ Controller Manager
      |
      v
  Worker Nodes
      |
      +------ Kubelet
      +------ Container Runtime
      +------ Networking components
      +------ Pods and Containers
```

📌 **Important:**
The API Server is the main communication point for Kubernetes components. Cluster state is stored in etcd through the API Server.

### 🧠 Control Plane

The Control Plane manages the cluster and works to maintain its desired state.

Main components:

1. API Server
2. etcd
3. Scheduler
4. Controller Manager


### 🖥️ Worker Node

A Worker Node is a machine that runs application workloads inside Pods.

Main components:

1. Kubelet – Manages Pods assigned to the node.
2. Container Runtime – Runs containers.
3. Networking Components – Enable Pod communication and networking.
4. kube-proxy – Implements Service networking rules when used by the cluster.

A Worker Node can run multiple Pods depending on available resources and scheduling requirements.


### 🌐 API Server

The API Server is the main entry point for Kubernetes API requests.

Responsibilities:

- Receives requests from kubectl and other clients.
- Authenticates and authorizes requests.
- Validates resource configurations.
- Applies admission controls.
- Processes requests and communicates with etcd to persist cluster state.
- Provides the API used by Kubernetes components.

💡 **Example:**

```bash
kubectl get pods
```
This command sends a request to the API Server, which returns information about Pods.


### 🗄️ etcd

etcd is a distributed key-value store that saves Kubernetes cluster state.

It stores information about Kubernetes resources, such as:

- Pods
- Deployments
- ConfigMaps
- Secrets
- Namespaces
- Other API objects

📌 **Important:**
etcd stores cluster configuration and resource data, not container images or ordinary application files.

Production clusters should protect etcd using access controls, backups, and encryption.


### 📍 Scheduler

The Scheduler selects a suitable Worker Node for a Pod that has not yet been assigned to a node.

It considers:

- Available CPU and memory.
- Node selectors.
- Node selectors.
- Affinity and anti-affinity rules.
- Taints and tolerations.
- Scheduling policies.

After selecting a node, the Scheduler records the assignment. The Kubelet on that node then works to start the Pod.


### 🔄 Controller Manager

The Controller Manager runs controllers that work to match the actual state with the desired state.

Examples:

- Deployment-related controllers.
- ReplicaSet controller.
- Node controller.
- Job controller.

💡 **Example:**
If a ReplicaSet requires three Pods but only two exist, its controller works to create another Pod.


### ⚙️ Kubelet

Kubelet is an agent that runs on each Worker Node.

Its responsibilities include:

- Watching for Pods assigned to its node.
- Working with the container runtime to start and manage containers.
- Reporting Pod and node status.
- Running configured health probes.


### 🔀 kube-proxy

kube-proxy implements networking rules that allow Kubernetes Services to route traffic to eligible backend Pods, when the cluster uses kube-proxy

📌 **Important:**
Some networking implementations provide Service functionality without kube-proxy.


### 📦 Container Runtime

The Container Runtime is responsible for running containers on Worker Nodes.

Examples:

- containerd
- CRI-O

Kubelet communicates with the runtime through the Container Runtime Interface (CRI).

Docker-built container images can generally run in Kubernetes, but Docker Engine is not normally the direct runtime on modern Kubernetes nodes.


### 🔄 How Kubernetes Works: Complete Workflow

1. The administrator creates a YAML manifest describing the desired application state.
2. The administrator submits it using kubectl.
3. The API Server validates and processes the request.
4. The desired resource state is saved in etcd through the API Server.
5. Controllers work to create the required resources.
6. The Scheduler assigns unscheduled Pods to suitable Worker Nodes.
7. Kubelet on each selected node receives the Pod specifications.
8. The container runtime pulls the required images and starts containers.
9. Kubelet reports status and runs configured health checks.
10. Networking components provide connectivity according to the cluster configuration.
11. Controllers continue reconciling the actual state with the desired state.

Easy way to remember:

- API Server → Receives and processes requests.
- etcd → Stores cluster state.
- Scheduler → Selects a node.
- Controller Manager → Maintains the desired state.
- Kubelet → Manages Pods on a node.
- Container Runtime → Runs containers.
- Networking Components → Connect workloads and route traffic.

---

## 7.3 ☸️ Kubernetes Objects and Workloads


### 📦 Pod

A **Pod** is the smallest unit that Kubernetes can deploy.

A Pod contains one or more containers. Containers inside the same Pod:

- Share the same Pod IP address and network space.
- Can talk to each other using `localhost`.
- Can use the same storage volumes when configured.

Pods are usually managed by resources such as **Deployments** or **StatefulSets**, instead of being created one by one.

💡 **Example:** `pod.yaml`

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
  labels:
    app: nginx
spec:
  containers:
    - name: nginx
      image: nginx:stable
      ports:
        - containerPort: 80
```

Commands:

```bash
kubectl apply -f pod.yaml
kubectl get pods
kubectl get pods -o wide
kubectl describe pod nginx-pod
kubectl logs nginx-pod
kubectl delete pod nginx-pod
```

📌 **Important:** `containerPort` describes the port used by the container. It does **not** make the Pod available from outside the cluster by itself.


### 🔄 Pod Lifecycle and Container States

A Pod can have these common phases:

**Pending:** Kubernetes has accepted the Pod, but it is not fully running yet. It may be waiting for a node, an image download, or setup.

**Running:** The Pod has been assigned to a node, and at least one container is running or starting.

**Succeeded:** All containers finished successfully and will not be restarted.

**Failed:** All containers have stopped, and at least one stopped with an error.

**Unknown:** Kubernetes cannot find out the Pod's state. This can happen when it cannot communicate with the node.

Common container states:

- **Waiting:** The container is waiting to start, for example while its image is downloading.
- **Running:** The container is running.
- **Terminated:** The container has stopped. Kubernetes records its exit code and reason.

📌 **Important:** `CrashLoopBackOff` is a waiting reason shown for a container. It is not a Pod phase.

Commands:

```bash
kubectl get pods
kubectl describe pod <pod-name>
kubectl get events
```

### 🔢 ReplicaSet

A **ReplicaSet** tries to keep the required number of matching Pod copies running.

💡 **Example:** If the desired number is `3`, the ReplicaSet works to keep three matching Pods available. If a Pod disappears, it tries to create a replacement.

Example YAML:

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: nginx-rs
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx-rs
  template:
    metadata:
      labels:
        app: nginx-rs
    spec:
      containers:
        - name: nginx
          image: nginx:stable
```

Commands:

```bash
kubectl apply -f replicaset.yaml
kubectl get replicasets
kubectl scale rs nginx-rs --replicas=5
kubectl delete rs nginx-rs
```

📌 **Important:** For most applications, create a **Deployment**. The Deployment manages the ReplicaSet for you.


### 🚀 Deployment

A **Deployment** manages stateless application Pods by managing ReplicaSets. It helps you update and roll back an application safely.

Main features:

- Keeps the desired number of replicas.
- Updates the application configuration declaratively.
- Supports rolling updates and rollbacks.
- Allows scaling up or down.
- Keeps rollout revision history.

Example YAML:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
        - name: nginx
          image: nginx:stable
          ports:
            - containerPort: 80
```

Commands:

```bash
kubectl apply -f deployment.yaml
kubectl get deployments
kubectl get replicasets
kubectl get pods
kubectl scale deployment nginx-deployment --replicas=5
kubectl rollout status deployment/nginx-deployment
kubectl rollout history deployment/nginx-deployment
kubectl rollout undo deployment/nginx-deployment
```

Update the image:

```bash
kubectl set image deployment/nginx-deployment nginx=nginx:1.28
```


### 🗃️ StatefulSet

A **StatefulSet** manages applications that need stable Pod names or stable storage, often both.

Common uses:

- Databases.
- Distributed data systems.
- Applications that need stable network names.
- Applications that need Pods created or stopped in a particular order.

Unlike Deployment replicas, which are usually interchangeable, StatefulSet Pods get stable names such as:

```text
database-0
database-1
database-2
```

A StatefulSet can use `volumeClaimTemplates` to create a separate PersistentVolumeClaim for each Pod.

📌 **Important:** A StatefulSet does not automatically set up database replication, backups, or data consistency. These need to be handled separately.


### 🖥️ DaemonSet

A **DaemonSet** makes sure a Pod runs on each node that is eligible under its scheduling rules.

Common uses:

- Log collection agents.
- Node monitoring agents.
- Networking components.
- Storage agents.

When a new eligible node joins the cluster, the DaemonSet controller works to run the required Pod on it.


### 🧰 Job

A **Job** runs a task and works to make sure it finishes successfully.

Common uses:

- Processing data.
- Database maintenance.
- Batch tasks.
- One-time admin tasks.

💡 **Example:**

```yaml
apiVersion: batch/v1
kind: Job
metadata:
  name: example-job
spec:
  template:
    spec:
      restartPolicy: Never
      containers:
        - name: task
          image: busybox:1.36
          command: ["sh", "-c", "echo Task completed"]
```

Commands:

```bash
kubectl apply -f job.yaml
kubectl get jobs
kubectl logs job/example-job
```


### ⏰ CronJob

A **CronJob** creates Jobs on a schedule.

💡 **Example:**

```yaml
apiVersion: batch/v1
kind: CronJob
metadata:
  name: scheduled-task
spec:
  schedule: "*/5 * * * *"
  jobTemplate:
    spec:
      template:
        spec:
          restartPolicy: Never
          containers:
            - name: task
              image: busybox:1.36
              command: ["sh", "-c", "date; echo Scheduled task"]
```

The schedule `*/5 * * * *` means the task is scheduled every five minutes.

Commands:

```bash
kubectl apply -f cronjob.yaml
kubectl get cronjobs
kubectl get jobs
```

📌 **Important:** A scheduled Job may not start at the exact second shown by the clock. For production tasks, think about missed schedules, retries, overlapping Jobs, and making the task safe to run more than once.


### 📊 Deployment vs StatefulSet vs DaemonSet vs Job vs CronJob

- **Deployment:** For interchangeable replicas, usually for stateless apps.
- **StatefulSet:** For apps that need stable Pod identities and often persistent storage.
- **DaemonSet:** For a Pod on each eligible node.
- **Job:** For a task that should finish.
- **CronJob:** For tasks that should run on a schedule.

### 🚦 Init Containers

**Init containers** run before the main application containers start. The init containers must finish successfully before the application containers can start.

They can be used to:

- Prepare files or folders.
- Check required dependencies.
- Run setup tasks.
- Wait for a required condition before starting the app.

💡 **Example:**

```yaml
spec:
  initContainers:
    - name: initialization
      image: busybox:1.36
      command: ["sh", "-c", "echo Initializing"]
  containers:
    - name: application
      image: nginx:stable
```


### 📦 Sidecar Containers and Multi-Container Pods

A Pod can run more than one container when the containers need to work closely together.

Examples:

- An application container with a log collector.
- An application container with a proxy.
- An application container with a helper agent.

Containers in the same Pod share the Pod's network and can share volumes when configured.

**Sidecar:** A helper container that runs alongside the main application container and adds a supporting feature.

📌 **Important:** Not every Pod with multiple containers uses a sidecar pattern. Put containers in one Pod when they need to share networking, storage, or a lifecycle closely.


### 🗂️ Namespaces

A **Namespace** groups and separates resources inside one cluster. It helps organize resources and apply access rules.

Common built-in Namespaces:

- `default`
- `kube-system`
- `kube-public`
- `kube-node-lease`

Commands:

```bash
kubectl get namespaces
kubectl create namespace development
kubectl get pods -n development
kubectl get all -n development
kubectl delete namespace development
```

📌 **Important:** `kubectl get all` does not show every resource type. Namespaces help with organization and access control, but they are not a complete security boundary on their own.

### 🏷️ Labels and Selectors

**Labels** are key-value pairs added to Kubernetes objects to describe or group them.

💡 **Example:**

```yaml
labels:
  app: frontend
  environment: production
```

**Selectors** find objects by checking their labels.

Commands:

```bash
kubectl get pods --show-labels
kubectl get pods -l app=frontend
kubectl get pods -l environment=production
```

📌 **Important:** A Service uses a selector to find its backend Pods. A Deployment's selector must match the labels in its Pod template.

### 📝 Annotations

**Annotations** store extra information about an object. They are not normally used to select objects.

Examples:

- Details about deployment tools.
- Links to documentation.
- Information used by external systems.
- Configuration used by controllers.

💡 **Example:**

```yaml
metadata:
  annotations:
    description: "Frontend application"
```

**Difference:** Labels help identify and select objects. Annotations store extra descriptive information.

---

## 7.4 🌐 Kubernetes Networking


### 🌐 Cluster Networking

Kubernetes networking allows:

- Pods to communicate with other Pods.
- Pods to access Services.
- External users to reach applications when access is configured.
- Applications to contact allowed external systems.

A **Container Network Interface (CNI) plugin** commonly provides Pod networking.

Examples:

- Cilium
- Calico
- Flannel

Each plugin has different features and configuration options.


### 🔗 Pod Networking

Each Pod gets its own network identity and IP address inside the cluster's Pod network.

Containers in the same Pod share the network namespace and can communicate using `localhost`.

A Pod's IP can change when Kubernetes replaces the Pod. For this reason, applications usually connect through a Service instead of depending on a Pod IP.

Commands:

```bash
kubectl get pods -o wide
kubectl describe pod <pod-name>
```

### 🌐 Service

A **Service** gives clients a stable network address for reaching matching Pods.

**Why do we need it?** Pods can be replaced and get new IP addresses. A Service provides a stable way to reach the application.

💡 **Example:**

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-service
spec:
  type: ClusterIP
  selector:
    app: nginx
  ports:
    - port: 80
      targetPort: 80
```

Explanation:

- `port`: The port clients use to connect to the Service.
- `targetPort`: The port on the backend Pod where traffic is sent.
- `selector`: Finds the Pods that should receive the traffic.

Commands:

```bash
kubectl apply -f service.yaml
kubectl get services
kubectl describe service nginx-service
kubectl get endpointslices
```


### 📋 Service Types

#### 🔒 ClusterIP

Creates an internal cluster IP for the Service.

🔧 **Use Case:** Communication between application parts inside the cluster.

#### 🚪 NodePort

Makes the Service available through a port on eligible nodes.

🔧 **Use Case:** Basic outside access when the network route and firewall rules allow it.

#### ⚖️ LoadBalancer

Requests an external load balancer from a supported cloud provider or infrastructure integration.

🔧 **Use Case:** Giving users an external endpoint to reach an application.

#### 🔗 ExternalName

Maps a Service name to an external DNS name using a CNAME record.

💡 **Example:**

```yaml
apiVersion: v1
kind: Service
metadata:
  name: external-service
spec:
  type: ExternalName
  externalName: example.com
```


### 🔗 EndpointSlices

**EndpointSlices** list the network endpoints connected to a Service. These endpoints often represent the Pods that receive Service traffic.

Commands:

```bash
kubectl get endpointslices
kubectl describe endpointslice <endpointslice-name>
```

If a Service has no usable endpoints, check its selector, Pod labels, readiness, and Namespace.

### 🌍 Kubernetes DNS

Kubernetes DNS lets applications find Services by name instead of using changing Pod IP addresses.

💡 **Example:**

```text
http://nginx-service
```

To refer to a Service in another Namespace, you can use a name like:

```text
http://nginx-service.development.svc.cluster.local
```

The full DNS domain can be different depending on the cluster setup.


### 🌐 Ingress

**Ingress** defines rules for HTTP and HTTPS traffic coming from outside the cluster to Services.

Rules can use:

- Hostnames.
- URL paths.
- Supported TLS settings.

💡 **Example:**

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: app-ingress
spec:
  ingressClassName: nginx
  rules:
    - host: app.example.com
      http:
        paths:
          - path: /
            pathType: Prefix
            backend:
              service:
                name: nginx-service
                port:
                  number: 80
```

📌 **Important:** An Ingress resource does not route traffic by itself. A compatible **Ingress controller** must be installed and configured.

The Ingress API is still supported, but its development is frozen. **Gateway API** is a newer and more flexible choice for many new networking needs.

### 🚦 Gateway API

**Gateway API** provides Kubernetes resources for configuring gateways and traffic routing.

Important resources:

- **GatewayClass:** Describes a type of gateway managed by a controller.
- **Gateway:** Represents a gateway that handles traffic.
- **HTTPRoute:** Defines HTTP routing rules to backend destinations.

Depending on the implementation, Gateway API can support more detailed routing and traffic distribution rules.

📌 **Important:** You need a compatible implementation and the required CRDs to use Gateway API resources.


### 🛡️ NetworkPolicy

A **NetworkPolicy** sets rules for which network traffic can reach selected Pods and which traffic those Pods can send.

It can control:

- Pod-to-Pod communication.
- Incoming traffic to Pods (ingress).
- Outgoing traffic from Pods (egress).

The cluster's network implementation must support NetworkPolicy for the rules to be enforced.

💡 **Example:**

```yaml
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: allow-frontend
spec:
  podSelector:
    matchLabels:
      app: backend
  policyTypes:
    - Ingress
  ingress:
    - from:
        - podSelector:
            matchLabels:
              app: frontend
```

This policy allows matching frontend Pods to send incoming traffic to matching backend Pods in the policy's Namespace, subject to other network rules.

📌 **Important:** The YAML being accepted does not mean the policy is enforced. The network implementation must support it.


---

## 7.5 💾 Kubernetes Storage


### 💾 Volumes

A **Volume** provides storage that containers in a Pod can mount and use. Some volumes are temporary, while others connect to persistent storage.

💡 **Example:**

```yaml
spec:
  containers:
    - name: nginx
      image: nginx:stable
      volumeMounts:
        - name: app-storage
          mountPath: /usr/share/nginx/html
  volumes:
    - name: app-storage
      emptyDir: {}
```

`emptyDir` is created for the Pod and removed when the Pod is removed. If a container restarts but the Pod stays, the `emptyDir` data normally remains.


### 💾 PersistentVolume (PV)

A **PersistentVolume (PV)** represents storage that Kubernetes can make available to workloads.

It can be created manually by an administrator or created automatically through dynamic provisioning. The actual storage may be a cloud disk, network storage, or another supported storage system.


### 💾 PersistentVolumeClaim (PVC)

A **PersistentVolumeClaim (PVC)** is a request for storage. It can ask for:

- A certain amount of storage.
- Specific access modes.
- A particular StorageClass.

💡 **Example:**

```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: app-pvc
spec:
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 1Gi
```

Commands:

```bash
kubectl apply -f pvc.yaml
kubectl get pvc
kubectl describe pvc app-pvc
```


### 🗃️ StorageClass

A **StorageClass** describes how a type of storage should be created dynamically.

It can define:

- The storage provisioner.
- Storage settings.
- Reclaim-related settings.
- Other settings supported by the storage system.

💡 **Example:**

```yaml
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: example-storage
provisioner: example.com/csi-driver
```

📌 **Important:** `example.com/csi-driver` is only a placeholder. A real StorageClass needs a supported provisioner and the required infrastructure.


### 🔐 Access Modes

- **ReadWriteOnce (RWO):** Allows read-write mounting from one node. Depending on the storage system, multiple Pods on that node may use it.
- **ReadOnlyMany (ROX):** Allows read-only mounting from multiple nodes when supported.
- **ReadWriteMany (RWX):** Allows read-write mounting from multiple nodes when supported.
- **ReadWriteOncePod (RWOP):** Allows read-write mounting by one Pod, when the Kubernetes and CSI versions support it.

📌 **Important:** Access modes describe how storage can be mounted. They do not automatically provide application-level file locking or database consistency.

### ♻️ Reclaim Policies

- **Retain:** Keeps the underlying storage after the claim is released. An administrator may need to clean it up.
- **Delete:** The backing storage may be deleted when the volume is released, depending on the provisioner.
- **Recycle:** An old, deprecated policy that should generally not be used.

📌 **Important:** Check the reclaim policy before deleting production PVCs or PVs.

### ⚖️ Dynamic vs Static Provisioning

**Static Provisioning:** An administrator creates the PV before a PVC requests storage.

**Dynamic Provisioning:** A PVC can trigger storage creation through a StorageClass and a supported provisioner.


---

## 7.6 🔧 Configuration and Security


### ⚙️ ConfigMap

A **ConfigMap** stores non-sensitive application settings separately from the container image.

An application can use ConfigMap data through:

- Environment variables.
- Container command arguments.
- Mounted files.

💡 **Example:**

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: app-config
data:
  APP_ENV: production
  LOG_LEVEL: info
```

Commands:

```bash
kubectl apply -f configmap.yaml
kubectl get configmaps
kubectl describe configmap app-config
```

📌 **Important:** Updating a ConfigMap does not automatically change environment variables inside containers that are already running. Mounted files behave differently, and the application may still need to reload the settings.


### 🔐 Secret

A **Secret** is designed to hold sensitive information such as passwords, tokens, or credentials.

💡 **Example:**

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: app-secret
type: Opaque
stringData:
  username: appuser
  password: change-me
```

Commands:

```bash
kubectl apply -f secret.yaml
kubectl get secrets
kubectl describe secret app-secret
```

Security points:

- Base64 encoding is **not encryption**.
- Give access only to identities that need it, using least-privilege RBAC.
- Enable encryption at rest where supported.
- Do not commit production credentials to source control.
- Consider using an external secret manager.
- Limit who can read Secrets.

📌 **Important:** Updating a Secret does not automatically change environment variable values inside already-running containers.


### 👤 ServiceAccount

A **ServiceAccount** gives a process running in a Pod an identity when it needs to use the Kubernetes API.

RBAC can grant permissions to that identity.

Common uses:

- Reading or managing Kubernetes API resources.
- Running controllers and automation.
- Giving a workload its own identity.

📌 **Important:** Give an application only the permissions it needs.


### 🛡️ RBAC

**RBAC** means **Role-Based Access Control**. It controls which identities can perform actions on Kubernetes resources.

- **Role:** Defines permissions within one Namespace.
- **ClusterRole:** Defines permissions at cluster level or permissions that can also be reused in bindings.
- **RoleBinding:** Gives a Role or ClusterRole permissions to subjects within one Namespace.
- **ClusterRoleBinding:** Gives a ClusterRole permissions across the cluster.

Example Role:

```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  namespace: development
  name: pod-reader
rules:
  - apiGroups: [""]
    resources: ["pods"]
    verbs: ["get", "list", "watch"]
```


### 🔒 SecurityContext

A **SecurityContext** sets security options for a Pod or container.

It can configure things such as:

- Running as a non-root user.
- Setting the user ID and group ID.
- Blocking privilege escalation.
- Removing Linux capabilities.
- Controlling filesystem access.

💡 **Example:**

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: secure-example
spec:
  securityContext:
    runAsNonRoot: true
    runAsUser: 10001
  containers:
    - name: app
      image: nginxinc/nginx-unprivileged:stable
      securityContext:
        allowPrivilegeEscalation: false
        capabilities:
          drop:
            - ALL
```

📌 **Important:** The security settings must work with the selected image and application. Check the application's runtime needs before using strict settings in production.


### 📊 Resource Requests and Limits

**Requests:** The CPU and memory a container asks Kubernetes to reserve for scheduling decisions.

**Limits:** The maximum CPU and memory usage configured for a container.

💡 **Example:**

```yaml
resources:
  requests:
    cpu: "100m"
    memory: "128Mi"
  limits:
    cpu: "500m"
    memory: "256Mi"
```

- **CPU:** `100m` means `0.1` of one CPU core.
- **Memory:** `128Mi` means 128 mebibytes.

If a container goes over its memory limit, it may be stopped because of an out-of-memory condition. If it reaches its CPU limit, it may be throttled. If the cluster cannot meet a Pod's resource requests, the Pod may stay Pending.


### ✅ Kubernetes Security Best Practices

1. Use RBAC with the least permissions needed.
2. Avoid running containers as root unless required.
3. Prevent unnecessary privilege escalation.
4. Protect Secrets and enable encryption at rest where supported.
5. Use NetworkPolicies when the network plugin supports them.
6. Use trusted container images.
7. Scan images for security issues.
8. Keep Kubernetes components and images updated.
9. Do not expose the Kubernetes API unnecessarily.
10. Use suitable Pod Security controls and admission policies.
11. Do not store credentials in Git repositories.
12. Review audit logs and security events.

---

## 7.7 ❤️ Health Checks and Probes


### 🩺 Why Are Probes Needed?

A container may be running even when its application is not ready to handle requests.

Kubernetes **probes** check whether an application has started, is healthy, and is ready to receive traffic.

The three main probes are:

1. Startup Probe
2. Liveness Probe
3. Readiness Probe

### 🩺 Startup Probe

A **startup probe** checks whether the application has finished starting. It is useful for apps that need more time to initialize.

When a startup probe is configured, liveness and readiness checks wait until the startup probe succeeds.

### 🩺 Liveness Probe

A **liveness probe** checks whether the container should be restarted. If it keeps failing past the configured threshold, kubelet restarts the container.

🔧 **Use Case:** Finding an application that is stuck or cannot recover by itself.

### 🩺 Readiness Probe

A **readiness probe** checks whether the application can receive traffic.

If it fails, the Pod is marked not ready and is normally removed from the set of endpoints receiving regular Service traffic. A readiness failure alone does not restart the container.

### 🩺 Probe Example

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: probe-demo
spec:
  replicas: 2
  selector:
    matchLabels:
      app: probe-demo
  template:
    metadata:
      labels:
        app: probe-demo
    spec:
      containers:
        - name: nginx
          image: nginx:stable
          ports:
            - containerPort: 80
          startupProbe:
            httpGet:
              path: /
              port: 80
            failureThreshold: 30
            periodSeconds: 5
          readinessProbe:
            httpGet:
              path: /
              port: 80
            periodSeconds: 5
          livenessProbe:
            httpGet:
              path: /
              port: 80
            initialDelaySeconds: 10
            periodSeconds: 10
```

Commands:

```bash
kubectl apply -f probe-demo.yaml
kubectl describe deployment probe-demo
kubectl get pods
```

📌 **Important:** Probe endpoints should check the real health of the app. A badly designed liveness check can cause repeated restarts when the system is busy.


---

## 7.8 📅 Scheduling and Scaling


### 📍 Node Selector

A `nodeSelector` restricts a Pod to nodes that have the requested labels.

💡 **Example:**

```yaml
spec:
  nodeSelector:
    disktype: ssd
```

Add the label to a node:

```bash
kubectl label nodes <node-name> disktype=ssd
```


### 📍 Node Affinity

**Node affinity** gives more control over which nodes can run a Pod. It supports rules that are required and rules that are preferred.

- **Required:** The Pod must match the rule to be scheduled on a node.
- **Preferred:** The Scheduler tries to follow the rule but can choose another suitable node.


### 📍 Taints and Tolerations

A **taint** tells Kubernetes to keep away Pods that do not tolerate it. A **toleration** allows a Pod to tolerate a matching taint, but it does not guarantee the Pod will run on that node.

Example taint:

```bash
kubectl taint nodes <node-name> dedicated=app:NoSchedule
```

Example toleration:

```yaml
tolerations:
  - key: dedicated
    operator: Equal
    value: app
    effect: NoSchedule
```

Common effects:

- **NoSchedule:** New Pods without a matching toleration are not scheduled on the node.
- **PreferNoSchedule:** Kubernetes tries to avoid that node for Pods without a matching toleration.
- **NoExecute:** Pods without a matching toleration may be evicted, and new ones without it are not scheduled there.


### 📍 Pod Affinity and Anti-Affinity

- **Pod affinity:** Tells Kubernetes to place a Pod near other matching Pods, either as a requirement or a preference.
- **Pod anti-affinity:** Tells Kubernetes to place a Pod away from matching Pods, either as a requirement or a preference.

Use cases:

- Keeping related workloads close together.
- Spreading replicas across different nodes.
- Reducing the effect of a node failure.


### 📍 Topology Spread Constraints

Topology spread constraints help distribute Pods across groups of nodes, such as separate nodes or availability zones.

This can improve reliability by avoiding a situation where too many replicas run in one place.

💡 **Example:**

```yaml
topologySpreadConstraints:
  - maxSkew: 1
    topologyKey: kubernetes.io/hostname
    whenUnsatisfiable: ScheduleAnyway
    labelSelector:
      matchLabels:
        app: web
```

This example asks Kubernetes to spread matching Pods more evenly across eligible nodes, based on the cluster's scheduling setup.

### 🔹 PriorityClass

A **PriorityClass** sets a priority value for Pods. The Scheduler uses priority when deciding which Pods should be scheduled first. It can also affect preemption, where a lower-priority Pod may be removed to make room for a higher-priority one.

📌 **Important:** Priority does not add resources to the cluster. Use priorities carefully because they can affect other workloads.

### 📈 Horizontal Pod Autoscaler (HPA)

The **Horizontal Pod Autoscaler (HPA)** changes the number of Pod replicas based on configured metrics.

💡 **Example:**

```bash
kubectl autoscale deployment nginx-deployment --cpu-percent=60 --min=2 --max=10
```

Check the HPA:

```bash
kubectl get hpa
kubectl describe hpa
```

📌 **Important:** CPU-based HPA usually needs resource requests and a working metrics source, such as Metrics Server. HPA changes the number of Pod replicas; it does not directly add Worker Nodes.

### 📈 Vertical Pod Autoscaler (VPA)

The **Vertical Pod Autoscaler (VPA)** can suggest or change the CPU and memory requests for containers, depending on how it is installed and configured.

It focuses on the resources given to each container, while HPA mainly changes the number of replicas.

📌 **Important:** VPA is an extra component and may not be installed in every cluster. Plan carefully before using VPA and HPA together, especially if both use CPU or memory metrics.

### 📈 Cluster Autoscaling

**Cluster Autoscaling** changes the number of cluster nodes when the infrastructure and autoscaling tools support it.

It can add nodes when Pods cannot be scheduled because there is not enough capacity. It may also remove suitable underused nodes when it is safe to do so.


---

## 7.9 🧪 Practical kubectl Commands


### 🔎 Cluster Information

```bash
kubectl version
kubectl cluster-info
kubectl get nodes
kubectl describe node <node-name>
```

### 📦 Pods

```bash
kubectl get pods
kubectl get pods -A
kubectl get pods -o wide
kubectl get pods --show-labels
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl logs <pod-name> --previous
kubectl exec -it <pod-name> -- sh
```

### 🚀 Deployments

```bash
kubectl get deployments
kubectl describe deployment <deployment-name>
kubectl scale deployment <deployment-name> --replicas=3
kubectl rollout status deployment/<deployment-name>
kubectl rollout history deployment/<deployment-name>
kubectl rollout undo deployment/<deployment-name>
```

### 🌐 Services

```bash
kubectl get services
kubectl describe service <service-name>
kubectl get endpointslices
```

### 🔧 Configuration and Security

```bash
kubectl get configmaps
kubectl get secrets
kubectl get serviceaccounts
kubectl get roles
kubectl get rolebindings
```

### 🗂️ Namespaces

```bash
kubectl get namespaces
kubectl get pods -n <namespace>
kubectl get all -n <namespace>
```

### 📄 Events and Logs

```bash
kubectl get events
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl logs <pod-name>
kubectl logs <pod-name> --previous
kubectl describe pod <pod-name>
```

### 🧱 Resource Usage

```bash
kubectl top nodes
kubectl top pods
```

These commands need a working metrics source in the cluster.

### 🚀 Apply and Validate YAML

```bash
kubectl apply -f deployment.yaml
kubectl diff -f deployment.yaml
kubectl apply --dry-run=client -f deployment.yaml
kubectl delete -f deployment.yaml
```

📌 **Important:** A client-side dry run checks the YAML locally. It does not prove that the live cluster can schedule or run the application.

### 🔧 Kubeconfig and Contexts

A **kubeconfig** file stores cluster connection details and user authentication settings.

Commands:

```bash
kubectl config get-contexts
kubectl config current-context
kubectl config use-context <context-name>
kubectl config view
```

A context connects a cluster, a user, and sometimes a default Namespace.

Be careful when changing contexts. Your next command may affect a different cluster.

---

## 7.10 🧪 Complete Practical: Deploy an Application


### 🚀 Create a Deployment and Service

Save the following YAML as `app.yaml`:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: web-app
spec:
  replicas: 2
  selector:
    matchLabels:
      app: web
  template:
    metadata:
      labels:
        app: web
    spec:
      containers:
        - name: nginx
          image: nginx:stable
          ports:
            - containerPort: 80
          resources:
            requests:
              cpu: "100m"
              memory: "64Mi"
            limits:
              cpu: "500m"
              memory: "128Mi"
---
apiVersion: v1
kind: Service
metadata:
  name: web-service
spec:
  type: ClusterIP
  selector:
    app: web
  ports:
    - port: 80
      targetPort: 80
```

### 🚀 Apply the Manifest

```bash
kubectl apply -f app.yaml
```

### 🚀 Check the Deployment

```bash
kubectl get deployments
kubectl rollout status deployment/web-app
```

**Expected:** The Deployment should show two desired replicas. After the Pods start and become ready, it should show two available replicas.

### 📦 Check the Pods

```bash
kubectl get pods -o wide
kubectl get pods --show-labels
```

**Expected:** Two Pods should eventually become Running and Ready if the cluster has enough resources and can download the image.

### 🌐 Check the Service

```bash
kubectl get service web-service
kubectl describe service web-service
kubectl get endpointslices
```

**Expected:** The Service should have endpoints for eligible backend Pods.

### 🧪 Test the Application

Run this command:

```bash
kubectl port-forward service/web-service 8080:80
```

Keep that terminal open. In another terminal on the same computer, open:

```text
http://localhost:8080
```

If the Deployment is healthy and port forwarding works, you should see the NGINX welcome page.

### 🔹 Scale the Application

```bash
kubectl scale deployment web-app --replicas=4
```

Verify:

```bash
kubectl get deployment web-app
kubectl get pods
```

**Expected:** Kubernetes should work toward keeping four replicas running.

### 🖼️ Update the Application Image

```bash
kubectl set image deployment/web-app nginx=nginx:1.28
```

Check:

```bash
kubectl rollout status deployment/web-app
kubectl rollout history deployment/web-app
```

The update will work only if the image is available and the new Pods start successfully.

### 🔹 Roll Back

```bash
kubectl rollout undo deployment/web-app
```

Check:

```bash
kubectl rollout status deployment/web-app
kubectl rollout history deployment/web-app
```

### 🔹 Clean Up

```bash
kubectl delete -f app.yaml
```

This deletes the Deployment and Service created by this manifest.

---

## 7.11 🧯 Troubleshooting


### 📦 Pod Pending

**Meaning:** Kubernetes has not been able to schedule the Pod or finish setting it up.

Possible causes:

- Not enough CPU or memory.
- Node selector or affinity rules do not match available nodes.
- The Pod does not tolerate a node taint.
- A PersistentVolumeClaim is not bound.
- Scheduling rules cannot be satisfied.

Commands:

```bash
kubectl describe pod <pod-name>
kubectl get nodes
kubectl get pvc
kubectl get events --sort-by=.metadata.creationTimestamp
```

Read the Events section to find the reported reason.

### 📥 ImagePullBackOff

**Meaning:** Kubernetes keeps failing to download the container image.

Possible causes:

- The image name is wrong.
- The image tag does not exist.
- Private registry credentials are missing or incorrect.
- There is a network problem.
- The registry is unavailable.

Command:

```bash
kubectl describe pod <pod-name>
```

Check the image name and tag, registry credentials, and Events.

### 🔁 CrashLoopBackOff

**Meaning:** The container starts, stops, and keeps getting restarted.

Possible causes:

- The application fails during startup.
- The command or arguments are wrong.
- Required configuration is missing.
- A dependency is not available.
- Startup or liveness probes fail.
- There is a bug in the application.

Commands:

```bash
kubectl logs <pod-name>
kubectl logs <pod-name> --previous
kubectl describe pod <pod-name>
```

### 🔹 OOMKilled

**Meaning:** The container was stopped because it ran out of memory or went over its memory limit.

Possible causes:

- The app needs more memory.
- The app has a memory leak.
- The memory limit is too low.
- The workload suddenly increased.

Commands:

```bash
kubectl describe pod <pod-name>
kubectl top pods
kubectl get pod <pod-name> -o yaml
```

Check the last termination state, exit code, resource limits, and memory usage.

### 📦 Pod Running but Not Ready

Possible causes:

- The readiness probe is failing.
- The application has not finished starting.
- A required dependency is unavailable.
- The application is overloaded.
- The probe uses the wrong path or port.

Commands:

```bash
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl get endpointslices
```

A Pod can be Running without being Ready to serve traffic.

### 🌐 Service Not Working

Check these points:

1. Is the Service in the correct Namespace?
2. Does its selector match the Pod labels?
3. Are the Pods Ready?
4. Are `port` and `targetPort` correct?
5. Are there usable EndpointSlices?
6. Are NetworkPolicies or other network rules blocking traffic?
7. Is the application listening on the expected interface and port?

Commands:

```bash
kubectl describe service <service-name>
kubectl get pods --show-labels
kubectl get endpointslices
kubectl describe pod <pod-name>
```

### 🖥️ Node NotReady

Possible causes:

- The node has a connectivity problem.
- Kubelet is not working.
- The container runtime has a problem.
- The node has resource pressure.
- The underlying infrastructure has failed.

Commands:

```bash
kubectl get nodes
kubectl describe node <node-name>
kubectl get events
```

You may need access to the node itself and its system logs to investigate further.

### 🚀 Deployment Rollout Stuck

Possible causes:

- The image cannot be downloaded.
- Pods cannot be scheduled.
- Readiness probes keep failing.
- There are not enough resources.
- The application configuration is invalid.

Commands:

```bash
kubectl rollout status deployment/<deployment-name>
kubectl rollout history deployment/<deployment-name>
kubectl describe deployment <deployment-name>
kubectl get pods
kubectl get events
```

### 💾 PersistentVolumeClaim Pending

Possible causes:

- No suitable PV is available.
- The required or default StorageClass is missing.
- The storage provisioner is not working.
- The requested capacity or access mode cannot be provided.

Commands:

```bash
kubectl get pvc
kubectl describe pvc <pvc-name>
kubectl get pv
kubectl get storageclass
```

### 🛠️ Troubleshooting Method

Follow this order when finding a problem:

1. Check the status of the affected resource.
2. Describe the resource for more details.
3. Read recent Events.
4. Check application logs.
5. Check labels, selectors, ports, and endpoints.
6. Check resource requests, limits, and actual usage.
7. Check configuration, Secrets, probes, and storage.
8. Check node health and networking.
9. Fix the actual cause.
10. Check that the application recovered and keep monitoring it.

Do not delete resources immediately without first understanding the problem.

---

## 7.12 ⚖️ Important Comparisons


### 📦 Pod vs Container

- **Container:** Runs an application process with its required dependencies.
- **Pod:** The Kubernetes unit that contains one or more containers.

### 🔢 ReplicaSet vs Deployment

- **ReplicaSet:** Keeps the required number of matching Pod replicas running.
- **Deployment:** Manages ReplicaSets and supports controlled updates and rollbacks.

### 📊 Deployment vs StatefulSet

- **Deployment:** Best for interchangeable replicas of stateless applications.
- **StatefulSet:** Best for applications that need stable Pod identities and often persistent storage.

### 🌐 Service vs Ingress

- **Service:** Gives clients a stable way to reach backend Pods.
- **Ingress:** Defines HTTP/HTTPS rules for outside traffic to reach Services through a compatible controller.

### 🌐 Ingress vs Gateway API

- **Ingress:** An established API for basic HTTP/HTTPS routing.
- **Gateway API:** A newer, more flexible set of resources for broader routing needs, when supported by an implementation.

### ⚙️ ConfigMap vs Secret

- **ConfigMap:** Stores non-sensitive configuration.
- **Secret:** Is designed for sensitive configuration and should be protected with proper access controls and encryption practices.

### ⚖️ Requests vs Limits

- **Requests:** Resource amounts used for scheduling and allocation decisions.
- **Limits:** Configured maximum resource usage for a container.

### 🩺 Liveness vs Readiness vs Startup Probe

- **Startup:** Checks whether the application has finished starting.
- **Liveness:** Checks whether the container should be restarted.
- **Readiness:** Checks whether the application should receive regular traffic.

### 📈 HPA vs Cluster Autoscaling

- **HPA:** Changes the desired number of Pod replicas.
- **Cluster Autoscaling:** Changes the number of Worker Nodes.

### 📍 Node Selector vs Affinity

- **Node Selector:** Matches simple node labels.
- **Node Affinity:** Supports more detailed required and preferred placement rules.

### ⚖️ Taints vs Tolerations

- **Taint:** Keeps away Pods that do not tolerate it.
- **Toleration:** Allows a Pod to tolerate a matching taint, but does not guarantee that it will be scheduled there.

### 🗃️ PV vs PVC vs StorageClass

- **PV:** Represents storage available to Kubernetes.
- **PVC:** Requests storage.
- **StorageClass:** Describes how a type of storage can be provisioned.

---

---

## 7.13 ⚡ Final Revision: How Everything Connects


1. A developer builds a container image.
2. The image is saved in a container registry.
3. A Deployment describes how many application replicas should run.
4. The API Server receives and processes the Deployment request.
5. Controllers create and manage ReplicaSets and Pods.
6. The Scheduler selects suitable Worker Nodes.
7. Kubelet and the container runtime start the containers.
8. Probes help check whether the app has started and is ready.
9. Services provide stable network access to eligible Pods.
10. Ingress or Gateway API can route external HTTP/HTTPS traffic when a compatible implementation is installed.
11. ConfigMaps and Secrets provide application configuration.
12. PVCs and StorageClasses can provide persistent storage.
13. Requests, limits, affinity, taints, and tolerations affect resource use and Pod placement.
14. HPA can change the number of Pod replicas, while Cluster Autoscaling can change node capacity.
15. Controllers keep working to make the actual state match the desired state.
16. Logs, Events, metrics, and resource descriptions help find and fix problems.

---

### 🌳 Final Kubernetes Study Tree

```text
KUBERNETES
├── 1. Kubernetes Fundamentals
├── 2. Kubernetes Architecture
├── 3. Kubernetes Objects and Workloads
├── 4. Kubernetes Networking
├── 5. Kubernetes Storage
├── 6. Configuration and Security
├── 7. Health Checks and Probes
├── 8. Scheduling and Scaling
├── 9. Practical kubectl Commands
├── 10. Complete Practical: Deploy an Application
├── 11. Troubleshooting
├── 12. Important Comparisons
└── 13. Final Revision: How Everything Connects
```


---

# 🏗️ PART 8 — Terraform — Infrastructure as Code

> **Terraform = Create and Manage Infrastructure Using Code**

---

## 8.1 📖 What is Terraform?


### 🔹 Technical Definition

**Terraform** is an open-source **Infrastructure as Code
(IaC)** tool created by **HashiCorp**.

It is used to:

- 🏗️ **Create infrastructure**
- 🔄 **Modify infrastructure**
- 🛠️ **Manage infrastructure**
- 🗑️ **Delete infrastructure**

**using configuration files.**

Terraform is commonly used with cloud platforms such as:

- ☁️ **AWS**
- ☁️ **Azure**
- ☁️ **Google Cloud**

Terraform can manage resources such as:

- **EC2**
- **VPC**
- **Subnet**
- **Security Group**
- **S3**
- **RDS**
- **Load Balancer**

### 💡 Simple Meaning

**Terraform lets us create and manage infrastructure using
code instead of creating everything manually from the cloud
console.**

### 🧪 Example

Instead of manually creating an EC2 instance from the **AWS
Console**, we can write **Terraform** code:

```text
Terraform Code
      ↓
Terraform
      ↓
AWS
      ↓
EC2 Instance
```

---

## 8.2 🤔 Why Do We Use Terraform?


### ❌ Without Terraform


### 🖥️ AWS Console

```text
   ↓
```

Manually create EC2
```text
   ↓
```

Manually create VPC
```text
   ↓
```

Manually create Security Group
```text
   ↓
```

Manually create S3

This can take time and can cause configuration mistakes.

### ✅ With Terraform


**Terraform** Code
```text
      ↓
```

**Terraform**
```text
      ↓
```

AWS Infrastructure

### 🚀 Main Benefits of Terraform


**1. Automation**


**Terraform** reduces manual infrastructure work.

**2. Repeatability**


The same **Terraform** configuration can be used again.

**3. Consistency**


The infrastructure can be created using the same configuration
each time.

**4. Version Control**


**Terraform** code can be stored in **Git**/**GitHub**.

**Terraform** Code
```text
      ↓
```

**Git**
```text
      ↓
```

**GitHub**

We can track changes made to infrastructure code.

**5. Easy Management**


Instead of manually managing many resources, we can manage
them through code.

**6. Multi-Cloud Support**


**Terraform** can work with different platforms using
providers.

---


### ⭐ Advantages of Terraform

**1. Infrastructure as Code**


Infrastructure is defined using code.

**2. Automation**


Reduces manual infrastructure creation.

**3. Repeatable**


The same configuration can be used again.

**4. Version Control**


**Terraform** files can be stored in **Git**.

**5. Multi-Cloud**


**Terraform** supports many providers and platforms.

**6. Plan Before Apply**


We can preview changes before making them.

**7. Reusable**


Modules and variables make configurations reusable.

---

### ⭐ Disadvantages of Terraform

**1. State Management**


**Terraform** state must be managed carefully, especially in
teams.

**2. Learning Curve**


Beginners need to understand **HCL**, providers, resources,
state, and modules.

**3. Manual Changes Can Cause Drift**


Changing infrastructure directly outside **Terraform** can
create differences.

**4. Provider Differences**


Different cloud providers have different resource types and
configurations.

**5. Sensitive Data**


**State** files may contain sensitive information, so they
must be protected.

---

---

## 8.3 📖 What is Infrastructure as Code (IaC)?


**Infrastructure as Code** means managing infrastructure using
code or configuration files instead of manually creating
resources.

### 💡 Simple Meaning


Instead of clicking:

**AWS Console** → EC2 → Create Instance

We write:

**Terraform** Code → terraform apply → EC2 Created

Example:

### 🖱️ Traditional

**AWS Console** → Create EC2 manually

### 💻 IaC

**Terraform** Code → Create EC2 automatically

Simple Meaning

```text
IaC = Infrastructure managed using code.

```

**Terraform** is an IaC tool.

---

## 8.4 ⚙️ What Does Terraform Do?


Terraform is used to **create, manage, modify, and delete
infrastructure** using configuration files.

Terraform provides features such as:

- Configuration files
- Automation
- Resource management
- Dependency management
- State management
- Planning before applying changes
- Reusable configurations
- Modules
- Provider integrations

### 🏗️ What Terraform Can Do

- **Create** infrastructure
- **Modify** existing infrastructure
- **Delete** infrastructure
- **Manage** existing infrastructure
- **Track** infrastructure using Terraform State
- **Show** what changes will happen before applying them

For example, Terraform can manage:

EC2

VPC

Subnet

Security Group

S3

RDS

Load Balancer

So, Terraform helps us **manage infrastructure using code
instead of doing everything manually.**

---

## 8.5 🏗️ How Terraform Works


**Terraform** has a basic workflow:

Write **Terraform** Code
```text
        ↓
terraform init
        ↓
terraform validate
        ↓
terraform plan
        ↓
terraform apply
        ↓
```

Infrastructure

And when we want to remove managed infrastructure:

```text
terraform destroy
        ↓
```

Infrastructure Removed

The core workflow in the reference notes is init → plan →
apply, with destroy for removal.

### 🏗️ 1️⃣ Step 1 — Write Terraform Code


We create **Terraform** configuration files.

Common file:

main.tf

Example:

```text
resource "aws_instance" "web" {
  ami           = "ami-xxxxxxxx"
  instance_type = "t2.micro"
}

```

This tells **Terraform** about an AWS EC2 resource.

### 🏗️ 2️⃣ Step 2 — `terraform init`


Command:

```text
terraform init
```

What does it do?

It initializes the **Terraform** working directory.

It also downloads the required providers and prepares the
project for **Terraform** operations.

### 🧠 Remember


```text
init = Initialize the Terraform project

```

### 🏗️ 3️⃣ Step 3 — `terraform validate`


Command:

```text
terraform validate

```

It checks whether the **Terraform** configuration is valid.

### 🧠 Remember


```text
validate = Check Terraform code

```

### 🏗️ 4️⃣ Step 4 — `terraform plan`


Command:

```text
terraform plan

```

**Terraform** shows what changes it plans to make.

For example:

**+** Create EC2

**+** Create Security Group

**~** Change **Resource**

**-** Destroy **Resource**

Important symbols:

**+**  Create

**~**  Change

**-**  Destroy

### 🧠 Remember


```text
Plan = Preview the changes

```

### 🏗️ 5️⃣ Step 5 — `terraform apply`


Command:

```text
terraform apply

```

This applies the configuration and creates or changes the
infrastructure.

**Terraform** Code
```text
      ↓
terraform apply
      ↓
```

AWS
```text
      ↓
```

EC2 Created
### 🧠 Remember


```text
Apply = Make the changes

```

### 🏗️ 6️⃣ Step 6 — `terraform destroy`


Command:

```text
terraform destroy

```

It removes infrastructure managed by **Terraform**.

### 🧠 Remember


```text
Destroy = Remove managed infrastructure

```

---

## 8.6 📖 What is HCL?


### 🔹 Definition


**HCL** stands for **HashiCorp** Configuration Language.

**Terraform** uses **HCL** to define infrastructure.

### 🧪 Example

```text
resource "aws_instance" "web" {
  instance_type = "t2.micro"
}

```

Here we are writing **Terraform** configuration using **HCL**.

Simple Meaning

```text
HCL = Language used to write Terraform configuration.

```

---

## 8.7 🔧 Terraform Configuration Files


**Terraform** configuration files contain the code that
describes our infrastructure.

**Terraform** files normally use:

.tf

extension.

Example:

main.tf

**Terraform** configuration is generally written using **HCL**
— **HashiCorp** Configuration Language.

A basic project can look like:

```text
terraform-project/
│
├── main.tf
├── variables.tf
├── outputs.tf
└── terraform.tfvars

```

---

"main.tf"

Contains the main infrastructure configuration.

"variables.tf"

Contains variable definitions.

"outputs.tf"

Contains output definitions.

"terraform.tfvars"

Contains variable values.

"terraform.tfstate"

Contains **Terraform** state information.

".terraform/"

Directory created by **Terraform** during initialization and
used for **Terraform**-related working data.

---

---

## 8.8 🧰 Terraform Provider


### 🔹 Definition


A **Provider** is a plugin that allows **Terraform** to
communicate with a external platform.

### 💡 Simple Meaning


```text
Provider = Connection between Terraform and the platform.

```

### 📚 Examples


- AWS **Provider**
- Azure **Provider**
- Google Cloud **Provider**
- **Kubernetes** **Provider**
- **GitHub** **Provider**

Example:

**Terraform**
```text
    ↓
```

AWS **Provider**
```text
    ↓
```

AWS API
```text
    ↓
```

AWS Resources

Simple Meaning

**Provider** connects **Terraform** to the platform we want to
manage.

### ❓ Why do we need a Provider?


**Terraform** itself doesn't know how to create an AWS EC2 or
Azure VM directly.

The provider gives **Terraform** the required connection and
resource definitions for that platform.

---

## 8.9 🧱 Terraform Resource


A **Resource** represents an infrastructure component that
**Terraform** creates or manages.

Such as:

- EC2 instance
- S3 bucket
- VPC
- Security Group
- RDS database

Example:

```text
resource "aws_instance" "web" {
  instance_type = "t2.micro"
}

```

Here:

- "aws_instance" → **Resource** type
- "web" → **Resource** name

### 💡 Simple Meaning


```text
Resource = Infrastructure we want Terraform to create/manage.

```

---

## 8.10 🔤 Terraform Variable


A variable is used to store a value that we can change later.

A **Variable** allows us to pass values into **Terraform**
configurations instead of hardcoding them.

Example:

```text
variable "instance_type" {
  default = "t2.micro"
}

```

Then:

```text
instance_type = var.instance_type

```

### ❓ Why use variables?


They make **Terraform** code:

- Reusable
- Flexible
- Easier to maintain

### 🛠️ How to Use a Variable?


We use:

var.variable_name

Example:

var.instance_type

Complete example:

variables.tf

```text
variable "instance_type" {
  type    = string
  default = "t2.micro"
}

```

main.tf

```text
resource "aws_instance" "web" {
  ami           = "ami-xxxxxxxx"
  instance_type = var.instance_type
}

```

**Terraform** gets the value from the variable.

```text
terraform.tfvars

terraform.tfvars is used to provide values to variables.

```

Example:

variables.tf

```text
variable "instance_type" {
  type = string
}
```

terraform.tfvars

```text
instance_type = "t2.micro"
```

main.tf
```text
resource "aws_instance" "web" {
  instance_type = var.instance_type
}

```

---

## 8.11 📤 Terraform Output


An **Output** displays useful information after **Terraform**
creates infrastructure.

Example:

```text
output "instance_ip" {
  value = aws_instance.web.public_ip
}

```

After applying **Terraform**, it can show the EC2 public IP.

Simple Meaning

```text
Output = Information Terraform gives us after execution.

```

---

## 8.12 📒 Terraform State


**Terraform State** is a file used by Terraform to store
information about the infrastructure resources it manages.

**Terraform** use this file to keep track of the
infrastructure it manages.

It helps to compare the current infrastructure with the
**Terraform configuration**.

The default state file is:

```text
terraform.tfstate

```

It helps **Terraform** understand:

- What resources it manages
- Current resource information
- What has changed
- What needs to be created, updated, or destroyed

### 🧪 Simple Example


**Terraform** Code
```text
      ↓
```

**State** File
```text
      ↓
```

Real Infrastructure

**Terraform** compares the configuration and state to
determine required changes.

### 📌 Terraform State Commands


List resources

```text
terraform state list

```

Shows resources tracked in state.

Show resource

```text
terraform state show aws_instance.web

```

Shows information about a specific resource in state.

Move resource

```text
terraform state mv

```

Moves a resource from one state address to another.

Remove resource from state

```text
terraform state rm

```

Removes a resource from **Terraform** state without
necessarily destroying the real infrastructure.

---

## 8.13 🌐 Terraform Remote State


**Remote State** means storing the Terraform state file in a
remote location instead of keeping it only on the local
machine.

For example, Terraform state can be stored in an **S3
bucket**.

### 🤔 Why Do We Use Remote State?

- Team members can access the same state
- State can be stored centrally
- It is useful for team workflows
- It helps avoid keeping the only state copy on one developer machine

### 💡 Simple Flow

```text
Terraform
    ↓
Remote Backend
    ↓
S3
    ↓
terraform.tfstate
```

**Simple Definition:** Remote State stores Terraform state in
a shared remote location.

---

## 8.14 🗄️ Terraform Backend


A **Backend** determines where **Terraform** stores its state
data.

By default, **Terraform** uses local state.

**Terraform** state can be stored remotely in an S3 bucket.

Remote state is useful when multiple team members work on the
same infrastructure.

Example:

Developer 1
```text
     \
      → Terraform → Remote State
     /
```

Developer 2

**Terraform** **Backend** = Place where **Terraform** stores
the terraform.tfstate file.

---

## 8.15 📒 State Locking


**State Locking** prevents multiple Terraform operations from
modifying the same state at the same time.

### 🤔 Why Do We Use State Locking?

Imagine two team members run `terraform apply` at the same
time.

Both operations may try to change the same state.

State locking helps prevent conflicting changes.

### 💻 Simple Example

```text
Developer A
     ↓
terraform apply
     ↓
State Locked

Developer B
     ↓
terraform apply
     ↓
Waits until the state is available
```

**Simple Definition:** State locking prevents conflicting
Terraform operations on the same state.

---

## 8.16 💻 Terraform State Commands


Terraform provides commands to inspect and manage the
resources tracked in state.

### 💻 Common Commands

```bash
terraform state list
terraform state show <resource>
terraform state mv <source> <destination>
terraform state rm <resource>
```

### 📒 terraform state list

Lists resources currently tracked in Terraform state.

### 📒 terraform state show

Shows information about a resource stored in state.

### 📒 terraform state mv

Moves a resource from one Terraform state address to another.

### 📒 terraform state rm

Removes a resource from Terraform state without directly
destroying the real infrastructure.

---

## 8.17 🔌 Terraform Data Source


A **Data Source** allows **Terraform** to read information
about existing infrastructure or external data without
creating that resource through the data block.

### 💡 Simple Definition


**Data Source** = Reads existing information of resource.

### 🔄 Resource vs Data Source

### 📦 Resource

```text
   ↓
```

Create / Manage **Resource**

### 🔎 Data Source

```text
   ↓
```

Read Existing Information
### 🧪 Example


Suppose an AMI already exists in AWS.

**Terraform** can read information about it using a data
source.

```text
data "aws_ami" "amazon_linux" {
  most_recent = true

  owners = ["amazon"]

  filter {
    name   = "name"
    values = ["al2023-ami-*"]
  }
}

```

Then:

```text
resource "aws_instance" "web" {
  ami           = data.aws_ami.amazon_linux.id
  instance_type = "t2.micro"
}

```

### 🧠 Remember

**Resource**    → Create/Manage
**Data Source** → Read

---

## 8.18 🧱 Terraform Module


A **Module** is a reusable collection of **Terraform**
configuration files.

Instead of writing the same infrastructure code again and
again, we can create a module and reuse it.

A module can receive values through variables.

Example:

**Module**
```text
   ↓
```

VPC Configuration
```text
   ↓
```

Reuse in Multiple Projects

Simple Meaning

```text
Module = Reusable Terraform code.

```

---

## 8.19 🗄️ Terraform Registry


**Terraform** Registry is a place where **Terraform** users
can find, share, and reuse **Terraform modules**,
**providers**, and **configurations**.

### 📚 Examples


AWS modules

**Kubernetes** modules

VPC modules

Networking modules

Instead of writing everything from scratch, we can use
existing modules when needed.

---

## 8.20 🏗️ Terraform Functions


**Terraform** provides built-in functions for manipulating
values.

### 📚 Examples


lookup()

length()

join()

split()

merge()

concat()

contains()

replace()


Example:

```text
locals {
  name = join("-", ["web", "server", "01"])
}

```

Result:

web-server-01

---

## 8.21 🔀 Conditional Expressions


Conditional expressions allow **Terraform** to select a value
based on a condition.

Syntax:

condition ? true_value : false_value

Example:

```text
instance_type = var.environment == "prod" ? "t3.medium" : "t2.micro"

```

Meaning:

If production → t3.medium
Otherwise     → t2.micro

---

## 8.22 🏗️ Terraform count


**count** is a meta-argument used to create multiple instances
of a resource.

Example:

```text
resource "aws_instance" "web" {
  count         = 3
  ami           = "ami-xxxxxxxx"
  instance_type = "t2.micro"
}

```

This creates:

aws_instance.web[0]

aws_instance.web[1]

aws_instance.web[2]

Simple Meaning

```text
count = Same resource ko multiple times create karna.

```

---

## 8.23 🏗️ Terraform for_each


**for_each** is used to create multiple resource instances
using a map or set.

Example:

```text
variable "instances" {
  default = {
    web = "t2.micro"
    app = "t3.micro"
  }
}

```

**Resource**:

```text
resource "aws_instance" "server" {
  for_each = var.instances

  ami           = "ami-xxxxxxxx"
  instance_type = each.value
}

```

Resources can be referenced using keys:

aws_instance.server["web"]
aws_instance.server["app"]

### 🔢 count vs for_each


**count**
```text
  ↓
```

Index-based

**for_each**
```text
  ↓
```

Key-based

**for_each** is useful when resources have meaningful unique
keys.

---

## 8.24 🏗️ Terraform Dependency


**Terraform** understands resource dependencies and creates
resources in the correct order.

Example:

VPC
```text
 ↓
```

Subnet
```text
 ↓
```

EC2

The EC2 instance needs the required network resources first.

**Terraform** can use these dependencies to create resources
in the correct order.

---

## 8.25 📌 depends_on


`depends_on` is used to explicitly tell Terraform that one
resource or module depends on another resource or module.

Normally, Terraform automatically understands dependencies
when one resource uses another resource's attributes.

Use `depends_on` when the dependency is not clear from the
configuration.

### 💻 Example

```hcl
resource "aws_instance" "server" {
  ami           = "ami-xxxxxxxx"
  instance_type = "t2.micro"

  depends_on = [aws_iam_role.example]
}
```

Here, Terraform creates the IAM role before creating the EC2
instance.

**Simple Definition:** `depends_on` explicitly defines a
resource dependency.

---

## 8.26 🏗️ Terraform Idempotency


**Terraform** is designed to make infrastructure match the
desired configuration.

If the infrastructure already matches the configuration,
running **Terraform** again should normally result in no
unnecessary changes.

Example:

**Terraform** Apply
```text
      ↓
```

Infrastructure Created

Run Again
```text
      ↓
```

No Changes Needed

Simple Meaning

Same configuration → No unnecessary changes.

---

## 8.27 🏗️ Terraform Drift


**Drift** happens when the real infrastructure is changed
outside **Terraform** and no longer matches the **Terraform**
configuration/state.

Example:

**Terraform**
```text
   ↓
```

Creates EC2
```text
   ↓
```

Someone manually changes it in AWS
```text
   ↓
```

Infrastructure ≠ **Terraform** Configuration

**Terraform** can detect differences during planning.

---

## 8.28 🏗️ Terraform Locals


**Locals** are named values used to simplify and reuse
expressions inside a Terraform module.

### 💻 Example

```hcl
locals {
  environment = "dev"
}
```

We can use the local value with:

```hcl
local.environment
```

### 🤔 Why Do We Use Locals?

- To avoid repeating the same expression
- To make configuration easier to read
- To reuse calculated or fixed values

**Simple Definition:** Locals are reusable named values inside
Terraform configuration.

---

## 8.29 🔁 Terraform Lifecycle Rules


**Lifecycle rules** control how Terraform creates, updates,
replaces, or destroys resources.

### 🔁 Common Lifecycle Rules

#### 💥 create_before_destroy

Creates the new resource before destroying the old resource.

```hcl
lifecycle {
  create_before_destroy = true
}
```

#### 💥 prevent_destroy

Prevents Terraform from destroying a resource.

```hcl
lifecycle {
  prevent_destroy = true
}
```

#### 🔹 ignore_changes

Tells Terraform to ignore changes to selected resource
attributes.

```hcl
lifecycle {
  ignore_changes = [tags]
}
```

**Simple Definition:** Lifecycle rules control how Terraform
handles resource changes and deletion.

---

## 8.30 🏗️ Terraform Dynamic Block


A **dynamic block** is used to generate repeated nested
configuration blocks dynamically.

It is useful when the number of nested blocks depends on a
variable, list, or map.

### 🧠 Simple Definition

**A dynamic block creates repeated nested blocks from dynamic
values.**

---

## 8.31 🏗️ Terraform Workspace


A **Terraform Workspace** provides a separate state instance
for the same Terraform configuration.

For example, we can have separate workspaces such as:

```text
dev
test
prod
```

Each workspace has its own state.

### 🧠 Simple Definition

**A workspace allows the same Terraform configuration to use
separate state instances.**

---

## 8.32 🏗️ Terraform Import


**Terraform Import** is used to bring an existing
infrastructure resource under Terraform management.

For example, if an EC2 instance was created manually in AWS,
we can associate it with a Terraform resource address using
import.

### 💻 Example

```bash
terraform import aws_instance.server i-1234567890abcdef0
```

Import updates Terraform state so Terraform knows about the
existing resource.

**Important:** Import does not automatically write the
complete Terraform configuration for the resource.

We still need the appropriate Terraform configuration.

### 🧠 Simple Definition

**Terraform import associates an existing resource with
Terraform state so Terraform can manage it.**

---

## 8.33 🏗️ Terraform Provisioner


A **Provisioner** runs a command or action on a local or
remote machine during resource provisioning.

### 🔹 Types of Provisioners

- **local-exec** → runs a command on the local machine
- **remote-exec** → runs commands on a remote machine
- **file** → copies files to a remote machine

### 💻 Example

```hcl
provisioner "local-exec" {
  command = "echo EC2 created"
}
```

### 📥 Important

Provisioners should generally be used only when a better
purpose-built solution is not available.

**Simple Definition:** A provisioner runs a command or action
during resource provisioning.

---

## 8.34 🏗️ Terraform with AWS


**Terraform** can manage many AWS services.

### 📚 Examples


EC2

VPC

Subnet

Route Table

Internet Gateway

NAT Gateway

Security Group

S3

IAM

RDS

EFS

Load Balancer

Auto Scaling

Route 53

CloudWatch

Example:

**Terraform**
```text
    ↓
```

AWS **Provider**
```text
    ↓
```

AWS
```text
 ┌──┼────┬──────┐
 ↓  ↓    ↓      ↓
```

EC2 VPC   S3    RDS

---

## 8.35 🐙 Terraform with Git/GitHub


**Terraform** files can be stored in **Git**/**GitHub**.

Example:

**Terraform** Code
```text
      ↓
```

**Git**
```text
      ↓
```

**GitHub**
```text
      ↓
```

Version History

This allows teams to:

- Track changes
- Review code
- Collaborate
- Roll back code changes

---

## 8.36 🏗️ Terraform with Jenkins


**Terraform** can be integrated with **Jenkins** to automate
infrastructure deployment.

Example:

Developer
```text
    ↓
```

**GitHub**
```text
    ↓
```

### 🔧 Jenkins

```text
    ↓
```

**Terraform** Init
```text
    ↓
```

**Terraform** Plan
```text
    ↓
```

**Terraform** Apply
```text
    ↓
```

AWS Infrastructure

### ⚠️ Important


**Jenkins** → Automates the pipeline

**Terraform** → Creates/manages infrastructure

---

## 8.37 🐳 Terraform with Docker


**Terraform** can manage some **Docker** resources through a
**Docker** provider.

In DevOps, **Terraform** is more commonly used for
infrastructure provisioning, while **Docker** is used for
containerizing applications.

---

## 8.38 ☸️ Terraform with Kubernetes


**Terraform** can also manage **Kubernetes** resources using
the **Kubernetes** provider.

Example:

**Terraform**
```text
    ↓
```

**Kubernetes** **Provider**
```text
    ↓
```

### ☸️ Kubernetes

```text
    ↓
```

Resources

---

## 8.39 💻 Important Terraform Commands


Initialize

```text
terraform init

```

Purpose: Initializes the **Terraform** working directory and
downloads required providers.

Validate

```text
terraform validate

```

Purpose: Checks whether the **Terraform** configuration is
valid.

Format

```text
terraform fmt

```

Purpose: Formats **Terraform** configuration files.

Plan

```text
terraform plan

```

Purpose: Shows planned infrastructure changes.

Apply

```text
terraform apply

```

Purpose: Creates or updates infrastructure.

Destroy

```text
terraform destroy

```

Purpose: Removes infrastructure managed by **Terraform**.

Show **State**

```text
terraform show

```

Purpose: Displays information about the current **Terraform**
state.

---

## 8.40 🧪 Basic Terraform Practical — Create EC2


### 🎯 Goal


Create an EC2 instance using **Terraform**.

### ⚙️ 1️⃣ Step 1 — Install Terraform


Install **Terraform** on your Linux machine.

### 🪜 2️⃣ Step 2 — Create a Directory


```text
mkdir terraform-ec2
cd terraform-ec2

```

### 🪜 3️⃣ Step 3 — Create `main.tf`


Example:

```text
provider "aws" {
  region = "ap-south-1"
}

resource "aws_instance" "web" {
  ami           = "YOUR_AMI_ID"
  instance_type = "t2.micro"
}

```

Replace the AMI ID with a valid AMI for the selected AWS
region.

### 🪜 4️⃣ Step 4 — Initialize


```text
terraform init

```

### 🪜 5️⃣ Step 5 — Validate


```text
terraform validate

```

### 🪜 6️⃣ Step 6 — Plan


```text
terraform plan

```

Check what **Terraform** plans to create.

### 🪜 7️⃣ Step 7 — Apply


```text
terraform apply

```

Confirm when **Terraform** asks.

### ✅ Result


**Terraform** creates the EC2 instance in AWS.

### 🪜 8️⃣ Step 8 — Destroy


When the practical is finished:

```text
terraform destroy

```

This removes the EC2 resource managed by **Terraform**.

---

## 8.41 🌍 Real-World DevOps Example


Suppose a company needs the same infrastructure for:

- Development
- Testing
- Production

Creating everything manually can take a lot of time.

**Terraform** can define the infrastructure as code.

**Terraform** Code
```text
      ↓
        ┌──────────────┐
        ↓              ↓
      Dev             Test
        ↓              ↓
   AWS Resources   AWS Resources
        │              │
        └──────┬───────┘
               ↓
          Production

```

The same **Terraform** approach can be reused with different
configurations.

---

## 8.42 ⚖️ Terraform vs AWS Console


| **AWS Console** | **Terraform** |
|---|---|
| **Manual** | Code-based |
| **Harder to repeat** | Easy to repeat |
| **More manual work** | Automated |
| **Difficult to track changes** | Can use Git |
| **Good for quick/manual tasks** | Good for repeatable infrastructure |

### 🧠 Remember


**AWS Console** → Manual Infrastructure

**Terraform** → **Infrastructure as Code**

---

## 8.43 ⚖️ Terraform vs Ansible


### 🟣 Terraform


- **Mainly used to provision and manage infrastructure.**

Example:

Create EC2
Create VPC
Create RDS

### ⚙️ Ansible


- **Mainly used to configure and manage systems after they exist.**

Example:

Install Apache
Configure application
Copy files
Start service

### ⚡ Easy Difference


**Terraform** → Create Infrastructure
**Ansible**   → Configure Infrastructure

---

## 8.44 ⚖️ Terraform vs Jenkins


### 🟣 Terraform


- **Creates and manages infrastructure.**

### 🔧 Jenkins


- **Automates CI/CD pipelines.**

They can work together:

**GitHub**
```text
   ↓
```

### 🔧 Jenkins

```text
   ↓
```

**Terraform**
```text
   ↓
```

AWS Infrastructure

### ⚡ Easy Difference


**Jenkins** → Automation of workflow

**Terraform** → Automation of infrastructure

---

## 8.45 ⚖️ Terraform vs CloudFormation


Both can be used for **Infrastructure as Code**.

### 🟣 Terraform


**HashiCorp** tool

- **Multi-cloud support**

- **Uses providers**

Uses **HCL**

### 🟠 AWS CloudFormation


- **AWS-native IaC service**

- **Mainly focused on AWS**

- **Uses AWS-supported template formats**

### 🔍 Simple Difference


**Terraform**       → Multi-provider IaC
**CloudFormation**  → AWS-native IaC

---


---


---

## 8.46 📌 Quick Revision


**Terraform**

```text
Terraform = Infrastructure as Code tool

```

### 🎯 Main Purpose


**Terraform** Code
```text
      ↓
```

**Terraform**
```text
      ↓
```

Cloud Infrastructure

### 🔄 Basic Workflow


Write Code
```text
   ↓
terraform init
   ↓
terraform validate
   ↓
terraform plan
   ↓
terraform apply

```

### 🔑 Important Concepts


- **HCL** → Language used to write **Terraform** configuration
- **Provider** → Connects **Terraform** to a platform
- **Resource** → Infrastructure component
- **Variable** → Input value
- **Output** → Displays useful information
- **State** → Tracks managed infrastructure
- **Module** → Reusable **Terraform** code
- **Backend** → Stores **Terraform** state

### 📁 Important Files


main.tf
variables.tf
outputs.tf
```text
terraform.tfvars
terraform.tfstate

```

### 🔗 Terraform + DevOps


Developer
```text
    ↓
```

**GitHub**
```text
    ↓
```

### 🔧 Jenkins

```text
    ↓
```

**Terraform**
```text
    ↓
```

AWS
```text
    ↓
```

Infrastructure

### ⭐ Final Memory Line


**Terraform** allows us to create and manage infrastructure as
code instead of creating everything manually.

---

## ⚡ Terraform Core Workflow


```text
Write Terraform Code
        ↓
terraform init
        ↓
terraform validate
        ↓
terraform plan
        ↓
terraform apply
        ↓
Infrastructure
```

> **🧠 Easy Memory:** `init → validate → plan → apply`

---

## 📌 Final Revision


| **Concept** | **Easy Meaning** |
|---|---|
| **Terraform** | Infrastructure as Code tool |
| **HCL** | Language used to write Terraform configuration |
| **Provider** | Connects Terraform to a platform |
| **Resource** | Infrastructure component Terraform manages |
| **Variable** | Input value |
| **Output** | Displays useful information |
| **State** | Tracks managed infrastructure |
| **Module** | Reusable Terraform code |
| **Backend** | Stores Terraform state |
| **Data Source** | Reads existing information |

### ⭐ Final Memory Line

> **Terraform allows us to create and manage infrastructure as code instead of creating everything manually.**


---

# 🅰️ PART 9 — Ansible — Configuration Management

> **Ansible = Configure Many Servers From One Place Using YAML**

---

## 9.1 🅰️ What is Ansible?


> **Ansible = Configuration Management and Automation Tool**

Ansible is an open-source tool used to **configure servers, install software and deploy applications** using simple **YAML files called playbooks**.

It is **agentless**: nothing needs to be installed on the servers. Ansible only uses **SSH** (and Python on the server).

### 🔹 We can use Ansible to:

- 📦 Install software on many servers.
- ⚙️ Configure servers in the same way.
- 🚀 Deploy applications.
- 🔁 Run tasks in a fixed order (orchestration).
- 🔐 Encrypt secrets using Vault.

### ⚙️ It Provides components such as:

- 🖥️ Control Node
- 📋 Inventory
- 📜 Playbooks
- 🧩 Modules
- 🧱 Roles

to manage many servers from one place.

#### 🏗 Ansible Basic Flow

```text
🖥️ Control Node (Ansible)
        │  SSH
 ┌──────┼──────┐
 ▼      ▼      ▼
🖥️ S1  🖥️ S2  🖥️ S3   ← Managed Nodes (No Agent)
```

#### 🧠 Easy Memory

> **Ansible = One Remote Control for Many Servers**

#### ⚠ Important

> **Ansible is idempotent.** Running the same playbook again does not break anything.

> **Use spaces, not tabs, in YAML.**

---

## 9.2 🤔 Why Do We Use Ansible?


Suppose a company has 100 servers and all need the same setup.

### ❌ Without Ansible

```text
🔑 Login to Each Server One by One
            ↓
⌨️ Run the Same Commands 100 Times
            ↓
💥 Mistakes + Different Configuration Everywhere
```

### ✅ With Ansible

```text
📜 Write One Playbook
 ↓
📋 List Servers in Inventory
 ↓
▶️ Run One Command
 ↓
✅ All Servers Configured the Same Way
```

#### ⭐ Main Reasons

- ⏱️ Save time: one command for many servers
- 🔁 Same result every time (idempotent)
- 🪶 Agentless: no software to install on servers
- 📖 Easy to read and learn (YAML)
- 🔐 Secrets can be encrypted with Vault
- 🔗 Works well with Terraform, Jenkins and Docker

---

## 9.3 🧰 What Does Ansible Provide?


Ansible provides:

- ⚙️ Configuration Management
- 🚀 Application Deployment
- 🔁 Orchestration
- 📦 Provisioning (with modules)
- 🧩 Ready-made Modules
- 🧱 Roles and Ansible Galaxy
- 🔐 Ansible Vault

| 🧰 Feature | 💡 Meaning |
| --- | --- |
| ⚙️ Configuration Management | Keep servers in the desired state |
| 🚀 Deployment | Deploy apps to many servers |
| 🔁 Orchestration | Run tasks in a defined order |
| 🧩 Modules | Ready-made tasks (apt, copy, service, user) |
| 🧱 Roles | Reusable packages of tasks |
| 🔐 Vault | Encrypt passwords and keys |

---

## 9.4 🧱 Ansible Architecture


```text
┌────────────────────────┐
│     Control Node       │   ← Ansible installed here
│ Inventory + Playbooks  │
└───────────┬────────────┘
            │ SSH (Linux) / WinRM (Windows)
   ┌────────┼────────┐
   ▼        ▼        ▼
 Node 1   Node 2   Node 3      ← Managed nodes (no agent)
```

| Component | Role |
| --- | --- |
| **Control Node** | Machine where Ansible runs |
| **Managed Node** | Server managed by Ansible |
| **Inventory** | List of managed nodes |
| **Playbook** | YAML file with tasks |
| **Module** | Small program that does one job |

---

## 9.5 ⚙️ Installation and First Test


```bash
sudo apt update
sudo apt install ansible -y
ansible --version
```

Set up SSH access from the control node:

```bash
ssh-keygen
ssh-copy-id user@<managed-node-ip>
```

---

## 9.6 📋 Inventory


Inventory tells Ansible **which servers** to manage.

`inventory.ini`:

```ini
[web]
web1 ansible_host=10.0.1.10
web2 ansible_host=10.0.1.11

[db]
db1 ansible_host=10.0.2.10

[all:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=~/.ssh/id_rsa
```

- 🌐 `[web]`, `[db]` are **groups**
- 🔹 Group variables are in `[group:vars]`
- 🖥️ **Dynamic inventory** can read servers from AWS, Azure etc.

---

## 9.7 💻 Ad-Hoc Commands


One-line tasks without a playbook.

```bash
ansible all -i inventory.ini -m ping
ansible web -i inventory.ini -m apt -a "name=nginx state=present" --become
ansible all -i inventory.ini -a "uptime"
```

| Option | Meaning |
| --- | --- |
| `-i` | Inventory file |
| `-m` | Module name |
| `-a` | Module arguments |
| `--become` | Run as root (sudo) |

---

## 9.8 📜 Playbook


A **playbook** is a YAML file with one or more **plays**. A play maps **hosts** to **tasks**.

```yaml
---
- name: Install and start Nginx
  hosts: web
  become: yes

  tasks:
    - name: Install nginx
      apt:
        name: nginx
        state: present
        update_cache: yes

    - name: Start nginx
      service:
        name: nginx
        state: started
        enabled: yes
```

Run it:

```bash
ansible-playbook -i inventory.ini site.yml
ansible-playbook -i inventory.ini site.yml --check     # dry run
ansible-playbook -i inventory.ini site.yml --syntax-check
```

---

## 9.9 🧩 Common Modules


| Module | Use |
| --- | --- |
| `ping` | Test connection |
| `apt` / `yum` / `package` | Install packages |
| `copy` | Copy a file to a node |
| `template` | Copy a file with variables (Jinja2) |
| `file` | Create / delete files, set permissions |
| `service` / `systemd` | Start / stop / enable services |
| `user` | Manage users |
| `command` / `shell` | Run commands |
| `git` | Clone repositories |
| `docker_container` | Manage containers |

> 🧠 Prefer **modules** over `shell`/`command`. Modules are idempotent.

---

## 9.10 🔁 Idempotency


Idempotent = **running it many times gives the same result**.

```text
state: present  → install only if not installed
state: started  → start only if not running
```

Task result colors: `ok` (no change), `changed` (something changed), `failed`, `skipped`.

---

## 9.11 🔤 Variables, Facts and Conditions


**Variables:**

```yaml
vars:
  app_port: 8080
tasks:
  - debug:
      msg: "App runs on {{ app_port }}"
```

**Facts** = information Ansible gathers about a node (OS, IP, memory): `ansible_facts`, `ansible_distribution`.

**Conditions (`when`):**

```yaml
- name: Install on Ubuntu only
  apt:
    name: nginx
  when: ansible_distribution == "Ubuntu"
```

**Loops:**

```yaml
- name: Install packages
  apt:
    name: "{{ item }}"
    state: present
  loop:
    - git
    - curl
    - unzip
```

---

## 9.12 🔔 Handlers


A **handler** runs only when it is **notified** by a changed task (e.g. restart a service after config change).

```yaml
tasks:
  - name: Update nginx config
    template:
      src: nginx.conf.j2
      dest: /etc/nginx/nginx.conf
    notify: Restart nginx

handlers:
  - name: Restart nginx
    service:
      name: nginx
      state: restarted
```

---

## 9.13 📄 Templates (Jinja2)


Files with variables, ending in `.j2`.

`nginx.conf.j2`:

```text
server {
    listen {{ app_port }};
    server_name {{ ansible_hostname }};
}
```

Used with the `template` module → the final file is created on each node with its own values.

---

## 9.14 🧱 Roles


A **role** is a **reusable, organized package** of tasks, variables, templates and handlers.

```text
roles/
└── nginx/
    ├── tasks/main.yml
    ├── handlers/main.yml
    ├── templates/
    ├── files/
    ├── vars/main.yml
    └── defaults/main.yml
```

Create and use:

```bash
ansible-galaxy init nginx
```

```yaml
- hosts: web
  become: yes
  roles:
    - nginx
```

**Ansible Galaxy** is a public place to download community roles.

---

## 9.15 🔐 Ansible Vault


Vault **encrypts sensitive data** (passwords, keys).

```bash
ansible-vault create secrets.yml
ansible-vault edit secrets.yml
ansible-vault encrypt vars.yml
ansible-playbook site.yml --ask-vault-pass
```

> ⚠️ Never commit plain-text passwords to Git.

---

## 9.16 🔗 Ansible in CI/CD and DevOps


```text
Terraform → creates servers
Ansible   → configures servers and deploys the app
Jenkins   → runs ansible-playbook as a pipeline stage
Nexus     → source of the artifact to deploy
```

```groovy
stage('Deploy with Ansible') {
  steps {
    sh 'ansible-playbook -i inventory.ini deploy.yml'
  }
}
```

---

## 9.17 ⚖️ Ansible vs Terraform


| Point | Ansible | Terraform |
| --- | --- | --- |
| Main job | Configuration management | Infrastructure provisioning |
| Language | YAML | HCL |
| Style | Mostly procedural (tasks in order) | Declarative |
| State file | No | Yes |
| Typical use | Install, configure, deploy | Create servers, networks, cloud resources |

> They work **together**: Terraform creates, Ansible configures.

---

## 9.18 🏗️ Real Example: Deploy a Web App on 3 Servers


### 🎯 Requirement

Deploy the same Java web application on **3 servers** with one command.

### 🏗 Architecture

```text
┌──────────────┐   SSH   ┌──────────┐
│ 🖥️ Control    │────────►│ 🖥️ web1   │
│ Node         │────────►│ 🖥️ web2   │   ← [web] group in inventory
│ (Ansible)    │────────►│ 🖥️ web3   │
└──────────────┘         └──────────┘
        ▲
        └── 🗄️ Nexus (jar file)
```

### 🪜 Steps to Build It

```text
1. Inventory has group [web] with 3 servers
2. Playbook installs Java and creates app user
3. Copies my-app.jar from Nexus to /opt/app
4. Template creates the systemd service file
5. Handler restarts the service after a change
6. ✅ One command updates all 3 servers: ansible-playbook deploy.yml
```

### ✅ Why This Is Better

| ❌ Manual Deployment | ✅ Ansible Deployment |
| --- | --- |
| Login to each server | One command |
| Different steps on each | Same steps on all |
| Slow and risky | Fast and repeatable |
| No record of what was done | Playbook is the record |

---

## 9.19 🧯 Troubleshooting


| Problem | Reason / Fix |
| --- | --- |
| `UNREACHABLE` / SSH error | Check IP, user, SSH key, security group |
| `Permission denied` | Add `become: yes` |
| `python not found` on node | Install Python on managed node |
| YAML error | Check indentation (spaces, not tabs) |
| Task always shows `changed` | Using `shell`/`command` — add `creates`/`changed_when` or use a module |

Debug with `-v`, `-vvv`, and the `debug` module.

---

## 9.20 📌 Ansible Quick Revision


- 🅰️ Ansible = **agentless** automation tool using **SSH + YAML**
- 🖥️ Parts: Control Node, Managed Node, Inventory, Playbook, Module
- 🔁 **Idempotent**: same result every time
- 🧱 **Handlers** run only on change; **Roles** make playbooks reusable
- 🔐 **Vault** encrypts secrets
- 🅰️ `ansible-playbook -i inventory file.yml`
- 🏗️ Terraform = create infrastructure, Ansible = configure it

---

## 9.21 🧠⚡ Ansible One-Line Memory


| Topic | Easy Memory |
| --- | --- |
| 🅰️ **Ansible** | Control many servers with YAML |
| 📋 **Inventory** | List of servers |
| 📜 **Playbook** | Tasks written in YAML |
| 🧩 **Module** | One ready-made task |
| 🔁 **Idempotent** | Run again, no harm |
| 🔔 **Handler** | Runs only after a change |
| 🧱 **Role** | Reusable package of tasks |
| 🔐 **Vault** | Encrypt secrets |

---

## 9.22 🗺️ Ansible Learning Map


```text
Ansible
 ├── Basics        → What, Why, Agentless
 ├── Setup         → Control Node, SSH, Inventory
 ├── Run           → Ad-hoc, Playbook
 ├── Writing       → Modules, Variables, Conditions, Loops
 ├── Advanced      → Handlers, Templates, Roles, Vault
 └── DevOps        → Jenkins + Terraform + Nexus
```

---

## 9.23 ⭐ Ansible Final Memory


```text
How to manage many servers together?   → Ansible
Where to list the servers?             → Inventory
Where to write the tasks?              → Playbook
How to reuse and organize code?        → Roles
How to protect passwords?              → Ansible Vault
```

> **Ansible configures and deploys to many servers at once using simple YAML playbooks, without any agent.**


---

# 🔥 PART 10 — Prometheus — Monitoring and Alerting

> **Prometheus = Collects Metrics and Sends Alerts**

---

## 10.1 🔥 What is Prometheus?


> **Prometheus = Monitoring and Alerting System**

Prometheus **collects metrics** (numbers such as CPU, memory, request count) from servers and applications, **stores them with time**, and **sends alerts** when something goes wrong.

It uses a **pull model**: Prometheus **scrapes** (asks for) data from targets again and again.

### 🔹 We can use Prometheus to:

- 📈 Collect CPU, memory, disk and network metrics.
- 🌐 Monitor web applications and APIs.
- ☸️ Monitor Kubernetes and containers.
- 🔎 Query data using PromQL.
- 🚨 Send alerts through Alertmanager.

### ⚙️ It Provides components such as:

- 🔥 Prometheus Server
- 🔌 Exporters
- 🚨 Alertmanager
- 🔎 PromQL

to monitor systems and raise alerts.

#### 🏗 Prometheus Basic Flow

```text
🎯 Targets (/metrics)
        ▲
        │ scrape (pull)
        │
🔥 Prometheus Server ─────► 🚨 Alertmanager ─────► 📧 Email / 💬 Slack
        │
        ▼
📊 Grafana (Dashboards)
```

#### 🧠 Easy Memory

> **Prometheus = Doctor Who Checks Server Health Again and Again**

#### ⚠ Important

> **Prometheus stores and queries metrics. Grafana only shows them.**

> **Use `rate()` with counters.**

---

## 10.2 🤔 Why Do We Use Prometheus?


Suppose an application runs on many servers and containers.

### ❌ Without Monitoring

```text
👤 Users Report the Problem First
            ↓
🔍 Team Starts Searching in the Dark
            ↓
💥 Long Downtime
```

### ✅ With Prometheus

```text
🔌 Exporters Expose Metrics
 ↓
🔥 Prometheus Collects Them
 ↓
🚨 Alert Fires When Something Is Wrong
 ↓
✅ Team Fixes It Before Users Notice
```

#### ⭐ Main Reasons

- 👀 Know the health of servers and apps in real time
- 🚨 Get alerts before users complain
- ☸️ Very popular for Kubernetes and containers
- 🔎 Powerful query language (PromQL)
- 🧭 Automatic target discovery (Kubernetes, AWS ...)
- 🆓 Open-source and widely used

---

## 10.3 🧰 What Does Prometheus Provide?


Prometheus provides:

- 📈 Time-Series Database
- 🔎 PromQL Query Language
- 🔄 Pull-Based Metric Collection
- 🧭 Service Discovery
- 🚨 Alerting Rules
- 🌐 Basic Web UI

| 🧰 Feature | 💡 Meaning |
| --- | --- |
| 📈 Time-series database | Stores metrics with timestamps |
| 🔎 PromQL | Query language for metrics |
| 🔄 Pull model | Prometheus scrapes targets |
| 🧭 Service discovery | Finds targets in Kubernetes, AWS etc. |
| 🚨 Alert rules | Define when to alert |
| 🌐 Web UI | Basic graphs and queries |

---

## 10.4 🧱 Prometheus Architecture


```text
┌───────────────┐   ┌─────────────────┐
│ Node Exporter │   │ Application     │
│  (/metrics)   │   │ (/metrics)      │
└──────┬────────┘   └───────┬─────────┘
       │ scrape             │ scrape
       ▼                    ▼
   ┌───────────────────────────────┐        ┌───────────────┐
   │      Prometheus Server        │ ─────► │ Alertmanager  │ → Email / Slack
   │ (Retrieval + TSDB + HTTP API) │        └───────────────┘
   └───────────────┬───────────────┘
                   ▼
                Grafana
```

| Component | Role |
| --- | --- |
| **Prometheus Server** | Scrapes, stores and queries metrics |
| **Exporters** | Expose metrics of systems that have no native support |
| **Pushgateway** | For short-lived jobs that cannot be scraped |
| **Alertmanager** | Groups, routes and sends alerts |
| **Grafana** | Visualization |

---

## 10.5 📊 Metric Types


| Type | Meaning | Example |
| --- | --- | --- |
| **Counter** | Only goes up (resets on restart) | `http_requests_total` |
| **Gauge** | Goes up and down | memory usage, temperature |
| **Histogram** | Counts values in buckets | request duration |
| **Summary** | Similar to histogram, calculates quantiles on the client | request latency |

Metric format:

```text
http_requests_total{method="GET", status="200"}  1027
└───── name ──────┘ └──────── labels ─────────┘  └value┘
```

---

## 10.6 ⚙️ Installation and Configuration


Run with Docker:

```bash
docker run -d --name prometheus -p 9090:9090 \
  -v $(pwd)/prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus
```

UI: `http://<server-ip>:9090`

`prometheus.yml`:

```yaml
global:
  scrape_interval: 15s
  evaluation_interval: 15s

rule_files:
  - "alert_rules.yml"

alerting:
  alertmanagers:
    - static_configs:
        - targets: ["alertmanager:9093"]

scrape_configs:
  - job_name: "prometheus"
    static_configs:
      - targets: ["localhost:9090"]

  - job_name: "node"
    static_configs:
      - targets: ["10.0.1.10:9100", "10.0.1.11:9100"]
```

- 🔹 **job** = group of targets
- 🖥️ **instance** = one target (`host:port`)

---

## 10.7 🔌 Exporters


Exporters turn system data into Prometheus metrics at `/metrics`.

| Exporter | Monitors | Port |
| --- | --- | --- |
| **Node Exporter** | Linux server (CPU, memory, disk, network) | 9100 |
| **cAdvisor** | Docker containers | 8080 |
| **Blackbox Exporter** | URL / port / ping checks | 9115 |
| **MySQL / Postgres Exporter** | Databases | varies |
| **kube-state-metrics** | Kubernetes objects | 8080 |

Run Node Exporter:

```bash
docker run -d --name node-exporter -p 9100:9100 prom/node-exporter
```

---

## 10.8 🔎 PromQL Basics


| Query | Meaning |
| --- | --- |
| `up` | 1 if target is up, 0 if down |
| `node_memory_MemAvailable_bytes` | Available memory |
| `http_requests_total{status="500"}` | Filter by label |
| `rate(http_requests_total[5m])` | Requests per second over last 5 minutes |
| `sum(rate(http_requests_total[5m])) by (job)` | Sum grouped by job |
| `avg(node_load1)` | Average load |

CPU usage % example:

```text
100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
```

> 🧠 Use `rate()` with **counters**. Counters alone only show a growing number.

---

## 10.9 🚨 Alerting


**Alert rule** (`alert_rules.yml`):

```yaml
groups:
  - name: basic-alerts
    rules:
      - alert: InstanceDown
        expr: up == 0
        for: 2m
        labels:
          severity: critical
        annotations:
          summary: "{{ $labels.instance }} is down"
```

Flow:

```text
Prometheus evaluates rule → condition true for 2m → Alert FIRING → Alertmanager → Email / Slack / PagerDuty
```

**Alertmanager** does: **grouping** (many alerts → one message), **routing** (send to the right team), **silencing** (mute during maintenance), **inhibition** (suppress less important alerts).

Alert states: `Inactive → Pending → Firing`.

---

## 10.10 ☸️ Prometheus in Kubernetes


- ☸️ Prometheus discovers Pods and Services using **Kubernetes service discovery**
- 🔥 Easiest setup: **kube-prometheus-stack** Helm chart (Prometheus + Alertmanager + Grafana + exporters)
- 🔥 **Prometheus Operator** uses `ServiceMonitor` and `PodMonitor` objects to define targets

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install monitoring prometheus-community/kube-prometheus-stack
```

---

## 10.11 💾 Storage and Retention


- ⏱️ Data is stored in a local **TSDB** (time-series database)
- ⏱️ Default retention is **15 days** (`--storage.tsdb.retention.time` to change)
- 📈 For long-term storage, use **remote write** (Thanos, Cortex, Mimir, VictoriaMetrics)

---

## 10.12 ⚖️ Pull vs Push Model


| Model | Meaning | Tool |
| --- | --- | --- |
| **Pull** | Monitoring system asks targets for data | Prometheus |
| **Push** | Targets send data to the monitoring system | Pushgateway (for short jobs) |

Pull helps to know easily if a target is **down** (`up == 0`).

---

## 10.13 🔗 Prometheus in DevOps


```text
Servers / Docker / Kubernetes / Jenkins → Exporters → Prometheus → Grafana dashboards
                                                          └──────→ Alertmanager → Slack
```

- ⚙️ Jenkins has a Prometheus metrics plugin
- 🏗️ Terraform / Ansible can install Node Exporter on all servers

---

## 10.14 🏗️ Real Example: Monitor 2 Web Servers


### 🎯 Requirement

Monitor **two web servers**, see their CPU and memory, and get a **Slack alert** when CPU stays high.

### 🏗 Architecture

```text
┌────────────────┐        ┌──────────────┐        ┌───────────────┐
│ 🖥️ web1         │        │              │        │ 🚨 Alertmanager│──► 💬 Slack
│ Node Exporter  │◄───────│ 🔥 Prometheus │───────►│               │
│ 🖥️ web2         │ scrape │              │        └───────────────┘
│ Node Exporter  │◄───────│              │───────► 📊 Grafana
└────────────────┘        └──────────────┘
```

### 🪜 Steps to Build It

```text
1. Ansible installs Node Exporter on web1 and web2
2. prometheus.yml has job "node" with both targets
3. Prometheus scrapes every 15 seconds
4. Alert rule: CPU > 80% for 5 minutes
5. Alertmanager sends a Slack message
6. ✅ Grafana shows CPU, memory and disk graphs
```

### ✅ Why This Is Better

| ❌ No Monitoring | ✅ With Prometheus |
| --- | --- |
| Users find problems first | Alert comes first |
| No history of data | Time-series history |
| Manual checking | Automatic checking |
| Slow troubleshooting | Quick root-cause search |

---

## 10.15 🧯 Troubleshooting


| Problem | Reason / Fix |
| --- | --- |
| Target shows `DOWN` | Check port, firewall / security group, exporter running |
| No data in graph | Check scrape config, time range, metric name |
| Config change not applied | Reload Prometheus (`/-/reload` or restart) |
| Alert not firing | Check `expr`, `for` duration, rule file path |
| Disk usage grows | Reduce retention or use remote storage |

Check config: `promtool check config prometheus.yml`. Check targets: `Status → Targets` in UI.

---

## 10.16 📌 Prometheus Quick Revision


- 🔥 Prometheus = **metrics monitoring + alerting**, **pull model**
- ⏱️ Stores **time-series** data in its TSDB
- 🔥 Config in `prometheus.yml` (jobs, targets, scrape interval)
- 🔥 **Exporters** expose metrics (Node Exporter port **9100**, Prometheus **9090**, Alertmanager **9093**)
- 📈 Metric types: Counter, Gauge, Histogram, Summary
- 🔹 **PromQL** for queries, `rate()` for counters
- 🚨 **Alertmanager** sends the notifications
- 📊 Grafana is used for dashboards

---

## 10.17 🧠⚡ Prometheus One-Line Memory


| Topic | Easy Memory |
| --- | --- |
| 🔥 **Prometheus** | Collects and stores metrics (pull) |
| 🔌 **Exporter** | Gives metrics from a system |
| 📈 **Time Series** | Value + time + labels |
| 🔎 **PromQL** | Query language |
| 🚨 **Alertmanager** | Sends alerts to people |
| 🔢 **Counter** | Only increases |
| 🌡️ **Gauge** | Goes up and down |
| 🎯 **Target** | Thing being monitored |

---

## 10.18 🗺️ Prometheus Learning Map


```text
Prometheus
 ├── Basics        → What, Why, Pull model
 ├── Architecture  → Server, Exporters, Alertmanager
 ├── Data          → Metrics, Labels, Types
 ├── Query         → PromQL, rate(), sum by
 ├── Alerts        → Rules, Alertmanager
 ├── Platform      → Docker, Kubernetes, Helm
 └── Visualization → Grafana
```

---

## 10.19 ⭐ Prometheus Final Memory


```text
How to collect server / app metrics?    → Prometheus + Exporters
How to monitor a Linux server?          → Node Exporter
How to query metrics?                   → PromQL
How to send alerts to Slack / email?    → Alertmanager
How to show graphs?                     → Grafana
```

> **Prometheus scrapes metrics from targets, stores them as time series, and raises alerts when something goes wrong.**


---

# 📊 PART 11 — Grafana — Dashboards and Visualization

> **Grafana = Turns Monitoring Data into Dashboards**

---

## 11.1 📊 What is Grafana?


> **Grafana = Visualization and Dashboard Platform**

Grafana **connects to many data sources** (Prometheus, Loki, CloudWatch, MySQL ...) and **shows the data as dashboards, graphs and alerts.**

**Grafana does not collect or store metrics itself.** It reads them from other tools.

### 🔹 We can use Grafana to:

- 📈 Create graphs and dashboards.
- 🔌 Connect many data sources in one place.
- 🚨 Create alerts and send them to Slack or email.
- 📥 Import ready-made dashboards.
- 👥 Share dashboards with the team.

### ⚙️ It Provides components such as:

- 🔌 Data Sources
- 🧩 Panels
- 📋 Dashboards
- 🚨 Alerting

to visualize and monitor data.

#### 🏗 Grafana Basic Flow

```text
🔥 Prometheus / 📜 Loki / ☁️ CloudWatch / 🗄️ MySQL
                    │ queries
                    ▼
               📊 Grafana (port 3000)
                    │
        ┌───────────┴───────────┐
        ▼                       ▼
 📋 Dashboards            🚨 Alerts → 💬 Slack
```

#### 🧠 Easy Memory

> **Grafana = TV Screen for Your Monitoring Data**

#### ⚠ Important

> **Prometheus collects the data. Grafana shows the data.**

> **Keep `/var/lib/grafana` on a volume, or dashboards are lost on restart.**

---

## 11.2 🤔 Why Do We Use Grafana?


Suppose metrics are stored in Prometheus, but only raw numbers are visible.

### ❌ Without Grafana

```text
🔢 Raw Numbers and Queries Only
            ↓
🤯 Hard to Understand the Trend
            ↓
🐌 Slow Problem Finding
```

### ✅ With Grafana

```text
🔌 Connect Data Source
 ↓
🧩 Create Panels
 ↓
📋 Build Dashboard
 ↓
✅ Whole Team Understands System Health Quickly
```

#### ⭐ Main Reasons

- 👀 See all monitoring data in one place
- 🔌 Combine data from different sources
- 📈 Understand trends quickly using graphs
- 🚨 Create alerts from the same screen
- 📥 Use ready-made dashboards
- 👥 Share with the team

---

## 11.3 🧰 What Does Grafana Provide?


Grafana provides:

- 📋 Dashboards
- 🧩 Panels
- 🔌 Data Sources
- 🚨 Alerting
- 🔍 Explore Mode
- 👥 Users and Teams
- 📥 Import / Export (JSON)

| 🧰 Feature | 💡 Meaning |
| --- | --- |
| 📊 Dashboards | Collection of panels |
| 🧩 Panels | One graph / gauge / table |
| 🔌 Data sources | Connect many backends |
| 🚨 Alerting | Notify when a condition is met |
| 🔍 Explore | Quick query mode for debugging |
| 👥 Users and teams | Access control |

---

## 11.4 🧱 Grafana Architecture


```text
┌──────────────────────────────┐
│      Data Sources            │
│ Prometheus | Loki | MySQL    │
│ CloudWatch | Elasticsearch   │
└──────────────┬───────────────┘
               │ queries
               ▼
        ┌─────────────┐        ┌──────────────┐
        │   Grafana   │ ─────► │ Contact Point│ → Slack / Email
        │ (port 3000) │        └──────────────┘
        └──────┬──────┘
               ▼
      Browser (Dashboards)
```

> Grafana's own settings, users and dashboards are saved in its **database** (SQLite by default, MySQL / PostgreSQL for production).

---

## 11.5 ⚙️ Installation


```bash
docker run -d --name grafana -p 3000:3000 grafana/grafana
```

- 🖥️ Open `http://<server-ip>:3000`
- 🔒 Default login: `admin` / `admin` (you are asked to change the password)
- 📊 Keep data in a volume: `-v grafana-data:/var/lib/grafana`

---

## 11.6 🔌 Data Sources


`Connections → Data sources → Add data source`

| Data Source | Used for |
| --- | --- |
| **Prometheus** | Metrics |
| **Loki** | Logs |
| **Elasticsearch** | Logs and search |
| **CloudWatch** | AWS metrics and logs |
| **MySQL / PostgreSQL** | Database data |
| **Tempo** | Traces |

Prometheus data source URL example: `http://prometheus:9090`.

---

## 11.7 🧩 Dashboards and Panels


- 📋 **Dashboard** = a page with many panels
- 🔎 **Panel** = one visualization with a query

Common panel types:

| Panel | Use |
| --- | --- |
| Time series | Line graph over time (CPU, requests) |
| Stat | One big number (current uptime) |
| Gauge | Value with min / max (disk usage %) |
| Bar chart | Compare values |
| Table | Rows and columns |
| Logs | Show log lines (with Loki) |

Example panel query (Prometheus):

```text
100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
```

---

## 11.8 🔁 Variables and Templating


**Variables** make one dashboard work for many servers / environments.

```text
Variable: instance   (dropdown)
Query:    label_values(node_cpu_seconds_total, instance)
Use in panel:  node_load1{instance="$instance"}
```

Now users **select a server from a dropdown** and all panels update.

---

## 11.9 📥 Importing Ready-Made Dashboards


- 📊 Grafana has a public dashboard library at **grafana.com/dashboards**
- 📋 Use `Dashboards → New → Import` and enter the dashboard **ID**
- 🖥️ Popular example: **Node Exporter Full** (ID **1860**)

```text
Import ID → choose Prometheus data source → Import → dashboard ready
```

---

## 11.10 🚨 Grafana Alerting


```text
Alert Rule → Notification Policy → Contact Point → Slack / Email / PagerDuty
```

| Part | Meaning |
| --- | --- |
| **Alert Rule** | Query + condition (e.g. CPU > 80% for 5m) |
| **Contact Point** | Where to send (Slack, email, webhook) |
| **Notification Policy** | Which alert goes to which contact point |
| **Silence** | Mute alerts for a time |

States: `Normal → Pending → Firing`.

> Prometheus Alertmanager can also be used. Grafana alerting is easier to manage inside the same UI.

---

## 11.11 👥 Users, Teams and Permissions


| Role | Can do |
| --- | --- |
| **Viewer** | See dashboards |
| **Editor** | Create and edit dashboards |
| **Admin** | Manage users, data sources and settings |

- 👥 Use **Teams** and **Folders** to control access
- 🌿 Login can be connected to **LDAP, OAuth, Google, GitHub** (SSO)

---

## 11.12 🧾 Provisioning (Config as Code)


Provisioning creates data sources and dashboards **from files**, not by clicking.

`/etc/grafana/provisioning/datasources/prometheus.yml`:

```yaml
apiVersion: 1
datasources:
  - name: Prometheus
    type: prometheus
    access: proxy
    url: http://prometheus:9090
    isDefault: true
```

Dashboards are stored as **JSON** and can be kept in Git.

---

## 11.13 🔗 Grafana in DevOps


```text
Servers → Node Exporter ┐
Docker  → cAdvisor      ├─► Prometheus ─► Grafana ─► Team sees dashboards
Kubernetes → kube-state ┘                        └──► Slack alerts
Logs → Promtail → Loki ─────────────────────────────┘
```

Typical stack: **Prometheus + Grafana** (metrics), **Loki + Grafana** (logs).

---

## 11.14 ☸️ Grafana in Kubernetes


Install the whole monitoring stack with Helm:

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install monitoring prometheus-community/kube-prometheus-stack
```

This installs **Prometheus, Alertmanager, Grafana** and ready dashboards for Nodes, Pods and Namespaces.

---

## 11.15 🏗️ Real Example: Server Monitoring Dashboard


### 🎯 Requirement

Give the team **one dashboard** to see all servers, with an **alert on high CPU**.

### 🏗 Architecture

```text
┌───────────────┐    ┌──────────────┐    ┌─────────────┐    ┌──────────┐
│ 🔌 Node        │───►│ 🔥 Prometheus │───►│ 📊 Grafana   │───►│ 💬 Slack  │
│   Exporters   │    │  (metrics)   │    │ (dashboard) │    │ (alerts) │
└───────────────┘    └──────────────┘    └─────────────┘    └──────────┘
```

### 🪜 Steps to Build It

```text
1. Node Exporter runs on all servers
2. Prometheus scrapes them every 15 seconds
3. Grafana adds Prometheus as a data source
4. Import dashboard ID 1860 (Node Exporter Full)
5. Create alert: CPU > 80% for 5 minutes → Slack
6. ✅ Team opens one dashboard and selects any server from the dropdown
```

### ✅ Why This Is Better

| ❌ Raw Metrics Only | ✅ Grafana Dashboard |
| --- | --- |
| Hard to read | Clear graphs |
| One server at a time | Dropdown for all servers |
| No shared view | Whole team sees same data |
| Manual alert checking | Automatic alert to Slack |

---

## 11.16 🧯 Troubleshooting


| Problem | Reason / Fix |
| --- | --- |
| "No data" in panel | Wrong data source, query or time range |
| Data source test fails | Wrong URL / port, network or firewall issue |
| Dashboard lost after restart | No volume for `/var/lib/grafana` |
| Alert not sent | Check contact point and notification policy |
| Cannot log in | Reset with `grafana-cli admin reset-admin-password <new>` |

---

## 11.17 📌 Grafana Quick Revision


- 📊 Grafana = **visualization + alerting**; it **does not collect or store metrics itself**
- 🔌 Port **3000**, default login `admin / admin`
- 📋 **Data source → Panel → Dashboard**
- 📋 **Variables** make dashboards reusable
- 📋 Import ready dashboards by ID (Node Exporter Full = **1860**)
- 🚨 Alerting: Rule → Policy → Contact Point
- 🌿 Provisioning keeps config in files / Git
- 🔥 Common stack: **Prometheus + Grafana**, **Loki + Grafana**

---

## 11.18 🧠⚡ Grafana One-Line Memory


| Topic | Easy Memory |
| --- | --- |
| 📊 **Grafana** | Dashboards for any data |
| 🔌 **Data Source** | Where Grafana reads data |
| 🧩 **Panel** | One graph |
| 📋 **Dashboard** | Many panels together |
| 🔁 **Variable** | Dropdown to change the view |
| 🚨 **Contact Point** | Where alerts are sent |
| 📥 **Import** | Use a ready dashboard |

---

## 11.19 🗺️ Grafana Learning Map


```text
Grafana
 ├── Basics        → What, Why, Install
 ├── Data Sources  → Prometheus, Loki, CloudWatch
 ├── Visualization → Panels, Dashboards, Variables
 ├── Reuse         → Import, Provisioning, JSON in Git
 ├── Alerting      → Rules, Contact Points, Policies
 ├── Access        → Users, Teams, SSO
 └── DevOps        → Prometheus + Kubernetes + Slack
```

---

## 11.20 ⭐ Grafana Final Memory


```text
How to see metrics as graphs?          → Grafana
Who collects the metrics?              → Prometheus (not Grafana)
How to reuse one dashboard?            → Variables
How to get a ready dashboard fast?     → Import by ID
How to get notified?                   → Alert Rule → Contact Point
```

> **Grafana turns monitoring data from many sources into dashboards and alerts that people can understand quickly.**


---

# 🧠⚡ Complete DevOps One-Line Memory

| Tool | Easy Memory |
| ---- | ----------- |
| 🌿 **Git** | Tracks code changes (version control) |
| 🐙 **GitHub** | Hosts Git repositories and enables teamwork |
| 📦 **Maven** | Builds Java projects and manages libraries (`pom.xml`) |
| ⚙️ **Jenkins** | Automates build, test and deploy (CI/CD) |
| 📜 **Jenkinsfile** | Pipeline written as code |
| 🔍 **SonarQube** | Checks code quality and security |
| 🚦 **Quality Gate** | Pass / Fail rule for code |
| 🗄️ **Nexus** | Warehouse for build artifacts |
| 🐳 **Docker** | Package app + dependencies into a container |
| 📄 **Dockerfile** | Recipe to build an image |
| ☸️ **Kubernetes** | Runs, scales and heals containers |
| 🧩 **Pod** | Smallest deployable unit in Kubernetes |
| 🏗️ **Terraform** | Create infrastructure from code |
| 📒 **State File** | Terraform's record of what exists |
| 🅰️ **Ansible** | Configure many servers with YAML (agentless) |
| 📋 **Inventory / Playbook** | List of servers / tasks in YAML |
| 🔥 **Prometheus** | Collects and stores metrics, sends alerts |
| 🔎 **PromQL** | Query language of Prometheus |
| 📊 **Grafana** | Dashboards for monitoring data |

---

# 🗺️ Complete DevOps Learning Map

```text
                                🚀 DevOps
                                    │
   ┌────────────┬───────────┬───────┴───────┬────────────┬────────────┐
   ▼            ▼           ▼               ▼            ▼            ▼
 SOURCE        BUILD       CI/CD         CONTAINERS     INFRA     MONITORING
   │            │           │               │            │            │
   └─ Git &     ├─ Maven    └─ Jenkins      ├─ Docker    ├─ Terraform ├─ Prometheus
      GitHub    ├─ SonarQube                  └─ Kubernetes└─ Ansible   └─ Grafana
                └─ Nexus
```

### 🪜 Suggested Learning Order (Same as the Order of These Notes)

```text
1️⃣  Git & GitHub   → Manage and share code
2️⃣  Maven          → Build the application
3️⃣  Jenkins        → Automate with CI/CD pipelines
4️⃣  SonarQube      → Check code quality
5️⃣  Nexus          → Store artifacts
6️⃣  Docker         → Containerize the app
7️⃣  Kubernetes     → Run containers at scale
8️⃣  Terraform      → Create infrastructure with code
9️⃣  Ansible        → Configure servers
🔟  Prometheus     → Collect metrics
1️⃣1️⃣ Grafana        → Visualize and alert
```

---

# ⭐ Complete DevOps Final Memory

```text
DevOps
 │
 ├── How to store and share code?
 │      └── Git & GitHub
 │
 ├── How to build a Java application?
 │      └── Maven
 │
 ├── How to automate build, test and deploy?
 │      └── Jenkins
 │
 ├── How to check code quality before release?
 │      └── SonarQube
 │
 ├── How to store build artifacts?
 │      └── Nexus
 │
 ├── How to package an app so it runs everywhere?
 │      └── Docker
 │
 ├── How to run and scale containers?
 │      └── Kubernetes
 │
 ├── How to create infrastructure from code?
 │      └── Terraform
 │
 ├── How to configure many servers together?
 │      └── Ansible
 │
 ├── How to collect metrics and alerts?
 │      └── Prometheus
 │
 └── How to see everything on dashboards?
        └── Grafana
```

---

<p align="center">

## 🚀 DevOps — Code → Build → Test → Deploy → Monitor

**Learn → Practice → Build → Automate → Monitor**

</p>
