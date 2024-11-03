# Previsão de Vendas de Fertilizantes com IA Local e IA Generativa

Este projeto utiliza técnicas de machine learning para prever a venda de fertilizantes para o próximo mês, com base em um dataset meteorológico e agronômico. A previsão é feita de forma local, sem a necessidade de chamadas para APIs externas, e incorpora a normalização e padronização de dados, além de uma arquitetura robusta para desnormalizar as previsões de volta aos seus valores reais.

## Visão Geral

O objetivo deste projeto é prever a demanda futura por diferentes tipos de fertilizantes em regiões agrícolas. O modelo é baseado em dados climáticos (como temperatura e precipitação) e de qualidade do solo (pH, nutrientes, etc.), e prevê as vendas para o mês seguinte.

### Principais Funcionalidades

- **Previsão de vendas para o mês desejado**: Utiliza algoritmos de machine learning treinados localmente para prever as vendas de fertilizantes.
- **Normalização e padronização de dados**: Inclui funções automáticas para verificar a normalidade dos dados e aplicar a transformação adequada.
- **Desnormalização de resultados**: Transforma os resultados de volta para os valores originais, tornando a previsão mais intuitiva para interpretação.
- **Machine Learning Local**: Substituição de uma chamada de API para um modelo local.
- **IA Generativa para Insights**: Integração com o modelo Gemini AI para gerar insights adicionais com base nas previsões.

## Arquitetura

A arquitetura do projeto é composta das seguintes partes principais:

1. **Leitura e Pré-processamento dos Dados**
   
2. **Verificação de Normalidade e Transformação**
   - Verifica a normalidade dos dados para aplicar normalização ou padronização conforme necessário.

3. **Algoritmo de Machine Learning Local**
   - Utiliza algoritmos de machine learning locais para prever as vendas com base em dados históricos e fatores climáticos.

4. **Desnormalização**
   - Converte os resultados de volta aos valores originais para facilitar a interpretação das previsões.

5. **IA Generativa (Nova Integração)**
   - Incorpora a integração com o modelo generativo Gemini AI para gerar insights adicionais a partir da previsão de vendas. Essa etapa utiliza o prompt personalizado para gerar respostas com base em dados históricos e prever tendências e recomendações.

6. **Previsão Final**
   - Gera o resultado final da previsão de vendas, considerando também os insights fornecidos pela IA Generativa.

### Diagrama da Arquitetura Atualizada

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
+------------------------+
|   IA Generativa       |
| (Geração de Insights) |
+------------------------+
         |
         v
+---------------------+
|   Previsão Final    |
+---------------------+
