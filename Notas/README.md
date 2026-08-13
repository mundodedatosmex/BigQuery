# SQL en BigQuery - Mundo de Datos Mex

Este repositorio contiene una guía técnica de referencia sobre el uso de **SQL en Google BigQuery**, desarrollada por **Erick Orlando Matla Cruz** para la marca educativa **Mundo de Datos Mex**.

El material abarca desde los fundamentos de consultas hasta conceptos avanzados de administración de datos en el ecosistema de Google Cloud.

## Contenido del Repositorio

Este archivo (`SQL en BigQuery.pdf`) cubre los siguientes temas esenciales:

### 1. Consultas Fundamentales
*   **Estructura básica:** Uso de `SELECT` y `FROM` para recuperación de datos.
*   **Condiciones:** Filtrado de tuplas utilizando la cláusula `WHERE` con diversos operadores (`LIKE`, `IN`, `BETWEEN`, etc.).

### 2. Manipulación de Datos y Conjuntos
*   **Subconsultas:** Utilización de resultados de consultas como tablas temporales o valores únicos.
*   **Expresiones Comunes de Tabla (CTE):** Definición de tablas virtuales temporales mediante la cláusula `WITH`.

### 3. Agregaciones y Análisis
*   **Funciones de Agregación:** Uso de `MAX`, `MIN`, `SUM`, `COUNT`, `AVG` y el uso de `GROUP BY` para generar análisis agrupados.
*   **Funciones de Ventana (Window Functions):** Aplicación de cálculos analíticos sobre bloques de datos sin colapsar las filas, incluyendo `ROW_NUMBER()` y `RANK()`.

### 4. Relaciones entre Tablas
*   **Operaciones JOIN:** Guía detallada sobre `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL OUTER JOIN` y `CROSS JOIN` para combinar datos eficazmente.

### 5. Objetos de Base de Datos y Automatización
*   **Vistas y Vistas Materializadas:** Definición de consultas reutilizables y optimización de rendimiento en BigQuery.
*   **Funciones Definidas por el Usuario (UDF):** Creación de rutinas personalizadas que devuelven valores.
*   **Procedimientos Almacenados:** Implementación de lógica compleja y consultas dinámicas mediante `CREATE PROCEDURE`.

---
*Documentación creada por Erick Orlando Matla Cruz - Mundo de Datos Mex.*
