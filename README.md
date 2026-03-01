# ChallengeTelecomX


##  Sobre este proyecto

Este es mi primer proyecto completo de análisis de datos, desarrollado como parte
del challenge de **Alura Oracle Next ONE — Data Science LATAM**.

El objetivo fue analizar el comportamiento de los clientes de **Telecom X** para
entender por qué se van (churn) y qué factores influyen en esa decisión.



##  Objetivo

Identificar patrones en los datos de clientes de una empresa de telecomunicaciones
para ayudar a reducir la tasa de evasión del **26.54%**.


##  Fuente de datos

Los datos fueron extraídos directamente desde una API en formato JSON:
```
https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/main/TelecomX_Data.json
```


##  Etapas del análisis

### 1. Extracción
- Conexión a la API con `requests`
- Normalización del JSON anidado con `pd.json_normalize()`
- Dataset inicial: **7,267 filas × 21 columnas**

### 2. Limpieza (ETL)
- Eliminación de 224 filas con `Churn` vacío
- Conversión de `Charges.Total` de texto a número
- Relleno de 11 nulos con la mediana
- Creación de columna `Cuentas_Diarias`
- Dataset final: **7,043 clientes, 22 columnas, 0 nulos** 

### 3. Análisis Exploratorio (EDA)
- Estadísticas descriptivas con `df.describe()`
- 6 visualizaciones con `matplotlib` y `seaborn`


## Principales hallazgos

| Factor | Hallazgo |
|---|---|
| Tasa de evasión | 26.54% (1,869 de 7,043 clientes) |
| Contrato mes a mes | Mayor tasa de cancelación |
| Tenure bajo | Los primeros meses son los más críticos |
| Cheque electrónico | Método de pago con más evasión |
| Cargo mensual alto | Clientes que pagan más tienden a cancelar más |
| Género | Sin diferencia significativa |



##  Recomendaciones

- Incentivar contratos anuales con descuentos
- Programa de bienvenida reforzado en los primeros meses
- Promover el pago automático
- Revisar la percepción de valor en planes de alto costo

---

## Tecnologías usadas

- Python 3
- Pandas
- Matplotlib
- Seaborn
- Google Colab

---

## 🌸 Sobre mí

¡Hola! Soy Giselle, estudiante de Data Science 💛  
Este es mi primer proyecto y estoy muy emocionada de seguir aprendiendo.  
Si tienes algún comentario o sugerencia, ¡con gusto lo recibo!


---

*Proyecto desarrollado como parte del Challenge 2 — Data Science LATAM | Alura ONE*
