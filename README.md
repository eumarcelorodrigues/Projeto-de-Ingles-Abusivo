# 🇧🇷 Classificação de Linguagem Ofensiva (Análise Exploratória Inicial)

Este projeto consiste na fase inicial de Análise Exploratória de Dados (EDA) para um problema de classificação binária, visando distinguir textos como **ofensivos** ou **não ofensivos**.

O objetivo desta etapa é carregar o dataset, inspecionar sua estrutura e analisar a distribuição das classes de destino, fundamental para o desenvolvimento de modelos de Machine Learning (ML).

## 🚀 Tecnologias Utilizadas

* **Python**
* **Pandas:** Manipulação e análise de dados.
* **Matplotlib e Seaborn:** Visualização de dados.

## 💾 Conjunto de Dados

O dataset utilizado (`train.csv`) é carregado diretamente de um repositório externo e possui a seguinte estrutura de colunas:

| Coluna | Descrição |
| :--- | :--- |
| `text` | A frase ou texto de entrada a ser classificado. |
| `label` | O rótulo de destino: `offensive` (ofensiva) ou `not offensive` (não ofensiva). |

## 📊 Análise Exploratória (EDA)

As principais etapas executadas no notebook (`Projeto_eingles.ipynb`) foram:

1.  **Carregamento de Dados:** Leitura do `train.csv` através da URL bruta do GitHub.
2.  **Inspeção Inicial:** Verificação das primeiras linhas (`.head()`) e da estrutura de dados (`.info()`) para garantir a qualidade e ausência de valores nulos.
3.  **Visualização da Distribuição de Classes:**
    * Criação de um gráfico de barras utilizando **Seaborn** e **Matplotlib**.
    * Este gráfico demonstra a contagem de frases ofensivas versus não ofensivas, identificando visualmente o grau de equilíbrio ou desequilíbrio do dataset.

### Código de Visualização
```python
import matplotlib.pyplot as plt
import seaborn as sns

label_counts = df['label'].value_counts()
sns.set_palette("colorblind")

plt.figure(figsize=(6,4))
sns.barplot(x=label_counts.index, y=label_counts.values)
plt.title('Contagem de Frases Ofensivas vs Não Ofensivas')
plt.show()
