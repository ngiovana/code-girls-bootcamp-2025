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
