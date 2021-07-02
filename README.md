Esse repositório é apenas um exemplo de servidor backend (NodeJS) que permite fazer a autenticação com JWT, ele está sendo usado para testar o sistema de autenticação
na poc-micro-frontend.

# Instalação
1. Fazer o clone do repositório
2. Abrir o terminal na pasta do projeto
3. Executar o comando `yarn`

# Iniciar o servidor
Para rodar o servidor na porta padrão `3333`, execute o comando abaixo:
```
yarn dev
```

## Configurações

### Alterar os usuários que estão cadastrados
1. No arquivo `database.ts` na função `seedUserStore`, basta adicionar ou alterar os usuários já cadastrados

### Alterar a duração para o token ser expirado
1. No arquivo `auth.ts`, alterar o atributo `expireIn` que está dentro da variável token":
```
const token = jwt.sign(payload, auth.secret, {
  subject: email,
  expiresIn: 5, // Duração em segundos (5s)
});
```

### Alterar a porta do servidor
1. No arquivo `server.ts`, editar a última linha:
```
app.listen(3333); // Trocar 3333 pela porta desejada
```






