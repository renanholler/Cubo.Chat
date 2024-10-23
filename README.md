<div align="center">
  <image height="32em" src="https://img.shields.io/badge/nestjs-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" />
  <image height="32em" src="https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white"/>
  <image height="32em" src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=Vite&logoColor=white" />
  <image height="32em" src="https://shields.io/badge/react-black?logo=react&style=for-the-badge" />
  <image height="32em" src="https://img.shields.io/badge/Tailwind_CSS-grey?style=for-the-badge&logo=tailwind-css&logoColor=38B2AC" />
</div>

<img width="1896" alt="capa" src="https://github.com/user-attachments/assets/71c7d4e4-90d4-40d0-af9e-655445ab9acb">

## Instalação

Após clonar o repositório principal, será necessário instalar as dependências tanto do backend quanto do frontend.

### Clonar o Repositório

Primeiro, clone o repositório:

```bash
  git clone <url-do-repositorio>`
  cd <nome-do-repositorio>`
```

### Submódulos

Os subprojetos são versionados como submódulos neste repositório. Para baixar o conteúdo completo, execute o seguinte comando:

```bash
  git submodule update --init --recursive
```

## Configuração Backend

O backend utiliza **NestJS** e **Prisma** como ORM para interagir com o banco de dados. Siga os passos abaixo para configurá-lo:

### 1. Instalar Dependências

Entre na pasta do backend e instale as dependências:

```bash
  cd backend/
  npm install
```

### 2. Configurar Variáveis de Ambiente

Renomeie o arquivo `.env.example` para `.env`.

### 3. Rodar Migrations e Seed

Para garantir que o banco de dados esteja atualizado, execute as migrations e a seed:

```bash
  npx prisma migrate dev
```

Se verificar que a seed não foi rodada automaticamente, pode rodar assim:
```base
  npx prisma db seed
```

## Configuração Frontend

O frontend utiliza **Vite** para desenvolvimento. Siga os passos abaixo para configurá-lo:

### 1. Instalar Dependências

Entre na pasta do frontend e instale as dependências:

```bash
  cd frontend/
  npm install
```

### 2. Solucionar Problemas de Dependências (se necessário)

Se você estiver utilizando um Mac com arquitetura ARM (Apple Silicon), pode ser necessário rodar o seguinte procedimento para corrigir problemas com dependências opcionais:

1. Remova a pasta `node_modules` e o arquivo `package-lock.json`.
2. Limpe o cache do npm com o comando `npm cache clean --force`.
3. Reinstale as dependências com `npm install`.

## Rodando os Projetos

### Backend

Para rodar o servidor backend em modo de desenvolvimento:

```bash
  cd backend
  npm run start:dev
```

### Frontend

Para rodar o servidor frontend em modo de desenvolvimento:

```bash
  cd frontend
  npm run dev
```

## Conclusão

Todo esse procedimento será automatizado usando docker-compose, mas pelo tempo da entrega foi organizado esse README.
