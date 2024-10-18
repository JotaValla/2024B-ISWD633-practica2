## Esquema para el ejercicio
![Imagen](img/esquema-ejercicio5.PNG)

### Crear la red

![alt text](image-18.png)

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias

![alt text](image-19.png)

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias

![alt text](image-20.png)
De acuerdo con el trabajo realizado, en la el esquema de ejercicio el puerto a es **(completar con el valor)**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
![alt text](image-21.png)

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
![alt text](image-22.png)
### Eliminar el contenedor wordpress
![alt text](image-23.png)

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
Cuando recreas el contenedor de WordPress, se pierde la configuración y las publicaciones que hiciste, ya que el contenedor se creó de nuevo desde cero sin ningún dato persistente. Esto significa que tendrás que volver a realizar la configuración inicial y crear las publicaciones nuevamente, a menos que estés utilizando un volumen para persistir los datos de WordPress.





