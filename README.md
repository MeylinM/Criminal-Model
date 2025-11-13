# Criminal-Model

**Resumen:**
- **Proyecto:** Pipeline de análisis y modelado para clasificación multiclase sobre datos de victimización personal.
- **Objetivo:** Explorar, preprocesar y entrenar modelos (árbol de decisión, random forest, regresión logística y redes neuronales) para predecir el tipo de delito (`newoff`).

**Estructura del proyecto:**
- **`data/`**: archivos CSV usados por los notebooks (ej.: `x_train.csv`, `y_train.csv`, `personal_victimization_mapped.csv`).
- **`src/`**: notebooks y carpetas con modelos y análisis.
	- `src/EDA/` — notebooks de análisis exploratorio y preprocesamiento (`analisis_exploratorio.ipynb`, `preprocesamiento.ipynb`).
	- `src/Mejor_modelo/` — comparativa de modelos (`comparativa_modelos.ipynb`).
	- `src/Modelos/Arbol_Decision/` — notebook `Arbol_Decision.ipynb`.
	- `src/Modelos/Random_Forest/` — notebook `random_forest.ipynb`.
	- `src/Modelos/Redes_Neuronales/` — notebook `Red_neuronal.ipynb` y métricas relacionadas.
	- `src/Modelos/Regresion_Logistica/` — notebook `regresion_logistica.ipynb`.

**Archivos de datos incluidos:**
- `data/personal_victimization_mapped.csv` — versión mapeada del dataset original.
- `data/Personal_Victimization_Original.csv` — dataset bruto original.
- `data/x_train.csv`, `data/x_test.csv`, `data/y_train.csv`, `data/y_test.csv` — splits preparados por el preprocesamiento.

**Dependencias (archivo):**
- `requirements.txt` contiene las dependencias detectadas en los notebooks. Contenido principal:
	- `numpy`
	- `pandas`
	- `matplotlib`
	- `seaborn`
	- `scikit-learn`
	- `tensorflow`
	- `imbalanced-learn`
	- `IPython`
	- `jupyter`
    
**Cómo usar los notebooks**
- Los notebooks principales y su propósito:
	- `src/EDA/analisis_exploratorio.ipynb`: análisis exploratorio del dataset bruto.
	- `src/EDA/preprocesamiento.ipynb`: limpieza, transformación y creación de `x_train/x_test/y_train/y_test` y escalado.
	- `src/Modelos/Arbol_Decision/Arbol_Decision.ipynb`: entrenamiento y evaluación de Decision Tree.
	- `src/Modelos/Random_Forest/random_forest.ipynb`: entrenamiento y evaluación de Random Forest.
	- `src/Modelos/Regresion_Logistica/regresion_logistica.ipynb`: regresión logística multiclase (grid search y análisis).
	- `src/Modelos/Redes_Neuronales/Red_neuronal.ipynb`: red neuronal con TensorFlow / Keras y uso de SMOTE para balanceo.

**Notas sobre ejecución**
- Asegúrate de que las rutas relativas a `data/` en los notebooks sean correctas desde la raíz del repo (los notebooks usan rutas como `../../../data/x_train.csv` dependiendo de su carpeta). Si obtienes errores de `FileNotFoundError`, ajusta la ruta o ejecuta el notebook desde la raíz del proyecto.
- Si faltan paquetes, instala solo los necesarios usando `pip install <paquete>` y vuelve a ejecutar la celda.