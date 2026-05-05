# 📊 Análise Exploratória de Dados (EDA) — NPS em E-commerce

**Integrantes**: Alfeson Luiz Araujo de Macedo; Fabio Luis Amaro de Lima Silva Santana; Letícia Alves de Sena

## Objetivo

O seguinte projeto tem como objetivo analisar os principais fatores que impactam a satisfação dos clientes em um e-commerce, utilizando métricas de NPS (Net Promoter Score). A análise busca identificar os fatores mais críticos para a experiência do cliente e entender o que torna um cliente em um detrator.

Com a análise exploratória, o projeto busca gerar insights estratégicos que possam auxiliar áreas do negócio na tomada de decisão e na priorização de melhorias operacionais e, consequentemente, melhorar a jornada do cliente.

---

## Descrição da base de dados

### Campos Originais:

- `customer_id`: Identificador do cliente  
- `customer_age`: Idade do cliente  
- `customer_region`: Região geográfica  
- `customer_tenure_months`: Tempo de relacionamento com a empresa  
- `order_id`: Identificador do pedido  
- `order_value`: Valor total da compra  
- `items_quantity`: Quantidade de itens  
- `discount_value`: Valor de desconto aplicado  
- `payment_installments`: Número de parcelas  
- `freight_value`: Valor do frete  
- `delivery_time_days`: Tempo total de entrega  
- `delivery_delay_days`: Dias de atraso  
- `delivery_attempts`: Tentativas de entrega  
- `customer_service_contacts`: Contatos com suporte  
- `resolution_time_days`: Tempo de resolução de problemas  
- `complaints_count`: Número de reclamações  

### Métricas de satisfação

- `csat_internal_score`: Score interno de satisfação  
- `nps_score`: Nota NPS do cliente  
- `repeat_purchase_30d`: Indica recompra em até 30 dias  

### Campos criados para a análise:

- `categoria_nps`: para categorizar os clientes entre detratores, neutros e promotores  
- `categoria_desconto`: para categorizar os descontos e fretes entre baixo, médio e alto  
- `categoria_frete`: para categorizar os fretes entre baixo, médio e alto  

---

## Metodologia Utilizada

A análise foi conduzida utilizando Python com as bibliotecas Pandas, Matplotlib e Seaborn. Seguimos a seguinte segmentação:

### 1. Entendimento da base
- Leitura prévia dos dados  
- Validação de colunas  
- Verificação do tamanho da base  

### 2. Qualidade dos dados
- Verificação de tipos de dados  
- Identificação de valores nulos  
- Estatísticas descritivas  

### 3. Análise exploratória
- Criação de categorias de NPS (promotores e detratores)  
- Comparação entre categorias  
- Correlação entre variáveis  
- Análise de impacto do atraso, reclamações e suporte  
- Identificação de possíveis pontos de ruptura  
- Análise e comparação de perfis de clientes  

---

## Como Reproduzir os Resultados

### Requisitos

- Realizar o download da base analisada  
- Instalar as bibliotecas utilizadas: `pandas`, `numpy`, `seaborn` e `matplotlib`  

### Executar o notebook

- Abrir o notebook do projeto  
- Carregar a base de dados CSV  
- Executar as células em sequência  

---

## Principais Resultados

A análise demonstra que os principais fatores que impactam a satisfação do cliente estão relacionados à experiência operacional, especialmente ao atraso nas entregas. Entre todas as variáveis analisadas, o atraso apresentou o maior impacto negativo no NPS, além de desencadear um efeito cascata na jornada do cliente, aumentando o número de reclamações, os contatos com o suporte e o tempo de resolução dos problemas.

**Atraso na entrega > Contato com o Suporte > Tempo de resolução alto > NPS detrator**

Os clientes detratores tendem a enfrentar experiências com maiores atrasos, mais reclamações e maior necessidade de interação com o atendimento, enquanto os promotores, em sua grande maioria, apresentam pouco ou nenhum atraso e, consequentemente, uma jornada muito mais fluida. 

A análise também indica um possível ponto de ruptura na experiência do cliente: a partir de aproximadamente três dias de atraso, observa-se uma maior variação na queda do NPS, o que pode sugerir um limite de tolerância para atrasos na entrega.

Por outro lado, variáveis como idade, região, valor do frete e descontos não apresentaram impacto significativo na satisfação. De forma geral, os resultados indicam que melhorias na eficiência logística e na resolução de problemas possuem o maior potencial de impacto positivo na experiência do cliente e no aumento do NPS.

---

## Fatores críticos para a satisfação

Os principais fatores identificados foram:

- Atraso na entrega (O atraso apresentou a maior correlação negativa com o NPS)  
- Número de reclamações  
- Contatos com suporte  
- Tempo de resolução  

---

## Resultados

Os resultados analisados por meio do EDA mostram que a satisfação do cliente está diretamente ligada à eficiência operacional. O atraso na entrega se destacou como o principal fator de impacto negativo no NPS, já que impacta diretamente no número de reclamações, contatos com suporte e tempo de resolução.

Clientes com maior NPS tendem a ter pouco ou nenhum atraso, menor número de reclamações, menor necessidade de contato com suporte. Enquanto clientes com menor NPS apresentam maiores atrasos, maior número de reclamações e maior tempo para resolução das reclamações. A análise também identificou um possível ponto de ruptura a partir de aproximadamente três dias de atraso, momento em que o NPS apresenta queda mais acentuada.

Além de medir satisfação, o NPS impacta diretamente a possibilidade de recompra, retenção de clientes e recomendações positivas. Esses fatores são essenciais para aumentar a competitividade no mercado desse e-commerce. 

Por isso, áreas como logística, atendimento, operações e estratégia podem utilizar esses insights para priorizar melhorias operacionais, reduzir falhas recorrentes e aprimorar a experiência do cliente.
