# Proyecto Final – Aprendizaje Máquina  
### Predicción de Arrestos en Crímenes Reportados en la Ciudad de Chicago (2024)

---

## 👩‍💻 Autores

- **María Belén Cattaneo**  
- **Nicolás Valentín Ciarrapico**  
- **Sabrina Daiana Pryszczuk**

---
## 🧭 Descripción General

Este proyecto constituye el trabajo final de la asignatura **Aprendizaje Máquina**, y tiene como propósito aplicar de forma integral los conceptos y metodologías abordados durante el curso.  
El objetivo principal es desarrollar un **modelo de clasificación supervisado** capaz de predecir si un crimen reportado en la ciudad de **Chicago durante el año 2024** culminó o no en un **arresto**, utilizando técnicas modernas de análisis y aprendizaje automático.

El proyecto sigue el **ciclo completo de un proyecto de ciencia de datos**, abarcando desde la selección y comprensión del dataset, el preprocesamiento y análisis exploratorio, hasta la construcción, evaluación y comparación de modelos predictivos.

---

## 🎯 Objetivo del Problema

A partir de los registros públicos de delitos proporcionados por el **City of Chicago Data Portal**, se busca **modelar la probabilidad de que un crimen derive en un arresto**.  
El conjunto de datos contiene información sobre:
- Tipo y clasificación del crimen (IUCR, Primary Type, FBI Code).  
- Ubicación geográfica (coordenadas, distrito, comunidad).  
- Contexto temporal (fecha, hora, estación del año).  
- Distancia al destacamento policial más cercano.

El problema se formaliza como una **tarea de clasificación binaria**, donde la variable objetivo es `Arrest_tag`:
- `1` → el crimen resultó en arresto.  
- `0` → el crimen no resultó en arresto.

---

## 🧮 Enfoque Metodológico

El trabajo aplica técnicas de **preprocesamiento, selección y extracción de características, balanceo de clases y modelización supervisada**.  
Los modelos fueron entrenados y evaluados bajo criterios estadísticos y métricas de rendimiento apropiadas para problemas de clasificación con clases desbalanceadas (precisión, recall, F1-score y AUC-ROC).

---

## 📂 Estructura del Repositorio

El repositorio se organiza en tres directorios principales, reflejando las etapas del proyecto:

### [`preprocesamiento/`](./preprocesamiento)
Contiene los notebooks que desarrollan todo el proceso de preparación y análisis de datos:
1. **Creación del dataset:** integración de fuentes, limpieza y estructura base.  
2. **EDA:** exploración descriptiva y detección de patrones y anomalías.  
3. **Tratamiento de outliers y codificación:** aplicación de transformaciones logarítmicas y codificación de variables categóricas.  
4. **Escalado:** comparación de diferentes métodos y selección de *StandardScaler*.  
5. **Balanceo:** combinación de *SMOTE* (oversampling) y undersampling aleatorio.  
6. **Selección y extracción de características:** análisis de correlaciones, ANOVA, información mutua y PCA.

### [`modelos/`](./modelos)
Incluye los notebooks correspondientes a la fase de modelización, donde se implementan y evalúan distintos **modelos de aprendizaje supervisado**, tales como:

**COMPLETAR**

### [`datasets/`](./datasets)
Directorio que contiene los datasets utilizados en las distintas etapas.

---

## 📈 Resultados Esperados

- Conjunto de datos completamente procesado, escalado y balanceado.  
- Reducción de dimensionalidad mediante PCA manteniendo más del **90% de la varianza total**.  
- Identificación de las variables más influyentes en la probabilidad de arresto.  
- Evaluación comparativa de modelos para determinar el enfoque predictivo más eficaz.

---

## 🧩 Requisitos del Proyecto

Este trabajo responde a la consigna académica del **Proyecto Final de la asignatura Aprendizaje Máquina**, cuyo objetivo es demostrar la capacidad de:
- Aplicar el flujo completo de un proyecto de *Machine Learning*.  
- Analizar, preparar y modelar datos reales de manera justificada.  
- Comunicar los resultados de forma clara, fundamentada y profesional.

---

## 📘 Referencias

- **City of Chicago – Data Portal:** [Crimes - 2024](https://data.cityofchicago.org/Public-Safety/Crimes-2024/dqcy-ctma)  
- **City of Chicago – Police Stations:** [Police Stations Dataset](https://data.cityofchicago.org/Public-Safety/Police-Stations/z8bn-74gv)

---

## 🧾 Como instalar el proyecto

El presente proyecto se ejecuta mediante Jupyter notebooks:

Para ejecutar los distintos notebooks ubicados en  `notebooks/`, siga los siguientes pasos:

1. **Asegurese de tener instalado Python 3.11 o superior**:

   ```bash
   python3 --version
   ```

2. **Clone el repositorio**:

   ```bash
   git clone https://github.com/CEIA-AndD-Grupo4/TP_Final.git

   ```

3. **Instale `uv` si aun no lo tiene instalado**:

   ```bash
   curl -Ls https://astral.sh/uv/install.sh | bash
   ```

4. **Instale las dependencias y cree el entorno virtual**:

   ```bash
   uv venv
   uv sync
   ```

5. **Active el entorno virtual**:

   - En Linux/macOS:
     ```bash
     source .venv/bin/activate
     ```
   - En Windows:
     ```powershell
     .\.venv\Scripts\activate
     ```

6. **Inicie Jupyter Notebook**:

   ```bash
   uv run jupyter notebook
   ```

7. **Abra el archivo** que desee ejecutar desde el directorio [`preprocesamiento`](./preprocesamiento) o [`modelos`](./modelos).

8. **Ejecute todas las celdas en orden** para correr el algoritmo.

---
