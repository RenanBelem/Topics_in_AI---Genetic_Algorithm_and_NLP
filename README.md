Este repositório contém um projeto abrangendo a implementação de um **Algoritmo Genético** para o Problema do Caixeiro Viajante (TSP) e uma análise de **Modelagem Vetorial de Linguagem Natural (NLP)** comparando técnicas clássicas e de Deep Learning.
> Trabalho realizado para a disciplina: Tópicos em IA, no curso de Inteligência Artifical Aplicada da UFPR

---

## 🚀 Estrutura do Projeto

O projeto está dividido em duas partes principais:

### 1. Algoritmo Genético (TSP - Traveling Salesperson Problem)

O objetivo é encontrar a menor rota que passe por 100 cidades geradas aleatoriamente em um mapa 100x100, retornando ao ponto de origem.

**Características da Implementação:**

* **Geração de Cidades:** Coordenadas (x, y) únicas geradas aleatoriamente.
* **População Inicial:** Criada através de permutações aleatórias dos índices das cidades.
* **Função de Fitness:** Baseada na distância euclidiana total da rota.
* **Operadores Genéticos:**
* **Cruzamento (Crossover):** Técnica **OX (Ordered Crossover)**, que preserva a ordem relativa das cidades sem duplicatas.
* **Mutação:** Técnica **Swap Mutation**, trocando a posição de duas cidades na rota.


* **Parâmetros Utilizados:**
* Gerações: 1000.
* Tamanho da População: 100.
* Taxa de Cruzamento: 90%.
* Taxa de Mutação: 1%.



**Resultados obtidos:**

* Melhora significativa na distância total (redução de aproximadamente **69.71%** em relação à melhor solução inicial).
* Gráficos gerados de convergência da distância e visualização da rota final no mapa.

---

### 2. Modelagem Vetorial e NLP (Processamento de Linguagem Natural)

Uma comparação entre representações estatísticas e semânticas de texto, utilizando projeção 2D para análise de agrupamento.

**Modelos Comparados:**

1. **TF-IDF (Term Frequency-Inverse Document Frequency):** Modelo estatístico clássico que valoriza palavras raras e penaliza as muito frequentes no corpus.
2. **Sentence-BERT (S-BERT):** Utilização do modelo pré-treinado `paraphrase-multilingual-MiniLM-L12-v2` para extrair *embeddings* semânticos que capturam o contexto e significado das frases em múltiplos idiomas.

**Visualização:**

* Aplicação de **PCA (Principal Component Analysis)** para reduzir a dimensionalidade dos vetores para 2D.
* Geração de gráficos de dispersão para observar como os diferentes modelos agrupam sentenças similares.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

O projeto foi desenvolvido em Python, utilizando as seguintes bibliotecas:

* **NumPy:** Manipulação de matrizes e cálculos matemáticos.
* **Matplotlib / Seaborn:** Geração de gráficos e visualização de dados.
* **Scikit-learn:** Implementação de TF-IDF e PCA.
* **Sentence-Transformers (Hugging Face):** Implementação do modelo BERT.
* **Pandas:** Estruturação de dados para visualização.

---

## 📋 Como Executar

### Pré-requisitos

Certifique-se de ter o Python instalado (recomendado 3.10+). Instale as dependências necessárias:

```bash
pip install numpy matplotlib pandas seaborn scikit-learn sentence-transformers

```

### Execução

1. **Notebook:** Abra o arquivo `Trabalho_Final_IAA015.ipynb` no Google Colab ou Jupyter Notebook e execute as células sequencialmente.
2. **Script Python:** Execute o arquivo `trabalho_final_iaa015.py` diretamente no terminal:

```bash
python trabalho_final_iaa015.py

```

---

## 📊 Principais Conclusões

* O **Algoritmo Genético** demonstrou ser eficiente para o TSP, apresentando uma curva de aprendizado consistente ao longo das gerações.
* Na análise de **NLP**, o modelo **S-BERT** apresentou agrupamentos mais intuitivos e coerentes em comparação ao TF-IDF, uma vez que considera a semântica das frases e não apenas a frequência de termos isolados.

---
