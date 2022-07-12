# Backend Ecommerce
## _Una API RESTFULL que nos brinda el backend para un ecommerce_

## Tecnologia
#### Backend
- NodeJS - Version 14.17.6 o superior 
- express - Version 4.17.1
- express-session - Version 1.17.2
- passport - Version 0.5.2
- passport-local - Version 1.0.0
- bcrypt - Version 5.0.1
- mongoose - Version 6.0.12
- log4js - Version 6.3.0
- multer - Version 1.4.4
- socket.io - Version 4.4.1
- nodemailer - Version 6.7.2
- twilio - Version 3.73.0
- dotenv - Version 12.0.3

## Instalacion

Esta app require [Node.js](https://nodejs.org/)

Instalar las dependencias antes de inicar el servidor, en el achivo DB podras encontrar una base de datos simples para poder probar
```sh
npm i
npm start
```

## El archivo .env requiere
- USERPASSMONGO = 'Usuario y password para MongoDB SAAS'  
- NODE_ENV = 'El entorno de desarollo en el que iniciara el servidor, puede ser test, development ó production'  
- SESSION_SECRET = 'Una palabra secreta para las sesiones'  
- NODEMMAILER_USER = 'Un email de gmail'  
- NODEMAILER_PASS = 'La contraseña del mail'
- TWILIO_SID = 'sid de twilio'
- TWILIO_TOKEN = 'token de twilio'

## Documentacion
https://documenter.getpostman.com/view/17626076/UVsJxSwD#854444aa-2164-4a62-8a7a-48f822ecd6cd
- En la documentacion podran ver ejemplos de los endpoints

## Deploy
 
