# Jenkins-On-Server-Java-Application

# STEP 1: Deploying Java Application Locally



# MAIN PROJECT

# Tools
- AWS
- GIT/GITHUB
- JENKINS
- MAVEN
- DOCKER
- SONARQUBE
- NEXUS
- KUBERNETES(EKS)
- TERRAFORM
- ANSIBLE

# Tools And Their Usage

- Linux- for scripts and command
- Git+Github-As a Source Code Management
- AWS-Cloud Service Provider
- SonarQube-for code analysis
- Maven- for building project
- Nexus-for storing artifacts
- Docker for creating images
- Dockerhub- for storing images
- Kubernetes(EKS)- for deployment purposes
- Terraform- for creating server infrastructure
- Ansible- for installing softwares

# Set Up Phases

PHASE 1: Infrastructure Setup

PHASE 2: Dependency Setup

- in this phase we add dependencies of the project like credentials, tools.

PHASE 3: Deployment Phase

- final build of project with all the jenkins stages

# Phase 1: Infrastructure Setup

1. Setting Jenkins Server

a. create scripts to install jenkins on a server

b. either using plugins or installing packages directly on server install terraform, ansible, docker, K8s and Git on same Server

c. After setting up the jenkins server, add Maven tool

d. Configure AWS user too

2. Git/Github Setup (Public/Private)

a. create a repo for placing all codes

b. for public repo-no creds required

c. for private repo-creds required

3. Kubernetes (EKS) Setup

a. Using EKS or Kubeadm setup the K8s cluster
- setup worker nodes
- Have details of Users/roles
- Information about Kubeconfig file

4. Terraform Scripts

a. create Terraform modules for having 3 servers for the working using jenkins job
- Sonar Server
- Nexus Server
- Test Server

b. place the terraform script in the github for working

5. Nexus And Sonar Server Setup

a. Download and install the Nexus Server
- verify its working at Port 8081
b. Download and install the Sonar Server
- verify its working at Port 9000

6. Test Server Setup

a. using ansible playbook script from jenkins job install the following 
- Docker
- Git
- Maven

7. Plugins And Credentials

a. Plugins
- install the SonarQube Plugin
- install the AWS Credentials Plugin
b. Credentials
- AWS Keys
- Private Key for Ansible
- Nexus Username And Password
- Dockerhub Creds(Optional for ECR)

# Phase 2: Dependency Setup

1. Docker Repository

a. Create Repository For Docker Images
- ECR
- Dockerhub

2. SonarQube Project Setup

a. Create A Sonarqube Project
b. Then API Token from security
c. update setting of sonarqube server in system and scanner in tools
d. Add Token in credentials

# Phase 3: Deployment Phase

1. Options
- Build Discarder
- Timeout
- Clean Workspace

2. Tools
- Maven

3. Environment
- Custom Variables
- Credentials

4. Agents
- Based On Requirements

5. Stages
- Checkout
- Sonar Test
- Maven Build
- Nexus Artifacts
- Docker Build
- Dockerhub Push/ECR Push
- K8s Deployment
- Post Actions


