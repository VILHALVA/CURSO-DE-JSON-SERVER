# TEORIAS:
## PRA QUE SERVE ESSE CURSO?
No curso de JSON Server você aprenderá sobre as requisições HTTP, como GET, POST, PUT, PATCH e DELETE. JSON Server é uma excelente ferramenta para entender como funcionam as operações CRUD (Create, Read, Update, Delete) em uma API REST, pois ele simula um servidor que responde a essas requisições com base em um arquivo JSON.

Essa tabela fornece uma visão geral de cada método HTTP, seu propósito e exemplos de uso comum:

| Método   | Descrição                                                                                             | 
|----------|-------------------------------------------------------------------------------------------------------|
| GET      | **Descrição**: Solicita dados de um recurso específico ou uma lista de recursos do servidor.         |
|          | **Uso Comum**: Recuperar informações de um usuário específico, uma lista de usuários, etc.            |
|          | **Exemplo**: `GET /api/users/1` para recuperar dados do usuário com ID 1.                             |
| POST     | **Descrição**: Envia dados ao servidor para criar um novo recurso.                                   |
|          | **Uso Comum**: Enviar dados de um formulário para criar um novo usuário, postagem, etc.              |
|          | **Exemplo**: `POST /api/users` com dados no corpo da requisição para criar um novo usuário.          |
| PUT      | **Descrição**: Atualiza completamente um recurso existente no servidor.                               |
|          | **Uso Comum**: Atualizar todos os dados de um usuário, postagem, etc.                                 |
|          | **Exemplo**: `PUT /api/users/1` com dados no corpo da requisição para atualizar o usuário com ID 1.   |
| PATCH    | **Descrição**: Atualiza parcialmente um recurso existente no servidor.                                |
|          | **Uso Comum**: Atualizar apenas alguns campos de um usuário, postagem, etc.                           |
|          | **Exemplo**: `PATCH /api/users/1` com dados no corpo da requisição para atualizar parcialmente o usuário com ID 1. |
| DELETE   | **Descrição**: Remove um recurso do servidor.                                                          |
|          | **Uso Comum**: Excluir um usuário, postagem, etc.                                                      |
|          | **Exemplo**: `DELETE /api/users/1` para excluir o usuário com ID 1.                                     |
| HEAD     | **Descrição**: Solicita apenas os cabeçalhos de resposta, sem o corpo da resposta.                     |
|          | **Uso Comum**: Verificar a existência de um recurso ou suas informações básicas.                       |
|          | **Exemplo**: `HEAD /api/users/1` para verificar se o usuário com ID 1 existe.                          |
| OPTIONS  | **Descrição**: Solicita os métodos HTTP permitidos em um recurso específico.                           |
|          | **Uso Comum**: Verificar quais métodos HTTP são permitidos em um endpoint.                             |
|          | **Exemplo**: `OPTIONS /api/users` para verificar os métodos permitidos para a rota de usuários.        |

Aqui está um resumo do que você pode esperar aprender sobre cada tipo de requisição HTTP:

- **GET**: Faz a leitura (Read) dos dados. Usado para recuperar dados do servidor. Você aprenderá a fazer requisições GET para obter dados armazenados no arquivo JSON.
  
- **POST**: Faz a escrita/gravação (Create) dos dados. Utilizado para enviar novos dados ao servidor. Você aprenderá a fazer requisições POST para adicionar novos registros ao arquivo JSON.
  
- **PUT**: Faz a edição/atualização (Update) completa dos dados. Usado para atualizar dados existentes no servidor. Você aprenderá a fazer requisições PUT para substituir completamente um registro existente.
  
- **PATCH**: Similar ao PUT, mas usado para atualizar parcialmente um registro. Você aprenderá a fazer requisições PATCH para modificar apenas partes específicas de um registro.
  
- **DELETE**: Faz a remoção (exclui/apaga - Delete) dos dados. Utilizado para remover dados do servidor. Você aprenderá a fazer requisições DELETE para excluir registros do arquivo JSON.

Com essas operações, você consegue criar, ler, atualizar e deletar dados, o que compõe o CRUD completo. Durante o curso, você praticará essas operações usando JSON Server, o que te dará uma compreensão prática de como funcionam as requisições HTTP e como manipular dados em uma API REST.

## EXEMPLO DE CRUD COM JSON SERVER:
1. **GET** - Ler dados:
   ```bash
   curl -X GET http://localhost:3000/posts
   ```
   Este comando retorna todos os registros da coleção `posts`.

2. **POST** - Criar novo dado:
   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"title": "Novo Post", "author": "Autor"}' http://localhost:3000/posts
   ```
   Este comando adiciona um novo registro à coleção `posts`.

3. **PUT** - Atualizar dado existente:
   ```bash
   curl -X PUT -H "Content-Type: application/json" -d '{"id": 1, "title": "Post Atualizado", "author": "Novo Autor"}' http://localhost:3000/posts/1
   ```
   Este comando substitui completamente o registro com `id` 1 na coleção `posts`.

4. **PATCH** - Atualizar parcialmente dado existente:
   ```bash
   curl -X PATCH -H "Content-Type: application/json" -d '{"author": "Autor Atualizado"}' http://localhost:3000/posts/1
   ```
   Este comando atualiza parcialmente o registro com `id` 1 na coleção `posts`, modificando apenas o campo `author`.

5. **DELETE** - Remover dado:
   ```bash
   curl -X DELETE http://localhost:3000/posts/1
   ```
   Este comando remove o registro com `id` 1 da coleção `posts`.

Esses exemplos mostram como você pode usar JSON Server para realizar operações CRUD completas, facilitando o desenvolvimento e teste de suas aplicações.

## COMPARAÇÃO ENTRE OS METODOS: HTTP, FORM HTML E JAVA POO:
Esta tabela destaca as semelhanças e diferenças entre os métodos HTTP, os métodos de formulários HTML e os métodos de acesso (getters e setters) em Java:

| Contexto               | Métodos HTTP       | Métodos HTML  | Métodos POO em Java |
|------------------------|--------------------|---------------|----------------------|
| Propósito              | Comunicação entre cliente e servidor na web. | Definir como os dados de um formulário HTML devem ser enviados ao servidor. | Manipular atributos dos objetos em uma aplicação Java. |
| GET                    | Recuperar dados do servidor. | Recuperar informações de um formulário HTML. | Recuperar o valor de um atributo de um objeto. |
| POST                   | Enviar dados ao servidor para criar um novo recurso. | Enviar dados de um formulário HTML ao servidor para processamento. | Definir ou modificar o valor de um atributo de um objeto. |
| PUT                    | Atualizar completamente um recurso existente no servidor. | Não aplicável em formulários HTML. | Não aplicável em getters e setters. |
| PATCH                  | Atualizar parcialmente um recurso existente no servidor. | Não aplicável em formulários HTML. | Não aplicável em getters e setters. |
| DELETE                 | Remover um recurso do servidor. | Não aplicável em formulários HTML. | Não aplicável em getters e setters. |

A analogia ajuda a entender a funcionalidade básica de leitura e escrita, mas é importante lembrar que os métodos HTTP operam em um contexto de rede (web), enquanto os getters e setters operam no contexto interno de uma aplicação.

## HEAD X SELECT:
Embora "HEAD" e "SELECT" tenham propósitos diferentes em contextos diferentes, eles compartilham algumas semelhanças que podem evocar essa associação.

- **HEAD** (HTTP): É um método HTTP usado para solicitar apenas os cabeçalhos de resposta de um recurso específico, sem o corpo da resposta. Ele é usado principalmente para verificar a existência de um recurso ou suas informações básicas, sem a necessidade de recuperar todo o conteúdo do recurso.

- **SELECT** (SQL): É uma cláusula SQL usada para recuperar dados de um banco de dados. Ele é usado para consultar dados de uma ou mais tabelas e retornar os resultados que correspondem aos critérios especificados na consulta.

Ambos os comandos envolvem a obtenção de informações de um recurso, mas de maneiras diferentes:

- **HEAD**: Obtém informações básicas sobre um recurso da web, como a existência do recurso, o tipo de conteúdo, tamanho do arquivo, entre outros, sem a sobrecarga de recuperar o corpo completo da resposta.

- **SELECT**: Obtém dados de um banco de dados com base em condições especificadas na consulta, retornando os registros que correspondem aos critérios definidos.

Portanto, enquanto "HEAD" e "SELECT" podem evocar uma associação superficial devido à sua função de obtenção de informações, é importante reconhecer que operam em contextos diferentes (HTTP e SQL) e têm propósitos distintos (verificação de recursos web e consulta de banco de dados).

## SOBRE O METODO HTTP "OPTIONS":
O método HTTP "OPTIONS" é usado para solicitar informações sobre os métodos HTTP permitidos em um recurso específico. Ele fornece uma maneira para o cliente (navegador, aplicação) verificar quais métodos são suportados em um endpoint da API.

Portanto, você pode usar o método "OPTIONS" para controlar como sua API deve ser usada, especificando quais métodos HTTP são permitidos em cada endpoint. Isso pode incluir permitir ou negar o uso de métodos específicos, como GET, POST, PUT, DELETE, etc.

Por exemplo, você pode configurar sua API para permitir apenas requisições GET em determinados endpoints, enquanto permite requisições GET e POST em outros. Isso ajuda a garantir a segurança e a integridade dos dados em sua API, limitando o tipo de operações que os clientes podem realizar em cada recurso.

Portanto, o método "OPTIONS" é uma ferramenta útil para controlar e configurar o comportamento da sua API, permitindo que você defina políticas de acesso e restrições de uso de maneira granular.

## API REST COMO INTERMEDIADOR ENTRE O CLIENTE E O BANCO DE DADOS:
Usar uma API REST como intermediário entre sua aplicação cliente e o banco de dados MySQL pode adicionar uma camada adicional de segurança e controle sobre o acesso aos dados. Aqui estão algumas maneiras pelas quais isso pode acontecer:

1. **Controle de Acesso**: A API REST pode implementar autenticação e autorização para controlar quem pode acessar os dados e quais operações podem ser realizadas em cada recurso. Isso ajuda a proteger o banco de dados contra acessos não autorizados.

2. **Validação de Dados**: A API pode validar os dados recebidos da aplicação cliente antes de encaminhá-los para o banco de dados. Isso ajuda a garantir a integridade dos dados armazenados no banco.

3. **Encapsulamento de Lógica de Negócios**: A API pode encapsular a lógica de negócios e regras de validação, garantindo que todas as operações no banco de dados sigam um conjunto predefinido de regras.

4. **Auditoria e Registro**: A API pode registrar todas as operações realizadas nos dados, fornecendo um registro detalhado de quem acessou os dados e quais alterações foram feitas.

5. **Escalabilidade e Flexibilidade**: Usar uma API REST como intermediário permite que você faça alterações na lógica de negócios ou no banco de dados sem afetar diretamente a aplicação cliente, tornando o sistema mais flexível e fácil de escalar.

No entanto, é importante garantir que a API REST seja implementada de forma segura, com práticas de segurança adequadas, como autenticação forte, criptografia de dados sensíveis e proteção contra ataques comuns, como injeção de SQL e ataques de negação de serviço (DoS). Com uma implementação adequada, uma API REST pode fornecer uma camada valiosa de segurança e controle sobre o acesso aos dados do seu banco de dados MySQL.

## PORQUE O "JSON SERVER" É UMA API REST FAKE?
O termo 'API REST fake' refere-se ao fato de que o JSON Server simula uma API REST completa, mas não está conectado a um banco de dados ou servidor backend complexo. Em vez disso, ele utiliza um arquivo `db.json` local como fonte de dados, o que permite realizar operações CRUD, como POST, GET, PUT e DELETE, em um ambiente de desenvolvimento simulado.

Existem algumas razões pelas quais o JSON Server é considerado uma 'API REST fake':

1. **Simulação de Backend**: O JSON Server é usado principalmente para desenvolvimento frontend, prototipagem rápida e testes, onde você precisa de uma API para interagir, mas ainda não possui um backend completo desenvolvido.

2. **Banco de Dados Simulado**: Ele usa um arquivo JSON como banco de dados para armazenar e manipular os dados. Este arquivo JSON pode conter qualquer tipo de dados, como se fosse um banco de dados real.

3. **Comportamento Controlado**: Você pode definir manualmente os endpoints da API, os dados que eles retornam e até mesmo simular atrasos de resposta, permitindo testar diferentes cenários de forma controlada.

4. **Simplicidade e Rapidez**: O JSON Server é extremamente fácil de configurar e usar. Com apenas um comando, você pode ter uma API REST funcional em funcionamento, o que é útil para projetos de desenvolvimento ágil.

5. **Persistência Limitada de Dados**: Embora o JSON Server atualize o arquivo `db.json` em tempo real para refletir as alterações feitas por solicitações POST, os dados armazenados nele não persistem entre as reinicializações do servidor. Isso o torna ideal para testes e desenvolvimento, mas não é adequado para produção, onde você precisa de um armazenamento de dados permanente.

Em resumo, o JSON Server é uma ferramenta valiosa para desenvolvedores que precisam de uma API REST rápida e fácil para fins de desenvolvimento, prototipagem e testes, mas não é adequado para aplicativos em produção que requerem um backend robusto e escalável.

## REQUESIÇÃO POST ALTERAM OS DADOS NO JSON:
Quando você faz um "POST" para o JSON Server usando o Postman ou qualquer outra ferramenta de cliente HTTP, o JSON Server recebe a solicitação, processa-a e retorna uma resposta com status "200 OK", indicando que a solicitação foi bem-sucedida.

O JSON Server atualiza o arquivo `db.json` em tempo real para refletir as alterações feitas por solicitações POST. Isso significa que os dados enviados em solicitações POST são persistentes e estarão disponíveis mesmo após reiniciar o servidor.

Portanto, quando você faz uma solicitação POST para adicionar novos dados, como novos produtos, eles são de fato adicionados ao arquivo `db.json` e permanecerão lá, a menos que você os exclua ou faça alterações neles posteriormente.
