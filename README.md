# TP2 - Swing o no swing, esa es la cuestión

## Integrantes

* Agustina Mackey
* Francisco Ovando
* Simón Gazze

---

# Objetivo

Este repositorio contiene el desarrollo del Trabajo Práctico 2 de Programación en Python.

El objetivo consiste en estimar de manera adecuada la probabilidad de que un bateador realice un **swing** frente a un determinado lanzamiento (*pitch*), utilizando información correspondiente a una temporada de datos de la Major League Baseball.

A partir del conjunto de datos **temporada1.parquet**, se realiza el proceso de exploración, ingeniería de variables, entrenamiento y evaluación de distintos modelos de machine learning.

Posteriormente, se utilizan los modelos para generar predicciones de la probabilidad de swing sobre los lanzamientos de otra temporada (**temporada2.parquet**), obteniendo como resultado final el archivo **validacion.parquet**, que contiene el identificador de cada lanzamiento (`pitch_id`) y su probabilidad estimada de swing.

---

# Requisitos

Para ejecutar el proyecto es necesario contar con:

* Python 3.14.
* `uv` instalado.

---

# Instalación del entorno

## 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

## 2. Instalar uv (si aún no se encuentra instalado)

Consultar la documentación oficial de uv para la instalación correspondiente al sistema operativo.

## 3. Crear el entorno e instalar las dependencias

Desde la carpeta raíz del proyecto ejecutar:

```bash
uv sync
```

Este comando:

* crea automáticamente el entorno virtual del proyecto;
* instala todas las dependencias especificadas;
* garantiza que se utilicen exactamente las mismas versiones de paquetes empleadas durante el desarrollo.

---

# Datos

Debido a las restricciones establecidas para el trabajo práctico, los archivos de datos no forman parte del repositorio.

Antes de ejecutar el proyecto, deben copiarse los archivos .parquet provistos por la cátedra dentro de la siguiente estructura:

```text
data/
└── raw/
    ├── temporada1.parquet
    └── temporada2.parquet
```

---

# Organización del repositorio

```text
.
├── data/
│   ├── raw/                # Datos originales
│   └── processed/          # Datos procesados
│
├── notebooks/              # Análisis exploratorio y modelado
│
├── outputs/
│
├── .gitignore
├── pyproject.toml
├── uv.lock
└── README.md
```

Las carpeta `data/` y `outputs/` se encuentran excluidas del control de versiones mediante `.gitignore`, ya que contienen archivos derivados o provistos externamente.

---

# Ejecución del proyecto

*Esta sección será completada una vez definido el pipeline principal.*

El objetivo es que el proyecto pueda ejecutarse mediante un único comando, reproduciendo todo el flujo de procesamiento y entrenamiento.

---

# Generación de `validacion.parquet`

*Esta sección será completada una vez implementado el modelo final.*

Aquí se documentará el procedimiento necesario para generar el archivo de predicciones a partir de `temporada2.parquet`.

