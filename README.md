Conexión híbrida entre una base de datos en la nube y una aplicación en Java
Proyecto desarrollado para la actividad sumativa de la Unidad 4 del módulo Fundamentos de la Tecnología Cloud (Maestría en Inteligencia Artificial y Computacional, Politécnico Grancolombiano).
Descripción
Aplicación de escritorio desarrollada en Java 21 con Maven, que se conecta a la base de datos NoSQL Firebase Firestore en la nube. El programa permite:
Leer un archivo CSV con información de estudiantes y cargarlo masivamente a Firestore.
Listar todos los registros almacenados en la nube.
Buscar un estudiante por su ID.
Insertar nuevos estudiantes.
Actualizar los datos de un estudiante existente.
Eliminar registros de la base de datos.
Todas las operaciones se pueden realizar desde una interfaz gráfica construida con Swing.
Estructura del proyecto
Estudiante: modelo de datos (POJO) con los atributos del estudiante.
LectorCSV: lectura del archivo CSV y conversión a objetos Estudiante.
FirebaseConnection: conexión Singleton con Firebase Firestore mediante el SDK de Firebase Admin.
EstudianteService: lógica de negocio con las operaciones CRUD.
VentanaPrincipal: interfaz gráfica con Swing.
Main: clase de pruebas que ejecuta el flujo completo del CRUD por consola.
Tecnologías utilizadas
Java 21
Apache Maven (gestión de dependencias)
Firebase Admin SDK 9.4.3
Cloud Firestore (base de datos NoSQL en la nube)
Swing (interfaz gráfica)
IntelliJ IDEA
Requisitos para ejecutar
JDK 21 o superior instalado.
Apache Maven.
Un proyecto en Firebase con Cloud Firestore habilitado.
El archivo serviceAccountKey.json (credenciales de cuenta de servicio) dentro de src/main/resources. Por seguridad, este archivo no se incluye en el repositorio; se entrega junto con el proyecto comprimido.
Cómo ejecutar
Clonar o descargar el repositorio.
Colocar el archivo serviceAccountKey.json en src/main/resources.
Colocar el archivo estudiantes.csv en la raíz del proyecto.
Compilar con: mvn clean install
Ejecutar la clase Main para las pruebas por consola, o la clase VentanaPrincipal para la interfaz gráfica.
