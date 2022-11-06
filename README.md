# API Wallink

Authors : Yumi & Megafredo

## Introduction

This API is made with love to bring all our favorite links together.

## Technologies

🖥️ Code editor :

- [VS Codium](https://vscodium.com/) (open source)

⚙️ Back end

- NodeJS
- Express
- Typescript

🎞️ Database

- PostgreSQL (DBSM)
- PgAdmin4 (GUI)

🪂 Versioning

- Git & GitHub
- Sqitch for database

🎨 Front end

- Not decided yet...

🧮 Agile Method

- Brainstorming tldraw
- Kanban GitHub project

📄 Documentation

- Swagger UI with swagger express

## Project

The idea of this application comes because who doesn't add a favourite link in a bookmark ? And how many bookmarks do you have ?

For us, so many. This simple app was first for us, and hope that it will be useful for you !

## How to launch the application ?

First, clone the repository

```sh
git clone <ssh link>
```

Then, install the packages needed for the application

```sh
npm install
# or npm i
```

Add `.env` file and configure your database :

```sh
#INFO CONNEXION DB FOR PSQL new Client()
PGHOST=#
PGDATABASE=#
PGUSER=#
PGPASSWORD=#
PGPORT=5432
```

And add all the **environment variables** needed for the application :

```sh
#SESSION
SESSION_SECRET=#

#JWT
#Generate random token :
#launch node and copy
#require("crypto").randomBytes(64).toString("hex")
ACCESS_TOKEN_SECRET=#
REFRESH_TOKEN_SECRET=#

# DEBUG
DEBUG=EntryPoint,Pool,ErrorHandling,Controller,Jwt,Schema

#MAILER
USER_MAILER=
PASSWORD_MAILER=

```

And then, you can run the application with the following command

```sh
npm run dev
```

And if you want to see the documentation, launch the app and add at the end of url `/api-docs`

```sh
http://localhost:<PORT>/api-docs
```

---

## Sources

Project conception :

- [tl;draw](https://www.tldraw.com/) => drawings for brainstorming
