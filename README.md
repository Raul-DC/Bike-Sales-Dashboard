
# Proyecto Excel: Análisis de Ventas de Motocicletas

## 📌 Introducción
 Este proyecto guía paso a paso la creación de un dashboard interactivo en Excel para analizar patrones de compra de motocicletas, utilizando técnicas profesionales de análisis de datos.

## 🔍 Paso 1: Preparación del Entorno
1. **Estructura del libro**:

     - `bike_buyers` (Dataset Original)

   - Creé 3 hojas adicionales:
     - `Working Sheet` (Datos limpios)
     - `Pivot Table` (Análisis)
     - `Dashboard` (Panel visual)

   ![image](https://github.com/user-attachments/assets/1d7c870c-ef98-4b53-ba1a-c73c7c9b8d79)


3. 🛡️**Protección de datos**:
   - Copié todos los datos de `bike_buyers` a `Working Sheet` para preservar los datos originales.

## 🧹 Paso 2: Limpieza de Datos
1. **Eliminación de duplicados**:
   - Usé la opción `Data > Remove Duplicates` (se encontraron y eliminaron 26 registros duplicados) ✔️

2. **Normalización de valores**:
  
   ![image](https://github.com/user-attachments/assets/0b659534-162b-4925-80a8-7c4b2972c8d7)

   ![image](https://github.com/user-attachments/assets/ea9e53c0-4e59-4b98-a4c8-214b0840a5aa)
   

4. **Creación de rangos de edad**:

   ![image](https://github.com/user-attachments/assets/180d31b6-441e-4ae0-9b92-74f74dd63131)

   - Añadí columna "Age Brackets" con la fórmula:

   ```excel
   =IF(L15>54,"Old",IF(L15>=31,"Middle Age",IF(L15<31,"Adolescent","Invalid")))
   ```

## 📐 Paso 3: Tablas Dinámicas (Pivot Tables)
1. **Ingreso promedio por género**:
   - Rows: Gender
   - Columns: Purchased Bike
   - Values: Average of Income

   ![image](https://github.com/user-attachments/assets/6e020412-7e80-4516-bb1d-6125041b6e90)

2. **Distancia de viaje al trabajo de cada cliente**:
   - Rows: Commute Distance
   - Values: Count of Purchased Bike
   - (Tuve que ajustar "10+ Miles" → "More than 10 Miles")
  
   ![image](https://github.com/user-attachments/assets/e3f3a5bb-c009-469e-be36-e206bad57d80)

3. **Rangos de edad**:
   - Rows: Age Brackets
   - Values: Count of Purchased Bike
  
   ![image](https://github.com/user-attachments/assets/414b556e-f671-48ca-88e3-8955dcbd078e)

4. **Rasgos de un cliente ideal**:
   - Rows: Income, Commute Distance y Cars
   - Columns: Purchased Bike
   - Values: Count of ID
     
   ![image](https://github.com/user-attachments/assets/836df74c-c322-4979-bf32-29b64b3189c6)

   

## 📊📈 Paso 4: Visualizaciones
1. **Gráficos de columnas**:
   - Para cada tabla dinámica creé gráficos clustered column
   - Añadí títulos y formato profesional

   ![image](https://github.com/user-attachments/assets/8d11341d-7387-4902-b73e-13a0fdb5347c)
   ![image](https://github.com/user-attachments/assets/310328a5-fd3c-41a3-b5ae-2af157f42aae)
   ![image](https://github.com/user-attachments/assets/ac81373d-97f5-4b6d-bf5f-87e5850771b7)


2. **Gráfico de anillos (cliente ideal)**:
   - Tipo: Doughnut Chart
   - Muestra relación entre Income, Cars y Commute Distance

## 🖥️ Paso 5: Dashboard Interactivo
1. **Diseño base**:
   - Eliminé gridlines (View > Show > Gridlines)
   - Creé un header con merge cells y formato profesional

   ![Header dashboard](https://i.imgur.com/ejemplo5.png)  
   *Captura: Diseño inicial del dashboard*

2. **Organización de gráficos**:
   - Alinear gráficos con:
     - `Shape Format > Align > Align Top/Left`
   - Tamaños proporcionales

3. **Filtros interactivos**:
   - Inserté slicers para:
     1. Marital Status
     2. Region
     3. Education
   - Conecté todos los filtros a cada tabla dinámica

   ![Filtros](https://i.imgur.com/ejemplo6.png)  
   *Captura: Dashboard final con filtros aplicados*

## 🔎 Hallazgos Clave
- **Casados vs Solteros**: Los compradores casados tienen ingresos promedio más altos
- **Edad**: Personas de mediana edad (31-54) compran más bicicletas
- **Distancia**: Clientes que viven a 5-10 millas son los que más compran

## 💡 Cómo Personalizar
1. Para cambiar rangos de edad, modifica la fórmula en "Age Brackets"
2. Añade más filtros con:  
   `PivotChart Analyze > Insert Slicer`
3. Cambia colores con:  
   `Chart Design > Change Colors`

## 📌 Notas sobre las capturas:
1. **Reemplaza las URLs** de ejemplo (i.imgur.com/ejemploX.png) con tus propias capturas
2. **Sugerencias para las imágenes**:
   - Usa nombres descriptivos como `dashboard_final.png`
   - Asegúrate que se vean claramente:
     - Las fórmulas importantes
     - El before/after de limpieza de datos
     - Los filtros en acción
3. **Herramientas recomendadas**:
   - Para capturas: Lightshot o Snipping Tool
   - Para edición: Paint o Canva
