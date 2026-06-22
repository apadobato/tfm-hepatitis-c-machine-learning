# 🧬 Clasificación de estadios de enfermedad hepática asociada a hepatitis C mediante Machine Learning
Trabajo Final de Máster — Bioinformática y Bioestadística

Barcelona, 2026

Autora: Ana Paula Adobato 

# 📋 Descripción del proyecto
Este proyecto desarrolla y compara modelos de machine learning supervisado para clasificar los distintos estadios de enfermedad hepática asociada a hepatitis C (sano, hepatitis, fibrosis y cirrosis) a partir de parámetros clínicos y bioquímicos de uso rutinario, sin necesidad de pruebas invasivas ni tecnología especializada.

# 🎯 Objetivo
Demostrar que analíticas clínicas estándar (ALT, AST, GGT, albúmina, bilirrubina, entre otras) pueden alimentar modelos interpretables con valor diagnóstico real, aplicables en entornos clínicos con recursos limitados.

# 📁 Contenido del repositorio
ArchivoDescripcióntfm_hepatitis_c_ml.ipynbNotebook completo con preprocesamiento, EDA y modelosTrabajo_final_de_master_Ana_Paula_Adobato.pdfDocumento completo del TFM

# 🗂️ Dataset

Fuente: Dataset proporcionado por el programa de máster (basado en datos clínicos de referencia)


Tamaño: 608 individuos tras preprocesamiento


Variables: edad, sexo y 10 biomarcadores bioquímicos (ALB, ALP, ALT, AST, BIL, CHE, CHOL, CREA, GGT, PROT)


Clases: Sano (87,7%) · Hepatitis (3,9%) · Fibrosis (3,5%) · Cirrosis (4,9%)


# ⚙️ Metodología

Imputación de valores faltantes con la mediana


Estandarización con StandardScaler (solo para modelos de regresión logística)


División entrenamiento/prueba 80/20 con estratificación por clase


Manejo del desbalance de clases con class_weight='balanced'


Evaluación mediante accuracy, recall, F1-score y matriz de confusión




# 🤖 Modelos evaluados
Se desarrollaron y compararon tres modelos de clasificación supervisada:


1. Regresión logística estándar

Accuracy: 0,95 · Macro avg F1: 0,75 · Macro avg Recall: 0,70


2. Random Forest


Accuracy: 0,93 · Macro avg F1: 0,61 · Macro avg Recall: 0,57


3. Regresión logística ponderada (class_weight='balanced')


Accuracy: 0,94 · Macro avg F1: 0,78 · Macro avg Recall: 0,84

# 🏆 Resultado principal
La regresión logística ponderada fue el modelo más útil clínicamente, alcanzando una sensibilidad del 80% para hepatitis, 75% para fibrosis y 83% para cirrosis, manteniendo una accuracy global del 94%.
Las variables con mayor peso predictivo fueron AST, GGT, bilirrubina, ALP y albúmina, coherentes con la fisiopatología del daño hepático.

# 🛠️ Tecnologías utilizadas

Lenguaje: Python 3.10


Entorno: Google Colaboratory


Librerías: pandas · numpy · scikit-learn · matplotlib · seaborn



# 📊 Visualizaciones incluidas

Distribución de categorías diagnósticas


Mapa de calor de correlaciones entre variables clínicas


Boxplots de biomarcadores por estadio de enfermedad


Matrices de confusión de los tres modelos



# 📬 Contacto
Ana Paula Adobato

https://www.linkedin.com/in/ana-paula-adobato/ · adobatoa@gmail.com
