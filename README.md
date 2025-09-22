# test-colab-jupyter
Repositorio Test para subir notebooks a github, desde colab o jupyter vsc

## Pasos y Análisis de Ventas Panini

Este repositorio test, contiene un conjunto de scripts y análisis exploratorios de datos (EDA) para entender mejor los patrones de ventas de "Panini" a partir de un dataset transaccional.

## Descripción del Proyecto

El objetivo principal es poder cargar o subir los archivos o cambios desde vs a github, en cuanto al proyecto tareas como limpiar datos queda pendiente,la carga y visualización de datos de ventas permitieron obtener insights sobre el rendimiento de productos, métodos de pago y tendencias de ingresos a lo largo del tiempo. Se utilizan las librerías `pandas` para la manipulación de datos, y `matplotlib` junto con `seaborn` para la visualización.

## Pasos para subir cambios desde Notebook a Github

### 1. Crear un repositorio nuevo en Github,sólo agregar Readme. 

### 2. Clonar tu repositorio (solo la primera vez en Notebook Jupyter o Colab)
`git clone https://github.com/LenninTemoche/test-colab-jupyter.git`

### 3. Entrar a la carpeta del repo
`%cd test-colab-jupyter`

### 4. Configurar tus credenciales de GitHub

`!git config --global user.name "TU-NOMBRE"`

`!git config --global user.email "TU-CORREO"`

### ⚠️Agrega o reemplaza TU-TOKEN con tu Personal Access Token de GitHub
. En VS te pedirá Token al hacer push

.En Colab podrás agregarlo usando:
`!git remote set-url origin https://TU-TOKEN@url_de_repo.git`

Por ejemplo:

`!git remote set-url origin https://TU-TOKEN@github.com/LenninTemoche/test-colab-jupyter.git`

### Subir los cambios

`!git add .`

`!git commit -m "Subo cambios desde Colab"`

`!git push origin main` #luego de la 1ra vez sólo `git push`


## Contenido del Repositorio

*   `panini.csv`: El dataset de ventas crudo utilizado para el análisis.
*   `notebook.ipynb` (o similar): Archivo principal que contiene el código para el procesamiento de datos y la generación de gráficos.
    *   Carga y preparación del dataset.
    *   Generación de diversos gráficos de visualización.

## Análisis Realizados y Visualizaciones Clave

El análisis incluye las siguientes visualizaciones, cada una diseñada para ofrecer una perspectiva diferente sobre los datos de ventas:

1.  **Top 10 Productos Más Vendidos:**
    *   **Tipo de Gráfico:** Barras
    *   **Conclusión Clave:** Identifica los productos con mayor número de transacciones, revelando los "best-sellers".
    *   **Utilidad:** Ayuda a gestionar inventario y enfocar estrategias de marketing en productos populares.

2.  **Ventas por Método de Pago:**
    *   **Tipo de Gráfico:** Barras
    *   **Conclusión Clave:** Muestra la preferencia de los clientes por los diferentes métodos de pago utilizados.
    *   **Utilidad:** Informa sobre qué opciones de pago son más utilizadas y puede guiar decisiones sobre nuevas implementaciones o promociones.

3.  **Ingresos Totales por Día (Serie de Tiempo):**
    *   **Tipo de Gráfico:** Línea
    *   **Conclusión Clave:** Visualiza la tendencia de los ingresos totales a lo largo del tiempo, identificando patrones diarios, semanales o picos de ventas.
    *   **Utilidad:** **Considerada la conclusión más relevante**, proporciona una visión macro del rendimiento financiero del negocio, crucial para la toma de decisiones estratégicas y pronósticos.

4.  **Distribución de los Valores de Venta:**
    *   **Tipo de Gráfico:** Histograma (con KDE)
    *   **Conclusión Clave:** Ilustra la frecuencia de los diferentes rangos de precios de las transacciones.
    *   **Utilidad:** Permite comprender la estructura de precios de los productos y la "ticket promedio" de las ventas, así como detectar valores atípicos.

## Cómo Utilizar

1.  **Clonar el Repositorio:**
    ```bash
    git clone https://github.com/LenninTemoche/test-colab-jupyter.git
    cd test-colab-jupyter
    ```
2.  **Instalar Dependencias:**
    Asegúrate de tener Python instalado. Luego, instala las librerías necesarias:
    ```bash
    pip install pandas matplotlib seaborn
    ```
3.  **Ejecutar el Análisis:**
    Abre el archivo `*.ipynb` en un entorno como Jupyter Notebook o JupyterLab, y ejecuta todas las celdas para ver los gráficos y conclusiones.

    Navega hasta el archivo `*.ipynb` y ábrelo.

## Dataset

El archivo `panini.csv` debe estar en el mismo directorio que el script o notebook para que el código funcione correctamente. Asegúrate de que las columnas `fecha`, `producto`, `valor` y `metodo_pago` existan y contengan datos consistentes.
