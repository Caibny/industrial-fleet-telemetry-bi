# 🚜 Industrial Fleet Telemetry & Operational Efficiency (BI)

Arquitetura de integração de dados via API REST e modelagem analítica em **Power BI (DAX & Power Query)** voltada para o monitoramento de eficiência operacional e gestão de frota industrial.

> **Nota de Privacidade:** Todos os endpoints, identificadores de equipamentos e volumes apresentados neste repositório são fictícios e ilustrativos, estruturados exclusivamente para demonstração técnica de arquitetura de dados e modelagem de indicadores.

---

### 🎯 Problema & Solução
Em operações industriais com movimentação intensa de materiais, dados brutos de telemetria costumam ficar isolados em plataformas operacionais, dificultando a visão consolidada de gargalos e ociosidade.

Este projeto estrutura um fluxo automatizado de extração e tratamento (ETL) para transformar eventos brutos de telemetria em indicadores gerenciais de tomada de decisão:
- **Disponibilidade Física:** Tempo em que o equipamento esteve apto para operar frente ao tempo programado.
- **Utilização:** Percentual de uso efetivo da frota disponível por turno e área.
- **Performance & OEE / TEEP:** Visão consolidada de eficiência operacional e aproveitamento da capacidade instalada.

---

### ⚙️ Arquitetura & Ferramentas
- **Extração & Tratamento (ETL):** Power Query (Linguagem M) e Python para consumo de API REST, tratamento de paginação, limpeza de timestamps e consolidação de tabelas fato/dimensão.
- **Modelagem & Cálculos:** Power BI com medidas em **DAX** para cálculo dinâmico de horas operacionais, ociosidade e comparativos entre turnos.
- **Automação de Rotina:** Atualização agendada para disponibilização diária dos indicadores logo no início do turno operacional.

---

### 📂 Estrutura do Repositório
- `/scripts`: Exemplos de consumo de API e tratamento de dados com variáveis de ambiente.
- `/dax`: Fórmulas estruturadas para cálculo de Disponibilidade, Utilização, OEE e TEEP.
- `/dados_mockados`: Base de exemplo fictícia para validação do modelo estrela (*Star Schema*).
