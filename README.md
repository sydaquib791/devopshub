# devopshub
#!/bin/bash

set -e

REPO_NAME="devopshub"

# Verify we're inside the correct repository
if [[ "$(basename "$PWD")" != "$REPO_NAME" ]]; then
    echo "Please run this script from the '$REPO_NAME' repository root."
    exit 1
fi

echo "Creating DevOps documentation directory structure..."

mkdir -p \
Linux \
App-Server-Web-Server \
Bash-Scripting \
Git-GitHub \
AWS/{Cloud-Introduction,Amazon-EC2,VPC,VPC-Peering,IAM,S3,Route53-CDN,CloudWatch-CloudTrail,Auto-Scaling-Groups,Load-Balancers,RDS,Lambda,API-Gateway,KMS,SQS,Amazon-MQ,Secrets-Manager,WAF,Systems-Manager/Parameter-Store,AWS-Architecture} \
Jenkins \
Docker \
ECS \
Terraform \
Kubernetes \
ArgoCD \
Jenkins-Pipeline \
Prometheus-Grafana \
Ansible

echo "Creating README.md..."

cat > README.md <<'EOF'
# DevOps Hub

Welcome to **DevOps Hub**.

This repository contains structured documentation, notes, hands-on labs, practicals, assignments, challenges, task solutions, and learning resources covering the complete DevOps learning journey.

## Repository Structure

```text
Linux/
App-Server-Web-Server/
Bash-Scripting/
Git-GitHub/
AWS/
├── Cloud-Introduction/
├── Amazon-EC2/
├── VPC/
├── VPC-Peering/
├── IAM/
├── S3/
├── Route53-CDN/
├── CloudWatch-CloudTrail/
├── Auto-Scaling-Groups/
├── Load-Balancers/
├── RDS/
├── Lambda/
├── API-Gateway/
├── KMS/
├── SQS/
├── Amazon-MQ/
├── Secrets-Manager/
├── WAF/
├── Systems-Manager/
│   └── Parameter-Store/
└── AWS-Architecture/
Jenkins/
Docker/
ECS/
Terraform/
Kubernetes/
ArgoCD/
Jenkins-Pipeline/
Prometheus-Grafana/
Ansible/
```
EOF

echo
echo "Directory structure created successfully."
echo "README.md updated successfully."

echo
echo "Repository structure:"

