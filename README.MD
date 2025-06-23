# Sprint 7 Hub de Lectura

# Verenice Alitzel Alba Hernández

# Capturas de pantalla del proyecto en ejecución
Se meuestra el hub de lectrura aplicando las distintas funcionalidades:
![Captura de pantalla 2](/ss/catalogo.png)
![Captura de pantalla 3](/ss/leidos.png)
![Captura de pantalla 4](/ss/favoritos.png)
![Captura de pantalla 5](/ss/quieroleer.png)
![Captura de pantalla 6](/ss/Agregar.png)
![Captura de pantalla 7](/ss/recomendacion.png)
![Captura de pantalla 8](/ss/eliminar.png)
![Captura de pantalla 9](/ss/eliminado.png)

# Descripción de como lo hice
Inicié por diseñar la base de datos en SQL Server, eligiendo una estructura normalizada para evitar datos duplicados. Separé los géneros y las calificaciones en tablas independientes, y establecí relaciones con la tabla principal Libros mediante claves foráneas.
Después pasé al desarrollo de la interfaz en Visual Basic, donde trabajé con un ListView para mostrar los registros de forma profesional. Agregué controles como TextBox para el título y autor, ComboBox para género y calificación, y CheckBox para marcar si el libro fue leído, es favorito o si quiero leerlo en el futuro. Lo primero que me enfoqué en lograr fue que los ComboBox se llenaran automáticamente al iniciar el formulario. Para esto usé una conexión ADO y consultas SQL simples.
Una vez cargados los datos en los controles, implementé el botón Agregar libro utilizando Command con parámetros. Además, añadí validaciones básicas para asegurar que no se insertaran libros con campos vacíos o sin selección.
Después implementé funciones adicionales como eliminar, filtrar por calificación, marcar como leído, mostrar libros por leer, y un módulo para libros recomendados. Cada una de estas funcionalidades fue desarrollada respetando el principio de modularidad, reutilizando configuraciones comunes del ListView y estableciendo controles de errores con On Error GoTo.

# Diagrama de entidad-relación
![Captura de pantalla 1](/ss/ER.png)

## Problemas conocidos
Si las tablas Géneros o Calificaciones están vacías, no se pueden agregar libros por restricciones de claves foráneas, lo que puede generar errores y confusión para el usuario.
La recarga completa del ListView puede volverse lenta cuando se tienen muchos registros.

## Retrospectiva
¿Qué hice bien?
- Comencé por la base de datos y mantuve un orden lógico entre el modelo, la interfaz y la lógica.
- El separar géneros y calificaciones para evitar datos repetidos.
- Usé parámetros en las consultas al agregar libros, lo cual ayuda a proteger la integridad de los datos.
- Realice una interfaz amigable, con validaciones claras y una distribución comprensible.
¿Qué no salió bien?
- Al principio no entendía cómo acceder al valor interno de los ComboBox, lo cual provocaba errores al insertar registros.
¿Qué puedo hacer diferente?
- Agregar mensajes más específicos y retroalimentación visual inmediata cuando se agrega, elimina o edita un registro.