# 🧠 Projeto de Previsão de Risco de AVC

Este repositório contém um projeto "End-to-End" de Ciência de Dados focado na área da saúde. O objetivo foi substituir um sistema de pontuação manual impreciso por um modelo de Machine Learning robusto capaz de prever a probabilidade de um paciente sofrer um AVC (Acidente Vascular Cerebral).

🔗 **[Acesse o Dashboard Online Aqui](https://marcellusrp7.github.io/risco-avc-dashboard/)**

## 📋 Sobre o Projeto

Neste projeto, atuei como Analista de Dados para ajudar uma organização de saúde a melhorar a precisão dos seus diagnósticos preventivos. Trabalhando com um conjunto de dados do mundo real, utilizei a linguagem **R** para limpar, processar e modelar os dados, finalizando com o deploy de uma solução web.

### O Problema Identificado
Sistemas legados utilizavam uma "fórmula de padaria" (soma simples de pontos) para calcular riscos. Isso gerava falsos alarmes, como classificar um paciente saudável de 46 anos com **18,8% (Risco Moderado)** apenas devido à sua idade.

### A Solução
Desenvolvi um modelo de **Regressão Logística** que analisa o contexto clínico completo (Glicose, IMC, Histórico de Doenças, Fumo), corrigindo a estimativa desse mesmo paciente para **1,44% (Risco Baixo)**, um valor muito mais condizente com a realidade médica.

## ⚙️ Etapas do Desenvolvimento

1.  **Coleta e Limpeza de Dados (R):**
    * Tratamento de valores nulos na coluna `BMI` (convertendo de texto para numérico).
    * Remoção de outliers e dados inconsistentes (gênero "Other").
    * Conversão de variáveis categóricas para fatores.

2.  **Modelagem Preditiva:**
    * Algoritmo: **Regressão Logística (Logistic Regression)**.
    * Divisão de dados: 70% Treino / 30% Teste.
    * Feature Selection: Identificação das variáveis mais impactantes (Idade, Hipertensão, Glicose).

3.  **Avaliação de Performance:**
    * **Acurácia:** 95.72% no conjunto de teste.
    * Análise da Matriz de Confusão para entender sensibilidade e especificidade.

4.  **Deploy (Implementação):**
    * Tradução dos coeficientes estatísticos (Log-Odds) do modelo R para **JavaScript**.
    * Atualização do Front-End (HTML/CSS) para realizar o cálculo em tempo real no navegador do usuário.

## 🛠️ Tecnologias Utilizadas

* **Linguagem de Análise:** R (RStudio)
* **Pacotes:** `tidyverse`, `caTools`
* **Web/Deploy:** HTML5, CSS3, JavaScript
* **Hospedagem:** GitHub Pages

## 📊 Resultados Chave

| Perfil de Teste (46 anos, Saudável) | Risco Calculado | Classificação |
| :--- | :--- | :--- |
| **Método Antigo (Manual)** | 18.80% | ⚠️ Risco Moderado |
| **Novo Modelo (Machine Learning)** | **1.44%** | ✅ Risco Baixo (Normal) |

---

### 👤 Autor

**Marcellus**
* [LinkedIn](https://www.linkedin.com/in/marcellusrp/)
* [Portfólio GitHub](https://github.com/marcellusrp7)

---
*Aviso Legal: Esta ferramenta é um projeto de demonstração de análise de dados e não substitui o diagnóstico profissional de um médico.*
