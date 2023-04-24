# Tetillas_mosca
Proyecto para facilitar la cuantificación de la densidad de las tetillas presentes en el lente del omatidio de Drosophila melanogaster (mosca de la fruta).
Desarrollado por alumnos de maestría del laboratio de Genética de Transducción de Señales en el INB, UNAM.

ENGLISH: Project to facilitate density quantification of nipple arrays of the Drosophila (fruit fly) lens of the ommatidium.
Developed by master's degree students from the Laboratory of Genetics and Signal Transduction at INB, UNAM.

Los datos de entrada deben de organizarse en dos columnas tituladas "x1" y "y1", cada fila corresponde a las coordenadas del centroide de una tetilla en una imagen obtenida por SEM, captura realizada previamente a mano. En la carpeta de tablas se ofrece el archivo "Pezones_control_coordenadas.csv" como dataset de prueba.

El código principal tetillas_mosca está desarrollado en python y utiliza las bibliotecas numpy y pandas. Comienza con la lectura del dataset, después se incluye la función "tetillas" que recibirá como entradas el dataset y un radio (r) en µm, esta función calculará desde cada punto cuántos puntos están a su alrededor y a qué distancia, discriminando los que se encuentren fuera del radio dado. También se dejarán fuera los puntos cuya región marcada por la r dada rebace los límites de la imagen. 

La función exporta 3 tablas para su posterior análisis. 
	"Conteo.csv" Indica cuántos puntos hay alrededor de cada punto(tetilla) en la imagen. Se incluye un identificador numérico para cada tetilla considerada. 
	"Coordenadas_de_los_puntos.csv" A cada punto (tetilla) se le asigna un identificador numérico y cuáles son sus coordenadas en la imagen. 
	"Distancias.csv" Este punto indica cuáles son los puntos entre los que se midió la distancia y su magnitud en µm. 

Autores: 
Manuel Alejandro Zúniga García,
Daniel Tapia Merino
