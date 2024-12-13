

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

#### Peliculas
##### * nombre
##### * descripción
##### * año de filmación
##### * poster
##### * genero de la pelicula
Dentro de Models en el peliculas.php se creo de la sigueinte manera:
![image](https://github.com/user-attachments/assets/b83458b9-69ed-4f84-8580-20eca532511c)
##  Controladores
### En el caso de los controladores para poder hacer consultas a la api se crean los metodos correspondientes.
#### Para los usuarios se crearon los siguientes métodos:
### -> Usuario
##### Método de obtener usuario
![image](https://github.com/user-attachments/assets/c1360133-e0aa-41e4-94fa-8da910067006)
##### La función retorna a todos los usuarios que esten dentro, con una respuesta 200.

##### Método obtener usaurio por ID
![image](https://github.com/user-attachments/assets/21b38aaa-4ef4-4753-bf9c-9e4778dc1b8d)
##### Para esta función lo que hace es buscar a un usuario por medio de una ID en específico

##### Método insertar usuario
![image](https://github.com/user-attachments/assets/bcb2a94d-ec44-4db0-ad53-de37a30ff246)
##### Se hace un servicio el cual insertara  un nuevo usuario con los datos correspondientes para almacenarlos en la base de datos.

##### Método hacer cambios en el usuario
![image](https://github.com/user-attachments/assets/0260ae9f-73f6-43e5-a56c-12e9c15d48a7)
##### En la función se realiza una solicitud HTTP la cual permite hacer modificaciones sobre el usuario, esta modificación la hace ubicando el ID y con ello se modifican los campos del usuario con el que se requiera.

##### Método eliminar usuario
![image](https://github.com/user-attachments/assets/3f519080-85cd-481d-98a7-0c01fa75f5d7)
##### Para hacer eliminación de usuarios se requiere de un ID de usuario para buscarlo en el json y ejecutar la acción.

#### Para las peliculas se crearon los siguientes métodos:
###  -> Películas
##### Método obtener película
![image](https://github.com/user-attachments/assets/6b914dfb-c53b-4627-9a60-99f6503dad39)
##### La función servirá para obtener las peliculas almacenadas en el json. 

##### Método obtener película por ID
![image](https://github.com/user-attachments/assets/710513ef-38b9-4e18-b382-48e1c363f7d5)
##### En esta función se podrá obtener unn solo resultado de película el cual es obtenido por medio del uso del ID sobre la película.

##### Método para insertar Pelicula
![image](https://github.com/user-attachments/assets/768b891b-57ad-4826-a59d-26758533da63)
##### La función agrega una nueva pelicula al json , que finalmente será a la base de datos. 

##### Método modificar película 
![image](https://github.com/user-attachments/assets/ee26d467-6584-45e6-b9d6-574558f919ab)
##### Para modificar una pelicula se requiere de una solicitud HTTP la cual buscara un id seleccionado lo busca dentro de la base y hace el cambió.

##### Método eliminar película
![image](https://github.com/user-attachments/assets/30ad65d6-761e-4fed-9537-dbd6c2cb87d3)
##### Eliminar peliculas con apartir de una ID seleccionada, por tanto una vez realizada la búsqueda y encontrado de borrará de lo contrario no se aplicara ningun cambio sobre la base sobre alguna eliminación de registros. 

##### Método buscar por nombre de película 
![image](https://github.com/user-attachments/assets/ba663ba3-272c-478f-bc80-9bbcff556aeb)
##### La función realizara la consulta de obtener una película con el nombre que habrá sido especificado con el nombre por lo cual se realiza la consulta para este por medio del uso de solicitudes HTTP. 

##### Método paginación de películas
![image](https://github.com/user-attachments/assets/0e507d85-13b0-4fef-9665-f7580754e089)
##### Se hace una obtención de peliculas para que puedan ser puestos en la paginación de la tabla, la cual esta hecha por medio de cantidad de películas por página y con ello se podrá variar la cantidad de paginas. 

### En la carpeta de routes dentro del archivo de api.php, se crearán los servicios los cuales se hacen por medio de las solicitudes HTTP las cuales son: 
#### - GET
##### El método GET solicita una representación de un recurso específico. Las peticiones que usan el método GET sólo deben recuperar datos.

#### - POST
##### El método POST se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.

#### - PUT
##### El modo PUT reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

#### - DELETE
##### El método DELETE borra un recurso en específico.

### Dentro de la carpeta de routes en el archivo api.php 

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



<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
