**Para Grado Superior, Introducción a Node.js**

*const http = require('http');* 
Node.js utiliza el sistema de módulos CommonJS y la función require le permite implementar varios módulos en el archivo donde se utiliza. En esta línea, importamos el módulo http de Node.js al código y lo llamamos http. ¡Nota! También es posible utilizar palabras clave de importación y exportación de ES6 con Node.js
*const port = 3000;*
Definimos un puerto llamado constante. El valor 3000 es el puerto del servicio web.

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain'); 
  res.end('Hola Mundo');
});

El módulo http proporciona un método createServer que crea un servidor web y devuelve un objeto que almacenamos en una variable llamada server. El método createServer toma como argumento una función de devolución de llamada que se llama cada vez que el usuario realiza una solicitud al servidor web. Esta función toma dos argumentos: req (solicitud) y res (respuesta). Dentro de la función de escucha, definimos el contenido de la respuesta que se enviará de vuelta. El estado (statusCode) como 200 y el encabezado de respuesta (setHeader). Finalmente, utilizamos el método final de la respuesta para enviar la respuesta y establecer su contenido en el texto Hola Mundo.

server.listen(port, () => {
  console.log('Server is running at port' + port);
});

El objeto de servidor tiene un método de escucha (listen) que inicia el servidor y escucha las solicitudes de red en el puerto 3000.

server.listen(port, host, () => {
  console.log('Server is running at port ' + port);
});

De forma predeterminada, siempre debes reiniciar el servicio si realizas cambios en el código fuente. Más adelante usaremos nodemon, que lo hará automáticamente cuando se actualice el código fuente. También puede especificar el servidor en el método listen(). Cuando ejecuta un servicio web en tu maquina, el servidor es localhost.



