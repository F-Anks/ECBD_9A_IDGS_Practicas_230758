# Práctica 09: Algoritmos de Análisis No Supervisado — Clientes de Centros Comerciales

## Descripción

Práctica de aprendizaje no supervisado utilizando el algoritmo **K-Means** para segmentar clientes de un centro comercial a partir del dataset `Mall_Customers.csv`. Se replica, traduce, analiza y documenta el notebook de Kaggle ["Unsupervised Learning: 3-6 Clusters | K-Means | EDA"](https://www.kaggle.com/code/tanmay111999/unsupervised-learning-3-6-clusters-k-means-eda).

## Estructura de Archivos

```
Practica09/
├── Mall_Customers.csv                      # Dataset de 200 clientes (5 variables)
├── Practica09.ipynb                        # Notebook principal con análisis y diagramas 3D
├── outputs/
│   └── cluster3d_mall_customers.html       # Diagrama 3D interactivo exportado en HTML (Plotly 3D)
└── README.md                               # Este archivo
```

## Dataset

- **Nombre:** Mall Customer Segmentation Data
- **Registros:** 200 clientes
- **Variables:**
  - `CustomerID`: Identificador único del cliente
  - `Gender`: Género (Male / Female)
  - `Age`: Edad del cliente (años)
  - `Annual Income (k$)`: Ingreso anual en miles de dólares
  - `Spending Score (1-100)`: Puntuación de gasto asignada por el centro comercial

## Instrucciones de Ejecución

### Requisitos

```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly
```

### Ejecutar el Notebook

1. Abrir `Practica09.ipynb` en Jupyter Notebook, JupyterLab o VS Code.
2. Ejecutar todas las celdas en orden secuencial (de la primera a la última).
3. El notebook genera todas las gráficas inline (incluyendo las proyecciones 3D con Matplotlib y el diagrama 3D interactivo con Plotly).

### Ejecución desde Terminal

```bash
jupyter nbconvert --to notebook --execute Practica09.ipynb --output Practica09.ipynb
```

## Contenido del Notebook

1. **Portada e Introducción** — Datos del estudiante y contexto teórico.
2. **Carga y Exploración** — Importación de datos, inspección inicial (`head`, `tail`, `info`, `describe`).
3. **Calidad de Datos** — Verificación de nulos, duplicados y rangos.
4. **Análisis Exploratorio (EDA)** — Distribuciones univariadas, boxplots, pairplot y correlación.
5. **Preprocesamiento** — Codificación de `Gender` con `LabelEncoder` y normalización con `MinMaxScaler`.
6. **Evaluación de K** — Método del Codo (WCSS) y Coeficiente de Silueta para 4 combinaciones de variables, con datos originales y normalizados.
7. **Modelos K-Means** — Entrenamiento, visualización 2D y reporte técnico.
8. **Diagramas 3D** — Visualización tridimensional multi-ángulo con Matplotlib y Diagrama 3D Interactivo con Plotly (`cluster3d_mall_customers.html`).
9. **Conclusiones** — Interpretaciones, perfiles de clientes, comparaciones y limitaciones.

## Autor

- **Estudiante:** Francisco Garcia Garcia
- **Matrícula:** 230758
- **Grupo:** 9°A IDGS
- **Asignatura:** Estadística Computacional y Big Data
