# Inventory

## Descripción del Proyecto

Inventory es una aplicación de inventarios desarrollada en Spring Boot. Proporciona funcionalidades para gestionar inventarios, seguimiento de productos y otras operaciones relacionadas con la gestión de inventarios.

## Requisitos Previos

Asegúrate de tener instaladas las siguientes versiones de las tecnologías requeridas:

- Spring Boot 3.0.4
- Spring Framework 6.0.6
- JDK 17.0.2 (build 17.0.2+8)
- Jakarta EE 9
- MySQL

## Instrucciones de Instalación

1. Clona el repositorio:

    ```bash
    git clone git@github.com:IngAamira/inventory-bk.git
    ```

2. Configura las propiedades de la base de datos en `application.properties`:
   **Nota:** Base de Datos:
   La aplicación utiliza MySQL como base de datos. Asegúrate de crear la base de datos y configurar las propiedades adecuadas en `application.properties`.

    ```properties
    spring.datasource.url=jdbc:mysql://localhost/you_name_db?allowPublicKeyRetrieval=true&useSSL=false&useLegacyDatetimeCode=false&serverTimezone=UTC
    spring.datasource.username=root
    spring.datasource.password=your_pastword
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.jpa.database-platform=org.hibernate.dialect.MySQL57Dialect
    spring.jpa.hibernate.ddl-auto=update
    logging.level.org.hibernate.SQL=debug
    spring.servlet.multipart.max-file-size=3MB
    spring.servlet.multipart.max-request-size=3MB
    ```

3. Ejecuta la aplicación:

    ```bash
    ./gradlew bootRun
    ```

## Estructura del Proyecto

```bash
/inventory
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── com.ingaamira.inventory
│   │   │   │   ├── controller
│   │   │   │   ├── dao
│   │   │   │   ├── model
│   │   │   │   ├── response
│   │   │   │   ├── service
│   │   │   │   ├── util
│   │   ├── resources
│   │   │   ├── application.properties
│   ├── test
├── .gitignore
├── build.gradle
├── settings.gradle
├── README.md

## Endpoint
- http://localhost:8080/api/v1/categories
```json
{
   "metadata": [
      {
         "date": "Respuesta exitosa",
         "code": "00",
         "type": "Respuesta ok"
      }
   ],
   "categoryResponse": {
      "category": [
         {
            "id": 1,
            "name": "prueba",
            "description": "test ok"
         }
      ]
   }
}
```

## Contribución
Si deseas contribuir al proyecto, sigue los pasos:

- Haz un fork del repositorio.
- Crea una nueva rama para tu función: `git checkout -b feature/nueva_funcion`.
- Realiza tus cambios y haz commit: `git commit -m "Añade nueva_funcion"`.
- Haz push a tu rama: `git push origin feature/nueva_funcion`.
- Crea un pull request.

## Licencia

Este proyecto está bajo la licencia [GNU GENERAL PUBLIC LICENSE]. Consulta el archivo [LICENSE.md](LICENSE.md) para obtener más detalles sobre los términos de la licencia.

## Información de Contacto

Para preguntas o comentarios, ponte en contacto con [andres.mira@outlook.com](mailto:andres.mira@outlook.com).

