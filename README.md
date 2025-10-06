# 📊 Projetos de Coleta de Dados SENAI – Sistema de Transparência

Este repositório contém **três scripts Python** que coletam e consolidam dados públicos do **Sistema de Transparência da Gratuidade do SENAI** via API.

---

## 🚀 Scripts incluídos

### 1. `Gratuidade`

Baixa e organiza os dados de **vagas de gratuidade** por departamento regional do SENAI, detalhando programas e produtos.

### 2. `Gratuidade Indicadores`

Coleta os **indicadores de desempenho da gratuidade**, como metas, realizações e índices de cumprimento por estado.

### 3. `SENAI - Resultado da Gratuidade Regimental`

Obtém o **cumprimento do acordo de gratuidade regimental**, consolidando informações de todos os departamentos regionais.

---

## ⚙️ Instalação de dependências

Para executar os scripts, instale as bibliotecas necessárias:

```bash
pip install pandas requests tqdm openpyxl
```

### 🧠 Função de cada biblioteca

* **pandas** → organiza e manipula os dados retornados da API em formato de tabela (DataFrame).
* **requests** → realiza as requisições HTTP para coletar os dados das APIs públicas do Sistema de Transparência.
* **tqdm** → exibe uma barra de progresso enquanto os dados de todos os estados são baixados.
* **openpyxl** → permite salvar os resultados em arquivos **Excel (.xlsx)**.

---

## 💾 Saída

Cada script gera um arquivo `.xlsx` consolidado contendo os dados de todos os 27 departamentos regionais do SENAI.

Os arquivos são nomeados automaticamente conforme o tipo de dado e o ano, por exemplo:

```
gratuidade_senai_2024.xlsx
gratuidade_indicadores_senai_2024.xlsx
resultado_gratuidade_senai_2024.xlsx
```

---

## 📅 Tratamento de Datas

Os scripts convertem automaticamente os campos de data (como `dataAtualizacao` e `dataSensibilizacao`) para o formato legível **AAAA-MM-DD HH:MM:SS**, corrigindo valores numéricos (timestamp) retornados pela API.
