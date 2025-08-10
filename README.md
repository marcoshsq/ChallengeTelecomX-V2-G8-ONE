<p align="center">
  <a href="https://github.com/marcoshsq/TelecomX-Churn-Analysis-ONE">
    <img src="https://github.com/marcoshsq/ChallengeTelecomX-V1-G8-ONE/blob/main/Challenge_Badge.png" alt="Challenge_Badge" height="150">
  </a>
</p>

<h2 align="center">Desafio - Previsão de Evasão de Clientes (Churn) da Telecom X 📉🤖</h2>

---

### Sobre o Projeto

Este projeto foi desenvolvido como parte da formação **"Data Science com Python"**, oferecida pelo programa **Oracle Next Education (ONE)**, em parceria com a **Alura**.

É a **Parte 2** do desafio Telecom X, onde assumimos o papel de **Analista de Machine Learning Júnior** para criar modelos preditivos capazes de **prever a evasão de clientes** a partir de dados demográficos, contratuais e de uso dos serviços.

O foco está em **pré-processamento de dados para Machine Learning, modelagem supervisionada, avaliação de desempenho e interpretação dos resultados**.

---

### Objetivo Geral 🚀

Construir e avaliar modelos de machine learning capazes de prever, com base em variáveis relevantes, quais clientes possuem maior risco de churn, fornecendo **insights acionáveis** para apoiar estratégias de retenção da Telecom X.

---

### Preparação dos Dados 🔄

- **Classificação das variáveis:**
  - Numéricas: `tenure`, `charges_total`, `charges_monthly`, `daily_charges`, etc.
  - Categóricas: `contract`, `internet_service`, `payment_method`, `tech_support`, etc.
- **Limpeza:** remoção de identificadores únicos (`customer_id`) e registros com `Churn` nulo.
- **Codificação:** `One-Hot Encoding` para variáveis categóricas.
- **Normalização:** `StandardScaler` aplicado somente em modelos sensíveis à escala (Logistic Regression).
- **Balanceamento:** uso do **SMOTE** para gerar exemplos sintéticos da classe minoritária (`Churn = 1`).
- **Divisão de dados:** 70% treino / 30% teste, estratificando pelo target.

---

### Modelos Criados 🤖

1. **Logistic Regression** (com padronização e SMOTE)
   - Interpretável, bom baseline, ótimo recall para detectar churners.
2. **Random Forest Classifier** (sem padronização, com `class_weight='balanced'`)
   - Captura relações não lineares e interações entre variáveis.

---

### Avaliação dos Modelos 📊

| Modelo               | Acurácia (Teste) | Precisão | Recall | F1-score |
|----------------------|------------------|----------|--------|----------|
| Logistic Regression  | 0.748            | 0.516    | 0.790  | 0.624    |
| Random Forest        | 0.783            | 0.616    | 0.483  | 0.542    |

- **Logistic Regression** → Melhor recall, identifica mais clientes em risco.
- **Random Forest** → Maior acurácia geral, mas recall mais baixo, com sinais de overfitting.

---

### Principais Fatores de Evasão 🔍

- **Menor tempo de contrato (`tenure`)**
- **Gasto total baixo (`charges_total`)**
- **Contrato mensal (`contract_month-to-month`)**
- **Pagamento via electronic check**
- **Serviço de internet por fibra óptica**
- **Ausência de serviços adicionais como suporte técnico e segurança online**

---

### Estratégias de Retenção 📌

1. **Incentivar contratos de longo prazo** com descontos ou benefícios.
2. **Ofertas de engajamento para novos clientes** nos primeiros 12 meses.
3. **Monitorar clientes de alto gasto mensal** e revisar percepção de valor.
4. **Investigar insatisfação entre usuários de fibra óptica**.
5. **Promover serviços adicionais** (segurança, suporte) para aumentar fidelidade.
6. **Analisar e revisar a experiência de clientes com pagamento via electronic check**.

---

### Como Executar 🚧

1. Clone este repositório ou abra o notebook no Google Colab.
2. Instale as bibliotecas necessárias:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```
3. Carregue dataframe.csv e execute o notebook em ordem.

---

###🎓 Sobre o Programa Oracle Next Education (ONE)

O Oracle Next Education (ONE), em parceria com a Alura, capacita talentos em tecnologia com foco em empregabilidade e transformação social.
O programa inclui formações em Python, análise de dados, SQL, modelagem e storytelling com dados, Git/GitHub e soft skills.

🔗 Saiba mais: [Oracle Next Education](https://www.oracle.com/br/education/oracle-next-education/)

