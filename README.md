
<div align="center">
<img width="200" height="200" alt="Image" src="https://github.com/user-attachments/assets/bd51a591-dcd1-4318-af00-2a6cc1836a07" alt="AWS Logo"/>

# HashiCorp Certified: Terraform Associate (004) 

Study & Prep Guide

</div>



#  

Repositório dedicado à preparação para a certificação **HashiCorp Certified: Terraform Associate (004)**. Aqui estão reunidas anotações teóricas, exemplos práticos em HCL e resoluções de questões simuladas.

---

## 🎯 Informações Gerais do Exame

| Item | Detalhe |
| :--- | :--- |
| **Versão Testada** | Terraform v1.12 |
| **Duração** | 1 hora (60 minutos) |
| **Formato** | Múltipla escolha, resposta múltipla e verdadeiro/falso |
| **Preço** | $70.50 USD (+ taxas locais) |
| **Validade** | 2 anos |

---

## 🗺️ Mapa de Estudos e Progresso

### 1. Infrastructure as Code (IaC) with Terraform
- [ ] **1a.** O que é IaC (*Infrastructure as Code*)
- [ ] **1b.** Vantagens dos padrões de IaC
- [ ] **1c.** Gerenciamento de fluxos multi-cloud, nuvem híbrida e *service-agnostic*

### 2. Terraform Fundamentals
- [ ] **2a.** Instalação e versionamento de *providers* (uso de `required_providers` e `.terraform.lock.hcl`)
- [ ] **2b.** Como o Terraform utiliza *providers* (plugins)
- [ ] **2c.** Escrita de configurações usando múltiplos *providers*
- [ ] **2d.** Como o Terraform usa e gerencia o *state*

### 3. Core Terraform Workflow
- [ ] **3a.** O fluxo de trabalho principal: Write → Plan → Apply
- [ ] **3b.** Inicialização do diretório de trabalho (`terraform init`)
- [ ] **3c.** Validação da sintaxe e configuração (`terraform validate`)
- [ ] **3d.** Geração e revisão do plano de execução (`terraform plan`)
- [ ] **3e.** Aplicação das mudanças (`terraform apply`)
- [ ] **3f.** Remoção de infraestrutura (`terraform destroy`)
- [ ] **3g.** Formatação de código HCL (`terraform fmt`)

### 4. Terraform Configuration *(Novo no Edital 004)*
- [ ] **4a.** Diferença entre blocos `resource` e `data`
- [ ] **4b.** Referência a atributos de recursos e dependências cruzadas
- [ ] **4c.** Uso de variáveis (`var`) e saídas (`output`)
- [ ] **4d.** Tipos de dados complexos (`list`, `map`, `object`, `tuple`)
- [ ] **4e.** Configurações dinâmicas com expressões e funções nativas
- [ ] **4f.** **(Novo)** Regras de ciclo de vida (`depends_on`, `create_before_destroy`, etc.)
- [ ] **4g.** **(Novo)** Validação de configurações com *custom conditions* (`validation` block)
- [ ] **4h.** **(Novo)** Boas práticas para dados sensíveis, argumentos *write-only* e integração com Vault

### 5. Terraform Modules
- [ ] **5a.** Origens de módulos (*local paths*, *Terraform Registry*, *Git*)
- [ ] **5b.** Escopo de variáveis dentro de módulos
- [ ] **5c.** Utilização de módulos na configuração
- [ ] **5d.** Gerenciamento e restrição de versões de módulos

### 6. Terraform State Management
- [ ] **6a.** Funcionamento do backend local (`local`)
- [ ] **6b.** Mecanismos de *state locking* (bloqueio de estado em execuções concorrentes)
- [ ] **6c.** Configuração de backend remoto (S3, GCS, Azure Blob, HCP Terraform)
- [ ] **6d.** Gerenciamento de *drift* e comandos de estado (`refresh-only`, blocos `moved` e `removed`)

### 7. Maintain Infrastructure with Terraform
- [ ] **7a.** Importação de infraestrutura existente (`terraform import` e bloco `import`)
- [ ] **7b.** Inspeção de estado via CLI (`terraform state list`, `terraform state show`)
- [ ] **7c.** Níveis e uso de logs detalhados (`TF_LOG` e `TF_LOG_PATH`)

### 8. HCP Terraform *(Cloud)*
- [ ] **8a.** Criação de infraestrutura usando HCP Terraform
- [ ] **8b.** Recursos de colaboração, governança e *Policy Enforcement* (OPA / Sentinel)
- [ ] **8c.** **(Novo)** Organização de workspaces e projetos no HCP Terraform
- [ ] **8d.** Integração da CLI com HCP Terraform e comandos de execução remota (`terraform login`)

---

## ⚡ Comandos Essenciais

```bash
# Inicialização e Formatação
terraform init          # Baixa providers e inicializa o backend
terraform fmt           # Formata os arquivos .tf nos padrões do HCL
terraform validate      # Valida a sintaxe do código HCL

# Planejamento e Execução
terraform plan          # Mostra as alterações previstas
terraform apply         # Aplica as alterações na infraestrutura
terraform destroy       # Remove todos os recursos do state atual

# Inspeção e Estado
terraform state list    # Lista os recursos salvos no arquivo de state
terraform state show <ID> # Exibe os atributos de um recurso no state

# Debug e Logs
export TF_LOG=TRACE                     # Habilita logs detalhados (TRACE, DEBUG, INFO, WARN, ERROR)
export TF_LOG_PATH="./terraform.log"    # Salva o output do log num ficheiro

# Gestão de Estado Avançada
terraform state mv                      # Renomeia ou move recursos no state sem destruir
terraform state rm                      # Remove um recurso do tracking do state sem destruí-lo na nuvem
terraform refresh                       # Atualiza o state com o estado real da infraestrutura
```

## Organização do Repositório
```
01-iac-concepts/ - Anotações sobre os conceitos de IaC.

02-fundamentals-providers/ - Exemplos de declaração de providers e lockfile.

03-core-workflow/ - Prática dos comandos essenciais da CLI.

04-configuration-syntax/ - Variáveis, validações personalizadas e funções.

05-modules/ - Criação e consumo de módulos locais e remotos.

06-state-management/ - Exemplos de backend remoto e state lock.

07-maintenance-and-cli/ - Importação de recursos e gerenciamento de drift.

08-hcp-terraform/ - Notas sobre workspaces, projetos e Cloud.

mock-questions/ - Questões e simulados resolvidos para o exame.
```
## Referências:

- [ Informações sobe o exame](https://developer.hashicorp.com/certifications/terraform-associate)
- [Exame Learning Path](https://developer.hashicorp.com/terraform/tutorials/certification-004/associate-study-004)
- [Terraform Associate (004) Study Notes curso](https://cloudfluently.com/dashboard/courses/hashicorp-terraform-associate-004-study-notes/lessons/1e2f4123-cdef-493a-8b5d-8f7f125c1545)


