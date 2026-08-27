# 🧮 Algoritmos y Estructuras de Datos

Este repositorio está diseñado para ser una guía organizada y progresiva del material de estudio, apuntes teóricos, ejercicios prácticos y recursos de la asignatura **Algoritmos y Estructuras de Datos (CB100)** de la Facultad de Ingeniería de la Universidad de Buenos Aires (FIUBA).

El código de clase y las guías de ejercicios viven dentro de un proyecto **Java 25 + Gradle** (`teoria/cb100/`), organizado por unidad temática: lo explicado en clase en `material/` y los ejercicios a resolver en `guia/`.

---

## 📊 Progreso del Curso

![Progreso](https://img.shields.io/badge/Progreso-En%20Cursada-brightgreen)
![Materia](https://img.shields.io/badge/FIUBA-CB100-blue)
![Cuatrimestre](https://img.shields.io/badge/Cursada-2C%202026-orange)
![Java](https://img.shields.io/badge/Java-25-red)
![Build](https://img.shields.io/badge/Build-Gradle-02303A)

---

## 👨‍🏫 Información de la Cursada

* **Modalidad:** clases no presenciales (remotas), con instancias **presenciales obligatorias** para los parciales y las defensas de trabajos grupales.
* **Días de cursada:** Miércoles (teoría) | Jueves (práctica y ejercicios de parcial)
* **Duración:** 16 semanas — 3 instancias de parcial + recuperatorios finales.
* **Repositorio de código de la cátedra:** [gschmidt-cb100/cb100](https://github.com/gschmidt-cb100/cb100)

---

## 📑 Índice de Contenidos

| Unidad | Tema Principal | Teoría | Ejercicios |
| :---: | :--- | :---: | :---: |
| 1 | Introducción al Lenguaje (Java, JVM, sintaxis, archivos) | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i01_intro/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i01_intro/) |
| 2 | Memoria: Valores, Referencias y Punteros | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i02_memoria/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i02_memoria/) |
| 3 | Abstracción, TDA y Programación Orientada a Objetos | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i03_poo/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i03_poo/) |
| 4 | Complejidad Computacional y Teorema Maestro | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i04_complejidad/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i04_complejidad/) |
| 5 | Estructuras Lineales: Vector, Pila, Cola y Listas Enlazadas | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i05_lineales/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i05_lineales/) |
| 6 | Estrategias: División y Conquista y Ordenamientos No Comparativos | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i06_estrategias/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i06_estrategias/) |
| 7 | Diccionarios, Tablas de Hashing y Resolución de Colisiones | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i07_hashing/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i07_hashing/) |
| 8 | Árboles, ABB y Árboles Autobalanceados | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i08_arboles/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i08_arboles/) |
| 9 | Heaps y Colas de Prioridad | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i09_heaps/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i09_heaps/) |
| 10 | Técnicas Algorítmicas: Backtracking, Greedy y Programación Dinámica | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i10_tecnicas/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i10_tecnicas/) |
| 11 | Grafos: Representaciones, Recorridos, Caminos Mínimos y MST | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i11_grafos/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i11_grafos/) |
| 12 | Java Profesional: Colecciones, Streams y Elección de Estructuras | [📖 Leer](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/i12_profesional/) | [💻 Ver Guía](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/guia/i12_profesional/) |

> Cada guía trae **10 preguntas teóricas** (`i01_teorico/`) y **30 ejercicios** repartidos en tres niveles: `i02_facil/`, `i03_medio/` e `i04_dificil/`.

---

## 🛠️ Detalle de los Temas

### Unidad 1: Introducción al Lenguaje
*   Tipos, variables, control de flujo, métodos y conversiones de rango.
*   `String`, `StringBuilder` y manipulación de cadenas de texto.
*   Entrada/salida, manejo de archivos (`java.nio.file.Files`) y fechas.
*   Excepciones propias, validaciones y funciones lambda.
*   Bytecode, JVM y el modelo "Write Once, Run Anywhere".

### Unidad 2: Memoria, Valores y Referencias
*   Stack vs. heap: qué vive en cada uno y por cuánto tiempo.
*   Paso de parámetros, identidad vs. igualdad (`==` vs. `equals`).
*   Objetos mutables e inmutables; copia superficial vs. copia profunda.
*   Referencias nulas y `Optional`; arreglos y aliasing.

### Unidad 3: Abstracción, TDA y POO
*   Abstracción como idea central: separar el **contrato** de la implementación.
*   Clases, encapsulamiento, invariantes y validación en el constructor.
*   Herencia, polimorfismo y clases abstractas.
*   Tipos genéricos (templates) aplicados al diseño de TDAs.

### Unidad 4: Complejidad Computacional
*   Por qué se mide en operaciones en función de `n` y no en segundos.
*   Notación asintótica y cálculo de complejidad de algoritmos iterativos.
*   Complejidad de algoritmos recursivos simples y **Teorema Maestro**.
*   Análisis amortizado y criterios de redimensión en estructuras sobre arreglo.
*   Casos de estudio: búsqueda binaria, potencia rápida, MergeSort y QuickSort.

### Unidad 5: Estructuras de Datos Lineales
*   Vector dinámico: tamaño vs. capacidad y política de crecimiento.
*   TDA Pila y TDA Cola: contrato, usos y costos.
*   Listas simplemente enlazadas, doblemente enlazadas y circulares.
*   Implementación de Lista con cursor sobre arreglo.
*   Análisis comparativo: estructuras en arreglo vs. estructuras enlazadas.

### Unidad 6: Estrategias — División y Conquista
*   Esquema de la recursividad: caso base y caso recursivo.
*   División y conquista: Torres de Hanói y algoritmo de Karatsuba.
*   Algoritmos de ordenamiento **no comparativos**: Counting Sort, Radix Sort y Bucket Sort.

### Unidad 7: Diccionarios y Tablas de Hashing
*   TDA Diccionario: contrato y casos de uso.
*   Funciones de hash y las propiedades que deben cumplir.
*   Resolución de colisiones: encadenamiento y direccionamiento abierto.
*   Factor de carga, rehashing y complejidad promedio vs. peor caso.

### Unidad 8: Árboles y Árboles de Búsqueda
*   Árboles binarios: recorridos y propiedades.
*   Árbol Binario de Búsqueda (ABB): invariante, inserción, borrado y degeneración.
*   Árboles autobalanceados (AVL): rotaciones y garantía logarítmica.
*   Árboles multivías, árbol B y Tries (autocompletado).

### Unidad 9: Heaps y Colas de Prioridad
*   Invariante de min-heap / max-heap: qué garantiza y qué no.
*   Representación de un heap sobre arreglo; `sift-up` y `sift-down`.
*   TDA Cola con Prioridad y sus aplicaciones.
*   Heapsort y construcción de heaps en tiempo lineal.

### Unidad 10: Técnicas Algorítmicas
*   Backtracking: elegir, avanzar y deshacer (N Reinas).
*   Algoritmos **Greedy**: selección de actividades y cambio de monedas.
*   **Programación Dinámica**: problema de la mochila y conteo de escaleras.
*   Criterios para decidir qué técnica aplica a cada problema.

### Unidad 11: Grafos
*   Concepto, características y tipos de grafos (dirigidos, ponderados, conexos).
*   Representaciones: lista de adyacencia vs. matriz de adyacencia.
*   Recorridos **BFS** y **DFS**; ordenamiento topológico.
*   Caminos mínimos: algoritmo de **Dijkstra**.
*   Árboles de tendido mínimo (MST): **Prim** y **Kruskal**; estructura Union-Find.

### Unidad 12: Java Profesional
*   Framework de Colecciones: `List`, `Set`, `Map` y sus implementaciones.
*   Programar contra la interfaz y no contra la implementación.
*   Streams, evaluación perezosa y pipelines de procesamiento.
*   Criterios prácticos para elegir la estructura de datos adecuada.

---

## 🗓️ Cronograma de Cursada

| Semana | Miércoles | Jueves |
| :---: | :--- | :--- |
| 1-2 | Introducción al Lenguaje | Introducción al Lenguaje |
| 3 | Punteros. Recursividad — División y conquista | Ejercicios sobre punteros |
| 4 | Concepto de TDA — Clase — Encapsulamiento | Ejercicios sobre TDA |
| 5 | TDA Vector — Templates | Ejercicios de TDA con genéricos |
| 6 | TDA Lista | TDA Lista |
| 7 | TDA Lista con cursor — TDA Pila — TDA Cola | Ejercicios de parcial: diseño e implementación de TDA |
| 8 | Complejidad algorítmica (parte 1) | Ejercicios de parcial: métodos de Lista y complejidad |
| 9 | Complejidad algorítmica (parte 2) | Ejercicios de parcial: uso de Listas y complejidad |
| 10 | TDA Conjunto: ABB, AVL | 📝 **Parcial (presencial)** |
| 11 | Árbol multivías, árbol B, Trie, array de bits | Ejercitación sobre árboles y otras estructuras |
| 12 | Tablas Hash — Cola con prioridad — Heap — Heapsort | 📝 **Parcial (presencial)** |
| 13 | TDA Grafo: concepto y recorridos | Práctica de grafos. Consultas |
| 14 | Grafos: caminos, Greedy y Programación Dinámica | 📝 **Parcial (presencial)** |
| 15 | Grafos no dirigidos. Backtracking | Práctica |
| 16 | Últimos recuperatorios | Recuperatorios y defensas de trabajos grupales (presencial) |

---

## 📂 Estructura del Repositorio

```text
.
├── README.md
├── temario.md                              ← temario oficial de la materia
├── paginas/                                ← documentos de estudio interactivos (HTML)
│   └── clase_1_y_2/
└── teoria/
    └── cb100/                              ← proyecto Java 25 + Gradle
        ├── gradlew / gradlew.bat           ← Gradle Wrapper
        ├── settings.gradle
        └── app/
            ├── build.gradle
            └── src/
                ├── main/java/ar/uba/fi/cb100/
                │   ├── material/           ← código explicado en clase, por unidad
                │   │   ├── general/        ← apunte CB100 y plan de estudios
                │   │   ├── i01_intro/  ...  i12_profesional/
                │   ├── guia/               ← ejercicios por unidad
                │   │   └── iNN_tema/
                │   │       ├── i01_teorico/   ← 10 preguntas teóricas
                │   │       ├── i02_facil/     ← 10 ejercicios
                │   │       ├── i03_medio/     ← 10 ejercicios
                │   │       └── i04_dificil/   ← 10 ejercicios
                │   └── clases/a2026/c02/   ← material del cuatrimestre en curso
                │       ├── s01/            ← cronograma y clase 1
                │       └── tps/tp1/        ← enunciado y datos del TP 1
                └── test/java/ar/uba/fi/cb100/  ← tests JUnit 5
```

---

## ⚙️ Cómo compilar y ejecutar

El proyecto trae el **Gradle Wrapper**, así que no hace falta instalar Gradle: sólo el **JDK 25** (recomendado Temurin / Eclipse Adoptium).

```bash
cd teoria/cb100
./gradlew run          # en Windows: gradlew.bat run
```

| Qué querés hacer | Comando |
| :--- | :--- |
| Ejecutar el programa principal | `./gradlew run` |
| Compilar todo | `./gradlew build` |
| Correr los tests | `./gradlew test` |
| Limpiar los compilados | `./gradlew clean` |

---

## 🧰 Herramientas y Recursos

* **Lenguaje:** Java 25 (JDK Temurin / Eclipse Adoptium).
* **Build:** Gradle (vía Wrapper) · **Tests:** JUnit 5.
* **IDE recomendado:** IntelliJ IDEA (Community o Ultimate).
* **Apunte de la materia:** [CB100-Apunte.pdf](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/material/general/CB100-Apunte.pdf)
* **Trabajos Prácticos:** [TP 1 — Registro de préstamos](./teoria/cb100/app/src/main/java/ar/uba/fi/cb100/clases/a2026/c02/tps/tp1/enunciado.md)

---

## 📝 Notas

* El contenido se actualiza semanalmente a medida que avanza el cuatrimestre.
* Los apuntes teóricos y las guías prácticas sirven como registro y acompañamiento del aprendizaje personal.
* `teoria/cb100/` es un clon del repositorio de código de la cátedra; los ejercicios resueltos se agregan sobre esa estructura.

---

> **“Los algoritmos son la poesía de la computación: elegantes, precisos e infinitamente reutilizables.”**
