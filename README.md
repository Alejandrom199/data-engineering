# OpenLearn Courses Repository

Catálogo oficial de cursos abiertos para **OpenLearn**.

## Cursos Disponibles

| Curso | Código Cert. | Nivel | Unidades | Lecciones | Labs | Duración | Versión | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Ingeniería de Datos Moderna** | `DE-01` | Progresivo (Junior a Senior) | 7 | 28 | 21 | ~48h | `1.0.0` | ![Activo](https://img.shields.io/badge/status-active-success) |

---

### Descripción del Curso de Ingeniería de Datos (`data-engineering`)
Diseñado con una progresión pedagógica integral que guía al estudiante desde los fundamentos básicos hasta el nivel senior profesional:

1. **Fundamentos y Ciclo de Vida del Dato**: Qué hace el Data Engineer, ciclo de vida de 5 etapas, manipulación de flujos de texto en Linux con pipes, reproducibilidad con Docker, Python defensivo con tipado/Pydantic y bases relacionales OLTP (PostgreSQL) con índices B-Tree.
2. **Ingestión, Formatos de Almacenamiento y Motores Locales**: Ingestión de APIs con backoff exponencial y cursores, almacenamiento columnar binario Parquet vs CSV, motores in-process vectorizados con DuckDB y Polars, y arquitectura de Data Lakes en capas (Medallion) con Hive Partitioning en S3.
3. **Modelado Dimensional y Almacenes Analíticos (DWH)**: Contraste OLTP vs OLAP en almacenes masivos (Snowflake/BigQuery), metodología Kimball con Esquema en Estrella (Hechos vs Dimensiones), Dimensiones de Cambio Lento (SCD Tipo 2 con claves subrogadas) y SQL analítico avanzado con funciones de ventana (`ROW_NUMBER`, `LAG`, `LEAD`).
4. **Computación Distribuida con Apache Spark**: Arquitectura Master/Worker (Driver y Executors), evaluación perezosa con el optimizador Catalyst, transformaciones Narrow vs Wide y el coste del Shuffle, y técnicas de producción: Broadcast Joins, mitigación de Data Skew (Salting) y prevención de OOM/Disk Spill.
5. **Arquitectura Lakehouse y Tablas Transaccionales**: Superación de las limitaciones de Data Lakes tradicionales con Delta Lake y Apache Iceberg, transacciones ACID con Transaction Log y Snapshot Isolation, operaciones atómicas de MERGE y Time Travel, y optimización física de layout con compactación (`OPTIMIZE`) y Z-Ordering multidimensional.
6. **Orquestación Robusta, Calidad y DataOps**: Grafos Acíclicos Dirigidos (DAGs) deterministas en Apache Airflow, fechas lógicas y backfilling idempotente, prevención de deadlocks con sensores en modo `reschedule`, contratos y Circuit Breakers de calidad con Great Expectations y cultura DataOps (CI/CD con GitHub Actions y Terraform).
7. **Streaming en Tiempo Real y Arquitecturas de Eventos**: Trade-offs arquitectónicos entre Batch y Streaming, el commit log inmutable distribuido de Apache Kafka, particiones y consumer groups, Change Data Capture (CDC) con Debezium leyendo directamente del WAL, y procesamiento de flujos con Watermarks y semántica Exactly-Once.

---

## Cómo Consumir este Repositorio en OpenLearn

En tu instancia de **OpenLearn**, agrega la URL remota:
```
https://github.com/Alejandrom199/data-engineering
```
OpenLearn detectará automáticamente el archivo `registry.json` e importará el curso completo de Ingeniería de Datos con validación estricta de esquemas, 21 laboratorios prácticos y simuladores de certificación oficial.
