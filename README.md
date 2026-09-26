
# Pipeline de Procesamiento de Lenguaje Natural (NLP) y Modelos de Lenguaje (LLMs)

Este repositorio contiene la implementación práctica y teórica de un pipeline completo de procesamiento de texto, que abarca desde las técnicas clásicas de limpieza lingüística hasta la integración y optimización de modelos de lenguaje modernos (Transformers y LLMs).

Este desarrollo forma parte del laboratorio académico para el curso de Procesamiento de Texto.

**Docente:** Paul Alexander Diaz Montaña  
**Integrantes:**
Jhon Eduardo Tinjaca Cruz - jetinjaca@ucundinamarca.edu.co
Julián Davied Silva Guzman - jdsilva@ucundinamarca.edu.co  
**Fecha:** 26 de Septiembre de 2026  

---

## 🚀 Características del Pipeline

El proyecto se divide en 19 etapas lógicas, implementando de forma robusta e independiente cada uno de los siguientes procesos:

1. **Instalación y Configuración:** Configuración de un entorno híbrido con soporte para CPU y GPU utilizando `PyTorch`, `SpaCy`, `NLTK`, `Transformers` y `Sentence-Transformers`.
2. **Dataset de Deportes & Otros:** Generación controlada de un corpus sintético de 500 documentos para simular escenarios de producción.
3. **Normalización de Texto:** Estandarización de textos eliminando URLs, caracteres especiales y espacios innecesarios.
4. **Stemming (Truncamiento):** Reducción de tokens a sus raíces morfológicas básicas mediante el algoritmo *Snowball*.
5. **Stopwords:** Limpieza profunda de ruido mediante la remoción de palabras vacías personalizables en español.
6. **Term Frequency (TF):** Construcción de matrices de frecuencia absoluta y relativa para análisis estadístico básico.
7. **IDF y TF-IDF:** Ponderación estadística de la relevancia de los términos discriminando palabras comunes.
8. **Part-of-Speech Tagging (POS):** Etiquetado e identificación gramatical del texto con redes neuronales convolucionales de SpaCy.
9. **Lematización:** Obtención de formas canónicas reales con apoyo del análisis morfosintáctico.
10. **Parsing (Análisis de Dependencias):** Generación de representaciones gráficas interactivas y jerárquicas del lenguaje.
11. **Named-Entity Recognition (NER):** Extracción de entidades clave (Personas, Lugares, Organizaciones).
12. **Generación con LLM:** Generación de textos condicionales estructurados mediante `google/flan-t5-small`.
13. **Question Answering (Sistemas QA):** Búsqueda y extracción precisa de respuestas utilizando BERT en español.
14. **Summarization (Resumen):** Condensación semántica abstractiva empleando el modelo multilingüe `mT5`.
15. **Sentence Similarity:** Medición de afinidad y distancia coseno usando incrustaciones vectoriales densas (*embeddings*).
16. **Text Classification:** Clasificador entrenado con Regresión Logística y optimizado con validación cruzada estratificada.
17. **Translation (Traducción):** Traducción local bidireccional (Español a Inglés) mediante modelos neuronales de la iniciativa `Helsinki-NLP`.
18. **Text Generation (Modelado Causal):** Generación creativa autorregresiva usando `gpt2-small-spanish`.
19. **Text Mining (Minería de Datos):** Visualizaciones analíticas avanzadas utilizando Gráficos de Distribución de Frecuencia y Nubes de Palabras (*WordClouds*).

---

## 🛠️ Tecnologías y Librerías Utilizadas

- **Lenguaje:** Python 3.10+
- **Librerías Clave:**
  - [SpaCy](https://spacy.io/) (Modelo `es_core_news_sm`)
  - [NLTK](https://www.nltk.org/)
  - [Scikit-Learn](https://scikit-learn.org/)
  - [Hugging Face Transformers & Tokenizers](https://huggingface.co/)
  - [Sentence-Transformers](https://www.sbert.net/)
  - [WordCloud](https://github.com/amueller/word_cloud)
  - [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/)

---

## 📦 Requisitos de Instalación

Para ejecutar el proyecto de forma local, clona este repositorio e instala el archivo de requerimientos:

```bash
pip install nltk spacy scikit-learn pandas matplotlib seaborn wordcloud transformers sentence-transformers torch sentencepiece accelerate sacremoses
python -m spacy download es_core_news_sm
```

---

## 📈 Resultados Obtenidos
- **Clasificador Supervisado:** Se alcanzó una precisión promedio de **0.75** en validación cruzada y del **100%** de precisión sobre particiones balanceadas de prueba gracias al uso de representaciones vectoriales enriquecidas semánticamente.
- **Robustez del Pipeline:** El código contiene bloques de seguridad (*defensive programming*) que evitan errores comunes de ejecución fuera de orden de las celdas en entornos interactivos de Jupyter/Google Colab.
