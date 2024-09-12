# Previsão de Vendas de Fertilizantes com IA Local

Este projeto utiliza técnicas de machine learning para prever a venda de fertilizantes para o próximo mês, com base em um dataset meteorológico e agronômico. A previsão é feita de forma local, sem a necessidade de chamadas para APIs externas, e incorpora a normalização e padronização de dados, além de uma arquitetura robusta para desnormalizar as previsões de volta aos seus valores reais.

## Visão Geral

O objetivo deste projeto é prever a demanda futura por diferentes tipos de fertilizantes em regiões agrícolas. O modelo é baseado em dados climáticos (como temperatura e precipitação) e de qualidade do solo (pH, nutrientes, etc.), e prevê as vendas para o mês seguinte.

### Principais Funcionalidades

- **Previsão de vendas para o mês desejado**: Utiliza algoritmos de machine learning treinados localmente para prever as vendas de fertilizantes.
- **Normalização e padronização de dados**: Inclui funções automáticas para verificar a normalidade dos dados e aplicar a transformação adequada.
- **Desnormalização de resultados**: Transforma os resultados de volta para os valores originais, tornando a previsão mais intuitiva para interpretação.
- **Machine Learning Local**: Substituição de uma chamada de API para um modelo local.

## Arquitetura

A arquitetura do projeto é composta das seguintes partes principais:

1. **Leitura e Pré-processamento dos Dados**
   
2. **Funções Para tratamento da base**

3. **Machine Learning Local**
   - A previsão é realizada utilizando técnicas de machine learning diretamente no código, sem a necessidade de chamadas para APIs externas. Um algoritmo é aplicado para prever as vendas com base nos dados históricos, usando os valores de temperatura, umidade, e outros fatores.
   
4. **One-Hot Encoding**
   - Para preparar os dados categóricos (como `Região`, `Tipo de Solo` e `Mês`), utilizamos `pd.get_dummies` para transformar essas colunas em variáveis. Isso facilita o uso de algoritmos de machine learning.

5. **Desnormalização**
   - Após gerar as previsões, os valores normalizados são transformados de volta aos seus valores reais utilizando a função `desnormaliza`.

6. **Previsão para o todos os meses, regiões e produtos**

### Diagrama da Arquitetura

```plaintext
+--------------------+
|  Leitura de Dados  |
+--------------------+
         |
         v
+------------------------+       +--------------------+
| Verificação de Normalidade|---->| Normalização/Padronização |
+------------------------+       +--------------------+
         |
         v
+----------------------+
|  Algoritmo de ML     |
+----------------------+
         |
         v
+-----------------------+
|  Desnormalização      |
+-----------------------+
         |
         v
+---------------------+
|   Previsão Final    |
+---------------------+
