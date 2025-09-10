# LIBRER-A-VIRTUAL---BASE-DE-DATOS
Proyecto final - Base de datos
# 📚 Proyecto Base de Datos - BIBLIOTECA_NEXUZ

## 📖 Descripción
El proyecto **BIBLIOTECA_NEXUZ** implementa un sistema de gestión para una biblioteca.  
Se desarrolló en **SQL Server** y contiene la creación de tablas, inserción de datos, aplicación de restricciones y consultas avanzadas.  
Permite administrar **usuarios, trabajadores, autores, libros, préstamos y categorías**, además de procedimientos almacenados y subconsultas para obtener información útil.

---

## 🏗️ Estructura de la Base de Datos
La base de datos está conformada por las siguientes tablas principales:

- **CATEGORIA** → Clasificación de los libros (Ej: Lírico, Dramático, Científicos, etc.).
- **USUARIO** → Datos de los usuarios registrados en la biblioteca.
- **TRABAJADORES** → Información de los empleados (limpieza y recepcionistas).
- **AUTOR** → Autores de los libros.
- **LIBRO** → Registro de libros disponibles, vinculados a categorías, autores y trabajadores.
- **PRESTAMO** → Control de préstamos realizados a los usuarios.
- **LIBRO_PRESTAMO** → Relación entre libros y préstamos.
- **LIMPIEZA** → Tareas asignadas a trabajadores de limpieza.
- **RECEPCIONISTA** → Datos adicionales de trabajadores recepcionistas.

---

## ⚙️ Restricciones y Reglas de Negocio
- **Usuarios**: fecha de registro no puede ser futura; correos únicos.  
- **Trabajadores**: salario ≥ 1025; solo puestos "LIMPIEZA" o "RECEPCIONISTA".  
- **Libros**: fecha de lanzamiento futura; relación con categoría y autor.  
- **Préstamos**: fecha de préstamo ≤ fecha actual.  
- **Limpieza**: tareas limitadas a `BARRER`, `DESEMPOLVAR LOS LIBROS`, `ORDENAR LOS LIBROS`.  
- **Recepcionistas**: conocimientos en `WORD` o `EXCEL`.  

---

## 🗄️ Inserción de Datos
El script incluye **datos de ejemplo** para todas las tablas:
- 10 categorías de libros.  
- 20 usuarios registrados.  
- 15 trabajadores (limpieza y recepción).  
- 10 autores reconocidos.  
- 15 libros (con autores y categorías asociadas).  
- 25 préstamos.  
- Asignaciones de limpieza y recepcionistas.  

---

## 🔍 Consultas Implementadas
Incluye **consultas con JOINs** y **subconsultas**, tales como:
- Usuarios con préstamos realizados.  
- Trabajadores relacionados con limpieza.  
- Relación de libros con autores y categorías.  
- Usuarios que no tienen préstamos.  
- Conteo de préstamos por usuario.  

---

## 🛠️ Procedimientos Almacenados
1. **Consulta_Prestamo_Usuario** → Muestra préstamos asociados a un usuario.  
2. **Consulta_Trabajadores_Limpieza** → Relaciona trabajadores con sus labores de limpieza.  
3. **Consulta_libro_autor** → Relaciona libros con sus autores.  
4. **SP_MostrarCategoriaMasSolicitada** → Muestra la categoría de libros más prestada.  
5. **SP_FiltrarRecepcionistasConConocimientoWord** → Lista recepcionistas con conocimiento en Word.  

---

## 🚀 Uso
1. Ejecutar el script en **SQL Server Management Studio (SSMS)**.  
2. Verificar la creación de la base de datos `BIBLIOTECA_NEXUZ`.  
3. Ejecutar las consultas y procedimientos almacenados para explorar la información.  

---
