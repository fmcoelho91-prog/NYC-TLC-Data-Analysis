#  NYC Yellow Taxi | Fleet & Revenue Optimization Dashboard

##  Project Overview

Este projeto foi desenvolvido no âmbito do curso de **Data Analyst** e consiste na criação de um dashboard interativo em **Power BI** para analisar a operação da frota de táxis da **New York City Taxi & Limousine Commission (NYC TLC)**.

O objetivo foi transformar milhões de registos de viagens em informação útil para apoiar decisões de negócio, disponibilizando duas perspetivas distintas:

- **Vendor View** – Apoio à gestão da empresa e otimização da frota.
- **Employee View** – Apoio aos motoristas na maximização dos seus rendimentos.

---

#  Business Problem

O projeto procurou responder às seguintes questões:

- Quais são as zonas mais rentáveis para operar?
- Como reduzir quilómetros percorridos sem passageiros (Dead Miles)?
- Quais os horários com maior potencial de receita?
- Que tipo de viagens geram maior rendimento para os motoristas?

---

#  Ferramentas Utilizadas

- Power BI
- Power Query
- DAX
- Data Modelling
- Star Schema

---

#  Processo de Desenvolvimento

### Preparação dos Dados

- Limpeza dos dados em Power Query
- Remoção de valores inconsistentes
- Separação de colunas de data e hora
- Preparação da tabela de factos

### Modelação

- Construção de um modelo em Star Schema
- Criação da tabela Fact_Trips
- Implementação de relações entre dimensões
- Desenvolvimento de medidas em DAX

### Dashboard

Desenvolvimento de dois dashboards distintos para diferentes perfis de utilizador.

---

#  Dashboard 1 — Vendor View

Objetivo: apoiar decisões estratégicas da empresa.

### Principais Indicadores

- Receita Total
- Receita por Zona
- Número de Viagens
- Distância Percorrida
- Rentabilidade por Localização

### Principais Descobertas

- Forte concentração da faturação em zonas específicas da cidade.
- Existência de oportunidades para reduzir Dead Miles através de uma melhor distribuição da frota.

### Recomendações

- Reposicionar veículos para zonas de maior procura.
- Reduzir circulação aleatória.
- Otimizar a distribuição da frota em função da procura.

![Vendor Dashboard](images/vendor_dashboard.png)

---

#  Dashboard 2 — Employee View

Objetivo: ajudar os motoristas a aumentar o rendimento por turno.

### Principais Indicadores

- Receita Média por Hora
- Receita por Distância
- Horários de Maior Procura
- Duração Média das Viagens

### Principais Descobertas

- Viagens de maior duração apresentam melhor rendimento médio.
- O período entre as 14h e as 18h concentra maior potencial de receita.

### Recomendações

- Priorizar viagens de maior duração.
- Adaptar os turnos aos horários de maior procura.

![Employee Dashboard](images/employee_dashboard.png)

---

#  Estrutura do Repositório

```
📁 powerbi/
    NYC_Taxi_Dashboard.pbix

📁 images/
    vendor_dashboard.png
    employee_dashboard.png


📄 README.md
```

---

#  Competências Demonstradas

- Power BI
- Power Query
- DAX
- Data Modelling
- ETL
- Star Schema
- Business Intelligence
- Dashboard Design
- Data Storytelling
- Performance Analysis
