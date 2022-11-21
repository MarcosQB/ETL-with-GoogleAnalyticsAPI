# Google Analytics Reporting API With Python for ETL and Request
### Problema
##### A Área de Retail&Performance de umas das organizações que trabalhei solicitou um Dashboard a onde fosse possível visualizar os dados de **TODAS** as Lojas Online que eles mantinham controle no Google Analytics. Ao iniciar à construção dele no Looker Studio nos deparamos com o problema da ferramenta apenas puxar os dados de uma Loja por vés e mesmo adicionando os dados de outras lojas ele tinha grande difuldade em unir esses dados em uma base única, além disso todo esse processo ficaria extremamente manual o que causaria um problema de escabilidade.
### Solução
##### Para solucionar essa questão decidi construir um script em Python que unisse os dados de **TODAS** as Lojas Online em uma única base de dados. Dessa forma o script apresentado nesse projeto faz requisições para a API do Google Sheets que retorna os identificadores das nossas Lojas Online que anteriormente solicitei para área responsavel preencher e manter atualizado em uma planilha. Esses identificadores são utilizados para realizar a Requesição para a API do Google Analytics. O retorno dos dados de cada Loja é tratado e unido em um único DataFrame que é enviado para o Google BigQuery como Tabela para posteriormente ser consumido pelo Looker Studio na construção do Dashboard.
### Detalhes Técnicos
* ######  O script foi construido no Jupyter Notebook
* ######  O script foi construido em PYTHON
* ######  Todo processo de ETL foi construído utilizando as seguintes bibliotecas: Pandas, Numpy e Itertools.
* ###### Para armazenar os dados foi utilizado o Google BigQuery
