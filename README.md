## Descrição rápida

Os scripts percorrem os **27 departamentos regionais (SENAI-XX)**, consultam os endpoints públicos da API e geram arquivos Excel separados ou consolidados com os dados.

## Scripts

* **SENAI - Resultado da Gratuidade Regimental**

  * Endpoint: `/publico/gratuidade/dr/senai/cumprimento-acordo`
  * Saída: `resultado_gratuidade_senai_{ANO}.xlsx`

* **Gratuidade**

  * Endpoint: `/publico/gratuidades/vagas/entidades/{sigla}/departamentos/{dep}/gratuidade`
  * Saída: `gratuidade_senai_{ANO}.xlsx`
  * Observação: flatten de `programas` → `produtos` quando existirem.

* **Gratuidade Indicadores**

  * Endpoint: `/publico/gratuidades/indicadores/entidades/{sigla}/departamentos/{dep}/gratuidade`
  * Saída: `gratuidade_indicadores_senai_{ANO}.xlsx`

## Dependências

```bash
pip install pandas requests tqdm openpyxl
```

## Como executar

```bash
python "SENAI - Resultado da Gratuidade Regimental.py"  # ou nome do arquivo .py correspondente
python "Gratuidade.py"
python "Gratuidade Indicadores.py"
```

Os arquivos `.xlsx` serão salvos no mesmo diretório do script.

## Observações

* Campos ausentes para um estado são ignorados — o script segue em frente.
* Datas que não forem timestamps válidos ficam como vazias (coerced).

---

Autor: Márcio Douglas Rocha
