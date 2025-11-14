# Red de coocurrencia de términos
Este repositorio contiene un script en Python para realizar análisis de contenido en un conjunto de documentos textuales. El algoritmo extrae los términos más relevantes, construye una red de coocurrencia para visualizar las relaciones entre ellos, identifica grupos temáticos y destaca los conceptos más centrales.

## 🎯 Objetivo del proyecto

El objetivo principal es transformar un corpus de texto no estructurado en una red visual y analítica. Este enfoque permite identificar los temas principales tratados en los documentos y comprender cómo se relacionan entre sí, lo que ofrece información valiosa para la investigación cualitativa y el análisis de contenido.

## ✨ Características

* **Preprocesamiento de texto:** Normalización, eliminación de *stopwords*, puntuación y números para limpiar los datos.

* **Construcción de redes:** Generación de una matriz de coocurrencia que cuantifica la frecuencia con la que los términos aparecen juntos en los mismos documentos.

* **Detección de comunidades:** aplicación del algoritmo de Louvain para agrupar términos en clústeres temáticos.

* **Análisis de centralidad:** uso del algoritmo PageRank para medir la importancia de cada término (nodo) en la red.

* **Visualización gráfica:** creación de un gráfico de red en el que:
    * Los nodos representan los términos.
    * Los bordes indican la coocurrencia entre términos.
    * Los colores diferencian los grupos temáticos.
    * El tamaño de los nodos es proporcional a su centralidad (PageRank).

## 📂 Estructura del repositorio

```
/
│
├── ClusterTemáticos.ipynb    # Script principal con toda la lógica de análisis y visualización.
├── extractos.txt             # Archivo de entrada que contiene los textos que se van a analizar.
├── requirements.txt          # Lista de dependencias de Python para el proyecto.
└── README.md                 # Este archivo de documentación.
```

## 🛠️ Requisitos

El script se ha desarrollado en Python 3 y utiliza las siguientes bibliotecas:

* `pandas`
* `networkx`
* `python-louvain`
* `matplotlib`

Todas las dependencias necesarias se enumeran en el archivo `requirements.txt`.

## 🚀 Cómo utilizarlo

Siga los pasos que se indican a continuación para ejecutar el análisis con sus propios datos.

**1. Clone el repositorio:**
```bash
git clone [https://github.com/your-username/analise-rede-coocorrencia-texto.git](https://github.com/your-username/analise-rede-coocorrencia-texto.git)
cd analise-rede-coocorrencia-texto
```

**2. (Opcional) Cree un entorno virtual:**
Es una buena práctica aislar las dependencias del proyecto.
```bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

**3. Instale las dependencias:**
```bash
pip install -r requirements.txt
```

**4. Prepare su archivo de entrada:**
* Edite el archivo `extractos.txt` o sustitúyalo por otro.
* El contenido debe ser texto sin formato, y cada documento (o extracto) debe estar separado por `###`.

    **Ejemplo de `extractos.txt`:**
    ```
    Este es el primer documento. Trata sobre política y educación.
    ###
    Este es el segundo documento. Trata sobre la relación entre la investigación, la política y la sociedad.
    ###
    El tercer documento se centra en la investigación y las metodologías educativas.
    ```

**5. Ejecute el script:**
Abra el terminal en la carpeta del proyecto y ejecute el siguiente comando:
```bash
python analise_rede.py
```

## 📊 Salida

Después de la ejecución, el script guardará una imagen de la red generada en el directorio principal con el nombre `analisis_red_final.png`.



## 📄 Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulte el archivo `LICENSE` para obtener más detalles.