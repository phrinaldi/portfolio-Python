# projeto-Python

Este é um projeto que tem o objetivo demonstrar a aplicação da linguagem Python em uma automação de processo.

Objetivo: Ao receber a planilha de vendas nacional, enviar um email para cada gerente das 25 lojas do Brasil com os indicadores de faturamento, diversidade de produtos e ticket médio acumulado e o do dia anterior.
Depois, enviar um email para a diretoria com o ranking das lojas.
(Porem, ao inves de usar o modulo win32 para envio real de emails, será utilizado o Ipython.display para mostrar como seria o email enviado com a formatação em HTML)

Importante antes de começar: Colocar o arquivo python na mesma pasta da pasta Base de Dados e Backup Arquivos Lojas

Passos do código:
1- Importar as 3 bibliotecas:
	Pandas - tabelas excel
	pathlib - pastas no pc
	IPython - visualização de como seriam os emails utilizando HTML

2- importar as bases:
	emails, lojas e  vendas

3- Mesclar a tabela de vendas com a tabela de lojas, para facilitar a criaçao de uma tabela unica para cada loja depois.

4- Criar uma tabela para cada loja
  1- fazer um FOR pra percorrer a coluna Loja
  2- colocar a tabela filtrada no dicionario

5- Definir o dia do indicador, pegando o maior valor da coluna Data

6- Back up dos arquivos (uma pasta para cada shopping com os arquivos diarios dentro):
verificar se a pasta para o shopping ja foi criada anteriormente, se nao foi, criar.
Tendo a pasta, salvar o excel lá.

  7 passos:
  1- colocar o caminho em uma variavel
  2- fazer uma lista das pastas que ja existem 
  3- criar uma lista vazia para receber os nomes das lojas
  4- adicionar, via FOR, o nome de todas as pastas que existem nessa lista vazia (passa de uma lista para outra, praticamente)
  5- verificar se existe uma pasta para a chave do dicionario de lojas. Se nao tiver, criar
  
  6- ja tendo a pasta, eh soh criar um nome e um caminho para a nova tabela do dia
  7- transforma a tabela em um excel e leva ate o caminho.

7- Calcular os 3 indicadores: faturamento – diversidade de produtos – ticket medio
  0- celula com as metas dos indicadores
  1- Para cada loja, criar 2 tabelas para fazer os indicadores – acumulado total e dia
  
  2- calculo do faturamento
  3- diversidade de produtos
  4- ticket medio

8- Corpo do email para os gerentes:
  1- criar os ícones para os indicadores
  2- corpo em html

9- Ranking para Diretoria:
  1- agrupar a tabela de vendas nacional por loja e somar
  2- criar um arquivo excel e salvar
  3- agrupar a tabela de vendas nacional por loja e somar os valores do dia
  4- criar um arquivo excel e salvar

10- Email para diretoria:
String simples, sem HTML, mas com os os primeiros e últimos colocados dos rankings.

