# Análise de Fraudes em Transações Financeiras

Projeto de aprendizado desenvolvido com Python para analisar transações financeiras e identificar padrões relacionados a operações fraudulentas.
O projeto utiliza Pandas, NumPy, Matplotlib, Seaborn e Scikit-learn para exploração dos dados, visualização e criação de um modelo simples de Machine Learning.

## Sobre o projeto

O conjunto de dados contém transações realizadas com cartões de crédito, classificadas como:

- `0` — Transação legítima
- `1` — Transação fraudulenta

Durante a análise foi identificado um forte desbalanceamento entre as classes, com aproximadamente 99,83% das transações sendo legítimas e apenas 0,17% fraudulentas.
O projeto utiliza Regressão Logística para realizar a classificação das transações.

### Principais etapas

- [x] Carregamento dos dados
- [x] Exploração e limpeza
- [x] Análise das transações
- [x] Preparação dos dados
- [x] Treinamento do modelo
- [x] Avaliação dos resultados

##  Resultados

O modelo de Regressão Logística apresentou:

- **Acurácia:** 97,52%
- **Recall para fraudes:** 0,87
- **Precision para fraudes:** 0,06
- **F1-score para fraudes:** 0,11

Das 95 transações fraudulentas presentes no conjunto de teste, o modelo identificou corretamente 83.

Apesar do alto Recall, o modelo apresentou uma quantidade elevada de falsos positivos, demonstrando a importância de não utilizar apenas a acurácia para avaliar modelos em conjuntos de dados desbalanceados.

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## 📁 Estrutura do projeto

```text
fraud-transaction-analysis/
│
├── notebooks/
│   └── fraud_analysis.ipynb
│
├── src/
│   └── main.py
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Pré-requisitos

Antes de executar o projeto, é necessário possuir:

- Python instalado;
- Git instalado;
- pip para instalação das dependências.

## Instalando o projeto

Clone o repositório:

```bash
git clone https://github.com/kaiovctr/fraud-transaction-analysis.git
```

Entre na pasta do projeto:

```bash
cd fraud-transaction-analysis
```

Crie um ambiente virtual.

### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

## Executando o projeto

Com o ambiente virtual ativado, execute:

```bash
jupyter notebook
```

Depois, abra o arquivo:

```text
notebooks/fraud_analysis.ipynb
```

Também é possível abrir o projeto diretamente pelo VS Code e executar o notebook utilizando o ambiente virtual `.venv` como kernel.

## Fonte dos dados

Os dados são carregados diretamente de uma fonte externa em formato CSV:

```text
https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv
```

Por esse motivo, não é necessário baixar ou armazenar o conjunto de dados dentro do repositório.

## Licença

Este projeto está sob a licença definida no arquivo [LICENSE](LICENSE).
