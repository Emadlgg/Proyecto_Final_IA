# 🎵 Sistema de Recomendación Musical
### Redes Bayesianas + Machine Learning | CC3085 – Inteligencia Artificial | UVG 2026

Sistema de recomendación musical personalizado que combina modelos de clasificación supervisada (KNN, Decision Tree, SVM) con inferencia probabilística mediante Redes Bayesianas Discretas. Dado un perfil de preferencias del usuario —géneros favoritos y canciones de ejemplo— el sistema infiere recomendaciones basándose en las características intrínsecas del audio, no en el comportamiento de otros usuarios.

---

## 🎬 Video Explicativo

<!-- Reemplazar con el link real del video -->
[📺 Ver video en YouTube / Drive](LINK_DEL_VIDEO_AQUÍ)

---

## 📁 Estructura del Repositorio

```
├── proyecto_final_ia.ipynb   # Notebook principal con todo el código
├── dataset.csv               # Spotify Tracks Dataset (114k canciones, 114 géneros)
├── Proyecto_Final_IA.docx    # Documento del proyecto
└── README.md
```

---

## 🧠 Técnicas de IA Aplicadas

| Técnica | Uso |
|---|---|
| K-Nearest Neighbors (KNN) | Clasificación de géneros musicales |
| Árbol de Decisión | Clasificación + análisis de importancia de features |
| Support Vector Machine (SVM) | Clasificación con kernel RBF |
| Red Bayesiana Discreta | Inferencia probabilística de popularidad dado un perfil |
| Variable Elimination | Algoritmo de inferencia exacta en la BN |

---

## 📊 Dataset

**Spotify Tracks Dataset** — [Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)

- 114,000 canciones | 114 géneros | 1,000 canciones por género (balanceado)
- Features de audio: `danceability`, `energy`, `valence`, `acousticness`, `tempo`, `loudness`, `speechiness`, `instrumentalness`, `liveness`, `popularity`
- Para este proyecto se seleccionaron 10 géneros: `reggaeton`, `latin`, `pop`, `rock`, `hip-hop`, `r-n-b`, `electronic`, `jazz`, `classical`, `metal`

---

## ⚙️ Instalación

```bash
pip install pandas numpy matplotlib seaborn scikit-learn pgmpy ipywidgets
```

Luego abrir `proyecto_final_ia.ipynb` en Jupyter y ejecutar todas las celdas en orden.

---

## 🎮 Demo Interactivo

El notebook incluye una interfaz interactiva al final (Sección 7) construida con `ipywidgets`:

1. **Seleccionás géneros favoritos** (Ctrl+Click para varios)
2. **Elegís canciones de ejemplo** que te gustan (máximo 5)
3. **El sistema detecta tu perfil** musical y aplica inferencia bayesiana
4. **Recibís recomendaciones** rankeadas con tabla y gráficos comparativos

---

## 📈 Resultados

| Modelo | Tarea | Accuracy |
|---|---|---|
| KNN (K=1) | Clasificación de género | 51.0% |
| Decision Tree (depth=16) | Clasificación de género | 50.5% |
| SVM (RBF) | Clasificación de género | 50.2% |
| Red Bayesiana | Predicción de popularidad | 31.2% |

> Los accuracies de clasificación de género son razonables considerando que varios géneros comparten espacio de features (reggaeton/latin, hip-hop/r-n-b). La Red Bayesiana resuelve una tarea distinta (3 clases de popularidad) y se complementa con los clasificadores en el sistema final.

---

## 👥 Integrantes

| Nombre | Carné |
|---|---|
| | |
| | |

---

## 📚 Bibliografía

- Russell, S. J., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
- Rogers, S., & Girolami, M. (2016). *A First Course in Machine Learning* (2nd ed.). CRC Press.
- Ankan, A., & Panda, A. (2015). *pgmpy: Probabilistic Graphical Models using Python*.
- Spotify Tracks Dataset. Kaggle. https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset
