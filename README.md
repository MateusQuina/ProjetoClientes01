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

Para esta análise iniciei agrupando o valor das vendas para cada mês, sendo possivel ja identificar possiveis tendências no decorrer do tempo. Em seguida realizei uma CTE para extrair a informação das vendas do mesmo passado e trazer para o mesmo contexto das vendas atuais, tornando possivel a comparação entre os periodos. A CTE (Common Table Expression) é utilizada para criar consultas temporarias, deixando o codigo mais otimizado e organizado, porém não é a unica forma de realizar esta análise.<br>
Com a CTE criada realizei o particionamento por ano e ordenamento por mês, montando assim a estrutura correta para a análise.<br>

<br><br>
<a href="https://github.com/MateusQuina/ProjetoClientes01/blob/main/SQL/Querys.sql" target="_blank">Clique aqui</a> e acesse o script SQL no Github.
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
## Conclusão técnica SQL

Com o SQL, podemos analisar, extrair, manipular e exibir os dados direto de uma base de dados de uma forma simples e rápida, apenas conectando na fonte dos dados. Porém, não é uma ferramenta dinâmica, pois cada vez que pricisar ver os dados de uma forma diferente, precisa reescrever o comando SQL para extrair os dados da forma que gostaria, porem os dados sempre serão exibidos em formato de tabela, deixando sua análise menos dinamica do que um dashboard, por exemplo.

A minha conclusão é que o SQL é sempre uma linguagem muito importante e deve ser utilizada para analisar um banco de dados antes de escolher outra ferramenta para análise dos dados, como o Power BI por exemplo. Ou seja, a validação das informações no SQL é indispiensavel e só depois considere outras ferramentas de acordo com a necessidade da empresa ou projeto que estiver atuando.
Não existe uma ferramenta melhor que a outra, existe ferramentas adequadas as necessidades apresentadas em cada projeto de dados.

## Estruturando o modelo

<img align="right" width="500"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/Modelo%20de%20Dados.png?raw=true">

Após a etapa inicial da análise que foi realizada direto no banco de dados, próximo passo foi necessario realizar a estrturação e a modelagem dos dados, como na primeira etapa eu ja havia verificado os campos, as chaves e como as tabelas se relacionavam, foi mais eficaz a estruturação do modelo na ferramenta Power BI.<br>
Iniciei trazendo a tabela fato das vendas onlines, e em seguida exportei as tabelas dimensões.<br>
Qual a necessidade de uma boa estruturação e modelagem dos dados: <br>
- Melhora no desempenho;
- Garante a integridade e consistência;
- Facilita a manipulação e as futuras atualizações;
<br><br>

## Desenvolvimento do Dashboard

<img align="left" width="500"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/Dashboad02.png?raw=true">

Após a análise de estruturação, modelagem e tambem de tratamento dos dados no power query, finalmente iniciei as análises com DAX, e a criação de gráficos interativos que possibilitam uma interação maior do cliente com os dados.
