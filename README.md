# Proyecto de Creación de Imágenes Panorámicas

Este proyecto permite crear imágenes panorámicas a partir de varias fotografías, usando métodos avanzados de procesamiento de imágenes y emparejamiento de características.

## Descripción

El proyecto se divide en dos partes:

1. **Unión de cinco imágenes**: Genera una panorámica a partir de cinco imágenes. La imagen central se mantiene sin deformar, mientras que las imágenes laterales se ajustan usando homografías para formar una única vista continua.

2. **Unión de siete imágenes con proyección cilíndrica**: Crea una panorámica extendida empleando siete imágenes y proyectándolas en un plano cilíndrico para reducir la distorsión en los bordes. Esta sección introduce una función de proyección cilíndrica, basada en cálculos de distancia focal y coordenadas 3D, antes de la unión de las imágenes.

## Funcionalidades Principales

- **SIFT Detector**: Detecta puntos de interés en las imágenes.
- **BF KNN Matcher**: Encuentra coincidencias entre pares de imágenes usando un enfoque de fuerza bruta.
- **RANSAC Homography**: Calcula la homografía entre imágenes para aplicar la transformación necesaria y unirlas.
- **WarpTwoImages**: Deforma y une dos imágenes, corrigiendo los bordes negros y aplicando transformaciones de perspectiva.
- **Cylinder Image Projection**: Proyecta imágenes en una superficie cilíndrica, útil para panorámicas amplias, con una función específica para ajustar las coordenadas.

## Requisitos

- Python 3.x
- OpenCV
- NumPy

## Referencias

- [Shapiro Linda - Image Stitching II](https://courses.cs.washington.edu/courses/cse576/17sp/notes/9_ImageStitching2-17.pdf)
- [Royshil - Función de Warping Cilíndrico](https://gist.github.com/royshil/0b21e8e7c6c1f46a16db66c384742b2b)




