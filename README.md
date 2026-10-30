# IBM HR Analytics | Análise de desligamento

Analisei os 1.470 registros **ficcionais** do IBM HR Analytics para comparar taxas de desligamento entre grupos. O [notebook](IBM_HR_Analytics.ipynb) passa pela conferência da base, pelas taxas e testes estatísticos e termina com uma regressão logística ajustada.

## Resultados principais

São 1.470 registros, dos quais 237 (`16,12%`) têm `Attrition = Yes`.

| Comparação | Evidência descritiva | Teste / tamanho do efeito |
|---|---|---|
| Horas extras | 30,53% de desligamento com horas extras; 10,44% sem | Qui-quadrado; V de Cramér = 0,244 |
| Satisfação no trabalho | 22,84% no nível 1; 11,33% no nível 4 | Qui-quadrado; V = 0,109 |
| Satisfação com o ambiente | 25,35% no nível 1; 13,45% no nível 4 | Qui-quadrado; V = 0,124 |
| Tempo de empresa | Mediana de 3 anos entre desligados; 6 entre os demais | Mann–Whitney; RBC absoluto = 0,298 |
| Renda mensal | Mediana de 3.202 entre desligados; 5.204 entre os demais | Mann–Whitney; RBC absoluto = 0,311 |

Os gráficos mostram o tamanho dos grupos e intervalos de Wilson de 95% para cada taxa. Nos cinco testes, o valor-p ajustado por Holm ficou abaixo de 0,001. Escolhi essas comparações depois de explorar a base; os testes acima analisam uma variável de cada vez, sem controlar cargo ou idade.

Para horas extras, a razão entre as taxas observadas é **2,93** (intervalo de 95% aproximado: **2,33 a 3,68**). Essa conta compara grupos da base e não prevê o desligamento de uma pessoa.

## Horas extras no modelo ajustado

A regressão logística considera **idade, tempo de empresa, cargo e satisfação com trabalho e ambiente**. A razão de **chances** associada a horas extras ficou em **5,31** (IC de 95%: **3,83 a 7,36**). Essa medida ajustada não é a mesma coisa que a razão entre taxas de 2,93 calculada acima.

O modelo ajusta apenas as variáveis incluídas. Mesmo com a associação observada, estes dados ficcionais não mostram que horas extras **causem** desligamento.

## Fonte e execução

Fonte: [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset). A descrição da fonte identifica os dados como **ficcionais**, criados para análise e ensino. Uma cópia do CSV está no repositório para reprodução do notebook.

```bash
git clone https://github.com/guimalucas/ibm-hr-analytics-attrition.git
cd ibm-hr-analytics-attrition
python -m venv .venv
# Ative o ambiente virtual no seu sistema
pip install -r requirements.txt
jupyter notebook
```

Abra [`IBM_HR_Analytics.ipynb`](IBM_HR_Analytics.ipynb) a partir da raiz do repositório e execute as células na ordem. O CSV é lido localmente.

As faixas de tempo de empresa incluem os **44 registros com zero anos**. Os testes de Mann–Whitney usam os valores originais de tempo e renda, sem agrupamento.

**Autor:** Lucas Guimarães · Engenharia da Computação, FIAP
