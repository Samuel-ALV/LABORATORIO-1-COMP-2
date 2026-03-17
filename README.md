Explique con sus propias palabras qué es Vue.js y cuál es su función dentro de la
página web desarrollada.
R// vue.js es un framework de javaScript que se utiliza para crear interfaces
graficas dinamicas y reactivas en este proyecto lo utilizamos para manejar los datos de la plataforma 
y para cear una interfaz de usuario interactiva


o Describa qué variables reactivas utilizó en su aplicación y cuál es la función de
cada una dentro del sistema.
R//En nuestra aplicacion utilizamos variables 
-nuevaActividad: almacenar el texto ingresado por el usuario  
-error:muestra mensajes de validacion
-Actividades:lista de actividades ingresadas por el usuario
completadas:estado de las actividades ingresadas por el usuario
-index:posicion de cada actividad en la lista de actividades

o Explique la diferencia entre las siguientes directivas utilizadas en su proyecto: v-
bind y v-model
R//v-bind se enlaza a un atributo de un elemento HTML y actualiza su valor dinámicamente, mientras que v-model se utiliza para crear una vinculación bidireccional entre un elemento de
 formulario y una variable reactiva en Vue.js, lo que permite que los cambios en el formulario actualicen automáticamente la variable y viceversa.
   - v-model: crea un enlace bidireccional entre un input y una variable reactiva.  

 


o Mencione al menos un ejemplo de evento utilizado dentro de su aplicación.
R// El evento @click="agregar" se utiliza para llamar a la función "agregar" cuando el usuario hace clic en el botón "Agregar". Esta función se encarga de agregar 
 una nueva actividad a la lista de actividades ingresadas por el usuario.


o Explique para qué utilizó la directiva v-for dentro de su aplicación.
R// Se utiliza para recorrer la lista de act
ividades ingresadas por el usuario y mostrar cada una de ellas en la interfaz de usuario.
 Permite generar dinámicamente elementos HTML basados en los datos de la lista, facilitando la visualización de las actividades sin necesidad de escribir código repetitivo para cada una.

o Describa en qué situación utilizó v-if y qué problema resuelve dentro de su
interfaz.
R//Se usa para mostrar un mensaje de error cuando el usuario intenta agregar una actividad 
sin ingresar texto. Resuelve el problema de proporcionar retroalimentación visual al usuario sobre la validez de su 
entrada, mejorando la experiencia del usuario al indicar claramente cuándo se ha cometido un error.



o Explique cómo se realiza la validación de datos en su aplicación y por qué es
importante validar la información ingresada por el usuario.
R// Se valida que el campo de texto no esté vacío antes de agregar una nueva actividad a la lista.
 Si el campo está vacío, se muestra un mensaje de error utilizando la variable reactiva "error".
  Es importante validar la información ingresada por el usuario para garantizar que los datos sean 
  correctos y evitar problemas en la funcionalidad de la aplicación, así como para mejorar la experiencia
   del usuario al proporcionar retroalimentación inmediata sobre cualquier error en su entrada.
