# Lab5-Deploy de app web com docker na AWS com ECS

![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Engenharia de Dados](https://img.shields.io/badge/Engenharia%20de%20Dados-orange?style=for-the-badge)

> **Resumo:** Este é um Lab de nível avançado. Neste projeto tive a chance de aprender um recurso cada vez mais importante para a automação de deploy de aplicações na nuvem: Como fazer o deploy da aplicação em um container Docker usando balanceamento de carga e serviço DNS. Para isso, utilizei o Amazon Elastic Container Service (ECS) e alguns recursos complementares. No total serão 28 recursos criados na AWS via IaC com Terraform.

---

## 📂 Estrutura do Projeto

```bash
Lab5-Deploy-de-app-web-com-docker-na-AWS-com-ECS/
├── IaC/                     # Diretório dos arquivos da automação para deploy da aplicação
│   ├── main.tf              # Orquestrador principal da infraestrutura do cluster ECS
│   ├── outputs.tf           # Definição das saídas (ALB - Aplication Load Balancer)
│   ├── providers.tf         # Configuração do provedor (AWS)
│   ├── security_group.tf    # Regras de Firewall e Grupos de Segurança
│   ├── terraform.tfvars     # Atribuição de valores para as variáveis
│   ├── variables.tf         # Declaração das variáveis do projeto
│   ├── vars.env             # Variáveis de ambiente locais
│   └── vpc.tf               # Configuração de Rede (VPC, Subnets)
├── .gitattributes
├── Dockerfile               # Configuração da imagem Docker da aplicação
├── LEIAME.txt               # Instruções adicionais
├── LICENSE
└── README.md                # Documentação do projeto
```

---

[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/T99Nf8R891o)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thiagoviniciusbsantos/)
