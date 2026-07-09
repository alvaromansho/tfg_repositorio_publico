# Large Language Models en el Dominio Tabular: Estudio Comparativo en Clasificación de Datos Médicos

> Universidad Rey Juan Carlos - Escuela de Ingeniería de Fuenlabrada
> Grado en Ciencia e Ingeniería de Datos - Trabajo Fin de Grado

| | |
|---|---|
| **Autor** | Álvaro Manso Horcajada |
| **Tutor** | Cristian David Chushig Muzo |
| **Cotutor** | Luis Bote Curiel |

## Descripción

Este Trabajo Fin de Grado evalúa la capacidad de los *Large Language Models* (LLMs) de código abierto para clasificar datos médicos tabulares, comparando su rendimiento y coste computacional frente a modelos de aprendizaje automático tradicionales (árbol de decisión, Random Forest y XGBoost).

Se evalúan nueve LLMs (Qwen, DeepSeek y Mistral, en tres tamaños cada uno) sobre tres conjuntos de datos clínicos del *UC Irvine Machine Learning Repository*, combinando dos técnicas de serialización, tres estrategias de *prompting* (*zero-shot*, *few-shot* y *few-shot* con recuperación aumentada por generación, RAG) y tres semillas aleatorias.

## Estructura del repositorio

- **`tfg_figuras_eda_cancer/`**, **`tfg_figuras_eda_dia/`**, **`tfg_figuras_eda_heart/`** - Figuras del análisis exploratorio, una carpeta por conjunto de datos.

- **`tfg_figuras_resultados/`** - Figuras de la comparación de resultados.

- **`tfg_tablas_resultados/`** - Tablas en LaTeX de la comparación de resultados.

- **`README.md`** - Este documento.

- **`drug_induced_autoimmunity_prediction_clean.csv`** - Dataset DIA tras el preprocesamiento.

- **`requirements.txt`** - Dependencias de Python y sus versiones exactas.

- **`resultados_llms.csv`** - Resultados consolidados de los LLMs, pipeline base.

- **`resultados_modelos_tradicionales.csv`** - Resultados consolidados: árbol de decisión, Random Forest, XGBoost.

- **`resultados_rag.csv`** - Resultados consolidados de los LLMs, pipeline RAG.

- **`tfg_notebook.ipynb`** - Notebook con la totalidad del código: adquisición y preprocesamiento de datos, modelos tradicionales, pipeline de LLMs, RAG y comparación de resultados.

## Reproducibilidad

La ejecución completa del notebook requiere GPU y horas de cómputo, al sumar el pipeline de LLMs y RAG más de 800 experimentos.

Las dependencias, con las versiones exactas empleadas en la ejecución, están fijadas en `requirements.txt`:

```bash
pip install -r requirements.txt
```

Los resultados consolidados (`resultados_llms.csv`, `resultados_modelos_tradicionales.csv`, `resultados_rag.csv`), junto con `tfg_figuras_resultados/` y `tfg_tablas_resultados/`, se conservan en este repositorio para que puedan consultarse directamente, sin necesidad de reejecutar el pipeline. 