Objetivo del proyecto: Crear una tienda online completa(front y backend) con la finalidad de mostrar productos basado en busqueda y filtros.


Las Caractericas de la aplicacion: 
* Frontend simple que despliega productos por busqueda dinamicamente
[Link del Demo](http://front-ecommerce-test.s3-website-us-east-1.amazonaws.com/)

## Tecnologias-Librerias-usadas
Frontend :
* [Vanilla.js](http://vanilla-js.com/)
* [HTML](https://developer.mozilla.org/es/docs/Web/HTML)
* [CSS](https://developer.mozilla.org/es/docs/Web/CSS)
* [Jquery](https://jquery.com/)
* [Axios](https://axios-http.com/docs/intro)

CI/CD Frontend:
Estoy integrando integrancion continua(CI/CD) a un bucket s3 de aws, no me detengo a explicar los pasos para integrar CI/CD  a  s3 de aws porque me explayaria bastante, 
Git Actions nos permite ejecutar entornos de prueba y manejar deployments automatizados con criterios que podemos definir , en este caso no necesito ejecutar casos de prueba,
Entonces cada vez que mando un commit a la rama main, el script [main.yml](./.github/workflows/main.yml) ejecutara el workflow para subir nuestro directorio a un bucket de aws,
se tiene que configurar la cuenta aws para permitir la integracion de Git Actions.

* [Git Actions](https://docs.github.com/es/actions)
* [IAM](https://aws.amazon.com/es/iam/)

## Deploy
Frontend: En El front es simple y directo , No se esta manejando ningun framework para el frontend asi que no hay requisitos para ejecutar,
Unicamente debes apuntar correctamente al index.html en el entorno que estes ejecutando

### Structura directorio Front

##|Directorio o Archivo | Descripcion
---|---|---
0|[apicalls](./front/apicalls)| Este Directorio Contiene toda la logica de los apicalls a nuestra api
1|[galery](./front/galery)| Este Directorio contiene imagenes que usa nuestra app
2|[js](./front/js)| En este Directorio tenemos funciones de utilidad 
3|[src](./front/src)| En este Directorio tenemos todas nuestas paginas html 
4|[styles](./front/styles)| Este Directorio contiene todo nuestros archivos css
4|[index.html](./front/index.html)| Nuestra pagina inicial
