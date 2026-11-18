# Diabetes Classification: Machine Learning aplicado a salud

Proyecto de clasificación binaria con el conjunto de datos **Pima Indians Diabetes**. El objetivo es documentar un flujo reproducible de aprendizaje automático: análisis exploratorio, preparación de datos, comparación de modelos, validación cruzada, evaluación y explicabilidad.

> **Uso educativo y de investigación.** Este proyecto no es una herramienta clínica, no realiza diagnósticos y no debe utilizarse para tomar decisiones sobre la atención de personas.

## Objetivos
- Explorar estructura, distribución y calidad de los datos.
- Revisar ceros que pueden representar mediciones no registradas.
- Comparar modelos bajo un esquema común.
- Estimar rendimiento mediante validación cruzada estratificada.
- Evaluar con métricas relevantes para clasificación binaria.
- Interpretar variables relevantes y discutir limitaciones.

## Dataset
- **Nombre:** Pima Indians Diabetes Database.
- **Fuente:** [Kaggle – Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database).
- **Tamaño de referencia:** 768 observaciones y 8 variables predictoras, más `Outcome`.
- **Objetivo:** `Outcome` (0 = resultado negativo; 1 = resultado positivo en el dataset).

La notebook descarga el archivo mediante `kagglehub`. No se incluyen datos en el repositorio. Si Kaggle solicita autenticación en tu entorno, configurá sus credenciales sin subir tokens ni secretos.

## Estructura
```text
machine-learning-diabetes/
├── README.md
├── notebooks/
│   └── diabetes_classification.ipynb
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Ejecución local
Se recomienda Python 3.10 o superior.

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
jupyter lab
```

Abrí `notebooks/diabetes_classification.ipynb` y ejecutá las celdas en orden.

GitHub permite visualizar la notebook, pero no ejecuta sus celdas. Para ejecutar Python necesitás un entorno Jupyter local u otro servicio compatible.

## Metodología
1. Carga y revisión inicial de datos.
2. EDA univariado y bivariado.
3. Revisión y tratamiento explícito de ceros potencialmente faltantes en variables seleccionadas.
4. División estratificada entrenamiento/prueba.
5. Pipelines para evitar fuga de información (*data leakage*).
6. Comparación de Regresión Logística, Árbol de Decisión, Random Forest y XGBoost (si está instalado).
7. Validación cruzada estratificada sobre entrenamiento.
8. Evaluación final sobre prueba.
9. Importancia por permutación.

## Métricas
Accuracy, balanced accuracy, Precision, Recall (sensibilidad), F1, especificidad y ROC-AUC. Deben interpretarse en conjunto: los falsos negativos y positivos tienen implicancias diferentes.

## Limitaciones
- Dataset pequeño y de contexto/población específicos.
- La distribución puede no representar otras poblaciones.
- Los ceros usados como posibles valores faltantes requieren una decisión metodológica.
- Los resultados no demuestran validez clínica, utilidad prospectiva ni generalización.
- La importancia de variables describe el comportamiento del modelo; no implica causalidad.

## Tecnologías
Python · pandas · NumPy · Matplotlib · Seaborn · scikit-learn · XGBoost · Jupyter

## Autora
**Amalia Guaymás Canavire**  
Data Scientist | Machine Learning | Responsible AI

[GitHub](https://github.com/AmaliaGuaymasCanavire) · [Sitio web](https://amaliaguaymascanavire.github.io/)

## Licencia
Distribuido bajo licencia MIT. Ver `LICENSE`.
