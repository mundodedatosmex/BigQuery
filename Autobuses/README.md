# Dataset y Esquema de Base de Datos - Sistema de Venta de Boletos (BigQuery)

Repositorio que contiene los conjuntos de datos en formato **CSV** diseñados para poblar y analizar un modelo relacional de un sistema de transporte y venta de boletos, optimizado para su uso en **Google BigQuery**.

---

## 📊 Modelo Entidad-Relación (ER)

El esquema de la base de datos consta de tres tablas principales (`rutas`, `horarios` y `boletos`) que estructuran la información operativa y transaccional del servicio.

[![Diagrama Entidad-Relación](https://lh3.googleusercontent.com/d/1W0KN58kStsP5-XV4G9CeBP9mawSUQFU9=s1200)](https://drive.google.com/file/d/1W0KN58kStsP5-XV4G9CeBP9mawSUQFU9/view?usp=sharing)

*(También puedes consultar el diagrama original en Google Drive haciendo [clic aquí](https://drive.google.com/file/d/1W0KN58kStsP5-XV4G9CeBP9mawSUQFU9/view?usp=sharing)).*

---

## 🗂️ Estructura del Esquema y Tablas

### 1. `rutas`
Contiene la información geográfica y comercial de las rutas disponibles.
*   `id_rutas` (INTEGER): Identificador único de la ruta (Clave Primaria).
*   `destino` (VARCHAR/STRING): Ciudad o destino de llegada.
*   `distancia_km` (INTEGER): Distancia total del recorrido en kilómetros.
*   `tiempo_hrs` (FLOAT): Tiempo estimado de viaje en horas.
*   `precio_base` (FLOAT): Tarifa base establecida para la ruta.

### 2. `horarios`
Registra la programación de salidas y asignación de unidades vehiculares por ruta.
*   `id_horario` (INTEGER): Identificador único del horario (Clave Primaria).
*   `id_ruta` (INTEGER): Referencia a la ruta asociada (Clave Foránea).
*   `hora_salida` (VARCHAR/STRING): Horario programado de salida.
*   `autobus` (VARCHAR/STRING): Identificador o tipo de unidad asignada.

### 3. `boletos`
Tabla transaccional que almacena el registro de cada boleto vendido.
*   `id_boleto` (INTEGER): Identificador único del boleto transaccionado (Clave Primaria).
*   `fecha_viaje` (DATE): Fecha en la que se llevará a cabo el viaje.
*   `id_ruta` (INTEGER): Referencia a la ruta (Clave Foránea).
*   `id_horario` (INTEGER): Referencia al horario seleccionado (Clave Foránea).
*   `asiento` (INTEGER): Número de asiento asignado dentro de la unidad.
*   `tipo_pasajero` (VARCHAR/STRING): Categoría del pasajero (ej. General, Estudiante, INAPAM).
*   `canal_venta` (VARCHAR/STRING): Medio a través del cual se realizó la compra (ej. Taquilla, Web, App).
*   `precio_pagado` (INTEGER/FLOAT): Monto final cobrado por el boleto.

---

## 🚀 Instrucciones para Carga en BigQuery

1.  **Crear el Dataset en BigQuery:**

2.  **Cargar los Archivos CSV:**
    *   Sube cada archivo CSV (`rutas.csv`, `horarios.csv`, `boletos.csv`) a un bucket en **Google Cloud Storage (GCS)** o cárgalos directamente mediante la interfaz web de BigQuery seleccionando "Crear tabla" a partir de una fuente de carga (Upload / GCS) con autodetección de esquema activada.

---
*Desarrollado para fines educativos y prácticos por **Mundo de Datos Mex** (Erick Orlando Matla Cruz).*
