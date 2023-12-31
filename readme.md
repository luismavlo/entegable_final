# RealmQuest: Tesoros Intercambiables

Explora el fascinante mundo de RealmQuest, un emocionante juego de aventuras y exploración en línea
donde las oportunidades son tan vastas como los horizontes que se despliegan ante ti.
Sumérgete en un reino lleno de misterio, tesoros y desafíos esperando a ser descubiertos.

En RealmQuest, tú eres el protagonista de tu propia leyenda. Viaja a través de vastos paisajes,
desde densos bosques hasta áridos desiertos, descubriendo áreas secretas y ocultos tesoros
a lo largo del camino. Cada rincón del mundo está lleno de elementos valiosos que pueden ser
recolectados y añadidos a tu inventario personal.

Pero eso no es todo. En el corazón de RealmQuest yace la capacidad de comerciar con otros jugadores.
Forja alianzas, haz amigos y participa en emocionantes intercambios donde puedes intercambiar los
tesoros que has encontrado por los que otros aventureros han descubierto. Cada comercio es una
oportunidad para fortalecer tu personaje, obtener objetos únicos y establecer tu lugar en la
historia de este vibrante mundo en línea.

Prepárate para una experiencia en la que la exploración, la camaradería y la estrategia se unen.
¡Desafía a tus amigos, descubre tesoros perdidos
y haz tu marca en RealmQuest: ¡Tesoros Intercambiables!

- Administrador de base de datos:
  Hola soy el administrador de base de datos, te dejare el diagrama entidad relación
  para que realices la implementación de la base de datos.
  ![Diagrama entidad Relación](pictures/RealmQuest.png)
  https://dbdiagram.io/d/64d7ab4d02bd1c4a5eacaf9a

## Funcionalidades a implementar

### Se deben considerar los siguientes endpoints:

| routa     | ->       | /api/v1/users                                                                    |
| --------- | -------- | -------------------------------------------------------------------------------- |
| HTTP VERB | ROUTE    | DESCRIPTION                                                                      |
| POST      | /signup  | crear un usuario, enviar por la req.body: username, password, email, place_birth |
| POST      | /signin  | iniciar session, enviar por la req.body: email, password                         |
| GET       | /        | obtener el listado de todos los usuarios                                         |
| GET       | /:id     | obtener un usuario dado un id, siendo :id el id del usuario                      |
| PATCH     | /:id     | actualizar el username del usuario, siendo :id el id del usuario                 |
| DELETE    | /:id     | eliminar la cuenta del usuario, siendo :id el id del usuario                     |
| DELETE    | /ban/:id | banear indefinidamente la cuenta de un usuario, siendo :id el id del usuario     |

#### consideraciones adicionales

1. Todas las rutas ecepto las post, /signup /signin deben estar protegidas por un metodo de autenticación
2. Las rutas Get /, y delete /ban/:id deben estar protegidas para que solo usuarios gm y admin puedan utilizarla
3. Las rutas patch /:id y delete /:id deben estar protegidas para que solo el usuario en sesión pueda ejecutarlas
4. Validar la informacion que viene de la req.body de las rutas post y patch
5. encriptar contraseñas

notas adicionales

- agregar una propiedad en la base de datos isOnline
- agregar funcionalidad de buscar todos los jugadores online por zona
