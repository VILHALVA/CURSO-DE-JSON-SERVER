# MANUAL
## INSTALAÇÃO INICIAL:
1. **Instalação do JSON Server**: Você precisará instalar o JSON Server em sua máquina. Você pode fazer isso usando o npm (Node Package Manager), executando o seguinte comando no seu terminal:
   ```
   npm install -g json-server
   ```

2. **Criar um Arquivo JSON**: Crie um arquivo JSON que servirá como seu banco de dados simulado. Este arquivo conterá os dados que você deseja acessar e manipular usando o JSON Server. Por exemplo, você pode criar um arquivo `db.json` com alguns dados iniciais:
   ```json
   {
     "posts": [
       { "id": 1, "title": "Post 1", "author": "Author 1" },
       { "id": 2, "title": "Post 2", "author": "Author 2" }
     ],
     "comments": [
       { "id": 1, "body": "Comment 1", "postId": 1 },
       { "id": 2, "body": "Comment 2", "postId": 1 }
     ]
   }
   ```

3. **Iniciar o JSON Server**: Após criar seu arquivo JSON, você pode iniciar o JSON Server executando o seguinte comando no terminal, apontando para o arquivo JSON que você criou:
   ```
   json-server --watch db.json
   ```

4. **Explorar os Endpoints**: Uma vez que o JSON Server estiver em execução, você poderá acessar seus dados simulados por meio dos endpoints RESTful que ele fornece. Por exemplo, você pode acessar os posts em `http://localhost:3000/posts` e os comentários em `http://localhost:3000/comments`.

5. **Experimentar as Requisições HTTP**: Use ferramentas como Postman, cURL ou seu navegador para enviar requisições HTTP para o JSON Server e ver como ele responde. Experimente fazer requisições GET, POST, PUT, PATCH e DELETE para manipular os dados.

6. **Explorar Recursos Adicionais**: Além das operações CRUD básicas, o JSON Server suporta recursos adicionais, como ordenação, filtragem, paginação e relacionamentos entre recursos. Experimente explorar esses recursos para entender completamente o que o JSON Server pode fazer.

## CRIANDO DOCUMENTAÇÃO COM POSTMAN:
O Postman oferece a funcionalidade de documentação, onde você pode descrever endpoints, parâmetros, cabeçalhos, corpos de requisição e respostas, bem como fornecer exemplos e descrições detalhadas.

Aqui estão os passos para criar uma documentação para sua API JSON Server no Postman:

1. **Abra o Postman**: Inicie o aplicativo Postman e faça login em sua conta, se necessário.

2. **Criar uma Coleção**: Crie uma nova coleção para sua API JSON Server, se ainda não tiver uma. Você pode fazer isso clicando no botão "New" na barra lateral esquerda e selecionando "Collection".

3. **Adicionar Requisições à Coleção**: Adicione todas as suas requisições (GET, POST, PUT, DELETE, etc.) à coleção, representando os endpoints da sua API JSON Server.

4. **Documentação da Coleção**: Com a coleção aberta, clique na aba "Documentation" na parte superior. Aqui você verá uma visualização da sua documentação atual.

5. **Adicionar Descrições e Exemplos**: Para cada requisição na coleção, você pode adicionar descrições detalhadas, parâmetros, exemplos de corpo de requisição e resposta, bem como outras informações relevantes. Isso ajudará os usuários a entender como usar sua API.

6. **Organizar e Personalizar**: Organize sua documentação como desejar, criando seções, subseções e ordenando as requisições de maneira lógica. Você também pode adicionar notas, observações ou qualquer outra informação útil para os usuários.

7. **Compartilhar a Documentação**: Depois de criar sua documentação, você pode compartilhá-la com outras pessoas clicando no botão "Share" na parte superior direita. Isso gerará um link público que você pode compartilhar com sua equipe ou outros usuários que precisem acessar sua API JSON Server.

Com a documentação criada, os usuários poderão entender facilmente como usar sua API JSON Server, ver exemplos de solicitações e respostas e obter todas as informações necessárias para interagir com sua API de forma eficaz.

- [SAIBA MAIS](https://youtu.be/aQwCwVViAik?si=XCIcg0s_V_N8ukcp)

## MAIS SOBRE O POSTMAN:
- [BAIXE O POSTMAN](https://www.postman.com/downloads/)
- [VEJA A DOCUMENTAÇÃO DO POSTMAN](https://learning.postman.com/docs/introduction/overview/)
- [COMO CRIAR DOCUMENTAÇÃO NO POSTMAN?](https://www.google.com/search?sca_esv=dccdf5943cc45056&rlz=1C1AVFC_enBR1025BR1025&sxsrf=ADLYWIJGxirxdAjxMJjnHXIJs0gyep7UYg:1717095366518&q=criar+documenta%C3%A7%C3%A3o+postman&spell=1&sa=X&ved=2ahUKEwicmffahraGAxUsr5UCHTgBBi8QBSgAegQIDhAB&biw=1094&bih=492&dpr=1.25)
- [VEJA O CURSO DE POSTMAN 22](https://youtube.com/playlist?list=PLDbrnXa6SAzUsLG1gjECgFYLSZDov09fO&si=8OEswrqCW86D5vyB)
- [VEJA O TUTURIAL BASICO DE POSTMAN](https://youtube.com/playlist?list=PLeo6Q1inqlOeC_zQMg2i3aZcGF_Jmyqd4&si=XGetKWsRXLwVgtJO)
- [VEJA TESTANDO API DO ZERO COM POSTMAN](https://youtube.com/playlist?list=PLEqTHftpM91OzKYUkpaEuByhSpJYc90Hs&si=sGGqi5NqqHr5zD2H)
- [VEJA O CURSO DE API REST VIA YOUTUBE](https://youtube.com/playlist?list=PLf8x7B3nFTl17WeEVj405tHlstiq1kNBX&si=2itotpzr-13JRAbm)
