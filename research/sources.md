# 📚 Fuentes Oficiales y Bibliografía del Mentor

Este curso fundamenta cada lección técnica en literatura académica de referencia, documentación técnica oficial y estándares de la industria.

---

## 1. Ciencias de la Computación, Sistemas Operativos y Arquitectura

- **Tanenbaum, Andrew S., & Bos, Herbert.** (2014). *Modern Operating Systems (4th Edition)*. Pearson.
  - Capítulos clave: Procesos, Hilos, Gestión de Memoria Virtual, Paginación, Sistemas de Archivos y E/S.
- **Hennessy, John L., & Patterson, David A.** (2017). *Computer Architecture: A Quantitative Approach (6th Edition)*. Morgan Kaufmann.
  - Jerarquía de memoria, caches L1/L2/L3, ancho de banda vs latencia, DMA (Direct Memory Access).
- **Cormen, Thomas H., Leiserson, Charles E., Rivest, Ronald L., & Stein, Clifford.** (2022). *Introduction to Algorithms (4th Edition)*. MIT Press.
  - Notación asintótica (Big-O), Hash Tables, Algoritmos de ordenamiento externo (*External Merge Sort*), B-Trees.
- **Shotts, William.** (2019). *The Linux Command Line (2nd Edition)*. No Starch Press.
  - Flujos estándar (`stdin`, `stdout`, `stderr`), tuberías, filtros (`grep`, `sed`, `awk`).

---

## 2. Ingeniería de Software y Python Avanzado

- **Ramalho, Luciano.** (2021). *Fluent Python (2nd Edition)*. O'Reilly Media.
  - Generadores y corrutinas (`yield`), protocolo de iteradores, `itertools`, gestión de contexto (`contextlib`), tipado estático con `typing` y dataclasses.
- **Percival, Harry, & Gregory, Bob.** (2020). *Architecture Patterns with Python*. O'Reilly Media.
  - Repository pattern, tolerancia a fallos, manejo de excepciones de dominio, inyección de dependencias.
- **Documentación Oficial de Python 3.12+**:
  - `https://docs.python.org/3/library/itertools.html`
  - `https://docs.python.org/3/library/typing.html`
  - `https://docs.python.org/3/howto/functional.html`

---

## 3. Bases de Datos, Modelado OLTP/OLAP y Data Warehousing

- **Kleppmann, Martin.** (2017). *Designing Data-Intensive Applications: The Big Ideas Behind Reliable, Scalable, and Maintainable Systems*. O'Reilly Media.
  - Modelos de datos, índices B-Tree vs LSM-Trees, semántica de transacciones ACID, aislamiento de transacciones (Dirty Reads, Phantom Reads, SSI).
- **Petrov, Alex.** (2019). *Database Internals: A Deep Dive into How Distributed Data Systems Work*. O'Reilly Media.
  - Estructuras en disco, páginas, Write-Ahead Logging (WAL), buffer management.
- **Kimball, Ralph, & Ross, Margy.** (2013). *The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling (3rd Edition)*. Wiley.
  - Esquema en Estrella, tablas de hechos transaccionales, periódicas y acumuladas, dimensiones conformadas, dimensiones lentamente cambiantes (SCD Tipo 1, 2 y 3).
- **PostgreSQL 16 Documentation**:
  - `https://www.postgresql.org/docs/current/wal-intro.html`
  - `https://www.postgresql.org/docs/current/using-explain.html`
  - `https://www.postgresql.org/docs/current/queries-with.html`

---

## 4. Sistemas Distribuidos, Big Data y Almacenamiento Masivo

- **Brewer, Eric.** (2012). *CAP Twelve Years Later: How the "Rules" Have Changed*. Computer, IEEE.
- **Damji, Jules S., et al.** (2020). *Learning Spark: Lightning-Fast Data Analytics (2nd Edition)*. O'Reilly Media.
  - Arquitectura Spark Catalyst, Catalyst Optimizer, Tungsten Engine, RDDs vs DataFrames, Shuffles, Data Skew y Salting.
- **Apache Parquet Documentation & Format Specification**:
  - `https://parquet.apache.org/docs/file-format/`
  - Codificación RLE, Bit-Packing, estadísticas a nivel de Row Group, Predicate Pushdown y Dictionary Encoding.
- **Delta Lake / Apache Iceberg Documentation**:
  - `https://delta.io/learn/blogs/`
  - `https://iceberg.apache.org/spec/`
  - Control de concurrencia optimista (OCC), tablas ACID sobre almacenamiento de objetos, metadatos y Time Travel.

---

## 5. Orquestación, Observabilidad y DataOps

- **Documentación Oficial de Apache Airflow 2.9+**:
  - `https://airflow.apache.org/docs/apache-airflow/stable/`
  - Concepto de DAG, `logical_date` vs `start_date`, Idempotencia de pipelines, Sensors y Dynamic DAG generation.
- **Great Expectations Documentation**:
  - `https://docs.greatexpectations.io/docs/`
  - Data Contracts, validación de esquemas en tiempo de ingesta, Circuit Breakers.
- **HashiCorp Terraform Documentation**:
  - `https://developer.hashicorp.com/terraform/docs`
  - IaC declarativo, State locking, Providers y Best Practices en Cloud Storage.

---

## 6. Streaming y Procesamiento en Tiempo Real

- **Shapira, Gwen, et al.** (2021). *Kafka: The Definitive Guide (2nd Edition)*. O'Reilly Media.
  - Estructura de particiones de Kafka, PageCache del kernel, protocolo de Rebalance de Consumer Groups, garantías At-least-once y Exactly-once (transaccional).
- **Akidau, Tyler, Chernyak, Slava, & Lax, Reuven.** (2018). *Streaming Systems: The What, Where, When, and How of Large-Scale Data Processing*. O'Reilly Media.
  - Event-Time vs Processing-Time, Ventanas de agregación (Tumbling, Sliding, Session), Watermarks, Triggers y reconciliación de datos tardíos (*Late data*).
- **Debezium Official Documentation**:
  - `https://debezium.io/documentation/reference/stable/`
  - Decodificación lógica de PostgreSQL (pgoutput), CDC no invasivo mediante lectura de WAL hacia tópicos de Kafka.
