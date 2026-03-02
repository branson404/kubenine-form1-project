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

## AWS and Apply

- Configure AWS using `aws configure` by using this video: [https://youtu.be/p5JVYjhXfko](https://youtu.be/p5JVYjhXfko)
- Apply the terraform `main.tf` configuration
```
terraform init && terraform apply
```

## Create ECR repositary

Create ECR Repositary names 'flask-app' in AWS.

## Deploy code to github and Github actions

The local folder where you contain the clone of this repositary to be pushed to github, go to `Actions` tab: create a deploy.yaml file paste the code for Github actions to deploy to eks automatically. Before that go to settings of that repositary and at secret sections, add your AWS_ACCESS_KEY_SECRET & AWS_SECRET_ACCESS_KEY to the secrets.
