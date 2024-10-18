# Variables de Entorno
### ¿Qué son las variables de entorno
# COMPLETAR

### Para crear un contenedor con variables de entorno?

Las variables de entorno son pares clave-valor que se utilizan para configurar el entorno en el que se ejecuta una aplicación. Estas variables permiten personalizar el comportamiento de los programas sin necesidad de cambiar el código. En Docker, las variables de entorno se utilizan para pasar parámetros de configuración a los contenedores.

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

![alt text](image-5.png)

### Crear un contenedor con mysql:8 , mapear todos los puertos

![alt text](image-6.png)

### ¿El contenedor se está ejecutando?
NO
![alt text](image-7.png)

### Identificar el problema

Debido a que no especificamos las variables de inicio

### Eliminar el contenedor creado con mysql:8 

![alt text](image-8.png)

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo


![alt text](image-9.png)

### ¿Qué bases de datos existen en el contenedor creado?

![alt text](image-10.png)