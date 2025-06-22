# Análisis AluraStore

## Descripción

Este proyecto analiza datos de ventas de la cadena **AluraStoreLatam** utilizando Python en un entorno Jupyter Notebook (Google Colab).
El objetivo es extraer insights comerciales sobre el desempeño de diferentes tiendas, categorías de productos y el comportamiento de los clientes.

---

## Estructura del Dataset

El conjunto de datos contiene **2,358 registros** distribuidos en **4 tiendas**.
Cada tienda tiene su propio archivo CSV. Las columnas principales son:

* **Producto:** Nombre del artículo (51 productos únicos)
* **Categoría del Producto:** 8 categorías diferentes
* **Precio:** Rango entre \$7,600 y \$2,902,200 COP
* **Costo de Envío:** Hasta \$154,700 COP
* **Calificación:** Puntuación de 1 a 5 estrellas
* **Método de Pago**
* **Cantidad de Cuotas**
* **Fecha de Compra**
* **Latitud / Longitud:** Ubicación geográfica del cliente

---

## Librerías Utilizadas

```python
import pandas as pd              # Manipulación de datos
import matplotlib.pyplot as plt  # Visualizaciones
import numpy as np               # Cálculos numéricos
```

---

## Principales Hallazgos

### 📊 Facturación por Tienda

La **Tienda 1** lidera en ventas totales con **\$1,150.9 millones USD**, seguida por:

* Tienda 2: \$1,116.3 millones USD
* Tienda 3: \$1,098.0 millones USD
* Tienda 4: \$1,038.4 millones USD

![Ingresos Totales por Tienda](Ingresos%20totales%20por%20tienda.png)

---

### ⭐️ Calificación Promedio por Tienda

Las calificaciones promedio son las siguientes:

* Tienda 3: 4.05
* Tienda 2: 4.04
* Tienda 4: 4.00
* Tienda 1: 3.98

![Calificación Promedio por Tienda](Calificacion%20promedio%20por%20tienda.png)

---

### 🛒 Productos Estrella - Tienda 1

Los **Top 5 productos más vendidos** en la Tienda 1 son:

* Microondas
* TV LED UHD 4K
* Armario
* Secadora de ropa
* Mesa de noche

![Top 5 productos más vendidos](5%20prod%20mas%20vendidos%20en%20las%20tiendas.png)

---

## Cómo Ejecutar el Análisis

### Instalación de dependencias

```bash
pip install pandas matplotlib numpy jupyter
```

### Ejecución del notebook

```bash
jupyter notebook "Alura Store.ipynb"
```

Si estás usando Google Colab, simplemente subí el archivo o vinculá el repositorio.

---

## Recomendaciones Comerciales

* 📦 Aumentar inventario en la categoría **Muebles**, ya que es la más demandada.
* 🌟 Promocionar los productos mejor calificados y con mayor rotación.
* 🚚 Analizar las ubicaciones geográficas para optimizar la logística de envío.

---

## Futuras Mejoras

* Visualización de mapas con las ubicaciones de las ventas utilizando **folium**.
* Análisis temporal de ventas por estacionalidad.

---

## Autor

Desarrollado por **Eros Alexandro Diaz**

📬 Contacto: [erosdc2018@gmail.com](mailto:erosdc2018@gmail.com)

🔗 Proyecto realizado como parte del **Challenge de Data Science de Alura Latam.**
