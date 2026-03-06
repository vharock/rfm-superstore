# rfm-superstore
Classificação dos clientes 

# Problema de Negócio
A SuperStore é uma rede de supermercados com várias unidades físicas espalhadas por todo o país, com o objetivo de fornecer alimentos e comercializar
os mais diversos produtos para consumo. Recentemente, o time de dados desenvolveu uma análise de Cohort para acompanhar a retenção dos clientes da rede e revelando números bons para alguns Cohorts e ruim para outros. Como essa informação, os gerentes resolveram fazer ações distintas para grupos específicos de clientes, afim de aumentar a taxa de retenção da empresa. Porém, ele não sabem como segmentar a base de clientes em grupos e nem qual seria a
necessidade para planejar a ação. 

# Contexto

Esse desafio chegou até o time de dados que precisar segmentar a base de clientes, criando grupo menores com necessidades específicas para uma ação mais precisa do time de Marketing e Produtos. O seu próximo problema de negócio é criar uma
segmentação de clientes e explicar as área de negócio, como Marketing, Vendas e Produto, a necessidade de cada grupo e quais ações poderiam ser feitas para
aumentar a retenção.

# Premissas da análise

Análise Descritiva:
Recência: Coluna “Order Date” - Tempo desde a última compra
Frequência: Coluna “Order ID” - Quantidade de pedidos comprados
Monetização: Coluna “Sales” - Soma de todos os produtos comprados

(Coluna, Dimensão, Descrição)
Order Date - Tempo - Quando aconteceu?
Ship Data - Tempo
Ship Mode - Entrega - Como foi entregue?
Sales - Produto - O que foi comprado?
Quantity - Produto
Discount - Produto
Product -  Produto
Use Id - Cliente - Quem comprou?

Combinação Fato-Dimensão
1. Quantidade de Pedidos por Data ( Dia, Mês, Ano, Semana, Feriado )
2. Quantidade de Pedidos por Data de Envio ( Dia, Mês, Ano, Semana, Feriado)
3. Quantidade de Pedidos por Tier de Preço ( Baixo, Médio, Alto )
4. Quantidade de Pedidos por Quantidade de Itens
5. Quantidade de Pedidos por Tier de desconto ( Baixo, Médio, Alto )
6. Quantidade de Pedidos por Produto
7. Quantidade de Pedidos por Clientes ( Frequência )
8. Quantidade de Pedidos Por Data e Tier de Preço
9. Quantidade de Pedidos Por Data e Quantidade de Itens
10. Quantidade de Pedidos por Data e Produto
11. Soma do preço de todos os pedidos realizados por Cliente ( Monetização )
12. Quantidade de Pedidos por Data e Clientes
13. Quantidade de Pedidos por Data de Envio e Tier de Preço
14. Quantidade de Clientes (Fato) que fizeram um novo pedido (Order Date) nos meses seguintes a partir da primeira compra (Order Date)
15. Tempo em dias desde a última compra por Cliente ( Recência )


Os 3 passos do SAPE
Passo 1: Determinar a Saída: 
Tabela>Customer ID, Recencia,Frequencia, Monetizacao, Nome do Segmento

Passo 2: Planejar o Processo
1. União das tabelas
2. Criar a tabela de Segmentos
3. Dar as notas para a Recência
4. Dar as notas para a Frequência
5. Dar as notas para a Monetrização
6. Combinar Frequência e Monetização
7. Atribuir cada usuário para um segmento
8. Interpretar o resultado
9. Responder a pergunta de negócio

Passo 3: Identificar as Entradas
1. Fonte de Dados:
a. orders.csv → Mês de Aquisição | Atividade | Mês Corrido
b. customer.csv → Customer ID
c. product.csv → Detalhes dos produtos
d. location.csv → Detalhes da localização


![rfm](img/rfm.jpg)
![img1](img/img1.jpg)
![img2](img/img2.jpg)
![img3](img/img3.jpg)
![img4](img/img4.jpg)
![img5](img/img5.jpg)





