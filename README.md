# kubenine-form1-project
A complete project of provisioning an EKS cluster, containerizing a Flask app, and automating deployment via GitHub Actions.

## Directory arch
```
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
```

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

In the local folder containing the cloned repository, go to the Actions tab on GitHub. Create a deploy.yml file and paste the workflow code to deploy to EKS automatically. Before running the workflow, go to the repository settings and add your AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY in the Secrets section.

## Conclusion

There were some issues in the code provided by Kubenine. To simplify, there were two errors. Once these are resolved, the project will succeed.
