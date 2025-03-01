# Desafio Terraform - VExpenses

## Descrição Técnica do Código Original
O código original cria uma infraestrutura básica na AWS, incluindo:
- Uma VPC, subnet, Internet Gateway e tabela de rotas.
- Um grupo de segurança permitindo SSH de qualquer lugar e todo o tráfego de saída.
- Uma instância EC2 com Debian 12, atualizada via user data.

## Melhorias Implementadas
1. **Segurança**:
   - Restrição de acesso SSH para um IP confiável.
   - Remoção da geração de chaves SSH no Terraform.
   - Adição de regras para permitir tráfego HTTP/HTTPS.

2. **Automação do Nginx**:
   - Instalação e inicialização automática do Nginx via user data.

## Instruções de Uso
1. **Pré-requisitos**:
   - Terraform instalado.
   - Credenciais da AWS configuradas.

2. **Comandos**:
   - `terraform init`: Inicializa o Terraform.
   - `terraform plan`: Verifica o plano de execução.
   - `terraform apply`: Aplica a configuração.
   - `terraform destroy`: Destrói a infraestrutura criada.

3. **Substituições**:
   - Substitua `SEU_IP_AQUI/32` no arquivo `main.tf` pelo seu IP.
   - Substitua `SUA_CHAVE_SSH_AQUI` pelo nome da sua chave SSH na AWS.
