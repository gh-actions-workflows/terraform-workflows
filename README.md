# Terraform Action

Faça o deploy do seu código Terraform com apenas um arquivo.

## Como utilizar?

```yaml
name: Deploy Infra
on: [push]

jobs:
    infra:
        uses: gh-actions-workflows/terraform-workflows/.github/workflows/terraform.yaml@1.4
        with:
            terraform_version: '1.7.5'
            working-directory: ./ # Diretório onde está o código Terraform
        secrets:
            tf_api_token: ${{ secrets.TF_API_TOKEN }} # Crie um projeto no Terraform Cloud e gere o Token de API - https://app.terraform.io
```

Para mais detalhes sobre o funcionamento consulte o arquivo: [terraform.yaml](https://github.com/gh-actions-workflows/terraform-workflows/blob/master/.github/workflows/terraform.yaml).
