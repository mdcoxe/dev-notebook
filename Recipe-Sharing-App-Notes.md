# Recipe Sharing App
## Technologies
- MERN Stack
  - React & React Native
  - NodeJS
  - Express
  - MongoDB
- Dependencies
  - Axios
  - Cors
  - DotENV
  - Express 
  - Mongoose
  - Nodemon
  - Authentication with JWT, Bcrypt

## Setting up
- Created repo in github
  - git cloned repo into proper directory
  
### Backend
- File structure
  - ```mkdir backend && cd backend```
  - ```mkdir controllers models```
  - ```touch controllers/controllers.js models/models.js models/user.js```
  - ```touch .env .gitignore app.js```
  
- CLI
  - ```npm init -y```
- Dependencies
  - ```npm i dotenv cors express mongoose axios```
  - ```npm i -D nodemon```
    - Add start and dev scripts to package.json
  - ```npm i jsonwebtoken bcryptjs```

[Gist with Backend app.js w/Auth Template](https://gist.github.com/mdcoxe/8bdab6db9826a0bab331f2e65dff2f66)

[Gist with Backend controllers.js w/Auth Template](https://gist.github.com/mdcoxe/ed79626f0f87bbeb6c7a6fdea8d7a0be)
