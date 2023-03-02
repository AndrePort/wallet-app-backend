<h1 align="center">👛 Wallet App API (Back-end)</h1>

<p align="center">
  This is an API created using Node.js, Express and PostgresSQL.
  The main goal is create an application that controls user finances
</p>

<br>

## Requirements

- Node.js
- Docker

Download links:
https://nodejs.org/en/download/
https://www.docker.com/products/docker-desktop/

## Documentation:

Use insomnia to import the file bellow:
https://github.com/AndrePort/wallet-app-backend/blob/master/Insomnia.json

## Steps tp run the project

1. Clone the project

```
git clone https://github.com/AndrePort/wallet-app-backend.git
```

2. Navigate to project folder and Install Dependencies

```
cd wallet-app-backend
npm install
```

3. Create an Postgres instance on Docker

```
Example:
docker run --name postgres-finances -e POSTGRES_PASSWORD=docker -e POSTGRES_USER=docker -p 5432:5432 -d -t postgres
```

4. Create a .env file following the example:

```
DB_USER=docker
DB_PASSWORD=docker
DB_NAME=finances
DB_HOST=localhost
DB_PORT=5432
```

5. Run config script tp create datebase and tables:

```
npm run config:init
Observation: If don't stop press CTRL + C
```

6. Run the project in dev version:

```
npm run start:dev
```

7. Run the project in final version:

```
npm run start
```