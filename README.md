# Terraform Workflow

Deploy your Terraform code with just one file.

## How to use?

```yaml
name: Deploy Infra
on: [push]

jobs:
    infra:
        uses: gh-actions-workflows/terraform-workflows/.github/workflows/terraform.yaml@1.4
        with:
            terraform_version: '1.7.5'
            working-directory: ./ # Directory where the Terraform code is located
        secrets:
            tf_api_token: ${{ secrets.TF_API_TOKEN }} # Create a project on Terraform Cloud and generate the API Token - https://app.terraform.io
```

For more details on how it works, see the file: [terraform.yaml](https://github.com/gh-actions-workflows/terraform-workflows/blob/master/.github/workflows/terraform.yaml).
