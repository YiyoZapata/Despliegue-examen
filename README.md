# Despliegue-examen

Vamos a desplegar nuestra app a traves de docker-compose.
 
Para ello primero debemos rellenar nuestro archivo docker compose con los volumenes e imagenes necesarios que requiera nuestra app.

Primero rellenamos el volumen el nombre de la imagen para arrancar nuestra base de datos.


![Captura de pantalla de 2022-06-07 19-47-21](https://user-images.githubusercontent.com/100800688/172449403-0328fc4c-e602-4d85-aa53-bd09a06ffc29.png)


Segundo volumen para nginx :


![Captura de pantalla de 2022-06-07 19-47-55](https://user-images.githubusercontent.com/100800688/172449540-87aabd37-11f2-4abb-874b-781b8c2e778c.png)


En tercer lugar otro volumen para nuestro servidor, en nuestro caso usamos java asi que nos va bien hacer correr tomcat.


![Captura de pantalla de 2022-06-07 19-48-07](https://user-images.githubusercontent.com/100800688/172449926-3445f20f-390f-4f6d-a62d-4dd8cff7bbdd.png)


Una vez tengamos nuestro archivo docker-compose.ymal lo siguiente sera crear un archivo docker con la imagen de nuestro servidor.


![Captura de pantalla de 2022-06-07 19-55-25](https://user-images.githubusercontent.com/100800688/172450501-fb1bb4d2-708b-456b-9c7f-bf6c4b743515.png)


Tomcat requiere de más archivos que son de tipo xml para poder arrancarlos.


![Captura de pantalla de 2022-06-07 19-58-00](https://user-images.githubusercontent.com/100800688/172450884-bbd8ed43-acba-43d5-9318-96cc57b9fb05.png)

![Captura de pantalla de 2022-06-07 19-58-12](https://user-images.githubusercontent.com/100800688/172450893-b548caec-81c5-4349-a453-a5880c184b2f.png)


Ya tenemos los volumenes y archivos necesarios para poder desplegar nuestra aplicación pero por supuesto debemos tener también incluidos en un mismo repositorio junto a los archivos anterioros el código de nuestra app (fronted, backend, sql...)

 
