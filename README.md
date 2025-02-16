# Análise de clientes ContosoRetailDW
Utilizando o banco de dados ContosoRetailDW, empresa fictícia de vendas de produtos eletronicos, iniciamos uma análise para entender a evolução dos clientes ao longo do tempo. O objetivo inicial é fazer uma análise exploratória dos clientes que compraram os produtos da ContosoRetailDW, entendendo onde estão, quanto e o que compram, como se comportaram as vendas ao longo dos meses e quais produtos foram mais vendidos.

Fazendo o download do arquivo ContosoRetailDW.bak e anexando-o no SQL Server, é possível executar cada consulta SQL utilizada nesta análise e obter os mesmos resultados apresentados.
<br><br>

## Análise exploratória no banco de dados
<img align="right" width="400"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/SQL%2003.png?raw=true">
Iniciamos o projeto entendendo cada objeto, tabela, campo, tipos de dados e relacionamentos do modelo de dados ContosoRetailDW. Após identificar as tabelas e entender como elas se relacionavam, iniciei as primeiras análises, utilizei primeiramente o campo de clientes e vendas e então desenvolvi os scripts em SQL para explorar os dados e extrair os primeiros insights. Como por exemplo: <br><br>
- Clientes com os maiores valores de venda <br>
- Em quais regiões estes clientes estvam <br>
- Produtos mais comprados por estes clientes <br>
<br><br>
<a href="https://github.com/MateusQuina/ProjetoClientes01/blob/main/SQL/Querys.sql" target="_blank">Clique aqui</a> e acesse o script SQL no Github.


<br><br>
<br><br>
<br><br>
## Análise exploratória com inteligência temporal

  <img align="left" width="500"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/SQL%2002.png?raw=true">
  <img align="left" width="500"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/SQL%2001.png?raw=true">
Após realizar as primeiras análises no SQL, iniciei na análise temporal que consiste em analisar dados e compara-los em contextos temporais diferentes, por exemplo, venda deste mês contra o mês passado, (MoM), vendas deste mês com o mesmo meês do ano passado etc. <br>

Para esta análise iniciei agrupando o valor das vendas por cada mês para ja identificar possiveis tendências no decorrer do tempo. Em seguida realizei uma CTE para extrair a informação das vendas do mesmo passado para o mesmo contexto das vendas atuais, tornando possivel assim a comparação entre os periodos. A CTE (Common Table Expression) é utilizada para criar consultas temporarias, deixando o codigo mais otimizado e organizado. Porém para este projeto não é a unica forma de realizar esta análise.
