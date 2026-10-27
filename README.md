# IBM HR Analytics | Análise de desligamento

Investigação exploratória de associações entre características do trabalho e desligamento em uma **base ficcional**. O projeto demonstra limpeza, escolha de denominadores, comparação de grupos, testes estatísticos e tamanhos de efeito. As conclusões se referem somente a estes dados.

## Resultados principais

São 1.470 registros, dos quais 237 (`16,12%`) têm `Attrition = Yes`.

| Comparação | Evidência descritiva | Teste / tamanho do efeito |
|---|---|---|
| Horas extras | 30,53% de desligamento com horas extras; 10,44% sem | Qui-quadrado; V de Cramér = 0,244 |
| Satisfação no trabalho | 22,84% no nível 1; 11,33% no nível 4 | Qui-quadrado; V = 0,109 |
| Satisfação com o ambiente | 25,35% no nível 1; 13,45% no nível 4 | Qui-quadrado; V = 0,124 |
| Tempo de empresa | Mediana de 3 anos entre desligados; 6 entre os demais | Mann–Whitney; RBC absoluto = 0,298 |
| Renda mensal | Mediana de 3.202 entre desligados; 5.204 entre os demais | Mann–Whitney; RBC absoluto = 0,311 |

Os cinco testes apresentaram p < 0,001 na amostra. Eles foram escolhidos depois de examinar os mesmos dados e **não** foram ajustados por múltiplas comparações ou por fatores como cargo e idade. Associação não indica causa.

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

Abra [`IBM_HR_Analytics.ipynb`](IBM_HR_Analytics.ipynb) a partir da raiz do repositório e execute todas as células. O arquivo é carregado localmente, sem depender de um endereço antigo do GitHub.

As faixas de tempo de empresa e de última promoção incluem os valores zero. Antes, os 44 registros com zero anos de empresa ficavam fora de algumas tabelas agrupadas; as proporções foram corrigidas. Os testes de Mann–Whitney sempre usam a variável original, sem agrupamento.

## Limites e próximo passo

Esta base não descreve empregados reais. As comparações são bivariadas e podem refletir outros fatores; por isso não servem para estimar o efeito de uma política de RH ou orientar decisões individuais. Um estudo aplicável a uma organização exigiria dados reais coletados com governança adequada, hipóteses definidas previamente, análise multivariada, avaliação de viés e revisão por pessoas da área.

**Autor:** Lucas Guimarães · Engenharia da Computação, FIAP
