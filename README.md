# Análisis Exploratorio del Titanic

## Descripción

Este proyecto realiza un análisis exploratorio de datos de los pasajeros del Titanic utilizando Python.

El objetivo es identificar características relacionadas con la supervivencia de los pasajeros mediante técnicas de limpieza, transformación, análisis estadístico y visualización de datos.

## Dataset

**Nombre:** Titanic

**Fuente:** Kaggle

**Archivo utilizado:** train.csv

El dataset contiene información de los pasajeros del Titanic, incluyendo su clase, sexo, edad, tarifa, familiares a bordo y si sobrevivieron al desastre.

## Objetivo

Analizar la información de los pasajeros del Titanic para identificar características asociadas con la supervivencia.

No se utiliza ningún modelo de Machine Learning.

## Tecnologías utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Git
- GitHub

## Estructura del proyecto

```text
rendimiento-academico/
│
├── data/
│   └── train.csv
│
├── src/
│   └── analysis.py
│
├── outputs/
│   └── resultados/
│       ├── supervivencia_genero.png
│       ├── supervivencia_clase.png
│       ├── supervivencia_edad.png
│       └── resultados_procesados.csv
│
├── README.md
├── requirements.txt
└── .gitignore


Requisitos

Para ejecutar el proyecto se necesita:

Python 3
Git
Las dependencias incluidas en requirements.txt
Instalación

Clonar el repositorio:

git clone URL_DEL_REPOSITORIO

Entrar al proyecto:

cd rendimiento-academico

Crear un entorno virtual:

python3 -m venv .venv

Activar el entorno virtual en Ubuntu:

source .venv/bin/activate

Instalar las dependencias:

pip install -r requirements.txt
Ejecución

Para ejecutar el análisis:

python src/analysis.py

Los resultados y visualizaciones se almacenarán en:

outputs/resultados/
Limpieza y preprocesamiento

Se revisaron los valores faltantes, registros duplicados y tipos de datos.

Para la variable Age, los valores faltantes fueron reemplazados utilizando la mediana según la clase del pasajero y su sexo.

Para Embarked, los valores faltantes fueron reemplazados utilizando la categoría más frecuente.

Para Cabin, los valores faltantes fueron reemplazados por Unknown, debido a que una cantidad considerable de registros no contiene información de cabina.

También se eliminaron registros duplicados.

Variables nuevas
FamilySize

Se creó utilizando:

FamilySize = SibSp + Parch + 1

Esta variable representa el tamaño de la familia con la que viajaba el pasajero.

IsAlone

Indica si el pasajero viajaba solo.

1 = viajaba solo
0 = viajaba acompañado
AgeGroup

Se creó una clasificación de edades:

Edad	Categoría
Menor de 13	Niño
13 a 19	Joven
20 a 59	Adulto
60 o más	Adulto mayor
Análisis realizados
1. Porcentaje de supervivencia

Se calculó el porcentaje general de pasajeros que sobrevivieron y no sobrevivieron.

2. Supervivencia según sexo

Se comparó el porcentaje de supervivencia entre hombres y mujeres.

3. Supervivencia según clase

Se analizó la supervivencia de los pasajeros pertenecientes a primera, segunda y tercera clase.

4. Supervivencia según grupo de edad

Se compararon los porcentajes de supervivencia entre niños, jóvenes, adultos y adultos mayores.

5. Viajar solo o acompañado

Se analizó si viajar solo o acompañado presenta diferencias en la supervivencia.

6. Tarifa y supervivencia

Se comparó la tarifa promedio pagada por pasajeros sobrevivientes y no sobrevivientes.

Visualizaciones

El proyecto genera tres visualizaciones principales:

Supervivencia según sexo.
Supervivencia según clase.
Supervivencia según grupo de edad.

Las gráficas se encuentran en:

outputs/resultados/
Conclusiones

El análisis permite identificar diferencias importantes en la supervivencia de los pasajeros según características como sexo, clase y grupo de edad.

También se analiza la posible relación entre viajar solo o acompañado y la supervivencia.

La variable FamilySize permite estudiar el tamaño del grupo familiar de los pasajeros, mientras que AgeGroup facilita la comparación entre diferentes rangos de edad.

Las visualizaciones permiten interpretar de manera sencilla los patrones encontrados en los datos.

Reproducibilidad

Este proyecto está preparado para ser reproducido en otra computadora.

Para reproducirlo únicamente es necesario clonar el repositorio, crear un entorno virtual nuevo, instalar las dependencias mediante requirements.txt y ejecutar el archivo analysis.py.

No es necesario recibir archivos adicionales fuera del repositorio.