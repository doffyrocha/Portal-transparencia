# 📊 Coleta e Tratamento de Dados de Gratuidade – SESI / SENAI / FIRJAN

Este repositório reúne **scripts Python** para coleta, tratamento e organização de dados de gratuidade educacional disponibilizados nos portais de transparência do **SESI** e **SENAI (FIRJAN)**.

Os scripts permitem extrair dados de **vagas gratuitas, indicadores, horas-aluno e cumprimento de acordo regulatório/regimental**, organizando tudo em arquivos **.xlsx prontos para análise e dashboards (ex: Power BI)**.

---

## ✅ Funcionalidades

✔ Coleta de dados por **ano, unidade federativa (UF) e entidade (SESI/SENAI)**  
✔ Tratamento e reorganização das planilhas (padronização de colunas, criação de “Outros Programas”)  
✔ Geração automática de arquivos Excel (.xlsx)  
✔ Scripts específicos para **cumprimento da gratuidade regulatória/regimental**  
✔ Compatível com **Power BI, Excel, Tableau ou CSV para bancos de dados**

---

## 📂 Estrutura dos Scripts

| Nº | Script | Finalidade | Saída Gerada | Quando Utilizar |
|----|--------|-------------|---------------|------------------|
| 1 | `coletar_vagas.py` | Coleta de **vagas gratuitas, hora-aluno e programas** por ano e UF | `gratuidade_vagas_completa.xlsx` | Usar para visualizar vagas ofertadas, hora-aluno e programas gratuitos. |
| 2 | `coletar_indicadores.py` | Coleta de **indicadores de gratuidade** (realizado x previsto) | `gratuidade_indicadores.xlsx` | Usar para comparar metas e execução da gratuidade. |
| 3 | `reorganizar_vagas_outros.py` | Reestrutura o arquivo de vagas, criando a categoria **“Outros Programas”** | `gratuidade_vagas_reorganizada.xlsx` | Usar após rodar o script 1, para organizar horas-aluno “Outros”. |
| 4 | `coletar_regulamentar_senai.py` | Coleta do **cumprimento da gratuidade regulatória (SENAI)** | `gratuidade_regulamentar_senai_2021_2025.xlsx` | Usar para SENAI entre 2021 e 2025. |
| 5 | `coletar_regulamentar_sesi.py` | Coleta do **cumprimento da gratuidade regulatória (SESI)** | `gratuidade_regulamentar_sesi_2021_2025.xlsx` | Usar para SESI entre 2021 e 2025. |
| 6 | `coletar_regulamentar_sesi_repeat.py` | Versão duplicada / backup do script do SESI | — | Usar apenas para testes ou comparações. |

---

## ⚙️ Como Utilizar

### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
cd SEU_REPOSITORIO
