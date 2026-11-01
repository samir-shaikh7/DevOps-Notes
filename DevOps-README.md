# 🔄🚀 DevOps — Complete Notes

<p align="center">

**Git & GitHub • Maven • Jenkins • SonarQube • Nexus • Docker • Terraform • Ansible • Kubernetes • Prometheus • Grafana**

![DevOps](https://img.shields.io/badge/DevOps-Tools-blue?style=for-the-badge)
![CI/CD](https://img.shields.io/badge/CI%2FCD-Automation-orange?style=for-the-badge)
![DevOps Learning](https://img.shields.io/badge/DevOps-Learning-success?style=for-the-badge)

</p>

---

## 📖 About These Notes

This single file covers **11 core DevOps tools** in simple English, in the **order of the DevOps lifecycle**.

```text
💻 Code            → Git & GitHub
🔨 Build           → Maven
🤖 Integrate       → Jenkins
🔍 Quality         → SonarQube
📦 Artifacts       → Nexus Repository
🐳 Package         → Docker
🏗️ Infrastructure  → Terraform
⚙️ Configuration   → Ansible
☸️ Orchestrate     → Kubernetes
📊 Monitor         → Prometheus → Grafana
```

Every tool follows the same flow:

```text
1. 📖 Definition and Simple Meaning
2. 🤔 Why do we use it?
3. 🧱 Concepts and sub-topics
4. 💻 Commands, code and configuration examples
5. 🏗️ Real example
6. 📌 Quick Revision + 🧠 One-Line Memory + 🗺️ Learning Map + ⭐ Final Memory
```

## 📚 Table of Contents

> Click a part to open its list of topics.

<details>
<summary><b>🔄 PART 1 — DEVOPS BASICS — Culture, Lifecycle and CI/CD</b></summary>

- [1.1 🔄 What is DevOps?](#11--what-is-devops)
- [1.2 🤔 Why Do We Use DevOps?](#12--why-do-we-use-devops)
- [1.3 ♾️ DevOps Lifecycle](#13--devops-lifecycle)
- [1.4 🔁 CI, CD and CD](#14--ci-cd-and-cd)
- [1.5 🧩 Core DevOps Practices](#15--core-devops-practices)
- [1.6 🏗️ Typical CI/CD Pipeline](#16--typical-cicd-pipeline)
- [1.7 🗺️ DevOps Tools Map](#17--devops-tools-map)
- [1.8 📚 Tools Covered in These Notes](#18--tools-covered-in-these-notes)

</details>

<details>
<summary><b>🔗 PART 2 — Git & GitHub — Version Control</b></summary>

- [2.1 🔗 What is Git?](#21--what-is-git)
- [2.2 🐙 What is GitHub?](#22--what-is-github)
- [2.3 🤔 Why Do We Use Git?](#23--why-do-we-use-git)
- [2.4 🧰 Types of Version Control Systems](#24--types-of-version-control-systems)
- [2.5 🧱 Git Basic Concepts](#25--git-basic-concepts)
- [2.6 ⚙️ Installing and Configuring Git](#26--installing-and-configuring-git)
- [2.7 🚀 Basic Git Workflow and Commands](#27--basic-git-workflow-and-commands)
- [2.8 🌿 Branching](#28--branching)
- [2.9 🌐 Working with Remote Repositories](#29--working-with-remote-repositories)
- [2.10 ⏪ Undoing Changes](#210--undoing-changes)
- [2.11 💼 Other Useful Git Features](#211--other-useful-git-features)
- [2.12 🔀 Branching Strategies](#212--branching-strategies)
- [2.13 🐙 GitHub Features](#213--github-features)
- [2.14 🏆 Git Best Practices](#214--git-best-practices)
- [2.15 ⌨️ Git Commands Cheat Sheet](#215--git-commands-cheat-sheet)
- [2.16 🏗️ Real Example: Feature to Pull Request](#216--real-example-feature-to-pull-request)
- [📌🧠 Git & GitHub Quick Revision](#-git--github-quick-revision)
- [🧠⚡ Git & GitHub One-Line Memory](#-git--github-one-line-memory)
- [🗺️ Git & GitHub Learning Map](#-git--github-learning-map)
- [⭐ Git & GitHub Final Memory](#-git--github-final-memory)

</details>

<details>
<summary><b>🔨 PART 3 — Maven — Build Tool</b></summary>

- [3.1 🔨 What is Maven?](#31--what-is-maven)
- [3.2 🤔 Why Do We Use Maven?](#32--why-do-we-use-maven)
- [3.3 🧰 What Does Maven Provide?](#33--what-does-maven-provide)
- [3.4 ⚙️ Installing Maven](#34--installing-maven)
- [3.5 📂 Standard Directory Layout](#35--standard-directory-layout)
- [3.6 📄 POM (Project Object Model)](#36--pom-project-object-model)
- [3.7 🗄️ Maven Repositories](#37--maven-repositories)
- [3.8 📥 Dependency Management](#38--dependency-management)
- [3.9 🔄 Maven Build Lifecycle](#39--maven-build-lifecycle)
- [3.10 🔌 Plugins and Goals](#310--plugins-and-goals)
- [3.11 ⌨️ Common Maven Commands](#311--common-maven-commands)
- [3.12 🧬 Archetypes (Project Templates)](#312--archetypes-project-templates)
- [3.13 ⚙️ settings.xml](#313--settingsxml)
- [3.14 📤 Deploying to Nexus](#314--deploying-to-nexus)
- [3.15 🧩 Multi-Module Projects](#315--multi-module-projects)
- [3.16 🎭 Profiles](#316--profiles)
- [3.17 🆚 Maven vs Gradle vs Ant](#317--maven-vs-gradle-vs-ant)
- [3.18 🔗 Maven in a CI/CD Pipeline](#318--maven-in-a-cicd-pipeline)
- [3.19 🏗️ Real Example: Build a Java Project](#319--real-example-build-a-java-project)
- [📌🧠 Maven Quick Revision](#-maven-quick-revision)
- [🧠⚡ Maven One-Line Memory](#-maven-one-line-memory)
- [🗺️ Maven Learning Map](#-maven-learning-map)
- [⭐ Maven Final Memory](#-maven-final-memory)

</details>

<details>
<summary><b>🤖 PART 4 — Jenkins — CI/CD Automation Server</b></summary>

- [4.1 🤖 What is Jenkins?](#41--what-is-jenkins)
- [4.2 🤔 Why Do We Use Jenkins?](#42--why-do-we-use-jenkins)
- [4.3 🧰 What Does Jenkins Provide?](#43--what-does-jenkins-provide)
- [4.4 🏛️ Jenkins Architecture](#44--jenkins-architecture)
- [4.5 ⚙️ Installing Jenkins](#45--installing-jenkins)
- [4.6 🖥️ Jenkins Dashboard and Key Areas](#46--jenkins-dashboard-and-key-areas)
- [4.7 🔌 Plugins](#47--plugins)
- [4.8 🧱 Types of Jenkins Jobs](#48--types-of-jenkins-jobs)
- [4.9 📜 Jenkins Pipeline](#49--jenkins-pipeline)
- [4.10 🔑 Credentials](#410--credentials)
- [4.11 ⏰ Build Triggers](#411--build-triggers)
- [4.12 🔧 Global Tool Configuration](#412--global-tool-configuration)
- [4.13 🔗 Jenkins Integrations](#413--jenkins-integrations)
- [4.14 🌍 Useful Built-in Variables](#414--useful-built-in-variables)
- [4.15 🖥️ Distributed Builds (Agents)](#415--distributed-builds-agents)
- [4.16 📚 Shared Libraries](#416--shared-libraries)
- [4.17 🔒 Jenkins Security](#417--jenkins-security)
- [4.18 💾 Backup and Maintenance](#418--backup-and-maintenance)
- [4.19 🏆 Jenkins Best Practices](#419--jenkins-best-practices)
- [4.20 🏗️ Real Example: Full CI/CD Pipeline](#420--real-example-full-cicd-pipeline)
- [📌🧠 Jenkins Quick Revision](#-jenkins-quick-revision)
- [🧠⚡ Jenkins One-Line Memory](#-jenkins-one-line-memory)
- [🗺️ Jenkins Learning Map](#-jenkins-learning-map)
- [⭐ Jenkins Final Memory](#-jenkins-final-memory)

</details>

<details>
<summary><b>🔍 PART 5 — SonarQube — Code Quality and Security</b></summary>

- [5.1 🔍 What is SonarQube?](#51--what-is-sonarqube)
- [5.2 🤔 Why Do We Use SonarQube?](#52--why-do-we-use-sonarqube)
- [5.3 🧰 What Does SonarQube Provide?](#53--what-does-sonarqube-provide)
- [5.4 🏛️ SonarQube Architecture](#54--sonarqube-architecture)
- [5.5 🧱 SonarQube Editions](#55--sonarqube-editions)
- [5.6 ⚙️ Installing SonarQube](#56--installing-sonarqube)
- [5.7 🧱 SonarQube Basic Concepts](#57--sonarqube-basic-concepts)
- [5.8 📏 Quality Profile](#58--quality-profile)
- [5.9 🚦 Quality Gate](#59--quality-gate)
- [5.10 🔑 Tokens](#510--tokens)
- [5.11 🔎 Running a Scan](#511--running-a-scan)
- [5.12 🧪 Code Coverage With JaCoCo](#512--code-coverage-with-jacoco)
- [5.13 🔗 SonarQube With Jenkins](#513--sonarqube-with-jenkins)
- [5.14 🪝 Webhooks and PR Decoration](#514--webhooks-and-pr-decoration)
- [5.15 👥 Users, Permissions and Security](#515--users-permissions-and-security)
- [5.16 🏆 SonarQube Best Practices](#516--sonarqube-best-practices)
- [5.17 🏗️ Real Example: Quality Check in a Pipeline](#517--real-example-quality-check-in-a-pipeline)
- [📌🧠 SonarQube Quick Revision](#-sonarqube-quick-revision)
- [🧠⚡ SonarQube One-Line Memory](#-sonarqube-one-line-memory)
- [🗺️ SonarQube Learning Map](#-sonarqube-learning-map)
- [⭐ SonarQube Final Memory](#-sonarqube-final-memory)

</details>

<details>
<summary><b>📦 PART 6 — Nexus Repository — Artifact Management</b></summary>

- [6.1 📦 What is Nexus Repository?](#61--what-is-nexus-repository)
- [6.2 🤔 Why Do We Use Nexus?](#62--why-do-we-use-nexus)
- [6.3 🧰 What Does Nexus Provide?](#63--what-does-nexus-provide)
- [6.4 🧱 Nexus Basic Concepts](#64--nexus-basic-concepts)
- [6.5 🗄️ Repository Types](#65--repository-types)
- [6.6 🔢 Default Maven Repositories](#66--default-maven-repositories)
- [6.7 🧩 Supported Formats](#67--supported-formats)
- [6.8 🧱 Editions](#68--editions)
- [6.9 ⚙️ Installing Nexus](#69--installing-nexus)
- [6.10 💾 Blob Stores](#610--blob-stores)
- [6.11 🧹 Cleanup Policies and Tasks](#611--cleanup-policies-and-tasks)
- [6.12 👥 Security: Users, Roles and Privileges](#612--security-users-roles-and-privileges)
- [6.13 🔗 Using Nexus With Maven](#613--using-nexus-with-maven)
- [6.14 🐳 Docker Registry in Nexus](#614--docker-registry-in-nexus)
- [6.15 🟢 Using Nexus With npm and PyPI](#615--using-nexus-with-npm-and-pypi)
- [6.16 🔗 Nexus With Jenkins](#616--nexus-with-jenkins)
- [6.17 💾 Backup and Maintenance](#617--backup-and-maintenance)
- [6.18 🆚 Nexus vs Artifactory vs Docker Hub](#618--nexus-vs-artifactory-vs-docker-hub)
- [6.19 🏆 Nexus Best Practices](#619--nexus-best-practices)
- [6.20 🏗️ Real Example: Nexus in a Maven Pipeline](#620--real-example-nexus-in-a-maven-pipeline)
- [📌🧠 Nexus Repository Quick Revision](#-nexus-repository-quick-revision)
- [🧠⚡ Nexus Repository One-Line Memory](#-nexus-repository-one-line-memory)
- [🗺️ Nexus Repository Learning Map](#-nexus-repository-learning-map)
- [⭐ Nexus Repository Final Memory](#-nexus-repository-final-memory)

</details>

<details>
<summary><b>🐳 PART 7 — Docker — Containers</b></summary>

- [7.1 🐳 What is Docker?](#71--what-is-docker)
- [7.2 🤔 Why Do We Use Docker?](#72--why-do-we-use-docker)
- [7.3 🧰 What Does Docker Provide?](#73--what-does-docker-provide)
- [7.4 🆚 Containers vs Virtual Machines](#74--containers-vs-virtual-machines)
- [7.5 🏛️ Docker Architecture](#75--docker-architecture)
- [7.6 ⚙️ Installing Docker](#76--installing-docker)
- [7.7 📦 Docker Images](#77--docker-images)
- [7.8 🐳 Docker Containers](#78--docker-containers)
- [7.9 📄 Dockerfile](#79--dockerfile)
- [7.10 🏗️ Multi-Stage Builds](#710--multi-stage-builds)
- [7.11 🗄️ Docker Registry](#711--docker-registry)
- [7.12 💾 Docker Volumes](#712--docker-volumes)
- [7.13 🌐 Docker Networking](#713--docker-networking)
- [7.14 🧩 Docker Compose](#714--docker-compose)
- [7.15 🔒 Docker Security](#715--docker-security)
- [7.16 🧹 Cleanup Commands](#716--cleanup-commands)
- [7.17 ⚡ Docker Best Practices](#717--docker-best-practices)
- [7.18 🔗 Docker in a CI/CD Pipeline](#718--docker-in-a-cicd-pipeline)
- [7.19 🏗️ Real Example: Containerize a Java App](#719--real-example-containerize-a-java-app)
- [📌🧠 Docker Quick Revision](#-docker-quick-revision)
- [🧠⚡ Docker One-Line Memory](#-docker-one-line-memory)
- [🗺️ Docker Learning Map](#-docker-learning-map)
- [⭐ Docker Final Memory](#-docker-final-memory)

</details>

<details>
<summary><b>🏗️ PART 8 — Terraform — Infrastructure as Code</b></summary>

- [8.1 🏗️ What is Terraform?](#81--what-is-terraform)
- [8.2 🤔 Why Do We Use Terraform?](#82--why-do-we-use-terraform)
- [8.3 🧰 What Does Terraform Provide?](#83--what-does-terraform-provide)
- [8.4 🆚 Declarative vs Imperative](#84--declarative-vs-imperative)
- [8.5 ⚙️ Installing Terraform](#85--installing-terraform)
- [8.6 🧱 Terraform Basic Concepts](#86--terraform-basic-concepts)
- [8.7 📝 Terraform Language (HCL)](#87--terraform-language-hcl)
- [8.8 📂 Terraform File Structure](#88--terraform-file-structure)
- [8.9 🔌 Providers](#89--providers)
- [8.10 🔄 Terraform Workflow](#810--terraform-workflow)
- [8.11 🎛️ Variables](#811--variables)
- [8.12 🔍 Data Sources](#812--data-sources)
- [8.13 📄 Terraform State](#813--terraform-state)
- [8.14 🔁 Meta-Arguments](#814--meta-arguments)
- [8.15 📚 Modules](#815--modules)
- [8.16 🌿 Workspaces](#816--workspaces)
- [8.17 🧮 Expressions and Functions](#817--expressions-and-functions)
- [8.18 🛠️ Provisioners (Last Resort)](#818--provisioners-last-resort)
- [8.19 🆚 Terraform vs CloudFormation vs Ansible](#819--terraform-vs-cloudformation-vs-ansible)
- [8.20 🔗 Terraform in a CI/CD Pipeline](#820--terraform-in-a-cicd-pipeline)
- [8.21 🏆 Terraform Best Practices](#821--terraform-best-practices)
- [8.22 🏗️ Real Example: EC2 Web Server With Security Group](#822--real-example-ec2-web-server-with-security-group)
- [📌🧠 Terraform Quick Revision](#-terraform-quick-revision)
- [🧠⚡ Terraform One-Line Memory](#-terraform-one-line-memory)
- [🗺️ Terraform Learning Map](#-terraform-learning-map)
- [⭐ Terraform Final Memory](#-terraform-final-memory)

</details>

<details>
<summary><b>⚙️ PART 9 — Ansible — Configuration Management</b></summary>

- [9.1 ⚙️ What is Ansible?](#91--what-is-ansible)
- [9.2 🤔 Why Do We Use Ansible?](#92--why-do-we-use-ansible)
- [9.3 🧰 What Does Ansible Provide?](#93--what-does-ansible-provide)
- [9.4 🏛️ Ansible Architecture](#94--ansible-architecture)
- [9.5 ⚙️ Installing Ansible](#95--installing-ansible)
- [9.6 📋 Inventory](#96--inventory)
- [9.7 ⌨️ Ad-Hoc Commands](#97--ad-hoc-commands)
- [9.8 📜 Playbooks](#98--playbooks)
- [9.9 🎛️ Variables and Facts](#99--variables-and-facts)
- [9.10 🧠 Conditions, Loops and Tags](#910--conditions-loops-and-tags)
- [9.11 🔔 Handlers](#911--handlers)
- [9.12 📄 Templates (Jinja2)](#912--templates-jinja2)
- [9.13 🎭 Roles](#913--roles)
- [9.14 🔐 Ansible Vault](#914--ansible-vault)
- [9.15 ⚙️ ansible.cfg](#915--ansiblecfg)
- [9.16 🧪 Safe Running and Debugging](#916--safe-running-and-debugging)
- [9.17 🆚 Ansible vs Terraform vs Puppet / Chef](#917--ansible-vs-terraform-vs-puppet--chef)
- [9.18 🔗 Ansible With Other Tools](#918--ansible-with-other-tools)
- [9.19 🏆 Ansible Best Practices](#919--ansible-best-practices)
- [9.20 🏗️ Real Example: Deploy an App to Web Servers](#920--real-example-deploy-an-app-to-web-servers)
- [📌🧠 Ansible Quick Revision](#-ansible-quick-revision)
- [🧠⚡ Ansible One-Line Memory](#-ansible-one-line-memory)
- [🗺️ Ansible Learning Map](#-ansible-learning-map)
- [⭐ Ansible Final Memory](#-ansible-final-memory)

</details>

<details>
<summary><b>☸️ PART 10 — Kubernetes — Container Orchestration</b></summary>

- [10.1 ☸️ What is Kubernetes?](#101--what-is-kubernetes)
- [10.2 🤔 Why Do We Use Kubernetes?](#102--why-do-we-use-kubernetes)
- [10.3 🧰 What Does Kubernetes Provide?](#103--what-does-kubernetes-provide)
- [10.4 🏛️ Kubernetes Architecture](#104--kubernetes-architecture)
- [10.5 📖 Kubernetes Key Terms](#105--kubernetes-key-terms)
- [10.6 ⚙️ Setting Up Kubernetes](#106--setting-up-kubernetes)
- [10.7 ⌨️ kubectl — The Command Line Tool](#107--kubectl--the-command-line-tool)
- [10.8 📄 YAML Manifest Structure](#108--yaml-manifest-structure)
- [10.9 📦 Pods](#109--pods)
- [10.10 🚀 Deployments and ReplicaSets](#1010--deployments-and-replicasets)
- [10.11 🌐 Services](#1011--services)
- [10.12 🌍 Ingress](#1012--ingress)
- [10.13 🧱 Namespaces](#1013--namespaces)
- [10.14 ⚙️ ConfigMaps and 🔐 Secrets](#1014--configmaps-and--secrets)
- [10.15 💾 Storage](#1015--storage)
- [10.16 🗂️ Other Workload Types](#1016--other-workload-types)
- [10.17 🩺 Health Checks (Probes)](#1017--health-checks-probes)
- [10.18 📏 Resource Requests and Limits](#1018--resource-requests-and-limits)
- [10.19 📈 Autoscaling](#1019--autoscaling)
- [10.20 🔐 Security and RBAC](#1020--security-and-rbac)
- [10.21 ⛵ Helm — The Package Manager](#1021--helm--the-package-manager)
- [10.22 🔗 Kubernetes in a CI/CD Pipeline](#1022--kubernetes-in-a-cicd-pipeline)
- [10.23 🏆 Kubernetes Best Practices](#1023--kubernetes-best-practices)
- [10.24 🏗️ Real Example: Deploy a Web App](#1024--real-example-deploy-a-web-app)
- [📌🧠 Kubernetes Quick Revision](#-kubernetes-quick-revision)
- [🧠⚡ Kubernetes One-Line Memory](#-kubernetes-one-line-memory)
- [🗺️ Kubernetes Learning Map](#-kubernetes-learning-map)
- [⭐ Kubernetes Final Memory](#-kubernetes-final-memory)

</details>

<details>
<summary><b>🔥 PART 11 — Prometheus — Metrics and Alerting</b></summary>

- [11.1 🔥 What is Prometheus?](#111--what-is-prometheus)
- [11.2 🤔 Why Do We Use Prometheus?](#112--why-do-we-use-prometheus)
- [11.3 🧰 What Does Prometheus Provide?](#113--what-does-prometheus-provide)
- [11.4 🏛️ Prometheus Architecture](#114--prometheus-architecture)
- [11.5 🔄 Pull Model vs Push Model](#115--pull-model-vs-push-model)
- [11.6 🧱 Data Model and Metric Types](#116--data-model-and-metric-types)
- [11.7 ⚙️ Installing Prometheus](#117--installing-prometheus)
- [11.8 📄 Configuration (`prometheus.yml`)](#118--configuration-prometheusyml)
- [11.9 🔌 Exporters](#119--exporters)
- [11.10 🔍 PromQL (Prometheus Query Language)](#1110--promql-prometheus-query-language)
- [11.11 🚨 Alerting Rules](#1111--alerting-rules)
- [11.12 🧾 Recording Rules](#1112--recording-rules)
- [11.13 🔔 Alertmanager](#1113--alertmanager)
- [11.14 🗄️ Storage and Retention](#1114--storage-and-retention)
- [11.15 🔭 Service Discovery](#1115--service-discovery)
- [11.16 ☸️ Prometheus With Kubernetes](#1116--prometheus-with-kubernetes)
- [11.17 🆚 Prometheus vs CloudWatch vs Nagios](#1117--prometheus-vs-cloudwatch-vs-nagios)
- [11.18 🔗 Prometheus in the DevOps Pipeline](#1118--prometheus-in-the-devops-pipeline)
- [11.19 🏆 Prometheus Best Practices](#1119--prometheus-best-practices)
- [11.20 🏗️ Real Example: Monitor Linux Servers](#1120--real-example-monitor-linux-servers)
- [📌🧠 Prometheus Quick Revision](#-prometheus-quick-revision)
- [🧠⚡ Prometheus One-Line Memory](#-prometheus-one-line-memory)
- [🗺️ Prometheus Learning Map](#-prometheus-learning-map)
- [⭐ Prometheus Final Memory](#-prometheus-final-memory)

</details>

<details>
<summary><b>📈 PART 12 — Grafana — Dashboards and Visualization</b></summary>

- [12.1 📈 What is Grafana?](#121--what-is-grafana)
- [12.2 🤔 Why Do We Use Grafana?](#122--why-do-we-use-grafana)
- [12.3 🧰 What Does Grafana Provide?](#123--what-does-grafana-provide)
- [12.4 🧱 Grafana Basic Concepts](#124--grafana-basic-concepts)
- [12.5 ⚙️ Installing Grafana](#125--installing-grafana)
- [12.6 🔌 Data Sources](#126--data-sources)
- [12.7 📊 Dashboards and Panels](#127--dashboards-and-panels)
- [12.8 🧮 Variables and Templating](#128--variables-and-templating)
- [12.9 📥 Import Ready-Made Dashboards](#129--import-ready-made-dashboards)
- [12.10 🔍 Explore](#1210--explore)
- [12.11 🚨 Grafana Alerting](#1211--grafana-alerting)
- [12.12 🏷️ Annotations](#1212--annotations)
- [12.13 👥 Users, Teams and Permissions](#1213--users-teams-and-permissions)
- [12.14 ⚙️ Provisioning (Config as Code)](#1214--provisioning-config-as-code)
- [12.15 🧩 Plugins and the Grafana Stack](#1215--plugins-and-the-grafana-stack)
- [12.16 ☸️ Grafana With Kubernetes](#1216--grafana-with-kubernetes)
- [12.17 🆚 Grafana vs Prometheus vs Kibana](#1217--grafana-vs-prometheus-vs-kibana)
- [12.18 🏆 Grafana Best Practices](#1218--grafana-best-practices)
- [12.19 🏗️ Real Example: Server Monitoring Dashboard](#1219--real-example-server-monitoring-dashboard)
- [📌🧠 Grafana Quick Revision](#-grafana-quick-revision)
- [🧠⚡ Grafana One-Line Memory](#-grafana-one-line-memory)
- [🗺️ Grafana Learning Map](#-grafana-learning-map)
- [⭐ Grafana Final Memory](#-grafana-final-memory)

</details>

<details>
<summary><b>🧩 PART 13 — Putting It All Together</b></summary>

- [13.1 🧩 Tool Categories — Big Picture](#131--tool-categories--big-picture)
- [13.2 🏗️ The Complete CI/CD Flow (End to End)](#132--the-complete-cicd-flow-end-to-end)
- [13.3 🌱 Environments: Dev → Test → Prod](#133--environments-dev--test--prod)
- [13.4 ⚖️ Important Comparisons](#134--important-comparisons)
- [13.5 ☁️ DevOps Tools and AWS Services](#135--devops-tools-and-aws-services)
- [13.6 ⌨️ Command Cheat Sheet](#136--command-cheat-sheet)
- [13.7 🔐 Security in DevOps (DevSecOps)](#137--security-in-devops-devsecops)
- [13.8 ✅ Production Checklist](#138--production-checklist)
- [13.9 🎯 Practice Project Roadmap](#139--practice-project-roadmap)
- [13.10 🚑 Troubleshooting Quick Guide](#1310--troubleshooting-quick-guide)

</details>

- **[📌🧠 Complete DevOps Quick Revision](#-complete-devops-quick-revision)**
- **[🧠⚡ Complete DevOps One-Line Memory](#-complete-devops-one-line-memory)**
- **[🗺️ Complete DevOps Learning Map](#-complete-devops-learning-map)**
- **[⭐ Complete DevOps Final Memory](#-complete-devops-final-memory)**
- [🔄 DevOps — Build, Ship, Run, Monitor, Repeat](#-devops--build-ship-run-monitor-repeat)

---

# 🔄 PART 1 — DEVOPS BASICS — Culture, Lifecycle and CI/CD

> Start here. Understand DevOps before learning the tools.

---

## 1.1 🔄 What is DevOps?

> **DevOps = Development + Operations**

DevOps is a **culture and a set of practices** that brings the **Development team** (who write code) and the **Operations team** (who run servers) **together**, so software can be **built, tested, released and monitored faster and more reliably**.

#### 👥 Two Teams

```text
👨‍💻 Development Team  → Writes code, adds new features
🛠️ Operations Team    → Deploys, runs and maintains servers
```

#### ❌ Before DevOps

```text
👨‍💻 Developers write code
        ↓  (throw it over the wall)
🛠️ Operations deploy it
        ↓
💥 "It works on my machine!" — "It fails on the server!"
        ↓
🐢 Slow releases, blame, manual work
```

#### ✅ With DevOps

```text
👨‍💻🛠️ One team shares responsibility
        ↓
🤖 Automation for build, test, deploy
        ↓
🚀 Fast, safe and frequent releases
        ↓
📊 Monitoring and quick feedback
```

#### 🧠 Easy Memory

> **DevOps = Dev + Ops working together with automation**

---

## 1.2 🤔 Why Do We Use DevOps?

#### ⭐ Main Reasons

- ⚡ **Faster delivery** of features
- 🐛 **Fewer bugs** (automatic testing and code checks)
- 🔁 **Repeatable** and reliable releases
- 🤝 Better **teamwork** between developers and operations
- 🛠️ Quick **fixing** of problems (monitoring + rollback)
- 💰 Less manual work, lower cost
- 📈 Easy **scaling**

#### 📊 Traditional vs DevOps

| Feature          | 🐢 Traditional                    | 🚀 DevOps                              |
| ---------------- | --------------------------------- | -------------------------------------- |
| Release speed    | Months                            | Days or hours                          |
| Process          | Manual                            | Automated (CI/CD)                      |
| Teams            | Separate (silos)                  | Shared responsibility                  |
| Infrastructure   | Set up by hand                    | Code (IaC)                             |
| Feedback         | Late                              | Fast and continuous                    |
| Failures         | Found in production               | Found early                            |

---

## 1.3 ♾️ DevOps Lifecycle

DevOps is a **continuous loop** (infinity cycle).

```text
        ┌──────────── DEV ────────────┐
        │                             │
   📝 Plan → 💻 Code → 🔨 Build → 🧪 Test
        ▲                             │
        │                             ▼
   📊 Monitor ← ⚙️ Operate ← 🚀 Deploy ← 📦 Release
        │                             
        └──────────── OPS ────────────┘
```

### 1.3.1 📖 Stages

| Stage        | What Happens                              | Example Tools (in these notes)        |
| ------------ | ----------------------------------------- | ------------------------------------- |
| 📝 Plan      | Decide features and tasks                 | Jira, GitHub Issues                   |
| 💻 Code      | Write and store code                      | **Git, GitHub**                       |
| 🔨 Build     | Compile code, create package              | **Maven**                             |
| 🧪 Test      | Test and check code quality               | JUnit, **SonarQube**                  |
| 📦 Release   | Store versions of packages and images     | **Nexus**, Docker Registry            |
| 🚀 Deploy    | Put the application on servers            | **Jenkins, Ansible, Kubernetes**      |
| ⚙️ Operate   | Create and manage infrastructure          | **Terraform, Ansible, Docker, Kubernetes** |
| 📊 Monitor   | Watch health, performance and errors      | **Prometheus, Grafana**               |

---

## 1.4 🔁 CI, CD and CD

```text
🔁 CI / CD
│
├── 🔗 CI  → Continuous Integration
├── 📦 CD  → Continuous Delivery
└── 🚀 CD  → Continuous Deployment
```

### 1.4.1 🔗 Continuous Integration (CI)

Developers **merge code often** into a shared repository, and every merge triggers an **automatic build and test**.

```text
👨‍💻 Push code → 🔨 Auto build → 🧪 Auto test → ✅ / ❌ Result
```

> **CI = Build and test automatically on every code change**

### 1.4.2 📦 Continuous Delivery

After CI, the application is **always ready to release**, but a **human approves** the final deployment to production.

> **Continuous Delivery = Always ready to deploy, manual approval for production**

### 1.4.3 🚀 Continuous Deployment

Every change that passes all tests is **deployed to production automatically**, with **no manual approval**.

> **Continuous Deployment = Fully automatic release to production**

### 1.4.4 📊 Comparison

| Practice                  | Build + Test | Ready to Release | Production Deploy        |
| ------------------------- | ------------ | ---------------- | ------------------------ |
| 🔗 Continuous Integration | ✅ Auto      | —                | —                        |
| 📦 Continuous Delivery    | ✅ Auto      | ✅ Always        | 👤 Manual approval       |
| 🚀 Continuous Deployment  | ✅ Auto      | ✅ Always        | 🤖 Automatic             |

#### 🧠 Easy Memory

```text
CI                     = Merge → Build → Test
Continuous Delivery    = CI + ready to release (button click)
Continuous Deployment  = CI + automatic release (no click)
```

---

## 1.5 🧩 Core DevOps Practices

```text
🧩 DevOps Practices
│
├── 🔗 Version Control             → Git
├── 🤖 CI/CD Pipeline              → Jenkins
├── 🏗️ Infrastructure as Code (IaC) → Terraform
├── ⚙️ Configuration Management    → Ansible
├── 🐳 Containerization            → Docker
├── ☸️ Container Orchestration     → Kubernetes
├── 📊 Monitoring and Logging      → Prometheus, Grafana
└── 🤝 Collaboration and Feedback
```

### 1.5.1 📖 Simple Definitions

| Practice                     | Simple Meaning                                              |
| ---------------------------- | ----------------------------------------------------------- |
| 🔗 Version Control           | Save and track every change in code                         |
| 🤖 CI/CD Pipeline            | Automatic steps from code to deployment                     |
| 🏗️ Infrastructure as Code    | Create servers and networks by writing code                 |
| ⚙️ Configuration Management  | Set up software and settings on many servers automatically  |
| 🐳 Containerization          | Pack an app with everything it needs to run anywhere        |
| ☸️ Orchestration             | Run and manage many containers automatically                |
| 📊 Monitoring                | Watch the system and alert when something is wrong          |

---

## 1.6 🏗️ Typical CI/CD Pipeline

```text
👨‍💻 Developer
     │ git push
     ▼
🐙 GitHub (Source Code)
     │ webhook
     ▼
🤖 Jenkins Pipeline
     │
     ├── 1️⃣ Checkout code
     ├── 2️⃣ 🔨 Build with Maven
     ├── 3️⃣ 🧪 Run unit tests
     ├── 4️⃣ 🔍 SonarQube code analysis (Quality Gate)
     ├── 5️⃣ 📦 Upload artifact (.jar / .war) to Nexus
     ├── 6️⃣ 🐳 Build Docker image and push to registry
     └── 7️⃣ 🚀 Deploy to Kubernetes (or servers using Ansible)
                       │
                       ▼
              ☸️ Kubernetes Cluster  (infrastructure created by 🏗️ Terraform)
                       │
                       ▼
        📊 Prometheus collects metrics → 📈 Grafana dashboards + 🔔 alerts
```

---

## 1.7 🗺️ DevOps Tools Map

| Category                    | Tool                  | Main Job                                  |
| --------------------------- | --------------------- | ----------------------------------------- |
| 🔗 Source Control           | **Git & GitHub**      | Store and track code                      |
| 🔨 Build Tool               | **Maven**             | Compile and package Java projects         |
| 🤖 CI/CD Server             | **Jenkins**           | Automate build, test and deploy           |
| 🔍 Code Quality             | **SonarQube**         | Find bugs and code smells                 |
| 📦 Artifact Repository      | **Nexus Repository**  | Store build artifacts and dependencies    |
| 🐳 Containerization         | **Docker**            | Package apps into containers              |
| 🏗️ Infrastructure as Code   | **Terraform**         | Create cloud infrastructure from code     |
| ⚙️ Configuration Management | **Ansible**           | Configure servers automatically           |
| ☸️ Orchestration            | **Kubernetes**        | Run containers at scale                   |
| 📊 Metrics Collection       | **Prometheus**        | Collect and store metrics, alerts         |
| 📈 Visualization            | **Grafana**           | Dashboards and graphs                     |

---

## 1.8 📚 Tools Covered in These Notes

These notes follow the **order of the DevOps lifecycle**: code → build → integrate → quality → artifacts → containers → infrastructure → configuration → orchestration → monitoring.

| Part | Tool                    | Category                  | Simple Meaning                           |
| ---- | ----------------------- | ------------------------- | ---------------------------------------- |
| 2    | 🔗 **Git & GitHub**     | Source Control            | Track and share code                     |
| 3    | 🔨 **Maven**            | Build Tool                | Build and manage Java projects           |
| 4    | 🤖 **Jenkins**          | CI/CD                     | Automation server                        |
| 5    | 🔍 **SonarQube**        | Code Quality              | Code analysis and quality gate           |
| 6    | 📦 **Nexus Repository** | Artifact Management       | Store artifacts and dependencies         |
| 7    | 🐳 **Docker**           | Containers                | Package apps in containers               |
| 8    | 🏗️ **Terraform**        | Infrastructure as Code    | Create infrastructure with code          |
| 9    | ⚙️ **Ansible**          | Configuration Management  | Configure servers automatically          |
| 10   | ☸️ **Kubernetes**       | Orchestration             | Run containers at scale                  |
| 11   | 📊 **Prometheus**       | Monitoring                | Collect metrics and alerts               |
| 12   | 📈 **Grafana**          | Visualization             | Dashboards                               |
| 13   | 🧩 **Putting It All Together** | Summary            | Full pipeline and comparisons            |

#### 🪜 Suggested Learning Order

```text
1️⃣  Git & GitHub     → Save and share code
2️⃣  Maven            → Build the project
3️⃣  Jenkins          → Automate with a pipeline
4️⃣  SonarQube        → Check code quality
5️⃣  Nexus            → Store artifacts
6️⃣  Docker           → Containerize the app
7️⃣  Terraform        → Create infrastructure
8️⃣  Ansible          → Configure servers
9️⃣  Kubernetes       → Orchestrate containers
🔟  Prometheus       → Collect metrics
1️⃣1️⃣ Grafana          → Visualize and alert
```

#### 💡 Prerequisites (Good to Know)

- 🐧 Basic **Linux** commands
- 🌐 Basic **networking** (IP, ports, DNS)
- ☁️ Basic **cloud** knowledge (AWS notes)
- 💻 Basic **scripting** (Bash, YAML)

---

# 🔗 PART 2 — Git & GitHub — Version Control

> **Git = Time machine for our code. GitHub = Online home for Git repositories.**

---

## 2.1 🔗 What is Git?

> **Git = Distributed Version Control System (VCS)**

Git is a tool that **tracks every change made to files** (mostly source code) and lets many people **work on the same project safely**.

It remembers **who changed what, when and why**, and lets us **go back to any old version**.

#### 🏠 Simple Example

```text
📄 Without Git                  📚 With Git
project_final.docx              One project folder
project_final_v2.docx           + complete history of every change
project_final_v2_REAL.docx      + easy undo, easy teamwork
```

#### 📦 Git Is Used To

- 💾 Save versions of code (history)
- ⏪ Go back to an older version
- 🌿 Work on features in separate **branches**
- 🤝 Work together with a team
- 🔍 Find who changed a line and why

#### 🧠 Easy Memory

> **Git = Time machine for our code**

---

## 2.2 🐙 What is GitHub?

> **GitHub = Online platform to host Git repositories**

GitHub is a **website (cloud service)** where we store our Git repositories, share code and collaborate with others.

#### ⚖️ Git vs GitHub

| 🔗 Git                              | 🐙 GitHub                                   |
| ----------------------------------- | ------------------------------------------- |
| A **tool** (software)               | A **service** (website)                     |
| Installed on our computer           | Runs in the cloud                           |
| Tracks changes locally              | Stores repositories online                  |
| Works **without** internet          | Needs internet                              |
| Command line (`git ...`)            | Web interface, Pull Requests, Issues, Actions|

#### 🧠 Easy Memory

```text
🔗 Git    = The tool that tracks changes
🐙 GitHub = The online home for Git repositories
```

#### 🌍 Similar Platforms

- 🦊 GitLab
- 🪣 Bitbucket
- ☁️ AWS CodeCommit (service closed to new customers — check AWS announcements)

---

## 2.3 🤔 Why Do We Use Git?

### ❌ Without Version Control

```text
👥 Two developers edit the same file
        ↓
💥 One overwrites the other's work
        ↓
😵 No history, no undo
```

### ✅ With Git

```text
🌿 Each developer works on a branch
        ↓
🔀 Changes are merged safely
        ↓
📜 Full history, easy rollback
```

#### ⭐ Main Reasons

- 📜 Complete **history** of changes
- ⏪ Easy **rollback**
- 🌿 **Branching** for safe experiments
- 🤝 **Teamwork** without overwriting each other
- 🌍 **Distributed** — every developer has a full copy
- 🤖 Triggers **CI/CD** pipelines (Jenkins, GitHub Actions)

---

## 2.4 🧰 Types of Version Control Systems

```text
🧰 Version Control Systems
│
├── 📁 Local VCS         → History stored on one computer only
├── 🏢 Centralized VCS   → One central server (SVN)
└── 🌍 Distributed VCS   → Every user has the full history (Git)
```

| Type              | Example     | Problem / Benefit                                      |
| ----------------- | ----------- | ------------------------------------------------------ |
| 📁 Local          | RCS         | No teamwork                                            |
| 🏢 Centralized    | SVN, CVS    | If the server fails, history can be lost; needs network|
| 🌍 Distributed    | **Git**     | Full copy everywhere, works offline, very fast         |

---

## 2.5 🧱 Git Basic Concepts

```text
🔗 Git Structure
│
├── 📁 Repository (repo)  → Project folder tracked by Git
├── 📝 Commit             → A saved snapshot of changes
├── 🌿 Branch             → A separate line of work
├── 📍 HEAD               → Pointer to the current commit/branch
├── 🌐 Remote             → Repository on a server (like GitHub)
└── 🏷️ Tag                → A named label on a commit (like v1.0)
```

### 2.5.1 📖 Simple Definitions

| Concept            | Simple Meaning                                                  |
| ------------------ | --------------------------------------------------------------- |
| 📁 Repository      | A project folder that Git tracks (has a hidden `.git` folder)   |
| 📝 Commit          | A saved snapshot with a message, author and unique ID (hash)    |
| 🌿 Branch          | A separate line of development (like a copy to work safely)     |
| 📍 HEAD            | Points to where we are now (current branch / commit)            |
| 🌐 Remote          | A copy of the repository on a server (name is usually `origin`) |
| 🏷️ Tag             | A fixed label for a release (v1.0, v2.0)                        |
| 🔑 Commit Hash     | Unique ID of a commit (like `a1b2c3d`)                          |

### 2.5.2 🏛️ The Three Areas of Git

```text
💻 Working Directory      →      🎭 Staging Area (Index)      →      🗄️ Local Repository
(files we edit)       git add     (files ready to commit)    git commit   (saved history)
                                                                              │
                                                                              │ git push
                                                                              ▼
                                                                    🌐 Remote Repository (GitHub)
```

| Area                    | Meaning                                         |
| ----------------------- | ----------------------------------------------- |
| 💻 Working Directory    | Our actual files where we make changes          |
| 🎭 Staging Area         | Files we selected to include in the next commit |
| 🗄️ Local Repository     | The `.git` database with all commits            |
| 🌐 Remote Repository    | The copy on GitHub                              |

#### 🧠 Remember

> **Edit → Add (stage) → Commit → Push**

### 2.5.3 🔄 File States

```text
🔄 File Lifecycle
│
├── ❓ Untracked   → New file, Git does not know it
├── ✏️ Modified    → Tracked file changed
├── 🎭 Staged      → Marked for the next commit
└── ✅ Committed   → Safely saved in the repository
```

---

## 2.6 ⚙️ Installing and Configuring Git

### 2.6.1 📥 Install

```bash
# Ubuntu / Debian
sudo apt update
sudo apt install git -y

# Amazon Linux / RHEL
sudo yum install git -y

# Check the version
git --version
```

(On Windows: install **Git for Windows**. On macOS: `brew install git`.)

### 2.6.2 🪪 First-Time Setup

```bash
git config --global user.name  "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
git config --global core.editor "nano"

# See all settings
git config --list
```

#### 🧱 Config Levels

| Level        | Flag         | Applies To                    |
| ------------ | ------------ | ----------------------------- |
| 🖥️ System    | `--system`   | All users on the computer     |
| 👤 Global    | `--global`   | Current user (all repos)      |
| 📁 Local     | `--local`    | Only the current repository   |

---

## 2.7 🚀 Basic Git Workflow and Commands

### 2.7.1 🆕 Start a Repository

```bash
# Create a new repository in the current folder
git init

# OR copy an existing repository
git clone https://github.com/user/project.git
```

### 2.7.2 📋 Check and Stage Changes

```bash
git status                 # What changed?
git add file.txt           # Stage one file
git add .                  # Stage all changes in the folder
git add -p                 # Choose parts of files to stage
```

### 2.7.3 📝 Commit

```bash
git commit -m "Add login page"          # Commit staged changes
git commit -am "Fix typo"               # Stage tracked files + commit
git commit --amend -m "Better message"  # Change the last commit
```

#### 💡 Good Commit Message

```text
✅ "Add user login validation"
✅ "Fix null error in payment service"
❌ "update"
❌ "changes"
```

### 2.7.4 📜 See History

```bash
git log                    # Full history
git log --oneline          # One line per commit
git log --oneline --graph --all   # Branch graph
git show <commit-hash>     # Details of one commit
git diff                   # Unstaged changes
git diff --staged          # Staged changes
git blame file.txt         # Who changed each line
```

### 2.7.5 🔁 The Daily Flow

```text
1. ✏️ Edit files
2. 📋 git status
3. ➕ git add .
4. 📝 git commit -m "message"
5. ⬆️ git push
```

---

## 2.8 🌿 Branching

A **branch** lets us work on a feature or fix **without touching the main code**.

```text
main     ●────●────●────────────●────●
                    \          /
feature              ●────●────●
```

### 2.8.1 ⌨️ Branch Commands

```bash
git branch                     # List local branches
git branch feature-login       # Create a branch
git switch feature-login       # Move to a branch
git switch -c feature-login    # Create + move (new way)
git checkout -b feature-login  # Create + move (old way)
git branch -d feature-login    # Delete a merged branch
git branch -D feature-login    # Force delete
git branch -a                  # List local + remote branches
```

### 2.8.2 🔀 Merging

**Merge** joins the changes of one branch into another.

```bash
git switch main
git merge feature-login
```

#### 🧩 Types of Merge

```text
🔀 Merge Types
│
├── ⏩ Fast-Forward   → main had no new commits; pointer just moves forward
└── 🔀 Three-Way Merge → Both branches changed; Git creates a merge commit
```

```text
⏩ Fast-Forward
main:    A──B
feature:      └──C──D        →   main:  A──B──C──D

🔀 Three-Way
main:    A──B──────E
              \     \
feature:       C──D──M       (M = merge commit)
```

### 2.8.3 💥 Merge Conflict

A **conflict** happens when **two branches change the same line** and Git cannot decide which one to keep.

```text
<<<<<<< HEAD
Hello from main
=======
Hello from feature
>>>>>>> feature-login
```

#### 🪜 How to Solve

```text
1. 📂 Open the conflicted file
2. ✂️ Keep the correct code and delete <<<<<<<, =======, >>>>>>> lines
3. ➕ git add file.txt
4. 📝 git commit   (completes the merge)
```

> `git merge --abort` cancels the merge.

### 2.8.4 🔄 Rebase

**Rebase** moves our branch commits **on top of the latest main**, giving a **straight, clean history**.

```bash
git switch feature-login
git rebase main
```

```text
Before:   main:    A──B──E
                    \
          feature:   C──D

After:    main:    A──B──E
                          \
          feature:         C'──D'
```

#### ⚠️ Golden Rule

> **Never rebase commits that are already pushed and shared with others.**

#### 📊 Merge vs Rebase

| 🔀 Merge                          | 🔄 Rebase                              |
| --------------------------------- | -------------------------------------- |
| Keeps full history with merge commit | Creates a straight line history     |
| Safe for shared branches          | Avoid on shared/public branches        |
| Easy to understand                | Cleaner history                        |

---

## 2.9 🌐 Working with Remote Repositories

```bash
git remote -v                                   # Show remotes
git remote add origin https://github.com/user/project.git
git push -u origin main                         # First push (set upstream)
git push                                        # Later pushes
git pull                                        # Fetch + merge
git fetch                                       # Download only (no merge)
git push origin feature-login                   # Push a branch
git push origin --delete feature-login          # Delete remote branch
```

### 2.9.1 ⚖️ fetch vs pull

| 📥 git fetch                         | ⬇️ git pull                                |
| ------------------------------------ | ------------------------------------------ |
| Downloads new data only              | Downloads **and merges** into our branch   |
| Does not change our files            | Changes our working files                  |
| Safe to check changes first          | Can cause conflicts immediately            |

> `git pull` = `git fetch` + `git merge`

### 2.9.2 🔑 Authentication with GitHub

```text
🔑 GitHub Authentication
│
├── 🔐 SSH Key                     → Recommended for daily use
└── 🎫 Personal Access Token (PAT) → Used instead of a password for HTTPS
```

#### 🔐 Setup SSH Key

```bash
ssh-keygen -t ed25519 -C "you@example.com"
cat ~/.ssh/id_ed25519.pub        # Copy this public key
# GitHub → Settings → SSH and GPG keys → New SSH key → Paste

ssh -T git@github.com            # Test the connection
git remote set-url origin git@github.com:user/project.git
```

#### ⚠️ Important

> **GitHub no longer accepts account passwords for Git over HTTPS.** Use a **Personal Access Token** or **SSH**.

> **Never share or commit your private key or tokens.**

---

## 2.10 ⏪ Undoing Changes

```text
⏪ Undo Options
│
├── ✏️ Discard changes in a file     → git restore
├── 🎭 Unstage a file                → git restore --staged
├── 🔄 Move back in history          → git reset
└── ↩️ Create an "opposite" commit   → git revert
```

### 2.10.1 🧰 Commands

```bash
git restore file.txt                 # Discard unsaved changes in a file
git restore --staged file.txt        # Remove file from staging area

git reset --soft  HEAD~1             # Undo last commit, keep changes STAGED
git reset --mixed HEAD~1             # Undo last commit, keep changes UNSTAGED (default)
git reset --hard  HEAD~1             # Undo last commit and DELETE changes ⚠️

git revert <commit-hash>             # New commit that cancels an older commit
```

### 2.10.2 📊 reset vs revert

| ⏪ git reset                          | ↩️ git revert                              |
| ------------------------------------ | ------------------------------------------ |
| Moves history backward               | Adds a new commit that undoes changes      |
| Rewrites history                     | Keeps history                              |
| Use on **local** commits             | Safe for **pushed/shared** commits         |
| `--hard` can lose work               | No data lost                               |

#### 🧠 Easy Memory

```text
reset  = Go back in time (rewrites history)
revert = Cancel a change with a new commit (keeps history)
```

---

## 2.11 💼 Other Useful Git Features

### 2.11.1 📦 Stash

**Stash** temporarily saves our **unfinished changes** so we can switch branches.

```bash
git stash                  # Save changes and clean the working folder
git stash list             # See saved stashes
git stash pop              # Bring back the latest stash (and remove it)
git stash apply            # Bring back but keep the stash
git stash drop             # Delete a stash
```

### 2.11.2 🍒 Cherry-Pick

Copy **one specific commit** from another branch.

```bash
git cherry-pick <commit-hash>
```

### 2.11.3 🏷️ Tags

Mark important points like releases.

```bash
git tag v1.0                       # Lightweight tag
git tag -a v1.0 -m "Release 1.0"   # Annotated tag
git push origin v1.0               # Push a tag
git tag                            # List tags
```

### 2.11.4 🙈 .gitignore

A file listing **files Git should NOT track**.

```text
# .gitignore example
target/
node_modules/
*.log
.env
.idea/
*.class
```

#### ⚠️ Important

> **Never commit passwords, API keys, or `.env` files.**

### 2.11.5 🪝 Git Hooks

**Hooks** are scripts that run automatically on Git events (like before a commit).

```text
.git/hooks/pre-commit   → runs before each commit (check code style)
.git/hooks/pre-push     → runs before each push (run tests)
```

---

## 2.12 🔀 Branching Strategies

```text
🔀 Common Strategies
│
├── 🌿 Feature Branch Workflow
├── 🌳 Git Flow
└── 🚀 Trunk-Based Development
```

### 2.12.1 🌿 Feature Branch Workflow

- `main` always has working code
- Each feature or fix gets its **own branch**
- Merge using a **Pull Request**

### 2.12.2 🌳 Git Flow

```text
main       ● ─────────────────── ● (release v1.0) ─────── ●
                                 ↑
release                  ● ──── ●
                        ↑
develop    ● ── ● ── ● ── ● ── ●
                \     /
feature          ● ─ ●
```

| Branch        | Purpose                              |
| ------------- | ------------------------------------ |
| `main`        | Production-ready code                |
| `develop`     | Integration of finished features     |
| `feature/*`   | New features                         |
| `release/*`   | Prepare a release                    |
| `hotfix/*`    | Urgent production fixes              |

### 2.12.3 🚀 Trunk-Based Development

- Everyone commits **small changes often** to `main` (the trunk)
- Short-lived branches
- Works well with **strong CI/CD** and feature flags

---

## 2.13 🐙 GitHub Features

```text
🐙 GitHub
│
├── 📁 Repositories       → Public / Private
├── 🍴 Fork               → Personal copy of someone else's repo
├── 🔀 Pull Request (PR)  → Ask to merge our changes
├── 🐛 Issues             → Track bugs and tasks
├── 🤖 GitHub Actions     → Built-in CI/CD
├── 🛡️ Branch Protection  → Rules for important branches
├── 🪝 Webhooks           → Notify other tools (like Jenkins)
├── 🔑 Secrets            → Store passwords/tokens for Actions
└── 📋 Projects / Wiki    → Planning and documentation
```

### 2.13.1 🔀 Pull Request (PR)

A **Pull Request** asks the team to **review and merge** our branch into another branch.

```text
1. 🌿 Create a feature branch
2. 📝 Commit and push changes
3. 🔀 Open a Pull Request (feature → main)
4. 👀 Team reviews the code and comments
5. 🤖 Automatic checks run (tests, SonarQube ...)
6. ✅ Approve and Merge
7. 🗑️ Delete the feature branch
```

#### 🔀 Merge Options on GitHub

| Option              | What It Does                                          |
| ------------------- | ----------------------------------------------------- |
| 🔀 Merge commit     | Keeps all commits + adds a merge commit               |
| 🧽 Squash and merge | Combines all PR commits into one                      |
| 🔄 Rebase and merge | Replays commits on top of the base branch             |

### 2.13.2 🍴 Fork vs Clone

| 🍴 Fork                                   | 📥 Clone                                   |
| ----------------------------------------- | ------------------------------------------ |
| Copy of a repo **on GitHub** (our account)| Copy of a repo **on our computer**         |
| Used to contribute to others' projects    | Used to work locally                       |

### 2.13.3 🛡️ Branch Protection

Rules for branches like `main`:

- ✅ Require **Pull Request reviews**
- ✅ Require **status checks to pass** (CI tests)
- 🚫 Block **force pushes**
- 🚫 Prevent **branch deletion**

### 2.13.4 🪝 Webhooks (GitHub → Jenkins)

```text
👨‍💻 git push
      ↓
🐙 GitHub
      ↓ (sends HTTP POST event)
🤖 Jenkins  → starts the pipeline automatically
```

### 2.13.5 🤖 GitHub Actions (Simple Example)

GitHub Actions runs workflows defined in `.github/workflows/*.yml`.

```yaml
name: CI

on:
  push:
    branches: [ main ]
  pull_request:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up Java
        uses: actions/setup-java@v4
        with:
          distribution: temurin
          java-version: '17'

      - name: Build with Maven
        run: mvn -B clean package
```

#### 📖 Understanding It

```text
on        → What triggers the workflow (push, pull request)
jobs      → Groups of steps
runs-on   → The machine type
steps     → Actions or commands to run
secrets   → Stored in GitHub: ${{ secrets.MY_TOKEN }}
```

---

## 2.14 🏆 Git Best Practices

```text
✅ Git Best Practices
│
├── 📝 Write clear commit messages
├── 🔁 Commit small and often
├── 🌿 Use branches for features and fixes
├── 🔀 Use Pull Requests and code reviews
├── 🔄 Pull latest changes before pushing
├── 🙈 Use .gitignore
├── 🔐 Never commit secrets
└── 🛡️ Protect the main branch
```

---

## 2.15 ⌨️ Git Commands Cheat Sheet

| Task                         | Command                                  |
| ---------------------------- | ---------------------------------------- |
| Create repo                  | `git init`                               |
| Copy repo                    | `git clone <url>`                        |
| Check status                 | `git status`                             |
| Stage changes                | `git add .`                              |
| Commit                       | `git commit -m "message"`                |
| View history                 | `git log --oneline`                      |
| Create + switch branch       | `git switch -c <branch>`                 |
| Merge a branch               | `git merge <branch>`                     |
| Add remote                   | `git remote add origin <url>`            |
| Push                         | `git push -u origin main`                |
| Pull                         | `git pull`                               |
| Undo staged file             | `git restore --staged <file>`            |
| Undo last commit (keep work) | `git reset --soft HEAD~1`                |
| Cancel a pushed commit       | `git revert <hash>`                      |
| Save unfinished work         | `git stash`                              |
| Tag a release                | `git tag -a v1.0 -m "Release 1.0"`       |

---

## 2.16 🏗️ Real Example: Feature to Pull Request

### 🎯 Requirement

Add a new feature to a project and merge it safely into `main`.

### 🪜 Steps

```bash
# 1. Get the project
git clone git@github.com:team/shop-app.git
cd shop-app

# 2. Create a feature branch
git switch -c feature/add-cart

# 3. Make changes, then save them
git add .
git commit -m "Add shopping cart feature"

# 4. Push the branch
git push -u origin feature/add-cart
```

```text
5. 🐙 On GitHub → Open a Pull Request (feature/add-cart → main)
6. 🤖 Jenkins / GitHub Actions run build and tests automatically
7. 👀 Teammates review and approve
8. ✅ Merge the Pull Request
```

```bash
# 9. Update local main
git switch main
git pull
git branch -d feature/add-cart
```

### 🏗️ Flow Diagram

```text
👨‍💻 Developer
   │ git push (feature branch)
   ▼
🐙 GitHub ──► 🔀 Pull Request ──► 🤖 CI checks ──► 👀 Review ──► ✅ Merge to main
                                                                       │
                                                                       ▼ webhook
                                                                  🤖 Jenkins pipeline
```

---

## 📌🧠 Git & GitHub Quick Revision

```text
🔗 Git & GitHub
│
├── 🧱 Git Basics
│   ├── Repository, Commit, Branch, HEAD
│   ├── Working Directory → Staging → Repository
│   └── Remote (origin)
│
├── 🚀 Daily Commands
│   ├── init / clone
│   ├── status / add / commit
│   └── log / diff / push / pull
│
├── 🌿 Branching
│   ├── switch / merge
│   ├── Fast-forward vs Three-way
│   ├── Conflicts
│   └── Rebase
│
├── ⏪ Undo
│   ├── restore
│   ├── reset (soft / mixed / hard)
│   └── revert
│
├── 💼 Extras
│   ├── stash, cherry-pick
│   ├── tags, .gitignore
│   └── hooks
│
├── 🔀 Strategies
│   ├── Feature Branch
│   ├── Git Flow
│   └── Trunk-Based
│
└── 🐙 GitHub
    ├── Fork, Pull Request, Issues
    ├── Branch Protection
    ├── Webhooks
    └── GitHub Actions
```

---

## 🧠⚡ Git & GitHub One-Line Memory

| Concept                 | Easy Memory                                         |
| ----------------------- | --------------------------------------------------- |
| 🔗 **Git**              | Tool That Tracks Code Changes                       |
| 🐙 **GitHub**           | Online Home for Git Repositories                    |
| 📁 **Repository**       | Project Folder Tracked by Git                       |
| 📝 **Commit**           | Saved Snapshot of Changes                           |
| 🌿 **Branch**           | Separate Line of Work                               |
| 📍 **HEAD**             | Where We Are Now                                    |
| 🎭 **Staging Area**     | Files Ready for the Next Commit                     |
| 🌐 **Remote / origin**  | Repository on a Server                              |
| 🔀 **Merge**            | Join Branches (Keeps History)                       |
| 🔄 **Rebase**           | Move Commits on Top (Straight History)              |
| 💥 **Conflict**         | Same Line Changed in Two Branches                   |
| ⏪ **reset**            | Go Back in Time (Rewrites History)                  |
| ↩️ **revert**           | Cancel a Change With a New Commit                   |
| 📦 **stash**            | Temporarily Save Unfinished Work                    |
| 🍒 **cherry-pick**      | Copy One Commit to Another Branch                   |
| 🏷️ **tag**              | Label for a Release                                 |
| 🙈 **.gitignore**       | Files Git Should Not Track                          |
| 🔀 **Pull Request**     | Request to Review and Merge                         |
| 🍴 **Fork**             | Our Own Copy of Someone's Repo on GitHub            |
| 🪝 **Webhook**          | GitHub Notifies Jenkins After a Push                |

---

## 🗺️ Git & GitHub Learning Map

```text
                       🔗 Git & GitHub
                              │
      ┌───────────────────────┼───────────────────────┐
      │                       │                       │
      ▼                       ▼                       ▼
   LOCAL GIT               BRANCHING               REMOTE / GITHUB
      │                       │                       │
      ├── init / clone        ├── branch / switch     ├── remote / push / pull
      ├── add / commit        ├── merge / rebase      ├── SSH / PAT
      ├── log / diff          ├── conflicts           ├── Pull Requests
      └── restore / reset     └── strategies          ├── Branch Protection
          / revert                 ├── Feature        ├── Webhooks
                                   ├── Git Flow       └── GitHub Actions
      │                            └── Trunk-based
      ▼
   EXTRAS
      │
      ├── stash
      ├── cherry-pick
      ├── tags
      └── .gitignore / hooks
```

---

## ⭐ Git & GitHub Final Memory

```text
Git & GitHub
 │
 ├── What is Git?
 │      └── Version control tool
 │
 ├── What is GitHub?
 │      └── Online platform for Git repositories
 │
 ├── Save changes locally?
 │      └── git add → git commit
 │
 ├── Share changes?
 │      └── git push
 │
 ├── Work safely on a feature?
 │      └── Create a branch
 │
 ├── Join branches?
 │      └── merge (or rebase)
 │
 ├── Undo a pushed commit safely?
 │      └── git revert
 │
 ├── Review before merging?
 │      └── Pull Request
 │
 └── Start Jenkins automatically on push?
        └── Webhook
```

---

# 🔨 PART 3 — Maven — Build Tool

> **Maven = One command to build, test and package a Java project**

---

## 3.1 🔨 What is Maven?

> **Maven = Build automation and dependency management tool (mainly for Java)**

Apache Maven is a tool that **builds, tests and packages Java projects automatically**, and **downloads the libraries (dependencies) the project needs**.

All project information is written in one file called **`pom.xml`**.

#### 📦 Maven Is Used To

- 🔨 **Compile** source code
- 🧪 **Run tests**
- 📦 **Package** the project (`.jar`, `.war`)
- 📥 **Download dependencies** automatically
- 📤 **Upload artifacts** to a repository (Nexus)
- 🔍 Work with **SonarQube** and **Jenkins**

#### 🏗️ Maven Basic Idea

```text
📄 pom.xml (what we want)
        │
        ▼
🔨 Maven
        │
        ├── 📥 Downloads dependencies
        ├── 🔨 Compiles code
        ├── 🧪 Runs tests
        └── 📦 Creates app.jar / app.war
```

#### 🧠 Easy Memory

> **Maven = One command to build, test and package a Java project**

---

## 3.2 🤔 Why Do We Use Maven?

### ❌ Without Maven

```text
📥 Download each .jar library manually
        ↓
📂 Copy jars into the project
        ↓
⚙️ Write long javac and jar commands
        ↓
🐛 Different developers have different library versions
```

### ✅ With Maven

```text
📄 Write dependencies in pom.xml
        ↓
⌨️ Run:  mvn clean package
        ↓
✅ Maven downloads libraries, builds, tests and packages the project
```

#### ⭐ Main Reasons

- 📥 **Automatic dependency management** (and their sub-dependencies)
- 📂 **Standard project structure** — every Maven project looks the same
- 🔁 **Same build** on every computer and on Jenkins
- 🔌 **Plugins** for many tasks
- 📦 Easy sharing of artifacts through repositories

---

## 3.3 🧰 What Does Maven Provide?

Maven provides:

- 📄 POM (Project Object Model)
- 📂 Standard Directory Layout
- 🔄 Build Lifecycles and Phases
- 🔌 Plugins and Goals
- 📥 Dependency Management
- 🗄️ Repositories (Local, Central, Remote)
- 🧩 Multi-Module Projects
- 🎭 Profiles
- 🧬 Archetypes (project templates)

---

## 3.4 ⚙️ Installing Maven

Maven needs **Java (JDK)** installed first.

```bash
# Check Java
java -version

# Install on Ubuntu / Debian
sudo apt update
sudo apt install openjdk-17-jdk maven -y

# Install on Amazon Linux / RHEL
sudo yum install java-17-amazon-corretto-devel maven -y

# Check Maven
mvn -version
```

#### 🧱 Important Environment Variables

| Variable      | Meaning                                      |
| ------------- | -------------------------------------------- |
| `JAVA_HOME`   | Path of the JDK                              |
| `M2_HOME` / `MAVEN_HOME` | Path of Maven (if installed manually) |
| `PATH`        | Must include `maven/bin`                     |

#### 💡 Maven Wrapper (`mvnw`)

Many projects include **`mvnw`** (Maven Wrapper). It **downloads the right Maven version automatically**, so we do not need Maven installed.

```bash
./mvnw clean package
```

---

## 3.5 📂 Standard Directory Layout

```text
📁 my-app/
├── 📄 pom.xml
├── 📁 src/
│   ├── 📁 main/
│   │   ├── 📁 java/          → Application source code
│   │   ├── 📁 resources/     → Config files (application.properties)
│   │   └── 📁 webapp/        → Web files (for WAR projects)
│   └── 📁 test/
│       ├── 📁 java/          → Test code
│       └── 📁 resources/     → Test config files
└── 📁 target/                → Output (created by Maven: classes, jar, war)
```

#### 🧠 Remember

> **`src/main` = application code. `src/test` = test code. `target` = build output.**

---

## 3.6 📄 POM (Project Object Model)

The **`pom.xml`** file is the **heart of a Maven project**. It describes the project, its dependencies and how to build it.

#### 💻 Simple pom.xml

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">

  <modelVersion>4.0.0</modelVersion>

  <!-- Project coordinates -->
  <groupId>com.example</groupId>
  <artifactId>my-app</artifactId>
  <version>1.0.0-SNAPSHOT</version>
  <packaging>jar</packaging>

  <name>My App</name>

  <properties>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
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

### 3.6.1 🔑 Maven Coordinates (GAV)

Every project and dependency is identified by **three values**:

```text
🔑 Maven Coordinates
│
├── 🏢 groupId     → Organization / group (com.example)
├── 📦 artifactId  → Project / library name (my-app)
└── 🔢 version     → Version (1.0.0)
```

#### 🧠 Easy Memory

```text
groupId    = Company name
artifactId = Project name
version    = Which version
(Together: GAV)
```

### 3.6.2 🧱 Main POM Elements

| Element               | Meaning                                                      |
| --------------------- | ------------------------------------------------------------ |
| `modelVersion`        | POM model version (always `4.0.0`)                           |
| `groupId`             | Group or organization                                        |
| `artifactId`          | Project name                                                 |
| `version`             | Project version                                              |
| `packaging`           | Output type: `jar`, `war`, `pom`, `ear` (default `jar`)      |
| `properties`          | Variables and settings used in the POM                       |
| `dependencies`        | Libraries the project needs                                  |
| `dependencyManagement`| Central place to control dependency versions                |
| `build`               | Plugins and build settings                                   |
| `parent`              | Inherit settings from another POM                            |
| `modules`             | List of sub-projects (multi-module)                          |
| `profiles`            | Environment-specific settings                                |
| `distributionManagement` | Where to deploy artifacts (Nexus)                         |
| `repositories`        | Extra repositories to download from                          |

### 3.6.3 📦 Packaging Types

| Packaging | Output           | Used For                         |
| --------- | ---------------- | -------------------------------- |
| `jar`     | `.jar` file      | Libraries, Spring Boot apps      |
| `war`     | `.war` file      | Web apps for Tomcat              |
| `pom`     | Only a POM       | Parent / multi-module projects   |
| `ear`     | `.ear` file      | Enterprise applications          |

### 3.6.4 🔢 SNAPSHOT vs Release Version

```text
1.0.0-SNAPSHOT  → Development version (can change, keeps updating)
1.0.0           → Release version (fixed, never changes)
```

| 🚧 SNAPSHOT                          | ✅ Release                               |
| ------------------------------------ | ---------------------------------------- |
| Under development                    | Final and stable                         |
| Can be overwritten                   | Cannot be changed once published         |
| Stored in **snapshot** repository    | Stored in **release** repository         |

---

## 3.7 🗄️ Maven Repositories

A **repository** is a place where Maven stores and finds artifacts (jars, poms).

```text
🗄️ Maven Repositories
│
├── 💻 Local Repository   → ~/.m2/repository (on our computer)
├── 🌍 Central Repository → https://repo.maven.apache.org (public, by Apache)
└── 🏢 Remote Repository  → Company repository like Nexus
```

#### 🔍 How Maven Finds a Dependency

```text
1. 💻 Check Local Repository (~/.m2/repository)
          ↓ (not found)
2. 🏢 Check Remote Repository (Nexus / mirror)
          ↓ (not found)
3. 🌍 Check Maven Central
          ↓
4. 📥 Download and save in the Local Repository
```

#### 🧠 Simple Meaning

> **Local = our computer. Central = public library. Remote = company library (Nexus).**

---

## 3.8 📥 Dependency Management

A **dependency** is a **library** our project needs.

```xml
<dependencies>
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
    <version>3.2.0</version>
  </dependency>
</dependencies>
```

Maven downloads this library **and all the libraries it needs** (transitive dependencies).

### 3.8.1 🔗 Transitive Dependencies

```text
📦 Our Project
   └── depends on  🅰️ Library A
                      └── depends on  🅱️ Library B   (Maven downloads this too!)
```

### 3.8.2 🎯 Dependency Scopes

**Scope** decides **when** a dependency is available.

| Scope        | Compile | Test | Runtime | In Final Package? | Example                    |
| ------------ | :-----: | :--: | :-----: | :---------------: | -------------------------- |
| `compile` (default) | ✅ | ✅ | ✅ | ✅ | Spring, Apache Commons     |
| `provided`   | ✅      | ✅   | ❌      | ❌ (server gives it) | Servlet API             |
| `runtime`    | ❌      | ✅   | ✅      | ✅                | JDBC driver                |
| `test`       | ❌      | ✅   | ❌      | ❌                | JUnit, Mockito             |
| `system`     | ✅      | ✅   | ❌      | ❌ (not recommended) | Local jar file          |
| `import`     | —       | —    | —       | —                 | Used in dependencyManagement|

#### 🧠 Easy Memory

```text
compile  = Needed everywhere (default)
test     = Only for tests (JUnit)
provided = Needed to compile, but the server provides it (Servlet API)
runtime  = Needed only when running (DB driver)
```

### 3.8.3 🛠️ Useful Dependency Commands

```bash
mvn dependency:tree        # Show all dependencies (including transitive)
mvn dependency:resolve     # Download dependencies
mvn dependency:analyze     # Find unused / undeclared dependencies
```

---

## 3.9 🔄 Maven Build Lifecycle

A **lifecycle** is an **ordered list of phases**. When we run a phase, Maven runs **all earlier phases first**.

```text
🔄 Maven Lifecycles
│
├── 🧹 Clean Lifecycle    → Remove old build output
├── 🔨 Default Lifecycle  → Build and deploy the project (most used)
└── 📚 Site Lifecycle     → Create project documentation
```

### 3.9.1 🧹 Clean Lifecycle

| Phase       | What It Does                              |
| ----------- | ----------------------------------------- |
| `pre-clean` | Before cleaning                           |
| `clean`     | **Deletes the `target/` folder**          |
| `post-clean`| After cleaning                            |

### 3.9.2 🔨 Default (Build) Lifecycle

```text
validate → compile → test → package → verify → install → deploy
```

| Phase       | What It Does                                              | Output / Result            |
| ----------- | --------------------------------------------------------- | -------------------------- |
| `validate`  | Check that the project and POM are correct                | —                          |
| `compile`   | Compile source code                                       | `target/classes`           |
| `test`      | Run unit tests                                            | Test reports               |
| `package`   | Create the `.jar` / `.war`                                | `target/my-app-1.0.jar`    |
| `verify`    | Run integration checks and quality checks                 | —                          |
| `install`   | Copy the package to the **local** repository (`~/.m2`)    | Local repo                 |
| `deploy`    | Upload the package to the **remote** repository (Nexus)   | Remote repo                |

#### 🔁 How Phases Work

```text
mvn package
   │
   └── runs:  validate → compile → test → package   (stops here)

mvn install
   │
   └── runs:  validate → compile → test → package → verify → install
```

#### 🧠 Easy Memory

```text
compile  = Make classes
test     = Run tests
package  = Make jar/war
install  = Save in LOCAL repo (~/.m2)
deploy   = Upload to REMOTE repo (Nexus)
```

---

## 3.10 🔌 Plugins and Goals

A **plugin** is a **set of tasks**. Each task inside a plugin is a **goal**.

```text
🔌 Plugin: maven-compiler-plugin
   └── 🎯 Goal: compile
   └── 🎯 Goal: testCompile
```

#### ⌨️ Run a Goal Directly

```bash
mvn compiler:compile
mvn surefire:test
mvn dependency:tree
mvn sonar:sonar
```

Format: **`mvn <plugin>:<goal>`**

### 3.10.1 🔗 Phases and Goals Together

Plugins attach their goals to lifecycle phases.

| Phase       | Default Plugin : Goal                |
| ----------- | ------------------------------------ |
| `compile`   | `maven-compiler-plugin:compile`      |
| `test`      | `maven-surefire-plugin:test`         |
| `package`   | `maven-jar-plugin:jar` (for jar)     |
| `install`   | `maven-install-plugin:install`       |
| `deploy`    | `maven-deploy-plugin:deploy`         |

### 3.10.2 🧰 Common Plugins

| Plugin                        | Purpose                                  |
| ----------------------------- | ---------------------------------------- |
| `maven-compiler-plugin`       | Compile Java code                        |
| `maven-surefire-plugin`       | Run unit tests                           |
| `maven-failsafe-plugin`       | Run integration tests                    |
| `maven-jar-plugin`            | Create JAR files                         |
| `maven-war-plugin`            | Create WAR files                         |
| `maven-deploy-plugin`         | Upload artifacts to a repository         |
| `jacoco-maven-plugin`         | Code coverage report                     |
| `sonar-maven-plugin`          | Send analysis to SonarQube               |
| `spring-boot-maven-plugin`    | Build runnable Spring Boot jar           |

#### 💻 Plugin in pom.xml

```xml
<build>
  <plugins>
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>3.11.0</version>
      <configuration>
        <source>17</source>
        <target>17</target>
      </configuration>
    </plugin>
  </plugins>
</build>
```

---

## 3.11 ⌨️ Common Maven Commands

| Command                           | What It Does                                          |
| --------------------------------- | ----------------------------------------------------- |
| `mvn clean`                       | Delete the `target/` folder                           |
| `mvn compile`                     | Compile the code                                      |
| `mvn test`                        | Compile and run tests                                 |
| `mvn package`                     | Create the jar/war                                    |
| `mvn clean package`               | Clean + build the package (**most used**)             |
| `mvn clean install`               | Build and save in the local repository                |
| `mvn deploy`                      | Upload to the remote repository                       |
| `mvn clean package -DskipTests`   | Build without **running** tests                       |
| `mvn clean package -Dmaven.test.skip=true` | Skip compiling **and** running tests         |
| `mvn -U clean package`            | Force update of SNAPSHOT dependencies                 |
| `mvn -o package`                  | Work **offline**                                      |
| `mvn -B package`                  | Batch mode (no interaction, good for Jenkins)         |
| `mvn -P prod package`             | Use the `prod` profile                                |
| `mvn dependency:tree`             | Show dependency tree                                  |
| `mvn help:effective-pom`          | Show the final POM after inheritance                  |

#### 🧠 Remember

> **`mvn clean package` = Clean old build, compile, test and create the jar/war.**

---

## 3.12 🧬 Archetypes (Project Templates)

An **archetype** creates a **ready-made project structure**.

```bash
mvn archetype:generate \
  -DgroupId=com.example \
  -DartifactId=my-app \
  -DarchetypeArtifactId=maven-archetype-quickstart \
  -DarchetypeVersion=1.4 \
  -DinteractiveMode=false
```

This creates:

```text
my-app/
├── pom.xml
└── src/
    ├── main/java/com/example/App.java
    └── test/java/com/example/AppTest.java
```

#### 🏃 Run the Built Jar

```bash
mvn clean package
java -cp target/my-app-1.0-SNAPSHOT.jar com.example.App
```

---

## 3.13 ⚙️ settings.xml

**`settings.xml`** is the **Maven configuration file** for the user or machine (not the project).

```text
📍 Locations
│
├── 🌍 Global → <maven-install>/conf/settings.xml
└── 👤 User   → ~/.m2/settings.xml  (overrides global)
```

#### 🎯 Used For

- 🔑 **Credentials** for Nexus (servers)
- 🪞 **Mirrors** (use Nexus instead of Maven Central)
- 🌐 **Proxy** settings
- 🎭 **Profiles** and local repository path

#### 💻 Example: Nexus Credentials and Mirror

```xml
<settings>
  <servers>
    <server>
      <id>nexus-releases</id>
      <username>deployer</username>
      <password>${env.NEXUS_PASSWORD}</password>
    </server>
    <server>
      <id>nexus-snapshots</id>
      <username>deployer</username>
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

#### ⚠️ Important

> The **server `id`** in `settings.xml` must **match** the `id` in the POM `distributionManagement`.

> **Never store plain passwords in files in Git.** Use environment variables or Jenkins credentials.

---

## 3.14 📤 Deploying to Nexus

Add **`distributionManagement`** to the POM.

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

#### 🚀 Deploy

```bash
mvn clean deploy
```

```text
🔨 mvn deploy
      │
      ├── Version ends with -SNAPSHOT → 📤 Goes to nexus-snapshots
      └── Normal version (1.0.0)      → 📤 Goes to nexus-releases
```

---

## 3.15 🧩 Multi-Module Projects

A **big project** can be split into **modules**. A **parent POM** controls them.

```text
📁 shop-app/                 ← Parent POM (packaging = pom)
├── 📄 pom.xml
├── 📁 shop-common/          ← Module 1 (shared code)
│   └── pom.xml
├── 📁 shop-service/         ← Module 2 (business logic)
│   └── pom.xml
└── 📁 shop-web/             ← Module 3 (web layer)
    └── pom.xml
```

#### 💻 Parent POM

```xml
<groupId>com.example</groupId>
<artifactId>shop-app</artifactId>
<version>1.0.0</version>
<packaging>pom</packaging>

<modules>
  <module>shop-common</module>
  <module>shop-service</module>
  <module>shop-web</module>
</modules>
```

```bash
mvn clean install        # Builds all modules in the correct order
```

---

## 3.16 🎭 Profiles

A **profile** changes build settings **for different environments** (dev, test, prod).

```xml
<profiles>
  <profile>
    <id>dev</id>
    <properties>
      <env>development</env>
    </properties>
  </profile>
  <profile>
    <id>prod</id>
    <properties>
      <env>production</env>
    </properties>
  </profile>
</profiles>
```

```bash
mvn clean package -P prod
```

---

## 3.17 🆚 Maven vs Gradle vs Ant

| Feature          | 🔨 Maven                      | 🐘 Gradle                       | 🐜 Ant                        |
| ---------------- | ----------------------------- | ------------------------------- | ----------------------------- |
| Config file      | `pom.xml` (XML)               | `build.gradle` (Groovy/Kotlin)  | `build.xml` (XML)             |
| Approach         | Convention over configuration | Flexible, script-based          | Fully manual tasks            |
| Dependency mgmt  | ✅ Built-in                   | ✅ Built-in                     | ❌ Needs Ivy                  |
| Speed            | Good                          | Faster (incremental, cache)     | Depends on script             |
| Learning curve   | Easy                          | Medium                          | Easy but long scripts         |
| Popular in       | Enterprise Java, Jenkins      | Android, modern projects        | Older projects                |

#### 🧠 Easy Memory

```text
🔨 Maven  = Standard rules, XML, easy
🐘 Gradle = Flexible, fast
🐜 Ant    = Old, manual
```

---

## 3.18 🔗 Maven in a CI/CD Pipeline

```text
🐙 GitHub
    ↓
🤖 Jenkins
    ├── mvn clean package          → Build + unit tests
    ├── mvn sonar:sonar            → Send code analysis to SonarQube
    └── mvn deploy                 → Upload the artifact to Nexus
```

#### 💻 Jenkins Pipeline Stage Example

```groovy
stage('Build') {
    steps {
        sh 'mvn -B clean package'
    }
}
```

---

## 3.19 🏗️ Real Example: Build a Java Project

### 🎯 Requirement

Create a simple Java project, build it and upload the result to Nexus.

### 🪜 Steps

```bash
# 1. Generate a project
mvn archetype:generate -DgroupId=com.example -DartifactId=hello-app \
    -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
cd hello-app

# 2. Build and test
mvn clean package

# 3. Run the jar
java -cp target/hello-app-1.0-SNAPSHOT.jar com.example.App

# 4. Install to local repository
mvn install

# 5. (After adding distributionManagement and settings.xml) Upload to Nexus
mvn deploy
```

### 🏗️ What Happens

```text
💻 Source code (src/main/java)
        │ mvn compile
        ▼
📁 target/classes
        │ mvn test
        ▼
🧪 Test reports
        │ mvn package
        ▼
📦 target/hello-app-1.0-SNAPSHOT.jar
        │ mvn install            │ mvn deploy
        ▼                        ▼
💻 ~/.m2/repository         🏢 Nexus Repository
```

---

## 📌🧠 Maven Quick Revision

```text
🔨 Maven
│
├── 📄 POM (pom.xml)
│   ├── GAV: groupId, artifactId, version
│   ├── packaging: jar / war / pom
│   ├── dependencies, properties
│   └── build, plugins, profiles
│
├── 📂 Directory Layout
│   ├── src/main, src/test
│   └── target
│
├── 🗄️ Repositories
│   ├── Local (~/.m2)
│   ├── Central
│   └── Remote (Nexus)
│
├── 🔄 Lifecycles
│   ├── clean
│   ├── default: validate → compile → test → package → verify → install → deploy
│   └── site
│
├── 🔌 Plugins and Goals
│
├── 📥 Dependencies
│   ├── Transitive
│   └── Scopes: compile, test, provided, runtime
│
└── ⚙️ Config
    ├── settings.xml (credentials, mirrors)
    ├── Profiles
    └── Multi-module projects
```

---

## 🧠⚡ Maven One-Line Memory

| Concept                    | Easy Memory                                        |
| -------------------------- | -------------------------------------------------- |
| 🔨 **Maven**               | Build and Dependency Tool for Java                 |
| 📄 **pom.xml**             | Project Configuration File                         |
| 🔑 **GAV**                 | groupId + artifactId + version                     |
| 📦 **Packaging**           | jar, war, pom, ear                                 |
| 🗄️ **Local Repo**          | ~/.m2/repository on Our Computer                   |
| 🌍 **Maven Central**       | Public Online Repository                           |
| 🏢 **Remote Repo**         | Company Repository (Nexus)                         |
| 📥 **Dependency**          | A Library Our Project Needs                        |
| 🔗 **Transitive**          | Dependencies of Dependencies                       |
| 🎯 **Scope**               | When a Dependency Is Available                     |
| 🔄 **Lifecycle**           | Ordered List of Phases                             |
| 🔌 **Plugin / Goal**       | Task Performed by Maven                            |
| 🧹 **clean**               | Delete target Folder                               |
| 📦 **package**             | Create jar/war                                     |
| 💻 **install**             | Save in Local Repository                           |
| 🚀 **deploy**              | Upload to Remote Repository                        |
| 🚧 **SNAPSHOT**            | Development Version That Can Change                |
| ⚙️ **settings.xml**        | User Config: Credentials, Mirrors                  |
| 🎭 **Profile**             | Settings for an Environment                        |

---

## 🗺️ Maven Learning Map

```text
                           🔨 Maven
                              │
      ┌───────────────────────┼───────────────────────┐
      │                       │                       │
      ▼                       ▼                       ▼
   PROJECT                  BUILD                  REPOSITORIES
      │                       │                       │
      ├── pom.xml             ├── Lifecycles          ├── Local
      ├── GAV                 │    ├── clean          ├── Central
      ├── Dependencies        │    ├── default        └── Remote (Nexus)
      │    └── Scopes         │    └── site                ├── Releases
      ├── Properties          ├── Phases                   └── Snapshots
      └── Packaging           └── Plugins / Goals
      │
      ▼
   ADVANCED
      │
      ├── Multi-module
      ├── Profiles
      ├── settings.xml
      └── Archetypes
      │
      ▼
   INTEGRATION
      │
      ├── Jenkins (mvn clean package)
      ├── SonarQube (mvn sonar:sonar)
      └── Nexus (mvn deploy)
```

---

## ⭐ Maven Final Memory

```text
Maven
 │
 ├── What is it?
 │      └── Build and dependency management tool for Java
 │
 ├── Which file controls everything?
 │      └── pom.xml
 │
 ├── How is a project identified?
 │      └── GAV (groupId, artifactId, version)
 │
 ├── Most used command?
 │      └── mvn clean package
 │
 ├── Where are libraries stored locally?
 │      └── ~/.m2/repository
 │
 ├── Difference between install and deploy?
 │      └── install = local repo, deploy = remote repo (Nexus)
 │
 ├── Where are Nexus credentials kept?
 │      └── settings.xml (server id must match POM)
 │
 └── Skip tests?
        └── -DskipTests
```

---

# 🤖 PART 4 — Jenkins — CI/CD Automation Server

> **Jenkins = Automation server that runs our build and deploy steps automatically**

---

## 4.1 🤖 What is Jenkins?

> **Jenkins = Open-source automation server for CI/CD**

Jenkins is a tool that **automatically builds, tests and deploys our applications** whenever the code changes.

It is the **"robot" of a DevOps team** — it runs the steps (checkout, build, test, scan, deploy) **one after another without human work**.

#### 📦 Jenkins Is Used To

- 🔨 **Build** projects (Maven, Gradle, npm ...)
- 🧪 **Run tests** automatically
- 🔍 Trigger **code quality checks** (SonarQube)
- 📦 **Upload artifacts** (Nexus)
- 🐳 **Build Docker images**
- 🚀 **Deploy** to servers or Kubernetes
- ⏰ Run **scheduled jobs**

#### 🏗️ Jenkins Basic Idea

```text
👨‍💻 Developer pushes code
        │
        ▼
🐙 GitHub ── webhook ──► 🤖 Jenkins
                              │
                              ├── 🔨 Build
                              ├── 🧪 Test
                              ├── 🔍 Scan
                              ├── 📦 Package
                              └── 🚀 Deploy
```

#### 🧠 Easy Memory

> **Jenkins = Automation server that runs our build and deploy steps automatically**

---

## 4.2 🤔 Why Do We Use Jenkins?

### ❌ Without Jenkins (Manual)

```text
👨‍💻 Developer finishes code
        ↓
🖐️ Someone builds manually on a laptop
        ↓
🖐️ Someone copies the file to a server
        ↓
🐛 Mistakes, delays, "works on my machine"
```

### ✅ With Jenkins (Automatic)

```text
👨‍💻 git push
        ↓
🤖 Jenkins runs the pipeline automatically
        ↓
✅ Same steps every time, fast feedback
```

#### ⭐ Main Reasons

- 🤖 **Automation** of repeated work
- ⚡ **Fast feedback** — we know quickly if a change breaks the build
- 🔁 **Same process** every time
- 🔌 **1800+ plugins** to connect with almost any tool
- 🆓 **Free and open source**
- 🌍 Large community
- 🧩 Works on Windows, Linux and macOS

---

## 4.3 🧰 What Does Jenkins Provide?

Jenkins provides:

- 🧱 Jobs (Freestyle, Pipeline, Multibranch)
- 📜 Pipeline as Code (`Jenkinsfile`)
- 🔌 Plugins
- 🔑 Credentials Management
- 🖥️ Distributed Builds (Agents)
- ⏰ Build Triggers (webhook, schedule, poll)
- 📊 Build Reports and History
- 👥 Users, Roles and Security
- 🔔 Notifications (email, Slack)

---

## 4.4 🏛️ Jenkins Architecture

```text
🏛️ Jenkins Architecture
│
├── 👑 Controller (earlier called Master)
│       → Manages jobs, schedules builds, shows the UI
│
└── 🖥️ Agents (earlier called Slaves / Nodes)
        → Machines that actually run the builds
            └── ⚙️ Executors (parallel build slots on each agent)
```

#### 🏗️ Distributed Build

```text
                  👑 Jenkins Controller
                          │
          ┌───────────────┼───────────────┐
          ▼               ▼               ▼
   🖥️ Agent 1        🖥️ Agent 2        🖥️ Agent 3
   (Linux, Java)    (Windows, .NET)   (Docker builds)
```

### 4.4.1 📖 Simple Definitions

| Concept          | Simple Meaning                                                     |
| ---------------- | ------------------------------------------------------------------ |
| 👑 Controller    | The main Jenkins server (UI, scheduling, configuration)            |
| 🖥️ Agent / Node  | A machine that runs build jobs for the controller                  |
| ⚙️ Executor      | One slot on a node that can run one build at a time                |
| 🏷️ Label         | A tag on an agent (like `docker`, `linux`) to choose where to run  |
| 📁 Workspace     | The folder where Jenkins checks out code and builds a job          |
| 🏠 JENKINS_HOME  | The folder where Jenkins stores all its data (`/var/lib/jenkins`)  |

#### ⚠️ Best Practice

> **Run builds on agents, not on the controller.** Keep the controller light and safe.

---

## 4.5 ⚙️ Installing Jenkins

Jenkins needs **Java**. It runs on **port 8080** by default.

#### 🐧 Install on Ubuntu / Debian

```bash
# 1. Install Java
sudo apt update
sudo apt install fontconfig openjdk-17-jre -y
java -version

# 2. Add the Jenkins repository
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/" | \
sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

# 3. Install and start Jenkins
sudo apt update
sudo apt install jenkins -y
sudo systemctl enable --now jenkins
sudo systemctl status jenkins
```

> 💡 Repository keys and supported Java versions change over time. Always check the **official Jenkins installation page** for current steps.

#### 🌐 First-Time Setup

```text
1. Open  http://<server-ip>:8080
2. Get the initial admin password:
      sudo cat /var/lib/jenkins/secrets/initialAdminPassword
3. Paste the password
4. Click "Install suggested plugins"
5. Create the first admin user
6. ✅ Jenkins dashboard is ready
```

#### 🔓 Security Group / Firewall

```text
Open port 8080 (only to trusted IPs)
```

#### 🐳 Run Jenkins in Docker

```bash
docker run -d --name jenkins \
  -p 8080:8080 -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  jenkins/jenkins:lts
```

| Port    | Use                                  |
| ------- | ------------------------------------ |
| `8080`  | Web interface                        |
| `50000` | Inbound agent connections            |

---

## 4.6 🖥️ Jenkins Dashboard and Key Areas

```text
🖥️ Jenkins Dashboard
│
├── ➕ New Item                → Create a job
├── 👥 People                  → Users
├── 📜 Build History           → Past builds
├── ⚙️ Manage Jenkins
│    ├── 🔌 Plugins            → Install / update plugins
│    ├── 🔧 Tools              → Configure JDK, Maven, Git
│    ├── 🔑 Credentials        → Store passwords, tokens, keys
│    ├── 🖥️ Nodes              → Add agents
│    ├── 🔒 Security           → Users, roles, authentication
│    └── ⚙️ System             → Global settings (SonarQube, email)
└── 👁️ Views                   → Group jobs
```

---

## 4.7 🔌 Plugins

**Plugins** add features to Jenkins.

#### 🧰 Common Plugins

| Plugin                         | Purpose                                      |
| ------------------------------ | -------------------------------------------- |
| 🔗 Git / GitHub                | Connect to Git repositories                  |
| 🔨 Maven Integration           | Build Maven projects                         |
| 📜 Pipeline                    | Pipeline as code                             |
| 🔍 SonarQube Scanner           | Send code to SonarQube                       |
| 📦 Nexus Artifact Uploader     | Upload artifacts to Nexus                    |
| 🐳 Docker / Docker Pipeline    | Build and run Docker containers              |
| ☸️ Kubernetes                  | Run agents in Kubernetes                     |
| 🔑 Credentials Binding         | Use secrets safely in pipelines              |
| 📧 Email Extension / Slack     | Notifications                                |
| 🌊 Blue Ocean                  | Modern pipeline visualization                |

#### 🪜 Install a Plugin

```text
Manage Jenkins → Plugins → Available plugins → Search → Install
```

#### ⚠️ Important

> Keep plugins **updated**, and install only plugins we need. Old plugins are a security risk.

---

## 4.8 🧱 Types of Jenkins Jobs

```text
🧱 Job Types
│
├── 🆓 Freestyle Project       → Simple, click-based configuration
├── 📜 Pipeline                → Pipeline as code (Jenkinsfile)
├── 🌿 Multibranch Pipeline    → One pipeline per Git branch automatically
├── 📁 Folder                  → Group jobs
└── 🏢 Organization Folder     → Scan a whole GitHub organization
```

| 🆓 Freestyle                      | 📜 Pipeline                              |
| --------------------------------- | ---------------------------------------- |
| Configure using the UI            | Write steps in a `Jenkinsfile`           |
| Good for simple tasks             | Good for complex CI/CD                   |
| Hard to version control           | Stored in Git (version controlled)       |
| Limited flow control              | Supports stages, parallel, conditions    |

#### 🧠 Remember

> **Modern Jenkins = Pipeline as Code (Jenkinsfile in the Git repository).**

---

## 4.9 📜 Jenkins Pipeline

A **Pipeline** is a **set of stages** that take code from **commit to deployment**.

```text
📜 Pipeline
│
├── 🔖 Stage: Checkout
├── 🔖 Stage: Build
├── 🔖 Stage: Test
├── 🔖 Stage: Analysis
├── 🔖 Stage: Package
└── 🔖 Stage: Deploy
```

### 4.9.1 📖 Pipeline Terms

| Term          | Simple Meaning                                              |
| ------------- | ----------------------------------------------------------- |
| 📜 Pipeline   | The full automated process                                  |
| 🖥️ Agent      | Where the pipeline runs                                     |
| 🔖 Stage      | A major step (Build, Test, Deploy)                          |
| 👣 Step       | One task inside a stage (`sh 'mvn package'`)                |
| 📄 Jenkinsfile| The text file that holds the pipeline code                  |

### 4.9.2 ⚖️ Declarative vs Scripted Pipeline

```text
📜 Pipeline Syntax
│
├── 📋 Declarative → Simple, structured, recommended
└── 💻 Scripted    → Groovy code, very flexible
```

| 📋 Declarative                          | 💻 Scripted                            |
| --------------------------------------- | -------------------------------------- |
| Starts with `pipeline { }`              | Starts with `node { }`                 |
| Structured and easy to read             | Free-form Groovy                       |
| Built-in `post`, `when`, `options`      | More power and complexity              |
| **Recommended for most users**          | For advanced logic                     |

### 4.9.3 📋 Declarative Pipeline Structure

```groovy
pipeline {
    agent any                       // Where to run

    tools {                         // Tools configured in Jenkins
        maven 'Maven3'
        jdk   'JDK17'
    }

    environment {                   // Environment variables
        APP_NAME = 'shop-app'
    }

    options {                       // Pipeline options
        timeout(time: 30, unit: 'MINUTES')
        buildDiscarder(logRotator(numToKeepStr: '10'))
    }

    triggers {                      // How it starts
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -B clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {                          // After the pipeline
        always  { echo 'Pipeline finished' }
        success { echo 'Build succeeded ✅' }
        failure { echo 'Build failed ❌' }
    }
}
```

### 4.9.4 🧱 Pipeline Sections Explained

| Section        | Meaning                                                          |
| -------------- | ---------------------------------------------------------------- |
| `pipeline`     | Top-level block (required)                                       |
| `agent`        | Where to run: `any`, `none`, `label 'docker'`, `docker { image }`|
| `tools`        | Use tools (Maven, JDK) set in Global Tool Configuration          |
| `environment`  | Variables and credentials                                        |
| `parameters`   | Inputs asked from the user when starting the build               |
| `triggers`     | Cron, polling, or upstream trigger                               |
| `options`      | Timeout, retry, build history rules                              |
| `stages`       | Contains all `stage` blocks (required)                           |
| `steps`        | Commands inside a stage (required)                               |
| `when`         | Run a stage only if a condition is true                          |
| `post`         | Actions after build: `always`, `success`, `failure`, `unstable`, `cleanup` |
| `input`        | Wait for manual approval                                         |
| `parallel`     | Run stages together                                              |

### 4.9.5 ❓ `when` Example

```groovy
stage('Deploy to Prod') {
    when { branch 'main' }
    steps {
        sh './deploy.sh'
    }
}
```

### 4.9.6 ✋ Manual Approval

```groovy
stage('Approval') {
    steps {
        input message: 'Deploy to production?', ok: 'Deploy'
    }
}
```

### 4.9.7 ⚡ Parallel Stages

```groovy
stage('Tests') {
    parallel {
        stage('Unit Tests')        { steps { sh 'mvn test' } }
        stage('Integration Tests') { steps { sh 'mvn verify' } }
    }
}
```

### 4.9.8 🎛️ Parameters

```groovy
pipeline {
    agent any
    parameters {
        string(name: 'VERSION', defaultValue: '1.0', description: 'App version')
        choice(name: 'ENV', choices: ['dev', 'test', 'prod'], description: 'Environment')
    }
    stages {
        stage('Show') {
            steps { echo "Deploying ${params.VERSION} to ${params.ENV}" }
        }
    }
}
```

---

## 4.10 🔑 Credentials

Never put passwords inside a Jenkinsfile. Store them in **Jenkins Credentials**.

```text
🔑 Credential Types
│
├── 👤 Username with password
├── 🎫 Secret text            → Tokens, API keys
├── 📄 Secret file            → kubeconfig, settings.xml
├── 🔐 SSH username with private key
└── 📜 Certificate
```

#### 🪜 Add a Credential

```text
Manage Jenkins → Credentials → System → Global credentials → Add Credentials
(Set ID, for example: dockerhub-creds)
```

#### 💻 Use in a Pipeline

```groovy
// Option 1: environment block (creates USER and PSW variables)
environment {
    DOCKER = credentials('dockerhub-creds')
}
// → DOCKER_USR and DOCKER_PSW

// Option 2: withCredentials
withCredentials([usernamePassword(
        credentialsId: 'dockerhub-creds',
        usernameVariable: 'USER',
        passwordVariable: 'PASS')]) {
    sh 'echo $PASS | docker login -u $USER --password-stdin'
}
```

#### ⚠️ Important

> Jenkins **hides (masks)** secrets in the console log. Still, **do not print secrets** with `echo`.

---

## 4.11 ⏰ Build Triggers

```text
⏰ Ways to Start a Build
│
├── 🪝 Webhook (GitHub → Jenkins)     → Best: instant, no waiting
├── 🔍 Poll SCM                       → Jenkins checks Git on a schedule
├── ⏰ Build Periodically (Cron)      → Run at fixed times
├── 🔗 Upstream / Downstream          → Start after another job
└── 🖱️ Manual                         → Click "Build Now"
```

### 4.11.1 🪝 GitHub Webhook

```text
1. GitHub repo → Settings → Webhooks → Add webhook
2. Payload URL:  http://<jenkins-server>:8080/github-webhook/
3. Content type: application/json
4. Event: Just the push event
5. In the Jenkins job: enable "GitHub hook trigger for GITScm polling"
```

### 4.11.2 ⏰ Cron Syntax

```text
MINUTE HOUR DAY-OF-MONTH MONTH DAY-OF-WEEK

H/5 * * * *      → Every 5 minutes
H 2 * * *        → Every day around 2 AM
H 9 * * 1-5      → Weekdays around 9 AM
```

#### 🧠 Webhook vs Polling

| 🪝 Webhook                      | 🔍 Poll SCM                          |
| ------------------------------- | ------------------------------------ |
| GitHub pushes the event         | Jenkins keeps asking Git             |
| Instant                         | Delay (depends on schedule)          |
| Less load                       | More load                            |
| Needs Jenkins reachable from GitHub | Works inside private networks    |

---

## 4.12 🔧 Global Tool Configuration

Set up tools Jenkins can use.

```text
Manage Jenkins → Tools
├── 🔧 JDK     → Name: JDK17  (install automatically or give path)
├── 🔨 Maven   → Name: Maven3
├── 🔗 Git     → Path to git
└── 🐳 Docker  → (or install Docker on the agent)
```

The **names** (`JDK17`, `Maven3`) are used in the Jenkinsfile `tools { }` block.

---

## 4.13 🔗 Jenkins Integrations

### 4.13.1 🔍 SonarQube

```groovy
stage('SonarQube Analysis') {
    steps {
        withSonarQubeEnv('sonarqube') {          // Server name from Jenkins settings
            sh 'mvn sonar:sonar'
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

### 4.13.2 📦 Nexus (Maven Deploy)

```groovy
stage('Upload to Nexus') {
    steps {
        configFileProvider([configFile(fileId: 'maven-settings', variable: 'MVN_SETTINGS')]) {
            sh 'mvn -s $MVN_SETTINGS -B deploy -DskipTests'
        }
    }
}
```

(Uses the **Config File Provider** plugin to hold `settings.xml` with Nexus credentials.)

### 4.13.3 🐳 Docker

```groovy
stage('Docker Build and Push') {
    steps {
        script {
            sh "docker build -t myuser/shop-app:${env.BUILD_NUMBER} ."
            withCredentials([usernamePassword(credentialsId: 'dockerhub-creds',
                    usernameVariable: 'USER', passwordVariable: 'PASS')]) {
                sh 'echo $PASS | docker login -u $USER --password-stdin'
                sh "docker push myuser/shop-app:${env.BUILD_NUMBER}"
            }
        }
    }
}
```

> The Jenkins user must be allowed to run Docker: `sudo usermod -aG docker jenkins` and restart Jenkins.

### 4.13.4 ☸️ Kubernetes Deploy

```groovy
stage('Deploy to Kubernetes') {
    steps {
        withCredentials([file(credentialsId: 'kubeconfig', variable: 'KUBECONFIG')]) {
            sh "kubectl set image deployment/shop-app shop-app=myuser/shop-app:${env.BUILD_NUMBER}"
        }
    }
}
```

### 4.13.5 📧 Notifications

```groovy
post {
    failure {
        mail to: 'team@example.com',
             subject: "FAILED: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
             body: "Check ${env.BUILD_URL}"
    }
}
```

---

## 4.14 🌍 Useful Built-in Variables

| Variable              | Meaning                                  |
| --------------------- | ---------------------------------------- |
| `${env.BUILD_NUMBER}` | Current build number                     |
| `${env.JOB_NAME}`     | Name of the job                          |
| `${env.BUILD_URL}`    | URL of the build                         |
| `${env.WORKSPACE}`    | Workspace folder path                    |
| `${env.BRANCH_NAME}`  | Branch name (Multibranch pipeline)       |
| `${env.GIT_COMMIT}`   | Commit hash                              |

---

## 4.15 🖥️ Distributed Builds (Agents)

```text
🖥️ Add an Agent
│
├── 🔐 SSH Agent        → Controller connects to the agent using SSH
├── 🔌 Inbound Agent    → Agent connects to the controller (port 50000)
└── ☸️ Kubernetes Agent → A pod is created for each build and deleted after
```

#### 🪜 Add an SSH Agent

```text
1. Install Java on the agent machine
2. Create a user and folder (remote root directory)
3. Manage Jenkins → Nodes → New Node → Permanent Agent
4. Set: Remote directory, Labels (like "linux docker"), Launch method (SSH)
5. Add SSH credentials
6. Save → Agent becomes online ✅
```

#### 💻 Use an Agent With a Label

```groovy
pipeline {
    agent { label 'docker' }
    stages { stage('Build') { steps { sh 'docker --version' } } }
}
```

#### 🐳 Docker as the Build Agent

```groovy
pipeline {
    agent { docker { image 'maven:3.9-eclipse-temurin-17' } }
    stages { stage('Build') { steps { sh 'mvn -B clean package' } } }
}
```

---

## 4.16 📚 Shared Libraries

A **Shared Library** is **common pipeline code** stored in Git and **reused by many pipelines**.

```groovy
// In the shared library: vars/buildApp.groovy
def call() {
    sh 'mvn -B clean package'
}

// In a Jenkinsfile
@Library('my-shared-lib') _
pipeline {
    agent any
    stages { stage('Build') { steps { buildApp() } } }
}
```

> **Shared Library = Write once, reuse in all pipelines**

---

## 4.17 🔒 Jenkins Security

```text
🔒 Jenkins Security
│
├── 👥 Authentication    → Who are you? (Jenkins users, LDAP, GitHub, SSO)
├── 🛂 Authorization     → What can you do? (Matrix, Role-based)
├── 🔑 Credentials       → Store secrets safely
├── 🌐 HTTPS             → Use a reverse proxy (Nginx) with SSL
└── 🔌 Plugin updates    → Keep everything updated
```

#### ✅ Best Practices

- 🚫 Do not allow anonymous access
- 👥 Use **role-based** access (Role Strategy plugin)
- 🔑 Use **Credentials**, not plain text
- 🖥️ Do **not** run builds on the controller
- 🔄 Update Jenkins and plugins regularly
- 🔒 Use HTTPS in production

---

## 4.18 💾 Backup and Maintenance

**Everything important is in `JENKINS_HOME`** (`/var/lib/jenkins`).

```text
📁 JENKINS_HOME
├── 📄 config.xml           → Main configuration
├── 📁 jobs/                → Job configurations and build history
├── 📁 plugins/             → Installed plugins
├── 📁 secrets/             → Encryption keys and initial password
├── 📁 users/               → User data
└── 📁 workspace/           → Build workspaces
```

#### 🧰 Maintenance Tips

- 💾 **Back up** `JENKINS_HOME` regularly
- 🧹 Limit **old builds** (`buildDiscarder`)
- 🧼 Clean old **workspaces**
- 📊 Watch **disk space**

---

## 4.19 🏆 Jenkins Best Practices

```text
✅ Jenkins Best Practices
│
├── 📜 Use Pipeline as Code (Jenkinsfile in Git)
├── 🔑 Store secrets in Credentials
├── 🖥️ Use agents for builds
├── 🪝 Use webhooks instead of polling
├── ⏱️ Add timeouts and build discarders
├── 🧩 Use Shared Libraries for common code
├── ❌ Fail fast (run quick tests first)
├── 🐳 Use Docker agents for clean, repeatable builds
└── 🔄 Keep Jenkins and plugins updated
```

---

## 4.20 🏗️ Real Example: Full CI/CD Pipeline

### 🎯 Requirement

On every push to `main`: **build with Maven, scan with SonarQube, upload to Nexus, build and push a Docker image, deploy to Kubernetes.**

### 🏗️ Flow

```text
🐙 GitHub (push) ── webhook ──► 🤖 Jenkins
                                    │
   1️⃣ Checkout ─► 2️⃣ Maven Build ─► 3️⃣ SonarQube ─► 4️⃣ Quality Gate
                                                         │
   7️⃣ Deploy to K8s ◄─ 6️⃣ Docker Push ◄─ 5️⃣ Nexus Upload ◄┘
```

### 📜 Jenkinsfile

```groovy
pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk   'JDK17'
    }

    environment {
        IMAGE = 'myuser/shop-app'
        TAG   = "${env.BUILD_NUMBER}"
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
        buildDiscarder(logRotator(numToKeepStr: '10'))
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/team/shop-app.git'
            }
        }

        stage('Build and Unit Test') {
            steps {
                sh 'mvn -B clean package'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('sonarqube') {
                    sh 'mvn sonar:sonar'
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

        stage('Upload to Nexus') {
            steps {
                configFileProvider([configFile(fileId: 'maven-settings', variable: 'MVN_SETTINGS')]) {
                    sh 'mvn -s $MVN_SETTINGS -B deploy -DskipTests'
                }
            }
        }

        stage('Docker Build and Push') {
            steps {
                sh "docker build -t ${IMAGE}:${TAG} ."
                withCredentials([usernamePassword(credentialsId: 'dockerhub-creds',
                        usernameVariable: 'USER', passwordVariable: 'PASS')]) {
                    sh 'echo $PASS | docker login -u $USER --password-stdin'
                    sh "docker push ${IMAGE}:${TAG}"
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                withCredentials([file(credentialsId: 'kubeconfig', variable: 'KUBECONFIG')]) {
                    sh "kubectl set image deployment/shop-app shop-app=${IMAGE}:${TAG}"
                    sh 'kubectl rollout status deployment/shop-app'
                }
            }
        }
    }

    post {
        success { echo 'Pipeline succeeded ✅' }
        failure { echo 'Pipeline failed ❌' }
        always  { cleanWs() }
    }
}
```

### 🪜 Setup Steps

```text
1. Install Jenkins and plugins (Git, Pipeline, SonarQube Scanner, Config File Provider, Docker Pipeline)
2. Manage Jenkins → Tools → add JDK17 and Maven3
3. Manage Jenkins → System → add the SonarQube server (name: sonarqube) with a token
4. Add credentials: dockerhub-creds, kubeconfig
5. Add settings.xml as a managed file (ID: maven-settings) with Nexus credentials
6. Create a Pipeline job → "Pipeline script from SCM" → Git repo URL → Jenkinsfile
7. Add the GitHub webhook
8. Push code → ✅ pipeline runs automatically
```

---

## 📌🧠 Jenkins Quick Revision

```text
🤖 Jenkins
│
├── 🏛️ Architecture
│   ├── Controller
│   ├── Agents / Nodes
│   └── Executors, Labels
│
├── 🧱 Jobs
│   ├── Freestyle
│   ├── Pipeline
│   └── Multibranch
│
├── 📜 Pipeline
│   ├── Declarative vs Scripted
│   ├── agent, tools, environment, parameters
│   ├── stages, steps, when, parallel
│   └── post (always, success, failure)
│
├── 🔑 Credentials
│
├── ⏰ Triggers
│   ├── Webhook
│   ├── Poll SCM
│   └── Cron
│
├── 🔗 Integrations
│   ├── Git, Maven
│   ├── SonarQube, Nexus
│   └── Docker, Kubernetes
│
└── 🔒 Operations
    ├── Plugins
    ├── Security (RBAC)
    └── Backup JENKINS_HOME
```

---

## 🧠⚡ Jenkins One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| 🤖 **Jenkins**             | Automation Server for CI/CD                         |
| 👑 **Controller**          | Main Jenkins Server                                 |
| 🖥️ **Agent / Node**        | Machine That Runs Builds                            |
| ⚙️ **Executor**            | One Build Slot on a Node                            |
| 🏷️ **Label**               | Tag to Choose an Agent                              |
| 🔌 **Plugin**              | Adds a Feature to Jenkins                           |
| 📜 **Pipeline**            | Automated Steps From Code to Deployment             |
| 📄 **Jenkinsfile**         | Pipeline Code Stored in Git                         |
| 📋 **Declarative**         | Structured Pipeline (Recommended)                   |
| 🔖 **Stage**               | Major Step (Build, Test, Deploy)                    |
| 👣 **Step**                | One Task Inside a Stage                             |
| 🔔 **post**                | Actions After the Build                             |
| 🔑 **Credentials**         | Safe Place for Passwords and Tokens                 |
| 🪝 **Webhook**             | GitHub Starts the Build Instantly                   |
| 🔍 **Poll SCM**           | Jenkins Checks Git on a Schedule                    |
| 📚 **Shared Library**      | Reusable Pipeline Code                              |
| 🏠 **JENKINS_HOME**        | Folder Holding All Jenkins Data                     |
| 🌐 **Port 8080**           | Default Jenkins Web Port                            |

---

## 🗺️ Jenkins Learning Map

```text
                          🤖 Jenkins
                              │
      ┌───────────────────────┼───────────────────────┐
      │                       │                       │
      ▼                       ▼                       ▼
   SETUP                   PIPELINE                INTEGRATIONS
      │                       │                       │
      ├── Install             ├── Jenkinsfile         ├── Git / GitHub
      ├── Plugins             ├── Declarative         ├── Maven
      ├── Tools               ├── Stages / Steps      ├── SonarQube
      ├── Credentials         ├── Parameters          ├── Nexus
      └── Security            ├── when / parallel     ├── Docker
                              └── post                └── Kubernetes
      │
      ▼
   TRIGGERS
      │
      ├── Webhook
      ├── Poll SCM
      └── Cron
      │
      ▼
   SCALING
      │
      ├── Agents / Nodes
      ├── Docker Agents
      ├── Kubernetes Agents
      └── Shared Libraries
```

---

## ⭐ Jenkins Final Memory

```text
Jenkins
 │
 ├── What is it?
 │      └── CI/CD automation server
 │
 ├── What defines the pipeline?
 │      └── Jenkinsfile
 │
 ├── Which pipeline type is recommended?
 │      └── Declarative
 │
 ├── Where do builds run?
 │      └── On Agents (not the Controller)
 │
 ├── How to start a build instantly on push?
 │      └── GitHub Webhook
 │
 ├── Where to keep passwords?
 │      └── Jenkins Credentials
 │
 ├── Default port?
 │      └── 8080
 │
 └── What to back up?
        └── JENKINS_HOME (/var/lib/jenkins)
```

---

# 🔍 PART 5 — SonarQube — Code Quality and Security

> **SonarQube = Automatic code reviewer that checks quality and security**

---

## 5.1 🔍 What is SonarQube?

> **SonarQube = Code quality and security analysis tool**

SonarQube **scans our source code automatically** and finds **bugs, security problems, bad coding practices and duplicate code** — **without running the program** (this is called **static code analysis**).

It shows the result on a **web dashboard** and can **stop a pipeline** if the code quality is not good enough.

#### 📦 SonarQube Checks

- 🐛 **Bugs** — code that may fail
- 🔓 **Vulnerabilities** — security problems
- 🔥 **Security Hotspots** — code that needs a security review
- 🧼 **Code Smells** — hard-to-maintain code
- 📋 **Duplications** — copy-pasted code
- 🧪 **Test Coverage** — how much code is tested

#### 🏗️ SonarQube Basic Idea

```text
💻 Source Code
      │
      ▼
🔎 SonarScanner / Maven plugin  (analyzes the code)
      │ sends report
      ▼
🔍 SonarQube Server
      │
      ├── 📊 Dashboard (issues, coverage, duplications)
      └── 🚦 Quality Gate  → ✅ Pass / ❌ Fail
```

#### 🧠 Easy Memory

> **SonarQube = Automatic code reviewer that checks quality and security**

---

## 5.2 🤔 Why Do We Use SonarQube?

### ❌ Without Code Analysis

```text
👨‍💻 Developer writes code
        ↓
👀 Manual review (people miss things)
        ↓
🚀 Bugs and security holes reach production
        ↓
💸 Expensive fixes later
```

### ✅ With SonarQube

```text
👨‍💻 Developer pushes code
        ↓
🔍 SonarQube scans automatically
        ↓
🚦 Quality Gate checks the rules
        ↓
✅ Good code moves forward   ❌ Bad code is stopped early
```

#### ⭐ Main Reasons

- 🐛 Find bugs **early** (cheaper to fix)
- 🔐 Find **security problems** early
- 🧼 Keep code **clean and maintainable**
- 📏 Enforce the **same quality rules** for the whole team
- 🚦 **Block** bad code using the Quality Gate
- 📈 Track quality **over time**
- 🌍 Supports many languages (Java, Python, JavaScript, C#, Go, PHP and more)

---

## 5.3 🧰 What Does SonarQube Provide?

SonarQube provides:

- 📊 Project Dashboards
- 🐛 Issue Detection (Bugs, Vulnerabilities, Code Smells)
- 🔥 Security Hotspots
- 📏 Quality Profiles (rule sets)
- 🚦 Quality Gates
- 🧪 Coverage and Duplication Reports
- ⏳ Technical Debt Estimates
- 🪝 Webhooks
- 🔑 Tokens and User Management
- 🔌 CI/CD Integration (Jenkins, GitHub Actions)

---

## 5.4 🏛️ SonarQube Architecture

```text
🏛️ SonarQube Components
│
├── 🌐 Web Server        → Dashboard and API (port 9000)
├── ⚙️ Compute Engine    → Processes the analysis reports
├── 🔎 Search Server     → Elasticsearch, makes searching fast
├── 🗄️ Database          → Stores configuration and results (PostgreSQL recommended)
└── 🔎 Scanner           → Runs on the build machine and analyzes the code
```

#### 🏗️ Flow

```text
🤖 Jenkins / Developer machine
        │  runs Scanner (mvn sonar:sonar)
        ▼
🔎 Scanner  ── sends report ──►  🌐 SonarQube Server
                                      │
                                      ├── ⚙️ Compute Engine (processes the report)
                                      ├── 🔎 Search (Elasticsearch)
                                      └── 🗄️ Database (PostgreSQL)
```

#### ⚠️ Important

> The **Scanner** runs on the **build machine**. The **SonarQube server** only receives and shows the results.

> The **embedded H2 database** is only for testing. Use **PostgreSQL** for real projects.

---

## 5.5 🧱 SonarQube Editions

| Edition                     | Cost        | Main Use                                           |
| --------------------------- | ----------- | -------------------------------------------------- |
| 🆓 **Community Build**      | Free        | Basic analysis, main branch                        |
| 👨‍💻 **Developer Edition**   | Paid        | Branch and Pull Request analysis, more languages   |
| 🏢 **Enterprise Edition**   | Paid        | Portfolios, reporting, large organizations         |
| 🏛️ **Data Center Edition**  | Paid        | High availability                                  |
| ☁️ **SonarQube Cloud**      | SaaS        | Hosted by Sonar (earlier called SonarCloud)        |

> 💡 Product names and edition features change. Check the official Sonar website for the current list.

---

## 5.6 ⚙️ Installing SonarQube

SonarQube runs on **port 9000**.

### 5.6.1 📋 Requirements

```text
📋 Requirements
│
├── ☕ Java (supported version — check the docs; Java 17 or newer for current releases)
├── 🗄️ Database (PostgreSQL recommended)
├── 💾 Enough RAM (at least 2–4 GB free)
└── 🐧 Linux kernel settings (see below)
```

### 5.6.2 🐧 Linux System Settings

SonarQube uses **Elasticsearch**, which needs these settings:

```bash
# Allow more memory maps
sudo sysctl -w vm.max_map_count=524288
sudo sysctl -w fs.file-max=131072

# Make permanent
echo "vm.max_map_count=524288" | sudo tee -a /etc/sysctl.conf
echo "fs.file-max=131072"      | sudo tee -a /etc/sysctl.conf

# Open files and process limits (for the sonar user)
# /etc/security/limits.conf
# sonar  -  nofile  131072
# sonar  -  nproc   8192
```

#### ⚠️ Important

> **SonarQube cannot run as the `root` user.** Create a normal user (like `sonar`) to run it.

### 5.6.3 🐳 Easy Way: Run With Docker

```bash
docker run -d --name sonarqube \
  -p 9000:9000 \
  -v sonarqube_data:/opt/sonarqube/data \
  -v sonarqube_logs:/opt/sonarqube/logs \
  -v sonarqube_extensions:/opt/sonarqube/extensions \
  sonarqube:community
```

> 💡 Check the Docker Hub page for the **current image tags** (like `community`, `lts-community`).

#### 🧩 Docker Compose (With PostgreSQL)

```yaml
services:
  sonarqube:
    image: sonarqube:community
    depends_on:
      - db
    environment:
      SONAR_JDBC_URL: jdbc:postgresql://db:5432/sonar
      SONAR_JDBC_USERNAME: sonar
      SONAR_JDBC_PASSWORD: sonar_password
    ports:
      - "9000:9000"
    volumes:
      - sonarqube_data:/opt/sonarqube/data
      - sonarqube_logs:/opt/sonarqube/logs
      - sonarqube_extensions:/opt/sonarqube/extensions

  db:
    image: postgres:16
    environment:
      POSTGRES_USER: sonar
      POSTGRES_PASSWORD: sonar_password
      POSTGRES_DB: sonar
    volumes:
      - postgresql_data:/var/lib/postgresql/data

volumes:
  sonarqube_data:
  sonarqube_logs:
  sonarqube_extensions:
  postgresql_data:
```

### 5.6.4 🌐 First Login

```text
1. Open  http://<server-ip>:9000
2. Default login:  admin / admin
3. 🔒 Change the password immediately
4. ✅ Dashboard is ready
```

#### 🔓 Firewall

```text
Open port 9000 (only to trusted IPs / Jenkins server)
```

---

## 5.7 🧱 SonarQube Basic Concepts

```text
🔍 SonarQube
│
├── 📁 Project           → One analyzed application
├── 🐛 Issue             → A problem found in the code
├── 📏 Quality Profile   → Set of rules for a language
├── 🚦 Quality Gate      → Pass/Fail rules for the project
├── 🆕 New Code          → Code changed recently (focus of the gate)
├── ⏳ Technical Debt    → Time needed to fix all issues
└── 🔑 Token             → Secret used by scanners to log in
```

### 5.7.1 🐛 Issue Types

| Type                  | Meaning                                                        | Example                              |
| --------------------- | -------------------------------------------------------------- | ------------------------------------ |
| 🐛 **Bug**            | Code that is **wrong** and may break at runtime                | Null pointer, resource not closed    |
| 🔓 **Vulnerability**  | A **security weakness** that can be attacked                   | SQL injection, hard-coded password   |
| 🔥 **Security Hotspot**| Security-sensitive code that **needs a human review**         | Use of weak encryption, cookies      |
| 🧼 **Code Smell**     | Code that is **hard to read or maintain** (not a direct bug)   | Long method, unused variable         |

#### 🧠 Easy Memory

```text
🐛 Bug           = It is wrong
🔓 Vulnerability = It is unsafe
🔥 Hotspot       = Please review for safety
🧼 Code Smell    = It is messy
```

### 5.7.2 ⚠️ Severity Levels

```text
🔴 Blocker → 🟠 Critical → 🟡 Major → 🔵 Minor → ⚪ Info
(most serious)                          (least serious)
```

> 💡 Newer SonarQube versions also show an **impact level (High / Medium / Low)** for issues.

### 5.7.3 🏅 Ratings (A to E)

SonarQube gives **ratings** from **A (best) to E (worst)**.

| Rating Area              | What It Measures                                     |
| ------------------------ | ---------------------------------------------------- |
| 🛡️ **Reliability**       | Bugs                                                 |
| 🔐 **Security**          | Vulnerabilities                                      |
| 🧼 **Maintainability**   | Code smells and technical debt                       |

```text
A = Excellent  →  B  →  C  →  D  →  E = Poor
```

### 5.7.4 ⏳ Technical Debt

**Technical Debt** = the **estimated time** needed to fix all maintainability issues.

```text
Example: Technical Debt = 2 days 4 hours
```

### 5.7.5 🆕 New Code and "Clean as You Code"

SonarQube focuses on **new and changed code** (the **New Code period**).

```text
💡 Clean as You Code
→ Do not worry about all old problems at once
→ Make sure every NEW change is clean
```

#### 🧠 Simple Meaning

> **Old code can wait. New code must be clean.**

---

## 5.8 📏 Quality Profile

A **Quality Profile** is a **collection of rules** for one programming language.

```text
📏 Quality Profile: "Sonar way" (Java)
├── Rule: Close resources after use
├── Rule: Do not hard-code passwords
├── Rule: Avoid empty catch blocks
└── ... hundreds of rules
```

#### ⭐ Key Points

- 🆕 Every language has a **default profile** (usually **Sonar way**)
- 🧬 We can **copy (extend)** a profile and change rules
- ✅ We can **activate / deactivate** rules
- 🎯 Different projects can use different profiles

> **Quality Profile = Which rules are checked**

---

## 5.9 🚦 Quality Gate

A **Quality Gate** is a **set of conditions** the project must meet to **pass**.

```text
📁 Project Analysis
        │
        ▼
🚦 Quality Gate (conditions)
        │
   ┌────┴─────┐
   ▼          ▼
✅ PASSED    ❌ FAILED
(continue)   (stop the pipeline)
```

### 5.9.1 📋 Default "Sonar way" Gate (On New Code)

| Condition                                  | Typical Requirement             |
| ------------------------------------------ | ------------------------------- |
| 🐛 New bugs                                | 0 (reliability rating A)        |
| 🔓 New vulnerabilities                     | 0 (security rating A)           |
| 🔥 Security hotspots reviewed              | 100%                            |
| 🧪 Coverage on new code                    | At least 80%                    |
| 📋 Duplicated lines on new code            | At most 3%                      |

> 💡 The exact default gate can change between SonarQube versions.

### 5.9.2 🛠️ Custom Quality Gate

We can **create our own gate**:

```text
Quality Gates → Create
├── Coverage on New Code      is less than  70%   → Fail
├── Bugs on New Code          is greater than 0   → Fail
└── Maintainability Rating    is worse than A     → Fail
```

#### 🧠 Remember

> **Quality Profile = rules to check. Quality Gate = pass/fail decision.**

### 5.9.3 📊 Profile vs Gate

| 📏 Quality Profile                 | 🚦 Quality Gate                          |
| ---------------------------------- | ---------------------------------------- |
| Decides **which rules** are checked| Decides **pass or fail**                 |
| Per language                       | Per project                              |
| Creates **issues**                 | Uses **metrics** (coverage, bugs...)     |

---

## 5.10 🔑 Tokens

A **Token** lets scanners and tools **log in to SonarQube** without a password.

#### 🪜 Generate a Token

```text
SonarQube → My Account (top right) → Security → Generate Tokens
→ Name: jenkins-token → Generate → Copy the token (shown only once)
```

#### ⚠️ Important

> **Copy the token immediately.** It is shown only once.

> **Store the token in Jenkins Credentials**, not in the code.

---

## 5.11 🔎 Running a Scan

### 5.11.1 🔨 With Maven (Easiest for Java)

```bash
mvn clean verify sonar:sonar \
  -Dsonar.projectKey=shop-app \
  -Dsonar.projectName="Shop App" \
  -Dsonar.host.url=http://<sonarqube-server>:9000 \
  -Dsonar.token=<your-token>
```

> 💡 Older versions use `-Dsonar.login=<token>`. Newer versions use `-Dsonar.token`.

### 5.11.2 📄 Using Properties in pom.xml

```xml
<properties>
  <sonar.projectKey>shop-app</sonar.projectKey>
  <sonar.host.url>http://sonar.example.com:9000</sonar.host.url>
  <sonar.coverage.jacoco.xmlReportPaths>target/site/jacoco/jacoco.xml</sonar.coverage.jacoco.xmlReportPaths>
</properties>
```

### 5.11.3 🔎 SonarScanner CLI (For Any Language)

Create **`sonar-project.properties`** in the project root:

```properties
sonar.projectKey=shop-app
sonar.projectName=Shop App
sonar.projectVersion=1.0
sonar.sources=src
sonar.host.url=http://sonar.example.com:9000
sonar.sourceEncoding=UTF-8
```

Run:

```bash
sonar-scanner -Dsonar.token=<your-token>
```

#### 📖 Common Properties

| Property                  | Meaning                                       |
| ------------------------- | --------------------------------------------- |
| `sonar.projectKey`        | Unique ID of the project                      |
| `sonar.projectName`       | Display name                                  |
| `sonar.sources`           | Folder with source code                       |
| `sonar.tests`             | Folder with test code                         |
| `sonar.host.url`          | SonarQube server URL                          |
| `sonar.token`             | Authentication token                          |
| `sonar.java.binaries`     | Compiled classes folder (Java)                |
| `sonar.exclusions`        | Files to ignore                               |
| `sonar.coverage.exclusions` | Files to ignore for coverage                |

---

## 5.12 🧪 Code Coverage With JaCoCo

SonarQube does **not run tests**. It **reads the coverage report** made by a tool like **JaCoCo**.

```text
🧪 Tests run (mvn test) + JaCoCo agent
        ↓
📄 jacoco.xml (coverage report)
        ↓
🔎 Sonar Scanner reads the report
        ↓
📊 Coverage % shown in SonarQube
```

#### 💻 JaCoCo Plugin in pom.xml

```xml
<plugin>
  <groupId>org.jacoco</groupId>
  <artifactId>jacoco-maven-plugin</artifactId>
  <version>0.8.11</version>
  <executions>
    <execution>
      <goals><goal>prepare-agent</goal></goals>
    </execution>
    <execution>
      <id>report</id>
      <phase>verify</phase>
      <goals><goal>report</goal></goals>
    </execution>
  </executions>
</plugin>
```

---

## 5.13 🔗 SonarQube With Jenkins

### 5.13.1 🪜 Setup Steps

```text
1. Jenkins → Install plugin: "SonarQube Scanner"
2. SonarQube → Generate a token
3. Jenkins → Credentials → Add "Secret text" (ID: sonar-token)
4. Jenkins → Manage Jenkins → System → SonarQube servers
        Name: sonarqube
        Server URL: http://<sonar-server>:9000
        Token: sonar-token
5. SonarQube → Administration → Configuration → Webhooks → Create
        Name: jenkins
        URL: http://<jenkins-server>:8080/sonarqube-webhook/
6. Use withSonarQubeEnv and waitForQualityGate in the Jenkinsfile
```

#### ⚠️ Important

> The **webhook** (step 5) is needed so Jenkins can **receive the Quality Gate result**. Without it, `waitForQualityGate` waits until timeout.

### 5.13.2 📜 Jenkinsfile Stages

```groovy
stage('SonarQube Analysis') {
    steps {
        withSonarQubeEnv('sonarqube') {
            sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=shop-app'
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

### 5.13.3 🏗️ Flow

```text
🤖 Jenkins ── mvn sonar:sonar ──► 🔍 SonarQube
                                       │ analysis done
                                       │ webhook (Quality Gate result)
🤖 Jenkins ◄──────────────────────────┘
      │
      ├── ✅ PASSED → continue (Nexus upload, Docker build ...)
      └── ❌ FAILED → pipeline stops
```

---

## 5.14 🪝 Webhooks and PR Decoration

- 🪝 **Webhook** — SonarQube sends a message (to Jenkins or others) when analysis finishes
- 🔀 **Pull Request Decoration** (Developer Edition and above) — shows issues directly inside the GitHub Pull Request

---

## 5.15 👥 Users, Permissions and Security

```text
🔒 SonarQube Security
│
├── 👥 Users and Groups         → Create users, put them in groups
├── 🛂 Permissions              → Admin, Browse, Execute Analysis, Issue Admin ...
├── 🔑 Tokens                   → For scanners and CI
├── 🌐 Authentication           → Local, LDAP, SAML, GitHub login
└── 🔐 HTTPS                    → Use a reverse proxy (Nginx) with SSL
```

#### ✅ Best Practices

- 🔒 Change the default `admin` password
- 🔑 Use **tokens** for CI (not user passwords)
- 👥 Give **minimum permissions**
- 🗄️ Use **PostgreSQL** and back it up

---

## 5.16 🏆 SonarQube Best Practices

```text
✅ SonarQube Best Practices
│
├── 🔁 Scan on every commit / pull request
├── 🚦 Use a Quality Gate and fail the pipeline when needed
├── 🆕 Focus on New Code (Clean as You Code)
├── 🧪 Add test coverage reports (JaCoCo)
├── 🔑 Keep tokens in Jenkins Credentials
├── 🗄️ Use PostgreSQL for real use
└── 📉 Fix Blocker and Critical issues first
```

---

## 5.17 🏗️ Real Example: Quality Check in a Pipeline

### 🎯 Requirement

Stop the pipeline if the code has **new bugs, new vulnerabilities or low coverage**.

### 🪜 Steps

```text
1. Run SonarQube (Docker or server) on port 9000
2. Change the admin password and generate a token
3. Create a Jenkins credential for the token
4. Add the SonarQube server in Jenkins (name: sonarqube)
5. Add the webhook in SonarQube → http://<jenkins>:8080/sonarqube-webhook/
6. Add JaCoCo plugin to pom.xml for coverage
7. Add 'SonarQube Analysis' and 'Quality Gate' stages to the Jenkinsfile
8. Push code
9. ✅ Pipeline passes only if the Quality Gate is PASSED
```

### 🏗️ Architecture

```text
🐙 GitHub
    │ webhook
    ▼
🤖 Jenkins ──► 🔨 Maven build + tests (JaCoCo report)
    │
    ├──► 🔎 Sonar Scanner ──► 🔍 SonarQube (analysis)
    │
    └──◄ 🚦 Quality Gate result (via webhook)
              │
         ✅ PASS → Nexus → Docker → Deploy
         ❌ FAIL → Stop and notify the team
```

---

## 📌🧠 SonarQube Quick Revision

```text
🔍 SonarQube
│
├── 🏛️ Architecture
│   ├── Web Server (9000)
│   ├── Compute Engine
│   ├── Elasticsearch
│   ├── Database (PostgreSQL)
│   └── Scanner
│
├── 🐛 Issue Types
│   ├── Bug
│   ├── Vulnerability
│   ├── Security Hotspot
│   └── Code Smell
│
├── 📏 Rules and Gates
│   ├── Quality Profile (rules)
│   ├── Quality Gate (pass / fail)
│   └── New Code / Clean as You Code
│
├── 📊 Metrics
│   ├── Coverage
│   ├── Duplications
│   ├── Ratings A–E
│   └── Technical Debt
│
├── 🔎 Scanning
│   ├── mvn sonar:sonar
│   ├── SonarScanner CLI
│   └── sonar-project.properties
│
└── 🔗 Integration
    ├── Token
    ├── Jenkins (withSonarQubeEnv, waitForQualityGate)
    └── Webhook
```

---

## 🧠⚡ SonarQube One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| 🔍 **SonarQube**           | Automatic Code Quality and Security Checker         |
| 🔎 **Static Analysis**     | Check Code Without Running It                       |
| 🐛 **Bug**                 | Code That Is Wrong                                  |
| 🔓 **Vulnerability**       | Code That Is Unsafe                                 |
| 🔥 **Security Hotspot**    | Needs a Human Security Review                       |
| 🧼 **Code Smell**          | Messy, Hard-to-Maintain Code                        |
| 📋 **Duplication**         | Copy-Pasted Code                                    |
| 🧪 **Coverage**            | % of Code Tested (From JaCoCo)                      |
| 📏 **Quality Profile**     | Set of Rules for a Language                         |
| 🚦 **Quality Gate**        | Pass / Fail Decision                                |
| 🆕 **New Code**            | Recently Changed Code (Clean as You Code)           |
| ⏳ **Technical Debt**      | Time to Fix All Maintainability Issues              |
| 🏅 **Ratings**             | A (Best) to E (Worst)                               |
| 🔑 **Token**               | Secret Used by Scanners to Log In                   |
| 🪝 **Webhook**             | Sends Quality Gate Result to Jenkins                |
| 🌐 **Port 9000**           | Default SonarQube Web Port                          |

---

## 🗺️ SonarQube Learning Map

```text
                         🔍 SonarQube
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
   SETUP                    ANALYSIS                 DECISION
      │                        │                        │
      ├── Docker / Install     ├── Scanner              ├── Quality Profile
      ├── PostgreSQL           │    ├── Maven           ├── Quality Gate
      ├── System settings      │    └── CLI             └── New Code
      ├── Token                ├── JaCoCo Coverage
      └── Users                └── Issues
                                    ├── Bug
      │                             ├── Vulnerability
      ▼                             ├── Hotspot
   INTEGRATION                      └── Code Smell
      │
      ├── Jenkins plugin
      ├── Webhook
      └── GitHub PR decoration
```

---

## ⭐ SonarQube Final Memory

```text
SonarQube
 │
 ├── What is it?
 │      └── Code quality and security analysis tool
 │
 ├── Does it run the program?
 │      └── No (static analysis)
 │
 ├── Default port?
 │      └── 9000
 │
 ├── What are the 4 issue types?
 │      └── Bug, Vulnerability, Security Hotspot, Code Smell
 │
 ├── What decides pass or fail?
 │      └── Quality Gate
 │
 ├── What decides which rules run?
 │      └── Quality Profile
 │
 ├── How does the scanner log in?
 │      └── Token
 │
 └── How does Jenkins get the gate result?
        └── SonarQube webhook → /sonarqube-webhook/
```

---

# 📦 PART 6 — Nexus Repository — Artifact Management

> **Nexus = Private storage room for our artifacts and libraries**

---

## 6.1 📦 What is Nexus Repository?

> **Nexus Repository = Artifact repository manager (by Sonatype)**

Nexus Repository is a **central store for build outputs (artifacts) and libraries (dependencies)**.

It is like a **private warehouse** for our company where we keep:

- 📦 Our own build files (`.jar`, `.war`, `.zip`)
- 📥 Downloaded libraries (cached copies from Maven Central, npm, PyPI)
- 🐳 Docker images
- 📚 Packages in many formats

#### 🏗️ Nexus Basic Idea

```text
🤖 Jenkins ── mvn deploy ──►  📦 Nexus Repository  ◄── mvn / npm / docker pull ── 👨‍💻 Developers
                                   │
                                   ├── 🏢 Our own artifacts (hosted)
                                   └── 🌍 Cached public libraries (proxy)
```

#### 🧠 Easy Memory

> **Nexus = Private storage room for our artifacts and libraries**

---

## 6.2 🤔 Why Do We Use Nexus?

### ❌ Without Nexus

```text
👨‍💻 Every developer and Jenkins downloads libraries from the internet
        ↓
🐢 Slow builds
🌐 Build fails if the internet or Maven Central is down
📁 Built artifacts are copied manually or kept on random servers
🔢 No clear version history of builds
```

### ✅ With Nexus

```text
📥 Libraries are downloaded once and cached in Nexus
📦 Every build artifact is uploaded to Nexus with a version
🔁 Same artifact is used for test, staging and production
⚡ Faster and reliable builds
```

#### ⭐ Main Reasons

- ⚡ **Faster builds** (local cache of dependencies)
- 🛡️ **Reliable** — builds work even if public repositories are down
- 📦 **Central place** for all artifacts
- 🔢 **Version control** of build outputs
- 🔒 **Security** — control who can upload and download
- 🌐 **One URL** for many repositories (using Group)
- 🧩 Supports **many formats** (Maven, npm, Docker, PyPI ...)

---

## 6.3 🧰 What Does Nexus Provide?

Nexus provides:

- 🗄️ Hosted, Proxy and Group Repositories
- 🧩 Many Package Formats
- 💾 Blob Stores (storage)
- 🧹 Cleanup Policies
- 👥 Users, Roles and Privileges
- 🔍 Search
- ⏰ Scheduled Tasks
- 🔌 REST API
- 🔗 Integration with Maven, Jenkins, Docker, npm

---

## 6.4 🧱 Nexus Basic Concepts

```text
📦 Nexus Repository
│
├── 🗄️ Repository   → A place that stores components
├── 📦 Component    → A package (like my-app 1.0.0)
├── 📄 Asset        → An actual file inside a component (.jar, .pom)
├── 💾 Blob Store   → Where files are physically stored on disk / S3
└── 🔑 Role / Privilege → Who can do what
```

### 6.4.1 📖 Simple Definitions

| Concept          | Simple Meaning                                                      |
| ---------------- | ------------------------------------------------------------------- |
| 🗄️ Repository    | A storage area for one format (like a Maven repository)             |
| 📦 Component     | A software package identified by group, name and version            |
| 📄 Asset         | A file that belongs to a component (jar, pom, checksum)             |
| 💾 Blob Store    | The physical storage location of the files                          |
| 🧩 Format        | Package type (Maven, npm, Docker, PyPI, NuGet, Raw ...)             |
| 🧹 Cleanup Policy| Rule to delete old or unused components automatically               |

#### 🏗️ Relationship

```text
🗄️ Repository: maven-releases
   └── 📦 Component: com.example : my-app : 1.0.0
          ├── 📄 Asset: my-app-1.0.0.jar
          ├── 📄 Asset: my-app-1.0.0.pom
          └── 📄 Asset: my-app-1.0.0.jar.sha1
```

---

## 6.5 🗄️ Repository Types

```text
🗄️ Nexus Repository Types
│
├── 🏠 Hosted  → We upload our own artifacts here
├── 🪞 Proxy   → Caches artifacts from a remote repository (Maven Central)
└── 🧩 Group   → Combines many repositories behind one URL
```

### 6.5.1 🏠 Hosted Repository

A repository **where we store our own artifacts**.

- ✅ Jenkins uploads builds here
- 🔢 Example: `maven-releases`, `maven-snapshots`

### 6.5.2 🪞 Proxy Repository

A repository that **points to a remote repository** (like Maven Central) and **caches** what is downloaded.

```text
👨‍💻 Developer asks for a library
        ↓
🪞 Nexus Proxy (maven-central)
        │
        ├── 💾 Already cached?  → Return from Nexus (fast)
        └── ❌ Not cached?      → Download from Maven Central, save a copy, return it
```

### 6.5.3 🧩 Group Repository

A repository that **combines several repositories** (hosted + proxy) into **one single URL**.

```text
🧩 maven-public  (Group)
   ├── 🏠 maven-releases
   ├── 🏠 maven-snapshots
   └── 🪞 maven-central
```

Developers use **only one URL** (`maven-public`) to get everything.

### 6.5.4 📊 Comparison

| 🏠 Hosted                      | 🪞 Proxy                           | 🧩 Group                           |
| ------------------------------ | ---------------------------------- | ---------------------------------- |
| Stores **our own** artifacts   | Caches **remote** repositories     | **Combines** many repositories     |
| We can upload                  | Read-only for users                | Read-only for users                |
| Example: `maven-releases`      | Example: `maven-central`           | Example: `maven-public`            |

#### 🧠 Easy Memory

```text
🏠 Hosted = Our own shelf (we put items)
🪞 Proxy  = Photocopy of a public library
🧩 Group  = One window that shows all shelves
```

---

## 6.6 🔢 Default Maven Repositories

Nexus creates these Maven repositories by default:

| Repository          | Type   | Version Policy | Purpose                                  |
| ------------------- | ------ | -------------- | ---------------------------------------- |
| `maven-central`     | Proxy  | Release        | Cache of Maven Central                   |
| `maven-releases`    | Hosted | Release        | Our **release** artifacts (1.0.0)        |
| `maven-snapshots`   | Hosted | Snapshot       | Our **SNAPSHOT** artifacts (1.0.0-SNAPSHOT) |
| `maven-public`      | Group  | —              | One URL for all of the above             |

### 6.6.1 🔢 Version Policy

```text
🔢 Version Policy
│
├── ✅ Release   → Only final versions (1.0.0)
├── 🚧 Snapshot  → Only development versions (1.0.0-SNAPSHOT)
└── 🔀 Mixed     → Both
```

### 6.6.2 🛡️ Deployment Policy (Hosted Repositories)

| Policy                | Meaning                                              |
| --------------------- | ---------------------------------------------------- |
| 🚫 Disable redeploy   | Cannot upload the same version again (**best for releases**) |
| ✅ Allow redeploy     | Can overwrite an existing version                    |
| 🔒 Read-only          | No uploads allowed                                   |

#### ⚠️ Important

> **Release artifacts should never change.** Use **Disable redeploy** on the releases repository.

---

## 6.7 🧩 Supported Formats

```text
🧩 Nexus Formats
│
├── ☕ Maven (Java)
├── 🟢 npm (Node.js)
├── 🐳 Docker
├── 🐍 PyPI (Python)
├── 🟣 NuGet (.NET)
├── 💎 RubyGems
├── ☸️ Helm
├── 🐧 apt (Debian) and yum (RPM)
├── 📁 Raw (any file)
└── ... and more
```

> 💡 The list of formats and edition limits changes. Check the Sonatype documentation for the current details.

---

## 6.8 🧱 Editions

| Edition                                | Notes                                                      |
| -------------------------------------- | ---------------------------------------------------------- |
| 🆓 **Nexus Repository Community Edition** | Free; has usage limits (components / requests)          |
| 💼 **Nexus Repository Pro**             | Paid; high availability, more features, support            |

> 💡 Sonatype changed its free edition name and limits over time (earlier called **OSS**). Check the current edition details on the Sonatype website before planning production use.

---

## 6.9 ⚙️ Installing Nexus

Nexus Repository runs on **port 8081** by default.

### 6.9.1 🐳 Docker (Easiest)

```bash
docker run -d --name nexus \
  -p 8081:8081 \
  -v nexus-data:/nexus-data \
  sonatype/nexus3
```

```text
Wait 2–3 minutes for Nexus to start, then open:  http://<server-ip>:8081
```

#### 🔑 Get the Admin Password

```bash
docker exec nexus cat /nexus-data/admin.password
```

### 6.9.2 🐧 Install on Linux (Manual)

```bash
# 1. Create a user (do not run as root)
sudo useradd -m -d /opt/nexus -s /bin/bash nexus

# 2. Download and extract Nexus (get the latest link from the Sonatype download page)
cd /opt
sudo tar -xzf nexus-<version>-unix.tar.gz
sudo mv nexus-<version> nexus
sudo chown -R nexus:nexus /opt/nexus /opt/sonatype-work

# 3. Run as the nexus user
# edit /opt/nexus/bin/nexus.rc   →   run_as_user="nexus"

# 4. Start Nexus
sudo -u nexus /opt/nexus/bin/nexus start
```

#### 📁 Important Locations

| Path                                         | Meaning                              |
| -------------------------------------------- | ------------------------------------ |
| `/opt/nexus`                                 | Nexus program files                  |
| `/opt/sonatype-work/nexus3`                  | **Data directory** (blobs, database) |
| `/opt/sonatype-work/nexus3/admin.password`   | Initial admin password               |
| `/nexus-data` (Docker)                       | Data directory in the container      |

#### 🔓 Firewall

```text
Open port 8081 (UI and Maven repositories)
Open the Docker registry port (like 8082) only if using Docker repositories
```

### 6.9.3 🌐 First-Time Setup

```text
1. Open  http://<server-ip>:8081
2. Click "Sign in" → username: admin → password from admin.password
3. Run the setup wizard → set a NEW admin password
4. Choose whether to allow anonymous access
5. ✅ Nexus is ready
```

#### ⚠️ Important

> **Disable anonymous access** for private artifacts, or give anonymous users **read-only** access to selected repositories only.

---

## 6.10 💾 Blob Stores

A **Blob Store** is **where Nexus saves the actual files**.

```text
💾 Blob Store Types
│
├── 📁 File       → On the local disk or mounted volume (default)
└── ☁️ S3         → Amazon S3 bucket
```

#### ⭐ Key Points

- 💾 Each repository uses one blob store
- 📈 Plan **enough disk space** — artifacts grow quickly
- ☁️ S3 blob store is useful for **cloud storage and durability**

---

## 6.11 🧹 Cleanup Policies and Tasks

Old artifacts use a lot of disk space.

### 6.11.1 🧹 Cleanup Policy

Automatically **removes components** based on rules.

```text
🧹 Example Cleanup Policy
├── Delete snapshots older than 30 days
└── Delete components not downloaded for 90 days
```

### 6.11.2 ⏰ Scheduled Tasks

Nexus runs **tasks** automatically.

| Task                              | Purpose                                         |
| --------------------------------- | ----------------------------------------------- |
| 🧹 Cleanup service                | Apply cleanup policies                          |
| 🗜️ Compact blob store             | Actually free disk space after deletion         |
| 💾 Database backup                | Back up the Nexus database                      |
| 🔍 Rebuild repository index       | Fix search problems                             |

#### ⚠️ Important

> **Deleting a component does not free disk space until you run the "Compact blob store" task.**

---

## 6.12 👥 Security: Users, Roles and Privileges

```text
🔒 Nexus Security
│
├── 👤 Users        → People or service accounts (like jenkins-deployer)
├── 🎭 Roles        → Groups of privileges (like nx-admin, nx-anonymous)
├── 🔑 Privileges   → Permissions (read, add, edit, delete on a repository)
└── 🌐 Realms       → Authentication sources (Local, LDAP, tokens)
```

#### 🧱 Common Setup

```text
👤 jenkins-deployer  → Role: can upload (deploy) to maven-releases and maven-snapshots
👤 developers        → Role: read-only access to maven-public
🙈 anonymous         → Disabled (or read-only)
```

#### ✅ Best Practices

- 🔒 **Change** the admin password
- 👤 Create a **separate user for Jenkins** (not admin)
- 🔑 Give **minimum permissions**
- 🌐 Use **HTTPS** (reverse proxy with SSL)

---

## 6.13 🔗 Using Nexus With Maven

### 6.13.1 🪞 Download Dependencies From Nexus (Mirror)

In **`~/.m2/settings.xml`**:

```xml
<settings>
  <mirrors>
    <mirror>
      <id>nexus</id>
      <mirrorOf>*</mirrorOf>
      <url>http://nexus.example.com:8081/repository/maven-public/</url>
    </mirror>
  </mirrors>

  <servers>
    <server>
      <id>nexus-releases</id>
      <username>jenkins-deployer</username>
      <password>${env.NEXUS_PASSWORD}</password>
    </server>
    <server>
      <id>nexus-snapshots</id>
      <username>jenkins-deployer</username>
      <password>${env.NEXUS_PASSWORD}</password>
    </server>
  </servers>
</settings>
```

### 6.13.2 📤 Upload Artifacts to Nexus

In **`pom.xml`**:

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

```bash
mvn clean deploy
```

```text
Version 1.0.0-SNAPSHOT → maven-snapshots
Version 1.0.0          → maven-releases
```

#### ⚠️ Important

> The **`id`** in `settings.xml` (`nexus-releases`, `nexus-snapshots`) must **match** the `id` in the POM.

### 6.13.3 🏗️ Flow

```text
🔨 Maven build
     │ mvn deploy
     ▼
📦 Nexus  (maven-snapshots or maven-releases)
     ▲
     │ dependency download (maven-public)
🔨 Other projects / developers
```

---

## 6.14 🐳 Docker Registry in Nexus

Nexus can work as a **private Docker registry**.

```text
🐳 Docker Repositories
│
├── 🏠 docker-hosted  → Our own images (push)
├── 🪞 docker-proxy   → Cache of Docker Hub
└── 🧩 docker-group   → One URL for both
```

#### 🪜 Setup

```text
1. Create a repository: docker (hosted)
2. Enable an HTTP connector on a port (example: 8082)
3. Open the port in the firewall
4. Enable the "Docker Bearer Token Realm" (Security → Realms) when needed
```

#### 💻 Push and Pull

```bash
# Login
docker login nexus.example.com:8082

# Tag the image with the registry address
docker tag shop-app:1.0 nexus.example.com:8082/shop-app:1.0

# Push
docker push nexus.example.com:8082/shop-app:1.0

# Pull
docker pull nexus.example.com:8082/shop-app:1.0
```

#### ⚠️ Important

> Docker requires **HTTPS** by default. For a test server using plain HTTP, add the registry to Docker's `insecure-registries` setting. **Use HTTPS in production.**

---

## 6.15 🟢 Using Nexus With npm and PyPI

### 6.15.1 🟢 npm

```bash
npm config set registry http://nexus.example.com:8081/repository/npm-group/
npm install express
```

### 6.15.2 🐍 PyPI (pip)

```bash
pip install --index-url http://nexus.example.com:8081/repository/pypi-group/simple requests
```

> **Same idea:** one private URL for downloading packages, and one hosted repository for our own packages.

---

## 6.16 🔗 Nexus With Jenkins

```text
🤖 Jenkins Pipeline
     │
     ├── 🔨 mvn clean package
     ├── 🔍 SonarQube Analysis
     └── 📤 mvn deploy  ──►  📦 Nexus
```

#### 💻 Pipeline Stage

```groovy
stage('Upload to Nexus') {
    steps {
        configFileProvider([configFile(fileId: 'maven-settings', variable: 'MVN_SETTINGS')]) {
            sh 'mvn -s $MVN_SETTINGS -B deploy -DskipTests'
        }
    }
}
```

#### 📚 Other Ways

| Method                             | Used For                                      |
| ---------------------------------- | --------------------------------------------- |
| `mvn deploy`                       | Maven projects (recommended)                  |
| Nexus Artifact Uploader plugin     | Upload any file from Jenkins                  |
| `curl` with REST API               | Upload raw files                              |

#### 💻 Upload a File With curl (Raw Repository)

```bash
curl -u jenkins-deployer:$NEXUS_PASSWORD \
  --upload-file app.zip \
  http://nexus.example.com:8081/repository/raw-hosted/app/app-1.0.zip
```

---

## 6.17 💾 Backup and Maintenance

```text
💾 What to Back Up
│
├── 🗄️ Nexus database (export using the scheduled backup task)
├── 📁 Blob stores (the actual artifact files)
└── ⚙️ Configuration
```

#### 🧰 Maintenance Tips

- 📊 Watch **disk space** carefully
- 🧹 Use **cleanup policies** and **compact blob store**
- 🔄 **Upgrade** Nexus regularly for security fixes
- 🔒 Use **HTTPS** and strong passwords

---

## 6.18 🆚 Nexus vs Artifactory vs Docker Hub

| Feature              | 📦 Nexus Repository         | 🐸 JFrog Artifactory        | 🐳 Docker Hub            |
| -------------------- | --------------------------- | --------------------------- | ------------------------ |
| Made by              | Sonatype                    | JFrog                       | Docker                   |
| Formats              | Many (Maven, npm, Docker …) | Many (Maven, npm, Docker …) | Docker images only       |
| Self-hosted          | ✅ Yes                      | ✅ Yes                      | ❌ Cloud service         |
| Free option          | ✅ Community Edition (limits) | ✅ Limited free edition   | ✅ Limited free          |
| Main use             | Artifact repository         | Artifact repository         | Public Docker images     |

---

## 6.19 🏆 Nexus Best Practices

```text
✅ Nexus Best Practices
│
├── 🧩 Use Group repositories (one URL for developers)
├── 🔒 Disable redeploy for release repositories
├── 👤 Use a separate deploy user for Jenkins
├── 🧹 Set cleanup policies for snapshots
├── 💾 Monitor disk space and compact blob stores
├── 🔐 Use HTTPS
└── 📦 Always use the same artifact from Nexus for every environment
```

---

## 6.20 🏗️ Real Example: Nexus in a Maven Pipeline

### 🎯 Requirement

Jenkins builds a Java app and stores the `.jar` in Nexus. Developers download libraries through Nexus.

### 🪜 Steps

```text
1. Run Nexus (Docker) on port 8081 and complete the setup wizard
2. Create a user: jenkins-deployer (role: deploy to maven-releases / snapshots)
3. Copy the URLs of maven-releases and maven-snapshots
4. Add distributionManagement to the pom.xml
5. Add the server credentials and mirror to settings.xml
6. Store settings.xml in Jenkins (Config File Provider, ID: maven-settings)
7. Add an 'Upload to Nexus' stage in the Jenkinsfile (mvn deploy)
8. Run the pipeline
9. ✅ Open Nexus → Browse → maven-snapshots → see the uploaded artifact
```

### 🏗️ Architecture

```text
👨‍💻 Developer ──► 🐙 GitHub ──► 🤖 Jenkins
                                    │
                         🔨 Maven build + 🔍 SonarQube
                                    │ mvn deploy
                                    ▼
                         📦 Nexus Repository
                            ├── 🏠 maven-snapshots   (1.0.0-SNAPSHOT)
                            ├── 🏠 maven-releases    (1.0.0)
                            ├── 🪞 maven-central     (cached libraries)
                            └── 🧩 maven-public      (group URL)
                                    │
                                    ▼
                         🚀 Deployment uses the artifact from Nexus
```

---

## 📌🧠 Nexus Repository Quick Revision

```text
📦 Nexus Repository
│
├── 🧱 Concepts
│   ├── Repository, Component, Asset
│   ├── Blob Store
│   └── Format
│
├── 🗄️ Repository Types
│   ├── 🏠 Hosted
│   ├── 🪞 Proxy
│   └── 🧩 Group
│
├── ☕ Default Maven Repos
│   ├── maven-central (proxy)
│   ├── maven-releases (hosted)
│   ├── maven-snapshots (hosted)
│   └── maven-public (group)
│
├── 🔒 Security
│   ├── Users, Roles, Privileges
│   └── Anonymous access
│
├── 🧹 Maintenance
│   ├── Cleanup Policies
│   ├── Compact Blob Store
│   └── Backups
│
└── 🔗 Integrations
    ├── Maven (settings.xml + pom.xml)
    ├── Jenkins (mvn deploy)
    ├── Docker registry
    └── npm / PyPI
```

---

## 🧠⚡ Nexus Repository One-Line Memory

| Concept                      | Easy Memory                                         |
| ---------------------------- | --------------------------------------------------- |
| 📦 **Nexus**                 | Private Storage for Artifacts and Libraries         |
| 🏠 **Hosted**                | Our Own Artifacts (We Upload)                       |
| 🪞 **Proxy**                 | Cache of a Remote Repository                        |
| 🧩 **Group**                 | One URL for Many Repositories                       |
| 📦 **Component**             | A Package With a Version                            |
| 📄 **Asset**                 | A File Inside a Component                           |
| 💾 **Blob Store**            | Where Files Are Stored                              |
| 🔢 **maven-releases**        | Final Versions (1.0.0)                              |
| 🚧 **maven-snapshots**       | Development Versions (-SNAPSHOT)                    |
| 🧩 **maven-public**          | Group URL Developers Use                            |
| 🚫 **Disable redeploy**      | Release Versions Cannot Be Overwritten              |
| 🧹 **Cleanup Policy**        | Auto-Delete Old Components                          |
| 🗜️ **Compact Blob Store**    | Really Free Disk Space                              |
| 🔑 **mvn deploy**            | Upload Artifact to Nexus                            |
| 🌐 **Port 8081**             | Default Nexus Web Port                              |

---

## 🗺️ Nexus Repository Learning Map

```text
                        📦 Nexus Repository
                                │
       ┌────────────────────────┼────────────────────────┐
       │                        │                        │
       ▼                        ▼                        ▼
    STORAGE                  REPOSITORIES              SECURITY
       │                        │                        │
       ├── Blob Stores          ├── Hosted               ├── Users
       ├── Cleanup Policies     ├── Proxy                ├── Roles
       └── Compact / Backup     └── Group                ├── Privileges
                                     │                   └── Anonymous access
                                     ▼
                                 FORMATS
                                     │
                                     ├── Maven
                                     ├── Docker
                                     ├── npm
                                     └── PyPI / Raw / more
       │
       ▼
   INTEGRATIONS
       │
       ├── Maven (mirror, deploy)
       ├── Jenkins (pipeline stage)
       ├── Docker registry
       └── npm / pip clients
```

---

## ⭐ Nexus Repository Final Memory

```text
Nexus Repository
 │
 ├── What is it?
 │      └── Artifact repository manager
 │
 ├── Where do we upload our own jars?
 │      └── Hosted repository (maven-releases / maven-snapshots)
 │
 ├── How to cache Maven Central?
 │      └── Proxy repository
 │
 ├── How to give developers one URL?
 │      └── Group repository (maven-public)
 │
 ├── How does Maven upload to Nexus?
 │      └── mvn deploy (distributionManagement + settings.xml)
 │
 ├── Default port?
 │      └── 8081
 │
 ├── How to stop overwriting a release?
 │      └── Disable redeploy
 │
 └── How to really free disk space?
        └── Compact blob store task
```

---

# 🐳 PART 7 — Docker — Containers

> **Docker = "It works on my machine" becomes "It works everywhere"**

---

## 7.1 🐳 What is Docker?

> **Docker = Platform to build, ship and run applications in containers**

Docker lets us **pack an application and everything it needs** (code, runtime, libraries, settings) into a single unit called a **container**.

A container **runs the same way everywhere** — on our laptop, on a test server and in the cloud.

#### 📦 Docker Is Used To

- 📦 **Package** applications with all dependencies
- 🚀 **Run** the same app on any machine
- ⚡ **Start** applications in seconds
- 🧪 Create **clean test environments**
- 🔁 Make CI/CD builds **repeatable**
- 🧩 Run many isolated apps on one server

#### 🏗️ Docker Basic Idea

```text
📄 Dockerfile  ──build──►  📦 Docker Image  ──run──►  🐳 Container
(recipe)                   (package / template)       (running application)
```

#### 🧠 Easy Memory

> **Docker = "It works on my machine" → "It works everywhere"**

---

## 7.2 🤔 Why Do We Use Docker?

### ❌ Without Docker

```text
👨‍💻 Developer: "It works on my laptop!"
        ↓
🖥️ Server has a different OS, Java version, libraries
        ↓
💥 Application fails after deployment
        ↓
😵 Hours of fixing the environment
```

### ✅ With Docker

```text
📦 App + runtime + libraries packed in one image
        ↓
🐳 Same image runs on laptop, test and production
        ↓
✅ Same result everywhere
```

#### ⭐ Main Reasons

- 🔁 **Consistency** — same environment everywhere
- ⚡ **Fast** — containers start in seconds
- 🪶 **Light** — share the host OS kernel, use less memory than VMs
- 🧩 **Isolation** — apps do not disturb each other
- 📈 **Easy scaling** — start more containers quickly
- 🤖 **CI/CD friendly** — build once, run anywhere
- 📦 Large library of ready images (Docker Hub)

---

## 7.3 🧰 What Does Docker Provide?

Docker provides:

- 📄 Dockerfile (build instructions)
- 📦 Images
- 🐳 Containers
- 🗄️ Registries (Docker Hub, private registries)
- 💾 Volumes (persistent data)
- 🌐 Networks
- 🧩 Docker Compose (multi-container apps)
- 🔒 Isolation using namespaces and cgroups

---

## 7.4 🆚 Containers vs Virtual Machines

```text
🖥️ Virtual Machines                     🐳 Containers
┌─────┐ ┌─────┐ ┌─────┐                 ┌─────┐ ┌─────┐ ┌─────┐
│ App │ │ App │ │ App │                 │ App │ │ App │ │ App │
│ Libs│ │ Libs│ │ Libs│                 │ Libs│ │ Libs│ │ Libs│
│Guest│ │Guest│ │Guest│                 └─────┘ └─────┘ └─────┘
│ OS  │ │ OS  │ │ OS  │                 ┌────────────────────┐
└─────┘ └─────┘ └─────┘                 │   Docker Engine    │
┌────────────────────┐                  └────────────────────┘
│    Hypervisor      │                  ┌────────────────────┐
└────────────────────┘                  │ Host Operating Sys │
┌────────────────────┐                  └────────────────────┘
│ Host Operating Sys │                  ┌────────────────────┐
└────────────────────┘                  │   Hardware         │
┌────────────────────┐                  └────────────────────┘
│   Hardware         │
└────────────────────┘
```

| Feature          | 🖥️ Virtual Machine                | 🐳 Container                         |
| ---------------- | --------------------------------- | ------------------------------------ |
| Operating system | Full **guest OS** in each VM      | **Shares the host kernel**           |
| Size             | Large (GBs)                       | Small (MBs)                          |
| Start time       | Minutes                           | Seconds                              |
| Resource use     | Heavy                             | Light                                |
| Isolation        | Strong (full OS)                  | Process-level isolation              |
| Best for         | Different OS, strong isolation    | Microservices, fast deployments      |

#### 🧠 Easy Memory

```text
🖥️ VM        = A whole house for each family
🐳 Container = A flat in one building (shared foundation)
```

---

## 7.5 🏛️ Docker Architecture

```text
🏛️ Docker Architecture
│
├── ⌨️ Docker Client (CLI)     → The `docker` command we type
├── ⚙️ Docker Daemon (dockerd) → Background service that builds and runs containers
├── 🗄️ Docker Registry         → Storage for images (Docker Hub, Nexus, ECR)
└── 📦 Objects                 → Images, Containers, Volumes, Networks
```

#### 🏗️ Flow

```text
⌨️ docker run nginx
      │ (talks to)
      ▼
⚙️ Docker Daemon
      │
      ├── 🔍 Image found locally?
      │       ├── ✅ Yes → Create and start the container
      │       └── ❌ No  → Pull from the 🗄️ Registry (Docker Hub), then run
      ▼
🐳 Running Container
```

### 7.5.1 📖 Simple Definitions

| Concept            | Simple Meaning                                                   |
| ------------------ | ---------------------------------------------------------------- |
| ⌨️ Docker Client   | The command line tool used to give commands                      |
| ⚙️ Docker Daemon   | The background service that does the real work                   |
| 📦 Image           | A **read-only template** used to create containers               |
| 🐳 Container       | A **running instance** of an image                               |
| 📄 Dockerfile      | A text file with **steps to build an image**                     |
| 🗄️ Registry        | A place to **store and share images**                            |
| 🏷️ Tag             | A version label of an image (`nginx:1.25`)                       |
| 💾 Volume          | Storage that **stays after the container is deleted**            |

#### 🧠 Remember

> **Image = Recipe result (template). Container = The dish being served (running).**

---

## 7.6 ⚙️ Installing Docker

### 7.6.1 🐧 Ubuntu (Using Docker's Install Script — Easy)

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

# Start and enable
sudo systemctl enable --now docker

# Check
docker --version
sudo docker run hello-world
```

### 7.6.2 👤 Run Docker Without sudo

```bash
sudo usermod -aG docker $USER
newgrp docker          # or log out and log in again
docker ps
```

#### ⚠️ Important

> Users in the **`docker` group** have almost **root-level power** on the machine. Give access carefully.

### 7.6.3 🪟 Docker Desktop

On **Windows and macOS**, install **Docker Desktop** (includes the engine and a GUI).

---

## 7.7 📦 Docker Images

An **image** is a **read-only package** that contains the OS files, application code, libraries and settings.

#### 🧱 Image Layers

Images are built in **layers**. Each Dockerfile instruction creates a layer.

```text
📦 Image: my-app
├── 🧱 Layer 4: CMD ["java", "-jar", "app.jar"]
├── 🧱 Layer 3: COPY app.jar /app/app.jar
├── 🧱 Layer 2: RUN install Java
└── 🧱 Layer 1: Base image (Ubuntu / Alpine)
```

#### ⭐ Why Layers Are Good

- ♻️ **Reuse** — layers are shared between images
- ⚡ **Cache** — unchanged layers are not rebuilt
- 📉 **Small downloads** — only new layers are downloaded

### 7.7.1 🏷️ Image Naming

```text
registry/repository:tag

docker.io/library/nginx:1.25
myuser/shop-app:1.0
nexus.example.com:8082/shop-app:1.0
```

| Part         | Meaning                                         |
| ------------ | ----------------------------------------------- |
| `registry`   | Where the image is stored (default Docker Hub)  |
| `repository` | Image name (`myuser/shop-app`)                  |
| `tag`        | Version (default is `latest`)                   |

#### ⚠️ Important

> **Avoid using the `latest` tag in production.** Use clear version tags (like `1.0.3`) so we know exactly what is running.

### 7.7.2 ⌨️ Image Commands

```bash
docker pull nginx:1.25          # Download an image
docker images                   # List local images
docker rmi nginx:1.25           # Remove an image
docker image prune              # Remove unused images
docker tag shop-app:1.0 myuser/shop-app:1.0   # Add a new name/tag
docker push myuser/shop-app:1.0 # Upload to a registry
docker history shop-app:1.0     # Show layers
docker inspect shop-app:1.0     # Detailed information
```

---

## 7.8 🐳 Docker Containers

A **container** is a **running instance of an image**.

### 7.8.1 🔄 Container Life Cycle

```text
📦 Image
   │ docker create
   ▼
🆕 Created ──docker start──► ▶️ Running ──docker stop──► ⏹️ Stopped
                                │  ▲                          │
                          pause │  │ unpause                  │ docker rm
                                ▼  │                          ▼
                             ⏸️ Paused                   🗑️ Removed
```

### 7.8.2 ⌨️ Container Commands

```bash
# Run a container
docker run nginx                              # Run in the foreground
docker run -d nginx                           # Run in the background (detached)
docker run -d --name web -p 8080:80 nginx     # Name + port mapping
docker run -it ubuntu bash                    # Interactive terminal
docker run --rm alpine echo "hi"              # Remove container after it exits

# See containers
docker ps                                     # Running containers
docker ps -a                                  # All containers

# Control containers
docker stop web
docker start web
docker restart web
docker rm web                                 # Remove a stopped container
docker rm -f web                              # Force remove

# Work inside containers
docker logs web                               # See logs
docker logs -f web                            # Follow logs live
docker exec -it web bash                      # Open a shell in a running container
docker inspect web                            # Detailed information
docker stats                                  # CPU / memory usage
docker cp web:/etc/nginx/nginx.conf .         # Copy files from a container
```

### 7.8.3 🚩 Important `docker run` Options

| Option                     | Meaning                                              |
| -------------------------- | ---------------------------------------------------- |
| `-d`                       | Run in the background (detached)                     |
| `-it`                      | Interactive terminal                                 |
| `--name`                   | Give the container a name                            |
| `-p host:container`        | Map a port (`-p 8080:80`)                            |
| `-v host:container`        | Mount a volume or folder                             |
| `-e KEY=value`             | Set an environment variable                          |
| `--rm`                     | Delete the container when it stops                   |
| `--restart unless-stopped` | Restart automatically after a reboot or crash        |
| `--network`                | Connect to a specific network                        |
| `--memory`, `--cpus`       | Limit memory and CPU                                 |

#### 🌐 Port Mapping Explained

```text
docker run -d -p 8080:80 nginx
                 │    │
                 │    └── Port inside the container
                 └─────── Port on the host (our server)

🌍 http://server-ip:8080  ──►  🐳 container port 80
```

---

## 7.9 📄 Dockerfile

A **Dockerfile** is a **text file with instructions** to build an image.

### 7.9.1 🧱 Important Instructions

| Instruction   | Meaning                                                               |
| ------------- | --------------------------------------------------------------------- |
| `FROM`        | **Base image** to start from (required first line)                    |
| `WORKDIR`     | Set the working folder inside the image                               |
| `COPY`        | Copy files from our computer into the image                           |
| `ADD`         | Like COPY, plus can download URLs and extract tar files               |
| `RUN`         | Run a command **while building** the image (creates a layer)          |
| `ENV`         | Set an environment variable                                           |
| `ARG`         | Build-time variable                                                   |
| `EXPOSE`      | Document the port the app uses                                        |
| `USER`        | Run as a specific (non-root) user                                     |
| `VOLUME`      | Create a mount point                                                  |
| `CMD`         | Default command when the container **starts** (can be overridden)     |
| `ENTRYPOINT`  | Main command that always runs (harder to override)                    |
| `HEALTHCHECK` | Command to check if the container is healthy                          |

### 7.9.2 💻 Example 1: Java Spring Boot App

```dockerfile
FROM eclipse-temurin:17-jre
WORKDIR /app
COPY target/shop-app-1.0.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]
```

### 7.9.3 🐍 Example 2: Python Flask App

```dockerfile
FROM python:3.12-slim
WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .
EXPOSE 5000
CMD ["python", "app.py"]
```

### 7.9.4 🔨 Build and Run

```bash
docker build -t shop-app:1.0 .          # Build (the dot = current folder)
docker run -d -p 8080:8080 shop-app:1.0
```

### 7.9.5 ⚖️ CMD vs ENTRYPOINT

| 🎯 CMD                                  | 🚪 ENTRYPOINT                              |
| --------------------------------------- | ------------------------------------------ |
| Default command / arguments             | The fixed main program                     |
| Easily replaced: `docker run img cmd`   | Replaced only with `--entrypoint`          |
| Good for flexible images                | Good for apps that always run one program  |

```text
ENTRYPOINT ["java", "-jar", "app.jar"]   → Always runs the app
CMD ["--spring.profiles.active=prod"]    → Default arguments (can change)
```

### 7.9.6 ⚖️ COPY vs ADD

> **Prefer `COPY`.** Use `ADD` only when we need its extra features (like auto-extract).

### 7.9.7 🙈 .dockerignore

Lists files **not to send** to the build.

```text
target/
.git
node_modules
*.log
.env
```

---

## 7.10 🏗️ Multi-Stage Builds

A **multi-stage build** uses **many `FROM` steps** so the **final image is small** (no build tools inside).

```dockerfile
# Stage 1: Build the app with Maven
FROM maven:3.9-eclipse-temurin-17 AS build
WORKDIR /src
COPY pom.xml .
COPY src ./src
RUN mvn -B clean package -DskipTests

# Stage 2: Run the app with a small runtime image
FROM eclipse-temurin:17-jre
WORKDIR /app
COPY --from=build /src/target/*.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]
```

```text
🏗️ Stage 1 (Build)  : Maven + JDK + source code   → creates app.jar
        │ copy only app.jar
        ▼
📦 Stage 2 (Runtime): JRE + app.jar               → small final image
```

#### ⭐ Benefits

- 📉 **Much smaller** image
- 🔒 **More secure** (no compilers or source in the final image)
- 🧼 Clean and simple

---

## 7.11 🗄️ Docker Registry

A **registry** stores and distributes images.

```text
🗄️ Registries
│
├── 🌍 Docker Hub          → Public default registry
├── ☁️ AWS ECR             → Amazon's private registry
├── 📦 Nexus Repository    → Our own private registry
└── 🐙 GitHub Container Registry (ghcr.io)
```

#### 💻 Push to Docker Hub

```bash
docker login
docker tag shop-app:1.0 myuser/shop-app:1.0
docker push myuser/shop-app:1.0
docker pull myuser/shop-app:1.0
```

#### 💡 Tip

> In CI, log in with `docker login -u USER --password-stdin` and store the password in **Jenkins Credentials**.

---

## 7.12 💾 Docker Volumes

A container's data is **deleted when the container is removed**. **Volumes** keep data **safe outside the container**.

```text
💾 Storage Options
│
├── 💾 Volume      → Managed by Docker (recommended)
├── 📁 Bind Mount  → A folder from the host (good for development)
└── 🧠 tmpfs       → Stored in memory only (temporary)
```

#### 💻 Commands

```bash
docker volume create mydata
docker run -d --name db -v mydata:/var/lib/mysql mysql:8      # Named volume
docker run -d -v $(pwd)/html:/usr/share/nginx/html nginx      # Bind mount
docker volume ls
docker volume inspect mydata
docker volume rm mydata
```

```text
🐳 Container (deleted)           💾 Volume "mydata" (data stays safe)
        │                                ▲
        └──── mounted at /var/lib/mysql ─┘
```

#### 🧠 Remember

> **Containers are temporary. Volumes are permanent.**

---

## 7.13 🌐 Docker Networking

Containers talk to each other and to the outside using **networks**.

```text
🌐 Network Drivers
│
├── 🌉 bridge   → Default. Private network on one host
├── 🏠 host     → Container shares the host's network
├── 🚫 none     → No network
└── 🌍 overlay  → Network across many hosts (Swarm)
```

#### 💻 Commands

```bash
docker network ls
docker network create mynet
docker run -d --name db  --network mynet mysql:8
docker run -d --name app --network mynet myapp
# Inside "app", we can reach the database using the name "db"
```

#### ⭐ Key Points

- 🏷️ On a **user-created bridge network**, containers find each other **by name** (built-in DNS)
- 🌐 Use `-p` to expose a port to the outside world
- 🔒 Containers on different networks cannot talk unless connected

---

## 7.14 🧩 Docker Compose

**Docker Compose** runs **multi-container applications** using one **YAML file** (`docker-compose.yml` or `compose.yaml`).

#### 💻 Example: Web App + Database

```yaml
services:
  web:
    build: .
    ports:
      - "8080:8080"
    environment:
      DB_HOST: db
      DB_USER: app
      DB_PASSWORD: app_password
    depends_on:
      - db
    restart: unless-stopped

  db:
    image: mysql:8
    environment:
      MYSQL_ROOT_PASSWORD: root_password
      MYSQL_DATABASE: shop
      MYSQL_USER: app
      MYSQL_PASSWORD: app_password
    volumes:
      - db_data:/var/lib/mysql

volumes:
  db_data:
```

#### ⌨️ Commands

```bash
docker compose up -d           # Create and start everything
docker compose ps              # List services
docker compose logs -f         # See logs
docker compose down            # Stop and remove containers
docker compose down -v         # Also remove volumes
docker compose build           # Build images
```

#### 🧠 Simple Meaning

> **Compose = One file, one command, whole application running**

---

## 7.15 🔒 Docker Security

```text
🔒 Docker Security Best Practices
│
├── 👤 Do not run as root → use USER in the Dockerfile
├── 📦 Use small, trusted base images (alpine, slim, distroless)
├── 🏷️ Use fixed image versions (no :latest)
├── 🔍 Scan images for vulnerabilities (docker scout, Trivy)
├── 🔑 Never put secrets inside images
├── 🧱 Use multi-stage builds
├── 📉 Limit resources (--memory, --cpus)
└── 🚫 Do not run containers with --privileged unless required
```

#### 💻 Non-Root User Example

```dockerfile
FROM eclipse-temurin:17-jre
RUN useradd -r -u 1001 appuser
USER appuser
WORKDIR /app
COPY --chown=appuser target/app.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]
```

#### ⚠️ Important

> **Never store passwords or API keys in a Dockerfile or image.** Pass them at runtime (environment variables, secrets, or Kubernetes Secrets).

---

## 7.16 🧹 Cleanup Commands

```bash
docker system df               # Disk usage of Docker
docker container prune         # Remove stopped containers
docker image prune -a          # Remove unused images
docker volume prune            # Remove unused volumes
docker system prune            # Remove unused containers, networks, images
```

> ⚠️ Be careful with `prune` commands on servers that hold important data.

---

## 7.17 ⚡ Docker Best Practices

```text
✅ Docker Best Practices
│
├── 🪶 Use small base images
├── 🧱 Use multi-stage builds
├── ⚡ Order Dockerfile steps so cache is used (copy dependency files first)
├── 🙈 Use .dockerignore
├── 🏷️ Tag images with versions
├── 👤 Run as a non-root user
├── 1️⃣ One main process per container
├── 💾 Keep data in volumes
└── 📝 Write logs to stdout/stderr
```

---

## 7.18 🔗 Docker in a CI/CD Pipeline

```text
🤖 Jenkins
   │
   ├── 🔨 mvn clean package          → app.jar
   ├── 🐳 docker build -t shop-app:42 .
   ├── 🗄️ docker push to Nexus / Docker Hub / ECR
   └── ☸️ kubectl set image ...      → Deploy to Kubernetes
```

#### 💻 Jenkins Stage

```groovy
stage('Docker Build and Push') {
    steps {
        sh "docker build -t myuser/shop-app:${env.BUILD_NUMBER} ."
        withCredentials([usernamePassword(credentialsId: 'dockerhub-creds',
                usernameVariable: 'USER', passwordVariable: 'PASS')]) {
            sh 'echo $PASS | docker login -u $USER --password-stdin'
            sh "docker push myuser/shop-app:${env.BUILD_NUMBER}"
        }
    }
}
```

---

## 7.19 🏗️ Real Example: Containerize a Java App

### 🎯 Requirement

Run a Spring Boot application as a container and push the image to a registry.

### 🪜 Steps

```bash
# 1. Build the jar
mvn clean package

# 2. Create the Dockerfile (see below)

# 3. Build the image
docker build -t shop-app:1.0 .

# 4. Run it
docker run -d --name shop -p 8080:8080 shop-app:1.0

# 5. Test
curl http://localhost:8080

# 6. Check logs
docker logs -f shop

# 7. Push to a registry
docker tag shop-app:1.0 myuser/shop-app:1.0
docker login
docker push myuser/shop-app:1.0
```

#### 📄 Dockerfile

```dockerfile
FROM eclipse-temurin:17-jre
WORKDIR /app
COPY target/shop-app-1.0.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]
```

### 🏗️ Flow

```text
💻 Source code
      │ mvn package
      ▼
📦 app.jar
      │ docker build
      ▼
📦 Docker Image  ──docker push──►  🗄️ Registry
      │                                │ docker pull
      │ docker run                     ▼
      ▼                           🖥️ Any server / ☸️ Kubernetes
🐳 Running Container
```

---

## 📌🧠 Docker Quick Revision

```text
🐳 Docker
│
├── 🏛️ Architecture
│   ├── Client (docker CLI)
│   ├── Daemon (dockerd)
│   └── Registry
│
├── 📦 Core Objects
│   ├── Image (read-only template, layers)
│   ├── Container (running image)
│   ├── Volume (persistent data)
│   └── Network
│
├── 📄 Dockerfile
│   ├── FROM, WORKDIR, COPY, RUN
│   ├── ENV, EXPOSE, USER
│   ├── CMD vs ENTRYPOINT
│   └── Multi-stage builds
│
├── 🗄️ Registries
│   ├── Docker Hub
│   ├── Nexus / ECR / GHCR
│   └── docker tag + docker push
│
├── 🧩 Docker Compose
│   └── docker compose up -d
│
└── 🔒 Best Practices
    ├── Non-root user
    ├── Small images, fixed tags
    └── Scan images, no secrets
```

---

## 🧠⚡ Docker One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| 🐳 **Docker**              | Package and Run Apps in Containers                  |
| 📦 **Image**               | Read-Only Template (Recipe Result)                  |
| 🐳 **Container**           | Running Instance of an Image                        |
| 📄 **Dockerfile**          | Steps to Build an Image                             |
| 🗄️ **Registry**            | Storage for Images (Docker Hub, Nexus, ECR)         |
| 🏷️ **Tag**                 | Version Label (Avoid :latest in Production)         |
| 🧱 **Layer**               | One Step of an Image (Cached and Reused)            |
| 💾 **Volume**              | Permanent Storage Outside the Container             |
| 🌉 **Bridge Network**      | Default Private Network, Containers Use Names       |
| 🔌 **-p 8080:80**          | Host Port : Container Port                          |
| 🧩 **Docker Compose**      | Run Many Containers With One File                   |
| 🏗️ **Multi-stage Build**   | Small Final Image Without Build Tools               |
| 🎯 **CMD**                 | Default Command (Easy to Override)                  |
| 🚪 **ENTRYPOINT**          | Main Program (Always Runs)                          |
| 🙈 **.dockerignore**       | Files Not Sent to the Build                         |
| 🐚 **docker exec -it**     | Open a Shell Inside a Running Container             |

---

## 🗺️ Docker Learning Map

```text
                            🐳 Docker
                                │
       ┌────────────────────────┼────────────────────────┐
       │                        │                        │
       ▼                        ▼                        ▼
     BUILD                     RUN                     SHARE
       │                        │                        │
       ├── Dockerfile           ├── Containers           ├── Registry
       ├── Layers               │    ├── run / stop      │    ├── Docker Hub
       ├── Multi-stage          │    ├── exec / logs     │    ├── Nexus
       └── .dockerignore        │    └── ports (-p)      │    └── ECR
                                ├── Volumes              └── tag + push / pull
                                └── Networks
       │
       ▼
   MULTI-CONTAINER
       │
       └── Docker Compose
       │
       ▼
   SECURITY & CI/CD
       │
       ├── Non-root, scanning
       ├── No secrets in images
       └── Jenkins build + push → Kubernetes
```

---

## ⭐ Docker Final Memory

```text
Docker
 │
 ├── What is it?
 │      └── Containerization platform
 │
 ├── Image vs Container?
 │      └── Image = template, Container = running instance
 │
 ├── How do we build an image?
 │      └── Dockerfile + docker build
 │
 ├── How to expose a port?
 │      └── docker run -p host:container
 │
 ├── How to keep data after deleting a container?
 │      └── Volumes
 │
 ├── How to run many containers together?
 │      └── Docker Compose
 │
 ├── How to make the image small?
 │      └── Multi-stage build + small base image
 │
 └── How to enter a running container?
        └── docker exec -it <name> bash
```

---

# 🏗️ PART 8 — Terraform — Infrastructure as Code

> **Terraform = Write infrastructure as code, run one command, cloud resources are created**

---

## 8.1 🏗️ What is Terraform?

> **Terraform = Infrastructure as Code (IaC) tool to create and manage cloud infrastructure**

Terraform (by **HashiCorp**) lets us **describe our infrastructure in code files**, and then it **creates, changes and deletes** servers, networks, databases and more — on **AWS, Azure, Google Cloud, Kubernetes and many other platforms**.

We write **what we want**, and Terraform figures out **how to do it**.

#### 📦 Terraform Can Create

- 🖥️ Servers (EC2)
- 🌐 Networks (VPC, Subnets)
- 🪣 Storage (S3)
- 🗄️ Databases (RDS)
- ☸️ Kubernetes clusters (EKS)
- 🔐 IAM roles and policies
- …almost anything that has an API

#### 🏗️ Terraform Basic Idea

```text
📝 Terraform code (.tf files)
        │
        ▼
🏗️ Terraform
        │  talks to cloud APIs using Providers
        ▼
☁️ AWS / Azure / GCP / Kubernetes ...
        │
        ▼
🖥️ Real infrastructure (EC2, VPC, S3 ...)
```

#### 🧠 Easy Memory

> **Terraform = Write infrastructure as code, run one command, cloud resources are created**

---

## 8.2 🤔 Why Do We Use Terraform?

### ❌ Manual Setup (Console Clicking)

```text
🖱️ Click, click, click in the cloud console
        ↓
😵 Hard to remember and repeat
        ↓
🐛 Mistakes and "configuration drift"
        ↓
🔁 Different dev, test and prod environments
```

### ✅ With Terraform

```text
📝 Write code once
        ↓
👀 terraform plan   → See what will change
        ↓
🚀 terraform apply  → Create everything
        ↓
🔁 Repeat for dev, test and prod using the same code
```

#### ⭐ Main Reasons

- 🔁 **Repeatable** — same code, same result
- 📝 **Version control** — store code in Git
- 👀 **Preview changes** before applying (`plan`)
- 🌍 **Multi-cloud** — one tool for many providers
- ⚡ **Fast** — build full environments in minutes
- 🧹 **Easy cleanup** — `terraform destroy`
- 🤝 **Teamwork** — review infrastructure changes like code (Pull Requests)

---

## 8.3 🧰 What Does Terraform Provide?

Terraform provides:

- 🔌 Providers (plugins for each platform)
- 🧩 Resources and Data Sources
- 🎛️ Variables, Outputs and Locals
- 📚 Modules (reusable code)
- 📄 State Management
- 🗄️ Remote Backends
- 🌿 Workspaces
- 🔄 Plan / Apply / Destroy workflow
- 🧮 Built-in Functions and Expressions

---

## 8.4 🆚 Declarative vs Imperative

```text
📋 Declarative (Terraform)           💻 Imperative (Scripts)
"I want 3 servers."                  "Create server 1. Create server 2. Create server 3."
Terraform decides the steps.         We write every step.
```

| 📋 Declarative                           | 💻 Imperative                             |
| ---------------------------------------- | ----------------------------------------- |
| Describe the **end result**              | Describe the **steps**                    |
| Tool finds the difference and fixes it   | We handle every condition ourselves       |
| Safe to run again (**idempotent**)       | Running again may create duplicates       |

> **Idempotent = Running the same code many times gives the same result.**

---

## 8.5 ⚙️ Installing Terraform

```bash
# Ubuntu / Debian (HashiCorp repository)
sudo apt update && sudo apt install -y gnupg software-properties-common curl
curl -fsSL https://apt.releases.hashicorp.com/gpg | \
  sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
  sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform -y

# Check
terraform -version
```

> 💡 Always follow the **official HashiCorp install page** for the latest steps. On macOS: `brew install terraform`. On Windows: use the installer or `choco install terraform`.

#### 🔑 AWS Credentials

Terraform needs permission to create AWS resources.

```text
🔑 Ways to Give AWS Access
│
├── 🎭 IAM Role on the machine (EC2 / Jenkins agent)  → Best
├── ⌨️ aws configure (stores keys in ~/.aws/credentials)
└── 🌍 Environment variables
        export AWS_ACCESS_KEY_ID=...
        export AWS_SECRET_ACCESS_KEY=...
        export AWS_DEFAULT_REGION=ap-south-1
```

#### ⚠️ Important

> **Never write AWS keys inside `.tf` files or commit them to Git.**

#### 🏛️ Note: OpenTofu

> **OpenTofu** is an **open-source fork of Terraform** (managed by the Linux Foundation). Commands and code are very similar (`tofu` instead of `terraform`). Terraform's license changed to BSL in 2023, so some teams choose OpenTofu.

---

## 8.6 🧱 Terraform Basic Concepts

```text
🏗️ Terraform
│
├── 🔌 Provider      → Plugin to talk to a platform (aws, azurerm, kubernetes)
├── 🧩 Resource      → An infrastructure object to create (EC2, S3 bucket)
├── 🔍 Data Source   → Read information that already exists
├── 🎛️ Variable      → Input value
├── 📤 Output        → Value shown after apply
├── 📚 Module        → Reusable group of resources
├── 📄 State         → Terraform's record of what it created
└── 🗄️ Backend       → Where the state is stored
```

### 8.6.1 📖 Simple Definitions

| Concept           | Simple Meaning                                                      |
| ----------------- | ------------------------------------------------------------------- |
| 🔌 **Provider**   | Plugin that lets Terraform work with AWS, Azure, GCP, etc.          |
| 🧩 **Resource**   | One thing we want to create (an EC2 instance, a bucket)             |
| 🔍 **Data Source**| Reads existing data (like the latest AMI ID)                        |
| 🎛️ **Variable**   | An input so the same code can be reused                             |
| 📤 **Output**     | A value we want to see (like the server's public IP)                |
| 🧮 **Locals**     | Named values used inside the code (like temporary variables)        |
| 📚 **Module**     | A folder of Terraform code that we can reuse                        |
| 📄 **State**      | A file that maps our code to the real resources                     |
| 🗄️ **Backend**    | Place where the state file is stored (local, S3 ...)                |

---

## 8.7 📝 Terraform Language (HCL)

Terraform uses **HCL = HashiCorp Configuration Language**.

### 8.7.1 🧱 Basic Block Structure

```hcl
<BLOCK TYPE> "<LABEL 1>" "<LABEL 2>" {
  argument = value
}
```

#### 💻 Example

```hcl
resource "aws_s3_bucket" "my_bucket" {
  bucket = "my-unique-bucket-name-12345"
}
```

```text
resource          → Block type
"aws_s3_bucket"   → Resource type (what to create)
"my_bucket"       → Name inside Terraform (our own name)
bucket = "..."    → Argument (setting)
```

### 8.7.2 🔗 Referencing Other Resources

```hcl
resource "aws_s3_bucket_versioning" "v" {
  bucket = aws_s3_bucket.my_bucket.id       # <type>.<name>.<attribute>

  versioning_configuration {
    status = "Enabled"
  }
}
```

> Terraform sees this link and **creates the bucket first**, then versioning (**implicit dependency**).

### 8.7.3 🔠 Data Types

| Type      | Example                                   |
| --------- | ----------------------------------------- |
| `string`  | `"t3.micro"`                              |
| `number`  | `3`                                       |
| `bool`    | `true`                                    |
| `list`    | `["a", "b", "c"]`                         |
| `map`     | `{ env = "dev", team = "ops" }`           |
| `object`  | Structured group of values                |

### 8.7.4 💬 Comments

```hcl
# Single-line comment
// Also a single-line comment
/* Multi-line
   comment */
```

---

## 8.8 📂 Terraform File Structure

```text
📁 my-infra/
├── 📄 main.tf            → Main resources
├── 📄 providers.tf       → Provider and Terraform settings
├── 📄 variables.tf       → Input variable definitions
├── 📄 outputs.tf         → Output definitions
├── 📄 terraform.tfvars   → Values for the variables
├── 📄 .terraform.lock.hcl → Provider version lock (commit to Git)
├── 📁 .terraform/        → Downloaded plugins (do NOT commit)
├── 📄 terraform.tfstate  → State file (do NOT commit if local)
└── 📁 modules/           → Our own reusable modules
```

> Terraform reads **all `.tf` files in the folder together**. The file names are only for our organization.

#### 🙈 .gitignore for Terraform

```text
.terraform/
*.tfstate
*.tfstate.*
*.tfvars
crash.log
```

---

## 8.9 🔌 Providers

A **provider** is a **plugin** that lets Terraform manage a platform.

```hcl
terraform {
  required_version = ">= 1.5.0"

  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
  region = "ap-south-1"
}
```

#### 📖 Understanding It

```text
required_providers → Which providers and versions are needed
source             → Where to download the provider (registry.terraform.io)
version "~> 5.0"   → Any 5.x version (but not 6.0)
provider "aws"     → Configuration of the provider (region)
```

#### 🔢 Version Constraints

| Constraint     | Meaning                                  |
| -------------- | ---------------------------------------- |
| `= 5.1.0`      | Exactly this version                     |
| `>= 5.0`       | This version or newer                    |
| `~> 5.0`       | Any 5.x (>= 5.0 and < 6.0)               |
| `~> 5.1.0`     | Any 5.1.x (>= 5.1.0 and < 5.2.0)         |

#### 🔒 Lock File

`.terraform.lock.hcl` **records the exact provider versions** used. **Commit it to Git** so the team uses the same versions.

---

## 8.10 🔄 Terraform Workflow

```text
🔄 Terraform Workflow
│
├── 1️⃣ Write   → Create .tf files
├── 2️⃣ Init    → terraform init      (download providers, set backend)
├── 3️⃣ Plan    → terraform plan      (preview changes)
├── 4️⃣ Apply   → terraform apply     (create / change resources)
└── 5️⃣ Destroy → terraform destroy   (delete everything)
```

#### 🏗️ Flow Diagram

```text
📝 Write code
     │
     ▼
⚙️ terraform init       → Downloads provider plugins
     │
     ▼
👀 terraform plan       → Shows: + create, ~ change, - destroy
     │
     ▼
🚀 terraform apply      → Creates real resources + updates the state file
     │
     ▼
🧹 terraform destroy    → Removes everything (when not needed)
```

### 8.10.1 ⌨️ Main Commands

| Command                        | What It Does                                              |
| ------------------------------ | --------------------------------------------------------- |
| `terraform init`               | Prepare the folder: download providers, configure backend |
| `terraform validate`           | Check the syntax of the code                              |
| `terraform fmt`                | Format code in the standard style                         |
| `terraform plan`               | Show what Terraform will do (no changes made)             |
| `terraform apply`              | Create or update resources (asks for `yes`)               |
| `terraform apply -auto-approve`| Apply without asking (used in pipelines)                  |
| `terraform destroy`            | Delete all managed resources                              |
| `terraform show`               | Show the current state in readable form                   |
| `terraform output`             | Show output values                                        |
| `terraform state list`         | List resources in the state                               |
| `terraform import`             | Bring an existing resource under Terraform control        |
| `terraform workspace ...`      | Manage workspaces                                         |

### 8.10.2 👀 Reading the Plan

```text
  + create       → A new resource will be created
  ~ update       → A resource will be changed in place
  - destroy      → A resource will be deleted
  -/+ replace    → A resource will be destroyed and created again
```

#### 💻 Example Output

```text
Plan: 2 to add, 1 to change, 0 to destroy.
```

#### ⚠️ Important

> **Always read the `plan` carefully** — especially `destroy` and `replace` (they can delete data).

---

## 8.11 🎛️ Variables

**Variables** make code reusable.

### 8.11.1 📥 Input Variables

```hcl
# variables.tf
variable "instance_type" {
  description = "EC2 instance type"
  type        = string
  default     = "t3.micro"
}

variable "environment" {
  description = "Environment name"
  type        = string
}

variable "allowed_ports" {
  type    = list(number)
  default = [22, 80, 443]
}

variable "db_password" {
  type      = string
  sensitive = true          # Hidden in plan/apply output
}
```

#### 💻 Use a Variable

```hcl
resource "aws_instance" "web" {
  instance_type = var.instance_type
  tags = {
    Environment = var.environment
  }
}
```

### 8.11.2 🔢 Ways to Provide Values (Order of Priority, Low → High)

```text
1. 🧱 default value in the variable block
2. 📄 terraform.tfvars  (or *.auto.tfvars)
3. 📄 -var-file="prod.tfvars"
4. ⌨️ -var="environment=prod"
5. 🌍 Environment variable:  TF_VAR_environment=prod
```

> Later methods in the list **override** earlier ones (command line `-var` wins over files).

#### 💻 terraform.tfvars

```hcl
environment   = "dev"
instance_type = "t3.micro"
```

#### ⌨️ Command Line

```bash
terraform apply -var="environment=prod" -var-file="prod.tfvars"
```

### 8.11.3 📤 Output Values

```hcl
# outputs.tf
output "instance_public_ip" {
  description = "Public IP of the web server"
  value       = aws_instance.web.public_ip
}

output "db_endpoint" {
  value     = aws_db_instance.main.endpoint
  sensitive = true
}
```

```bash
terraform output
terraform output instance_public_ip
```

### 8.11.4 🧮 Locals

```hcl
locals {
  name_prefix = "${var.environment}-shop"
  common_tags = {
    Project     = "shop"
    Environment = var.environment
    ManagedBy   = "terraform"
  }
}

resource "aws_s3_bucket" "logs" {
  bucket = "${local.name_prefix}-logs"
  tags   = local.common_tags
}
```

#### 🧠 Easy Memory

```text
variable = Input from outside
local    = Value calculated inside
output   = Value shown to the outside
```

---

## 8.12 🔍 Data Sources

A **data source** **reads information** that already exists (not created by this code).

```hcl
# Find the latest Amazon Linux 2023 AMI
data "aws_ami" "al2023" {
  most_recent = true
  owners      = ["amazon"]

  filter {
    name   = "name"
    values = ["al2023-ami-2023*-x86_64"]
  }
}

resource "aws_instance" "web" {
  ami           = data.aws_ami.al2023.id     # data.<type>.<name>.<attribute>
  instance_type = "t3.micro"
}
```

#### 🧠 Resource vs Data Source

| 🧩 Resource                        | 🔍 Data Source                         |
| ---------------------------------- | -------------------------------------- |
| **Creates** and manages things     | **Reads** existing things              |
| `resource "aws_..." "name"`        | `data "aws_..." "name"`                |
| Terraform owns it                  | Terraform only looks at it             |

---

## 8.13 📄 Terraform State

Terraform keeps a **state file (`terraform.tfstate`)** that records **which real resources belong to our code**.

```text
📝 Code  ◄──────────── compare ───────────►  📄 State  ◄──── map ────►  ☁️ Real Resources
(what we want)                               (what Terraform knows)      (what exists)
```

#### 🎯 Why State Is Needed

- 🗺️ Maps **code → real resource IDs**
- 🔍 Lets Terraform **compare** and find what to change
- ⚡ Improves performance for big setups

#### ⚠️ Important

> **State may contain secrets** (like passwords). **Never commit it to Git.** Store it in a **secure remote backend**.

### 8.13.1 🗄️ Remote Backend (Team Use)

For teams, store state **remotely** with **locking**.

```hcl
terraform {
  backend "s3" {
    bucket         = "my-terraform-state-bucket"
    key            = "shop/prod/terraform.tfstate"
    region         = "ap-south-1"
    encrypt        = true
    dynamodb_table = "terraform-locks"      # State locking
  }
}
```

```text
🗄️ Remote Backend Benefits
│
├── 🤝 Whole team shares one state
├── 🔒 State locking (no two applies at the same time)
├── 🔐 Encryption and access control
└── 💾 Versioning and backup (S3 versioning)
```

> 💡 Newer Terraform versions can also use **S3 native state locking** (a lock file in S3) instead of DynamoDB. Check the current Terraform documentation for the recommended setting.

### 8.13.2 ⌨️ State Commands

```bash
terraform state list                         # List resources
terraform state show aws_instance.web        # Details of one resource
terraform state rm aws_instance.web          # Stop managing a resource (does not delete it)
terraform state mv old_name new_name         # Rename in the state
terraform refresh                            # (older) Update state from real resources
terraform plan -refresh-only                 # Safe way to detect drift
```

### 8.13.3 📥 Import Existing Resources

```bash
terraform import aws_instance.web i-0123456789abcdef0
```

> **Import = Bring an existing, manually created resource under Terraform.** (Newer Terraform versions also support `import` blocks in code.)

---

## 8.14 🔁 Meta-Arguments

Special arguments available on **most resources**.

```text
🔁 Meta-Arguments
│
├── 🔢 count        → Create many copies of a resource
├── 🔁 for_each     → Create resources from a list / map
├── 🔗 depends_on   → Force an explicit dependency
├── 🏷️ provider     → Use a specific provider configuration
└── 🛡️ lifecycle    → Control create / update / destroy behavior
```

### 8.14.1 🔢 count

```hcl
resource "aws_instance" "web" {
  count         = 3
  ami           = data.aws_ami.al2023.id
  instance_type = "t3.micro"

  tags = {
    Name = "web-${count.index}"      # web-0, web-1, web-2
  }
}
```

### 8.14.2 🔁 for_each

```hcl
variable "buckets" {
  default = ["logs", "images", "backups"]
}

resource "aws_s3_bucket" "b" {
  for_each = toset(var.buckets)
  bucket   = "myapp-${each.key}-12345"
}
```

#### ⚖️ count vs for_each

| 🔢 count                              | 🔁 for_each                              |
| ------------------------------------- | ---------------------------------------- |
| Uses a number                         | Uses a list, set or map                  |
| Resources identified by **index** (0,1,2) | Identified by **key** (name)         |
| Removing one in the middle shifts others | Removing one affects only that one    |
| Good for identical copies             | **Better for different items**           |

### 8.14.3 🛡️ lifecycle

```hcl
resource "aws_instance" "web" {
  # ...
  lifecycle {
    create_before_destroy = true      # Create new before destroying old
    prevent_destroy       = true      # Block accidental destroy
    ignore_changes        = [tags]    # Ignore changes made outside Terraform
  }
}
```

### 8.14.4 🔗 depends_on

```hcl
resource "aws_instance" "app" {
  # ...
  depends_on = [aws_db_instance.main]    # Create the database first
}
```

> Terraform finds most dependencies **automatically** from references. Use `depends_on` only when the link is not visible in the code.

---

## 8.15 📚 Modules

A **module** is a **folder of Terraform code** that we can **reuse**.

```text
📁 project/
├── 📄 main.tf                  ← Root module (calls the modules)
└── 📁 modules/
    ├── 📁 vpc/                 ← Child module
    │   ├── main.tf
    │   ├── variables.tf
    │   └── outputs.tf
    └── 📁 ec2/
        ├── main.tf
        ├── variables.tf
        └── outputs.tf
```

#### 💻 Use a Module

```hcl
module "network" {
  source     = "./modules/vpc"
  cidr_block = "10.0.0.0/16"
  env        = var.environment
}

module "web" {
  source    = "./modules/ec2"
  subnet_id = module.network.public_subnet_id     # Use another module's output
}
```

#### 🌍 Public Modules

We can use ready modules from the **Terraform Registry**.

```hcl
module "vpc" {
  source  = "terraform-aws-modules/vpc/aws"
  version = "~> 5.0"

  name = "my-vpc"
  cidr = "10.0.0.0/16"
}
```

#### 🧠 Simple Meaning

> **Module = A reusable package of infrastructure code (like a function)**

---

## 8.16 🌿 Workspaces

**Workspaces** let us keep **separate states** for **the same code** (like dev, test, prod).

```bash
terraform workspace list
terraform workspace new dev
terraform workspace select prod
terraform workspace show
```

```hcl
# Use the workspace name inside code
resource "aws_s3_bucket" "b" {
  bucket = "myapp-${terraform.workspace}-bucket"
}
```

#### ⚠️ Important

> Many teams prefer **separate folders / state files per environment** for production because workspaces share the same backend and code.

---

## 8.17 🧮 Expressions and Functions

### 8.17.1 🧮 Useful Functions

| Function              | Example                               | Meaning                          |
| --------------------- | ------------------------------------- | -------------------------------- |
| `length()`            | `length(var.list)`                    | Number of items                  |
| `join()`              | `join("-", ["a","b"])`                | `"a-b"`                          |
| `lower()` / `upper()` | `lower("DEV")`                        | `"dev"`                          |
| `merge()`             | `merge(map1, map2)`                   | Combine maps                     |
| `toset()`             | `toset(["a","b"])`                    | Convert list to set              |
| `lookup()`            | `lookup(var.map, "key", "default")`   | Read a map value                 |
| `file()`              | `file("script.sh")`                   | Read a file's content            |
| `cidrsubnet()`        | `cidrsubnet("10.0.0.0/16", 8, 1)`     | Calculate a subnet range         |

### 8.17.2 ❓ Conditional Expression

```hcl
instance_type = var.environment == "prod" ? "m5.large" : "t3.micro"
```

```text
condition ? value_if_true : value_if_false
```

### 8.17.3 🔄 Dynamic Blocks

Create **repeated nested blocks** from a list.

```hcl
resource "aws_security_group" "web" {
  name = "web-sg"

  dynamic "ingress" {
    for_each = var.allowed_ports
    content {
      from_port   = ingress.value
      to_port     = ingress.value
      protocol    = "tcp"
      cidr_blocks = ["0.0.0.0/0"]
    }
  }
}
```

---

## 8.18 🛠️ Provisioners (Last Resort)

**Provisioners** run **scripts** on a resource after creation.

```hcl
resource "aws_instance" "web" {
  # ...
  user_data = file("install_nginx.sh")        # ✅ Preferred way
}
```

#### ⚠️ Important

> **HashiCorp advises using provisioners only as a last resort.** Prefer:
> - 🖥️ `user_data` (script run at first boot)
> - 📦 Custom AMIs (Packer)
> - ⚙️ **Ansible** for configuration

---

## 8.19 🆚 Terraform vs CloudFormation vs Ansible

| Feature           | 🏗️ Terraform                      | ☁️ CloudFormation             | ⚙️ Ansible                       |
| ----------------- | --------------------------------- | ----------------------------- | -------------------------------- |
| Main job          | **Provision** infrastructure      | **Provision** AWS infrastructure | **Configure** servers / software |
| Works with        | Many clouds and platforms         | AWS only                      | Servers, network devices, cloud  |
| Language          | HCL                               | JSON / YAML                   | YAML (playbooks)                 |
| State             | State file (we manage)            | AWS manages                   | No state file                    |
| Style             | Declarative                       | Declarative                   | Mostly procedural (tasks in order)|

#### 🧠 Easy Memory

```text
🏗️ Terraform = BUILD the infrastructure (servers, networks)
⚙️ Ansible   = SET UP the software inside the servers
```

---

## 8.20 🔗 Terraform in a CI/CD Pipeline

```text
🐙 Git push (infrastructure code)
      ↓
🤖 Jenkins / GitHub Actions
      ├── terraform fmt -check
      ├── terraform init
      ├── terraform validate
      ├── terraform plan -out=tfplan
      ├── 👤 Manual approval
      └── terraform apply tfplan
```

#### 💻 Jenkins Pipeline

```groovy
pipeline {
    agent any
    stages {
        stage('Init')     { steps { sh 'terraform init -input=false' } }
        stage('Validate') { steps { sh 'terraform validate' } }
        stage('Plan')     { steps { sh 'terraform plan -input=false -out=tfplan' } }
        stage('Approve')  { steps { input message: 'Apply the plan?' } }
        stage('Apply')    { steps { sh 'terraform apply -input=false tfplan' } }
    }
}
```

---

## 8.21 🏆 Terraform Best Practices

```text
✅ Terraform Best Practices
│
├── 📝 Store code in Git
├── 🗄️ Use a remote backend with locking and encryption
├── 🔐 Never commit state files or secrets
├── 🔒 Commit .terraform.lock.hcl
├── 📌 Pin provider and module versions
├── 👀 Always run plan before apply
├── 📚 Use modules for reusable code
├── 🏷️ Tag all resources
├── 🧩 Use separate states for dev / test / prod
├── 🛡️ Use prevent_destroy for critical resources
└── 🧹 Run terraform fmt and validate
```

---

## 8.22 🏗️ Real Example: EC2 Web Server With Security Group

### 🎯 Requirement

Create an **EC2 web server** with a **Security Group** that allows **HTTP (80)** and **SSH (22)**.

### 📁 Files

#### 📄 providers.tf

```hcl
terraform {
  required_version = ">= 1.5.0"
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
  region = var.region
}
```

#### 📄 variables.tf

```hcl
variable "region" {
  type    = string
  default = "ap-south-1"
}

variable "instance_type" {
  type    = string
  default = "t3.micro"
}

variable "my_ip" {
  description = "Our public IP for SSH, like 203.0.113.5/32"
  type        = string
}
```

#### 📄 main.tf

```hcl
data "aws_ami" "al2023" {
  most_recent = true
  owners      = ["amazon"]

  filter {
    name   = "name"
    values = ["al2023-ami-2023*-x86_64"]
  }
}

resource "aws_security_group" "web" {
  name        = "web-sg"
  description = "Allow HTTP and SSH"

  ingress {
    description = "HTTP"
    from_port   = 80
    to_port     = 80
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

  ingress {
    description = "SSH from my IP"
    from_port   = 22
    to_port     = 22
    protocol    = "tcp"
    cidr_blocks = [var.my_ip]
  }

  egress {
    from_port   = 0
    to_port     = 0
    protocol    = "-1"
    cidr_blocks = ["0.0.0.0/0"]
  }
}

resource "aws_instance" "web" {
  ami                    = data.aws_ami.al2023.id
  instance_type          = var.instance_type
  vpc_security_group_ids = [aws_security_group.web.id]

  user_data = <<-EOF
    #!/bin/bash
    dnf install -y httpd
    systemctl enable --now httpd
    echo "Hello from Terraform" > /var/www/html/index.html
  EOF

  tags = {
    Name      = "terraform-web"
    ManagedBy = "terraform"
  }
}
```

#### 📄 outputs.tf

```hcl
output "public_ip" {
  value = aws_instance.web.public_ip
}

output "website_url" {
  value = "http://${aws_instance.web.public_ip}"
}
```

### 🪜 Run It

```bash
terraform init
terraform fmt
terraform validate
terraform plan  -var="my_ip=203.0.113.5/32"
terraform apply -var="my_ip=203.0.113.5/32"
terraform output website_url
# Open the URL in the browser ✅

terraform destroy -var="my_ip=203.0.113.5/32"     # Delete everything when done
```

### 🏗️ What Happens

```text
📝 main.tf
     │ terraform apply
     ▼
🏗️ Terraform
     ├── 🔍 Reads data: latest Amazon Linux AMI
     ├── 🛡️ Creates Security Group (ports 80, 22)
     └── 🖥️ Creates EC2 instance (uses the Security Group)
             │
             ▼
     📤 Output: public IP / website URL
```

---

## 📌🧠 Terraform Quick Revision

```text
🏗️ Terraform
│
├── 🧱 Concepts
│   ├── Provider
│   ├── Resource
│   ├── Data Source
│   ├── Variable / Output / Locals
│   ├── Module
│   └── State + Backend
│
├── 🔄 Workflow
│   ├── init
│   ├── plan
│   ├── apply
│   └── destroy
│
├── 📝 HCL Language
│   ├── Blocks and arguments
│   ├── References (type.name.attribute)
│   ├── Functions
│   └── Conditionals, dynamic blocks
│
├── 🔁 Meta-Arguments
│   ├── count
│   ├── for_each
│   ├── depends_on
│   └── lifecycle
│
├── 📄 State
│   ├── terraform.tfstate
│   ├── Remote backend (S3 + locking)
│   └── import, state commands
│
├── 📚 Reuse
│   ├── Modules
│   └── Workspaces
│
└── 🔗 Integration
    ├── CI/CD (Jenkins)
    └── Ansible (configuration)
```

---

## 🧠⚡ Terraform One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| 🏗️ **Terraform**           | Infrastructure as Code Tool (Multi-Cloud)           |
| 📝 **HCL**                 | Language Used in .tf Files                          |
| 🔌 **Provider**            | Plugin for AWS / Azure / GCP                        |
| 🧩 **Resource**            | Thing to Create                                     |
| 🔍 **Data Source**         | Read Something That Already Exists                  |
| 🎛️ **Variable**            | Input                                               |
| 📤 **Output**              | Value Shown After Apply                             |
| 📚 **Module**              | Reusable Infrastructure Code                        |
| 📄 **State**               | Record of What Terraform Created                    |
| 🗄️ **Remote Backend**      | Shared, Locked, Safe State (S3)                     |
| ⚙️ **terraform init**      | Download Providers and Setup                        |
| 👀 **terraform plan**      | Preview Changes                                     |
| 🚀 **terraform apply**     | Create / Change Resources                           |
| 🧹 **terraform destroy**   | Delete Everything                                   |
| 🔢 **count**               | Many Copies by Number                               |
| 🔁 **for_each**            | Many Items by Name                                  |
| 🛡️ **lifecycle**           | Control Create / Destroy Behavior                   |
| 🌿 **Workspace**           | Separate State for Same Code                        |
| 🔒 **.terraform.lock.hcl** | Locks Provider Versions                             |

---

## 🗺️ Terraform Learning Map

```text
                        🏗️ Terraform
                              │
      ┌───────────────────────┼───────────────────────┐
      │                       │                       │
      ▼                       ▼                       ▼
   LANGUAGE                WORKFLOW                 STATE
      │                       │                       │
      ├── Providers           ├── init                ├── terraform.tfstate
      ├── Resources           ├── validate / fmt      ├── Remote Backend (S3)
      ├── Data Sources        ├── plan                ├── Locking
      ├── Variables           ├── apply               └── import / state cmds
      ├── Outputs / Locals    └── destroy
      └── Functions
      │
      ▼
   REUSE & SCALE
      │
      ├── Modules
      ├── count / for_each
      ├── Workspaces
      └── dynamic blocks
      │
      ▼
   INTEGRATION
      │
      ├── Jenkins pipeline
      ├── Ansible (after provisioning)
      └── Kubernetes / EKS
```

---

## ⭐ Terraform Final Memory

```text
Terraform
 │
 ├── What is it?
 │      └── IaC tool to provision infrastructure
 │
 ├── What language?
 │      └── HCL (.tf files)
 │
 ├── Basic workflow?
 │      └── init → plan → apply → destroy
 │
 ├── What tracks created resources?
 │      └── State file
 │
 ├── Where should team state be stored?
 │      └── Remote backend (S3 with locking)
 │
 ├── How to reuse code?
 │      └── Modules
 │
 ├── Many similar resources?
 │      └── count / for_each
 │
 ├── Terraform vs Ansible?
 │      └── Terraform builds infrastructure, Ansible configures servers
 │
 └── What should never be in Git?
        └── State files and secrets
```

---

# ⚙️ PART 9 — Ansible — Configuration Management

> **Ansible = Write steps in YAML, run on many servers using SSH**

---

## 9.1 ⚙️ What is Ansible?

> **Ansible = Automation tool for configuration management and deployment**

Ansible is a tool that **automatically configures servers, installs software and deploys applications** on **many machines at the same time**, using simple **YAML files** called **playbooks**.

It is **agentless** — we do **not need to install anything on the servers we manage**. Ansible connects using **SSH** (Linux) or **WinRM** (Windows).

#### 📦 Ansible Is Used To

- 📥 **Install software** (Nginx, Java, Docker)
- ⚙️ **Configure servers** (users, files, services)
- 🚀 **Deploy applications**
- 🔄 **Run tasks** on hundreds of servers together
- 🛡️ **Keep servers consistent**
- ☁️ **Provision** some cloud resources

#### 🏗️ Ansible Basic Idea

```text
👨‍💻 Admin writes a Playbook (YAML)
        │
        ▼
💻 Control Node (Ansible installed)
        │ SSH
        ├──────────────┬──────────────┐
        ▼              ▼              ▼
   🖥️ Server 1     🖥️ Server 2     🖥️ Server 3
   (Managed Nodes — no Ansible agent needed)
```

#### 🧠 Easy Memory

> **Ansible = Write steps in YAML, run on many servers using SSH**

---

## 9.2 🤔 Why Do We Use Ansible?

### ❌ Manual Configuration

```text
🖥️ Login to server 1 → install Nginx → edit config → start service
🖥️ Login to server 2 → install Nginx → edit config → start service
🖥️ Login to server 3 → ... (50 more servers)
        ↓
🐢 Slow, boring work
🐛 Each server ends up slightly different
```

### ✅ With Ansible

```text
📝 One playbook
        ↓
⌨️ ansible-playbook site.yml
        ↓
✅ All servers configured the same way, in minutes
```

#### ⭐ Main Reasons

- 🪶 **Agentless** — only SSH needed
- 📖 **Simple YAML** — easy to read and write
- 🔁 **Idempotent** — safe to run again and again
- 📈 **Scales** from 1 server to thousands
- 🧩 **Many modules** (thousands of ready tasks)
- 🆓 **Free and open source** (by Red Hat)
- 🤝 Works well with **Terraform, Jenkins, Docker, Kubernetes, cloud**

> **Idempotent = If the server is already in the desired state, Ansible changes nothing.**

---

## 9.3 🧰 What Does Ansible Provide?

Ansible provides:

- 📋 Inventory (list of servers)
- 📜 Playbooks, Plays and Tasks
- 🧩 Modules
- 🎭 Roles
- 🎛️ Variables and Facts
- 🔔 Handlers
- 📄 Templates (Jinja2)
- 🔐 Vault (encrypt secrets)
- 📦 Collections and Galaxy
- ⌨️ Ad-hoc commands

---

## 9.4 🏛️ Ansible Architecture

```text
🏛️ Ansible Architecture
│
├── 💻 Control Node      → Machine where Ansible is installed and run
├── 🖥️ Managed Nodes     → Servers that Ansible configures (also called hosts)
├── 📋 Inventory         → List of managed nodes (and groups)
├── 📜 Playbook          → YAML file with the automation steps
├── 🧩 Modules           → Small programs that do the actual work
├── 🔌 Plugins           → Extend Ansible (connection, inventory, filters)
└── 🔐 Connection        → SSH (Linux) / WinRM (Windows)
```

### 9.4.1 📖 Simple Definitions

| Concept            | Simple Meaning                                                     |
| ------------------ | ------------------------------------------------------------------ |
| 💻 Control Node    | The machine where we run `ansible` commands (Linux/macOS/WSL)      |
| 🖥️ Managed Node    | A server that Ansible controls                                     |
| 📋 Inventory       | A file listing servers and groups                                  |
| 🧩 Module          | A ready-made task (install a package, copy a file, start a service) |
| 📝 Task            | One action that uses one module                                    |
| 🎬 Play            | A set of tasks applied to a group of hosts                         |
| 📜 Playbook        | A YAML file with one or more plays                                 |
| 🎭 Role            | A reusable, organized package of tasks, files and templates        |
| 🔔 Handler         | A task that runs only when notified (like "restart nginx")         |

#### 🏗️ Relationship

```text
📜 Playbook
   └── 🎬 Play (hosts: webservers)
         ├── 📝 Task 1 → module: apt  (install nginx)
         ├── 📝 Task 2 → module: copy (copy config)
         └── 📝 Task 3 → module: service (start nginx)
```

#### 🧠 Remember

> **Playbook → Plays → Tasks → Modules**

### 9.4.2 🔄 Push vs Pull

| ⚙️ Ansible (Push)                          | 🐶 Puppet / Chef (Pull)                    |
| ------------------------------------------ | ------------------------------------------ |
| Control node **pushes** changes            | Agents on servers **pull** changes         |
| No agent needed                            | Agent must be installed                    |
| Runs when we start it                      | Agents check regularly                     |

---

## 9.5 ⚙️ Installing Ansible

Ansible is installed **only on the control node**.

```bash
# Ubuntu / Debian
sudo apt update
sudo apt install ansible -y

# Amazon Linux / RHEL (using pip)
sudo yum install python3-pip -y
pip3 install --user ansible

# Check
ansible --version
```

#### 📋 Requirements

```text
💻 Control Node  → Linux / macOS (or WSL on Windows) with Python
🖥️ Managed Nodes → SSH access + Python (for most modules)
```

### 9.5.1 🔑 Setup SSH Access

```bash
# On the control node: create an SSH key
ssh-keygen -t ed25519

# Copy the public key to each managed node
ssh-copy-id ubuntu@192.168.1.10
ssh-copy-id ubuntu@192.168.1.11

# Test
ssh ubuntu@192.168.1.10
```

#### ⚠️ Important

> Use **SSH keys** (not passwords) for Ansible. **Never** store passwords in plain text files.

---

## 9.6 📋 Inventory

The **inventory** is a file that lists **servers and groups**.

### 9.6.1 📄 INI Format (`inventory.ini`)

```ini
[webservers]
web1 ansible_host=192.168.1.10
web2 ansible_host=192.168.1.11

[dbservers]
db1 ansible_host=192.168.1.20

[production:children]
webservers
dbservers

[all:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=~/.ssh/id_ed25519
```

### 9.6.2 📄 YAML Format (`inventory.yml`)

```yaml
all:
  vars:
    ansible_user: ubuntu
  children:
    webservers:
      hosts:
        web1:
          ansible_host: 192.168.1.10
        web2:
          ansible_host: 192.168.1.11
    dbservers:
      hosts:
        db1:
          ansible_host: 192.168.1.20
```

#### 📖 Understanding It

```text
[webservers]       → A group of hosts
ansible_host       → IP address of the server
ansible_user       → SSH username
[group:children]   → A group made of other groups
[all:vars]         → Variables for all hosts
```

#### 🔤 Special Groups

| Group       | Meaning                                  |
| ----------- | ---------------------------------------- |
| `all`       | Every host in the inventory              |
| `ungrouped` | Hosts that are not in any group          |

### 9.6.3 ☁️ Dynamic Inventory

For cloud servers that change often, Ansible can **read the server list from the cloud** (for example, the **`amazon.aws.aws_ec2`** plugin finds EC2 instances by tags).

```text
☁️ AWS EC2 (tags: Role=web) ──► 📋 Dynamic Inventory ──► ⚙️ Ansible
```

---

## 9.7 ⌨️ Ad-Hoc Commands

**Ad-hoc commands** run **one quick task** without writing a playbook.

```bash
ansible <hosts> -i <inventory> -m <module> -a "<arguments>"
```

### 9.7.1 💻 Examples

```bash
# Check connection to all servers
ansible all -i inventory.ini -m ping

# Run a command
ansible webservers -i inventory.ini -m command -a "uptime"

# Install a package (needs sudo → --become)
ansible webservers -i inventory.ini -m apt -a "name=nginx state=present" --become

# Restart a service
ansible webservers -i inventory.ini -m service -a "name=nginx state=restarted" --become

# Copy a file
ansible all -i inventory.ini -m copy -a "src=./file.txt dest=/tmp/file.txt"

# Gather facts
ansible web1 -i inventory.ini -m setup
```

#### 🚩 Common Options

| Option            | Meaning                                         |
| ----------------- | ----------------------------------------------- |
| `-i`              | Inventory file                                  |
| `-m`              | Module name                                     |
| `-a`              | Arguments for the module                        |
| `--become` / `-b` | Run with sudo (privilege escalation)            |
| `-u`              | SSH user                                        |
| `--limit`         | Run on a subset of hosts                        |
| `-v`, `-vvv`      | More detailed output (debugging)                |

#### 🧠 Remember

> **Ad-hoc = quick one-time job. Playbook = repeatable, saved automation.**

---

## 9.8 📜 Playbooks

A **playbook** is a **YAML file** that describes **what to do on which servers**.

### 9.8.1 💻 First Playbook: Install and Start Nginx

```yaml
---
- name: Install and start Nginx
  hosts: webservers
  become: true

  tasks:
    - name: Install Nginx
      ansible.builtin.apt:
        name: nginx
        state: present
        update_cache: true

    - name: Start and enable Nginx
      ansible.builtin.service:
        name: nginx
        state: started
        enabled: true

    - name: Copy the home page
      ansible.builtin.copy:
        content: "<h1>Hello from Ansible</h1>"
        dest: /var/www/html/index.html
```

#### ▶️ Run It

```bash
ansible-playbook -i inventory.ini site.yml
```

### 9.8.2 📖 Understanding the Playbook

```text
---                      → YAML document start
- name:                  → Name of the play (human-readable)
  hosts: webservers      → Which group to run on
  become: true           → Use sudo
  tasks:                 → List of tasks
    - name: ...          → Task description
      module:            → Module with its arguments
        key: value
```

#### ⚠️ YAML Rules

```text
✅ Use SPACES for indentation (never tabs)
✅ Keep indentation consistent (2 spaces)
✅ Lists start with "- "
✅ Key and value are written as  key: value
```

### 9.8.3 🧩 Common Modules

| Module                          | Purpose                                         |
| ------------------------------- | ----------------------------------------------- |
| `ansible.builtin.ping`          | Test connection                                 |
| `ansible.builtin.apt` / `yum` / `dnf` / `package` | Install or remove packages   |
| `ansible.builtin.service` / `systemd` | Manage services                           |
| `ansible.builtin.copy`          | Copy files to servers                           |
| `ansible.builtin.template`      | Copy a Jinja2 template with variables           |
| `ansible.builtin.file`          | Create folders, set permissions, delete files   |
| `ansible.builtin.user` / `group`| Manage users and groups                         |
| `ansible.builtin.git`           | Clone Git repositories                          |
| `ansible.builtin.command` / `shell` | Run commands                                |
| `ansible.builtin.lineinfile`    | Add or change one line in a file                |
| `ansible.builtin.debug`         | Print messages / variables                      |
| `ansible.builtin.uri`           | Call a web URL / API                            |
| `community.docker.docker_container` | Manage Docker containers                    |
| `kubernetes.core.k8s`           | Manage Kubernetes objects                       |

#### ⚖️ command vs shell

| 🎯 command                          | 🐚 shell                                   |
| ----------------------------------- | ------------------------------------------ |
| Runs a command directly             | Runs through a shell (`/bin/sh`)           |
| No pipes (`|`), no redirects (`>`)  | Supports pipes, redirects, variables       |
| Safer                               | Use only when needed                       |

> 💡 Prefer **real modules** (apt, service, copy) over `command`/`shell` — they are **idempotent**.

### 9.8.4 🔁 Module States

Many modules use **`state`** to describe the **desired result**.

| State       | Meaning                              |
| ----------- | ------------------------------------ |
| `present`   | Must exist / be installed            |
| `absent`    | Must not exist / be removed          |
| `latest`    | Install the newest version           |
| `started`   | Service must be running              |
| `stopped`   | Service must be stopped              |
| `restarted` | Restart the service                  |

---

## 9.9 🎛️ Variables and Facts

### 9.9.1 🎛️ Variables

```yaml
---
- name: Use variables
  hosts: webservers
  become: true
  vars:
    package_name: nginx
    web_port: 80

  tasks:
    - name: Install {{ package_name }}
      ansible.builtin.apt:
        name: "{{ package_name }}"
        state: present

    - name: Show the port
      ansible.builtin.debug:
        msg: "Web port is {{ web_port }}"
```

#### ⚠️ Important

> When a value **starts with `{{ }}`**, put it inside **quotes**: `name: "{{ package_name }}"`.

### 9.9.2 📂 Where to Keep Variables

```text
📁 project/
├── 📄 site.yml
├── 📄 inventory.ini
├── 📁 group_vars/
│   ├── all.yml              → Variables for all hosts
│   └── webservers.yml       → Variables for the webservers group
└── 📁 host_vars/
    └── web1.yml             → Variables for one host
```

### 9.9.3 🔢 Passing Variables From the Command Line

```bash
ansible-playbook site.yml -e "web_port=8080 env=prod"
```

> Command-line variables (`-e`) have the **highest priority**.

### 9.9.4 🔍 Facts

**Facts** are **information Ansible collects from each server** automatically (OS, IP address, memory, CPU).

```yaml
- name: Show OS family
  ansible.builtin.debug:
    msg: "{{ ansible_facts['os_family'] }} - {{ ansible_facts['distribution'] }}"
```

```bash
ansible web1 -m setup        # See all facts
```

### 9.9.5 📝 register

Save the **result of a task** in a variable.

```yaml
- name: Check Nginx status
  ansible.builtin.command: systemctl is-active nginx
  register: nginx_status
  changed_when: false

- name: Show result
  ansible.builtin.debug:
    var: nginx_status.stdout
```

---

## 9.10 🧠 Conditions, Loops and Tags

### 9.10.1 ❓ Conditions (`when`)

```yaml
- name: Install Nginx on Debian systems
  ansible.builtin.apt:
    name: nginx
    state: present
  when: ansible_facts['os_family'] == "Debian"

- name: Install Nginx on RedHat systems
  ansible.builtin.dnf:
    name: nginx
    state: present
  when: ansible_facts['os_family'] == "RedHat"
```

### 9.10.2 🔁 Loops

```yaml
- name: Install many packages
  ansible.builtin.apt:
    name: "{{ item }}"
    state: present
  loop:
    - git
    - curl
    - unzip
```

### 9.10.3 🏷️ Tags

Run **only selected tasks**.

```yaml
- name: Install Nginx
  ansible.builtin.apt:
    name: nginx
    state: present
  tags: install

- name: Copy config
  ansible.builtin.template:
    src: nginx.conf.j2
    dest: /etc/nginx/nginx.conf
  tags: config
```

```bash
ansible-playbook site.yml --tags config
ansible-playbook site.yml --skip-tags install
```

---

## 9.11 🔔 Handlers

A **handler** is a task that runs **only when another task changes something** (and it **notifies** the handler).

```yaml
---
- name: Configure Nginx
  hosts: webservers
  become: true

  tasks:
    - name: Copy Nginx config
      ansible.builtin.template:
        src: nginx.conf.j2
        dest: /etc/nginx/nginx.conf
      notify: Restart Nginx

  handlers:
    - name: Restart Nginx
      ansible.builtin.service:
        name: nginx
        state: restarted
```

```text
📝 Task "Copy config" → changed?
        ├── ✅ Yes → 🔔 notify → Handler "Restart Nginx" runs (once, at the end)
        └── ❌ No  → Handler does NOT run
```

> **Handler = "Restart only if something really changed."**

---

## 9.12 📄 Templates (Jinja2)

A **template** is a file with **variables** that Ansible fills in for each server.

#### 📄 `templates/nginx.conf.j2`

```jinja
server {
    listen {{ web_port }};
    server_name {{ ansible_facts['hostname'] }};

    location / {
        root /var/www/html;
        index index.html;
    }
}
```

#### 📜 Use in a Task

```yaml
- name: Create Nginx site config
  ansible.builtin.template:
    src: nginx.conf.j2
    dest: /etc/nginx/conf.d/site.conf
    owner: root
    mode: "0644"
  notify: Restart Nginx
```

#### 🔤 Jinja2 Basics

| Syntax                   | Meaning                        |
| ------------------------ | ------------------------------ |
| `{{ variable }}`         | Print a variable               |
| `{% if x %} ... {% endif %}` | Condition                  |
| `{% for i in list %} ... {% endfor %}` | Loop             |
| `{{ var \| default('x') }}` | Filter (default value)      |

---

## 9.13 🎭 Roles

A **role** is a **reusable, organized folder** that holds everything for one job (like "nginx" or "docker").

#### 📁 Role Structure

```text
📁 roles/
└── 📁 nginx/
    ├── 📁 tasks/         → main.yml (the tasks)
    ├── 📁 handlers/      → main.yml (handlers)
    ├── 📁 templates/     → Jinja2 templates (.j2)
    ├── 📁 files/         → Static files to copy
    ├── 📁 vars/          → Variables (high priority)
    ├── 📁 defaults/      → Default variables (low priority)
    └── 📁 meta/          → Role information and dependencies
```

#### ⌨️ Create a Role

```bash
ansible-galaxy init roles/nginx
```

#### 📜 Use Roles in a Playbook

```yaml
---
- name: Configure web servers
  hosts: webservers
  become: true
  roles:
    - common
    - nginx
```

#### 🧠 Simple Meaning

> **Role = A reusable package of Ansible code, like a function or a module in programming**

### 9.13.1 📦 Ansible Galaxy and Collections

```text
📦 Sharing Ansible Content
│
├── 🌍 Ansible Galaxy → Public website with community roles and collections
└── 📚 Collection     → A package of modules, roles and plugins (amazon.aws, community.docker)
```

```bash
ansible-galaxy collection install community.docker
ansible-galaxy role install geerlingguy.docker
```

---

## 9.14 🔐 Ansible Vault

**Vault** **encrypts secrets** (passwords, keys) so we can store them safely in Git.

```bash
ansible-vault create secrets.yml        # Create an encrypted file
ansible-vault encrypt vars.yml          # Encrypt an existing file
ansible-vault edit secrets.yml          # Edit
ansible-vault view secrets.yml          # View
ansible-vault decrypt secrets.yml       # Decrypt
ansible-vault rekey secrets.yml         # Change the vault password
```

#### ▶️ Use Vault When Running

```bash
ansible-playbook site.yml --ask-vault-pass
ansible-playbook site.yml --vault-password-file ~/.vault_pass.txt
```

#### 💻 Example Encrypted Variables

```yaml
# secrets.yml (encrypted)
db_password: SuperSecret123
```

```yaml
# playbook
vars_files:
  - secrets.yml
```

#### ⚠️ Important

> **Never commit unencrypted passwords.** In Jenkins, store the vault password as a **credential**.

---

## 9.15 ⚙️ ansible.cfg

**`ansible.cfg`** sets **default options** for Ansible.

```ini
[defaults]
inventory = ./inventory.ini
remote_user = ubuntu
host_key_checking = False
forks = 10
roles_path = ./roles

[privilege_escalation]
become = True
become_method = sudo
become_user = root
```

```text
📍 Ansible Looks for ansible.cfg in this order:
1. ANSIBLE_CONFIG (environment variable)
2. ./ansible.cfg (current folder)   ← Most common
3. ~/.ansible.cfg
4. /etc/ansible/ansible.cfg
```

#### ⚠️ Important

> `host_key_checking = False` is okay for **learning labs**. In production, **keep host key checking ON** for security.

---

## 9.16 🧪 Safe Running and Debugging

| Command                                      | What It Does                                      |
| -------------------------------------------- | ------------------------------------------------- |
| `ansible-playbook site.yml --syntax-check`   | Check YAML/playbook syntax                        |
| `ansible-playbook site.yml --check`          | **Dry run** — show what would change              |
| `ansible-playbook site.yml --diff`           | Show file differences                             |
| `ansible-playbook site.yml -v` / `-vvv`      | Verbose output                                    |
| `ansible-playbook site.yml --limit web1`     | Run only on one host                              |
| `ansible-playbook site.yml --start-at-task "Install Nginx"` | Start from a specific task        |
| `ansible-lint site.yml`                      | Check style and best practices                    |

#### 📊 Understanding the Result

```text
PLAY RECAP
web1 : ok=5  changed=2  unreachable=0  failed=0  skipped=1
```

| Result        | Meaning                                       |
| ------------- | --------------------------------------------- |
| `ok`          | Task ran successfully (no change or change)   |
| `changed`     | Task changed something                        |
| `unreachable` | Could not connect (SSH problem)               |
| `failed`      | Task failed                                   |
| `skipped`     | Task skipped (`when` was false)               |

---

## 9.17 🆚 Ansible vs Terraform vs Puppet / Chef

| Feature           | ⚙️ Ansible                         | 🏗️ Terraform                       | 🐶 Puppet / Chef               |
| ----------------- | ---------------------------------- | ---------------------------------- | ------------------------------ |
| Main job          | **Configure** servers, deploy apps | **Provision** infrastructure       | **Configure** servers          |
| Agent needed?     | ❌ No (agentless)                  | ❌ No                              | ✅ Yes                         |
| Language          | YAML                               | HCL                                | Ruby-based DSL                 |
| Style             | Push                               | API calls (declarative)            | Pull                           |
| State file        | ❌ No                              | ✅ Yes                             | Server holds the state         |
| Learning curve    | Easy                               | Medium                             | Harder                         |

#### 🧠 Easy Memory

```text
🏗️ Terraform = Creates the servers and network (the building)
⚙️ Ansible   = Sets up the software inside them (the furniture)
```

---

## 9.18 🔗 Ansible With Other Tools

```text
🔗 Ansible Integrations
│
├── 🏗️ Terraform   → Terraform creates servers → Ansible configures them
├── 🤖 Jenkins     → Pipeline runs ansible-playbook to deploy
├── 🐳 Docker      → Install Docker, run containers
├── ☸️ Kubernetes  → Deploy objects using the k8s module
├── ☁️ AWS         → Dynamic inventory and cloud modules
└── 🔧 AWX / Ansible Automation Platform → Web UI, scheduling, RBAC
```

#### 💻 Jenkins Pipeline Stage

```groovy
stage('Deploy with Ansible') {
    steps {
        sshagent(credentials: ['ansible-ssh-key']) {
            sh 'ansible-playbook -i inventory.ini deploy.yml -e "app_version=${BUILD_NUMBER}"'
        }
    }
}
```

---

## 9.19 🏆 Ansible Best Practices

```text
✅ Ansible Best Practices
│
├── 📝 Keep playbooks in Git
├── 🎭 Use roles to organize code
├── 🧩 Use modules instead of shell/command
├── 🔁 Make tasks idempotent
├── 🏷️ Give every task a clear name
├── 🔐 Use Vault for secrets
├── 🧪 Test with --check and ansible-lint
├── 📂 Use group_vars and host_vars
└── 🔑 Use SSH keys and least privilege
```

---

## 9.20 🏗️ Real Example: Deploy an App to Web Servers

### 🎯 Requirement

Install **Java**, copy the **application jar**, and run it as a **service** on **two web servers**.

### 📁 Project Layout

```text
📁 deploy-app/
├── 📄 ansible.cfg
├── 📄 inventory.ini
├── 📄 deploy.yml
└── 📁 templates/
    └── shop-app.service.j2
```

#### 📄 inventory.ini

```ini
[webservers]
web1 ansible_host=192.168.1.10
web2 ansible_host=192.168.1.11

[webservers:vars]
ansible_user=ubuntu
```

#### 📄 templates/shop-app.service.j2

```ini
[Unit]
Description=Shop Application
After=network.target

[Service]
User=ubuntu
ExecStart=/usr/bin/java -jar /opt/shop-app/app.jar --server.port={{ app_port }}
Restart=always

[Install]
WantedBy=multi-user.target
```

#### 📄 deploy.yml

```yaml
---
- name: Deploy Shop Application
  hosts: webservers
  become: true

  vars:
    app_dir: /opt/shop-app
    app_port: 8080
    jar_file: target/shop-app-1.0.jar

  tasks:
    - name: Install Java
      ansible.builtin.apt:
        name: openjdk-17-jre-headless
        state: present
        update_cache: true

    - name: Create the application folder
      ansible.builtin.file:
        path: "{{ app_dir }}"
        state: directory
        owner: ubuntu
        mode: "0755"

    - name: Copy the application jar
      ansible.builtin.copy:
        src: "{{ jar_file }}"
        dest: "{{ app_dir }}/app.jar"
        owner: ubuntu
        mode: "0644"
      notify: Restart shop-app

    - name: Create the systemd service
      ansible.builtin.template:
        src: shop-app.service.j2
        dest: /etc/systemd/system/shop-app.service
        mode: "0644"
      notify: Restart shop-app

    - name: Enable and start the service
      ansible.builtin.systemd:
        name: shop-app
        enabled: true
        state: started
        daemon_reload: true

  handlers:
    - name: Restart shop-app
      ansible.builtin.systemd:
        name: shop-app
        state: restarted
        daemon_reload: true
```

### ▶️ Run It

```bash
ansible all -i inventory.ini -m ping                    # Test connection
ansible-playbook -i inventory.ini deploy.yml --check    # Dry run
ansible-playbook -i inventory.ini deploy.yml            # Deploy ✅
```

### 🏗️ What Happens

```text
💻 Control Node  (ansible-playbook deploy.yml)
        │ SSH
        ├────────────────────────┐
        ▼                        ▼
🖥️ web1                         🖥️ web2
  ├── ☕ Install Java              ├── ☕ Install Java
  ├── 📁 Create /opt/shop-app      ├── 📁 Create /opt/shop-app
  ├── 📦 Copy app.jar              ├── 📦 Copy app.jar
  ├── 📄 Create systemd service    ├── 📄 Create systemd service
  └── ▶️ Start shop-app            └── ▶️ Start shop-app
```

---

## 📌🧠 Ansible Quick Revision

```text
⚙️ Ansible
│
├── 🏛️ Architecture
│   ├── Control Node
│   ├── Managed Nodes (agentless, SSH)
│   ├── Inventory
│   └── Modules
│
├── 📜 Playbooks
│   ├── Play → Tasks → Modules
│   ├── become (sudo)
│   └── YAML rules (spaces, not tabs)
│
├── 🎛️ Data
│   ├── Variables (vars, group_vars, host_vars, -e)
│   ├── Facts (setup)
│   └── register
│
├── 🧠 Logic
│   ├── when (conditions)
│   ├── loop
│   └── tags
│
├── 🔔 Handlers + Templates (Jinja2)
│
├── 🎭 Roles + Galaxy + Collections
│
├── 🔐 Vault
│
└── 🧪 Testing
    ├── --syntax-check
    ├── --check (dry run)
    └── ansible-lint
```

---

## 🧠⚡ Ansible One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| ⚙️ **Ansible**             | Agentless Automation Using YAML and SSH             |
| 💻 **Control Node**        | Machine Where We Run Ansible                        |
| 🖥️ **Managed Node**        | Server Ansible Configures                           |
| 📋 **Inventory**           | List of Servers and Groups                          |
| 📜 **Playbook**            | YAML File With Automation Steps                     |
| 🧩 **Module**              | Ready-Made Task (apt, copy, service)                |
| 🔁 **Idempotent**          | Running Again Changes Nothing If Already Correct    |
| 🔔 **Handler**             | Runs Only When Notified (Restart on Change)         |
| 📄 **Template**            | File With Variables (Jinja2, .j2)                   |
| 🎭 **Role**                | Reusable Package of Tasks and Files                 |
| 🔍 **Facts**               | Information Collected From Servers                  |
| 🔐 **Vault**               | Encrypt Secrets                                     |
| 📦 **Galaxy**              | Public Site for Roles and Collections               |
| ⬆️ **become**              | Run With sudo                                       |
| 🧪 **--check**             | Dry Run (No Changes)                                |
| 🏗️ **Terraform vs Ansible**| Terraform Builds, Ansible Configures                |

---

## 🗺️ Ansible Learning Map

```text
                            ⚙️ Ansible
                                │
      ┌─────────────────────────┼─────────────────────────┐
      │                         │                         │
      ▼                         ▼                         ▼
    SETUP                   AUTOMATION                 ORGANIZE
      │                         │                         │
      ├── Install               ├── Ad-hoc commands       ├── Roles
      ├── SSH keys              ├── Playbooks             ├── Collections
      ├── Inventory             │    ├── Plays / Tasks    ├── Galaxy
      └── ansible.cfg           │    ├── Modules          └── group_vars / host_vars
                                │    ├── Variables
                                │    ├── when / loop      
                                │    └── Handlers
                                └── Templates (Jinja2)
      │
      ▼
   SECURITY
      │
      ├── Vault
      └── SSH keys + become
      │
      ▼
   INTEGRATION
      │
      ├── Terraform → Ansible
      ├── Jenkins pipeline
      └── Docker / Kubernetes / AWS
```

---

## ⭐ Ansible Final Memory

```text
Ansible
 │
 ├── What is it?
 │      └── Agentless configuration management and automation tool
 │
 ├── How does it connect?
 │      └── SSH (Linux), WinRM (Windows)
 │
 ├── What language do we write?
 │      └── YAML (playbooks)
 │
 ├── Where is the server list?
 │      └── Inventory
 │
 ├── How to run a playbook?
 │      └── ansible-playbook -i inventory site.yml
 │
 ├── How to restart a service only on change?
 │      └── notify + handler
 │
 ├── How to reuse automation code?
 │      └── Roles
 │
 ├── How to protect passwords?
 │      └── Ansible Vault
 │
 └── How to test without changing anything?
        └── --check (dry run)
```

---

# ☸️ PART 10 — Kubernetes — Container Orchestration

> **Kubernetes = Manager that keeps our containers running, scaled and healthy**

---

## 10.1 ☸️ What is Kubernetes?

> **Kubernetes (K8s) = Container orchestration platform**

Kubernetes is an **open-source system that automatically runs, scales, heals and updates containers** across **many servers**.

It was created by **Google** and is now managed by the **CNCF (Cloud Native Computing Foundation)**. The short name **K8s** means "K + 8 letters + s".

#### 🤔 What is Orchestration?

Docker runs **one container** easily. But real applications need **hundreds of containers** on **many servers**. **Orchestration** means **managing all of them automatically**.

#### 📦 Kubernetes Is Used To

- 🚀 **Deploy** containers on a cluster of servers
- 📈 **Scale** up and down automatically
- 🩹 **Self-heal** — restart failed containers
- 🔄 Do **rolling updates** with no downtime
- ⚖️ **Load balance** traffic between containers
- 🔍 **Discover** services by name
- 🔐 Manage **configuration and secrets**

#### 🏗️ Kubernetes Basic Idea

```text
👨‍💻 We say:  "I want 3 copies of my app running."
        │
        ▼
☸️ Kubernetes
        │
        ├── 🐳 Pod 1 on Node A
        ├── 🐳 Pod 2 on Node B
        └── 🐳 Pod 3 on Node C

💥 If Pod 2 crashes → Kubernetes starts a new one automatically
```

#### 🧠 Easy Memory

> **Kubernetes = Manager that keeps our containers running, scaled and healthy**

---

## 10.2 🤔 Why Do We Use Kubernetes?

### ❌ Only Docker (Manual)

```text
🐳 Container crashes at 3 AM → nobody restarts it
📈 Traffic grows → we start more containers by hand
🔄 New version → we stop the old, start the new (downtime)
🌐 Many servers → hard to know where each container runs
```

### ✅ With Kubernetes

```text
🩹 Self-healing    → Failed containers restart automatically
📈 Auto-scaling    → More Pods when traffic grows
🔄 Rolling update  → New version with no downtime, easy rollback
⚖️ Load balancing  → Traffic spreads across Pods
🔍 Service discovery → Apps find each other by name
```

#### ⭐ Main Reasons

- 🩹 **High availability** and self-healing
- 📈 **Easy scaling** (manual or automatic)
- 🔄 **Zero-downtime updates** and rollbacks
- 🌍 **Runs anywhere** — on-premises or any cloud (EKS, AKS, GKE)
- 📝 **Declarative** — we describe the desired state in YAML
- 🧩 Huge ecosystem (Helm, Prometheus, Ingress controllers)

---

## 10.3 🧰 What Does Kubernetes Provide?

Kubernetes provides:

- 🐳 Pods, ReplicaSets and Deployments
- 🌐 Services and Ingress
- ⚙️ ConfigMaps and Secrets
- 💾 Persistent Storage (PV / PVC)
- 📈 Horizontal Pod Autoscaler
- 🩺 Health Checks (Probes)
- 🧱 Namespaces and Resource Limits
- 🔐 RBAC (access control)
- 🔄 Rolling Updates and Rollbacks
- ⏰ Jobs and CronJobs

---

## 10.4 🏛️ Kubernetes Architecture

A **Kubernetes cluster** has a **Control Plane** (the brain) and **Worker Nodes** (the muscles).

```text
                    ☸️ Kubernetes Cluster
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│   🧠 CONTROL PLANE (Master)                                  │
│   ┌────────────────────────────────────────────────────┐     │
│   │ 🚪 kube-apiserver   → Front door (all requests)    │     │
│   │ 🗄️ etcd             → Database (cluster state)     │     │
│   │ 📅 kube-scheduler   → Decides which node gets a Pod│     │
│   │ 🎛️ controller-manager → Keeps desired state        │     │
│   │ ☁️ cloud-controller  → Talks to the cloud provider │     │
│   └────────────────────────────────────────────────────┘     │
│                          │                                   │
│        ┌─────────────────┼─────────────────┐                 │
│        ▼                 ▼                 ▼                 │
│   🖥️ WORKER NODE 1   🖥️ WORKER NODE 2   🖥️ WORKER NODE 3     │
│   ┌────────────┐     ┌────────────┐     ┌────────────┐       │
│   │ 🤖 kubelet │     │ 🤖 kubelet │     │ 🤖 kubelet │       │
│   │ 🌐 kube-proxy│   │ 🌐 kube-proxy│   │ 🌐 kube-proxy│     │
│   │ 🐳 runtime │     │ 🐳 runtime │     │ 🐳 runtime │       │
│   │ 📦 Pods    │     │ 📦 Pods    │     │ 📦 Pods    │       │
│   └────────────┘     └────────────┘     └────────────┘       │
└──────────────────────────────────────────────────────────────┘
```

### 10.4.1 🧠 Control Plane Components

| Component                    | Simple Meaning                                                    |
| ---------------------------- | ----------------------------------------------------------------- |
| 🚪 **kube-apiserver**        | The **front door**. All commands (`kubectl`) go through it        |
| 🗄️ **etcd**                  | A **key-value database** that stores the **whole cluster state**  |
| 📅 **kube-scheduler**        | **Chooses the best node** for each new Pod                        |
| 🎛️ **kube-controller-manager**| Runs controllers that **keep the actual state equal to desired state** |
| ☁️ **cloud-controller-manager**| Connects Kubernetes with **cloud services** (load balancers, disks)|

### 10.4.2 🖥️ Worker Node Components

| Component              | Simple Meaning                                                      |
| ---------------------- | ------------------------------------------------------------------- |
| 🤖 **kubelet**         | **Agent** on each node. Makes sure Pods run as described            |
| 🌐 **kube-proxy**      | Handles **network rules** so Services can reach Pods                |
| 🐳 **Container Runtime** | Runs the containers (**containerd**, CRI-O)                       |

### 10.4.3 🔄 What Happens When We Create a Pod

```text
1. 👨‍💻 kubectl apply -f pod.yaml
        ↓
2. 🚪 API Server receives and saves the request in 🗄️ etcd
        ↓
3. 📅 Scheduler picks a suitable node
        ↓
4. 🤖 kubelet on that node gets the instruction
        ↓
5. 🐳 Container runtime pulls the image and starts the container
        ↓
6. ✅ Pod is Running (kubelet reports status to the API Server)
```

#### 🧠 Easy Memory

```text
🚪 API Server = Receptionist       🗄️ etcd = Record book
📅 Scheduler  = Planner            🤖 kubelet = Node supervisor
```

---

## 10.5 📖 Kubernetes Key Terms

| Term                | Simple Meaning                                                           |
| ------------------- | ------------------------------------------------------------------------ |
| 🌐 **Cluster**      | A group of machines (control plane + worker nodes)                       |
| 🖥️ **Node**         | One machine (VM or physical) in the cluster                              |
| 📦 **Pod**          | The **smallest unit**; one or more containers running together           |
| 🔁 **ReplicaSet**   | Keeps a **fixed number** of identical Pods running                       |
| 🚀 **Deployment**   | Manages ReplicaSets, gives **rolling updates and rollbacks**             |
| 🌐 **Service**      | A **stable address** to reach a group of Pods                            |
| 🌍 **Ingress**      | **HTTP/HTTPS routing** from outside to Services                          |
| 🧱 **Namespace**    | A **virtual cluster** inside the cluster to separate things              |
| ⚙️ **ConfigMap**    | Stores **non-secret configuration**                                      |
| 🔐 **Secret**       | Stores **sensitive data** (passwords, tokens)                            |
| 🏷️ **Label**        | A key-value tag on an object (`app=shop`)                                |
| 🎯 **Selector**     | A way to find objects using labels                                       |
| 📄 **Manifest**     | A YAML file that describes an object                                     |

---

## 10.6 ⚙️ Setting Up Kubernetes

```text
⚙️ Ways to Get Kubernetes
│
├── 💻 Local Learning
│   ├── 🧪 minikube    → Single-node cluster on our laptop
│   ├── 🐳 kind        → Kubernetes in Docker
│   └── 🐳 Docker Desktop (built-in Kubernetes)
│
├── 🔧 Self-Managed
│   └── 🛠️ kubeadm     → Build a real cluster on our own servers
│
└── ☁️ Managed Cloud (Control plane managed by the provider)
    ├── 🟠 Amazon EKS
    ├── 🔵 Azure AKS
    └── 🟢 Google GKE
```

### 10.6.1 🧪 Install kubectl and minikube (Quick Start)

```bash
# Install kubectl (check the official Kubernetes docs for the latest method)
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
kubectl version --client

# Install minikube (check the official minikube docs for the latest method)
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

# Start a local cluster
minikube start --driver=docker

# Check
kubectl get nodes
```

### 10.6.2 ☁️ Managed Kubernetes (EKS)

```text
🏗️ Terraform / eksctl creates the EKS cluster
        ↓
☁️ AWS manages the 🧠 Control Plane
        ↓
🖥️ We manage (or let AWS manage) the Worker Nodes
        ↓
aws eks update-kubeconfig --name my-cluster --region ap-south-1
kubectl get nodes
```

#### 🧠 Simple Meaning

> **Managed Kubernetes = The cloud runs the control plane for us.**

### 10.6.3 📄 kubeconfig

**kubeconfig** (`~/.kube/config`) tells `kubectl` **which cluster to connect to** and **which credentials to use**.

```bash
kubectl config get-contexts           # List clusters/contexts
kubectl config use-context my-ctx     # Switch cluster
kubectl config current-context        # Show the current one
```

---

## 10.7 ⌨️ kubectl — The Command Line Tool

**kubectl** is the tool to **talk to the Kubernetes API Server**.

```text
kubectl <action> <resource> <name> [options]
Example: kubectl get pods -n dev
```

### 10.7.1 🔍 View Resources

```bash
kubectl get nodes
kubectl get pods
kubectl get pods -o wide              # More details (node, IP)
kubectl get pods -n kube-system       # In a specific namespace
kubectl get pods -A                   # In ALL namespaces
kubectl get deployments
kubectl get svc
kubectl get all                       # Common resources together
kubectl describe pod <pod-name>       # Detailed information and events
kubectl logs <pod-name>               # Pod logs
kubectl logs -f <pod-name>            # Follow logs live
kubectl logs <pod-name> -c <container># A specific container
```

### 10.7.2 🏗️ Create and Change Resources

```bash
kubectl apply -f deployment.yaml      # Create or update from a file (recommended)
kubectl delete -f deployment.yaml     # Delete resources defined in a file
kubectl create deployment web --image=nginx    # Quick create
kubectl edit deployment web           # Edit live
kubectl scale deployment web --replicas=5
kubectl set image deployment/web nginx=nginx:1.25
```

### 10.7.3 🔧 Debugging and Access

```bash
kubectl exec -it <pod-name> -- bash           # Shell inside a Pod
kubectl port-forward pod/<pod-name> 8080:80   # Reach a Pod from our laptop
kubectl port-forward svc/web 8080:80          # Reach a Service
kubectl top pods                              # CPU/memory (needs metrics-server)
kubectl get events --sort-by=.metadata.creationTimestamp
```

### 10.7.4 🔄 Rollouts

```bash
kubectl rollout status  deployment/web
kubectl rollout history deployment/web
kubectl rollout undo    deployment/web           # Go back to the previous version
kubectl rollout restart deployment/web
```

### 10.7.5 🧪 Handy Tricks

```bash
kubectl explain pod.spec                          # Documentation of fields
kubectl apply -f x.yaml --dry-run=client          # Test without creating
kubectl create deployment web --image=nginx --dry-run=client -o yaml > web.yaml   # Generate YAML
kubectl api-resources                             # List all resource types
```

#### 🧠 Imperative vs Declarative

| 💻 Imperative                         | 📝 Declarative                              |
| ------------------------------------- | ------------------------------------------- |
| `kubectl create ...`, `kubectl scale` | `kubectl apply -f file.yaml`                |
| Give direct commands                  | Describe the **desired state** in YAML      |
| Quick tests                           | **Recommended** for real work (keep in Git) |

---

## 10.8 📄 YAML Manifest Structure

Every Kubernetes object has **four main parts**:

```yaml
apiVersion: v1            # 1. API version of the object
kind: Pod                 # 2. Type of object
metadata:                 # 3. Name, labels, namespace
  name: my-pod
  labels:
    app: web
spec:                     # 4. Desired state (the details)
  containers:
    - name: nginx
      image: nginx:1.25
```

#### 📖 apiVersion Quick Table

| Object                                  | apiVersion               |
| --------------------------------------- | ------------------------ |
| Pod, Service, ConfigMap, Secret, Namespace, PV, PVC | `v1`         |
| Deployment, ReplicaSet, StatefulSet, DaemonSet | `apps/v1`         |
| Job, CronJob                            | `batch/v1`               |
| Ingress, NetworkPolicy                  | `networking.k8s.io/v1`   |
| HorizontalPodAutoscaler                 | `autoscaling/v2`         |
| Role, ClusterRole, RoleBinding          | `rbac.authorization.k8s.io/v1` |

---

## 10.9 📦 Pods

A **Pod** is the **smallest deployable unit** in Kubernetes. It holds **one or more containers** that **share the same network and storage**.

```text
📦 Pod
├── 🐳 Container 1 (main app)
├── 🐳 Container 2 (helper / sidecar)  ← optional
├── 🌐 One shared IP address
└── 💾 Shared volumes
```

#### 💻 Pod Example

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: web-pod
  labels:
    app: web
spec:
  containers:
    - name: nginx
      image: nginx:1.25
      ports:
        - containerPort: 80
```

### 10.9.1 ⭐ Key Facts

- 🏷️ A Pod gets **its own IP address**
- ⏳ Pods are **temporary** — when a Pod dies, a **new Pod with a new IP** replaces it
- 1️⃣ Usually **one main container per Pod**
- ⚠️ We rarely create bare Pods. We use **Deployments**.

### 10.9.2 🔄 Pod Phases

| Phase         | Meaning                                       |
| ------------- | --------------------------------------------- |
| `Pending`     | Accepted, waiting to be scheduled / pulling image |
| `Running`     | At least one container is running             |
| `Succeeded`   | All containers finished successfully          |
| `Failed`      | A container ended with an error               |
| `Unknown`     | State cannot be found                         |

### 10.9.3 🚨 Common Pod Errors

| Status                | Meaning / Usual Cause                                    |
| --------------------- | -------------------------------------------------------- |
| `ImagePullBackOff`    | Cannot download the image (wrong name, no access)        |
| `CrashLoopBackOff`    | Container keeps crashing and restarting                  |
| `Pending`             | No node has enough resources, or scheduling problem      |
| `OOMKilled`           | Container used more memory than its limit                |

#### 🔧 Troubleshooting Steps

```bash
kubectl describe pod <pod>      # Check the "Events" section
kubectl logs <pod>              # See application errors
kubectl logs <pod> --previous   # Logs of the crashed container
```

---

## 10.10 🚀 Deployments and ReplicaSets

### 10.10.1 🔁 ReplicaSet

A **ReplicaSet** makes sure **a fixed number of identical Pods** are always running.

```text
🔁 ReplicaSet (replicas: 3)
├── 📦 Pod 1
├── 📦 Pod 2
└── 📦 Pod 3     ← if one dies, a new one is created
```

### 10.10.2 🚀 Deployment

A **Deployment** manages **ReplicaSets** and gives:

- 🔄 **Rolling updates**
- ⏪ **Rollbacks**
- 📈 **Scaling**
- 🩹 **Self-healing**

```text
🚀 Deployment
    └── 🔁 ReplicaSet (version 2 — current)
          ├── 📦 Pod
          ├── 📦 Pod
          └── 📦 Pod
    └── 🔁 ReplicaSet (version 1 — old, kept for rollback)
```

#### 💻 Deployment Example

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: shop-app
  labels:
    app: shop
spec:
  replicas: 3
  selector:
    matchLabels:
      app: shop
  strategy:
    type: RollingUpdate
    rollingUpdate:
      maxSurge: 1
      maxUnavailable: 0
  template:                         # Pod template
    metadata:
      labels:
        app: shop                   # Must match the selector
    spec:
      containers:
        - name: shop-app
          image: myuser/shop-app:1.0
          ports:
            - containerPort: 8080
          resources:
            requests:
              cpu: "250m"
              memory: "256Mi"
            limits:
              cpu: "500m"
              memory: "512Mi"
```

#### ⚠️ Important

> The **`selector.matchLabels`** must match the **Pod template labels**. If not, the Deployment will not work.

### 10.10.3 🔄 Rolling Update

```text
v1 v1 v1   (3 Pods, old version)
  ↓
v1 v1 v1 v2     ← start a new Pod (maxSurge)
v1 v1 v2        ← remove an old Pod
v1 v1 v2 v2
v1 v2 v2
v2 v2 v2        ← all updated, no downtime ✅
```

| Setting          | Meaning                                              |
| ---------------- | ---------------------------------------------------- |
| `maxSurge`       | How many **extra** Pods can be created during update |
| `maxUnavailable` | How many Pods can be **unavailable** during update   |

#### ⏪ Rollback

```bash
kubectl rollout undo deployment/shop-app
```

### 10.10.4 🔄 Update Strategies

| Strategy          | Meaning                                                   |
| ----------------- | --------------------------------------------------------- |
| `RollingUpdate`   | Replace Pods gradually (**default**, no downtime)         |
| `Recreate`        | Stop all old Pods, then start new Pods (downtime)         |

---

## 10.11 🌐 Services

Pods get **new IPs when they restart**. A **Service** gives a **stable name and IP** to reach a **group of Pods**.

```text
🌐 Service "shop-svc"  (stable IP + DNS name)
        │ selects Pods using labels (app=shop)
        ├──► 📦 Pod 1 (10.1.0.5)
        ├──► 📦 Pod 2 (10.1.0.8)
        └──► 📦 Pod 3 (10.1.0.12)
```

### 10.11.1 🧩 Service Types

```text
🌐 Service Types
│
├── 🔒 ClusterIP     → Only inside the cluster (default)
├── 🚪 NodePort      → Opens a port on every node (30000–32767)
├── ⚖️ LoadBalancer  → Creates a cloud load balancer (AWS ELB)
└── 🔗 ExternalName  → Maps to an external DNS name
```

| Type             | Access From              | Used For                                    |
| ---------------- | ------------------------ | ------------------------------------------- |
| 🔒 **ClusterIP** | Inside the cluster only  | Internal services (backend, database)       |
| 🚪 **NodePort**  | `NodeIP:NodePort`        | Testing, simple external access             |
| ⚖️ **LoadBalancer** | Cloud load balancer URL | Production external access on cloud         |
| 🔗 **ExternalName** | DNS alias             | Pointing to an outside service              |

#### 🏗️ Flow

```text
🌍 User ──► ⚖️ LoadBalancer ──► 🚪 NodePort ──► 🔒 ClusterIP ──► 📦 Pods
```

### 10.11.2 💻 Service Example

```yaml
apiVersion: v1
kind: Service
metadata:
  name: shop-svc
spec:
  type: ClusterIP
  selector:
    app: shop              # Sends traffic to Pods with this label
  ports:
    - port: 80             # Service port
      targetPort: 8080     # Container port
```

```yaml
# LoadBalancer example
apiVersion: v1
kind: Service
metadata:
  name: shop-lb
spec:
  type: LoadBalancer
  selector:
    app: shop
  ports:
    - port: 80
      targetPort: 8080
```

### 10.11.3 🔍 Service Discovery (DNS)

Inside the cluster, Pods can reach a Service **by name** (CoreDNS).

```text
http://shop-svc                         → Same namespace
http://shop-svc.dev                     → Another namespace (dev)
http://shop-svc.dev.svc.cluster.local   → Full name
```

#### 🧠 Remember

> **Service = Stable address for changing Pods.**

---

## 10.12 🌍 Ingress

An **Ingress** routes **HTTP/HTTPS traffic from outside** to **Services** using **hostnames and paths**.

```text
🌍 Internet
      │
      ▼
🌍 Ingress Controller (Nginx / AWS ALB)
      │
      ├── shop.example.com/       ──► 🌐 Service: shop-svc
      ├── shop.example.com/api    ──► 🌐 Service: api-svc
      └── blog.example.com        ──► 🌐 Service: blog-svc
```

#### 💻 Ingress Example

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: shop-ingress
spec:
  ingressClassName: nginx
  rules:
    - host: shop.example.com
      http:
        paths:
          - path: /
            pathType: Prefix
            backend:
              service:
                name: shop-svc
                port:
                  number: 80
  tls:
    - hosts:
        - shop.example.com
      secretName: shop-tls
```

#### ⚠️ Important

> An **Ingress needs an Ingress Controller** (like **ingress-nginx** or the **AWS Load Balancer Controller**). The Ingress object alone does nothing.

| 🌐 Service LoadBalancer                | 🌍 Ingress                                   |
| -------------------------------------- | -------------------------------------------- |
| One load balancer **per service**      | **One entry point** for many services        |
| Works at TCP/UDP level                 | Works at HTTP/HTTPS level (host, path rules) |
| Costs more with many services          | Saves cost                                   |

---

## 10.13 🧱 Namespaces

A **Namespace** **divides one cluster into virtual sections**.

```text
☸️ Cluster
├── 🧱 Namespace: dev
├── 🧱 Namespace: test
├── 🧱 Namespace: prod
└── 🧱 Namespace: kube-system   (Kubernetes system components)
```

```bash
kubectl get namespaces
kubectl create namespace dev
kubectl get pods -n dev
kubectl config set-context --current --namespace=dev     # Set default namespace
```

#### 🎯 Used For

- 👥 Separate teams and environments
- 📏 Apply **resource quotas** and **access rules** per namespace

#### 🔤 Default Namespaces

| Namespace          | Purpose                                    |
| ------------------ | ------------------------------------------ |
| `default`          | Used when no namespace is given            |
| `kube-system`      | Kubernetes system components               |
| `kube-public`      | Public data readable by everyone           |
| `kube-node-lease`  | Node heartbeat data                        |

---

## 10.14 ⚙️ ConfigMaps and 🔐 Secrets

### 10.14.1 ⚙️ ConfigMap

Stores **non-secret configuration** (settings, URLs).

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: shop-config
data:
  APP_ENV: "production"
  DB_HOST: "mysql-svc"
```

### 10.14.2 🔐 Secret

Stores **sensitive data** (passwords, tokens).

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: shop-secret
type: Opaque
stringData:
  DB_PASSWORD: "S3cr3tPass"
```

```bash
kubectl create secret generic shop-secret --from-literal=DB_PASSWORD=S3cr3tPass
```

#### ⚠️ Important

> **Secrets are only Base64-encoded by default — not strongly encrypted.** Enable **encryption at rest**, restrict access with **RBAC**, and consider tools like **AWS Secrets Manager**, **External Secrets** or **Sealed Secrets**.

### 10.14.3 🔌 Use Them in a Pod

```yaml
spec:
  containers:
    - name: shop-app
      image: myuser/shop-app:1.0
      env:
        - name: APP_ENV
          valueFrom:
            configMapKeyRef:
              name: shop-config
              key: APP_ENV
        - name: DB_PASSWORD
          valueFrom:
            secretKeyRef:
              name: shop-secret
              key: DB_PASSWORD
      # OR load everything at once:
      envFrom:
        - configMapRef:
            name: shop-config
```

#### 🧠 Easy Memory

```text
⚙️ ConfigMap = Normal settings
🔐 Secret    = Passwords and tokens
```

---

## 10.15 💾 Storage

Containers lose data when they restart. Kubernetes provides **persistent storage**.

```text
💾 Storage Objects
│
├── 💽 PersistentVolume (PV)       → Actual storage (EBS disk, NFS)
├── 📋 PersistentVolumeClaim (PVC) → A request for storage by a Pod
└── 🏷️ StorageClass                → Defines how storage is created dynamically
```

#### 🏗️ Flow

```text
📦 Pod ──uses──► 📋 PVC (request: 10Gi) ──binds──► 💽 PV (10Gi EBS disk)
                                  ▲
                      🏷️ StorageClass creates the PV automatically
```

#### 💻 PVC Example

```yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: db-pvc
spec:
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 10Gi
  storageClassName: gp3
```

```yaml
# Use the PVC in a Pod
spec:
  containers:
    - name: mysql
      image: mysql:8
      volumeMounts:
        - name: data
          mountPath: /var/lib/mysql
  volumes:
    - name: data
      persistentVolumeClaim:
        claimName: db-pvc
```

#### 🔤 Access Modes

| Mode              | Meaning                                        |
| ----------------- | ---------------------------------------------- |
| `ReadWriteOnce`   | Mounted read-write by **one node**             |
| `ReadOnlyMany`    | Mounted read-only by **many nodes**            |
| `ReadWriteMany`   | Mounted read-write by **many nodes**           |

---

## 10.16 🗂️ Other Workload Types

| Workload              | Used For                                                    |
| --------------------- | ----------------------------------------------------------- |
| 🚀 **Deployment**     | Stateless apps (web apps, APIs)                             |
| 🗄️ **StatefulSet**    | Stateful apps (databases) — stable names and storage        |
| 👥 **DaemonSet**      | One Pod on **every node** (log agents, monitoring agents)   |
| ⏱️ **Job**            | Run a task **once** until it completes                      |
| ⏰ **CronJob**        | Run a Job **on a schedule**                                 |

#### ⏰ CronJob Example

```yaml
apiVersion: batch/v1
kind: CronJob
metadata:
  name: nightly-report
spec:
  schedule: "0 2 * * *"            # Every day at 2:00 AM
  jobTemplate:
    spec:
      template:
        spec:
          containers:
            - name: report
              image: myuser/report-job:1.0
          restartPolicy: OnFailure
```

---

## 10.17 🩺 Health Checks (Probes)

**Probes** let Kubernetes **check if a container is healthy**.

```text
🩺 Probe Types
│
├── 💓 Liveness Probe   → "Is it alive?"  If it fails → container is RESTARTED
├── ✅ Readiness Probe  → "Is it ready for traffic?" If it fails → REMOVED from Service
└── 🚀 Startup Probe    → "Has it finished starting?" (for slow apps)
```

#### 💻 Example

```yaml
containers:
  - name: shop-app
    image: myuser/shop-app:1.0
    livenessProbe:
      httpGet:
        path: /actuator/health/liveness
        port: 8080
      initialDelaySeconds: 30
      periodSeconds: 10
    readinessProbe:
      httpGet:
        path: /actuator/health/readiness
        port: 8080
      initialDelaySeconds: 10
      periodSeconds: 5
```

#### 🧠 Easy Memory

```text
💓 Liveness  = Dead?  → Restart it
✅ Readiness = Ready? → Send traffic only if yes
```

---

## 10.18 📏 Resource Requests and Limits

```yaml
resources:
  requests:            # Minimum guaranteed (used by the scheduler)
    cpu: "250m"
    memory: "256Mi"
  limits:              # Maximum allowed
    cpu: "500m"
    memory: "512Mi"
```

| Setting      | Meaning                                                         |
| ------------ | --------------------------------------------------------------- |
| `requests`   | Amount **reserved**; scheduler finds a node with this much free |
| `limits`     | **Maximum** the container can use                               |
| `250m`       | 250 millicores = **0.25 CPU**                                   |
| `256Mi`      | 256 mebibytes of memory                                         |

#### ⚠️ What Happens at the Limit

```text
CPU over the limit    → Container is slowed down (throttled)
Memory over the limit → Container is killed (OOMKilled)
```

> **Always set requests and limits** so one Pod does not harm others.

---

## 10.19 📈 Autoscaling

### 10.19.1 📈 Horizontal Pod Autoscaler (HPA)

HPA **adds or removes Pods** based on **CPU / memory (or custom metrics)**.

```yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: shop-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: shop-app
  minReplicas: 2
  maxReplicas: 10
  metrics:
    - type: Resource
      resource:
        name: cpu
        target:
          type: Utilization
          averageUtilization: 70
```

```text
CPU above 70%  → ➕ Add Pods (up to 10)
CPU below 70%  → ➖ Remove Pods (down to 2)
```

> HPA needs the **metrics-server** installed.

### 10.19.2 🗂️ Types of Autoscaling

| Type                         | What It Scales                                  |
| ---------------------------- | ----------------------------------------------- |
| 📈 **HPA**                   | Number of **Pods**                              |
| 📏 **VPA**                   | **Size (CPU/memory)** of Pods                   |
| 🖥️ **Cluster Autoscaler / Karpenter** | Number of **Nodes**                    |

---

## 10.20 🔐 Security and RBAC

**RBAC = Role-Based Access Control** decides **who can do what** in the cluster.

```text
🔐 RBAC Objects
│
├── 👤 ServiceAccount     → Identity for Pods / applications
├── 🎭 Role               → Permissions inside one namespace
├── 🎭 ClusterRole        → Permissions across the whole cluster
├── 🔗 RoleBinding        → Gives a Role to a user / ServiceAccount (namespace)
└── 🔗 ClusterRoleBinding → Gives a ClusterRole (cluster-wide)
```

#### 💻 Example: Read-Only Pods in the dev Namespace

```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  namespace: dev
  name: pod-reader
rules:
  - apiGroups: [""]
    resources: ["pods"]
    verbs: ["get", "list", "watch"]
---
apiVersion: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  namespace: dev
  name: read-pods
subjects:
  - kind: User
    name: john
    apiGroup: rbac.authorization.k8s.io
roleRef:
  kind: Role
  name: pod-reader
  apiGroup: rbac.authorization.k8s.io
```

#### ✅ Security Best Practices

- 🔒 Use **RBAC** with least privilege
- 🔐 Protect **Secrets** (encryption at rest, external secret managers)
- 🚧 Use **Network Policies** to control Pod-to-Pod traffic
- 👤 Run containers as **non-root**
- 🔍 **Scan images** and use trusted registries
- 🔄 Keep the cluster **updated**

---

## 10.21 ⛵ Helm — The Package Manager

**Helm** is the **package manager for Kubernetes**. A **chart** is a package of Kubernetes YAML templates.

```text
⛵ Helm
│
├── 📦 Chart     → Package of Kubernetes templates
├── 🚀 Release   → An installed instance of a chart
└── 🗄️ Repository → Place where charts are stored
```

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm search repo nginx
helm install my-nginx bitnami/nginx
helm list
helm upgrade my-nginx bitnami/nginx --set replicaCount=3
helm rollback my-nginx 1
helm uninstall my-nginx
```

#### 🧠 Simple Meaning

> **Helm = apt/yum for Kubernetes**

---

## 10.22 🔗 Kubernetes in a CI/CD Pipeline

```text
🐙 GitHub → 🤖 Jenkins
              │
              ├── 🔨 Maven build + 🔍 SonarQube + 📦 Nexus
              ├── 🐳 docker build + docker push
              └── ☸️ kubectl set image deployment/shop-app shop-app=myuser/shop-app:42
                              │
                              ▼
                     🔄 Rolling update (no downtime)
```

#### 💻 Jenkins Stage

```groovy
stage('Deploy to Kubernetes') {
    steps {
        withCredentials([file(credentialsId: 'kubeconfig', variable: 'KUBECONFIG')]) {
            sh "kubectl set image deployment/shop-app shop-app=myuser/shop-app:${env.BUILD_NUMBER}"
            sh 'kubectl rollout status deployment/shop-app --timeout=120s'
        }
    }
}
```

> 💡 **GitOps** (Argo CD / Flux) is another popular way: the cluster **pulls** the desired state from Git.

---

## 10.23 🏆 Kubernetes Best Practices

```text
✅ Kubernetes Best Practices
│
├── 📝 Store YAML in Git and use kubectl apply / Helm / GitOps
├── 🏷️ Use clear labels and namespaces
├── 📏 Set resource requests and limits
├── 🩺 Add liveness and readiness probes
├── 🚀 Use Deployments (not bare Pods)
├── 🔖 Use fixed image tags (not :latest)
├── 🔐 Use RBAC, Secrets safely, Network Policies
├── 📈 Use HPA for scaling
└── 📊 Monitor with Prometheus and Grafana
```

---

## 10.24 🏗️ Real Example: Deploy a Web App

### 🎯 Requirement

Run **3 copies** of a web app, expose it to users, and keep configuration outside the image.

### 📁 Files

#### 📄 `app.yaml`

```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: shop
---
apiVersion: v1
kind: ConfigMap
metadata:
  name: shop-config
  namespace: shop
data:
  APP_ENV: "production"
---
apiVersion: v1
kind: Secret
metadata:
  name: shop-secret
  namespace: shop
type: Opaque
stringData:
  DB_PASSWORD: "S3cr3tPass"
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: shop-app
  namespace: shop
spec:
  replicas: 3
  selector:
    matchLabels:
      app: shop
  template:
    metadata:
      labels:
        app: shop
    spec:
      containers:
        - name: shop-app
          image: myuser/shop-app:1.0
          ports:
            - containerPort: 8080
          envFrom:
            - configMapRef:
                name: shop-config
          env:
            - name: DB_PASSWORD
              valueFrom:
                secretKeyRef:
                  name: shop-secret
                  key: DB_PASSWORD
          resources:
            requests:
              cpu: "250m"
              memory: "256Mi"
            limits:
              cpu: "500m"
              memory: "512Mi"
          readinessProbe:
            httpGet:
              path: /
              port: 8080
            initialDelaySeconds: 10
---
apiVersion: v1
kind: Service
metadata:
  name: shop-svc
  namespace: shop
spec:
  type: LoadBalancer
  selector:
    app: shop
  ports:
    - port: 80
      targetPort: 8080
```

### 🪜 Run It

```bash
kubectl apply -f app.yaml
kubectl get all -n shop
kubectl get svc shop-svc -n shop          # Get the external address
kubectl logs -f deployment/shop-app -n shop

# Scale
kubectl scale deployment shop-app --replicas=5 -n shop

# Update to a new version (rolling update)
kubectl set image deployment/shop-app shop-app=myuser/shop-app:2.0 -n shop
kubectl rollout status deployment/shop-app -n shop

# Roll back if there is a problem
kubectl rollout undo deployment/shop-app -n shop

# Delete everything
kubectl delete -f app.yaml
```

### 🏗️ What Happens

```text
🌍 User
   │
   ▼
⚖️ LoadBalancer Service (shop-svc)
   │
   ├──► 📦 shop-app Pod 1  ┐
   ├──► 📦 shop-app Pod 2  ├── from Deployment (3 replicas)
   └──► 📦 shop-app Pod 3  ┘      uses ⚙️ ConfigMap + 🔐 Secret
```

---

## 📌🧠 Kubernetes Quick Revision

```text
☸️ Kubernetes
│
├── 🏛️ Architecture
│   ├── 🧠 Control Plane: API Server, etcd, Scheduler, Controller Manager
│   └── 🖥️ Worker Node: kubelet, kube-proxy, container runtime
│
├── 📦 Workloads
│   ├── Pod
│   ├── ReplicaSet
│   ├── Deployment (rolling update, rollback)
│   ├── StatefulSet, DaemonSet
│   └── Job, CronJob
│
├── 🌐 Networking
│   ├── Service: ClusterIP / NodePort / LoadBalancer
│   └── Ingress (+ Ingress Controller)
│
├── ⚙️ Configuration
│   ├── ConfigMap
│   ├── Secret
│   └── Namespace, Labels, Selectors
│
├── 💾 Storage
│   └── PV, PVC, StorageClass
│
├── 🩺 Reliability
│   ├── Probes: liveness, readiness, startup
│   ├── Requests and Limits
│   └── HPA (autoscaling)
│
├── 🔐 Security
│   └── RBAC, ServiceAccount, Network Policy
│
└── 🧰 Tools
    ├── kubectl
    ├── Helm
    └── minikube / kubeadm / EKS
```

---

## 🧠⚡ Kubernetes One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| ☸️ **Kubernetes**          | Orchestrator That Runs and Manages Containers       |
| 🌐 **Cluster**             | Control Plane + Worker Nodes                        |
| 🚪 **API Server**          | Front Door of the Cluster                           |
| 🗄️ **etcd**                | Database of Cluster State                           |
| 📅 **Scheduler**           | Chooses Node for a Pod                              |
| 🤖 **kubelet**             | Agent on Each Node                                  |
| 📦 **Pod**                 | Smallest Unit (One or More Containers)              |
| 🔁 **ReplicaSet**          | Keeps N Pods Running                                |
| 🚀 **Deployment**          | Rolling Updates + Rollbacks for Pods                |
| 🌐 **Service**             | Stable Address for Pods                             |
| 🔒 **ClusterIP**           | Internal Only (Default)                             |
| 🚪 **NodePort**            | Port on Every Node (30000–32767)                    |
| ⚖️ **LoadBalancer**        | Cloud Load Balancer                                 |
| 🌍 **Ingress**             | HTTP Routing by Host and Path                       |
| 🧱 **Namespace**           | Virtual Cluster Section                             |
| ⚙️ **ConfigMap**           | Normal Settings                                     |
| 🔐 **Secret**              | Passwords and Tokens                                |
| 💾 **PV / PVC**            | Storage and Request for Storage                     |
| 💓 **Liveness Probe**      | Dead? Restart It                                    |
| ✅ **Readiness Probe**     | Ready? Send Traffic                                 |
| 📈 **HPA**                 | Auto-Scale Pods                                     |
| ⛵ **Helm**                | Package Manager for Kubernetes                      |
| ⌨️ **kubectl**             | CLI for Kubernetes                                  |

---

## 🗺️ Kubernetes Learning Map

```text
                          ☸️ Kubernetes
                                │
       ┌────────────────────────┼────────────────────────┐
       │                        │                        │
       ▼                        ▼                        ▼
  ARCHITECTURE               WORKLOADS               NETWORKING
       │                        │                        │
       ├── Control Plane        ├── Pod                  ├── Service
       ├── Worker Nodes         ├── ReplicaSet           │    ├── ClusterIP
       └── kubectl              ├── Deployment           │    ├── NodePort
                                ├── StatefulSet          │    └── LoadBalancer
                                ├── DaemonSet            └── Ingress
                                └── Job / CronJob
       │
       ▼
  CONFIG & STORAGE
       │
       ├── ConfigMap / Secret
       ├── Namespace / Labels
       └── PV / PVC / StorageClass
       │
       ▼
  RELIABILITY & SCALE
       │
       ├── Probes
       ├── Requests / Limits
       └── HPA / Cluster Autoscaler
       │
       ▼
  SECURITY & TOOLS
       │
       ├── RBAC / Network Policy
       ├── Helm
       └── CI/CD (Jenkins, GitOps)
```

---

## ⭐ Kubernetes Final Memory

```text
Kubernetes
 │
 ├── What is it?
 │      └── Container orchestration platform
 │
 ├── Smallest unit?
 │      └── Pod
 │
 ├── How to run many Pods with rolling updates?
 │      └── Deployment
 │
 ├── How to give Pods a stable address?
 │      └── Service
 │
 ├── How to route HTTP traffic from outside?
 │      └── Ingress (needs an Ingress Controller)
 │
 ├── Where to keep settings and passwords?
 │      └── ConfigMap and Secret
 │
 ├── How to keep data after Pod restart?
 │      └── PV and PVC
 │
 ├── How to scale automatically?
 │      └── HPA
 │
 ├── How to roll back a bad update?
 │      └── kubectl rollout undo
 │
 └── Which tool talks to the cluster?
        └── kubectl
```

---

# 🔥 PART 11 — Prometheus — Metrics and Alerting

> **Prometheus = A system that regularly asks our servers "How are you?" and remembers the answers**

---

## 11.1 🔥 What is Prometheus?

> **Prometheus = Open-source monitoring and alerting system that stores metrics as time-series data**

Prometheus **collects numbers (metrics) from our servers and applications at regular intervals**, **stores them**, lets us **query them**, and **sends alerts** when something goes wrong.

It was built at **SoundCloud** and is now a **CNCF graduated project** (just like Kubernetes).

#### 📦 Prometheus Is Used To

- 📈 **Collect metrics** (CPU, memory, disk, requests, errors)
- 🗄️ **Store** them as time-series data
- 🔍 **Query** them with **PromQL**
- 🚨 **Alert** when a rule is broken (with Alertmanager)
- ☸️ **Monitor** Kubernetes, Docker and microservices

#### 🏗️ Prometheus Basic Idea

```text
🖥️ Servers / 🐳 Containers / ⚙️ Apps
        ▲
        │ 🔄 Prometheus PULLS (scrapes) metrics every 15 seconds
        │
🔥 Prometheus Server ──► 🗄️ Time-Series Database
        │
        ├──► 🔍 PromQL queries ──► 📈 Grafana dashboards
        └──► 🚨 Alert rules ──► 🔔 Alertmanager ──► 📧 Email / 💬 Slack
```

#### 🧠 Easy Memory

> **Prometheus = A system that regularly asks "How are you?" to all our servers and remembers the answers**

---

## 11.2 🤔 Why Do We Use Prometheus?

### ❌ Without Monitoring

```text
💥 Server runs out of memory at night
        ↓
😴 Nobody knows
        ↓
👥 Users face downtime
        ↓
📞 Customers complain first
```

### ✅ With Prometheus

```text
📈 Prometheus collects memory usage every 15 seconds
        ↓
🚨 Alert rule: "memory > 90% for 5 minutes"
        ↓
📧 Team gets an alert before users are affected
```

#### ⭐ Main Reasons

- 🔄 **Pull model** — easy to manage and detect "target down"
- 🏷️ **Labels** — flexible, powerful data model
- 🔍 **PromQL** — strong query language
- 🚨 **Built-in alerting** (with Alertmanager)
- ☸️ **Great for Kubernetes** and dynamic cloud systems (service discovery)
- 🆓 **Free and open source**
- 🧩 Hundreds of **exporters** for databases, servers, hardware and more

---

## 11.3 🧰 What Does Prometheus Provide?

Prometheus provides:

- 🔎 Metrics Collection (Scraping)
- 🗄️ Time-Series Database (TSDB)
- 🔍 PromQL (Query Language)
- 🚨 Alerting Rules
- 🧾 Recording Rules
- 🔭 Service Discovery
- 🌐 Web UI and HTTP API
- 🔌 Exporters ecosystem

---

## 11.4 🏛️ Prometheus Architecture

```text
┌────────────────────────── 🔥 Prometheus Server ──────────────────────────┐
│                                                                           │
│  🔎 Retrieval (Scraper) ──► 🗄️ TSDB (Storage) ──► 🌐 HTTP Server / PromQL │
│          ▲                                                  │             │
└──────────┼──────────────────────────────────────────────────┼─────────────┘
           │ pull (scrape)                                    │
   ┌───────┴─────────────┐                          ┌─────────┴─────────┐
   │                     │                          ▼                   ▼
🔌 Exporters         ⚙️ Apps with           📈 Grafana         🚨 Alertmanager
(node_exporter,      /metrics endpoint        (dashboards)            │
 cAdvisor ...)                                                        ▼
                                                              📧 Email / 💬 Slack
🔄 Pushgateway ◄── (short-lived jobs push metrics)
🔭 Service Discovery (Kubernetes, EC2, Consul) tells Prometheus where targets are
```

### 11.4.1 📖 Simple Definitions

| Component              | Simple Meaning                                                          |
| ---------------------- | ----------------------------------------------------------------------- |
| 🔥 **Prometheus Server** | Scrapes, stores and queries metrics (port **9090**)                   |
| 🎯 **Target**          | Something Prometheus monitors (a server, an app)                        |
| 🔌 **Exporter**        | A small program that **exposes metrics** of a system in Prometheus format |
| 📄 **/metrics endpoint** | A web page that shows current metric values as text                   |
| 🔄 **Scrape**          | One collection of metrics from a target                                 |
| 🗄️ **TSDB**            | The built-in time-series database                                       |
| 🔍 **PromQL**          | The query language                                                      |
| 🚨 **Alertmanager**    | Handles alerts: grouping, silencing and sending notifications (port **9093**) |
| 🔄 **Pushgateway**     | Lets short-lived jobs **push** metrics so Prometheus can scrape them    |
| 🔭 **Service Discovery** | Finds targets automatically (Kubernetes, EC2, Consul)                 |

#### 🧠 Remember

> **Prometheus = Collect + Store + Query + Alert.** Visualization is done by **Grafana**.

---

## 11.5 🔄 Pull Model vs Push Model

```text
🔄 Pull Model (Prometheus)           📤 Push Model (Others)
Server asks targets for metrics      Targets send metrics to the server
```

| 🔄 Pull (Prometheus)                         | 📤 Push                                      |
| -------------------------------------------- | -------------------------------------------- |
| Prometheus **scrapes** targets               | Targets **send** data                        |
| Easy to see if a target is **down** (`up == 0`) | Harder to know if a sender stopped        |
| Central control of what is monitored         | Each sender controls itself                  |
| Targets must be reachable by Prometheus      | Works for short jobs and firewalls           |

> 💡 For **short-lived jobs** (like batch scripts), use the **Pushgateway**.

---

## 11.6 🧱 Data Model and Metric Types

### 11.6.1 🏷️ Metrics and Labels

Every metric has a **name** and **labels** (key-value tags).

```text
http_requests_total{method="GET", status="200", instance="web1:8080"}  1027
└────────┬────────┘ └──────────────────┬───────────────────────────┘  └─┬─┘
    Metric name                      Labels                           Value
```

```text
🏷️ Time Series = Metric name + Labels + (Timestamp, Value) pairs
```

#### 🧠 Simple Meaning

> **Labels let us slice data: by server, by status code, by region, by job.**

### 11.6.2 🗂️ The 4 Metric Types

```text
📊 Metric Types
│
├── 🔢 Counter    → Only goes UP (resets on restart)
├── 🌡️ Gauge      → Goes UP and DOWN
├── 📊 Histogram  → Counts values in buckets (for latency, sizes)
└── 📋 Summary    → Calculates quantiles on the client side
```

| Type             | Meaning                                              | Example                                     |
| ---------------- | ---------------------------------------------------- | ------------------------------------------- |
| 🔢 **Counter**   | A value that **only increases**                      | `http_requests_total`, errors total         |
| 🌡️ **Gauge**     | A value that can **go up and down**                  | Memory usage, temperature, active users     |
| 📊 **Histogram** | Puts observations in **buckets** (can compute percentiles) | Request duration                      |
| 📋 **Summary**   | Pre-calculated **quantiles** (like 0.95)             | Request duration (client-side)              |

#### 🧠 Easy Memory

```text
🔢 Counter = Odometer of a car (only increases) → use rate()
🌡️ Gauge   = Speedometer (up and down)
📊 Histogram = Count of requests in time buckets
```

#### ⚠️ Important

> **For a Counter, never look at the raw value. Use `rate()` to see "per second".**

---

## 11.7 ⚙️ Installing Prometheus

Prometheus runs on **port 9090**.

### 11.7.1 🐳 Docker (Easy)

```bash
docker run -d --name prometheus \
  -p 9090:9090 \
  -v $(pwd)/prometheus.yml:/etc/prometheus/prometheus.yml \
  -v prometheus_data:/prometheus \
  prom/prometheus
```

Open: `http://<server-ip>:9090`

### 11.7.2 🐧 Install From the Official Binary

```bash
# Download from https://prometheus.io/download/ (check the latest version)
wget https://github.com/prometheus/prometheus/releases/download/v<version>/prometheus-<version>.linux-amd64.tar.gz
tar xvf prometheus-<version>.linux-amd64.tar.gz
cd prometheus-<version>.linux-amd64

./prometheus --config.file=prometheus.yml
```

> 💡 For production, create a **systemd service** and a dedicated **prometheus user**.

### 11.7.3 📁 Important Files and Settings

| Item                    | Meaning                                                    |
| ----------------------- | ---------------------------------------------------------- |
| `prometheus.yml`        | Main configuration file                                    |
| `--storage.tsdb.path`   | Folder where data is stored                                |
| `--storage.tsdb.retention.time` | How long to keep data (**default 15 days**)        |
| `--web.enable-lifecycle`| Allows reloading config using HTTP                         |

#### 🔓 Firewall

```text
Open port 9090 only to trusted users / Grafana
```

---

## 11.8 📄 Configuration (`prometheus.yml`)

```yaml
global:
  scrape_interval: 15s          # How often to scrape
  evaluation_interval: 15s      # How often to check rules

rule_files:
  - "alert_rules.yml"

alerting:
  alertmanagers:
    - static_configs:
        - targets: ["localhost:9093"]

scrape_configs:
  - job_name: "prometheus"
    static_configs:
      - targets: ["localhost:9090"]

  - job_name: "node"
    static_configs:
      - targets:
          - "192.168.1.10:9100"
          - "192.168.1.11:9100"
        labels:
          env: "production"

  - job_name: "spring-app"
    metrics_path: /actuator/prometheus
    static_configs:
      - targets: ["192.168.1.20:8080"]
```

### 11.8.1 📖 Understanding It

| Setting                | Meaning                                                      |
| ---------------------- | ------------------------------------------------------------ |
| `scrape_interval`      | How often Prometheus collects metrics                        |
| `evaluation_interval`  | How often alert/recording rules are checked                  |
| `rule_files`           | Files with alert and recording rules                         |
| `alerting`             | Where Alertmanager is                                        |
| `scrape_configs`       | List of jobs (what to scrape)                                |
| `job_name`             | Name of a group of targets (becomes the `job` label)         |
| `static_configs`       | Fixed list of targets                                        |
| `metrics_path`         | URL path of metrics (default `/metrics`)                     |

#### 🔄 Reload the Configuration

```bash
# Check the config first
promtool check config prometheus.yml

# Reload without restart (needs --web.enable-lifecycle)
curl -X POST http://localhost:9090/-/reload
```

#### 🔍 Check Targets

```text
Prometheus UI → Status → Targets   (UP = working, DOWN = problem)
```

---

## 11.9 🔌 Exporters

An **exporter** is a **helper program** that **collects metrics from a system** and **shows them at `/metrics`** in Prometheus format.

```text
🔌 Popular Exporters
│
├── 🖥️ node_exporter       → Linux server metrics (CPU, memory, disk, network)  [port 9100]
├── 🪟 windows_exporter    → Windows server metrics
├── 🐳 cAdvisor            → Docker container metrics
├── 🗄️ mysqld_exporter     → MySQL metrics
├── 🐘 postgres_exporter   → PostgreSQL metrics
├── 🌐 blackbox_exporter   → Probe websites and ports (HTTP, TCP, ping)
├── ☸️ kube-state-metrics  → Kubernetes object metrics
└── 📦 JMX exporter        → Java application metrics
```

### 11.9.1 🖥️ Install node_exporter

```bash
# Download from https://prometheus.io/download/ (node_exporter)
wget https://github.com/prometheus/node_exporter/releases/download/v<version>/node_exporter-<version>.linux-amd64.tar.gz
tar xvf node_exporter-<version>.linux-amd64.tar.gz
cd node_exporter-<version>.linux-amd64
./node_exporter &

# Check
curl http://localhost:9100/metrics | head
```

```bash
# Or with Docker
docker run -d --name node-exporter --net=host --pid=host \
  -v "/:/host:ro,rslave" prom/node-exporter --path.rootfs=/host
```

#### 🔓 Firewall

```text
Open port 9100 only for the Prometheus server
```

### 11.9.2 📄 Example `/metrics` Output

```text
# HELP node_memory_MemTotal_bytes Memory information field MemTotal_bytes.
# TYPE node_memory_MemTotal_bytes gauge
node_memory_MemTotal_bytes 8.3e+09
node_cpu_seconds_total{cpu="0",mode="idle"} 123456.78
```

### 11.9.3 ☕ Monitoring a Spring Boot App

Add **Actuator + Micrometer Prometheus** dependencies, then expose the endpoint.

```xml
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
<dependency>
  <groupId>io.micrometer</groupId>
  <artifactId>micrometer-registry-prometheus</artifactId>
</dependency>
```

```properties
management.endpoints.web.exposure.include=health,prometheus
```

Metrics are then available at **`/actuator/prometheus`**.

---

## 11.10 🔍 PromQL (Prometheus Query Language)

**PromQL** is used to **select and calculate** metrics.

### 11.10.1 🧱 Basic Selectors

```promql
# All values of a metric
node_memory_MemAvailable_bytes

# Filter by labels
http_requests_total{job="spring-app", status="200"}

# Filter with regex
http_requests_total{status=~"5.."}        # Status codes 500–599
http_requests_total{status!="200"}        # Not 200
```

| Label Matcher | Meaning              |
| ------------- | -------------------- |
| `=`           | Equal                |
| `!=`          | Not equal            |
| `=~`          | Matches regex        |
| `!~`          | Does not match regex |

### 11.10.2 ⏱️ Instant Vector vs Range Vector

```text
📍 Instant Vector → The latest value of each series
   node_load1

⏱️ Range Vector   → Values over a time window
   node_cpu_seconds_total[5m]
```

### 11.10.3 🧮 Important Functions

| Function                      | Meaning                                                  |
| ----------------------------- | -------------------------------------------------------- |
| `rate(metric[5m])`            | **Per-second average increase** of a counter over 5 min  |
| `irate(metric[5m])`           | Per-second rate using the last two points (fast-moving)  |
| `increase(metric[1h])`        | Total increase over 1 hour                               |
| `sum(...)`                    | Add values together                                      |
| `avg(...)`                    | Average                                                  |
| `max(...)` / `min(...)`       | Maximum / minimum                                        |
| `count(...)`                  | Number of series                                         |
| `sum by (label) (...)`        | Sum grouped by a label                                   |
| `topk(5, ...)`                | Top 5 values                                             |
| `histogram_quantile(0.95, ...)`| 95th percentile from a histogram                        |

### 11.10.4 💻 Useful Query Examples

```promql
# Is a target up? (1 = up, 0 = down)
up

# Targets that are down
up == 0

# CPU usage % per server
100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)

# Memory usage %
(1 - (node_memory_MemAvailable_bytes / node_memory_MemTotal_bytes)) * 100

# Disk usage % of the root filesystem
100 - (node_filesystem_avail_bytes{mountpoint="/"} / node_filesystem_size_bytes{mountpoint="/"} * 100)

# Requests per second
sum(rate(http_requests_total[5m]))

# Error percentage
sum(rate(http_requests_total{status=~"5.."}[5m])) / sum(rate(http_requests_total[5m])) * 100

# 95th percentile request latency
histogram_quantile(0.95, sum(rate(http_request_duration_seconds_bucket[5m])) by (le))
```

#### 🧠 Easy Memory

```text
rate()  = "How fast is this counter growing per second?"
by()    = "Group the answer by this label."
up == 0 = "Which targets are down?"
```

---

## 11.11 🚨 Alerting Rules

**Alerting rules** are conditions written in PromQL. When true for some time, Prometheus **fires an alert**.

#### 📄 `alert_rules.yml`

```yaml
groups:
  - name: server-alerts
    rules:
      - alert: InstanceDown
        expr: up == 0
        for: 2m
        labels:
          severity: critical
        annotations:
          summary: "Instance {{ $labels.instance }} is down"
          description: "{{ $labels.job }} target has been down for more than 2 minutes."

      - alert: HighCPUUsage
        expr: 100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100) > 80
        for: 5m
        labels:
          severity: warning
        annotations:
          summary: "High CPU on {{ $labels.instance }}"

      - alert: LowDiskSpace
        expr: (node_filesystem_avail_bytes{mountpoint="/"} / node_filesystem_size_bytes{mountpoint="/"}) * 100 < 15
        for: 10m
        labels:
          severity: warning
        annotations:
          summary: "Disk almost full on {{ $labels.instance }}"
```

#### 📖 Understanding It

| Field          | Meaning                                                       |
| -------------- | ------------------------------------------------------------- |
| `alert`        | Name of the alert                                             |
| `expr`         | PromQL condition                                              |
| `for`          | How long the condition must be true before firing             |
| `labels`       | Extra labels (like `severity`) used for routing               |
| `annotations`  | Human-readable messages (summary, description)                |

### 11.11.1 🚦 Alert States

```text
🚦 Alert States
│
├── 🟢 Inactive → Condition is false
├── 🟡 Pending  → Condition is true, waiting for "for" duration
└── 🔴 Firing   → Condition has been true long enough → sent to Alertmanager
```

#### ✅ Check Rules

```bash
promtool check rules alert_rules.yml
```

---

## 11.12 🧾 Recording Rules

A **recording rule** **pre-calculates a heavy query** and **saves the result as a new metric**, so dashboards are faster.

```yaml
groups:
  - name: recording-rules
    rules:
      - record: job:http_requests:rate5m
        expr: sum by (job) (rate(http_requests_total[5m]))
```

> **Recording rule = Save an expensive calculation as a ready-to-use metric.**

---

## 11.13 🔔 Alertmanager

**Alertmanager** receives alerts from Prometheus and **decides how to notify people**.

```text
🔥 Prometheus ── firing alerts ──► 🔔 Alertmanager
                                        │
                  ┌─────────────────────┼─────────────────────┐
                  ▼                     ▼                     ▼
              📧 Email              💬 Slack             📟 PagerDuty
```

### 11.13.1 🧰 Alertmanager Features

| Feature          | Meaning                                                    |
| ---------------- | ---------------------------------------------------------- |
| 🗂️ **Grouping**   | Combine similar alerts into one notification               |
| 🔁 **Deduplication** | Remove duplicate alerts                                 |
| 🔇 **Silencing**  | Mute alerts for a time (like during maintenance)           |
| 🛣️ **Routing**    | Send different alerts to different teams / receivers       |
| 🚫 **Inhibition** | Do not send less important alerts if a bigger one is firing|

### 11.13.2 📄 `alertmanager.yml`

```yaml
route:
  receiver: team-email
  group_by: ['alertname', 'instance']
  group_wait: 30s
  group_interval: 5m
  repeat_interval: 4h
  routes:
    - matchers:
        - severity = "critical"
      receiver: team-slack

receivers:
  - name: team-email
    email_configs:
      - to: "team@example.com"
        from: "alerts@example.com"
        smarthost: "smtp.example.com:587"
        auth_username: "alerts@example.com"
        auth_password: "<app-password>"

  - name: team-slack
    slack_configs:
      - api_url: "<slack-webhook-url>"
        channel: "#alerts"
        send_resolved: true
```

#### ⚠️ Important

> **Do not commit passwords or webhook URLs to Git.** Use secrets or environment-based configuration.

#### 🐳 Run Alertmanager

```bash
docker run -d --name alertmanager -p 9093:9093 \
  -v $(pwd)/alertmanager.yml:/etc/alertmanager/alertmanager.yml \
  prom/alertmanager
```

#### 🧠 Simple Meaning

> **Prometheus decides WHEN to alert. Alertmanager decides WHO gets it and HOW.**

---

## 11.14 🗄️ Storage and Retention

```text
🗄️ Prometheus Storage
│
├── 📁 Local TSDB   → Stored on the Prometheus server disk
├── ⏳ Retention    → Default 15 days (change with --storage.tsdb.retention.time=30d)
└── ☁️ Remote Write → Send data to long-term storage (Thanos, Mimir, Cortex)
```

#### ⭐ Key Points

- 💾 Local storage is **not highly available** by itself
- 📈 For **long-term storage** and **many clusters**, use **Thanos**, **Mimir** or **Cortex**
- 🔗 **Federation** lets one Prometheus scrape another

---

## 11.15 🔭 Service Discovery

Instead of writing every target by hand, Prometheus can **find targets automatically**.

```text
🔭 Service Discovery Types
│
├── ☸️ Kubernetes   → Finds Pods, Services, Nodes
├── ☁️ EC2          → Finds instances by tags
├── 🗂️ File-based   → Reads targets from a JSON/YAML file
├── 🔍 Consul       → Reads from Consul
└── 📌 Static       → Fixed list (simple)
```

#### 💻 EC2 Service Discovery Example

```yaml
scrape_configs:
  - job_name: "ec2-nodes"
    ec2_sd_configs:
      - region: ap-south-1
        port: 9100
    relabel_configs:
      - source_labels: [__meta_ec2_tag_Monitor]
        regex: "true"
        action: keep
```

> This keeps only EC2 instances that have the tag **`Monitor=true`**.

---

## 11.16 ☸️ Prometheus With Kubernetes

The easiest way is the **kube-prometheus-stack** Helm chart. It installs:

```text
☸️ kube-prometheus-stack
├── 🔥 Prometheus (Operator)
├── 🔔 Alertmanager
├── 📈 Grafana
├── 🖥️ node-exporter
├── 📊 kube-state-metrics
└── 📏 Ready-made dashboards and alert rules
```

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install monitoring prometheus-community/kube-prometheus-stack -n monitoring --create-namespace
```

#### 🧩 Prometheus Operator Objects

| Object            | Purpose                                                   |
| ----------------- | --------------------------------------------------------- |
| `ServiceMonitor`  | Tells Prometheus **which Services to scrape**             |
| `PodMonitor`      | Tells Prometheus **which Pods to scrape**                 |
| `PrometheusRule`  | Holds **alert and recording rules**                       |

```yaml
apiVersion: monitoring.coreos.com/v1
kind: ServiceMonitor
metadata:
  name: shop-app
  labels:
    release: monitoring
spec:
  selector:
    matchLabels:
      app: shop
  endpoints:
    - port: http
      path: /actuator/prometheus
```

---

## 11.17 🆚 Prometheus vs CloudWatch vs Nagios

| Feature            | 🔥 Prometheus                      | 📊 AWS CloudWatch               | 🟢 Nagios                      |
| ------------------ | ---------------------------------- | ------------------------------- | ------------------------------ |
| Type               | Metrics + alerts (open source)     | AWS monitoring service          | Host and service checks        |
| Data model         | Labeled time series                | Metrics with dimensions         | Check results                  |
| Collection         | Pull (scrape)                      | AWS services push automatically | Active / passive checks        |
| Query              | **PromQL**                         | Metric math, Logs Insights      | Limited                        |
| Kubernetes fit     | ⭐ Excellent                       | Container Insights              | Weak                           |
| Cost               | Free (we run it)                   | Pay per metric / log            | Free / paid                    |
| Best for           | Cloud-native, Kubernetes, custom apps | AWS resources               | Traditional infrastructure     |

---

## 11.18 🔗 Prometheus in the DevOps Pipeline

```text
🤖 Jenkins deploys the app to ☸️ Kubernetes
                │
                ▼
🔥 Prometheus scrapes the app, nodes and cluster
                │
        ┌───────┴────────┐
        ▼                ▼
📈 Grafana          🔔 Alertmanager
(dashboards)         (alerts to Slack / email)
```

#### 🧰 Other Things We Can Monitor

- 🤖 **Jenkins** — Prometheus metrics plugin
- 🗄️ **Databases** — mysqld_exporter, postgres_exporter
- 🌐 **Websites** — blackbox_exporter
- 🐳 **Docker** — cAdvisor

---

## 11.19 🏆 Prometheus Best Practices

```text
✅ Prometheus Best Practices
│
├── 🏷️ Use clear metric and label names
├── ⚠️ Do not use labels with too many unique values (like user ID) — causes huge memory use
├── ⏱️ Use rate() for counters
├── 🚨 Alert on symptoms users feel (errors, latency), not only on causes
├── ⏳ Use "for:" to avoid false alerts
├── 🧾 Use recording rules for heavy queries
├── 🔒 Secure Prometheus and exporters (firewall, TLS, auth)
├── 💾 Plan storage and long-term retention
└── 📏 Follow the "Four Golden Signals": Latency, Traffic, Errors, Saturation
```

#### 🥇 The Four Golden Signals

| Signal         | Question                                   |
| -------------- | ------------------------------------------ |
| ⏱️ Latency     | How long do requests take?                 |
| 🚦 Traffic     | How many requests do we get?              |
| ❌ Errors      | How many requests fail?                    |
| 📈 Saturation  | How full are our resources (CPU, disk)?    |

---

## 11.20 🏗️ Real Example: Monitor Linux Servers

### 🎯 Requirement

Monitor **two Linux servers** and **get an alert** when a server is down or CPU is above 80%.

### 🏗️ Architecture

```text
🖥️ Server 1 (node_exporter :9100) ┐
                                  ├──◄ 🔥 Prometheus (:9090) ──► 🔔 Alertmanager (:9093) ──► 📧 Email
🖥️ Server 2 (node_exporter :9100) ┘            │
                                               ▼
                                        📈 Grafana (:3000)
```

### 🪜 Steps

```text
1. Install node_exporter on both servers (port 9100)
2. Install Prometheus on a monitoring server
3. Add both servers as targets in prometheus.yml
4. Add alert_rules.yml (InstanceDown, HighCPUUsage)
5. Install Alertmanager and configure email or Slack
6. Check Prometheus UI → Status → Targets (all UP)
7. Run a query:   100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
8. Add Prometheus as a data source in Grafana (next part)
9. Test: stop node_exporter on one server → wait 2 minutes → ✅ InstanceDown alert fires
```

#### 📄 Docker Compose (Quick Lab)

```yaml
services:
  prometheus:
    image: prom/prometheus
    ports:
      - "9090:9090"
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml
      - ./alert_rules.yml:/etc/prometheus/alert_rules.yml
      - prometheus_data:/prometheus

  alertmanager:
    image: prom/alertmanager
    ports:
      - "9093:9093"
    volumes:
      - ./alertmanager.yml:/etc/alertmanager/alertmanager.yml

  node-exporter:
    image: prom/node-exporter
    ports:
      - "9100:9100"

volumes:
  prometheus_data:
```

---

## 📌🧠 Prometheus Quick Revision

```text
🔥 Prometheus
│
├── 🏛️ Architecture
│   ├── Prometheus Server (:9090)
│   ├── Exporters (node_exporter :9100)
│   ├── Alertmanager (:9093)
│   ├── Pushgateway
│   └── Service Discovery
│
├── 🔄 Pull Model
│   ├── Scrape /metrics
│   └── up metric
│
├── 🧱 Data Model
│   ├── Metric name + Labels
│   └── Types: Counter, Gauge, Histogram, Summary
│
├── 🔍 PromQL
│   ├── Selectors and matchers
│   ├── rate(), sum by(), avg()
│   └── histogram_quantile()
│
├── 🚨 Alerting
│   ├── Alerting Rules (expr, for, labels)
│   └── Alertmanager (group, route, silence)
│
├── 🧾 Recording Rules
│
└── 🗄️ Storage
    ├── Local TSDB (15 days default)
    └── Remote write (Thanos, Mimir)
```

---

## 🧠⚡ Prometheus One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| 🔥 **Prometheus**          | Monitoring System That Stores Time-Series Metrics   |
| 🔄 **Scrape**              | Prometheus Pulls Metrics From Targets               |
| 🎯 **Target**              | Thing Being Monitored                               |
| 🔌 **Exporter**            | Exposes Metrics of a System at /metrics             |
| 🖥️ **node_exporter**       | Linux Server Metrics (Port 9100)                    |
| 🏷️ **Label**               | Key-Value Tag to Slice Metrics                      |
| 🔢 **Counter**             | Only Goes Up — Use rate()                           |
| 🌡️ **Gauge**               | Goes Up and Down                                    |
| 📊 **Histogram**           | Buckets for Latency Percentiles                     |
| 🔍 **PromQL**              | Query Language                                      |
| 📏 **rate()**              | Per-Second Growth of a Counter                      |
| 🔼 **up**                  | 1 = Target Alive, 0 = Down                          |
| 🚨 **Alert Rule**          | PromQL Condition + `for` Time                       |
| 🔔 **Alertmanager**        | Sends, Groups and Silences Notifications            |
| 🧾 **Recording Rule**      | Pre-Calculated Query Saved as a Metric              |
| 🔄 **Pushgateway**         | For Short-Lived Jobs to Push Metrics                |
| 🌐 **Port 9090**           | Default Prometheus Port                             |
| 📈 **Grafana**             | Shows Prometheus Data as Dashboards                 |

---

## 🗺️ Prometheus Learning Map

```text
                          🔥 Prometheus
                                │
       ┌────────────────────────┼────────────────────────┐
       │                        │                        │
       ▼                        ▼                        ▼
    COLLECT                   STORE & QUERY             ALERT
       │                        │                        │
       ├── Scrape (pull)        ├── TSDB                 ├── Alerting Rules
       ├── Exporters            ├── PromQL               ├── Alertmanager
       ├── App /metrics         ├── Recording Rules      │    ├── Email
       ├── Pushgateway          └── Retention / Remote   │    ├── Slack
       └── Service Discovery                             │    └── PagerDuty
                                                         └── Silence / Group / Route
       │
       ▼
   ENVIRONMENTS
       │
       ├── Linux servers (node_exporter)
       ├── Docker (cAdvisor)
       ├── Kubernetes (kube-prometheus-stack)
       └── Applications (Micrometer, JMX)
       │
       ▼
   VISUALIZE
       │
       └── 📈 Grafana dashboards
```

---

## ⭐ Prometheus Final Memory

```text
Prometheus
 │
 ├── What is it?
 │      └── Metrics monitoring and alerting system
 │
 ├── Push or pull?
 │      └── Pull (scrape)
 │
 ├── Where do metrics come from?
 │      └── /metrics endpoint (exporters or apps)
 │
 ├── Which exporter for Linux servers?
 │      └── node_exporter
 │
 ├── Which query language?
 │      └── PromQL
 │
 ├── How to read a counter?
 │      └── rate()
 │
 ├── Who sends the notifications?
 │      └── Alertmanager
 │
 ├── Default port?
 │      └── 9090
 │
 └── What shows the graphs?
        └── Grafana
```

---

# 📈 PART 12 — Grafana — Dashboards and Visualization

> **Grafana = The screen that shows our monitoring data**

---

## 12.1 📈 What is Grafana?

> **Grafana = Open-source visualization and dashboard tool**

Grafana **connects to many data sources** (Prometheus, CloudWatch, MySQL, Loki and more) and **shows the data as beautiful dashboards, graphs and alerts**.

It does **not collect or store metrics itself** — it **reads and displays** data from other systems.

#### 📦 Grafana Is Used To

- 📈 Build **dashboards** for servers, apps and business data
- 🔍 **Explore** metrics and logs
- 🚨 Create **alerts** and send notifications
- 👥 **Share** dashboards with teams
- 🔗 Show data from **many different sources** in one place

#### 🏗️ Grafana Basic Idea

```text
🗂️ Data Sources                          📈 Grafana
┌──────────────────┐                  ┌────────────────────────┐
│ 🔥 Prometheus    │ ───────────────► │ 📊 Dashboards          │
│ 📊 CloudWatch    │ ───────────────► │ 📈 Panels (graphs)     │
│ 📜 Loki (logs)   │ ───────────────► │ 🚨 Alerts              │
│ 🗄️ MySQL / SQL   │ ───────────────► │ 👥 Users and Teams     │
└──────────────────┘                  └────────────────────────┘
```

#### 🧠 Easy Memory

> **Grafana = The screen (TV) that shows our monitoring data**

---

## 12.2 🤔 Why Do We Use Grafana?

### ❌ Without Grafana

```text
🔥 Prometheus UI
├── Basic graphs only
├── Hard to share with the team
└── Hard to build a full monitoring screen
```

### ✅ With Grafana

```text
📈 Grafana
├── Beautiful, interactive dashboards
├── Many data sources in one dashboard
├── Variables (choose a server from a dropdown)
├── Alerts and notifications
└── Easy sharing and permissions
```

#### ⭐ Main Reasons

- 🎨 **Rich visualizations** (graphs, gauges, tables, heatmaps)
- 🔌 **Many data sources**
- 🔁 **Reusable dashboards** with variables
- 📥 **Ready-made dashboards** to import in seconds
- 🚨 **Alerting**
- 👥 **Teams, roles and access control**
- 🆓 **Free and open source** (paid Grafana Cloud and Enterprise also exist)

---

## 12.3 🧰 What Does Grafana Provide?

Grafana provides:

- 📊 Dashboards and Panels
- 🔌 Data Sources
- 🔍 Explore (ad-hoc queries)
- 🚨 Alerting
- 🧮 Variables and Templating
- 🏷️ Annotations
- 📁 Folders and Permissions
- 🧩 Plugins
- 📥 Import / Export Dashboards
- ⚙️ Provisioning (config as code)

---

## 12.4 🧱 Grafana Basic Concepts

```text
📈 Grafana
│
├── 🔌 Data Source   → Where the data comes from (Prometheus)
├── 📊 Dashboard     → A page with many panels
│     └── 📈 Panel   → One graph / number / table
├── 🔍 Query         → What data to read from the data source
├── 🧮 Variable      → A dropdown to change the dashboard (like instance)
├── 🚨 Alert Rule    → Condition that sends a notification
└── 📁 Folder / Org  → Organize dashboards and users
```

### 12.4.1 📖 Simple Definitions

| Concept            | Simple Meaning                                                   |
| ------------------ | ---------------------------------------------------------------- |
| 🔌 **Data Source** | A connection to a place that holds data                          |
| 📊 **Dashboard**   | A collection of panels shown on one page                         |
| 📈 **Panel**       | One visual block (a graph, a gauge, a table)                     |
| 🔍 **Query**       | A request for data (PromQL for Prometheus)                       |
| 🧮 **Variable**    | A changeable value (dropdown) used inside queries                |
| 🚨 **Alert Rule**  | A rule that checks a query and notifies when it is true          |
| 📢 **Contact Point** | Where alerts go (email, Slack)                                 |
| 🏷️ **Annotation**  | A marker on a graph for an event (like a deployment)             |
| 📁 **Folder**      | A group of dashboards with common permissions                    |
| 🏢 **Organization**| A separate workspace with its own dashboards and users           |

#### 🧠 Remember

> **Data Source → Query → Panel → Dashboard**

---

## 12.5 ⚙️ Installing Grafana

Grafana runs on **port 3000**.

### 12.5.1 🐳 Docker (Easy)

```bash
docker run -d --name grafana \
  -p 3000:3000 \
  -v grafana_data:/var/lib/grafana \
  grafana/grafana
```

Open: `http://<server-ip>:3000`

### 12.5.2 🐧 Install on Ubuntu / Debian

```bash
sudo apt-get install -y apt-transport-https software-properties-common wget
sudo mkdir -p /etc/apt/keyrings/
wget -q -O - https://apt.grafana.com/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/grafana.gpg > /dev/null
echo "deb [signed-by=/etc/apt/keyrings/grafana.gpg] https://apt.grafana.com stable main" | \
  sudo tee /etc/apt/sources.list.d/grafana.list

sudo apt-get update
sudo apt-get install grafana -y

sudo systemctl daemon-reload
sudo systemctl enable --now grafana-server
sudo systemctl status grafana-server
```

> 💡 Always check the **official Grafana installation page** for the latest steps.

### 12.5.3 🌐 First Login

```text
1. Open  http://<server-ip>:3000
2. Default login:  admin / admin
3. 🔒 Change the password when asked
4. ✅ Grafana home page opens
```

### 12.5.4 📁 Important Locations

| Path                              | Meaning                           |
| --------------------------------- | --------------------------------- |
| `/etc/grafana/grafana.ini`        | Main configuration file           |
| `/var/lib/grafana`                | Data (database, plugins)          |
| `/var/log/grafana`                | Logs                              |
| `/etc/grafana/provisioning`       | Provisioning files (config as code)|

#### 🔓 Firewall

```text
Open port 3000 (and use HTTPS with a reverse proxy in production)
```

---

## 12.6 🔌 Data Sources

A **data source** is **where Grafana reads data from**.

```text
🔌 Common Data Sources
│
├── 🔥 Prometheus          → Metrics
├── 📜 Loki                → Logs
├── 🔭 Tempo               → Traces
├── 📊 CloudWatch          → AWS metrics and logs
├── 🔎 Elasticsearch / OpenSearch → Logs and search
├── 🗄️ MySQL / PostgreSQL  → SQL data
├── 📈 InfluxDB            → Time-series data
└── 🧩 Many more through plugins
```

### 12.6.1 🪜 Add Prometheus as a Data Source

```text
1. Grafana → Connections → Data sources → Add data source
2. Choose "Prometheus"
3. URL:  http://<prometheus-server>:9090
         (in Docker Compose: http://prometheus:9090)
4. Click "Save & test"
5. ✅ "Successfully queried the Prometheus API"
```

#### 🧠 Simple Meaning

> **Data Source = The connection between Grafana and the place with our data**

---

## 12.7 📊 Dashboards and Panels

A **dashboard** is a **page with panels**. A **panel** shows **one query result**.

```text
📊 Dashboard: "Server Overview"
┌──────────────────┬──────────────────┬──────────────────┐
│ 🔢 Stat: Uptime  │ 🔢 Stat: Servers │ 🌡️ Gauge: CPU %  │
├──────────────────┴──────────────────┴──────────────────┤
│ 📈 Time Series: CPU usage per server                   │
├─────────────────────────────┬──────────────────────────┤
│ 📈 Time Series: Memory %    │ 📋 Table: Disk usage     │
└─────────────────────────────┴──────────────────────────┘
```

### 12.7.1 🎨 Panel (Visualization) Types

| Visualization      | Used For                                             |
| ------------------ | ---------------------------------------------------- |
| 📈 **Time series** | Values over time (CPU, memory, requests) — most used |
| 🔢 **Stat**        | One big number (current value)                       |
| 🌡️ **Gauge**       | A value inside a range (0–100%)                      |
| 📊 **Bar chart**   | Compare values                                       |
| 📋 **Table**       | Rows and columns of data                             |
| 🔥 **Heatmap**     | Distribution over time (latency)                     |
| 📜 **Logs**        | Log lines (from Loki)                                |
| 🥧 **Pie chart**   | Parts of a whole                                     |
| 🚦 **State timeline / Status history** | Up/down status over time         |

### 12.7.2 🪜 Create a Dashboard and Panel

```text
1. Dashboards → New → New dashboard
2. Add visualization → choose the data source (Prometheus)
3. Write a query in the Query editor, for example:
      100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
4. Choose the visualization: Time series
5. Set the title: "CPU Usage %", unit: Percent (0-100)
6. Apply → Save dashboard
```

### 12.7.3 🧰 Panel Options

| Option             | Purpose                                                 |
| ------------------ | ------------------------------------------------------- |
| 📏 **Unit**        | Show as %, bytes, seconds, requests/sec                 |
| 🎚️ **Thresholds**  | Change color by value (green → yellow → red)            |
| 🏷️ **Legend**      | Show names of series (use `{{instance}}`)               |
| ⏱️ **Time range**  | Choose the time window (last 6 hours, last 7 days)      |
| 🔄 **Refresh**     | Auto refresh every 5s, 30s, 1m                          |

#### 💡 Useful Prometheus Panel Queries

```promql
# Memory usage %
(1 - (node_memory_MemAvailable_bytes / node_memory_MemTotal_bytes)) * 100

# Disk usage % (root)
100 - (node_filesystem_avail_bytes{mountpoint="/"} / node_filesystem_size_bytes{mountpoint="/"} * 100)

# Requests per second
sum(rate(http_requests_total[5m]))

# Targets that are up
sum(up)
```

---

## 12.8 🧮 Variables and Templating

**Variables** make a dashboard **reusable**. A dropdown lets users choose a server, job or namespace.

```text
🎛️ Dashboard Variable: $instance  [ web1:9100 ▼ ]
        ↓
Query uses it:  rate(node_cpu_seconds_total{instance="$instance"}[5m])
        ↓
All panels change when the user picks another server
```

#### 🪜 Create a Variable

```text
Dashboard → Settings → Variables → Add variable
Type:        Query
Name:        instance
Data source: Prometheus
Query:       label_values(node_cpu_seconds_total, instance)
Options:     Enable "Multi-value" and "Include All option" if needed
```

#### 🧠 Simple Meaning

> **Variable = Dropdown that changes every panel on the dashboard**

---

## 12.9 📥 Import Ready-Made Dashboards

We do **not need to build every dashboard**. The **Grafana Dashboards library** has thousands of ready dashboards.

```text
Dashboards → New → Import
→ Enter a Dashboard ID (example: 1860)
→ Load → Choose the Prometheus data source → Import ✅
```

#### 📚 Popular Dashboard Examples

| Dashboard                     | Use                                            |
| ----------------------------- | ---------------------------------------------- |
| 🖥️ **Node Exporter Full** (ID 1860) | Linux server monitoring                 |
| 🐳 Docker / cAdvisor dashboards| Container monitoring                           |
| ☸️ Kubernetes dashboards       | Cluster, node and pod monitoring               |
| 🤖 Jenkins performance dashboards | Jenkins monitoring                          |
| ☕ JVM / Spring Boot dashboards | Java application monitoring                    |

> 💡 Dashboard IDs and availability can change. Search the **Grafana Dashboards** website for the latest options.

#### 💾 Export / Share

- 📤 **Export** a dashboard as **JSON** and store it in **Git**
- 🔗 **Share** by link or snapshot (with permission settings)

---

## 12.10 🔍 Explore

**Explore** is a place to **run queries quickly** without building a dashboard.

```text
Left menu → Explore
├── 🔌 Choose a data source
├── 🔍 Write a query
├── ▶️ Run it
└── 📈 See graphs or logs immediately
```

#### 🎯 Used For

- 🛠️ **Troubleshooting** a problem right now
- 🧪 **Testing** a PromQL query before adding it to a panel
- 📜 Viewing **logs** together with metrics (with Loki)

---

## 12.11 🚨 Grafana Alerting

Grafana can **check queries on a schedule** and **send notifications** when a condition is true.

```text
🚨 Grafana Alerting
│
├── 📏 Alert Rule          → Query + Condition + Duration
├── 📢 Contact Point       → Where to send (email, Slack, webhook)
├── 🛣️ Notification Policy → Which alerts go to which contact point
└── 🔇 Silences / Mute Timings → Pause notifications
```

#### 🏗️ Flow

```text
📊 Query (CPU %) → 📏 Alert Rule (CPU > 80% for 5m)
                         │ fires
                         ▼
                🛣️ Notification Policy
                         │
                         ▼
                📢 Contact Point → 📧 Email / 💬 Slack
```

#### 🪜 Create an Alert

```text
1. Alerting → Alert rules → New alert rule
2. Name: High CPU
3. Query: choose Prometheus and write the PromQL query
4. Condition: IS ABOVE 80
5. Evaluate every: 1m, for: 5m
6. Add labels (severity=warning) and a summary
7. Alerting → Contact points → Add (Email or Slack)
8. Alerting → Notification policies → Route alerts to the contact point
9. Save ✅
```

#### ⚖️ Grafana Alerts vs Prometheus Alertmanager

| 📈 Grafana Alerting                              | 🔔 Prometheus + Alertmanager                   |
| ------------------------------------------------ | ---------------------------------------------- |
| Works with **many data sources**                 | Works only with **Prometheus** data            |
| Created and managed in the Grafana UI            | Defined in YAML rule files                     |
| One place for all alerts                         | Strong, widely used for Prometheus setups      |
| Good when using multiple data sources            | Good for "config as code" Prometheus setups    |

> 💡 Many teams use **Prometheus alert rules + Alertmanager** and use **Grafana only for dashboards**. Both are valid.

---

## 12.12 🏷️ Annotations

**Annotations** are **markers on graphs** that show events, like **deployments** or **incidents**.

```text
📈 CPU graph:   ─────╱╲───────────────╱╲╲───
                       ▲                 ▲
                  🚀 Deployed v1.2   🔥 Incident
```

- ✍️ Add **manually** (Ctrl + click on a graph)
- 🤖 Add **automatically** using the Grafana HTTP API (for example from a Jenkins pipeline after a deployment)

#### 💻 Add an Annotation From a Pipeline

```bash
curl -X POST http://grafana:3000/api/annotations \
  -H "Authorization: Bearer $GRAFANA_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"text":"Deployed shop-app v42","tags":["deploy","shop-app"]}'
```

---

## 12.13 👥 Users, Teams and Permissions

```text
👥 Grafana Access Control
│
├── 🏢 Organizations   → Separate workspaces
├── 👤 Users           → People who log in
├── 👥 Teams           → Groups of users
├── 🎭 Roles           → Admin, Editor, Viewer
├── 📁 Folder permissions → Who can view or edit which dashboards
└── 🔑 Service Accounts / API Tokens → For automation
```

| Role         | Can Do                                                      |
| ------------ | ----------------------------------------------------------- |
| 👑 **Admin** | Manage everything (users, data sources, plugins)            |
| ✏️ **Editor**| Create and edit dashboards                                  |
| 👀 **Viewer**| View dashboards only                                        |

#### 🔒 Authentication Options

- 👤 Built-in users
- 🏢 LDAP / Active Directory
- 🌐 OAuth (GitHub, Google, Azure AD)
- 🔑 SAML (enterprise)

#### ✅ Best Practices

- 🔒 Change the default admin password
- 👥 Use **teams and folder permissions**
- 🔑 Use **service accounts** for automation
- 🌐 Use **HTTPS**

---

## 12.14 ⚙️ Provisioning (Config as Code)

**Provisioning** sets up **data sources and dashboards from files**, so Grafana is **ready automatically** after install (useful for Docker and Kubernetes).

```text
📁 /etc/grafana/provisioning/
├── 📁 datasources/
│   └── prometheus.yml
└── 📁 dashboards/
    └── dashboards.yml
```

#### 📄 `datasources/prometheus.yml`

```yaml
apiVersion: 1
datasources:
  - name: Prometheus
    type: prometheus
    access: proxy
    url: http://prometheus:9090
    isDefault: true
```

#### 📄 `dashboards/dashboards.yml`

```yaml
apiVersion: 1
providers:
  - name: "default"
    folder: "DevOps"
    type: file
    options:
      path: /var/lib/grafana/dashboards
```

> **Provisioning = Grafana configuration stored in Git, applied automatically**

---

## 12.15 🧩 Plugins and the Grafana Stack

### 12.15.1 🧩 Plugins

Plugins add **data sources**, **panels** and **apps**.

```bash
grafana-cli plugins install grafana-piechart-panel
sudo systemctl restart grafana-server
```

### 12.15.2 📚 Grafana Labs Stack (LGTM)

```text
📚 Grafana Observability Stack
│
├── 📜 Loki    → Logs
├── 📈 Grafana → Dashboards
├── 🔭 Tempo   → Traces
└── 📊 Mimir   → Long-term metrics storage
```

#### 🧠 Three Pillars of Observability

| Pillar          | Meaning                              | Tools                           |
| --------------- | ------------------------------------ | ------------------------------- |
| 📊 **Metrics**  | Numbers over time                    | Prometheus, Mimir               |
| 📜 **Logs**     | Text records of events               | Loki, Elasticsearch             |
| 🔭 **Traces**   | Path of a request through services   | Tempo, Jaeger                   |

> **Grafana can show all three in one place.**

---

## 12.16 ☸️ Grafana With Kubernetes

The **kube-prometheus-stack** Helm chart installs **Grafana together with Prometheus** and **ready-made Kubernetes dashboards**.

```bash
helm install monitoring prometheus-community/kube-prometheus-stack -n monitoring --create-namespace

# Access Grafana locally
kubectl port-forward svc/monitoring-grafana 3000:80 -n monitoring
# Open http://localhost:3000
```

```bash
# Get the admin password
kubectl get secret monitoring-grafana -n monitoring \
  -o jsonpath="{.data.admin-password}" | base64 --decode
```

---

## 12.17 🆚 Grafana vs Prometheus vs Kibana

| Feature           | 📈 Grafana                         | 🔥 Prometheus                    | 🔎 Kibana                        |
| ----------------- | ---------------------------------- | -------------------------------- | -------------------------------- |
| Main job          | **Visualize** data                 | **Collect and store** metrics    | Visualize **Elasticsearch** data |
| Stores data?      | ❌ No                              | ✅ Yes (TSDB)                    | ❌ No (Elasticsearch stores)     |
| Data sources      | Many                               | Metrics only                     | Mainly Elasticsearch             |
| Alerts            | ✅ Yes                             | ✅ Yes (+ Alertmanager)          | ✅ Yes                           |
| Best for          | Dashboards for any data            | Metrics and alert rules          | Log search and analytics         |

#### 🧠 Easy Memory

```text
🔥 Prometheus = Collects and stores the numbers
📈 Grafana    = Draws the pictures from those numbers
```

---

## 12.18 🏆 Grafana Best Practices

```text
✅ Grafana Best Practices
│
├── 📊 Keep dashboards simple and focused
├── 🥇 Show the Four Golden Signals first
├── 🧮 Use variables instead of many copies of a dashboard
├── 🎚️ Use thresholds and colors to show problems quickly
├── 📁 Organize dashboards in folders
├── ⚙️ Store dashboards and provisioning files in Git
├── 🔒 Secure with HTTPS, roles and strong passwords
├── 🏷️ Add deployment annotations
└── 💾 Back up the Grafana data
```

---

## 12.19 🏗️ Real Example: Server Monitoring Dashboard

### 🎯 Requirement

Show **CPU, memory and disk usage** of Linux servers on a dashboard and **alert** when CPU is high.

### 🏗️ Architecture

```text
🖥️ Server 1 (node_exporter) ┐
                            ├──► 🔥 Prometheus ──► 📈 Grafana ──► 👀 Team
🖥️ Server 2 (node_exporter) ┘                            │
                                                          └──► 🚨 Alert → 📧 Email / 💬 Slack
```

### 🪜 Steps

```text
1. Install node_exporter on all servers
2. Install Prometheus and add the servers as targets
3. Install Grafana (port 3000) and change the admin password
4. Add the Prometheus data source (Save & test)
5. Import dashboard ID 1860 (Node Exporter Full) ✅
6. Create your own dashboard "Team Overview" with panels:
      CPU %, Memory %, Disk %, Targets Up
7. Add a variable $instance to select a server
8. Create an alert: CPU > 80% for 5 minutes → Contact point: Slack
9. Test the alert by creating CPU load on a server
```

### 📄 Docker Compose (Quick Lab)

```yaml
services:
  prometheus:
    image: prom/prometheus
    ports:
      - "9090:9090"
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml

  node-exporter:
    image: prom/node-exporter
    ports:
      - "9100:9100"

  grafana:
    image: grafana/grafana
    ports:
      - "3000:3000"
    environment:
      GF_SECURITY_ADMIN_PASSWORD: change_me_now
    volumes:
      - grafana_data:/var/lib/grafana
    depends_on:
      - prometheus

volumes:
  grafana_data:
```

#### 💡 Prometheus Data Source URL Inside Compose

```text
http://prometheus:9090
(Containers in the same Compose network use the service name)
```

---

## 📌🧠 Grafana Quick Revision

```text
📈 Grafana
│
├── 🧱 Concepts
│   ├── Data Source
│   ├── Query
│   ├── Panel
│   └── Dashboard
│
├── 🔌 Data Sources
│   ├── Prometheus
│   ├── Loki, Tempo
│   ├── CloudWatch
│   └── SQL databases
│
├── 🎨 Panels
│   ├── Time series, Stat, Gauge
│   ├── Table, Bar chart, Heatmap
│   └── Thresholds, Units
│
├── 🧮 Variables and Templating
│
├── 📥 Import Dashboards (ID 1860)
│
├── 🔍 Explore
│
├── 🚨 Alerting
│   ├── Alert Rule
│   ├── Contact Point
│   └── Notification Policy
│
├── 👥 Access Control
│   ├── Orgs, Teams, Roles
│   └── Folders, Service Accounts
│
└── ⚙️ Provisioning (config as code)
```

---

## 🧠⚡ Grafana One-Line Memory

| Concept                    | Easy Memory                                         |
| -------------------------- | --------------------------------------------------- |
| 📈 **Grafana**             | Dashboards for Monitoring Data                      |
| 🔌 **Data Source**         | Where Grafana Reads Data From                       |
| 📊 **Dashboard**           | Page With Many Panels                               |
| 📈 **Panel**               | One Graph / Number / Table                          |
| 🔍 **Query**               | Request for Data (PromQL for Prometheus)            |
| 🧮 **Variable**            | Dropdown That Changes All Panels                    |
| 📥 **Import**              | Use a Ready-Made Dashboard (ID 1860)                |
| 🔍 **Explore**             | Quick Ad-Hoc Queries                                |
| 🚨 **Alert Rule**          | Condition That Notifies                             |
| 📢 **Contact Point**       | Where Alerts Go (Email, Slack)                      |
| 🏷️ **Annotation**          | Marker for Events (Deployments)                     |
| 🎚️ **Threshold**           | Color Changes by Value                              |
| ⚙️ **Provisioning**        | Setup From Files (Config as Code)                   |
| 📜 **Loki**                | Logs for Grafana                                    |
| 🌐 **Port 3000**           | Default Grafana Port                                |
| 🔑 **admin / admin**       | Default Login (Change Immediately)                  |

---

## 🗺️ Grafana Learning Map

```text
                           📈 Grafana
                               │
       ┌───────────────────────┼───────────────────────┐
       │                       │                       │
       ▼                       ▼                       ▼
    CONNECT                  VISUALIZE                  ACT
       │                       │                       │
       ├── Data Sources        ├── Dashboards          ├── Alert Rules
       │    ├── Prometheus     ├── Panels              ├── Contact Points
       │    ├── Loki           ├── Variables           ├── Notification Policies
       │    ├── CloudWatch     ├── Import / Export     └── Annotations
       │    └── SQL            └── Explore
       │
       ▼
   MANAGE
       │
       ├── Users / Teams / Roles
       ├── Folders and Permissions
       ├── Provisioning (Git)
       └── Plugins
       │
       ▼
   OBSERVABILITY STACK
       │
       ├── Metrics → Prometheus / Mimir
       ├── Logs    → Loki
       └── Traces  → Tempo
```

---

## ⭐ Grafana Final Memory

```text
Grafana
 │
 ├── What is it?
 │      └── Visualization and dashboard tool
 │
 ├── Does it store metrics?
 │      └── No (it reads from data sources)
 │
 ├── Default port?
 │      └── 3000
 │
 ├── First step after install?
 │      └── Add a data source (Prometheus)
 │
 ├── Quick way to get a dashboard?
 │      └── Import by ID (like 1860)
 │
 ├── How to make one dashboard work for many servers?
 │      └── Variables
 │
 ├── How to get alert notifications?
 │      └── Alert rule + Contact point + Notification policy
 │
 └── Prometheus and Grafana together?
        └── Prometheus collects, Grafana shows
```

---

# 🧩 PART 13 — Putting It All Together

> The full pipeline, comparisons, cheat sheets, security and a practice roadmap.

---

## 13.1 🧩 Tool Categories — Big Picture

```text
🔄 DevOps Tools in These Notes
│
├── 💻 Plan and Code
│   └── Git & GitHub
│
├── 🔨 Build and Integrate
│   ├── Maven
│   └── Jenkins
│
├── 🧪 Quality and Artifacts
│   ├── SonarQube
│   └── Nexus Repository
│
├── 📦 Package and Run
│   ├── Docker
│   └── Kubernetes
│
├── 🏗️ Infrastructure and Configuration
│   ├── Terraform
│   └── Ansible
│
└── 📊 Monitor
    ├── Prometheus
    └── Grafana
```

#### 📊 One Table for All Tools

| Tool                    | Stage        | Main Job                                  | Default Port |
| ----------------------- | ------------ | ----------------------------------------- | ------------ |
| 🔗 **Git**              | Code         | Track code changes                        | —            |
| 🐙 **GitHub**           | Code         | Host repositories, Pull Requests          | 443 / 22     |
| 🔨 **Maven**            | Build        | Build and manage Java projects            | —            |
| 🤖 **Jenkins**          | CI/CD        | Automate the pipeline                     | **8080**     |
| 🔍 **SonarQube**        | Test         | Code quality and security scan            | **9000**     |
| 📦 **Nexus**            | Release      | Store artifacts and libraries             | **8081**     |
| 🐳 **Docker**           | Package      | Containers and images                     | 2375/2376 (API, usually not exposed) |
| 🏗️ **Terraform**        | Infrastructure | Create infrastructure with code         | —            |
| ⚙️ **Ansible**          | Configuration| Configure servers and deploy              | 22 (SSH)     |
| ☸️ **Kubernetes**       | Deploy       | Run and scale containers                  | 6443 (API server) |
| 🔥 **Prometheus**       | Monitor      | Collect metrics, alert rules              | **9090**     |
| 🔔 **Alertmanager**     | Monitor      | Send alert notifications                  | **9093**     |
| 🖥️ **node_exporter**    | Monitor      | Linux server metrics                      | **9100**     |
| 📈 **Grafana**          | Monitor      | Dashboards and visualization              | **3000**     |

---

## 13.2 🏗️ The Complete CI/CD Flow (End to End)

```text
👨‍💻 Developer
   │ 1️⃣ git push (feature branch) → Pull Request
   ▼
🐙 GitHub  ── 2️⃣ review + merge to main ── webhook ──►
                                                      │
                                                      ▼
                                             🤖 Jenkins Pipeline
   ┌──────────────────────────────────────────────────┐
   │ 3️⃣ Checkout code from Git                        │
   │ 4️⃣ 🔨 Maven: compile + unit tests + package      │
   │ 5️⃣ 🔍 SonarQube: scan + Quality Gate             │
   │ 6️⃣ 📦 Nexus: upload the .jar                     │
   │ 7️⃣ 🐳 Docker: build image + push to registry     │
   │ 8️⃣ ☸️ Kubernetes: rolling update (kubectl / Helm)│
   └──────────────────────────────────────────────────┘
                                                      │
   🏗️ Terraform created the cluster / servers earlier │
   ⚙️ Ansible configured the servers earlier          │
                                                      ▼
                                          ☸️ Application is LIVE
                                                      │
                                                      ▼
                         🔥 Prometheus scrapes metrics ──► 📈 Grafana dashboards
                                      │
                                      ▼
                         🔔 Alertmanager ──► 📧 Email / 💬 Slack
                                      │
                                      ▼
                         👨‍💻 Team fixes issues → back to step 1 (the loop continues ♾️)
```

#### 📖 Story in Simple Words

```text
1. Developer writes code and pushes it to a feature branch on GitHub
2. Team reviews the Pull Request and merges it
3. GitHub sends a webhook to Jenkins
4. Jenkins builds the code using Maven and runs the tests
5. SonarQube checks code quality; if the Quality Gate fails, the pipeline stops
6. The built .jar is uploaded to Nexus with a version
7. Jenkins builds a Docker image and pushes it to a registry
8. Kubernetes updates the Deployment with the new image (no downtime)
9. Prometheus watches the app and servers; Grafana shows dashboards
10. If something breaks, Alertmanager notifies the team
```

---

## 13.3 🌱 Environments: Dev → Test → Prod

```text
🌱 Environment Flow
│
├── 💻 DEV     → Developers test new features (auto-deploy on every merge)
├── 🧪 TEST    → QA tests and integration tests (auto-deploy after Dev)
├── 🎭 STAGING → Same as production, final checks (optional)
└── 🚀 PROD    → Real users (manual approval or automatic)
```

```text
📦 Build the artifact / image ONCE
        │
        ├──► 💻 Dev   (same image)
        ├──► 🧪 Test  (same image)
        └──► 🚀 Prod  (same image)

Only the configuration changes (ConfigMap, Secrets, environment variables).
```

#### 🧠 Golden Rule

> **Build once, deploy many times.** The same tested image goes to every environment.

#### 🛠️ How Each Tool Helps

| Tool                | Role in Environments                                     |
| ------------------- | -------------------------------------------------------- |
| 🏗️ Terraform        | Create the same infrastructure for dev / test / prod     |
| ⚙️ Ansible          | Configure servers the same way                           |
| 🐳 Docker           | Same container image everywhere                          |
| ☸️ Kubernetes       | Namespaces and ConfigMaps per environment                |
| 🤖 Jenkins          | Pipeline stages with approvals for production            |
| 📦 Nexus            | Keeps versioned artifacts for every environment          |

---

## 13.4 ⚖️ Important Comparisons

### 13.4.1 🏗️ Terraform vs Ansible vs Kubernetes

| Tool               | Question It Answers                                 |
| ------------------ | --------------------------------------------------- |
| 🏗️ **Terraform**   | "Create the servers, network and cloud resources."  |
| ⚙️ **Ansible**     | "Install and configure software on the servers."    |
| ☸️ **Kubernetes**  | "Run, scale and heal our containers."               |

```text
🏗️ Terraform → creates 🖥️ servers / ☸️ cluster
        ↓
⚙️ Ansible   → configures the servers (Docker, packages, users)
        ↓
☸️ Kubernetes → runs the application containers
```

### 13.4.2 🐳 Docker vs Kubernetes

| 🐳 Docker                              | ☸️ Kubernetes                               |
| -------------------------------------- | ------------------------------------------- |
| Builds and runs **containers**         | **Manages many containers** on many servers |
| Works on one machine                   | Works on a cluster                          |
| Manual scaling and restarts            | Auto scaling and self-healing               |
| `docker run`, Compose                  | Deployments, Services, Ingress              |

### 13.4.3 🔥 Prometheus vs Grafana

| 🔥 Prometheus                     | 📈 Grafana                           |
| --------------------------------- | ------------------------------------ |
| Collects and stores metrics       | Shows data on dashboards             |
| Alert rules                       | Alerts across many data sources      |
| PromQL queries                    | Panels and visualizations            |

### 13.4.4 🔨 Maven vs Jenkins vs Nexus

| Tool            | Role                                                         |
| --------------- | ------------------------------------------------------------ |
| 🔨 **Maven**    | **Builds** the project and creates the `.jar`                |
| 🤖 **Jenkins**  | **Runs** Maven (and everything else) automatically           |
| 📦 **Nexus**    | **Stores** the `.jar` and downloaded libraries               |

### 13.4.5 🤖 Jenkins vs GitHub Actions vs GitLab CI

| Feature          | 🤖 Jenkins                        | 🐙 GitHub Actions                | 🦊 GitLab CI                    |
| ---------------- | --------------------------------- | -------------------------------- | ------------------------------- |
| Hosting          | Self-hosted (we manage)           | GitHub-hosted or self-hosted runners | GitLab-hosted or self-hosted |
| Config file      | `Jenkinsfile` (Groovy)            | `.github/workflows/*.yml`        | `.gitlab-ci.yml`                |
| Plugins          | 1800+ plugins                     | Marketplace actions              | Built-in features               |
| Setup effort     | Higher                            | Low                              | Low (inside GitLab)             |
| Best for         | Flexible, custom, on-premises     | Projects already on GitHub       | Projects already on GitLab      |

---

## 13.5 ☁️ DevOps Tools and AWS Services

How the tools we learned map to **AWS services** (from our AWS notes).

| DevOps Tool           | AWS Service (Similar Role)                                  |
| --------------------- | ----------------------------------------------------------- |
| 🔗 Git & GitHub       | AWS CodeCommit (closed to new customers), GitHub itself     |
| 🤖 Jenkins            | AWS CodePipeline + CodeBuild + CodeDeploy                   |
| 📦 Nexus Repository   | AWS CodeArtifact (packages), Amazon ECR (Docker images)     |
| 🐳 Docker             | ECS / Fargate, ECR                                          |
| ☸️ Kubernetes         | **Amazon EKS**                                              |
| 🏗️ Terraform          | AWS CloudFormation                                          |
| ⚙️ Ansible            | AWS Systems Manager (Run Command, State Manager)            |
| 🔥 Prometheus         | Amazon Managed Service for Prometheus / CloudWatch metrics  |
| 📈 Grafana            | Amazon Managed Grafana / CloudWatch dashboards              |
| 🔍 SonarQube          | Amazon CodeGuru Reviewer (different approach)               |

#### 🧠 Simple Meaning

> **Open-source tools run anywhere (any cloud or on-premises). AWS services are the "managed" versions inside AWS.**

---

## 13.6 ⌨️ Command Cheat Sheet

### 13.6.1 🔗 Git

```bash
git clone <url>            git switch -c <branch>      git add .
git commit -m "message"    git push -u origin <branch> git pull
git merge <branch>         git log --oneline           git revert <hash>
```

### 13.6.2 🔨 Maven

```bash
mvn clean package          mvn clean install           mvn clean deploy
mvn test                   mvn -DskipTests package     mvn dependency:tree
mvn sonar:sonar
```

### 13.6.3 🐳 Docker

```bash
docker build -t app:1.0 .            docker run -d -p 8080:8080 app:1.0
docker ps                            docker logs -f <name>
docker exec -it <name> bash          docker push user/app:1.0
docker compose up -d                 docker compose down
```

### 13.6.4 🏗️ Terraform

```bash
terraform init                       terraform validate
terraform plan                       terraform apply
terraform destroy                    terraform output
```

### 13.6.5 ⚙️ Ansible

```bash
ansible all -i inventory.ini -m ping
ansible-playbook -i inventory.ini site.yml
ansible-playbook site.yml --check
ansible-vault encrypt secrets.yml
```

### 13.6.6 ☸️ Kubernetes

```bash
kubectl get pods -A                  kubectl apply -f app.yaml
kubectl describe pod <pod>           kubectl logs -f <pod>
kubectl exec -it <pod> -- bash       kubectl scale deployment <name> --replicas=5
kubectl rollout status deployment/<name>
kubectl rollout undo deployment/<name>
```

### 13.6.7 🔥 Prometheus / Grafana

```bash
promtool check config prometheus.yml
promtool check rules alert_rules.yml
curl -X POST http://localhost:9090/-/reload

# Useful queries
up
100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
```

---

## 13.7 🔐 Security in DevOps (DevSecOps)

**DevSecOps** means adding **security checks into every stage** of the pipeline.

```text
🔐 DevSecOps in the Pipeline
│
├── 🔗 Code     → No secrets in Git, signed commits, branch protection
├── 🔨 Build    → Dependency vulnerability scan (OWASP Dependency-Check)
├── 🔍 Test     → SonarQube (code security), Quality Gate
├── 🐳 Package  → Image scan (Trivy, Docker Scout), minimal base images
├── 📦 Release  → Private registry, signed artifacts, access control
├── 🏗️ Infra    → Terraform plan review, least-privilege IAM
├── ☸️ Deploy   → RBAC, Network Policies, Secrets management
└── 📊 Monitor  → Alerts for suspicious behavior, audit logs
```

#### ✅ Security Checklist

```text
✅ Never store passwords or keys in Git (use Jenkins Credentials, Vault, Secrets Manager)
✅ Use least-privilege access (IAM, RBAC, Nexus roles)
✅ Scan code, dependencies and images
✅ Keep tools updated (Jenkins, plugins, Nexus, SonarQube)
✅ Use HTTPS for Jenkins, Nexus, SonarQube and Grafana
✅ Restrict ports with firewalls / Security Groups
```

---

## 13.8 ✅ Production Checklist

```text
✅ Source Control
├── 🛡️ Protect the main branch (PR reviews + status checks)
└── 🙈 Use .gitignore, no secrets in Git

✅ CI/CD
├── 📜 Jenkinsfile stored in Git
├── 🚦 SonarQube Quality Gate enforced
├── 🧪 Automated tests run on every change
└── 🙋 Manual approval before production (if needed)

✅ Artifacts and Images
├── 📦 Versioned artifacts in Nexus
├── 🏷️ Docker images with fixed tags (no :latest)
└── 🔍 Images scanned for vulnerabilities

✅ Infrastructure
├── 🏗️ Terraform with remote state and locking
├── ⚙️ Ansible for repeatable configuration
└── 📝 Everything in Git (Infrastructure as Code)

✅ Kubernetes
├── 📏 Requests and limits set
├── 🩺 Liveness and readiness probes
├── 📈 HPA configured
└── 🔐 RBAC and Network Policies

✅ Monitoring
├── 🔥 Prometheus scraping apps, nodes and cluster
├── 📈 Grafana dashboards (Four Golden Signals)
├── 🔔 Alerts to Slack / email
└── 💾 Backups for Jenkins, Nexus, SonarQube DB, Grafana, Terraform state
```

---

## 13.9 🎯 Practice Project Roadmap

Build **one project step by step** to practice every tool.

```text
🎯 Project: "Shop App" (Spring Boot or Flask)
│
├── 1️⃣ Git       → Create a GitHub repo, use feature branches and Pull Requests
├── 2️⃣ Maven     → Build the app (mvn clean package) and add JUnit tests
├── 3️⃣ Jenkins   → Create a Pipeline with a Jenkinsfile and GitHub webhook
├── 4️⃣ SonarQube → Add analysis and a Quality Gate to the pipeline
├── 5️⃣ Nexus     → Upload the artifact with mvn deploy
├── 6️⃣ Docker    → Write a Dockerfile (multi-stage) and push the image
├── 7️⃣ Terraform → Create a VPC + EC2 (or EKS) on AWS
├── 8️⃣ Ansible   → Configure the EC2 server (install Docker, deploy)
├── 9️⃣ Kubernetes→ Deploy with Deployment + Service + Ingress
├── 🔟 Prometheus → Monitor the app and nodes, add alert rules
└── 1️⃣1️⃣ Grafana  → Build a dashboard and an alert
```

#### 🪜 Level Up Ideas

- 🔄 Add **Blue/Green** or **Canary** deployments
- ⛵ Package the app with **Helm**
- 🌊 Try **GitOps** (Argo CD)
- 📜 Add **centralized logging** (Loki or ELK)
- 🔐 Add **image scanning** (Trivy) to Jenkins

---

## 13.10 🚑 Troubleshooting Quick Guide

| Problem                                      | Where to Look / What to Try                                  |
| -------------------------------------------- | ------------------------------------------------------------ |
| 🤖 Jenkins build fails                       | Console Output, tool names (JDK/Maven), credentials          |
| 🔨 `mvn deploy` fails with 401               | `settings.xml` server `id` and Nexus user permissions        |
| 🔍 `waitForQualityGate` waits forever        | SonarQube webhook to `/sonarqube-webhook/` missing           |
| 🐳 Container exits immediately               | `docker logs <name>`, check CMD/ENTRYPOINT                   |
| 🐳 Cannot reach app on server                | Port mapping `-p`, firewall / Security Group                 |
| ☸️ Pod in `ImagePullBackOff`                 | Image name/tag, registry credentials (imagePullSecret)       |
| ☸️ Pod in `CrashLoopBackOff`                 | `kubectl logs --previous`, config and probes                 |
| ☸️ Service not reachable                     | Selector labels match Pod labels? `kubectl get endpoints`    |
| 🏗️ Terraform state lock error                | Another apply is running, or release the stale lock          |
| ⚙️ Ansible `UNREACHABLE`                     | SSH key, user, IP, Security Group port 22                    |
| 🔥 Prometheus target DOWN                    | Port open? exporter running? correct target address          |
| 📈 Grafana shows "No data"                   | Data source URL, time range, query and label names           |

---

# 📌🧠 Complete DevOps Quick Revision

```text
🔄 DevOps
│
├── 🔗 Git & GitHub
│   ├── Repository, Commit, Branch, HEAD
│   ├── Working Directory → Staging → Repository → Remote
│   ├── merge vs rebase, reset vs revert
│   └── Pull Request, Webhook, GitHub Actions
│
├── 🔨 Maven
│   ├── pom.xml, GAV, packaging
│   ├── Lifecycle: validate → compile → test → package → verify → install → deploy
│   ├── Local / Central / Remote repositories
│   └── settings.xml, profiles, multi-module
│
├── 🤖 Jenkins
│   ├── Controller + Agents
│   ├── Jenkinsfile (Declarative pipeline)
│   ├── Credentials, Webhooks, Plugins
│   └── Integrations: Maven, SonarQube, Nexus, Docker, Kubernetes
│
├── 🔍 SonarQube
│   ├── Bug, Vulnerability, Hotspot, Code Smell
│   ├── Quality Profile (rules) vs Quality Gate (pass/fail)
│   └── Scanner, Token, Webhook
│
├── 📦 Nexus Repository
│   ├── Hosted, Proxy, Group
│   ├── maven-releases / snapshots / public
│   └── mvn deploy, Docker registry
│
├── 🐳 Docker
│   ├── Image, Container, Dockerfile, Registry
│   ├── Volumes, Networks, Compose
│   └── Multi-stage builds, security
│
├── 🏗️ Terraform
│   ├── Provider, Resource, Data, Variable, Output
│   ├── init → plan → apply → destroy
│   └── State, Remote Backend, Modules
│
├── ⚙️ Ansible
│   ├── Inventory, Playbook, Modules, Roles
│   ├── Handlers, Templates, Vault
│   └── Agentless (SSH), Idempotent
│
├── ☸️ Kubernetes
│   ├── Control Plane + Worker Nodes
│   ├── Pod, Deployment, Service, Ingress
│   ├── ConfigMap, Secret, PV/PVC
│   └── Probes, HPA, RBAC, Helm
│
├── 🔥 Prometheus
│   ├── Pull model, Exporters, /metrics
│   ├── PromQL, Alert Rules, Alertmanager
│   └── Counter, Gauge, Histogram, Summary
│
└── 📈 Grafana
    ├── Data Sources, Dashboards, Panels
    ├── Variables, Import, Explore
    └── Alerting, Provisioning
```

---

# 🧠⚡ Complete DevOps One-Line Memory

| Tool / Concept                | Easy Memory                                              |
| ----------------------------- | -------------------------------------------------------- |
| 🔄 **DevOps**                 | Dev + Ops Working Together With Automation               |
| 🔁 **CI**                     | Merge → Build → Test Automatically                       |
| 📦 **Continuous Delivery**    | Always Ready to Release (Manual Approval)                |
| 🚀 **Continuous Deployment**  | Automatic Release to Production                          |
| 🔗 **Git**                    | Time Machine for Code                                    |
| 🐙 **GitHub**                 | Online Home for Git Repositories                         |
| 🔀 **Pull Request**           | Ask to Review and Merge                                  |
| 🔨 **Maven**                  | Build and Dependency Tool for Java                       |
| 📄 **pom.xml**                | Maven Project File                                       |
| 🤖 **Jenkins**                | CI/CD Automation Server (Port 8080)                      |
| 📄 **Jenkinsfile**            | Pipeline as Code in Git                                  |
| 🔍 **SonarQube**              | Automatic Code Quality Reviewer (Port 9000)              |
| 🚦 **Quality Gate**           | Pass / Fail for Code Quality                             |
| 📦 **Nexus**                  | Private Storage for Artifacts (Port 8081)                |
| 🏠🪞🧩 **Hosted / Proxy / Group** | Our Own / Cache / One URL                            |
| 🐳 **Docker**                 | Package Apps in Containers                               |
| 📦 **Image vs Container**     | Template vs Running Instance                             |
| 🏗️ **Terraform**              | Create Infrastructure From Code                          |
| 📄 **Terraform State**        | Record of What Terraform Created                         |
| ⚙️ **Ansible**                | Configure Servers With YAML Over SSH                     |
| 🔁 **Idempotent**             | Run Again, Nothing Changes if Already Correct            |
| ☸️ **Kubernetes**             | Runs, Scales and Heals Containers                        |
| 📦 **Pod**                    | Smallest Kubernetes Unit                                 |
| 🚀 **Deployment**             | Rolling Updates and Rollbacks                            |
| 🌐 **Service**                | Stable Address for Pods                                  |
| 🔥 **Prometheus**             | Collects and Stores Metrics (Port 9090)                  |
| 🔍 **PromQL**                 | Query Language for Metrics                               |
| 🔔 **Alertmanager**           | Sends Alert Notifications (Port 9093)                    |
| 📈 **Grafana**                | Dashboards for Monitoring Data (Port 3000)               |

---

# 🗺️ Complete DevOps Learning Map

```text
                                 🔄 DevOps
                                     │
   ┌──────────────┬──────────────┬───┴──────────┬──────────────┬──────────────┐
   │              │              │              │              │              │
   ▼              ▼              ▼              ▼              ▼              ▼
  CODE          BUILD &        QUALITY &      PACKAGE &      INFRA &        MONITOR
                INTEGRATE      ARTIFACTS      DEPLOY         CONFIG
   │              │              │              │              │              │
   └── Git &      ├── Maven      ├── SonarQube  ├── Docker     ├── Terraform  ├── Prometheus
       GitHub     └── Jenkins    └── Nexus      └── Kubernetes └── Ansible    └── Grafana
```

### 🪜 Suggested Learning Order (Same as These Notes)

```text
1️⃣  Git & GitHub     → Save and share code
2️⃣  Maven            → Build the project
3️⃣  Jenkins          → Automate with a pipeline
4️⃣  SonarQube        → Check code quality
5️⃣  Nexus            → Store artifacts
6️⃣  Docker           → Containerize the app
7️⃣  Terraform        → Create infrastructure
8️⃣  Ansible          → Configure servers
9️⃣  Kubernetes       → Orchestrate containers
🔟  Prometheus       → Collect metrics
1️⃣1️⃣ Grafana          → Visualize and alert
```

---

# ⭐ Complete DevOps Final Memory

```text
DevOps
 │
 ├── How do we store and share code?
 │      └── Git & GitHub
 │
 ├── How do we build a Java project?
 │      └── Maven
 │
 ├── How do we automate the pipeline?
 │      └── Jenkins (Jenkinsfile + webhook)
 │
 ├── How do we check code quality and security?
 │      └── SonarQube (Quality Gate)
 │
 ├── Where do we store build artifacts?
 │      └── Nexus Repository
 │
 ├── How do we package the app?
 │      └── Docker
 │
 ├── How do we create cloud infrastructure from code?
 │      └── Terraform
 │
 ├── How do we configure the servers?
 │      └── Ansible
 │
 ├── How do we run and scale containers?
 │      └── Kubernetes
 │
 ├── How do we collect metrics and alerts?
 │      └── Prometheus + Alertmanager
 │
 └── How do we see everything on dashboards?
        └── Grafana
```

---

<p align="center">

## 🔄 DevOps — Build, Ship, Run, Monitor, Repeat

**Learn → Practice → Build → Deploy → Automate**

</p>
