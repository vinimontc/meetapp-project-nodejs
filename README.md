# MeetApp - Aplicação para organização de Meetup's

Aplicação criada do zero utilizando Express e Node.js que tem como conceito, ser um app agregador de eventos para desenvolvedores chamado Meetapp (um acrônimo à Meetup + App).

Ferramentas e tecnologias utilizadas: 

- Sucrase + Nodemon;
- ESLint + Prettier + EditorConfig;
- Sequelize (com PostgresSQL);
- Para a realização de testes e administração de ambientes foi utilizado a plataforma Docker;
- Para a autenticação do usuário que é o foco da primeira parte do sistema foi utilizado o JWT (JavaWebToken);
- Bcryptjs para criptografia de senha do usuário;
- Youch para tratativa dos erros de uma forma mais detalhada;
- Sentry para a análise dos erros em ambiente de produção;
- Bee-Queue e banco de dados Redis (por conta da performance do mesmo) para a tratativa de filas;
- Nodemailer para o uso da funcionalidade de emails;
- Banco de dados MongoDB para trabalhar com as notificações que são dados que não necessitavam de muitas informações detalhadas salvas no banco;

## Funcionalidades - 1° PARTE

Abaixo estão descritas as funcionalidades que foram adicionadas na primeira parte do projeto.

### Autenticação

Permite que um usuário se autentique na aplicação utilizando e-mail e senha.

### Cadastro e atualização de usuários

Permite que novos usuários se cadastrem na aplicação utilizando nome, e-mail e senha. 
E também permite a alteração desses dados, nome, e-mail e principalmente a senha, onde é solicitado uma confirmação de nova senha e senha atual.

## Funcionalidades - 2° PARTE

Abaixo estão descritas as funcionalidades que foram adicionadas na segunda parte do projeto.

### Gerenciamento de arquivos

Rota para upload de arquivos que cadastra em uma tabela o caminho e nome do arquivo e retorna todos dados do arquivo cadastrado.

### Gerenciamento de meetups

O usuário pode cadastrar meetups na plataforma com título do meetup, descrição, localização, data e hora e imagem (banner). Todos campos são obrigatórios.

Não é possível cadastrar meetups com datas que já passaram.

O usuário também pode editar todos os dados de meetups que ainda não aconteceram e que ele é organizador.

Há uma rota para listar os meetups que são organizados pelo usuário logado.

O usuário também pode cancelar meetups organizados por ele e que ainda não aconteceram. 

### Inscrição no meetup

O usuário só pode se inscrever em meetups que não organiza.

O usuário não pode se inscrever em meetups que já aconteceram.

O usuário não pode se inscrever no mesmo meetup duas vezes.

O usuário não pode se inscrever em dois meetups que acontecem no mesmo horário.

Sempre que um usuário se inscrever no meetup, um e-mail é enviado ao organizador contendo os dados relacionados ao usuário inscrito.

### Listagem de meetups

Rota para listar os meetups com filtro por data, os resultados dessa listagem so retornados com paginação em 10 itens por página.

### Listagem de inscrições

Rota para listar os meetups em que o usuário logado está inscrito.

É listado apenas meetups que ainda não passaram e são ordenadas pelas meetups mais próximos como primeiros da lista.

## Observações

- Aplicação feita com base no conteúdo estudado no GoStack 8.0 da RocketSeat;
- Link para o desafio do curso referente a primeira parte dessa aplicação: <https://github.com/Rocketseat/bootcamp-gostack-desafio-02>

- Link para o desafio do curso referente a segunda parte dessa aplicação: <https://github.com/Rocketseat/bootcamp-gostack-desafio-03>
