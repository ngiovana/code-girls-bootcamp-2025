# ☁️ Armazenamento na Nuvem com Amazon EBS e S3

## 📦 EBS (Elastic Block Store)  
- Armazenamento em **blocos**, semelhante a um disco rígido ou SSD.  
- Altamente confiável e pode ser anexado a qualquer instância **EC2**.  
- Cada instância EC2 já possui ao menos um volume EBS associado.  
- Permite **expansão rápida** de capacidade de forma escalável.  
- Ideal para:  
  - Bancos de dados transacionais,  
  - Logs de sistemas,  
  - Aplicações que exigem leitura e escrita com **baixa latência**.  

🔎 **Observações importantes**  
- Volumes EBS são criados dentro de uma **zona de disponibilidade (AZ)**, e só podem ser anexados a instâncias na mesma AZ.  
- É possível fazer **snapshots** (backups) que ficam salvos no S3 e podem ser usados para restaurar volumes.  

---

## 🗄️ S3 (Simple Storage Service)  
- Armazenamento de **objetos** (arquivos, imagens, vídeos, backups, etc).  
- Altamente escalável, seguro e durável (**11 9s de durabilidade**, ou seja, **99,999999999% ao ano**).  
- O que isso significa na prática: se você armazenar **10 milhões de objetos**, pode esperar perder **um único objeto a cada 10.000 anos**.  
- Essa alta durabilidade é possível porque o S3 mantém cópias redundantes dos dados em **múltiplos dispositivos e zonas de disponibilidade (AZs)**.  

- **Classes de armazenamento** para otimização de custo:  
  - **S3 Standard** → uso frequente  
  - **S3 Standard-IA** → acesso infrequente, mas alta disponibilidade  
  - **S3 One Zone-IA** → acesso infrequente em uma única zona  
  - **S3 Glacier / Glacier Deep Archive** → arquivamento de longo prazo, baixo custo  
  - **S3 Intelligent-Tiering** → muda automaticamente os objetos de classe conforme o padrão de acesso  

- Suporta **regras de ciclo de vida (lifecycle)** para automatizar a transição de objetos entre classes e arquivar no Glacier.  
- Ideal para:  
  - Armazenamento de mídias,  
  - Backups e arquivamento,  
  - Hospedagem de sites estáticos,  
  - Data lakes para análise de dados.  

---

## 📊 Comparação rápida
- **EBS** → armazenamento em blocos, anexado a instâncias EC2, ideal para dados de uso intensivo e persistente.  
- **S3** → armazenamento de objetos, ideal para grandes volumes de dados e acessos variados.  

---

## 📑 Comparação entre EBS, S3 e EFS

| Serviço | Tipo de Armazenamento | Caso de Uso Principal | Características |
|---------|------------------------|-----------------------|-----------------|
| **EBS** | Blocos | Bancos de dados, logs, apps que exigem baixa latência | Persistente, deve estar na mesma AZ da instância EC2, snapshots para backup |
| **S3**  | Objetos | Arquivos, mídias, backups, data lakes | Alta durabilidade (11 9s), várias classes de storage, ciclo de vida para otimização de custo |
| **EFS** | Arquivos | Compartilhamento de arquivos entre múltiplas instâncias EC2 | Sistema de arquivos elástico, gerenciado, escalável automaticamente, acessível em várias AZs |

