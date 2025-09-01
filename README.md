# Dashboard Interactivo de Análisis de Homicidios en Norteamérica (2005-2022)

Este proyecto documenta el desarrollo de un dashboard interactivo para el análisis comparativo de tasas de homicidios en México, Estados Unidos y Canadá durante el período 2005-2022. A través del uso de Python y librerías especializadas como Plotly, Dash y pandas, se implementa una solución de visualización multi-dimensional que combina mapas coropléticos, análisis por género y evolución temporal. Los datos provienen de la Oficina de las Naciones Unidas contra la Droga y el Delito (UNODC), garantizando la fiabilidad y estandarización internacional de la información.

## Objetivo

Desarrollar una herramienta de visualización interactiva que permita analizar y comparar patrones de criminalidad entre los tres países de Norteamérica, identificando disparidades regionales, diferencias de género y tendencias temporales en las tasas de homicidios intencionales.

## Flujo de trabajo

### 1. Preparación y limpieza de datos
- Carga del dataset CSV de 4,241 registros con `pandas`
- Eliminación de filas sin datos relevantes y reestructuración de columnas
- Conversión de tipos de datos y validación de valores numéricos
- Filtrado específico para México, Estados Unidos y Canadá

### 2. Procesamiento de datos por dimensiones
- **Datos geográficos**: Agrupación por país y año para tasas generales
- **Datos de género**: Extracción y clasificación de porcentajes por sexo
- **Datos temporales**: Consolidación de series históricas 2005-2022
- Aplicación de transformaciones para optimizar visualizaciones

### 3. Desarrollo de visualizaciones interactivas
- **Mapa coroplético animado**:
  - Proyección geográfica enfocada en Norteamérica
  - Escala de colores secuencial (OrRd) para intensidad de tasas
  - Animación temporal con controles de reproducción
- **Gráficos de barras por género**:
  - Paneles faceteados por país (facet_col)
  - Agrupación por género con modo barras comparativas
  - Diseño responsivo con template 'plotly_white'

### 4. Análisis de evolución temporal
- **Gráfico de líneas múltiples**:
  - Líneas suavizadas (spline) para tendencias
  - Código de colores distintivo por país
  - Marcadores para puntos de datos específicos
- Implementación de hover unificado para comparación directa

### 5. Integración en dashboard Dash
- Desarrollo de aplicación web interactiva con layout estructurado
- Organización jerárquica de componentes HTML y gráficos
- Estilización CSS integrada para presentación profesional
- Configuración de servidor de desarrollo con modo debug

### 6. Validación y presentación
- Verificación de integridad de datos tras transformaciones
- Documentación de objetivos específicos por visualización
- Contextualización sociopolítica de patrones observados

## Herramientas utilizadas

- Python 3.x
- pandas, NumPy  
- Plotly, Plotly Express
- Dash framework
- Jupyter Notebook

## Características técnicas destacadas

### Visualizaciones implementadas
1. **Mapa coroplético**: Distribución geográfica con animación temporal
2. **Barras agrupadas**: Análisis comparativo por género y país
3. **Líneas temporales**: Evolución histórica con marcadores distintivos

### Procesamiento de datos
- Filtrado de 4,241 registros a 71 observaciones relevantes
- Manejo de valores nulos y conversión de tipos automática
- Agrupación y agregación por múltiples dimensiones

### Interactividad
- Dashboard web completamente funcional
- Controles de animación temporal
- Hover tooltips informativos
- Diseño responsivo multi-panel

## Conclusiones

- La limpieza de datos redujo el dataset en 94% manteniendo solo información relevante para el análisis regional
- El enfoque multi-dimensional (geográfico, género, temporal) proporciona perspectiva integral del fenómeno
- La implementación de Dash permite exploración interactiva superior a visualizaciones estáticas
- Los patrones identificados revelan disparidades significativas entre países y géneros
- La contextualización sociopolítica conecta los datos con realidades regionales (violencia organizada, políticas públicas)
- El framework desarrollado es escalable para incluir otros países o períodos temporales
