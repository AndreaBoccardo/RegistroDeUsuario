# RegistroDeUsuario
Aplicación que permitirá registrar un usuario, desarrollada en base a dos requerimientos secuenciales

Descripción Primera Parte

En el siguiente desafío se deberá construir una aplicación para dispositivos Android, con una
actividad principal de inicio de sesión, que permita ingresar un nombre de usuario, una
contraseña y simular con un botón “Ingresar” la acción, que en esta oportunidad,
limitaremos con un mensaje informativo de tipo “Usuario ingresado con éxito”. Además
debemos mostrar un logo de Desafío Latam sobre el formulario, utilizando la librería Picasso
(una de las más usadas por los desarrolladores para la carga y renderización de imágenes).

Instrucciones
1. Crear un nuevo proyecto con una actividad vacía, seleccionando lenguaje java y
versión mínima de Android API 23.
2. Crear un AVD Nexus 6 API 29 (Android Q), sobre el cual realizamos nuestras pruebas.
Esta acción puede conllevar una descarga de recursos.
3. Implementar las librerías Picasso y Material Design a través del Gradle,
asegurándonos de que nuestra aplicación compile perfectamente y además de que
nuestra aplicación inicie correctamente, visualizando la actividad inicial con el
mensaje “Hello World”.
4. Modificar el layout activity_main.xml, eliminando el TextView existente y agregando
una nueva vista de tipo ImageView, indicando un width de 0dp y un height de
‘wrap_content’, además no indicamos ningún recurso de imagen desde el archivo
layout (solo usar para pruebas de centrado). La vista debe estar centrada vertical y
horizontalmente usando los parámetros de ConstraintLayout.
5. En el archivo MainActivity.java debemos ingresar la carga de la imágen del logo de
desafío latam en su método onCreate(), con las instrucciones que da la web de
Picasso y la url dada en este ejercicio.
Recordatorio: para cargar la imágen desde una url es necesario otorgar los permisos de
acceso a internet desde el archivo AndroidManifest.xml. También deben agregar en el tag
<application , el parámetro: android:usesCleartextTraffic="true"
6. Modificar el layout activity_main.xml agregando dos vistas de tipo EditText, la
primera para indicar que se ingresa el usuario, y la segunda indicando que se ingresa
el password. Se requiere aplicar en ambas vistas los parámetros android:hint y
android:inputType, también indicar un width ‘match_parent’ y un height
‘wrap_content’. Es importante asegurarse de centrar estas vistas y ubicarlas debajo
de la imágen del logo usando los parámetros de ConstraintLayout.
7. Agregar validación de longitud máxima al campo de password desde xml con el
atributo maxLength. Modificar el layout activity_main.xml agregando una vista de
tipo Button con los parámetros width 0dp y height ‘wrap_content’, agregar el texto
“INGRESAR” al botón, cambiar su color de fondo al @color/colorPrimary, y su color
de texto a blanco. En nuestra MainActivity.java se requiere añadir una acción al hacer
click en este botón que nos muestre un mensaje usando el recurso android Toast de
tipo “Usuario ingresado con éxito”.
8. Uso de archivo strings.xml, colors.xml para parametrizar todos los textos y colores
ingresados tanto en el layout como en la clase java.

Descripción Segunda Parte
En el siguiente desafío se deberá continuar con la aplicación creada en el desafío uno para
dispositivos Android, creando en esta ocasión una nueva actividad de registro de usuarios y
una nueva actividad home, permitiendo su acceso desde la pantalla de login. Es requerido
aplicar el theme Material Design Theme.Design.
Instrucciones
Usaremos el proyecto existente del desafío anterior llamado Login Page.
1. Cambiar el tema de la aplicación en el archivo styles.xml a Theme.Design.
2. Crear nueva actividad de Registro de usuario (clase java y su respectivo layout) con
siete elementos, cuatro campos para ingresar usuario, email, contraseña,
confirmación de contraseña, un campo spinner para ingreso de la edad (entre 16 y
40) y un radio button para la selección del sexo “masculino” o “femenino”; además
de un botón para la acción registrar. Recuerda alinear todos los campos en el centro
horizontal y vertical de la pantalla con ConstraintLayout.
3. Crear nueva actividad Home (clase java y su respectivo layout) que deberá mostrar
una imagen de Android que abarque toda la pantalla, cargada con la librería Picasso
en nuestra la actividad creada y su método onCreate(). Usar ConstraintLayout.
4. Modificar la actividad y vista existente de Login, agregando un nuevo botón
“REGÍSTRESE” en la misma línea y antes del botón existente “INGRESAR”, separar
con márgenes ambos botones. En el archivo java de la actividad Login se deben
crear dos nuevas acciones, la primera al hacer click sobre el botón registrar este
debe abrir la actividad de registro, y la segunda, al hacer click sobre el botón ingresar,
este debe abrir la actividad Home.
