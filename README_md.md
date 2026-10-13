# Dashboard de Vendas do Xbox Game Pass

## Sobre o Projeto

Dashboard interativo desenvolvido em Excel para analisar as vendas de assinaturas do Xbox Game Pass. O objetivo é transformar uma base de dados bruta em informações visuais claras, permitindo acompanhar o desempenho de vendas e apoiar decisões com base em dados.

Projeto desenvolvido como desafio prático do curso **Excel Avançado com IA e Claude** (Santander Open Academy / DIO).

## Perguntas de Negócio

O dashboard foi construído para responder a quatro perguntas, todas filtráveis pelo tipo de assinatura (Mensal, Trimestral ou Anual):

1. Qual o total de vendas de assinaturas, com todos os planos agregados?
2. Qual o faturamento total, separado entre assinaturas com e sem renovação automática?
3. Qual o total de vendas do complemento EA Play Season Pass?
4. Qual o total de vendas do complemento Minecraft Season Pass?

## Dados Utilizados

A base de exemplo utilizada no curso está na aba **Bases**, com 295 registros de assinantes, referentes ao período de 01/01/2024 a 31/12/2024. Cada registro contém:

| Coluna | Descrição |
|---|---|
| Subscriber ID | Identificador do assinante |
| Name | Nome do assinante |
| Plan | Plano contratado (Core, Standard ou Ultimate) |
| Start Date | Data de início da assinatura |
| Auto Renewal | Renovação automática (Yes/No) |
| Subscription Price | Preço do plano |
| Subscription Type | Tipo de assinatura (Monthly, Quarterly ou Annual) |
| EA Play Season Pass | Contratou o EA Play (Yes/No) |
| EA Play Season Pass Price | Valor do EA Play |
| Minecraft Season Pass | Contratou o Minecraft Season Pass (Yes/No) |
| Minecraft Season Pass Price | Valor do Minecraft Season Pass |
| Coupon Value | Valor do cupom de desconto |
| Total Value | Valor total da assinatura (preço do plano + complementos − cupom) |

## Estrutura do Arquivo

O arquivo possui quatro abas:

- **Dashboard** (visível): painel final com os indicadores, o gráfico e a segmentação de dados.
- **Cálculos** (oculta): tabelas dinâmicas que respondem às perguntas de negócio.
- **Bases** (oculta): tabela com os dados brutos.
- **Assets** (oculta): paleta de cores, logos e ícones usados na identidade visual.

## Recursos Utilizados

- Tabelas dinâmicas para agregar os dados
- Segmentação de dados (Subscription Type) conectada às três tabelas dinâmicas
- Gráfico dinâmico de barras com o faturamento por renovação automática
- Big Numbers: indicadores em caixas de texto vinculadas às células com `GETPIVOTDATA`
- Identidade visual com a paleta de cores do Xbox, sem linhas de grade e com abas de apoio ocultas

## Como Usar

1. Baixe o arquivo `Dashboard_Xbox.xlsx` e abra no Excel.
2. Na aba **Dashboard**, clique em um tipo de assinatura na segmentação de dados para filtrar os números e o gráfico. O arquivo abre filtrado em Quarterly.
3. Os Big Numbers e o gráfico se atualizam automaticamente conforme o filtro.

## Como Reproduzir

1. Coloque os dados na aba **Bases** e formate como Tabela do Excel.
2. Na aba **Cálculos**, insira três tabelas dinâmicas a partir dessa tabela:
   - Linhas: Auto Renewal; Valores: soma de Total Value
   - Linhas: Plan; Valores: soma de EA Play Season Pass Price
   - Linhas: Plan; Valores: soma de Minecraft Season Pass Price
3. Em cada tabela dinâmica, coloque Subscription Type nos filtros.
4. Insira uma segmentação de dados de Subscription Type e conecte-a às três tabelas dinâmicas (Relatório de Conexões).
5. Crie um gráfico dinâmico de barras a partir da tabela de Auto Renewal e leve-o para a aba **Dashboard**.
6. Crie os Big Numbers: insira uma caixa de texto, selecione-a, digite `=` na barra de fórmulas e clique na célula com o `GETPIVOTDATA` do total.
7. Organize o layout com formas, imagens e a paleta de cores, desative as linhas de grade e oculte as abas de apoio.

## Autora

Aura Gaspar Ribeiro
