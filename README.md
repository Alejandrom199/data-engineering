# OpenLearn Courses Repository

Catálogo oficial de cursos abiertos para **OpenLearn**.

## Cursos Disponibles

| Curso | Código Cert. | Nivel | Unidades | Lecciones | Labs | Duración | Versión | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Ingeniería de Datos Moderna** | `DE-01` | Intermedio | 6 | 25 | 18 | ~36h | `1.0.0` | ![Activo](https://img.shields.io/badge/status-active-success) |

---

### Descripción del Curso de Ingeniería de Datos (`data-engineering`)
Diseñado según los estándares pedagógicos de OpenLearn (micro-learning, lecciones de 10-14m, diagramas interactivos, flashcards y post-mortems reales):

1. **Ingestión, Almacenamiento y Formatos**: Apache Parquet vs CSV/JSON, Snappy, Hive Partitioning en S3/GCS, Small File Problem, generadores lazy en Python e ingestión HTTP con backoff y jitter.
2. **Modelado Relacional, SQL Analítico y DWH**: OLTP vs OLAP, Ralph Kimball Star Schema, Dimensiones de Cambio Lento (SCD Tipo 2), funciones de ventana SQL (`ROW_NUMBER`, `LAG`, `LEAD`) y optimización con `EXPLAIN ANALYZE`.
3. **Computación Distribuida con Apache Spark**: Driver vs Executors, transformaciones Narrow vs Wide y coste del Shuffle, optimizador Catalyst, mitigación de Data Skew con Salting y Broadcast Joins, y prevención de OOM/Disk Spill.
4. **Arquitectura Lakehouse y Tablas ACID**: Transacciones ACID con Delta Lake y Apache Iceberg, Snapshot Isolation, Time Travel y rollback de versiones, operaciones incrementales MERGE, y optimización con Z-Ordering.
5. **Orquestación Robusta, Calidad y DataOps**: DAGs declarativos en Apache Airflow, programación idempotente con `logical_date`, sensores en modo `reschedule`, contratos de calidad con Great Expectations como Circuit Breakers y CI/CD con DataOps.
6. **Streaming en Tiempo Real y CDC**: Arquitecturas basadas en eventos con Apache Kafka, particiones y consumer groups, semántica Exactly-Once y deduplicación idempotente, Event Time y Watermarks, y Change Data Capture (CDC) con Debezium.

---

## Cómo Consumir este Repositorio en OpenLearn

En tu instancia de **OpenLearn**, agrega la URL remota:
```
https://github.com/Alejandrom199/data-engineering
```
OpenLearn detectará automáticamente el archivo `registry.json` e importará el curso de Ingeniería de Datos con validación completa y soporte para laboratorios guiados y certificación.
