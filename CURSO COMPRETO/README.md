# INSTRUÇÕES
## 01) INTRODUÇÃO
### O que é o JSON Server?
O JSON Server é uma ferramenta que permite criar rapidamente uma API REST simulada usando um arquivo JSON como banco de dados. Ele é útil para desenvolvimento frontend, prototipagem rápida e testes, onde você precisa de uma API para interagir, mas ainda não possui um backend completo desenvolvido.

### Principais Características:
1. **Simulação de Backend**: O JSON Server simula um backend completo, permitindo que você defina endpoints, adicione dados e manipule recursos como se estivesse lidando com um servidor real.

2. **Banco de Dados Simulado**: Usa um arquivo JSON como banco de dados para armazenar e manipular os dados. Isso simplifica o processo de desenvolvimento, eliminando a necessidade de configurar e gerenciar um banco de dados real durante as fases iniciais do desenvolvimento.

3. **Operações CRUD**: Suporta operações CRUD (Create, Read, Update, Delete), permitindo que você crie, leia, atualize e delete dados usando os métodos HTTP correspondentes (POST, GET, PUT, DELETE).

4. **Configuração Flexível**: Oferece várias opções de configuração para personalizar o comportamento da API, incluindo ordenação, filtragem, paginação e definição de relacionamentos entre recursos.

### Como Usar:
1. **Inicializar um Projeto Node.js**: Como você já tem o Node.js instalado, o primeiro passo é inicializar um novo projeto Node.js. Isso pode ser feito executando o comando no terminal: 
   ```
   npm init -y
   ```

2. **Instalar o JSON Server localmente**: Em seguida, você precisará instalar o JSON Server como uma dependência do seu projeto Node.js. Você pode fazer isso executando o seguinte comando no terminal:
   ```
   npm install json-server
   ```

3. **Instalar o JSON Server globalmente (Opcional)**: Você pode instalar o JSON Server globalmente usando npm (Node Package Manager) com o seguinte comando:
   ```
   npm install -g json-server
   ```

4. **Criar um Arquivo JSON**: Agora, você precisa criar um arquivo JSON que servirá como seu banco de dados simulado. Você pode criar um arquivo chamado `db.json` e adicionar alguns dados de exemplo a ele. Por exemplo:
   ```json
      {
   "products": [
      {
         "id": 1,
         "title": "Product 1",
         "category": "electronics",
         "price": 4000,
         "description": "This is description about product 1"
      },
      {
         "id": 2,
         "title": "Product 2",
         "category": "electronics",
         "price": 2000,
         "description": "This is description about product 2"
      },
      {
         "id": 3,
         "title": "Product 3",
         "category": "books",
         "price": 1000,
         "description": "This is description about product 3"
      },
      {
         "id": 4,
         "title": "Product 4",
         "category": "fitness",
         "price": 3000,
         "description": "This is description about product 4"
      },
      {
         "id": 5,
         "title": "Product 5",
         "category": "fitness",
         "price": 4000,
         "description": "This is description about product 5"
      },
      {
         "id": 6,
         "title": "Product 6",
         "category": "gardening",
         "price": 5000,
         "description": "This is description about product 6"
      },
      {
         "id": 7,
         "title": "Product 7",
         "category": "furniture",
         "price": 6000,
         "description": "This is description about product 7"
      },
      {
         "id": 8,
         "title": "Product 8",
         "category": "furniture",
         "price": 7000,
         "description": "This is description about product 8"
      },
      {
         "id": 9,
         "title": "Product 9",
         "category": "accessories",
         "price": 4000,
         "description": "This is description about product 9"
      },
      {
         "id": 10,
         "title": "Product 10",
         "category": "electronics",
         "price": 3000,
         "description": "This is description about product 10",
         "discount": {
         "type": "shipping"
         }
      }
   ],
   "reviews": [
      {
         "id": 1,
         "rating": 3,
         "comment": "Review 1 for product id 1",
         "productId": 1
      },
      {
         "id": 2,
         "rating": 4,
         "comment": "Review 2 for product id 1",
         "productId": 1
      },
      {
         "id": 3,
         "rating": 4,
         "comment": "Review 3 for product id 1",
         "productId": 1
      },
      {
         "id": 4,
         "rating": 5,
         "comment": "Review 1 for product id 2",
         "productId": 2
      },
      {
         "id": 1,
         "rating": 3,
         "comment": "Review 1 for product id 3",
         "productId": 3
      }
   ]
   }
   ```

5. **Editar o package.json**: Agora, você pode editar o arquivo `package.json` para adicionar um script que iniciará o servidor JSON. Abra o arquivo `package.json` e adicione um script `"start"` que executará o JSON Server, apontando para o arquivo `db.json`. Por exemplo:
   ```json
   "scripts": {
     "start": "json-server --watch db.json"
   }
   ```

6. **Iniciar o Servidor JSON**: Por fim, você pode iniciar o servidor JSON executando o comando no terminal:
   ```
   npm start
   ```

7. **Explorar Endpoints**: Você pode acessar seus dados simulados por meio dos endpoints RESTful fornecidos pelo JSON Server. Experimente fazer requisições HTTP GET, POST, PUT, PATCH e DELETE para manipular os dados. (Veja a url sendo exibida no console).

8. **Experimentação**: Use ferramentas como Postman, cURL ou seu navegador para enviar requisições HTTP para o JSON Server e ver como ele responde. Experimente explorar recursos adicionais, como ordenação, filtragem e paginação.

O JSON Server é uma ferramenta poderosa e versátil para desenvolvimento frontend e teste de APIs. Ele permite que você comece rapidamente e iterativamente desenvolva e teste suas aplicações sem a necessidade de um backend completo.

## 02) GET REQUEST
### INSTRODUÇÃO:
Para fazer uma solicitação GET para o seu servidor JSON usando o Postman, siga estas etapas:

1. **Iniciar o Servidor JSON**: Certifique-se de que seu servidor JSON esteja em execução. Se você seguiu os passos anteriores, pode iniciar o servidor executando `npm start` no terminal.

2. **Abrir o Postman**: Abra o aplicativo Postman em seu computador.

3. **Criar uma Nova Solicitação**: No Postman, clique no botão "New" para criar uma nova solicitação.

4. **Selecionar o Método e a URL**: Na guia de criação de solicitação, selecione o método "GET" no menu suspenso ao lado da barra de URL. Em seguida, insira a URL do endpoint que deseja acessar. Por exemplo, se você deseja acessar todos os posts, a URL seria `http://localhost:3000/products` e
`http://localhost:3000/reviews`.

5. **Enviar a Solicitação**: Depois de inserir o método e a URL, clique no botão "Send" (Enviar) para enviar a solicitação GET para o servidor JSON.

6. **Verificar a Resposta**: O Postman mostrará a resposta do servidor JSON na área de resposta abaixo da barra de solicitação. Você verá os dados retornados pelo servidor JSON para a solicitação GET.

### EXEMPLOS DE SOLICITAÇÃO GET:
1. **Obter todos os produtos**:
   ```
   GET /products
   ```

2. **Obter um produto específico por ID**:
   ```
   GET /products/1
   ```

3. **Filtrar produtos por categoria** (por exemplo, 'electronics'):
   ```
   GET /products?category=electronics
   ```

4. **Ordenar produtos por preço em ordem crescente**:
   ```
   GET /products?_sort=price&_order=asc
   ```

5. **Obter as avaliações de um produto específico por ID**:
   ```
   GET /reviews?productId=1
   ```

6. **Filtrar produtos por preço mínimo (por exemplo, preço mínimo de 3000)**:
   ```
   GET /products?price_gte=3000
   ```

7. **Filtrar produtos por preço máximo (por exemplo, preço máximo de 4000)**:
   ```
   GET /products?price_lte=4000
   ```

8. **Filtrar produtos por preço entre um intervalo específico (por exemplo, entre 2000 e 4000)**:
   ```
   GET /products?price_gte=2000&price_lte=4000
   ```

## 03) FILTRAGEM GET:
Para realizar filtragem em solicitações GET no JSON Server, você pode usar parâmetros de consulta para especificar os critérios de filtragem. Aqui estão alguns exemplos de como você pode usar a filtragem GET com o seu servidor JSON:

1. **Filtrar produtos por categoria**:
   ```
   GET /products?category=electronics
   ```

   Isso retornará todos os produtos que pertencem à categoria "electronics".

2. **Filtrar produtos por preço mínimo**:
   ```
   GET /products?price_gte=3000
   ```

   Isso retornará todos os produtos com um preço igual ou superior a 3000.

3. **Filtrar produtos por preço máximo**:
   ```
   GET /products?price_lte=4000
   ```

   Isso retornará todos os produtos com um preço igual ou inferior a 4000.

4. **Filtrar produtos por preço dentro de um intervalo específico**:
   ```
   GET /products?price_gte=2000&price_lte=4000
   ```

   Isso retornará todos os produtos com preço entre 2000 e 4000.

5. **Filtrar produtos por categoria e preço mínimo**:
   ```
   GET /products?category=electronics&price_gte=2000
   ```

   Isso retornará todos os produtos da categoria "electronics" com um preço igual ou superior a 2000.

Esses são apenas alguns exemplos de como você pode usar a filtragem GET para buscar dados específicos no seu servidor JSON. Você pode experimentar diferentes combinações de parâmetros de consulta para atender às suas necessidades específicas de filtragem.

## 04) ORDENAÇÃO
Para ordenar os resultados de uma solicitação GET no JSON Server, você pode usar os parâmetros de consulta `_sort` e `_order`. Aqui estão alguns exemplos de como você pode usar a ordenação GET com o seu servidor JSON:

1. **Ordenar produtos por preço em ordem crescente**:
   ```
   GET /products?_sort=price&_order=asc
   ```

   Isso retornará todos os produtos ordenados pelo preço em ordem crescente.

2. **Ordenar produtos por preço em ordem decrescente**:
   ```
   GET /products?_sort=price&_order=desc
   ```

   Isso retornará todos os produtos ordenados pelo preço em ordem decrescente.

3. **Ordenar produtos por título em ordem alfabética**:
   ```
   GET /products?_sort=title&_order=asc
   ```

   Isso retornará todos os produtos ordenados pelo título em ordem alfabética crescente.

4. **Ordenar produtos por categoria em ordem alfabética**:
   ```
   GET /products?_sort=category&_order=asc
   ```

   Isso retornará todos os produtos ordenados pela categoria em ordem alfabética crescente.

Esses são alguns exemplos de como você pode usar a ordenação GET para ordenar os resultados da sua solicitação de acordo com um critério específico. Você pode experimentar diferentes combinações de parâmetros `_sort` e `_order` para atender às suas necessidades de ordenação. 

## 05) PAGINAÇÃO
Para realizar a paginação em solicitações GET no JSON Server, você pode usar os parâmetros de consulta `_page` e `_limit`. Aqui está como você pode usar a paginação GET com o seu servidor JSON:

1. **Paginar os resultados com um número específico de itens por página**:
   ```
   GET /products?_page=1&_limit=5
   ```

   Isso retornará os primeiros 5 produtos da primeira página.

2. **Acessar diferentes páginas de resultados**:
   ```
   GET /products?_page=2&_limit=5
   ```

   Isso retornará os próximos 5 produtos, correspondentes à segunda página.

3. **Definir um limite de itens por página e acessar uma página específica**:
   ```
   GET /products?_page=3&_limit=10
   ```

   Isso retornará os próximos 10 produtos, correspondentes à terceira página.

4. **Obter informações de paginação nos cabeçalhos da resposta**:
   Quando você faz uma solicitação GET paginada, o JSON Server inclui informações de paginação nos cabeçalhos da resposta. Você pode ver o número total de itens (`X-Total-Count`) e o número total de páginas (`X-Total-Pages`) na resposta.

   Por exemplo:
   ```
   X-Total-Count: 50
   X-Total-Pages: 10
   ```

Isso significa que há um total de 50 itens no recurso solicitado e pode ser paginado em 10 páginas, com 5 itens por página (se você estiver usando `_limit=5`). 

Esses são alguns exemplos de como você pode usar a paginação GET para dividir os resultados da sua solicitação em várias páginas. Você pode ajustar os valores de `_page` e `_limit` conforme necessário para navegar pelos resultados paginados. 

## 06) OPERADORES
No JSON Server, você pode usar operadores de consulta para realizar filtragem mais avançada em suas solicitações GET. Aqui estão alguns operadores comumente usados:

1. **_gte**: Maior ou igual a
   ```
   GET /products?price_gte=3000
   ```

2. **_lte**: Menor ou igual a
   ```
   GET /products?price_lte=4000
   ```

3. **_gt**: Maior que
   ```
   GET /products?price_gt=2000
   ```

4. **_lt**: Menor que
   ```
   GET /products?price_lt=5000
   ```

5. **_ne**: Diferente de
   ```
   GET /products?category_ne=electronics
   ```

6. **_like**: Contém uma string (case-sensitive)
   ```
   GET /products?title_like=Product
   ```

7. **_ilike**: Contém uma string (case-insensitive)
   ```
   GET /products?title_ilike=product
   ```

8. **_in**: Está em uma lista de valores
   ```
   GET /products?id_in=1,2,3
   ```

Esses operadores podem ser usados em conjunto com os parâmetros de consulta para filtrar os resultados de acordo com condições específicas. Experimente diferentes combinações de operadores e valores para obter os resultados desejados em suas solicitações GET. 

## 07) PESQUISA DE TEXTO COMPLETO:
No JSON Server, para realizar pesquisas de texto completo em campos de texto, você pode usar o operador `_q`. Este operador permite que você pesquise por um termo em todos os campos de texto dos seus dados. Aqui está como você pode usar a pesquisa de texto completo:

```
GET /products?q=searchTerm
```

Substitua `searchTerm` pelo termo que você deseja pesquisar. Isso retornará todos os produtos onde qualquer campo de texto contenha o termo especificado. Por exemplo:

```
GET /products?q=description
```

Isso retornará todos os produtos onde o campo de descrição contém a palavra "description".

Tenha em mente que a pesquisa de texto completo é case-insensitive, o que significa que não faz distinção entre maiúsculas e minúsculas. 

## 08) RELACIONAMENTOS
No JSON Server, é possível definir relacionamentos entre recursos diferentes usando IDs. Por exemplo, em seu arquivo `db.json`, você tem uma lista de produtos e uma lista de avaliações. Cada avaliação pode estar relacionada a um produto específico pelo ID do produto. Aqui está um exemplo de como você pode definir um relacionamento entre recursos:

```json
{
  "products": [
    { "id": 1, "title": "Product 1", ... },
    { "id": 2, "title": "Product 2", ... }
  ],
  "reviews": [
    { "id": 1, "productId": 1, "rating": 5, "comment": "Great product!" },
    { "id": 2, "productId": 1, "rating": 4, "comment": "Good quality." },
    { "id": 3, "productId": 2, "rating": 3, "comment": "Average product." }
  ]
}
```

Neste exemplo, a chave `productId` na lista de avaliações é usada para indicar a qual produto a avaliação está relacionada. A avaliação com `id` 1 está relacionada ao produto com `id` 1, e assim por diante.

Para obter avaliações de um produto específico, você pode fazer uma solicitação GET para `/reviews` e filtrar as avaliações pelo `productId`. Por exemplo:

```
GET /reviews?productId=1
```

Isso retornará todas as avaliações relacionadas ao produto com `id` 1.

Dessa forma, você pode estabelecer e trabalhar com relacionamentos entre diferentes recursos em seu servidor JSON. 

## 09) POST REQUEST
Para fazer uma solicitação POST no JSON Server, você pode usar o Postman ou qualquer outra ferramenta HTTP para enviar dados para o servidor. Aqui está um exemplo de como fazer uma solicitação POST usando o Postman:

1. Abra o Postman e crie uma nova solicitação.

2. Selecione o método POST na barra de seleção de método.

3. Insira a URL do endpoint onde deseja enviar os dados. Por exemplo, se você quiser adicionar um novo produto, a URL pode ser `http://localhost:3000/products`.

4. Selecione a aba "Body" abaixo da barra de URL.

5. Selecione o formato do corpo da solicitação. Para enviar dados JSON, selecione "raw" e escolha "JSON (application/json)" no menu suspenso.

6. Insira os dados que você deseja enviar no corpo da solicitação em formato JSON. Por exemplo:
   ```json
   {
     "title": "New Product",
     "category": "electronics",
     "price": 1500,
     "description": "This is a new product."
   }
   ```

7. Clique no botão "Send" (Enviar) para enviar a solicitação POST para o servidor.

Isso enviará os dados fornecidos para o endpoint especificado no corpo da solicitação POST. O servidor JSON Server responderá com os dados recém-adicionados, incluindo um ID único atribuído automaticamente. Você pode verificar a resposta para confirmar que os dados foram adicionados com sucesso.

No JSON Server, quando você faz uma solicitação POST para adicionar novos dados, o servidor atualiza o arquivo `db.json` em tempo real para refletir as alterações. Isso significa que os novos dados serão persistentes e estarão disponíveis mesmo após reiniciar o servidor.

Certifique-se de ajustar a URL e os dados conforme necessário para corresponder ao seu ambiente e aos dados que você deseja adicionar. 

## 10) PUT, PATCH E DELETE 
1. **PUT**:
   - O método PUT é usado para atualizar um recurso existente ou substituir completamente um recurso por um novo conjunto de dados.
   - Ao enviar uma solicitação PUT, o cliente fornece o URI do recurso que deseja atualizar e o novo conjunto completo de dados para substituir o recurso existente.
   - Se o recurso especificado no URI não existir, o servidor pode criar um novo recurso com os dados fornecidos.
   - Exemplo:
     ```
     PUT /products/1
     {
       "title": "New Title",
       "category": "electronics",
       "price": 1500,
       "description": "Updated description"
     }
     ```

2. **PATCH**:
   - O método PATCH é usado para aplicar modificações parciais a um recurso existente.
   - Em vez de substituir completamente o recurso, como no PUT, o PATCH aplica apenas as alterações especificadas aos campos do recurso.
   - Isso é útil quando você deseja atualizar apenas alguns campos do recurso sem afetar o restante.
   - Exemplo:
     ```
     PATCH /products/1
     {
       "price": 2000
     }
     ```

3. **DELETE**:
   - O método DELETE é usado para excluir um recurso existente.
   - Ao enviar uma solicitação DELETE, o cliente fornece o URI do recurso que deseja excluir.
   - Após a exclusão bem-sucedida, o servidor geralmente retorna um status 204 (No Content) para indicar que o recurso foi excluído com sucesso.
   - Exemplo:
     ```
     DELETE /products/1
     ```

Esses métodos são fundamentais para operações de CRUD (Create, Read, Update, Delete) em uma API RESTful. Eles permitem que os clientes interajam com recursos e realizem operações de modificação conforme necessário. 

## 11) CONFIGURAÇÕES
Para configurar o JSON Server e definir diferentes opções, você pode usar um arquivo de configuração `json-server.json` ou fornecer opções diretamente na linha de comando ao iniciar o servidor. Aqui estão algumas configurações comuns que você pode ajustar:

1. **Porta**:
   - Você pode especificar a porta em que o servidor irá escutar. Por padrão, o JSON Server usa a porta 3000.
   - Exemplo: `json-server --port 4000 db.json`

2. **Arquivo de dados**:
   - Por padrão, o JSON Server usa um arquivo chamado `db.json` como fonte de dados. No entanto, você pode especificar um arquivo diferente, se desejar.
   - Exemplo: `json-server --watch data.json`

3. **Roteamento personalizado**:
   - Você pode definir rotas personalizadas usando um arquivo de roteamento.
   - Exemplo: `json-server --watch db.json --routes routes.json`

4. **Atraso de resposta**:
   - Você pode simular atrasos de resposta para testar o comportamento do cliente em condições de rede mais lentas.
   - Exemplo: `json-server --watch db.json --delay 1000`

5. **Middlewares**:
   - O JSON Server permite que você use middlewares personalizados para adicionar funcionalidades extras à sua API.
   - Exemplo: `json-server --watch db.json --middlewares middleware.js`

Essas são apenas algumas das opções de configuração disponíveis no JSON Server. Você pode encontrar mais opções e detalhes sobre como configurar o JSON Server na documentação oficial: [JSON Server - Opções de CLI](https://github.com/typicode/json-server#options)

As opções configuradas para o JSON Server, como porta, atraso de resposta, roteamento personalizado, etc., não são salvas automaticamente em um arquivo como `package-lock.json`. Em vez disso, você pode salvar essas configurações em um arquivo de configuração específico para o JSON Server ou no script de inicialização do seu projeto.

### Opções de configuração com arquivo `json-server.json`
Você pode criar um arquivo de configuração chamado `json-server.json` na raiz do seu projeto para definir as opções padrão do JSON Server. Aqui está um exemplo de como configurar o JSON Server usando um arquivo `json-server.json`:

```json
{
  "port": 3001,
  "delay": 1000,
  "routes": "routes.json",
  "watch": "db.json"
}
```

### Salvando opções no `package.json`
Outra abordagem é adicionar um script no seu `package.json` para iniciar o JSON Server com as opções desejadas. Aqui está um exemplo de como fazer isso:

1. Abra o arquivo `package.json`.
2. Adicione um script para iniciar o JSON Server com as opções desejadas:

```json
{
  "name": "json-server-example",
  "version": "1.0.0",
  "scripts": {
    "start": "json-server --watch db.json --port 3001 --delay 1000 --routes routes.json"
  },
  "dependencies": {
    "json-server": "^0.17.0"
  }
}
```

### Usando um script JavaScript para iniciar o JSON Server
Você também pode criar um script JavaScript para configurar e iniciar o JSON Server com as opções desejadas. Por exemplo, crie um arquivo chamado `server.js`:

```javascript
const jsonServer = require('json-server');
const server = jsonServer.create();
const router = jsonServer.router('db.json');
const middlewares = jsonServer.defaults();

server.use(middlewares);
server.use(router);

server.listen(3001, () => {
  console.log('JSON Server is running on port 3001');
});
```

E adicione um script no `package.json` para iniciar o servidor:

```json
{
  "name": "json-server-example",
  "version": "1.0.0",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "json-server": "^0.17.0"
  }
}
```

### Resumo
- **Arquivo `json-server.json`**: Define as opções padrão em um arquivo de configuração JSON.
- **Arquivo `package.json`**: Adicione um script para iniciar o JSON Server com opções especificadas diretamente na linha de comando.
- **Script JavaScript (`server.js`)**: Configura e inicia o JSON Server usando código JavaScript.

## 12) GERAR DADOS ALEATÓRIOS
Para gerar dados aleatórios para usar com o JSON Server, você pode usar a biblioteca `faker.js` (ou sua versão mais recente, `@faker-js/faker`). Esta biblioteca permite gerar uma variedade de dados fictícios, como nomes, endereços, produtos, etc. Vou mostrar como configurar isso para gerar um conjunto de dados aleatórios e inicializar o JSON Server com esses dados.

### Passos para configurar o JSON Server com dados aleatórios
1. **Instalar o Faker.js**:
   - Primeiro, instale o `@faker-js/faker` usando npm:
     ```bash
     npm install @faker-js/faker
     ```

2. **Criar um script para gerar dados aleatórios**:
   - Crie um arquivo, por exemplo, `generateData.js`, para gerar dados aleatórios:
     ```javascript
     const { faker } = require('@faker-js/faker');
     const fs = require('fs');

     // Função para gerar dados aleatórios
     const generateData = () => {
       const data = {
         products: [],
         reviews: []
       };

       // Gerar produtos
       for (let i = 1; i <= 10; i++) {
         data.products.push({
           id: i,
           title: faker.commerce.productName(),
           category: faker.commerce.department(),
           price: faker.commerce.price(),
           description: faker.lorem.sentence()
         });
       }

       // Gerar avaliações
       for (let i = 1; i <= 10; i++) {
         data.reviews.push({
           id: i,
           rating: faker.datatype.number({ min: 1, max: 5 }),
           comment: faker.lorem.sentence(),
           productId: faker.datatype.number({ min: 1, max: 10 })
         });
       }

       return data;
     };

     // Escrever os dados gerados em um arquivo db.json
     fs.writeFileSync('db.json', JSON.stringify(generateData(), null, 2));
   ```

3. **Executar o script para gerar o arquivo `db.json`**:
   - Execute o script para gerar o arquivo `db.json` com dados aleatórios:
     ```bash
     node generateData.js
     ```

4. **Iniciar o JSON Server com o arquivo `db.json` gerado**:
   - Inicie o JSON Server usando o arquivo `db.json` que foi gerado:
     ```bash
     json-server --watch db.json
     ```

     Ou:

     ```bash
     npm start
     ```

### Exemplo de dados gerados
Aqui está um exemplo de como os dados no arquivo `db.json` podem parecer após executar o script:

```json
{
  "products": [
    {
      "id": 1,
      "title": "Awesome Granite Table",
      "category": "Furniture",
      "price": "500.00",
      "description": "Lorem ipsum dolor sit amet."
    },
    {
      "id": 2,
      "title": "Ergonomic Cotton Shoes",
      "category": "Footwear",
      "price": "120.00",
      "description": "Consectetur adipiscing elit."
    }
    // Mais produtos...
  ],
  "reviews": [
    {
      "id": 1,
      "rating": 4,
      "comment": "Great product!",
      "productId": 1
    },
    {
      "id": 2,
      "rating": 5,
      "comment": "Very comfortable.",
      "productId": 2
    }
    // Mais avaliações...
  ]
}
```

Seguindo esses passos, você terá um conjunto de dados aleatórios gerado pelo Faker.js e servido pelo JSON Server. Isso é extremamente útil para desenvolvimento e testes, permitindo criar um ambiente de dados realista sem necessidade de escrever tudo manualmente. 
