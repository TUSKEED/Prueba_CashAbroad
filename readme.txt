Para poder realizar esta prueba técnica hicimos uso de node.js, express y npm.

En caso de error instalar las dependencias previamente mencionadas

Node.js desde su página oficial:
https://nodejs.org/en/download/current

Instalamos npm en visual con el siguiente comando: npm install 
definimos que es un proyecto node.js con el comando: npm init, dejamos todo de manera default y lo definimos de tipo module dentro del package.json

y por ultimo instalamos express con el comando: npm install express


Una vez tenemos todas las dependencias corremos nuestra api en la terminal con el comando:
node index.js

Para probar la api hacemos uso de la herramienta postman y creamos una colección, dentro de la colección creamos una solicitud de tipo post y le asignamos el siguiente endpoint, ya que es donde se realiza el cambio de divisa.

localhost:3000/cambio

Dentro del apartado body seleccionamos la opción raw y en formato json 

y enviamos el objeto con el la moneda y cantidad que deseamos convertir, enviamos y la api nos responderá con la conversión.

Ejemplo de como enviar el objeto:

1.- 	{	
  	    "mxn": 20
	}
2.- 	{
	    "usd": 40
	}
Enviamos únicamente una moneda, si enviamos las 2 nos responderá con un error.
