# Clasificador_de_archivos_AI
# Clasificador Automático de Archivos por Contenido

Este proyecto implementa un sistema de clasificación semántica de archivos usando
modelos de lenguaje y clustering no supervisado. Analiza el contenido de los documentos
y los organiza automáticamente en carpetas temáticas.

## 1. Descripción General

El sistema lee archivos de distintos formatos (.pdf, .docx, .csv, .txt, .ipynb, .xlsx,
.html, .pptx, etc.), extrae el contenido textual, genera embeddings, agrupa por
similitud y luego usa GPT-4 para sugerir nombres y revisar clasificaciones.

## 2. Tecnologías Utilizadas

- SentenceTransformer ("all-MiniLM-L6-v2") para embeddings
- KMeans (scikit-learn) para clustering
- GPT-4 (API de OpenAI) para evaluación cualitativa
- pytesseract para imágenes
- openpyxl para Excel
- Python script funcional (sin GUI)

## 3. Flujo de Procesamiento

1. Leer archivos y extraer texto.
2. Vectorizar contenido con embeddings.
3. Agrupar por similitud con KMeans.
4. Evaluar con GPT-4: temas, nombres, errores.
5. Crear carpetas con nombres sugeridos.
6. Mover archivos clasificados.
7. Analizar archivos dudosos y reubicar si es necesario.

## 4. Precisión y Validación

No se usa accuracy clásico. Validación por:

- Distancia al centroide (los más alejados son "dudosos").
- Juicio GPT-4 en los casos dudosos para decidir reubicación.

## 5. Requisitos

- Python 3.8+
- Librerías: scikit-learn, sentence-transformers, openai,
  pytesseract, openpyxl, beautifulsoup4, python-pptx,
  matplotlib, Pillow, fitz (PyMuPDF)
- Clave API de OpenAI

## 6. Ejecución

```bash
python clasificador.py
Los resultados se organizan automáticamente en subcarpetas creadas con base en la temática detectada por GPT-4.


---

### ✅ Corrige tu bloque de texto del diagrama de flujo (parece que no cerraste bien el bloque en ` ```text `):

```md
## 7. Diagrama de Flujo

```text
┌────────────────────────────┐
│      Leer archivos         │
└────────────┬───────────────┘
             ↓
┌────────────────────────────┐
│     Extraer contenido      │
└────────────┬───────────────┘
             ↓
┌────────────────────────────┐
│    Generar embeddings      │
└────────────┬───────────────┘
             ↓
┌────────────────────────────┐
│   Clustering con KMeans    │
└────────────┬───────────────┘
             ↓
┌────────────────────────────────────────┐
│ Evaluación GPT (temas y errores)       │
└────────────┬───────────────────────────┘
             ↓
┌────────────────────────────────────────┐
│ Crear carpetas con nombres temáticos   │
└────────────┬───────────────────────────┘
             ↓
┌────────────────────────────┐
│      Mover archivos        │
└────────────┬───────────────┘
             ↓
┌────────────────────────────┐
│ Analizar casos dudosos     │
└────────────┬───────────────┘
             ↓
┌────────────────────────────┐
│ Reubicar si es necesario   │
└────────────────────────────┘

## 8. Autora

**Claudia Ximena Paz Cendejas**  
Proyecto desarrollado como parte de un sistema de organización inteligente de archivos impulsado por IA.

