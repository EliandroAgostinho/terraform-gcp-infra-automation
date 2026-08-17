📘 README.md — Automação da Implantação de Infraestrutura Usando Terraform (GCP)

Projeto desenvolvido no laboratório Automação da Implantação de Infraestrutura Usando Terraform, demonstrando provisionamento automatizado, organização modular e boas práticas de IaC no Google Cloud.

🚀 Visão Geral

Este repositório contém a implementação completa do laboratório de automação de infraestrutura com Terraform no Google Cloud.
O objetivo é demonstrar como o Terraform permite criar recursos cloud de forma declarativa, repetível e segura, eliminando configurações manuais e garantindo consistência entre ambientes.



A infraestrutura provisionada inclui:

-Uma instância Compute Engine

  -Um bucket Google Cloud Storage
  
  -Variáveis, provider e outputs organizados em ficheiros separados
  
  -Fluxo completo de init → plan → apply → destroy



🧱 Arquitetura dos Recursos

Compute Engine Instance
    ↓
Google Cloud Storage Bucket



📂 Estrutura do Projeto

tfinfra/
│
├── provider.tf          # Configuração do provider Google Cloud
├── variables.tf         # Variáveis utilizadas nos recursos
├── instance.tf          # Instância Compute Engine
├── bucket.tf            # Bucket GCS
├── outputs.tf           # Outputs do Terraform
└── .gitignore           # Exclusões (state, cache, etc.)

⚙️ Recursos Criados

🖥️ Instância Compute Engine
  -Tipo: e2-micro
  
  -Imagem: Debian 11
  
  -Rede: default
  
  -Labels e metadados conforme o laboratório

🗄️ Bucket Google Cloud Storage
  -Nome único global
  
  -Região definida no laboratório
  
  -Configuração básica de armazenamento


▶️ Como Executar

1. Inicializar o Terraform -> terraform init
2. Validar o plano -> terraform plan
3. Aplicar a infraestrutura -> terraform apply
4. Destruir a infraestrutura (opcional) -> terraform destroy
