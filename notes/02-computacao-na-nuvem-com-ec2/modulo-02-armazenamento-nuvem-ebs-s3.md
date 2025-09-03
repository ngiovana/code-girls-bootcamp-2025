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
- Altamente escalável, seguro e durável (11 9s de durabilidade).  
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
