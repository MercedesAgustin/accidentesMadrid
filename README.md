# 🚦 Predicción de Severidad de Accidentes de Tráfico en Madrid

## 📋 Descripción del Proyecto

Este proyecto de **Data Science** aborda un problema de **clasificación supervisada** para predecir la severidad (lesividad) de accidentes de tráfico ocurridos en Madrid.  
La severidad se agrupa en dos categorías:  

- 🔴 **GRAVE:** Accidentes que requieren asistencia sanitaria.  
- 🟢 **LEVE:** Accidentes que no requieren asistencia sanitaria.  

El objetivo es desarrollar un modelo predictivo que, a partir de variables como las condiciones meteorológicas, la hora del accidente y el consumo de alcohol y drogas, permita clasificar correctamente la severidad del accidente.

**Fuente de datos**:  
[Portal de Datos Abiertos del Ayuntamiento de Madrid](https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default&vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&utm_source=chatgpt.com)

---

## 📂 Estructura del Proyecto

El proyecto está organizado en las siguientes secciones principales:

### 1️⃣ Metadata y Preparación de Datos  
- Carga y descripción del dataset original.  
- Limpieza y tratamiento de datos faltantes o erróneos.  
- Ingeniería de atributos: transformación de la variable objetivo en dos clases (GRAVE / LEVE), codificación de variables categóricas y normalización si es necesario.

### 2️⃣ Análisis Exploratorio de Datos (EDA)  
- Análisis estadístico descriptivo.  
- Visualización de la distribución de variables y relaciones entre ellas.  
- Identificación de patrones y posibles insights preliminares.

### 3️⃣ Entrenamiento y Evaluación Inicial  
- División del dataset en entrenamiento (70%) y testeo (30%).  
- Entrenamiento y evaluación de tres modelos supervisados:  
  - 🌳 Árbol de Decisión  
  - 🌲 Random Forest  
  - ⚡ XGBoost  
- Evaluación con métricas como accuracy, matriz de confusión, precisión, recall y F1-score.

### 4️⃣ Selección del Mejor Modelo  
- Comparación de resultados entre modelos.  
- Selección de **Random Forest** por su desempeño equilibrado y estabilidad.

### 5️⃣ Validación Cruzada y Métricas Finales  
- Aplicación de validación cruzada (K-Fold y LOOCV) sobre Random Forest para evaluar robustez y evitar overfitting.  
- Cálculo de métricas promedio y curva ROC AUC para medir capacidad discriminativa.

### 6️⃣ Optimización de Hiperparámetros  
- Uso de Grid Search y Randomized Search para encontrar la mejor combinación de hiperparámetros en Random Forest y XGBoost.  
- Mejora en el desempeño gracias a la optimización.

### 7️⃣ Modelo de Ensamble con Boosting  
- Implementación y evaluación del modelo XGBoost como método de ensamble.  
- Comparativa con Random Forest para valorar su efectividad en la clasificación.

---

## 📊 Resultados

- La precisión final alcanzada con el mejor modelo (Random Forest optimizado) supera el **63%**.  
- La validación cruzada confirma la estabilidad del modelo y su capacidad para generalizar.  
- El modelo de ensamble (**XGBoost**) mostró una mejora interesante tras la optimización de hiperparámetros.

---

M. Mercedes Agustin
