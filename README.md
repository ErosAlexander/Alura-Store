# Análisis AluraStore

## Descripción

Este proyecto analiza datos de ventas de la cadena **AluraStoreLatam** utilizando Python en un entorno Jupyter Notebook (Google Colab). El objetivo es extraer insights comerciales sobre el desempeño de diferentes tiendas, categorías de productos y el comportamiento de los clientes.

---

## Estructura del Dataset

El conjunto de datos contiene **2,358 registros** distribuidos en **4 tiendas**. Cada tienda tiene su propio archivo CSV. Las columnas principales son:

- **Producto**: Nombre del artículo (51 productos únicos)
- **Categoría del Producto**: 8 categorías diferentes
- **Precio**: Rango entre $7,600 y $2,902,200 COP
- **Costo de Envío**: Hasta $154,700 COP
- **Calificación**: Puntuación de 1 a 5 estrellas
- **Método de Pago**
- **Cantidad de Cuotas**
- **Fecha de Compra**
- **Latitud / Longitud**: Ubicación geográfica del cliente

---

## Librerías Utilizadas

```python
import pandas as pd           # Manipulación de datos
import matplotlib.pyplot as plt  # Visualizaciones
import numpy as np            # Cálculos numéricos

Principales Hallazgos
1️⃣ Facturación por Tienda
La Tienda 1 lidera en ventas totales con $1,150,880,400 COP, seguida por:

Tienda 2

Tienda 3

Tienda 4

2️⃣ Categorías Más Populares
df.groupby('Categoría del Producto').size().sort_values(ascending=False)
Resultado:

Muebles (465 productos)

Electrónicos (448 productos)

Juguetes (324 productos)

3️⃣ Calificaciones Promedio
Todas las tiendas mantienen calificaciones superiores a 3.9/5.

⭐️ Tienda 3: 4.05

Tienda 2: 4.04

Tienda 4: 4.00

Tienda 1: 3.98

4️⃣ Productos Estrella

df['Producto'].value_counts().head(3)
Top 3 productos más vendidos:

Lavadora de ropa

Microondas

Set de ollas

Cómo Ejecutar el Análisis
1. Instalar dependencias
bash
Copiar
Editar
pip install pandas matplotlib numpy jupyter
2. Ejecutar el notebook
bash
Copiar
Editar
jupyter notebook AluraStoreLatam.ipynb
Si estás usando Google Colab, simplemente subí el archivo o vinculá el repositorio.

Ejemplo de Visualización
Gráfico de torta mostrando la valoración promedio de cada tienda:

import matplotlib.pyplot as plt

tiendas = [tienda, tienda2, tienda3, tienda4]
promedios_calificacion = [df["Calificación"].mean() for df in tiendas]

plt.figure(figsize=(6,6))
plt.pie(promedios_calificacion, 
        labels=[f'Tienda {i+1}' for i in range(len(promedios_calificacion))],
        autopct='%1.2f%%',
        startangle=90,
        colors=plt.cm.Paired.colors)
plt.title('Promedio de calificaciones por tienda')
plt.show()
 Recomendaciones Comerciales
 Aumentar inventario en la categoría Muebles, ya que es la más demandada.


 Promocionar los productos mejor calificados y con mayor rotación.

 Analizar las ubicaciones geográficas para optimizar logística de envío.

Futuras Mejoras:
Mapas con ubicaciones de ventas (folium)

Autor
Desarrollado por Eros Alexandro Diaz
📬 Contacto: [erosdc2018@gmail.com]
🔗 Challenge de Data Science de Alura Latam.