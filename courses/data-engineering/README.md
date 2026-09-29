# 🧠 Mentor de Ingeniería de Datos (Nivel 0 → Experto)

[![OpenLearn Course](https://img.shields.io/badge/OpenLearn-Course-blue.svg)](https://github.com/alenj0x1/open-learn)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](LICENSE)
[![Status: Active](https://img.shields.io/badge/Status-Active-emerald.svg)](#)
[![Level: Beginner to Expert](https://img.shields.io/badge/Level-0%20%E2%86%92%20Expert-purple.svg)](#)

> **Mentoría de élite en Ingeniería de Datos.** Un currículum integral, riguroso y autosuficiente diseñado para transformar a cualquier persona desde el nivel 0 absoluto hasta un dominio profesional y profundo de la disciplina. Cero atajos, máxima profundidad técnica.

---

## 📌 Contexto y Filosofía de Aprendizaje

- **Nivel de entrada:** 0 absoluto (no se asume ningún conocimiento previo de programación, sistemas ni matemáticas avanzadas).
- **Comprensión profunda vs. memorización:** Se enseña primero el principio físico y matemático (teoría de la computación, hardware, álgebra relacional, sistemas distribuidos) antes de tocar herramientas concretas.
- **Autosuficiencia:** Todas las explicaciones, diagramas, laboratorios y proyectos contienen el contexto necesario para ser ejecutados y comprendidos.
- **Tono directo y honesto:** La ingeniería de datos de producción es exigente. Si un concepto requiere horas de depuración o fundamentos matemáticos, se aborda con claridad y rigor.
- **Dedicación estimada:** 9 a 12 meses de trabajo intensivo (15 a 20 horas por semana).

---

## 🗺️ Mapa de Ruta General (6 Bloques)

```
[BLOQUE 1: Fundamentos de CS y SO]
  ├── Fase 1: Lógica Formal, Conjuntos y Grafos (DAGs)
  ├── Fase 2: Arquitectura de Computadores, Memoria y Linux Headless
  ├── Fase 3: Algoritmos, Complejidad (Big-O) y External Sort
  └── 🏆 Proyecto 1: Procesador de Logs de Bajo Nivel (<50MB RAM)
       ↓
[BLOQUE 2: Programación Robusta y Adquisición]
  ├── Fase 1: Python Avanzado, Generadores (yield) y Gestión de Memoria
  ├── Fase 2: Redes, HTTP/TCP, Paginación, Backoff Exponencial y Circuit Breaker
  └── 🏆 Proyecto 2: Extractor Resiliente de Alta Concurrencia (80%+ Coverage)
       ↓
[BLOQUE 3: Modelado Relacional, OLTP y OLAP]
  ├── Fase 1: Motores Transaccionales (PostgreSQL), ACID e Índices B-Tree
  ├── Fase 2: SQL Analítico Avanzado, CTEs y Funciones de Ventana
  ├── Fase 3: Data Warehousing, Esquema en Estrella y Dimensiones SCD Tipo 2
  └── 🏆 Proyecto 3: Pipeline ETL Idempotente Hacia Data Warehouse Local
       ↓
[BLOQUE 4: Sistemas Distribuidos y Big Data]
  ├── Fase 1: Teorema CAP, Formatos Columnares (Parquet) y Almacenamiento S3
  ├── Fase 2: Data Lakes y Lakehouses ACID (Delta Lake / Apache Iceberg)
  ├── Fase 3: Cómputo Distribuido con Apache Spark (Evitar Skew, Salting, Shuffles)
  └── 🏆 Proyecto 4: Pipeline Distribuido de Alto Rendimiento en MinIO/Spark
       ↓
[BLOQUE 5: Orquestación, Calidad y DataOps]
  ├── Fase 1: Orquestación Basada en Grafos (Apache Airflow, Sensores y Backfill)
  ├── Fase 2: Calidad de Datos (Great Expectations) y Circuit Breakers de Esquema
  ├── Fase 3: Infraestructura como Código (Terraform), Docker y CI/CD (GitHub Actions)
  └── 🏆 Proyecto 5: Plataforma DataOps Automatizada y Contenerizada
       ↓
[BLOQUE 6: Streaming y Procesamiento en Tiempo Real]
  ├── Fase 1: Logs Inmutables y Mensajería con Apache Kafka (Consumer Groups, Semánticas)
  ├── Fase 2: Stream Processing (Apache Flink / Spark Streaming, Event-Time y Watermarks)
  ├── Fase 3: Change Data Capture (Debezium + WAL) y Arquitectura Kappa
  └── 🏆 Proyecto Final: Arquitectura Kappa de Detección de Fraude en Tiempo Real
```

---

## 📂 Estructura del Curso

Este curso sigue la especificación estándar de **[OpenLearn](https://github.com/alenj0x1/open-learn)**:

```text
courses/data-engineering/
├── README.md                      # Documentación y guía del mentor
├── course.json                    # Manifiesto del curso y configuración de dominios
├── .gitignore                     # Configuración de exclusiones Git
├── research/                      # Material de referencia, bibliografía y plan de estudio
│   ├── README.md
│   ├── sources.md
│   ├── study-plan.md
│   └── syllabus.json
├── exams/                         # Evaluaciones diagnósticas e intermedias
│   ├── diagnostic.json
│   ├── midterm-systems-sql.json
│   └── final-distributed-streaming.json
└── units/
    ├── 01-fundamentos-cs-so/      # Bloque 1
    ├── 02-programacion-adquisicion/# Bloque 2
    ├── 03-modelado-oltp-olap/     # Bloque 3
    ├── 04-sistemas-distribuidos-bigdata/ # Bloque 4
    ├── 05-orquestacion-calidad-dataops/  # Bloque 5
    └── 06-streaming-tiempo-real/  # Bloque 6
```

Cada unidad contiene:
- `unit.json`: Manifiesto de la unidad, objetivos y lista de lecciones/laboratorios.
- `project.json`: Proyecto integrador del bloque con rúbrica detallada.
- `case-studies.json`: Análisis de casos reales de producción e incidentes de datos.
- `questions.json`: Banco de preguntas conceptuales y de análisis de código.
- `lessons/`: Lecciones teóricas autosuficientes con diagramas de flujo y términos clave.
- `labs/`: Laboratorios prácticos guiados con código reproducible y criterios de verificación.

---

## 🛠️ Entorno de Trabajo Requerido

Para completar todas las prácticas y proyectos de este curso, necesitarás:

1. **Sistema Operativo:** Linux (Ubuntu 22.04 LTS o superior) o Windows con **WSL2** (Ubuntu).
2. **Terminal y Shell:** Bash, `coreutils`, `awk`, `sed`, `grep`, `jq`, `curl`.
3. **Lenguajes:**
   - **Python:** 3.11 o superior (`uv` o `poetry` para gestión de dependencias).
   - **Java / JVM:** OpenJDK 17 (requerido para Apache Spark y Kafka).
4. **Bases de Datos y Motores:**
   - **PostgreSQL:** 16+.
   - **Docker y Docker Compose:** Para levantar clústeres locales de MinIO, Spark, Kafka, Debezium y Airflow.
5. **Herramientas de Infraestructura:**
   - **Terraform:** 1.8+.
   - **Git:** Control de versiones y flujos de trabajo en equipo.

---

## 🚀 Cómo Usar Este Curso

### Opción A: Usar este repositorio en OpenLearn
Si tienes una instancia de OpenLearn:
1. Registra este repositorio como remote en **Explorar Cursos → Remotos**.
2. Instala el curso **Mentor de Ingeniería de Datos**.
3. Todo el contenido interactivo, lecciones, flashcards y laboratorios estarán disponibles en la plataforma.

### Opción B: Trabajar como Repositorio Git Independiente
Si deseas publicar este curso como tu propio repositorio personal en GitHub:
```bash
# 1. Navegar a la carpeta del curso
cd courses/data-engineering

# 2. Inicializar un repositorio Git
git init
git branch -M main

# 3. Añadir todos los archivos y realizar el primer commit
git add .
git commit -m "feat: initial commit of data engineering mentor course"

# 4. Vincular con tu repositorio remoto de GitHub
git remote add origin https://github.com/<TU-USUARIO>/<TU-REPOSITORIO>.git
git push -u origin main
```

---

## 📜 Licencia

Todo el contenido pedagógico de este curso está licenciado bajo **[Creative Commons Atribución-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](LICENSE)**.
