# PLAN DE PRUEBAS  – AVANSER

## 1. Información General

**Proyecto:** Avanser  
**Tipo de aplicación:** API REST  
**Tipo de pruebas:** Pruebas de integración  
**Herramientas:** Jest, Supertest  
**Fecha:** 17 de diciembre de 2025  
**Versión:** 1.0  

---

## 2. Objetivo

Definir los casos de prueba necesarios para validar el correcto funcionamiento de los módulos de autenticación, usuario, ficha y programa de la API Avanser, garantizando el cumplimiento de los requerimientos funcionales del sistema.

---

## 3. Alcance

El presente plan de pruebas cubre los siguientes módulos y archivos de prueba automatizada:

- Autenticación (`test_auth`)
- Gestión de usuarios (`test_usuario`)
- Gestión de fichas (`test_ficha`)
- Gestión de programas (`test_programa`)

---

## 4. Casos de Prueba

---

## 🔐 Módulo Autenticación (`test_auth`)

### CP-AUTH-01 – Crear usuario correctamente

**Endpoint:** `/api/usuario`  
**Método:** POST  

**Descripción:**  
Validar que el sistema permita registrar un usuario cuando los datos enviados son válidos.

**Resultado esperado:**  
- Código HTTP 201  
- Usuario creado correctamente  

---

### CP-AUTH-02 – Documento duplicado

**Endpoint:** `/api/usuario`  
**Método:** POST  

**Descripción:**  
Validar que el sistema no permita registrar usuarios con documentos duplicados.

**Resultado esperado:**  
- Código HTTP 400  
- Mensaje de error indicando documento duplicado  

---

### CP-AUTH-03 – Datos inválidos

**Endpoint:** `/api/usuario`  
**Método:** POST  

**Descripción:**  
Validar el manejo de errores cuando se envían datos inválidos o incompletos.

**Resultado esperado:**  
- Código HTTP 400 / 500  
- Mensaje de error correspondiente  

---

## 👤 Módulo Usuario (`test_usuario`)

### CP-USU-01 – Obtener listado de usuarios

**Endpoint:** `/api/usuario`  
**Método:** GET  

**Descripción:**  
Validar que el sistema retorne el listado de usuarios registrados.

**Resultado esperado:**  
- Código HTTP 200  
- Listado de usuarios  

---

### CP-USU-02 – Error interno del sistema

**Endpoint:** `/api/usuario`  
**Método:** GET  

**Descripción:**  
Validar el manejo de errores internos del sistema.

**Resultado esperado:**  
- Código HTTP 500  
- Mensaje de error interno  

---

## 📄 Módulo Ficha (`test_ficha`)

### CP-FIC-01 – Crear ficha correctamente

**Endpoint:** `/api/ficha`  
**Método:** POST  

**Descripción:**  
Validar la creación de una ficha con datos válidos.

**Resultado esperado:**  
- Código HTTP 201  
- Ficha creada correctamente  

---

### CP-FIC-02 – Datos inválidos en ficha

**Endpoint:** `/api/ficha`  
**Método:** POST  

**Descripción:**  
Validar errores al crear una ficha con datos incompletos o inválidos.

**Resultado esperado:**  
- Código HTTP 400 / 500  
- Mensaje de error  

---

## 📘 Módulo Programa (`test_programa`)

### CP-PRO-01 – Crear programa correctamente

**Endpoint:** `/api/programa`  
**Método:** POST  

**Descripción:**  
Validar la creación de un programa con datos válidos.

**Resultado esperado:**  
- Código HTTP 201  
- Programa creado correctamente  

---

### CP-PRO-02 – Error interno del sistema

**Endpoint:** `/api/programa`  
**Método:** POST  

**Descripción:**  
Validar el manejo de errores internos del sistema.

**Resultado esperado:**  
- Código HTTP 500  
- Mensaje de error interno  
