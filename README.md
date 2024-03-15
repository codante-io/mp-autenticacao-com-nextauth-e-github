# Autenticação com NextAuth.js e GitHub

Você está desenvolvendo um novo App, que tem a habilidade de fazer um _analytics_ no GitHub de seus usuários. Essa aplicação é "passwordless", ou seja, faz a autenticação do usuário apenas utilizando o OAuth do github.com. Experimente o poder - e a facilidade - de um sistema de login com NextAuth.js utilizando o GitHub para autenticação em uma aplicação Next.js.

## 🔨 Requisitos

- Utilize o Next.js e claro, NextAuth.js para a autenticação.
- Crie uma Landing Page para sua aplicação que contenha um botão de login com o GitHub.
- Crie a página que o usuário será redirecionado após a autenticação (página logada).
	- Essa página deverá exibir informações básicas da conta do GitHub do usuário - incluindo nome e avatar.
 	- Essa página deverá exibir um botão de _logout_. 
- O usuário deverá ser redirecionado para a Landing Page nos seguintes casos:
	- Falha na autenticação
 	- Usuário deslogado tentando acessar a página logada
  	- Após o logout

> [!Tip] 
> Obs. será necessário criar um _App OAuth_ no GitHub.  
> Obs1. A estratégia de login do NextAuth deverá ser a de `jwt` (e não `database`). Isso significa que as informações do usuário logado serão persistidas no token, e não na base de dados. 


### Criando um App OAuth no GitHub:
- A página de Apps OAuth está [nesse link](https://github.com/settings/developers)
- Veja detalhes nesse [guia do GitHub](https://docs.github.com/pt/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app)

### Informações adicionais do GitHub

Por padrão o NextAuth.js traz apenas algumas informações do usuário na sessão: _name_, _image_, _email_. 
Mas ao analisarmos o figma do nosso projeto, algumas informações adicionais são necessárias, como quantidade de repositórios, gists e seguidores. 
Para que você consiga acessar essas informações será necessário utilizar as _callbacks_ do NextAuth.js. Mais [infos aqui](https://next-auth.js.org/configuration/callbacks).

## 🎨 Design Sugerido

Temos uma sugestão de design no Figma. Entretanto, fique à vontade para montar a aplicação conforme a sua criatividade.

### Figma

🔗 [Link do design](https://www.figma.com/community/file/1337488395640254170/mini-projeto-autenticacao-com-nextauth-e-github)

## 👉🏽 Sobre esse mini-projeto

### O que você irá praticar:

#### Http e Internet
- Sessão
- Cookies
- Protocolo OAuth2

#### Next.js

- NextAuth.js
- Login e Logout usando NextAuth.js
- Habilidade 2

### Pré requisitos

- Conhecimentos básicos de React
