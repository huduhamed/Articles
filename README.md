# Articles

Full-stack Articles app (React + Redux on the front end, Node/Express + MongoDB on the back end) that implements authenticated CRUD for posts, search, tags, pagination and Google sign-in.

## Tech stack

![React.js](https://img.shields.io/badge/React.js-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Redux](https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)
![Material UI](https://img.shields.io/badge/Material_UI-0081CB?style=for-the-badge&logo=material-ui&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)

## Key features

- User signup / signin with JWT (and Google sign-in integration)
- Create, read, update and delete posts (CRUD)
- Search posts by text and tags
- Pagination for post lists
- Commenting endpoint and optimistic UI updates
- Protected API routes for authenticated actions

## Project structure

- client/ — React app (Redux, Axios, Material UI)
- server/ — Express API (routes, controllers, models) and Mongoose for MongoDB

## Getting started (developer setup)

Note: client and server are independent. Run them in separate terminals.

1. Clone the repo

   git clone https://github.com/huduhamed/Articles.git
   cd Articles

2. Server (API)

   cd server
   npm install

   Create a `.env` file inside the `server/` folder with the following values:

   MONGODB_URL=
   PORT=

   Start server:
   npm start

3. Client (UI)
   cd ../client

   npm install
   npm start

## Useful tips & troubleshooting

- If you see an error about `MONGODB_URL` being undefined, make sure a `.env` exists in `server/` and includes `MONGODB_URL`.
- For Atlas access, ensure your IP is whitelisted in the network access settings or use the appropriate connection rules for your environment.
-
- Quick API check (after server starts):
  curl http://localhost:5000/posts

## Screenshot

![Posts page](client/src/images/readMe.png)

## Next steps

- Add automated tests (Jest) for key API endpoints and component tests for UI.
- Add CI pipeline and a deploy script (Netlify/Vercel for client, Heroku/Render for server or Docker-based deployment).
