# Sprint 7 Hub de Lectura

# Verenice Alitzel Alba Hernández

## Capturas de pantalla del proyecto en ejecución

## Descripción de como lo hice
Inicié por diseñar la base de datos en SQL Server, eligiendo una estructura normalizada para evitar datos duplicados. Separé los géneros y las calificaciones en tablas independientes, y establecí relaciones con la tabla principal Libros mediante claves foráneas.
Después pasé al desarrollo de la interfaz en Visual Basic, donde trabajé con un ListView para mostrar los registros de forma profesional. Agregué controles como TextBox para el título y autor, ComboBox para género y calificación, y CheckBox para marcar si el libro fue leído, es favorito o si quiero leerlo en el futuro. Lo primero que me enfoqué en lograr fue que los ComboBox se llenaran automáticamente al iniciar el formulario. Para esto usé una conexión ADO y consultas SQL simples.
Una vez cargados los datos en los controles, implementé el botón Agregar libro utilizando Command con parámetros. Además, añadí validaciones básicas para asegurar que no se insertaran libros con campos vacíos o sin selección. 
Después implementé funciones adicionales como eliminar, filtrar por calificación, marcar como leído, mostrar libros por leer, y un módulo para libros recomendados. Cada una de estas funcionalidades fue desarrollada respetando el principio de modularidad, reutilizando configuraciones comunes del ListView y estableciendo controles de errores con On Error GoTo.

## Diagrama de entidad-relación




## Problemas conocidos

## Retrospectiva
¿Qué hice bien?
¿Qué no salió bien?
¿Qué puedo hacer diferente?
