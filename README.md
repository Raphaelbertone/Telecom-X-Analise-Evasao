# 📊 Análise de Evasão de Clientes (Churn) da TelecomX

---

## 🧭 1. Introdução

O presente relatório tem como objetivo analisar os dados da empresa fictícia **TelecomX**, com foco na **evasão de clientes (Churn)**. A evasão representa a perda de clientes ao longo do tempo, sendo um dos principais desafios enfrentados por empresas de serviços contínuos, como telecomunicações. Identificar padrões e fatores associados ao cancelamento de serviços pode contribuir para a formulação de estratégias de retenção.

---

## 🧹 2. Limpeza e Tratamento de Dados

Foram realizados os seguintes passos de preparação e limpeza dos dados:

- 📥 Leitura do arquivo JSON diretamente de uma URL pública e criação de um DataFrame.
- 🧾 Normalização da estrutura dos dados para facilitar a análise.
- 🔄 Conversão de tipos de dados, incluindo:
  - `account_Charges_Total` para `float64`
- ✅ Padronização de valores categóricos, como “Yes/No” para 1 e 0.
- ⚠️ Substituição de campos em branco na coluna `Churn` por `'Nao_informado'`.
- 🔍 Verificação e tratamento de valores nulos e registros duplicados.
- ➕ Criação de novas colunas como `Contas_Diarias` para entender melhor o comportamento financeiro médio dos clientes.

---

## 📊 3. Análise Exploratória de Dados (EDA)

### 📉 Distribuição de Churn
- A maioria dos clientes **permaneceu na empresa**, porém há uma proporção significativa que cancelou o serviço (26%).

### 📌 Análise por Variáveis Categóricas

#### 3.1. Gênero (`customer_gender`)
- Não houve diferenças significativas de evasão entre os gêneros.

#### 3.2. Tipo de Contrato (`account_Contract`)
- Clientes com contratos **mensais** apresentaram **maior taxa de cancelamento (churn)**.
- Contratos com prazos maiores têm **índices mais baixos de cancelamento**, sugerindo maior fidelização.

#### 3.3. Método de Pagamento (`account_PaymentMethod`)
- Clientes que utilizam **pagamentos eletrônicos automáticos** tiveram maiores taxas de churn.

### 📈 Análise por Variáveis Numéricas

#### 3.4. Tempo de Permanência (`customer_tenure`)
- Clientes com **menor tempo de permanência** (< 10 meses) são os que mais cancelam.
  
#### 3.5. Total de Gastos (`account_Charges_Total`)
- Evasão de clientes (Churn) é mais comum entre clientes com **gastos mais baixos**, sugerindo menor engajamento com os serviços.

---

## ✅ 4. Conclusões e Insights

- **Contratos curtos** e **pagamentos automatizados** estão fortemente associados à evasão.
- Clientes com **menor tempo de relacionamento** com a empresa são mais propensos a cancelar o serviço.
- Estratégias de fidelização e acompanhamento **nos primeiros meses** são cruciais.
- **Educar clientes** sobre as vantagens de contratos de longo prazo pode ajudar a reduzir o churn.

---

## 💡 5. Recomendações

1. **Incentivar contratos anuais ou bianuais** com descontos ou vantagens adicionais.
2. Criar programas de **onboarding e suporte personalizado** para novos clientes (0 a 6 meses).
3. Monitorar de perto os usuários com **gastos baixos e contratos mensais**, aplicando campanhas de retenção direcionadas.
4. Avaliar a experiência de clientes com **pagamento eletrônico automático**, buscando pontos de frustração ou desengajamento.
5. Implementar uma **estratégia preditiva** de churn com base nos dados históricos para ação proativa.

---

