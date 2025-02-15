## Acompanhamento de Cartões Ativos

Este projeto realiza um processo ETL (Extract, Transform, Load) em dados de transações de cartões. O notebook ETL.ipynb lê dados de arquivos CSV, processa-os para derivar insights significativos e exporta os resultados para novos arquivos CSV.

### Estrutura do Projeto

```
.gitignore
app/
	ETL.ipynb
data/
	Output/
		active_cards_status.csv
		quarter_grouped_statuses.csv
	Sources/
		cards_status.csv
		cards_transactions.csv
		cards.csv
poetry.lock
pyproject.toml
README.md
```

### Dependências

As dependências do projeto estão listadas no arquivo pyproject.toml:

```toml
[project]
name = "acompanhamento-de-cart-es-ativos"
version = "0.1.0"
description = ""
authors = [
    {name = "theo lourencao"}
]
readme = "README.md"
requires-python = ">=3.13"
dependencies = [
    "pandas (>=2.2.3,<3.0.0)"
]

[build-system]
requires = ["poetry-core>=2.0.0,<3.0.0"]
build-backend = "poetry.core.masonry.api"
```

### Executando o Notebook

1. Certifique-se de que todas as dependências estão instaladas. Você pode usar o Poetry para instalar as dependências:

    ```sh
    poetry install
    ```

2. Abra o notebook ETL.ipynb em um ambiente Jupyter Notebook ou JupyterLab.

3. Execute todas as células do notebook para processar os dados e gerar os arquivos de saída.

### Estrutura do Notebook

1. **Importando Libraries**: Importa as bibliotecas necessárias para manipulação de dados.
2. **Criando Data Frames Iniciais**: Lê os dados iniciais dos arquivos CSV.
3. **Fazendo Ajustes de Colunas**: Converte colunas de data para o formato datetime e adiciona novas colunas para datas de início e fim de trimestre.
4. **Definindo Janelas de Tempo de cada trimestre**: Define as datas de início e fim para cada trimestre.
5. **Construindo a Lógica de Ativos no Início de Cada Quarter**: Identifica os cartões ativos no início de cada trimestre e agrega os dados.
6. **Construindo a Lógica de Ativos no Final de Cada Quarter**: Identifica os cartões ativos no final de cada trimestre e agrega os dados.
7. **Consolidação**: Consolida os dados, aplicando lógica de negócios para determinar o status final de cada cartão.
8. **Exportando outputs**: Exporta os dados processados para arquivos CSV.

### Arquivos de Saída

Os resultados processados são exportados para os seguintes arquivos CSV:

- active_cards_status.csv
- quarter_grouped_statuses.csv

### Contribuição

Sinta-se à vontade para contribuir com este projeto. Para isso, faça um fork do repositório, crie uma branch para suas alterações e envie um pull request.

### Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

theolourencao: preencha essa documentação aqui

GitHub Copilot: ```markdown
# Acompanhamento de Cartões Ativos

Este projeto realiza um processo ETL (Extract, Transform, Load) em dados de transações de cartões. O notebook [`app/ETL.ipynb`](app/ETL.ipynb) lê dados de arquivos CSV, processa-os para derivar insights significativos e exporta os resultados para novos arquivos CSV.

## Estrutura do Projeto

```
.gitignore
app/
    ETL.ipynb
data/
    Output/
        active_cards_status.csv
        quarter_grouped_statuses.csv
    Sources/
        cards_status.csv
        cards_transactions.csv
        cards.csv
poetry.lock
pyproject.toml
README.md
```

## Dependências

As dependências do projeto estão listadas no arquivo [`pyproject.toml`](pyproject.toml):

```toml
[project]
name = "acompanhamento-de-cart-es-ativos"
version = "0.1.0"
description = ""
authors = [
    {name = "theo lourencao"}
]
readme = "README.md"
requires-python = ">=3.13"
dependencies = [
    "pandas (>=2.2.3,<3.0.0)"
]

[build-system]
requires = ["poetry-core>=2.0.0,<3.0.0"]
build-backend = "poetry.core.masonry.api"
```

## Executando o Notebook

1. Certifique-se de que todas as dependências estão instaladas. Você pode usar o Poetry para instalar as dependências:

    ```sh
    poetry install
    ```

2. Abra o notebook ETL.ipynb em um ambiente Jupyter Notebook ou JupyterLab.

3. Execute todas as células do notebook para processar os dados e gerar os arquivos de saída.

## Estrutura do Notebook

1. **Importando Libraries**: Importa as bibliotecas necessárias para manipulação de dados.
2. **Criando Data Frames Iniciais**: Lê os dados iniciais dos arquivos CSV.
3. **Fazendo Ajustes de Colunas**: Converte colunas de data para o formato datetime e adiciona novas colunas para datas de início e fim de trimestre.
4. **Definindo Janelas de Tempo de cada trimestre**: Define as datas de início e fim para cada trimestre.
5. **Construindo a Lógica de Ativos no Início de Cada Quarter**: Identifica os cartões ativos no início de cada trimestre e agrega os dados.
6. **Construindo a Lógica de Ativos no Final de Cada Quarter**: Identifica os cartões ativos no final de cada trimestre e agrega os dados.
7. **Consolidação**: Consolida os dados, aplicando lógica de negócios para determinar o status final de cada cartão.
8. **Exportando outputs**: Exporta os dados processados para arquivos CSV.

## Arquivos de Saída

Os resultados processados são exportados para os seguintes arquivos CSV:

- active_cards_status.csv
- quarter_grouped_statuses.csv

## Contribuição

Sinta-se à vontade para contribuir com este projeto. Para isso, faça um fork do repositório, crie uma branch para suas alterações e envie um pull request.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
```

theolourencao: escreva a documentação do ETL

GitHub Copilot: ```markdown
# Acompanhamento de Cartões Ativos

Este projeto tem como objetivo monitorar e acompanhar o uso de cartões ativos. Abaixo estão as seções principais desta documentação:

## Introdução

O acompanhamento de cartões ativos é essencial para garantir a segurança e eficiência no uso dos mesmos. Este projeto visa fornecer ferramentas e relatórios para monitorar o status e a atividade dos cartões.

## Estrutura do Projeto

```
.gitignore
app/
    ETL.ipynb
data/
    Output/
        active_cards_status.csv
        quarter_grouped_statuses.csv
    Sources/
        cards_status.csv
        cards_transactions.csv
        cards.csv
poetry.lock
pyproject.toml
README.md
```

## Instalação

Para instalar as dependências do projeto, execute o seguinte comando:

```sh
poetry install
```

## Uso

Para iniciar o projeto, utilize o comando:

```sh
poetry run jupyter notebook
```

Abra o notebook ETL.ipynb e execute todas as células para processar os dados e gerar os arquivos de saída.

## Estrutura do Notebook

1. **Importando Libraries**: Importa as bibliotecas necessárias para manipulação de dados.
2. **Criando Data Frames Iniciais**: Lê os dados iniciais dos arquivos CSV.
3. **Fazendo Ajustes de Colunas**: Converte colunas de data para o formato datetime e adiciona novas colunas para datas de início e fim de trimestre.
4. **Definindo Janelas de Tempo de cada trimestre**: Define as datas de início e fim para cada trimestre.
5. **Construindo a Lógica de Ativos no Início de Cada Quarter**: Identifica os cartões ativos no início de cada trimestre e agrega os dados.
6. **Construindo a Lógica de Ativos no Final de Cada Quarter**: Identifica os cartões ativos no final de cada trimestre e agrega os dados.
7. **Consolidação**: Consolida os dados, aplicando lógica de negócios para determinar o status final de cada cartão.
8. **Exportando outputs**: Exporta os dados processados para arquivos CSV.

## Arquivos de Saída

Os resultados processados são exportados para os seguintes arquivos CSV:

- active_cards_status.csv
- quarter_grouped_statuses.csv

## Contribuição

Contribuições são bem-vindas! Por favor, siga as diretrizes de contribuição e abra um pull request.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.

## Contato

Para mais informações, entre em contato com [seu-email@exemplo.com](mailto:seu-email@exemplo.com).
```