# Análisis de Evasión de Clientes (Churn) - Telecom X

## 📄 Descripción General del Proyecto

Este repositorio contiene el análisis completo de evasión de clientes (Churn) para **Telecom X**, una empresa de telecomunicaciones. El objetivo principal de este proyecto es comprender los factores subyacentes que contribuyen a la pérdida de clientes y proporcionar insights accionables para desarrollar estrategias de retención efectivas.

El análisis abarca desde la preparación y limpieza de los datos hasta la exploración visual de patrones, culminando en conclusiones y recomendaciones estratégicas.

## 🎯 Objetivo del Análisis

El objetivo de este análisis es:
* Identificar las variables y patrones que influyen en la decisión de los clientes de cancelar su servicio (Churn).
* Cuantificar la magnitud del problema de churn.
* Proporcionar insights basados en datos que permitan a Telecom X comprender mejor a sus clientes y tomar decisiones informadas para reducir la tasa de evasión.

## 🚀 Contenido del Repositorio

* `notebook/`: Contiene el notebook de Google Colab (`TelecomX_LATAM (1).ipynb`) con todo el código, análisis, visualizaciones y el informe final.
* `data/`: Aquí se debería almacenar el conjunto de datos original (`TelecomX_Data.json`).
* `README.md`: Este archivo, que proporciona una descripción del proyecto.

## 🛠️ Herramientas y Librerías Utilizadas

El análisis fue realizado utilizando Python y las siguientes librerías principales:

* **`pandas`**: Para manipulación y análisis de datos.
* **`numpy`**: Para operaciones numéricas y manejo de datos faltantes.
* **`matplotlib`**: Para la creación de visualizaciones estáticas.
* **`seaborn`**: Para la creación de gráficos estadísticos más atractivos y complejos.
* **`json`**: Para la lectura de archivos JSON.

## ⚙️ Pasos del Análisis

El análisis se llevó a cabo siguiendo una metodología estructurada:

### 1. **Limpieza y Tratamiento de Datos**
    * **Carga de Datos:** Importación del archivo de datos (`.json` en este caso) y normalización de su estructura si contenía diccionarios anidados.
    * **Renombre y Estandarización:** Renombre de columnas para mayor claridad y conversión de textos a minúsculas.
    * **Manejo de Datos Faltantes y Tipos de Datos:** Identificación y tratamiento de valores nulos (rellenando con 0 en columnas numéricas como `Total`). Conversión de tipos de datos a los formatos adecuados (ejemplo, strings a numéricos).
    * **Estandarización de Variables Binarias:** Transformación de columnas con valores `Yes`/`No` a `1`/`0`.
    * **Creación de Nuevas Características:** Generación de la columna `CuentasDiarias` a partir de `Monthly`.

### 2. **Análisis Exploratorio de Datos (EDA)**
    * **Distribución de Churn:** Visualización de la proporción de clientes que No Permanecen vs. los que Permanecen (gráfico de pastel y barras).
    * **Análisis por Variables Categóricas:**
        * **Género:** Comparación de la distribución de género entre clientes que No Permanecen y los que Permanecen (gráficos de barras).
        * **Tipo de Contrato:** Análisis del churn según la duración del contrato (gráficos de barras).
        * **Método de Pago:** Exploración de la relación entre el método de pago y la evasión (gráficos de barras).
        * **SeniorCitizen:** Comparación de la tasa de churn entre clientes mayores de 65 años y menores a 65 años (gráficos de barras).
    * **Análisis por Variables Numéricas:**
        * **Total Gastado:** Distribución del gasto total para clientes que No Permanecen y los que Permanecen (histogramas con KDE).
        * **Meses de Contrato (Tenure):** Distribución de la antigüedad del contrato para clientes que No Permanecen y los que Permanecen (histogramas con KDE).

## 📊 Conclusiones e Insights Clave

Los hallazgos principales del análisis incluyen:

* **Alta Tasa de Churn:** Telecom X enfrenta una tasa de churn significativamente alta (aproximadamente **74.28%** de los clientes 'No Permanecen'), lo que requiere atención inmediata.
* **El Contrato "Month-to-month" es un Gran Riesgo:** Los clientes con este tipo de contrato son, por mucho, los más propensos a la evasión. Tienen una mayor flexibilidad para cancelar, lo que se traduce en menor lealtad.
* **Método de Pago "Electronic Check" es un Punto Débil:** Los clientes que utilizan este método de pago muestran una mayor tendencia al churn, lo que sugiere posibles problemas con el proceso o la percepción de este método.
* **Clientes Nuevos y con Bajo Gasto son los Más Vulnerables:** La evasión es notablemente alta en los primeros meses de contrato y entre clientes con un bajo gasto total acumulado. Esto indica que la fase de la propuesta de valor inicial es crítica.
* **Clientes Mayores a 65 años, un Segmento de Atención:** Proporcionalmente, los clientes mayores de 65 años (`SeniorCitizen`) muestran una mayor propensión a la evasión, lo que podría indicar necesidades no cubiertas para este demográfico.
* **El Género no es un Factor Diferenciador:** No se encontró una relación significativa entre el género del cliente y la probabilidad de evasión.

## 📝 Recomendaciones Estratégicas

Basado en los insights anteriores, se proponen las siguientes acciones para Telecom X:

1.  **Incentivar Contratos a Largo Plazo:** Crear ofertas atractivas (descuentos, beneficios exclusivos, mejoras de servicio) para migrar clientes de contratos "month-to-month" a planes de uno o dos años.
2.  **Fortalecer la propuesta inicial y Monitoreo Temprano:** Implementar un programa de bienvenida robusto y un seguimiento proactivo durante los primeros 3-6 meses de servicio, especialmente para clientes con bajo gasto inicial. Esto puede incluir llamadas de seguimiento, encuestas de satisfacción y asistencia técnica personalizada.
3.  **Evaluar y Optimizar el Método de Pago "Electronic Check":** Investigar las razones detrás del churn asociado a este método. Considerar campañas para incentivar el cambio a métodos de pago automáticos y más estables (ejemplo, tarjeta de crédito, transferencia bancaria).
4.  **Desarrollar Estrategias Específicas para Clientes Mayores a 65 años:** Adaptar la comunicación, el soporte y posiblemente los paquetes de servicios para satisfacer las necesidades de los clientes mayores, fomentando su retención.
5.  **Implementar un Sistema de Alerta Temprana de Churn:** Utilizar los insights de este análisis para construir un modelo predictivo de churn que identifique a los clientes en riesgo antes de que cancelen, permitiendo intervenciones proactivas y personalizadas.

Al abordar estos factores clave, Telecom X puede mejorar significativamente sus tasas de retención de clientes y asegurar un crecimiento más sostenible.

---

## 🚀 Cómo Ejecutar el Proyecto

1.  **Clonar el Repositorio:**
    ```bash
    git clone [https://github.com/JorgeJuarez97/telecomx_analisis_datos](https://github.com/JorgeJuarez97/telecomx_analisis_datos)
    cd tu-repositorio
    ```
2.  **Instalar Dependencias:**
    Se recomienda usar un entorno virtual.
    ```bash
    pip install pandas
    pip install numpy
    pip install matplotlib
    pip install seaborn
    ```
3.  **Abrir el Notebook:**
    ```bash
    jupyter notebook
    ```
    Navega hasta el archivo `notebook/TelecomX_LATAM (1).ipynb` y ábrelo.

4.  **Ejecutar las Celdas:**
    Ejecuta todas las celdas del notebook secuencialmente para replicar el análisis y las visualizaciones.

---

## 🤝 Contribuciones

Si tienes sugerencias o mejoras, no dudes en abrir un *issue* o enviar un *pull request*.

## 📞 Contacto

* **Correo Electrónico:** [jorgejuarez0407@gmail.com]
* **LinkedIn:** [https://www.linkedin.com/in/jorge-d-juarez/]
