# Regressão Linear para Séries Temporais: Planejamento de Dispêndios de Alimentação da Marinha do Brasil

## Visão Geral do Projeto

Este projeto de Machine Learning aborda um desafio crucial para a gestão pública: a previsão de dispêndios com alimentação para militares e servidores da Marinha do Brasil. Utilizando técnicas avançadas de análise de séries temporais, o objetivo é otimizar a alocação de recursos orçamentários, reduzir desperdícios e aprimorar a eficiência logística. Em um cenário onde a compra de gêneros alimentícios representa uma despesa recorrente e significativa, a capacidade de prever custos futuros com maior precisão é fundamental para a transparência e a responsabilidade fiscal. Este trabalho explora a aplicação de modelos preditivos para transformar a gestão de suprimentos em uma das instituições mais estratégicas do país.

## Definição do Problema

O problema central deste estudo é a previsão dos gastos mensais com alimentação para organizações militares da Marinha do Brasil. A gestão de municiamento, que engloba o planejamento, aquisição, controle de estoque e prestação de contas de gêneros alimentícios, é um processo complexo e vital. A previsão acurada desses dispêndios é essencial para:

*   **Otimização Orçamentária:** Alocar recursos financeiros de forma inteligente, evitando gastos desnecessários e garantindo a disponibilidade de fundos.
*   **Redução de Desperdícios:** Minimizar perdas por validade ou má conservação através de uma gestão de estoques mais eficiente.
*   **Transparência e Responsabilidade Fiscal:** Assegurar que os recursos públicos sejam utilizados de forma eficiente, econômica e legal.

O trabalho propõe tratar este desafio como um problema de previsão de série temporal, onde os gastos mensais são influenciados por fatores como o efetivo atendido, o custo de aquisição dos insumos e a composição do cardápio. A análise considera dados históricos de consumo, aplicando técnicas que capturam tendências, sazonalidades e anomalias para gerar insights que subsidiem políticas de abastecimento e aquisição.

## Dados e Preparação

O projeto utiliza dados históricos de mapas mensais de municiamento (MMM), informações sobre as Organizações Militares (OM) e dados de centralização de municiamento. Uma etapa robusta de preparação de dados foi realizada, incluindo:

*   **Consolidação de Dados:** Combinação de múltiplos arquivos de movimentação mensal e etapas em DataFrames unificados.
*   **Limpeza e Filtragem:** Identificação e remoção de organizações com dados incompletos e filtragem de dados recentes não consolidados para garantir a integridade da série temporal.
*   **Seleção de Atributos:** Exclusão de colunas irrelevantes ou com alta cardinalidade para focar nos atributos mais significativos para a modelagem.
*   **Tratamento de Valores Ausentes:** Preenchimento manual de dados faltantes em informações cruciais das OM.

## Abordagem de Modelagem

O projeto adota uma abordagem abrangente para a modelagem de séries temporais, explorando uma variedade de algoritmos para identificar o mais adequado à previsão dos dispêndios. As bibliotecas importadas indicam a intenção de avaliar:

*   **Modelos Clássicos:** SARIMA (Sazonal AutoRegressive Integrated Moving Average) e Suavização Exponencial de Holt-Winters, que são referências para séries temporais.
*   **Modelos Modernos:** Prophet (desenvolvido pelo Facebook, robusto para dados com fortes efeitos sazonais e feriados) e XGBoost (um algoritmo de boosting baseado em árvores de decisão, eficaz para dados tabulares e capaz de lidar com variáveis exógenas).
*   **Redes Neurais:** LSTM (Long Short-Term Memory), uma arquitetura de rede neural recorrente ideal para sequências de dados, e NBEATS (Neural Basis Expansion Analysis for Interpretable Time Series Forecasting), um modelo de deep learning de última geração para previsão.
*   **AutoML:** AutoGluon, uma ferramenta que automatiza a seleção e o ajuste de modelos, buscando a melhor performance de forma eficiente.

Cada modelo será treinado e otimizado, visando garantir a robustez e a capacidade de generalização das previsões.

Este projeto tem o potencial de se tornar uma ferramenta valiosa para a gestão estratégica de recursos na Marinha do Brasil, contribuindo para a eficiência operacional e a responsabilidade fiscal.

## Como Executar o Projeto

Para replicar e executar este projeto, siga os passos abaixo:

1.  **Clone o Repositório:**
    ```bash
    git clone https://github.com/ffserro/MVP.git
    cd MVP
    ```

2.  **Instale as Dependências:**
    O projeto utiliza um arquivo `requirements.txt` para gerenciar as dependências. Certifique-se de ter o `pip` instalado e execute:
    ```bash
    pip install -r requirements.txt
    ```
    
3.  **Execute o Notebook:**
    Abra o arquivo `mvp.ipynb` em um ambiente Jupyter (Jupyter Notebook, JupyterLab ou Google Colab). O notebook está configurado para ser executado no Google Colab, o que simplifica a configuração do ambiente.
    *   **Google Colab:** Clique no badge "Abra no Colab" no início do notebook ou acesse diretamente o link: [https://colab.research.google.com/github/ffserro/MVP/blob/master/mvp.ipynb](https://colab.research.google.com/github/ffserro/MVP/blob/master/mvp.ipynb)
    *   **Localmente:** Certifique-se de ter o Jupyter instalado (`pip install jupyter`) e execute `jupyter notebook` ou `jupyter lab` no diretório do projeto, abrindo em seguida o arquivo `mvp.ipynb`.

4.  **Siga as Instruções:**
    Execute as células do notebook sequencialmente, observando as explicações e os resultados em cada etapa. As seções de preparação de dados e modelagem fornecerão os passos para a análise e previsão dos modelos.

## Contribuições

Contribuições são bem-vindas! Se você tiver sugestões de melhoria, identificou um bug ou gostaria de adicionar novas funcionalidades, sinta-se à vontade para abrir uma *issue* ou enviar um *pull request* no repositório do GitHub.
