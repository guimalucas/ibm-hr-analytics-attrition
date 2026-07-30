# Análise Exploratória de Dados e Testes Estatísticos sobre Rotatividade de Funcionários

## Sobre o projeto

A rotatividade de funcionários (Attrition) representa um dos principais desafios enfrentados pelas organizações, impactando custos de recrutamento, treinamento, produtividade e retenção de conhecimento.

O objetivo deste projeto é identificar quais fatores apresentam associação estatisticamente significativa com o desligamento de funcionários por meio de uma Análise Exploratória de Dados (EDA) e da aplicação de testes estatísticos apropriados para diferentes tipos de variáveis.

Todo o processo foi desenvolvido utilizando Python e bibliotecas voltadas para análise de dados e estatística.

---

## Objetivos

- Realizar a limpeza e preparação dos dados;
- Explorar o comportamento das variáveis do conjunto de dados;
- Formular hipóteses sobre possíveis fatores relacionados ao Attrition;
- Validar as hipóteses utilizando testes estatísticos;
- Interpretar os resultados sob uma perspectiva de negócio;
- Apresentar recomendações baseadas nas evidências encontradas.

---

## Dataset

**Origem:** IBM HR Analytics Employee Attrition & Performance

O conjunto de dados contém informações relacionadas ao perfil profissional, características do trabalho e satisfação dos funcionários, permitindo investigar fatores associados à rotatividade.

A variável de interesse analisada neste projeto é:

- **Attrition** (desligamento do funcionário)

---

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Jupyter Notebook

---

## Etapas do projeto

O projeto foi desenvolvido seguindo as seguintes etapas:

1. Compreensão do problema de negócio;
2. Importação e inspeção inicial dos dados;
3. Limpeza e tratamento do dataset;
4. Análise exploratória dos dados (EDA);
5. Formulação de hipóteses;
6. Aplicação de testes estatísticos;
7. Interpretação dos resultados;
8. Conclusões e recomendações.

---

## Principais análises realizadas

Durante o desenvolvimento do projeto foram investigadas diversas características relacionadas ao desligamento dos funcionários, incluindo:

- Horas extras;
- Faixa salarial;
- Tempo de empresa;
- Satisfação no trabalho;
- Ambiente de trabalho;
- Cargo;
- Departamento;
- Estado civil;
- Distância entre residência e trabalho;
- Escolaridade;
- Idade;
- Entre outras variáveis relevantes.

---

## Testes estatísticos utilizados

De acordo com o tipo de variável analisada, foram aplicados diferentes testes estatísticos, incluindo:

- Teste Qui-Quadrado;
- Teste de Mann-Whitney;
- V de Cramér (tamanho de efeito);
- Correlação bisserial por postos.

A interpretação dos resultados considera não apenas a significância estatística (valor-p), mas também a magnitude das associações observadas.

---

## Principais conclusões

A análise permitiu identificar fatores com associação estatisticamente significativa com o desligamento dos funcionários, possibilitando compreender quais características apresentam maior relação com a rotatividade.

Além da identificação dessas associações, o projeto discute possíveis interpretações dos resultados e apresenta recomendações que podem auxiliar gestores na definição de estratégias voltadas à retenção de talentos.

---

## Estrutura do repositório

```
IBM_HR_ANALYTICS
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
└── IBM_HR_Analytics.ipynb
```

---

## Como executar

Clone o repositório:

```bash
git clone https://github.com/guimalucas/IBM_HR_ANALYTICS.git
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra o notebook no Jupyter Notebook ou no Google Colab e execute as células em sequência.

---

## Autor

Lucas Guimarães

Estudante de Engenharia da Computação – FIAP

GitHub: https://github.com/guimalucas
