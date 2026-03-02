# kubenine-form1-project
A complete project of provisioning an EKS cluster, containerizing a Flask app, and automating deployment via GitHub Actions.

## Directory arch
`
.
├── app.py
├── requirements.txt
├── Dockerfile
├── k8s/
│   └── deployment.yaml
├── terraform/
│   ├── main.tf
│   └── outputs.tf
└── .github/
    └── workflows/
        └── deploy.yml
`

## Installing Terraform (Step-1)

Follow the steps to this document based on your machine: [https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
