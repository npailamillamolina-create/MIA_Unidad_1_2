
# Métodos de Inteligencia Artificial
## Universidad Mayor — Unidades 1 y 2

### Descripción del proyecto

Este proyecto desarrolla un problema de clasificación binaria de tumores mamarios mediante algoritmos de Machine Learning supervisado.

Se utilizan 569 observaciones, 10 variables predictoras y una variable objetivo denominada `Diagnosis`:

- 0: Tumor benigno.
- 1: Tumor maligno.

El objetivo es entrenar, optimizar y comparar diferentes modelos predictivos utilizando métricas apropiadas para clasificación binaria.

## Algoritmos implementados

1. Regresión logística regularizada L2 (Ridge).
2. Random Forest.
3. XGBoost.
4. Red neuronal simple (MLPClassifier).

## Metodología

- Análisis exploratorio de datos.
- Revisión de calidad de datos.
- División estratificada: 80 % entrenamiento y 20 % validación.
- Entrenamiento de cuatro algoritmos.
- Optimización mediante GridSearchCV.
- Validación cruzada estratificada de cinco particiones.
- Comparación de Accuracy, Precision, Recall, F1-Score, AUC-ROC y KS.
- Análisis de matrices de confusión y curvas ROC.

## Resultados principales

| Modelo | F1 validación | AUC-ROC |
|---|---:|---:|
| Regresión logística L2 | 0.8750 | 0.9712 |
| Random Forest | 0.8718 | 0.9567 |
| XGBoost | 0.8571 | 0.9683 |
| Red neuronal MLP | 0.8675 | 0.9669 |

### Modelo seleccionado

Se seleccionó la regresión logística regularizada L2, con C = 10, debido a su desempeño en validación cruzada, F1-Score, AUC-ROC e interpretabilidad.

La red neuronal MLP obtuvo el mayor Recall en la muestra de validación.

## Tecnologías utilizadas

- Python 3.12.10
- Visual Studio Code
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

## Instrucciones de ejecución

1. Descargar o clonar el repositorio.
2. Abrir la carpeta en Visual Studio Code.
3. Crear un entorno virtual de Python 3.12.
4. Instalar las dependencias:

```powershell
python -m pip install ipykernel numpy pandas matplotlib seaborn scikit-learn xgboost
```

5. Abrir `Trabajo_IA_U1_U2.ipynb`.
6. Seleccionar el kernel del entorno virtual.
7. Ejecutar todas las celdas en orden.

El archivo `datos.csv` debe encontrarse en la misma carpeta que el notebook.

## Archivos del proyecto

- `Trabajo_IA_U1_U2.ipynb`: desarrollo y resultados.
- `datos.csv`: conjunto de datos.
- `README.md`: documentación.
- `.gitignore`: exclusión de archivos temporales.

## Limitaciones

El análisis identificó 38 registros con valores negativos en características geométricas. Estos valores se conservaron y documentaron.

Los resultados corresponden a un ejercicio académico y no constituyen una herramienta validada para diagnóstico clínico.

## Asignatura

Métodos de Inteligencia Artificial — Universidad Mayor.

Trabajo correspondiente a las unidades 1 y 2.
