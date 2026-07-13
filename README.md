# 🚖 NYC Yellow Taxi - Fleet & Revenue Optimization Dashboard

## Resumo do Projeto
Este projeto consiste num painel de controlo interativo desenvolvido em **Power BI** para analisar os dados operacionais da Taxi and Limousine Commission (NYC TLC) de Nova Iorque. O objetivo principal foi criar uma ferramenta de duplo impacto:
1. **Vendor View (Empresa):** Identificar zonas de maior faturação para reduzir 'Dead Miles' (quilómetros a vazio).
2. **Employee View (Motorista):** Entregar táticas reais para maximizar o ganho por hora e otimizar turnos de condução.

## Tecnologias Utilizadas
* **Power BI:** Visualização de dados e criação de dashboards.
* **Power Query (M):** Processamento ETL (Extract, Transform, Load), limpeza de dados (ex: remoção de datas inconsistentes) e separação de timestamps.
* **DAX:** Criação de métricas financeiras centralizadas e tabelas virtuais (`DATATABLE`).

## Arquitetura de Dados (Star Schema)
Para garantir alta performance e escalabilidade na leitura de milhões de registos, o modelo foi construído com base num **Star Schema** puro:
* **Tabela de Factos (`Fact_Trips`):** Centralização dos valores transacionais (distâncias, valores financeiros).
* **Role-Playing Dimension:** Utilização de relações duplas (ativas e inativas) na tabela de Zonas para cruzar `Pickup` e `Dropoff` sem duplicar a base de dados.
* **Integridade de Dados:** Utilização de lógicas de segurança em DAX, como a função `DIVIDE`, para isolar erros de divisão por zero causados por anomalias na base de dados original (ex: veículos com 0 milhas registadas).

## 📊 Dashboards & Insights

### 1. Vendor View (Visão da Empresa)
Foco no aumento de volume e eficiência da frota.
* **Insight:** Forte concentração de receita em zonas específicas (ex: Lincoln Square East).
* **Recomendação:** Adoção de uma estratégia de alocação proativa em vez de circulação aleatória, mitigando drasticamente os 'Dead Miles'.
*(Adiciona aqui a imagem do Vendor View usando este código: `![Vendor Dashboard](images/nome_da_tua_imagem_vendor.png)`)*

### 2. Employee View (Visão do Motorista)
Foco na rentabilidade real por turno de condução.
* **Insight:** Viagens mais longas aumentam exponencialmente o rendimento médio (de ~$12 para +$60), eliminando o 'tempo morto' não remunerado entre viagens curtas.
* **Recomendação:** Priorizar viagens de maior duração e alinhar horários com as janelas de pico (14h-18h).
*(Adiciona aqui a imagem do Employee View usando este código: `![Employee Dashboard](images/nome_da_tua_imagem_employee.png)`)*

## 📁 Ficheiros Neste Repositório
* NYC_Taxi_Dashboard.pbix: Ficheiro completo do Power BI.
* Apresentação_Executiva.pdf: Slides com as recomendações de negócio.
* /images: Imagens do modelo arquitetónico e dashboards.

---
*Projeto desenvolvido no âmbito de Análise e Engenharia de Dados.*
