# IA - Laboratório 2: Fontes de Dados

Repositório dedicado ao Laboratório 2 da disciplina de Inteligência Artificial (IA), do curso de ADS da FATEC.

## Propósito

Este laboratório demonstra o uso de diferentes fontes de dados em Python. O trabalho principal está no notebook `lab/main.ipynb`, que carrega e explora dados a partir de três origens:

- arquivo CSV local, usando a base `CarPrice_Assignment.csv`;
- API pública, usando dados de inflação do Banco Central do Brasil;
- web scraping, usando `requests` e `BeautifulSoup` em uma página arquivada da National Gallery of Art.

## Estrutura do projeto

```text
.
+-- docs/
|   +-- IA-UA02-Lab2-Fontes de Dados.docx
|   +-- IA-UA02-Lab2-Fontes de Dados.pdf
+-- lab/
|   +-- data/
|   |   +-- CarPrice_Assignment.csv
|   +-- .python-version
|   +-- DEPENDENCIES.md
|   +-- main.ipynb
|   +-- main.py
|   +-- pyproject.toml
|   +-- uv.lock
+-- README.md
```

## Tecnologias e bibliotecas

- Python 3.12 ou superior
- uv
- Jupyter Notebook/JupyterLab
- pandas
- requests
- beautifulsoup4
- numpy
- matplotlib
- seaborn

As dependências do ambiente ficam registradas em `lab/pyproject.toml` e `lab/uv.lock`.

## Como executar

Clone o repositório e entre na pasta do projeto:

```bash
git clone <url-do-repositorio>
cd ia-lab2-fontes-de-dados
```

Entre na pasta do laboratório:

```bash
cd lab
```

Instale as dependências:

```bash
uv sync
```

Esse comando cria o ambiente virtual local em `lab/.venv/` e instala as versões registradas no `uv.lock`.

## Execução do notebook

Para abrir o projeto no Jupyter Notebook:

```bash
uv run jupyter notebook
```

Ou, se preferir o JupyterLab:

```bash
uv run jupyter lab
```

Depois, abra o arquivo `main.ipynb` e execute as células em ordem.

Também é possível abrir `lab/main.ipynb` diretamente no VS Code e selecionar o kernel do ambiente `.venv` criado pelo `uv sync`.

## Fontes de dados usadas

### 1. CSV local

Arquivo: `lab/data/CarPrice_Assignment.csv`

O notebook lê a base com `pandas` e exibe a quantidade de linhas e colunas do conjunto de dados.

### 2. API do Banco Central do Brasil

Endpoint usado:

```text
https://api.bcb.gov.br/dados/serie/bcdata.sgs.433/dados?formato=json
```

A API retorna dados da série SGS 433 em formato JSON.

### 3. Web scraping

Página usada:

```text
https://web.archive.org/web/20121007172955/https://www.nga.gov/collection/anZ1.htm
```

O notebook usa `requests` para baixar a página e `BeautifulSoup` para extrair nomes de artistas da estrutura HTML.

## Execução pelo terminal

O arquivo `lab/main.py` contém apenas uma validação simples do ambiente:

```bash
uv run python main.py
```

A análise de fontes de dados está concentrada no notebook `lab/main.ipynb`.

## Observações

- Execute os comandos do projeto a partir da pasta `lab/`.
- O ambiente virtual `.venv/` não deve ser versionado.
- O arquivo `uv.lock` deve permanecer no repositório para garantir reprodutibilidade.
- A parte de API e web scraping depende de conexão com a internet.
