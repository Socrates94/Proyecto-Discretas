# Proyecto Discretas: Análisis de Propiedades de las Relaciones

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://java.com/)
[![Maven](https://img.shields.io/badge/Maven-C71A22?style=for-the-badge&logo=apachemaven&logoColor=white)](https://maven.apache.org/)

Este proyecto fue desarrollado como parte de un trabajo académico en el área de **Matemáticas Discretas**. Es una aplicación en consola escrita en Java que permite definir un conjunto y una relación sobre él, para posteriormente analizar exhaustivamente sus propiedades matemáticas y generar visualizaciones gráficas interactivas.

## 🚀 Características Principales

La aplicación solicita al usuario ingresar un conjunto de números enteros y los pares ordenados que conforman la relación, y luego evalúa las siguientes propiedades:

*   **Reflexiva e Irreflexiva:** Comprobación de la existencia (o ausencia) de los pares de la forma `(a, a)` para todo elemento en el conjunto.
*   **Simétrica y Asimétrica:** Evaluación de la existencia de pares recíprocos `(a, b)` y `(b, a)`.
*   **Antisimétrica:** Verificación de que si `(a, b)` y `(b, a)` existen, entonces `a = b`.
*   **Transitiva:** Comprobación de que si existen `(a, b)` y `(b, c)`, entonces también existe `(a, c)`.

Además, basándose en el cumplimiento de estas propiedades elementales, el programa determina si se trata de tipos de relaciones especiales y ofrece funcionalidades avanzadas:

### Relación de Equivalencia
*(Cumple: Reflexiva, Simétrica y Transitiva)*
*   **Clases de Equivalencia y Particiones:** Agrupa el conjunto en subconjuntos disjuntos.
*   **Matriz de Equivalencia:** Genera la matriz booleana que representa la relación.
*   **Grafo Visual:** Utiliza la librería GraphStream para mostrar la representación gráfica interactiva de la relación.

### Relación de Orden Parcial
*(Cumple: Reflexiva, Antisimétrica y Transitiva)*
*   **Diagrama de Hasse:** Simplifica el grafo eliminando ciclos reflexivos y aristas transitivas redundantes, y lo renderiza gráficamente de forma organizada.
*   **Verificación de Retícula (Lattice):** Evalúa computacionalmente si todo par de elementos tiene un supremo (mínima cota superior) y un ínfimo (máxima cota inferior).

### Relación General
Si la relación no es ni de equivalencia ni de orden parcial, el sistema generará una vista interactiva del grafo general dirigido con la relación ingresada.

## 🛠️ Tecnologías Utilizadas

*   **Lenguaje:** Java
*   **Gestor de Dependencias:** Maven (`pom.xml`)
*   **Visualización de Grafos:** [GraphStream](https://graphstream-project.org/) - Se utiliza para renderizar los diagramas de Hasse y los grafos de las relaciones utilizando Swing.

## 📋 Requisitos Previos

*   Java Development Kit (JDK) 11 o superior.
*   Maven instalado en el sistema.

## ⚙️ Instalación y Ejecución

1. Clona el repositorio en tu máquina local:
   ```bash
   git clone https://github.com/Socrates94/Proyecto-Discretas.git
   ```

2. Accede al directorio del proyecto:
   ```bash
   cd Proyecto-Discretas
   ```

3. Compila el proyecto y descarga las dependencias utilizando Maven:
   ```bash
   mvn clean install
   ```

4. Ejecuta la clase principal (`PropiedadesRelaciones`):
   ```bash
   mvn exec:java -Dexec.mainClass="org.example.PropiedadesRelaciones"
   ```
   *(También puedes ejecutar el proyecto directamente desde tu IDE favorito importándolo como un proyecto Maven).*

## 💡 Uso del Programa

Al ejecutar la aplicación, aparecerá un menú interactivo en la consola:

1. Selecciona la opción `1` para ingresar un conjunto y una relación.
2. **Ingreso del Conjunto:** Introduce elementos enteros uno por uno. Cuando finalices, escribe `fin`.
3. **Ingreso de la Relación:** Introduce los pares en formato `x,y` (por ejemplo, `1,2`). Cuando finalices, escribe `fin`.
4. El programa analizará los datos e imprimirá un reporte detallado en la consola verificando cada propiedad y mostrando los pares faltantes o encontrados.
5. Si aplica, se abrirá automáticamente una ventana gráfica de Java (Swing) mostrando el grafo o el diagrama de Hasse.

---

> **Nota del autor:** Este proyecto fue uno de los primeros desarrollos durante la maestría, sirviendo como una herramienta clave para comprender empíricamente la teoría de grafos y las relaciones en matemáticas discretas. Recientemente depurado para fines de portafolio y lectura.
