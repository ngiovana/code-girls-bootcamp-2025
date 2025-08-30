# 🌐 Fundamentos Essenciais da Infraestrutura AWS

## 📍 Regions  
Cada **Region** é projetada para ser **isolada** das demais, proporcionando maior **tolerância a falhas** e **estabilidade**.  
- Uma região é composta por **duas ou mais Availability Zones (AZs)**.  

### 🔑 Pontos para considerar ao escolher uma Region:  
- **Compliance** → atender requisitos legais e regulatórios  
- **Disponibilidade de serviços** → nem todos os serviços estão em todas as regiões  
- **Custo** → preços podem variar entre regiões  
- **Latência** → quanto mais próxima a região do usuário final, menor o tempo de resposta  

---

## 🏢 Availability Zones (AZs)  
- Cada **Availability Zone** é um **data center independente**, com energia, refrigeração e rede próprias.  
- As AZs dentro de uma mesma região são **conectadas entre si**, garantindo **alta disponibilidade** e **recuperação de falhas**.  
- Os recursos são exclusivos da região escolhida, ou seja, ao criar algo em uma região, ele não aparece automaticamente em outra.  

---

# 📊 Principais Recursos AWS e suas Responsabilidades

| Recurso | Responsabilidade AWS | Responsabilidade do Cliente |
|---------|----------------------|-----------------------------|
| **Computação** |||
| EC2 (Elastic Compute Cloud) | Fornecer e gerenciar a infraestrutura de computação subjacente. | Configurar e manter o sistema operacional e aplicativos dentro da instância EC2. |
| LightSail | Implementar e gerenciar automaticamente os recursos de computação, armazenamento e rede. | Configurar e gerenciar aplicativos e dados do ambiente LightSail. |
| Elastic Beanstalk | Oferecer implantação e provisionamento automatizados de recursos para aplicativos de produção. | Desenvolver e gerenciar o código do aplicativo, bem como configurar o ambiente de execução no Elastic Beanstalk. |
| EKS (Elastic Container Service para Kubernetes) | Gerenciar a infraestrutura subjacente para execução e orquestração de contêineres Kubernetes. | Configurar e gerenciar os aplicativos e contêineres no ambiente Kubernetes. |
| AWS Lambda | Gerenciar a execução de funções na nuvem de forma escalável e sem servidor. | Desenvolver e carregar funções personalizadas para AWS Lambda, bem como configurar eventos e triggers associados. |
| **Migração** |||
| DMS (Serviço de Migração de Banco de Dados) | Facilitar a migração de bancos de dados locais para a AWS. | Configurar e monitorar o processo de migração, incluindo seleção de fontes e destinos de dados. |
| SMS (Serviço de Migração de Servidor) | Auxiliar na migração de servidores locais para a AWS. | Planejar, preparar e executar a migração de servidores, incluindo configuração de conectividade e integração de sistemas. |
| Snowball | Fornecer uma solução para transferência de grandes volumes de dados para a AWS. | Preparar e gerenciar os dados a serem transferidos usando o dispositivo Snowball. |
| **Armazenamento** |||
| Amazon Glacier | Oferecer armazenamento seguro e de baixo custo para arquivamento e backup de dados. | Gerenciar políticas de retenção e acessos aos dados armazenados no Amazon Glacier. |
| Amazon Elastic Block Store (EBS) | Fornecer armazenamento em bloco para instâncias EC2. | Configurar e gerenciar volumes EBS, incluindo snapshots e políticas de backup. |
| AWS Storage Gateway | Integrar aplicativos locais com armazenamento em nuvem. | Configurar e gerenciar a integração entre os sistemas locais e o armazenamento em nuvem usando o AWS Storage Gateway. |

---
