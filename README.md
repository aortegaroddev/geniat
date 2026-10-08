# Geniat API

API REST en Node.js y Express para administrar usuarios y publicaciones. Incluye registro e inicio de sesion, autenticacion mediante JWT, autorizacion por rol y persistencia con Sequelize.

## Requisitos

- Node.js 18.7.0 o compatible
- npm
- Instancia de SQL Server accesible desde la aplicacion

## Configuracion

Define en un archivo local `.env` los valores necesarios para `PORT`, `JSON_LIMIT`, `KEY`, `NAME_DATABASE`, `USER_DATABASE`, `PASSWORD_DATABASE` y `HOST_DATABASE`. No compartas ni subas credenciales. Si la base de datos aun no existe, revisa `createDatabase.sql`.

## Instalacion y ejecucion

```bash
npm install
npx sequelize-cli db:migrate
npm run dev
```

La API usa el puerto `3000` si no se define `PORT`. Los endpoints de publicaciones y usuarios estan montados bajo `/api/post` y `/api/user`; el inicio de sesion usa `/api/login`. La coleccion `Services.postman_collection.json` contiene ejemplos de solicitudes.

## Comandos

```bash
npm start
npm run dev
```

`npm run dev` inicia la aplicacion con nodemon.
