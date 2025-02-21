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

Após a etapa de estruturação, modelagem e tambem de tratamento dos dados no power query, finalmente iniciei as análises com DAX, e a criação de gráficos interativos que possibilitam uma maior interação do cliente com os dados.
Iniciei trazendo alguns indicadores fundamentais como o total das vendas, o custo total, a margem de lucro, o ticket médio de clientes e a quatidade de vendas realizadas, para que assim, com esses indicadores o gestão ja possa ter um panorama geral da situação da empresa.<br>
Ainhado aos indicadores, através de medidas dax, criei um gráfico indicando os 3 maiores clientes por valores de vendas, um grafico trazendo a região com mais clientes e com maiores valores de vendas e tambem trouxe um grafico informando qual a porcentagem dos tipos de clientes que a empresa atende. Com esses gráficos podemos tomar as seguintes conclusões:
- A região da América do Norte concentra a maior parte dos clientes da empresa;
- quase 75% destes clientes são outras empresas;<br>

Com essas informações os gestores podem tomar decisões mais acertivas, como por exemplo:
- Maiores incentivos na região da Amrérca do Norte, ou análisar qual a diferenã desta região para as demais, e aplicar está diferença nas outras regiões, buscando aumentar tambem as vendas nas demais regiões;
- Criação de promoções, ou estrátegias que fidelizam ainda mais empresas, ou aplicar mais esforços nos clientes pf. <br>

Além destas análises realizei tambem a criação de gráficos para análisar as vendas no decorrer do tempo. Por meio destas análises podemos concluir que:
- As vendas aumentam no meio do ano, mais precisamente no mês de julho;
- Enquanto as vendas para outras empresas se mantém, as vendas para clientes do tipo pessoas vem em uma tendência de declínio.<br>

Estas foram algumas das análises que são possiveis de realizar através deste dashboard.<br>
<br><br>
<a href="https://app.powerbi.com/view?r=eyJrIjoiN2RlNjcxODUtZDQ2NC00YWMzLWI0OGUtNGE4N2M4ODc3YTAzIiwidCI6IjUwZTI0ZTMwLWQyM2QtNDhkOC05NGQ0LWNkNmMzYTI2ODU0OCJ9" target="_blank">Clique aqui</a> e acesse o a solução desenvolvida para o cliente.

## Página Drill through

  <img align="right" width="500"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/Drill-through.png?raw=true">

Para facilitar a validação de informações, e auxiliar na análise dos dados por parte de gestões e clientes que irão utilizar este relatório, criei uma pagina drill through.

A página Drill Through no Power BI é uma funcionalidade que permite aos usuários navegar de um relatório mais geral para uma página detalhada, focada em um contexto específico. Isso significa que, ao selecionar um determinado elemento em um relatório (como uma categoria de produto, um cliente ou uma região), o usuário pode ser direcionado automaticamente para outra página que exibe informações mais detalhadas sobre essa seleção. <br>

<br>

## Tooltip

  <img align="left" width="350"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/tt_01%20(Detalhes%20do%20cliente).png?raw=true">
  <img align="left" width="350"  src="https://github.com/MateusQuina/ProjetoClientes01/blob/main/Imagens/tt_02%20(detalhes%20do%20produto).png?raw=true">

  Alinhado ao Drill Through, elaborei tambem as Tooltips ou dicas de ferramentas. As tooltips são dicas visuais que aparecem quando você passa o mouse sobre um elemento do relatório, fornecendo informações adicionais. 
  Qual a importância dessas dicas de ferramentas?
  - Elas possibilitam que informações relevantes sejam compreendias de maneira mais facil;
  - Possibilita dar foco em dados que precisam ser mais observados;
<br><br>

## Ferramentas e linguagens utilizadas
<div style="display: inline_block">
    <img align="center" alt="SQL" height="40" width="40" src="https://github.com/BruceFonseca/ferramentas/blob/main/logo.png?raw=true">
    <img align="center" alt="Power BI" height="40" width="40" src="https://github.com/BruceFonseca/ferramentas/blob/main/1200px-New_Power_BI_Logo.svg.png?raw=true">
</div>







