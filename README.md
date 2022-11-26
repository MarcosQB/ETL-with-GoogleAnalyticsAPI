# Google Analytics Reporting API With Python for request and ETL 
### Proposta:
##### A área de Retail & Performance de umas das organizações que trabalhei solicitou um Dashboard onde fosse possível visualizar os dados de todas as Lojas Online cujo os dados eram mantidos sob controle no Google Analytics.

##### Ao iniciar a construção do dashboard no Looker Studio obtive um resultado não correspondente às minhas expectativas iniciais: a ferramenta era capaz apenas de importar os dados de uma loja por vez, e ainda que fizéssemos essa importação uma a uma de forma manual, os dados não eram unificados em uma base única, somando-se a problemática de no futuro esse ser um processo altamente trabalhoso no caso de atingirmos um número maior de lojas.

### Solução:
##### A fim de resolver este problema, unifiquei os dados de todas as lojas em uma única base de dados, me utilizando da programação de um script em linguagem Python. E para tornar isso possível, o script faz requisições para a API do Google Sheets que retorna os identificadores das Lojas Online que anteriormente solicitei para área responsável preencher e manter atualizado em uma planilha. Posteriormente, os identificadores obtidos serão utilizados para uma nova requisição: a de solicitar os dados das lojas para o Google Analytics. Já com os dados à disposição, eles são tratados e unificados em um Data Frame, que é enviado em formato de tabela para o Google Big Query (serviço de armazenamento de dados em nuvem) e posteriormente são utilizados para nutrir o Looker Studio onde eles serão trabalhados na construção do dashboard.

### Detalhes Técnicos
* ######  A interface de desenvolvimento utilizada foi o Jupyter Notebook;
* ######  A linguagem de programação utilizada foi a Python;
* ######  Todo processo de extração, transformação e carregamento (ETL) dos dados foi construído utilizando as seguintes bibliotecas: Pandas, Numpy e Itertools.
* ###### Para armazenar os dados foi utilizado o Google BigQuery

### [Confira o script clikando aqui!](https://github.com/MarcosQB/ETL-with-GoogleAnalyticsAPI/blob/main/Google%20Analytics%20Request%20API.ipynb)
