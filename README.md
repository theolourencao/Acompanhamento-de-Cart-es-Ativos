# Acompanhamento de Cartões Ativos

Este projeto tem como objetivo analisar e acompanhar o status de cartões ativos ao longo de diferentes trimestres. Utilizamos dados de transações e status dos cartões para gerar insights sobre o comportamento dos cartões ao longo do tempo.

## Estrutura do Projeto

- **app/ETL.ipynb**: Notebook principal que contém todo o processo de ETL (Extração, Transformação e Carga) dos dados.
- **data/Sources/**: Diretório contendo os arquivos CSV de origem dos dados.
- **data/Output/**: Diretório onde os arquivos de saída são salvos.

## Dependências

- Python 3.8+
- Pandas
- DuckDB

## Instalação

1. Clone o repositório:
    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd Acompanhamento-de-Cart-es-Ativos
    ```

2. Crie um ambiente virtual e ative-o:
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # No Windows, use: .venv\Scripts\activate
    ```

3. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

## Execução

1. Abra o notebook `app/ETL.ipynb` em um ambiente Jupyter:
    ```bash
    jupyter notebook app/ETL.ipynb
    ```

2. Execute todas as células do notebook para processar os dados e gerar os arquivos de saída.

## Estrutura do Notebook

- **Importando Libraries**: Importação das bibliotecas necessárias.
- **Criando Data Frames Iniciais**: Leitura dos arquivos CSV de origem.
- **Fazendo Ajustes de Colunas**: Ajustes nas colunas dos DataFrames.
- **Definindo Janelas de Tempo de cada trimestre**: Definição das janelas de tempo para análise trimestral.
- **Construindo a Lógica de Ativos no Início de Cada Quarter**: Lógica para identificar cartões ativos no início de cada trimestre.
- **Construindo a Lógica de Ativos no Final de Cada Quarter**: Lógica para identificar cartões ativos no final de cada trimestre.
- **Exportando outputs**: Exportação dos resultados para arquivos CSV.

## Arquivos de Saída

- **active_cards_status.csv**: Contém o status final dos cartões ativos por trimestre.
- **quarter_grouped_statuses.csv**: Contém o agrupamento dos status dos cartões por trimestre.
- **temp_blocked.csv**: Contém informações sobre cartões temporariamente bloqueados.
- **avg_days.csv**: Contém a média de dias em que os cartões ficaram em cada status.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.
