#  **Final Challenge VtexIo**

Este Repositório hospeda os seguintes items 

  * [Loja Vtex](https://github.com/HamiltonLopes/vtex-finalchallenge-theme): Usa da estratégia de compre junto para aumentar o ticket
    médio da loja, na home se encontra o componente com as maiores vendas da loja sendo oferecidas ao cliente, e na página do produto
    se encontra o componente que mostra ao cliente as melhores combinações para aquele produto.
  * [Api Combinations](https://github.com/HamiltonLopes/combinationsAPI): API Hospedada na aws com Ec2, Route53 e com dominio
    próprio, essa api acessa um documento no MasterData da VTEX e armazena os dados de combinações de compras, e dados das melhores
    combinacoes (com maior quantidade de compras) com ela pode-se consultar as melhores combinacoes de um determinado produto, e, com 
    ajuda da configuração do OrderHook, creditar as novas combinacoes de acordo com as novas compras que são inseridas.
  * [Vtex ReactApp compre-junto-component](https://github.com/HamiltonLopes/compreJuntoComponentVtexIO): App em VtexIO que mostra na página
    do produto as melhores combinações de compra para aquele produto. Este app faz uma consulta na Combinations API e retorna para o cliente
    as melhores opções de compras em conjunto para serem adicionadas no carrinho de uma vez só.
  * [Vtex ReactApp compre-junto-component-home](https://github.com/HamiltonLopes/compreJuntoComponentHome): Outro VtexIO App que mostra ao cliente
    as melhores combinações de vendas de toda a loja, este componente se encontra na Home e faz a busca no backend da lista de combinações campeãs 
    de venda.
  * [Vtex-Admin-Block admin-combinations](https://github.com/Eu-Henrique/Componente_Admin_HC3_Travellog): Componente Admin Vtex que mostrra ao lojista
    as principais combinações da loja e a quantidade de vendas que cada combinação teve.

## Team 

  * [Jean Fraga](https://www.linkedin.com/in/jean-fraga/)
  * [Hamilton Lopes](https://www.linkedin.com/in/hamilton-lopes/)
  * [Gustavo Sobreiro](https://www.linkedin.com/in/gustavo-sobreiro-de-assis/)
  * [Hamiceis Pereira](https://www.linkedin.com/in/hamiceis-pereira/)
  * [Beatriz Cunha Guimarães](https://www.linkedin.com/in/mbeatrizcg/)
  * [Derek Santos](https://www.linkedin.com/in/derekcsantos/)
  * [Marco Antonio](https://www.linkedin.com/in/marco-antonio-pereira-esteves-005185113/)
  * [Renato Tadeu](https://www.linkedin.com/in/renato-tadeu)
  * [Henrique Scherer](https://www.linkedin.com/in/henrique-scherer/)
  * [Fabio Rogerio](https://www.linkedin.com/in/fabio-rogerio-234b65223/)

## Organização
  * Foi feito a divisão das atividades em pequenas atividades utilizando a ferramenta [Trello](https://trello.com/)
  o nosso quadro de trabalho está disponível para visualização neste [link](https://trello.com/b/L6qMTBtS/vtex-challenge-travellog-final).
  
  ![trello](https://user-images.githubusercontent.com/9729963/183319914-d0601b1b-bdf9-4460-8b41-147ff1490460.jpg)
  
## Fluxograma
  ![fluxograma](https://user-images.githubusercontent.com/9729963/183322419-27f0d1a4-3183-434e-ad98-ec8ed8587b9d.jpg)
  
  O fluxograma foi desenvolvido para auxiliar durante todo o projeto e para organizar a separação de tarefas.

  
## Vtex-Store

### Como rodar este projeto ?

* `git clone` com a url deste repositório 
* Assegure-se de ter seu ambiente configurado e o  Vtex-CLI instalado e configurado
  * [ambiente](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-1-basicsetup)  
  * [Vtex-cli](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-vtex-io-cli-installation-and-command-reference) 
* Dentro da pasta travellog-group1-store, execute   `vtex login  <yourAccount>`    
* Em seguida para criar um workspace execute `vtex use <dev>`
* Execute `vtex setup`
* Execute `npm install`
* Execute `vtex link`
* Log in to your store yourdomain.vtex.com


### Screenshots 
  ![imgstore](https://user-images.githubusercontent.com/9729963/180127132-e46ec500-2792-451a-b2c6-465d42258674.gif)
  
  ![travellog1](https://user-images.githubusercontent.com/9729963/180127291-7ea815ed-e532-43f6-8917-4118a55773b6.png)
  
  ![travellog2](https://user-images.githubusercontent.com/9729963/180127547-3de7d05f-be27-4863-ba67-7a450451059d.png)
  
  ![travellog3](https://user-images.githubusercontent.com/9729963/180127666-b6431a5f-f4d3-4264-bb36-79a7a141631a.png)
  
###  Principais Componentes
  ```"travellog.compre-junto-component-home": "0.x",```
  
  ```"travellog.compre-junto-component": "0.x",```
  
  ```"travellog.admin-combinations": "0.x"```

## Admin  - Combinations  
  O Lojista poderá ver e entender as combinações que estão aparecendo em sua loja no mesmo local onde configura outras informações:
  ![combinacoes-admin](https://user-images.githubusercontent.com/9729963/183322887-313a1240-5765-4dbf-80b5-789ed346016f.jpg)

## Rotas importantes
  * `https://hccombinationsapi.tk/combinations-api/v1/store-top-combinations` - Acessa as principais combinações da loja
  * `https://hccombinationsapi.tk/combinations-api/v1/combinations-by-id/:productId` - Acessa pontuação do usuário por id

## Documentação-Swagger

  Combinations API:
  
  ![rewardsapi](https://user-images.githubusercontent.com/9729963/180130510-0223a161-4899-49ad-af65-cc90127bcb3e.jpg)
  

  Antes de acessar a documentação online certifique-se de que as instruções de **Como rodar o projeto** foram executadas.
## Consultas por GraphQL
  Foi utilizado GraphQL para consultas internas no catalogo Vtex para ter maior segurança e performance:
  ![graphql query](https://user-images.githubusercontent.com/9729963/183323332-fccc91dc-da20-4647-87e8-2bb983dbb349.jpg)

## 🚀 Melhorias
As seguintes melhorias poderiam ser feitas para aprimoramento do projeto

Principais Pontos de Melhoria:
 - Melhorias no layout em geral, front-end de loja
 - Utilizar mais ferramentas de performance
 - Disponibilizar opções para customização de combinações
 - Ranking, opnião do cliente sobre aquela combinação

## Tecnologias utilizadas

#### Principais tecnologias utilizadas no código

💻 [Node.js](https://nodejs.org/)

🛠 [JavaScript](https://www.javascript.com/)

🛠 [TypeScript](https://www.typescriptlang.org/)

🛠 [ReactJS](https://pt-br.reactjs.org/)

💻 [AWS](https://aws.amazon.com/pt/)

💻 [GraphQL](https://graphql.org/)

#### Vtex Techs|Apis

🛠 [VtexIO](https://vtex.com/pt-br/blog/vtex-book/vtexbook-vtex-io/)

🛠 [VtexContext](https://developers.vtex.com/vtex-developer-docs/reference-edit/catalog-api-get-product-context)

🗄️ [Vtex-MasterData](https://developers.vtex.com/vtex-rest-api/reference/master-data-api-v2-overview)

⚓[Vtex-Hook](https://developers.vtex.com/vtex-rest-api/docs/orders-feed)
