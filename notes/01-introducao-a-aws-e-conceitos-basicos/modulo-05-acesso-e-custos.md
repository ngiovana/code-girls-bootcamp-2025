# 🚀 Primeiros Passos com Acesso Seguro e Controle de Custos na AWS

## 📌 Formas de criar recursos na AWS
Você pode criar recursos na AWS de diferentes formas:  
1. **Portal AWS (Console)** – interface gráfica acessada pelo navegador.  
2. **AWS SDK** – bibliotecas de programação para integrar com aplicações.  
3. **Cloud Shell** – ambiente de linha de comando integrado no console AWS.  

💡 *Curiosidade*:  
- Região **mais cara** → São Paulo (sa-east-1)  
- Região **mais barata** → Norte da Virgínia (us-east-1)  

---

## 🔑 IAM – Identity and Access Management
O **IAM** é o serviço responsável por **gerenciar identidades, permissões e acessos** na AWS.  

- O **usuário root** cria **grupos de usuários**.  
- Os **usuários** adicionados aos grupos herdam as **permissões** definidas no grupo.  
- Após a criação, deve-se **habilitar uma senha** para permitir acesso ao painel (console AWS).  

---

## 🔐 Formas de Acesso: Console, Cloud Shell e AWS CLI
- **Console AWS** → acesso via navegador, usado nas primeiras aulas.  
- **Cloud Shell** → ambiente interativo em shell, integrado ao console.  
- **AWS CLI (Command Line Interface)** → comandos executados para criar e gerenciar recursos.  

---

## ⚙️ Automação com Usuários e Grupos
Passos básicos para configurar e automatizar:  
1. Instalar o **Git Bash**.  
2. Instalar o **AWS CLI**.  
3. Configurar o **AWS CLI** (chaves de acesso, região etc.).  
4. Criar os **Grupos**.  
5. Executar o **script** para criação de usuários/grupos.  

---

## 📖 Glossário
- **EC2 (Elastic Compute Cloud)** → cria e gerencia máquinas virtuais na nuvem.  
- **S3 (Simple Storage Service)** → armazenamento de objetos (arquivos, imagens, vídeos, backups).  
- **IAM (Identity and Access Management)** → gerencia usuários, permissões e papéis.  
- **RDS (Relational Database Service)** → banco de dados relacional gerenciado (MySQL, PostgreSQL, Oracle etc.).  
- **Lambda** → serviço *serverless* que executa funções sem necessidade de servidores.  
- **VPC (Virtual Private Cloud)** → rede privada e isolada para organizar serviços de forma segura.  
- **CloudWatch** → monitoramento e observabilidade, com métricas, logs e alertas para os recursos AWS.  

---
