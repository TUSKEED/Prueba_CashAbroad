Para poder realizar esta prueba técnica hicimos uso de node.js, express y npm.

En caso de error instalar las dependencias previamente mencionadas

Node.js desde su página oficial:
https://nodejs.org/en/download/current

Instalamos npm en visual con el siguiente comando: npm install 
definimos que es un proyecto node.js con el comando: npm init, dejamos todo de manera default y lo definimos de tipo module dentro del package.json

y por ultimo instalamos express con el comando: npm install express


Una vez tenemos todas las dependencias corremos nuestra api en la terminal con el comando:
node index.js

Para probar la api hacemos uso de la herramienta postman y creamos una colección, dentro de esta colección creamos dos solicitudes de tipo post, la primera solicitud es para llevar acabo el login y poder generar el token para necesario para la verificación.
Asignamos el siguiente endpoint: 
localhost:3000/login
En el apartado de body seleccionamos la opción raw y definimos que será JSON
ingresamos un objeto que tendrá como unica clave el usuario.
ejemplo: 
{
   "username": "Antonio"
}

Sino nos marca error nos responderá con el token, lo copiamos y entramos en la siguiente solicitud para probar las rutas protegidas
le asignamos el siguiente endpoint, ya que es donde se realiza el cambio de divisa.
localhost:3000/cambio
En el apartado de headers agregamos una nueva key llamada
*Authorization y en el valor escribiremos Bearer separado por un espacio pegamos el toke copiado en la solicitud anterior y nos
redireccionamos al apartado body, es este apartado seleccionamos la opción raw y en formato json 

y enviamos el objeto con el la moneda y cantidad que deseamos convertir, enviamos y la api nos responderá con la conversión.

Ejemplo de como enviar el objeto:

1.- 	{	
  	    "mxn": 20
	}
2.- 	{
	    "usd": 40
	}
Enviamos únicamente una moneda, si enviamos las 2 nos responderá con un error.
