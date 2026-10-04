# Conexión Híbrida entre una Base de Datos en la Nube y una Aplicación en Java

**Maestría en Inteligencia Artificial y Computacional**  
**Módulo:** Fundamentos de la Tecnología Cloud (Unidad 4: Monitores de Servicios)  
**Institución:** Politécnico Grancolombiano  
**Estudiante:** Sebastian Echavez Cadena  
**Fecha:** 3 de octubre de 2026  

---

## 📄 Descripción

Proyecto académico enfocado en el desarrollo de una aplicación de escritorio orientada a objetos en **Java 21**[cite: 2], que implementa una arquitectura híbrida al conectarse con el servicio de base de datos NoSQL **Firebase Firestore** alojado en la nube (`us-east1`). 

El sistema gestiona la información de estudiantes universitarios mediante el ciclo de vida completo de operaciones CRUD (Crear, Leer, Actualizar, Eliminar)[cite: 2, 5], permitiendo la carga masiva desde archivos locales CSV y ofreciendo persistencia distribuida en tiempo real accesible tanto por consola como por una interfaz gráfica interactiva[cite: 2, 5].

---

## 🎯 Objetivos del Proyecto

* **Objetivo General:** Desarrollar una aplicación en Java conectada a Firebase Firestore para la gestión de datos de estudiantes universitarios mediante las cuatro operaciones fundamentales del CRUD[cite: 5].
* **Objetivos Específicos:**
  * Leer y procesar archivos locales `.csv` con datos estructurados de estudiantes[cite: 5].
  * Cargar registros masivamente en la nube utilizando el SDK de Firebase Admin para Java[cite: 5].
  * Consultar la información en Firestore mediante listados completos y búsquedas por identificador único[cite: 5].
  * Modificar y actualizar la información de estudiantes existentes directamente en la base de datos distribuida[cite: 5].
  * Eliminar registros en la nube de forma controlada[cite: 5].
  * Diseñar una interfaz gráfica de usuario (GUI) con la biblioteca Swing de Java[cite: 5].

---

## 🏗️ Arquitectura y Estructura del Código

El proyecto aplica la separación de responsabilidades y patrones de diseño orientados a objetos[cite: 8, 9]:

```text
src/main/java/org/example/
├── Estudiante.java         # Modelo de datos POJO (atributos, getters, setters, toString y toCSV).
├── LectorCSV.java          # Lectura de archivos CSV y conversión a objetos Estudiante.
├── FirebaseConnection.java # Conexión Singleton con Firebase Firestore mediante Firebase Admin SDK.
├── EstudianteService.java  # Capa de lógica de negocio y operaciones CRUD en Firestore.
├── VentanaPrincipal.java   # Interfaz gráfica de usuario construida con Swing.
└── Main.java               # Prueba secuencial del flujo completo del CRUD por consola.
