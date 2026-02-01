# Segmentacao_Clientes_Olist
"Clusterização de clientes e Análise RFM usando K-Means

# 🛍️ Segmentação de Clientes no E-commerce (Análise RFM)


## 📌 Visão Geral
Este projeto utiliza **Machine Learning (K-Means Clustering)** para agrupar clientes de um e-commerce brasileiro (Olist) com base em seu comportamento de compra. O objetivo é permitir campanhas de marketing personalizadas através da análise **RFM** (Recência, Frequência e Monetário).

## 💼 Problema de Negócio
Uma loja com milhares de clientes não pode tratar todos da mesma forma.
* Gastar verba de marketing com quem já compra sempre é desperdício.
* Ignorar clientes que gastam muito (VIPs) é perder oportunidade.
* Não tentar recuperar clientes inativos (Churn) é deixar dinheiro na mesa.

O desafio foi: **Como segmentar a base automaticamente para aplicar estratégias de CRM mais eficientes?**

## 📊 Metodologia
Utilizei o dataset público da **Olist** (Brazilian E-Commerce Public Dataset).
1.  **Tratamento de Dados:** Unificação de tabelas de Pedidos, Itens e Clientes.
2.  **Engenharia de Atributos (RFM):** Criação das métricas para cada cliente:
    * **R**ecência: Dias desde a última compra.
    * **F**requência: Quantidade de compras realizadas.
    * **M**onetário: Valor total gasto.
3.  **Pré-processamento:** Padronização dos dados com `StandardScaler` (essencial para o K-Means não enviesar pelos valores monetários altos).
4.  **Modelagem:**
    * Método do Cotovelo (Elbow Method) para definir o número ideal de clusters.
    * Aplicação do algoritmo **K-Means** com 4 grupos.

## 📈 Resultados e Insights

O algoritmo identificou 4 perfis distintos de consumidores:

| Segmento | Características | Ação Recomendada (CRM) |
| :--- | :--- | :--- |
| **VIP 💎** | Alto Ticket Médio e Boa Frequência. | Atendimento exclusivo, acesso antecipado a ofertas. |
| **Leais 🔄** | Compram com frequência (Fidelizados). | Programas de fidelidade/pontos para manter o hábito. |
| **Novos / Promissores 🌱** | Baixa Recência (compraram agora), mas só 1 vez. | Ofertas de *Cross-sell* para incentivar a 2ª compra rápido. |
| **Perdidos (Churn) 💤** | Alta Recência (não compram há muito tempo). | Ofertas agressivas de recuperação ou limpeza da base. |


## 🛠️ Tecnologias
* **Python** (Pandas, NumPy, Matplotlib, Seaborn)
* **Scikit-Learn** (K-Means, StandardScaler)

## 🚀 Como Executar
1. Clone o repositório.
2. Baixe o dataset da Olist no Kaggle.
3. Execute o notebook `Segmentacao_Clientes_Olist.ipynb`.

---
Desenvolvido por **Matheus Henrique Lopes de Mello**
