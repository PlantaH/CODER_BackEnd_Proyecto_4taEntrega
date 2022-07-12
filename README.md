# Backend Ecommerce CODER
## _Desarrollo de ecommerce by Hernán Dupuy 2022_

## Ejecutable
https://hdcoder.herokuapp.com/

## Instalacion
Se necesita instalar [Node.js](https://nodejs.org/)

Instalar las dependencias 
```sh
npm i
npm start
```

## Dependencies
    "bcrypt": "^5.0.1",
    "dotenv": "^12.0.3",
    "express": "^4.17.1",
    "express-session": "^1.17.2",
    "log4js": "^6.3.0",
    "mongoose": "^6.0.12",
    "multer": "^1.4.4",
    "nodemailer": "^6.7.2",
    "passport": "^0.5.2",
    "passport-local": "^1.0.0",
    "socket.io": "^4.4.1",
    "twilio": "^3.73.0"

## El archivo .env requiere
* BASEDATOS 
* MONGO_CONEXION  
* SESSION_SECRET  
* TWILIO_SID 
* TWILIO_TOKEN 
* NODEMMAILER_USER 
* NODEMAILER_PASS
* AVISO_EMAIL 
* SMS_FROM 
* SMS_TO 
* WSP_FROM
* WSP_TO 
 
## Endpoints HTTP 

### Productos
	method: POST
    /api/productos ---> Alta
    {    nombre, descripcion, codigo, thumbail, precio, stock}

    method: GET
    /api/productos ---> Lista todos los productos
    /api/productos /:id ---> Lista por id 

    method: DELETE
    /api/productos /:id ---> Elimina un producto por id

    method: PUT
    /api/productos/:id ---> Modifica un item por id 
    {    nombre, descripcion, codigo, thumbail, precio, stock}
	
### Carrito
	method: POST
    /api/carrito ---> Alta
    /api/carrito/:idCarrito/:idPto ---> Alta producto al carrito
        
    method: DELETE
    /api/carrito/:id ---> Elimina un carrito
    /api/carrito/:idCarrito/:idPto ---> Elimina producto del carrito

    method: GET
    /api/carrito---> Lista todos los carritos
    /api/carrito/:id ---> Lista por id 

### Registro 
    method: POST
    /register---> alta cliente
    {   username, password, nombre, direccion, edad, telefono, avatar }
	
### Login
    method: GET
    /login ---> Lista datos cliente

    method: POST
    /login ---> valida datos cliente y conecta
    {    username, password }
 
### Logout
    method: GET
	/logout---> desconecta cliente
	 
### Ordenes
    method: GET
    /api/ordenes---> Lista todas las ordenes

    method: POST
    /api/ordenes/:idCarrito---> Alta orden con carrito 

### Chat
    method: POST
    /api/chat ---> Envio mensaje admin chat general
    { msg }

    /api/chat ---> Envio mensaje usuario chat general
    { msg }

    /api/chat/private ---> Envio mensaje usuario chat privado
    { msg }

    /api/chat/private?email=usuario ---> Envio mensaje admin chat privado

    method: GET
    /api/chat ---> Listado mensaje chat general

    /api/chat/:usuario  ---> Listado mensaje de un usuario en el chat general

    /api/chat/private ---> Listado mensaje chat privado

    /api/chat/private?email=usuario ---> Listado mensaje admin chat privado
 
