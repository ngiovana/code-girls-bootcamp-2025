# ☁️ Entendendo as Instâncias EC2 e a Otimização de Recursos na AWS

## 📌 O que é o EC2?
O **EC2 (Elastic Compute Cloud)** permite criar **máquinas virtuais na AWS** com sistema operacional Windows ou Linux.  
Uma instância EC2 é composta por:  
- CPU  
- Rede  
- Memória  
- Disco  
- Sistema Operacional  

É possível ter:  
- Uma **máquina virtual isolada**, ou  
- **Várias máquinas virtuais** ao mesmo tempo dentro de um servidor, compartilhando os recursos disponíveis.  

No modelo Cloud, o EC2 se enquadra como **IaaS (Infrastructure as a Service)**.  

---

## 🤔 Como escolher a EC2 correta para minha aplicação?
Depende das **necessidades da aplicação** e da forma de usar os recursos de nuvem para buscar eficiência operacional e econômica.  

💡 **Dicas práticas:**  
- Se possível, **desligue instâncias à noite, em finais de semana ou em períodos sem uso** para economizar.  
- Utilize o **AWS Pricing Calculator** para estimar custos.  

---

# 📊 Tipos de Instâncias EC2

| Categoria              | Instância | Descrição |
|-------------------------|-----------|-----------|
| **General Purpose**     | A1        | ARM based core and custom silicon |
|                         | T2        | Tiny – Web servers and small DBs |
|                         | M4        | Main – App servers and general purpose |
| **Compute Optimised**   | C4        | Compute – CPU intensive apps and DBs |
|                         | z1d       | High Compute and High Memory – Gaming |
| **Memory Optimised**    | R4        | RAM – Memory Intensive apps and DBs |
|                         | X1        | Xtreme RAM – For SAP/Spark |
| **Accelerated Computing** | P2      | Processing optimised – Machine Learning |
|                         | G3        | Graphics Intensive – Video and Streaming |
|                         | F1        | Field Programmable – Hardware acceleration |
| **Storage Optimised**   | H1        | High Disk Throughput – Big data clusters |
|                         | I3        | IOPS – No SQL DBs |
|                         | D2        | Dense Storage – Data Warehousing |

📌 Observação:  
- A instância **C4** costuma ser uma das mais utilizadas.  
- Em geral, **quanto maior a letra do alfabeto, mais caro o recurso**.  

---

## 📖 Terminologia Importante
- O **EC2 fornece capacidade de computação na nuvem da AWS**.  
- As **Amazon Machine Images (AMIs)** estão disponíveis para escolha no momento da criação.  
- É possível definir segurança básica usando:  
  - **Firewall embutido da AWS**  
  - **Grupos de segurança** (Security Groups)  
  - Controle de **protocolo, porta e IPs de origem** para permitir ou negar acesso às instâncias EC2.  
- **Uma instância é uma máquina virtual dentro da AWS.**  

---

## 📈 Escalabilidade
A escalabilidade permite ajustar recursos conforme a demanda da aplicação:  

- **Escalar verticalmente:** aumentar ou reduzir capacidade em um mesmo nó (vCPUs, memória, armazenamento, rede).  
- **Escalar horizontalmente:** aumentar o número de recursos, adicionando mais instâncias, discos ou servidores para suportar a aplicação.  

---

## 💵 Modelos de Instâncias EC2

- **Sob demanda (On-Demand):**  
  - Paga-se uma taxa fixa por hora.  
  - Ideal para cargas irregulares e de curto prazo.  
  - Recomendada para testes e desenvolvimento.  

- **Reservadas (Reserved):**  
  - Mais baratas que as sob demanda.  
  - Compromisso de uso por 1 ou 3 anos.  
  - Desvantagem: pagar por tempo integral mesmo sem usar com frequência.  

- **Spot:**  
  - Oferece descontos de até **90%**.  
  - Bom para workloads flexíveis.  
  - Desvantagem: podem ser encerradas pela AWS a qualquer momento, com aviso prévio de 2 minutos.  

---
