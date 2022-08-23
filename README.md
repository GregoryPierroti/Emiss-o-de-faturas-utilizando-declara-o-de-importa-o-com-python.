<h1>Emissão de faturas utilizando declaração de importação com python.<h1>

O projeto se trata de uma automação realizada via codificação python, no qual tem a intenção de utilizar uma fonte de arquivos XML de uma declaração de importação, e através da mesma, após alguns calculos e modificações de dados específicos, é montado uma fatura, constando informações que são importantes para o cliente dar entrada em seu sistema, e essa fatura é emitida via arquivo excel. A automação, le os dados do xml, cria uma estrutura que recebe esses dados modificados e alimenta uma planilha excel para cada importação realizada, a fonte de dados consta na pasta XML, os arquivos 'modele' e 'nova tabela sicomex' são outras fontes para criar a fatura e ajudar em um calculo respectivamente, enquanto o arquivo PO XXXXXXXXXXX, seria o arquivo final gerado pela automação, lembrando que por conter diversos dados sensíveis, eu censurei os mesmos para nõa haver exposição de terceiros.

Abaixo utilizamos diversas bibliotecas e recursos do python, são elas:

-> **BeautifulSoup**: para extrairmos informações de uma documentação XML
-> **os**: para identificarmos os arquivos que queremos manipular
-> **re**: método Regex para que consigamos extrair informações dentro de uma descrição complexa dentro da declaração de importação
-> **Datetime & timedelta**: para que possamos fazer manipulação das datas com maior facilidade
-> **pandas**: para acessarmos um arquivo excel via dataframe(tabela siscomex) e facilitar a consulta
-> **xlrd & openpyxl**: a fim de abrir, manipular e escrever um arquivo excel.
-> **pycotação**: lib que faz webscrapping do banco central e usamos para pegar informações das taxas de venda de euro e dolar do dia da data de registro
da declaração de importação
-> Além de tudo isso, utilizamos bastante a metodologia **kwargs**, para evitarmos de fazermos diversos loops em cada função, afim de melhorar o desempenho e organização no código, além da documentação de todas as funções com **DocString's**.
