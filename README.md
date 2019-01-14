# Formulario
En esta práctica hemos creado un formulario y una pagina de login.

#Creacion del formulario:
Hemos creado un formulario con una serie de campos obligatorios como: Nombre, Apellido, Fecha Contrato, Salario, contraseña y confirmacion de contraseña. El resto de campos son opcionales.
La estructura del formulario la hemos implementado en HTML5 y con CSS para poder darle estilo.

---1. Requisitos---:

Uno de los requisitos de la practica es validar los datos introducidos por el usuario. Para ello utilizamos restricciones que nos proporciona HTML5 con las etiquetas pattern y type junto a la funciones que hemos creamos en JavaScritp.

Para validar los diferentes campos obligatorios primero deben de pasarlo por los filtros del pattern y type del HTML. Tambien hemos añadido el campo required para que el usuario no se deje ningun campo obligatorio sin rellenar. En el caso de los campos obligatorios se comprueban con los pattern y las funcions de JS.

Para las validaciones del JS consiste en crear un input dandole un nombre al id para poder crear un evento al escribir con el teclado (keyup), para comprobar si cumple la expresion regular. En el caso de no cumplirla saltará un mensaje de error al enviar dicho formulario o un mensaje debajo de cada campo diciendo el porqué. Solo se mandará el formulario si todos los campos obligatorios estan rellenos.

Para los campos trabajos y jefes hemos creado un array con dicho valores y despues los hemos cargado en una lista con selectores.

Para la creacion de las contraseñas lo primero que tiene que hacer es cumplir los requisitos y despues, la contraseña de confirmacion sea igual que la primera que has metido, por el caso contrario saltará un error.

---2. Funcionalidad Cookies---

-Cookie de usuario:
	Para la creacion de las cookies hemos creado una funcion llamada setCookie que recibe el nombre,contraseña y un valor numerico para saber el tiempo en el que se borrara la cookie. Llamamos a dicha funcion cuando hemos comprobado todos los datos del formulario son correctos y le damos al boton de "enviar" para poder redirigirte a la pagina del Login.

-Cookie de sesion:
	Para la creacion de la cookie de sesion llamamos a un condicion para que compruebe que el nombre que ha obtenido de la cookie sea igual a la contraseña introducida por el usuario. Si todo va bien llama a la funcion setCookie y crea la cookie de sesion junto a un mensaje que ha ido todo correctamente con un boton de cerrar sesion que solo aparecerá si todo ha ido correctamente. En el caso de que no puedas loguearte aparecera un mensaje de error.

-Borrado Cookie sesion:
	Cuando le demos al boton de cerrar sesión llamaremos a la función logoutSesion(), que cambia la fecha de expiración a la fecha unix y asi permite borrar la sesion de la cookie.
