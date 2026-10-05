# Estado Actual de la Práctica: Lab#SE03-1

## 📊 Resumen del Proyecto

* **Proyecto:** `library-model`
* **Tecnología Base:** Java SE con sistema de construcción **Maven**
* **IDE Utilizado:** IntelliJ IDEA

---

## 📋 Lista de Requisitos y Estado de Cumplimiento

### 1. Configuración del Proyecto y Entorno
* **[PASADO]** Creación de la estructura de directorios estándar de Maven (`src/main/java` y `src/test/java`).
* **[PASADO]** Configuración del archivo `pom.xml` con compatibilidad para Java 21.

### 2. Gestión de Dependencias
* **[PASADO]** **Lombok:** Configurado en su versión estable `1.18.30` para solucionar incompatibilidades con las características modernas del compilador de Java.
* **[PASADO]** **Java Faker:** Integrado correctamente para la generación dinámica de juegos de datos de prueba aleatorios.
* **[PASADO]** **JUnit 5 (Jupiter):** Añadido y sincronizado como motor principal para la ejecución del entorno de pruebas.

### 3. Modelo de Datos Estructural (`moviemodel.java`)
* **[PASADO]** **Jerarquía de Personas:** Implementación del modelo completo respetando los diagramas UML del profesor:
  * Clase base `Person`.
  * Especialización de usuario mediante `User`.
  * Introducción de la clase intermedia `Worker` para agrupar costes y flujos laborales.
  * Clases finales especializadas `Staff` y `Freelancer`.
  * Modelado de autoría mediante la clase `Author`.
* **[PASADO]** **Abstracción de Publicaciones:** 
  * Interfaz reguladora `Publication` con el contrato operativo del método `publish()`.
  * Clases base `Book` y `Multimedia` que implementan las reglas de la interfaz.
  * Clases de persistencia e inventario real para ejemplares físicos: `BookItem` y `MultimediaItem`.

### 4. Entorno de Pruebas y Validación (`testfaker.java`)
* **[PASADO]** **Pruebas Unitarias (`testLibraryModelWithFaker`):** Validación en aislamiento de la asignación de atributos aleatorios creados con Faker y gestionados de fondo por las anotaciones de Lombok.
* **[PASADO]** **Pruebas de Integración (`testLibraryIntegration`):** Verificación del comportamiento del ecosistema uniendo instancias de `Staff`, `User` y `BookItem` en un único flujo operativo de simulación lógica de biblioteca.

---

## 🛠️ Próximas Mejoras Sugeridas (Opcionales para Nota Máxima)
1. **Clase Manager:** Incorporación de una clase controladora centralizada que gestione colecciones (como listas indexadas) para automatizar el alta, baja y préstamo interactivo de publicaciones.
2. **Control de Estados (Enum):** Clasificación del inventario a través de estados reservados (`AVAILABLE`, `BORROWED`, `RESERVED`).
