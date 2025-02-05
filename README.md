

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>


# Creacion de API de peliculas usando LARAVEL


#### Para la creación del proyecto en laravel los primeros pasos son la instalación de LARAVEL y demás componentes que se utilzaran en el proceso para crear la API
#### Una vez abierto y detectado Laravel se crean carpetas las cuales serviran para ubicar los contenidos de Controladores, routes, modulos, etc. 

### -->  En el proyecto de nombre API si genera una carpeta app que contiene a Models, en este caso para el proyecto se crean los modelos de películas y usuario cada una de estas tiene ciertos atributos los cuales son:
#### Usuario
##### * nombre
##### * correo
##### * password
##### * foto de perfil
Dentro de Models en el usuario.php se creo de la sigueinte manera:
![image](https://github.com/user-attachments/assets/82d3da09-ea6a-4aee-9e50-307a0fb5c751)

![image](https://github.com/user-attachments/assets/320e5e14-c8e0-4484-a1f8-bb21367adc8b)


#### Peliculas
##### * nombre
##### * descripción
##### * año de filmación
##### * poster
##### * genero de la pelicula
Dentro de Models en el peliculas.php se creo de la sigueinte manera:
![image](https://github.com/user-attachments/assets/b83458b9-69ed-4f84-8580-20eca532511c)

![image](https://github.com/user-attachments/assets/b5ecf04c-2a3a-467e-82d0-df0aaab3a9b1)

##  Controladores
### En el caso de los controladores para poder hacer consultas a la api se crean los metodos correspondientes.
#### Para los usuarios se crearon los siguientes métodos:
### -> Usuario
##### Método de obtener usuario
![image](https://github.com/user-attachments/assets/c1360133-e0aa-41e4-94fa-8da910067006)
##### La función retorna a todos los usuarios que esten dentro, con una respuesta 200.
![image](https://github.com/user-attachments/assets/d1a6bc93-70ee-4abe-b8b1-937cfc583998)

##### Método obtener usuario por ID
![image](https://github.com/user-attachments/assets/21b38aaa-4ef4-4753-bf9c-9e4778dc1b8d)
##### Para esta función lo que hace es buscar a un usuario por medio de una ID en específico
![image](https://github.com/user-attachments/assets/19ae40fe-d32e-4e9f-982f-b51195245f1c)


##### Método insertar usuario
![image](https://github.com/user-attachments/assets/bcb2a94d-ec44-4db0-ad53-de37a30ff246)
##### Se hace un servicio el cual insertara  un nuevo usuario con los datos correspondientes para almacenarlos en la base de datos.
![image](https://github.com/user-attachments/assets/29d0d8a1-5115-41c5-bc17-81077bd1067b)

##### Método hacer cambios en el usuario
![image](https://github.com/user-attachments/assets/0260ae9f-73f6-43e5-a56c-12e9c15d48a7)
##### En la función se realiza una solicitud HTTP la cual permite hacer modificaciones sobre el usuario, esta modificación la hace ubicando el ID y con ello se modifican los campos del usuario con el que se requiera.
![image](https://github.com/user-attachments/assets/5bab97b3-a542-4747-9eab-571558a05479)

##### Método eliminar usuario
![image](https://github.com/user-attachments/assets/3f519080-85cd-481d-98a7-0c01fa75f5d7)
##### Para hacer eliminación de usuarios se requiere de un ID de usuario para buscarlo en el json y ejecutar la acción.
![image](https://github.com/user-attachments/assets/4838201b-af1e-41bb-8a76-0465a1234cf0)


#### Para las peliculas se crearon los siguientes métodos:
###  -> Películas
##### Método obtener película
![image](https://github.com/user-attachments/assets/6b914dfb-c53b-4627-9a60-99f6503dad39)
##### La función servirá para obtener las peliculas almacenadas en el json. 
![image](https://github.com/user-attachments/assets/4dbd47ac-5752-4bc7-8466-968dbcb47655)

##### Método obtener película por ID
![image](https://github.com/user-attachments/assets/710513ef-38b9-4e18-b382-48e1c363f7d5)
##### En esta función se podrá obtener unn solo resultado de película el cual es obtenido por medio del uso del ID sobre la película.
![image](https://github.com/user-attachments/assets/4dbd47ac-5752-4bc7-8466-968dbcb47655)

##### Método para insertar Pelicula
![image](https://github.com/user-attachments/assets/768b891b-57ad-4826-a59d-26758533da63)
##### La función agrega una nueva pelicula al json , que finalmente será a la base de datos. 
![image](https://github.com/user-attachments/assets/3103a3e3-1a6e-4415-a5d1-ee1eff2c65ec)


##### Método modificar película 
![image](https://github.com/user-attachments/assets/ee26d467-6584-45e6-b9d6-574558f919ab)
##### Para modificar una pelicula se requiere de una solicitud HTTP la cual buscara un id seleccionado lo busca dentro de la base y hace el cambió.
![image](https://github.com/user-attachments/assets/fb4cccd8-8625-4232-8fef-b1ac21bcfe9b)

##### Método eliminar película
![image](https://github.com/user-attachments/assets/30ad65d6-761e-4fed-9537-dbd6c2cb87d3)
##### Eliminar peliculas con apartir de una ID seleccionada, por tanto una vez realizada la búsqueda y encontrado de borrará de lo contrario no se aplicara ningun cambio sobre la base sobre alguna eliminación de registros. 
![image](https://github.com/user-attachments/assets/66898ccf-c052-4a2e-9347-89bf3db719f1)

##### Método buscar por nombre de película 
![image](https://github.com/user-attachments/assets/ba663ba3-272c-478f-bc80-9bbcff556aeb)
##### La función realizara la consulta de obtener una película con el nombre que habrá sido especificado con el nombre por lo cual se realiza la consulta para este por medio del uso de solicitudes HTTP. 

##### Método paginación de películas
![image](https://github.com/user-attachments/assets/0e507d85-13b0-4fef-9665-f7580754e089)
##### -> Se hace una obtención de peliculas para que puedan ser puestos en la paginación de la tabla, la cual esta hecha por medio de cantidad de películas por página y con ello se podrá variar la cantidad de paginas. 
![image](https://github.com/user-attachments/assets/9d00d99e-86b3-4b3a-871a-5ace988121a5)

### En la carpeta de routes dentro del archivo de api.php, se crearán los servicios los cuales se hacen por medio de las solicitudes HTTP las cuales son: 
#### - GET
##### El método GET solicita una representación de un recurso específico. Las peticiones que usan el método GET sólo deben recuperar datos.

#### - POST
##### El método POST se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.

#### - PUT
##### El modo PUT reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

#### - DELETE
##### El método DELETE borra un recurso en específico.

### -> Dentro de la carpeta de routes en el archivo api.php 

#### Se crearon los servicios para los usuarios y las películas que son los elementos con los que se trabajarán en el proyecto.

##### ° Usuarios
![image](https://github.com/user-attachments/assets/94bbdd60-0221-4e83-aac5-9fbe00c42f20)

##### Se ingresan las rutas del controlador y el nombre de la función, así como también el atributo que requiere que en este caso es sobre el ID del usuario sobre el cual se hara el servicio que corresponde.

##### ° Película

![image](https://github.com/user-attachments/assets/90855c29-71a1-4dbe-8413-4f64f3358c9d)

##### Se ingresan las rutas del controlador y el nombre de la función, así como también el atributo que requiere que en este caso es sobre el ID que tiene la pelicula sobre el cual se realizara el servicio que corresponde.

#### En el archivo de .env en el cual se coloca  el nombre de la base de datos, el usuario y contraseña que tiene. 
![image](https://github.com/user-attachments/assets/724bae55-1efe-46ad-9122-28f171aab650)


----------------------------------------------------------------------------------------------
## Cuando se requieran hacer consultas por medio de los botones los servicios de laravel tienen que estar inicializados, esto se logra con el comando "php artisan serve"
![image](https://github.com/user-attachments/assets/4e7f1cc2-49fe-4911-b58c-2dd413f3a080)

----------------------------------------------------------------------------------------------
