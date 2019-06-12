## DevOps Exercise

#### Terraform
Objective: Deploy a T2.Micro EC2 instance including the supporting IAM role, VPC Networking, and Security Groups
- Security Group must allow access via port 22 for SSH
- EC2 instance must be accessible via the Internet
- Terraform Statefile must be located on an S3 bucket
- All necessary configurations must be captured in Terraform so the instance can be spun down when not in use
- Recommend using the Amazon Linux 2 AMI

#### Ansible
Objective: Configuring a fresh EC2 Instance with a complete installation of Minikube with no user input beyond launching the Ansible Playbook
- Ansible Playbook should include all the steps necessary to install Minikube.

#### Docker
Objective: Containerize an existing script in preparation for deploying it to Minikube
- Container must be built from a Dockerfile.
- Recommend writing a fairly simple script like the one located here: https://github.com/DivvyPayHQ/devops-interview

#### Helm
Objective: Use a helm chart to capture all the necessary configurations for deploying the script container to Minikube
- Must include all necessary manifests to support the script container.

#### CI/CD
Objective: Implement a pipeline that will redeploy the helm chart any time there's a commit to the master branch of the script's repo
- Should include steps for rebuilding the Docker container if the associated code changes
- Recommend using Gitlab's Free Tier for the code repo and CI/CD tooling.
- Recommend using a separate Ansible Playbook for the deployment of the new container to the minikube installation
