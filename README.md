# 📊 TelecomX: Análisis de Evasión de Clientes (Churn Analysis)

Este proyecto realiza un análisis profundo de los datos de **TelecomX**, una empresa de telecomunicaciones, con el objetivo de identificar patrones de comportamiento en los clientes que deciden cancelar sus servicios (*Churn*). A través de la limpieza, normalización y visualización de datos, buscamos generar insights estratégicos para reducir la tasa de abandono.

## 🎯 Objetivo del Proyecto
Identificar las variables clave que influyen en la salida de clientes y proporcionar recomendaciones basadas en datos para mejorar la retención y la fidelidad de los usuarios.

## 🛠️ Tecnologías Utilizadas
* **Python 3.x**
* **Pandas**: Manipulación y limpieza de datos.
* **Seaborn & Matplotlib**: Visualización de datos y análisis estadístico.
* **NumPy**: Operaciones matemáticas y manejo de nulos.
* **JSON Normalize**: Procesamiento de estructuras de datos anidadas.

## 📁 Estructura de los Datos
El dataset original se encuentra en formato JSON con estructuras anidadas. Las dimensiones principales incluyen:
* **Customer**: ID, género, edad (SeniorCitizen), dependientes.
* **Phone & Internet**: Servicios contratados, líneas múltiples, seguridad en línea, etc.
* **Account**: Tipo de contrato, método de pago, cargos mensuales y totales.

## 🚀 Proceso de Transformación (ETL)
Para asegurar la calidad del análisis, se realizaron las siguientes tareas:
1.  **Normalización**: Desglose de diccionarios anidados en el JSON a columnas individuales.
2.  **Limpieza**: Conversión de `Charges.Total` a formato numérico y tratamiento de valores nulos.
3.  **Estandarización**: Conversión de variables categóricas ("Sí", "No") a valores binarios (1, 0).
4.  **Ingeniería de Variables**: Creación de la métrica `Cuentas_Diarias` (Cargo Mensual / 30) para granularidad económica.

## 📊 Principales Hallazgos (Insights)
* **Contratos Críticos**: Los clientes con contratos **mes a mes** representan el mayor volumen de evasión.
* **Sensibilidad al Precio**: Existe una tendencia de abandono en clientes con cargos mensuales superiores al promedio, especialmente si no cuentan con servicios de valor agregado (Soporte Técnico o Seguridad).
* **Lealtad vs. Antigüedad**: Los primeros 6 meses de contrato son críticos; si el cliente supera este periodo, su probabilidad de abandono disminuye drásticamente.
* **Métodos de Pago**: Los pagos manuales (Electronic Check) tienen una tasa de deserción mucho más alta que los pagos automatizados.

## 📋 Conclusiones y Recomendaciones
1.  **Migración de Contratos**: Implementar incentivos para convertir clientes "Month-to-month" a contratos anuales.
2.  **Fidelización Temprana**: Crear programas de acompañamiento (*Customer Success*) para nuevos usuarios durante su primer trimestre.
3.  **Automatización**: Promover el pago domiciliado mediante beneficios exclusivos para reducir la fricción en la facturación.

## 💻 Cómo ejecutar el proyecto
1. Clona este repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/TelecomX-Churn-Analysis.git](https://github.com/tu-usuario/TelecomX-Churn-Analysis.git)
