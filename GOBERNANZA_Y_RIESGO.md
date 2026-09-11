# GOBERNANZA Y RIESGO — Agente de Análisis y Prevención de Accidentes Laborales

## 1. Principio de funcionamiento

El agente funciona como una herramienta de apoyo a la gestión de Seguridad e Higiene. Su objetivo es transformar una base de accidentes laborales en indicadores, focos de riesgo, recomendaciones y un plan de acción priorizado.

El sistema no reemplaza el criterio profesional ni toma decisiones finales. Las interpretaciones y recomendaciones generadas requieren supervisión humana antes de ser utilizadas para implementar acciones.

## 2. Sistemas utilizados y permisos

El agente trabaja sobre un archivo Excel proporcionado por el usuario.

Permisos habilitados:
- Lectura de la información cargada.
- Validación y análisis de los datos.
- Cálculo de indicadores.
- Generación de una salida estructurada.
- Elaboración de recomendaciones y propuestas de acción.

Permisos no habilitados:
- Modificación de la base original.
- Escritura o modificación de sistemas corporativos.
- Envío automático de comunicaciones.
- Implementación automática de acciones.
- Aplicación de sanciones o medidas disciplinarias.
- Decisiones médicas, legales o laborales.

Por lo tanto, el agente posee capacidad de análisis y recomendación, pero no capacidad de ejecución sobre los sistemas o procesos de la organización.

## 3. Niveles de supervisión humana

Para este proyecto se definen los siguientes niveles:

| Nivel | Actividad | Supervisión |
|---|---|---|
| L0 | Decisiones disciplinarias, médicas, legales o determinación de responsabilidades | Fuera del alcance del agente |
| L1 | Lectura del Excel, validación, conteos, indicadores y detección de faltantes o duplicados | Ejecución automática |
| L2 | Identificación de patrones, focos de riesgo y priorización | El agente propone y una persona revisa |
| L2 | Recomendaciones preventivas, correctivas y de capacitación | El agente propone y una persona revisa |
| L3 | Plan de acción, responsables sugeridos, plazos e indicadores de seguimiento | Requiere aprobación humana antes de su implementación |
| L4 | Ejecución automática de acciones o modificaciones en sistemas de la organización | No habilitada |

Los niveles utilizados son una definición operativa específica de este proyecto para explicitar el grado de autonomía y supervisión de cada actividad.

## 4. Principales modos de falla

### Exposición de información confidencial

El agente puede reproducir nombres de personas, empresas u operaciones si las instrucciones de anonimización no son suficientemente específicas.

Este riesgo se verificó durante las primeras corridas del proyecto y motivó dos iteraciones del contrato. La versión final reemplaza las denominaciones organizacionales por identificadores genéricos y prohíbe generar equivalencias con los valores originales.

### Inferencia de causas no demostradas

La recurrencia de determinados accidentes no demuestra por sí misma una causa raíz. El agente debe diferenciar los datos observados de sus interpretaciones y no atribuir causalidad cuando la base no la permite establecer.

### Comparaciones sin información de exposición

Una operación puede concentrar mayor cantidad de accidentes simplemente porque posee mayor dotación, actividad u horas trabajadas. Sin esos denominadores, el agente no debe afirmar que una operación posee mayor riesgo relativo.

Cuando la información necesaria no se encuentra disponible debe indicar “Datos insuficientes”.

### Calidad insuficiente de los datos

Errores, registros incompletos, clasificaciones inconsistentes o información faltante pueden afectar las conclusiones. El agente debe informar estas limitaciones antes de elaborar recomendaciones.

### Recomendaciones no aplicables al contexto real

Una recomendación puede ser coherente con los datos y, sin embargo, no ser técnica, económica u operativamente viable. Por ese motivo ninguna recomendación se implementa automáticamente.

## 5. Controles humanos antes de utilizar la salida

Antes de utilizar las conclusiones o recomendaciones, el responsable humano debe revisar:

1. La calidad y suficiencia de la información analizada.
2. La correcta interpretación de los patrones identificados.
3. La validez de cualquier hipótesis sobre causas.
4. La priorización propuesta de los riesgos.
5. La viabilidad técnica y operativa de las acciones sugeridas.
6. Los responsables y plazos propuestos.
7. La ausencia de información confidencial en la salida.

## 6. Aprobación final

El Responsable de Seguridad e Higiene es quien debe validar las interpretaciones, prioridades y recomendaciones antes de utilizarlas para tomar decisiones o implementar acciones.

Cuando una medida propuesta implique decisiones organizacionales de mayor impacto, deberá intervenir además la gerencia correspondiente.

Las decisiones disciplinarias, médicas y legales permanecen fuera del alcance del agente y deben ser tratadas exclusivamente por los responsables humanos y profesionales correspondientes.

## 7. Criterio final de gobernanza

El diseño adoptado prioriza un esquema de autonomía limitada: el agente puede analizar, detectar y recomendar, pero no ejecutar.

El valor del sistema consiste en acelerar y estructurar el análisis de información, manteniendo la responsabilidad y la decisión final en las personas responsables de la gestión.