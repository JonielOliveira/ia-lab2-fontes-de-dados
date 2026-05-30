# Dependências do Projeto

As dependências instaladas são registradas automaticamente nos arquivos:

```text
pyproject.toml
uv.lock
```

Para recriar o ambiente em outra máquina:

```bash
uv sync
```

## Jupyter e Notebooks

Utilizadas para execução de notebooks e integração com o VS Code.

```bash
uv add ipykernel
uv add notebook
uv add jupyterlab
```

---

## Análise e Visualização de Dados

Utilizadas para manipulação, processamento e visualização de dados.

```bash
uv add pandas
uv add numpy
uv add matplotlib
uv add seaborn
```

---

## Bibliotecas específicas necessárias para esse projeto

Utilizadas para o funcionamento adequado do projeto, conforme código apresentado.

```bash
uv add pandas
uv add requests
uv add beautifulsoup4
```
