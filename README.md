# MeetApp - Iniciando a aplicação

Aplicação criada do zero utilizando Express que tem como conceito, ser um app agregador de eventos para desenvolvedores chamado Meetapp (um acrônimo à Meetup + App).

Ferramentas e tecnologias utilizadas: 

- Sucrase + Nodemon;
- ESLint + Prettier + EditorConfig;
- Sequelize (com PostgresSQL);
- Para a realizaço de testes e administração de ambientes foi utilizado a plataforma Docker;
- Para a autenticação do usuário que é o foco dessa primeira parte do sistema foi utilizado o JWT (JavaWebToken);
- Bcryptjs para criptografia de senha do usuário;

## Funcionalidades

Abaixo estão descritas as funcionalidades que foram adicionadas nessa primeira parte do projeto.

### Autenticação

Permite que um usuário se autentique na aplicação utilizando e-mail e senha.

### Cadastro e atualização de usuários

Permite que novos usuários se cadastrem na aplicação utilizando nome, e-mail e senha. 
E também permite a auteração de dados como nome, e-mail e principalmente a senha, onde é solicitado uma confirmação de nova senha e senha atual.

## Observações

- Aplicação feita com base no conteúdo estudado no GoStack 8.0 da RocketSeat;
- Link para o desafio do curso referente a essa aplicação: <https://github.com/Rocketseat/bootcamp-gostack-desafio-02>
