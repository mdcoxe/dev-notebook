# MERRNN App Cheetsheet
## Technologies
- MERN Stack
  - React & React Native
  - NodeJS
  - Express
  - MongoDB
- Dependencies
  - Cors
  - DotENV
  - Express 
  - Mongoose
  - Nodemon
  - Authentication with JWT, Bcrypt

## Setting up
- Plan out build, wireframe/user stories/white board...get the idea fleshed out before building
- Created repo in github
  - git cloned repo into proper directory
  
## Backend - Express, MongoDB, NodeJS
### File structure
  - ```mkdir backend && cd backend```
  - ```mkdir controllers models```
  - ```touch controllers/controllers.js models/models.js models/user.js```
  - ```touch .env .gitignore app.js```
  
### CLI
  - ```npm init -y```
### Dependencies
  - ```npm i dotenv cors express mongoose axios```
  - ```npm i -D nodemon```
    - Add start and dev scripts to package.json
  - ```npm i jsonwebtoken bcryptjs```

### Backend Templates
[Gist with Backend app.js w/Auth Template](https://gist.github.com/mdcoxe/8bdab6db9826a0bab331f2e65dff2f66)

[Gist with Backend controllers.js w/Auth Template](https://gist.github.com/mdcoxe/ed79626f0f87bbeb6c7a6fdea8d7a0be)

### Backend Model and Route Testing 
- Build models based on needs (Test using Postman if needed)
- Test authorization/authentication, routes and models with postman.  If successful continue onto frontend.

## Frontend - React Native/Expo, React
### File Structure/Build environment
  - Use Expo CLI to build react native file structure
  - In directory for frontend
  ```$ expo init <file name>```
  - Select template -> use blank
  - Open project in VSC/editor
  ```yarn start```
  - Yarn start opens expo window
    - On expo window, localhost:19002, run emulator/simulator/web browser to view live changes to mobile and browser environments

#### Suggested Dependencies
- react-native-paper
- react-native-elements
- @react-navigation/native
- @react-navigation/stack

#### Tips / Don't forget
- 10.0.2.2 for android
- 127.0.0.1 for iOS

