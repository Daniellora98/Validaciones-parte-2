# Validaciones-parte-2
Formulario con HTML CSS y JS parte 2
# Lora Jalomo Daniel Alejo Marzo 2024 

Explique los arreglos en JavaScript
Los arreglos en javascript funcionan igual que en otros lenguajes de programacion ,basicamente son una estructura de datos que nos permitiran almacenar multiples valores en una sola variable , cabe recalcar que estos valores pueden ser de distintos tipos de datos,ya sena numeros, strings, funciones etc.

Explique el almacenamiento del navegador (sessionStorage y localStorage) indique ventajas y desventajas, capacidad de almacenamiento y como accederlo utilizando java script (como almacenar, recuperar y eliminar datos)
localstorage: nos permitiran guardar o almacenar los datos en nuestro navegador, no importa si este se cierra los datos seguiran alli , la capacidad de almacenamiento es mayor en comparacion de sessionStorage, se pueden recuperar y almacenar datos
utilizando la funcion localStorage.setitam(key,value) para almacenar datos y local.storage.getItem(key,value) para recuperarlos, como bien dijimos sessionStorage los datos seran eliminados una vez se cierre el navegador

¿Qué es JSON?
JSON es basicamente un  formato que nos permitira compartir e intercambiar datos de una manera facil y ligera, facil refiriendonos a que es muy facil de leer, a comparacion a transmitir datos en binario un humano no tiene la capacidad de leerlos
tan rapidamente, en cambio un archivo JSON si lo podremos leer facilmente.  Es comúnmente utilizado para transmitir datos entre un servidor y un navegador web como una alternativa a XML. JSON se compone de pares de clave/valor y estructuras de datos anidadas, lo que lo hace muy versátil. Es nativo en JavaScript y se utiliza para serializar y deserializar datos.

¿Qué hacen las funciones JSON.parse() y JSON.stringify() ? 
JSOn.parse Convierte una cadena JSON en un objeto JavaScript. Es útil cuando recibes datos JSON desde una fuente externa, como un servidor, y necesitas convertirlos en objetos JavaScript para poder trabajar con ellos en tu aplicación.
JSON.Stringify Convierte un objeto JavaScript en una cadena JSON. Es útil cuando necesitas enviar datos desde tu aplicación a una fuente externa, como un servidor, y deseas enviar los datos en formato JSON.

¿Cómo funciona window.location.href ? es una propiedad en JavaScript que devuelve la URL de la página actual. Al asignarle un valor, puedes redirigir a otra página web. Por ejemplo, al asignarle una nueva URL, se redireccionará automáticamente a esa URL.

Explique el funcionamiento de scriptResultados.js
Este script se encarga de mostrar los datos del formulario almacenados en el almacenamiento local en la página de resultados. Primero, accede al elemento HTML donde se mostrarán los datos

Agregue un botón que borre completamente la tabla de capturas 
el codigo añadido apra eliminar las tablas de las capturas es el siguiente:
document.addEventListener("DOMContentLoaded", function() {
    const borrarTablaBtn = document.getElementById("borrarTablaBtn");
    const tablaResultados = document.getElementById("tablaResultados");
    
    borrarTablaBtn.addEventListener("click", function() {
        // Eliminar todas las filas de la tabla
        tablaResultados.innerHTML = "";
        
        // Eliminar los datos del formulario del almacenamiento local
        localStorage.removeItem("formularioData");
    });
});
