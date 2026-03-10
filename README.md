# API de Soporte Técnico

## Descripción

Este proyecto consiste en el desarrollo de una **API RESTful** utilizando **Java y Spring Boot** para gestionar solicitudes de soporte técnico de clientes.

La API permite registrar, consultar, actualizar y eliminar solicitudes de soporte de manera eficiente.
El almacenamiento de datos se simula utilizando **listas en memoria**, sin conexión a una base de datos.

---

## Tecnologías utilizadas

* Java
* Spring Boot
* Maven
* Postman
* GitHub

---

## Arquitectura del proyecto

El proyecto está organizado siguiendo una **arquitectura en capas** para separar responsabilidades y mejorar el mantenimiento del código.

```
src/main/java/com/example/soporteapi

controller
dto
exception
model
service
util
```

### Descripción de las capas

**controller**
Contiene los controladores REST que reciben las solicitudes HTTP.

**service**
Contiene la lógica de negocio de la aplicación.

**model**
Define las entidades del sistema como Solicitud, Cliente y Tecnico.

**dto**
Clases utilizadas para transferir datos entre el cliente y la API.

**exception**
Manejo centralizado de errores.

**util**
Clases utilitarias como Mapper para convertir DTO a entidades.

---

## Endpoints de la API

### Obtener todas las solicitudes

GET

```
/api/solicitudes
```

---

### Obtener solicitud por ID

GET

```
/api/solicitudes/{id}
```

---

### Crear una solicitud

POST

```
/api/solicitudes
```

Body JSON

```json
{
  "clienteId": 1,
  "tecnicoId": 1,
  "descripcion": "Laptop no enciende",
  "estado": "Pendiente"
}
```

---

### Actualizar una solicitud

PUT

```
/api/solicitudes/{id}
```

Body JSON

```json
{
  "clienteId": 1,
  "tecnicoId": 1,
  "descripcion": "Laptop reparada",
  "estado": "Resuelto"
}
```

---

### Eliminar una solicitud

DELETE

```
/api/solicitudes/{id}
```

---

## Ejecución del proyecto

### . Entrar al proyecto

```
cd api-soporte-tecnico
```

### 3. Ejecutar la aplicación

```
mvn spring-boot:run
```

La API se ejecutará en:

```
http://localhost:8080
```

---

## Pruebas

Las pruebas de los endpoints se realizaron utilizando **Postman**, verificando el funcionamiento de:

* Crear solicitud (POST)
* Listar solicitudes (GET)
* Obtener solicitud por ID (GET)
* Actualizar solicitud (PUT)
* Eliminar solicitud (DELETE)

---

## Repositorio

Repositorio del proyecto:

```
[https://github.com/tuusuario/api-soporte-tecnico](https://github.com/paolo2007/api)
```

---

## Autores

Proyecto desarrollado como parte de la unidad didáctica **Desarrollo de los Componentes del Negocio**.
