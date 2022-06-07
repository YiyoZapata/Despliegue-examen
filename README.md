### Despliegue-examen

# Introducción

Vamos a desplegar nuestra app a traves de docker-compose, creando nuestra imagen, y subiendola en dockerhub.

# Configuración del yaml
 
Para ello primero debemos rellenar nuestro archivo docker compose con los volumenes e imagenes necesarios que requiera nuestra app.

Primero rellenamos el volumen el nombre de la imagen para arrancar nuestra base de datos.


![Captura de pantalla de 2022-06-07 19-47-21](https://user-images.githubusercontent.com/100800688/172449403-0328fc4c-e602-4d85-aa53-bd09a06ffc29.png)


Segundo volumen para nginx :


![Captura de pantalla de 2022-06-07 19-47-55](https://user-images.githubusercontent.com/100800688/172449540-87aabd37-11f2-4abb-874b-781b8c2e778c.png)


En tercer lugar otro volumen para nuestro servidor, en nuestro caso usamos java asi que nos va bien hacer correr tomcat.


![Captura de pantalla de 2022-06-07 19-48-07](https://user-images.githubusercontent.com/100800688/172449926-3445f20f-390f-4f6d-a62d-4dd8cff7bbdd.png)


Una vez tengamos nuestro archivo docker-compose.ymal lo siguiente sera crear un archivo docker con la imagen de nuestro servidor.

# Dockerfile


![Captura de pantalla de 2022-06-07 19-55-25](https://user-images.githubusercontent.com/100800688/172450501-fb1bb4d2-708b-456b-9c7f-bf6c4b743515.png)


Tomcat requiere de más archivos que son de tipo xml para poder arrancarlos.


![Captura de pantalla de 2022-06-07 19-58-00](https://user-images.githubusercontent.com/100800688/172450884-bbd8ed43-acba-43d5-9318-96cc57b9fb05.png)

![Captura de pantalla de 2022-06-07 19-58-12](https://user-images.githubusercontent.com/100800688/172450893-b548caec-81c5-4349-a453-a5880c184b2f.png)


Ya tenemos los volumenes y archivos necesarios para poder desplegar nuestra aplicación pero por supuesto debemos tener también incluidos en un mismo local junto a los archivos anterioros el código de nuestra app (fronted, backend, sql...)

Una vez tengamos todo ejecutamos el comando docker up para correr el contenedor

![Captura de pantalla de 2022-06-07 20-32-43](https://user-images.githubusercontent.com/100800688/172456935-2d282071-b6fc-4367-8f2e-cee972e033d6.png)

Hacemos un docker-compose ps para comprobar

![Captura de pantalla de 2022-06-07 20-34-58](https://user-images.githubusercontent.com/100800688/172457183-86edad3a-e5b0-4a5d-bd07-e09b6cf3ad76.png)

Ahora vamos a subir la imagen de nuestro proyecto. Para ello ejecutamos primero docker login docker build y docker push

# Preparacion para la subida de imagen.

![Captura de pantalla de 2022-06-07 21-06-20](https://user-images.githubusercontent.com/100800688/172462402-883e70ae-431e-4797-b4bb-33b84b1ce669.png)

![Captura de pantalla de 2022-06-07 21-07-54](https://user-images.githubusercontent.com/100800688/172462894-f76e0342-4de1-4716-afbb-2fb2c872186a.png)

Ultimo paso: docker push yiyozapata/nombre imagen.

![Captura de pantalla de 2022-06-07 21-12-52](https://user-images.githubusercontent.com/100800688/172463538-2cb4e74e-4ab0-42d7-a2a4-323377617252.png)

![Captura de pantalla de 2022-06-07 21-15-26](https://user-images.githubusercontent.com/100800688/172463888-41eeb7cf-638a-42f1-9f3a-6c0b2c64ef80.png)

Asi queda la aplicación corriendo con docker-compose.

![Captura de pantalla de 2022-06-07 21-21-59](https://user-images.githubusercontent.com/100800688/172465075-52ec7333-079e-41b7-a7b2-5047afdf06b1.png)



## Anexo

Link de mi dockerhub :

https://hub.docker.com/repository/docker/yiyozapata/9-jdk16-openjdk











 
