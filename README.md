# TP2 - Swing o no swing, esa es la cuestión

## Integrantes

* Agustina Mac kay
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
git clone https://github.com/franovando/swing_prediction.git
```

## 2. Instalar uv (si aún no se encuentra instalado)

Consultar la [documentación oficial](https://docs.astral.sh/uv/getting-started/installation/) de `uv` para la instalación correspondiente al sistema operativo.

## 3. Crear el entorno e instalar las dependencias

Desde la carpeta raíz del proyecto ejecutar en la terminal:

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
├── notebooks/
│   ├── 00_target_definition.ipynb 
│   ├── 01_features.ipynb  
│   ├── 02_eda.ipynb  
│   ├── 03.1_regresion_logistica.ipynb  
│   ├── 03.2_lgbm.ipynb  
│   └── 03.3_xgboost.ipynb             
│
├── outputs/ 
│   ├── lightgbm_1/ 
│   ├── lightgbm_2/ 
│   ├── regresion_logistica/
│   ├── xgboost_1/
│   └── xgboost_1/
├── .gitignore
├── .python-version
├── pyproject.toml
├── uv.lock
└── README.md
```

Las carpeta `data/` y `outputs/` se encuentran vacías, ya que contienen archivos derivados o provistos externamente.

---

# Ejecución del proyecto

Una vez guardados los datos, las notebooks deben ejecutarse en el orden que están enumeradas.

---