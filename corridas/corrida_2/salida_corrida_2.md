# CORRIDA 2 — V2

Fecha: 11/09/2026
Entrada: misma base real de accidentes laborales utilizada en la Corrida 1.
Contrato: System Prompt V2 + mismo User Prompt V1.
Iteración aplicada: modificación exclusiva de RESTRICCIONES para incorporar validación previa de anonimización.

## SALIDA ORIGINAL
### A. VALIDACIÓN DE LA BASE

| Campo | Resultado |
|---|---|
| Registros analizados | 60 |
| Período analizado | 02/01/2026 al 30/07/2026 |
| Registros duplicados | 0 duplicados exactos; 0 duplicados al excluir nombre y apellido |
| Datos faltantes relevantes | Sin valores faltantes en las 15 columnas analizadas |
| Calidad general de datos | Adecuada para análisis descriptivo de casos y días. Las fechas y campos numéricos resultaron válidos; no se detectaron días negativos ni días ILT superiores a días de baja. |
| Limitaciones detectadas | La base contiene nombre y apellido, que no se reproducen. No hay dotación ni horas trabajadas: **Datos insuficientes** para tasas de frecuencia, gravedad o comparaciones de riesgo por exposición. Julio puede continuar acumulando días de baja. La clasificación de causa raíz es general y requiere validación humana. |

### B. INDICADORES PRINCIPALES

| Indicador | Resultado |
|---|---:|
| Total de accidentes | 60 |
| Días de baja | 1.522 |
| Días ILT | 976 |
| Promedio de días perdidos por caso | 25,4 |
| Operación con mayor cantidad de casos | Operación CMQ: 35 casos (58,3%) |
| Operación con mayor impacto | Operación CMQ: 551 días de baja (36,2%) |
| Tipo de lesión más frecuente | Contusiones: 32 casos (53,3%) |
| Parte del cuerpo más afectada | Tobillo: 9 casos (15,0%) y 282 días de baja |
| Evolución temporal | Ene: 12 casos / 266 días; Feb: 10 / 334; Mar: 10 / 410; Abr: 5 / 87; May: 5 / 144; Jun: 8 / 159; Jul: 10 / 122 |

### C. FOCOS DE RIESGO PRIORIZADOS

| Prioridad | Foco de riesgo | Evidencia observada | Frecuencia | Impacto/gravedad | Nivel de riesgo | Confianza |
|---|---|---|---:|---|---|---|
| 1 | Fracturas cerradas | 5 casos y 491 días de baja; promedio de 98,2 días por caso | Baja | 32,3% de los días de baja totales | Alto | Alta |
| 2 | Clasificación “No uso de los tres puntos de apoyo” | 13 casos y 463 días de baja | Alta | Promedio de 35,6 días por caso | Alto | Media |
| 3 | Manipulación manual de cargas (MMC) | 19 casos y 423 días de baja | Más alta entre las clasificaciones de causa | Promedio de 22,3 días por caso | Alto | Media |
| 4 | Operación CMQ | 35 casos y 551 días de baja | 58,3% de los casos | 36,2% de los días de baja | Alto | Alta |
| 5 | Lesiones en tobillo | 9 casos y 282 días de baja | Mayor zona corporal afectada | Promedio de 31,3 días por caso | Medio-alto | Alta |

### D. PLAN DE ACCIÓN

| Prioridad | Riesgo identificado | Acción propuesta | Tipo de acción | Responsable sugerido | Plazo | Indicador de seguimiento |
|---|---|---|---|---|---|---|
| 1 | Fracturas cerradas | Revisar individualmente los cinco eventos y validar condiciones, tareas y controles asociados antes de definir medidas específicas. | Investigación preventiva | Seguridad e Higiene y responsable operativo | 30 días | Casos y días de baja por fractura |
| 2 | Tres puntos de apoyo | Revisar tareas de ascenso y descenso, condiciones de acceso y realizar observaciones preventivas y capacitación específica. | Correctiva y capacitación | Seguridad e Higiene y supervisión operativa | 30 días | Casos y días de baja con esa clasificación |
| 3 | MMC | Evaluar tareas asociadas, métodos de manipulación y necesidad de ayudas mecánicas o rediseño operativo. | Preventiva y ergonómica | Seguridad e Higiene y Operaciones | 45 días | Casos y días de baja clasificados como MMC |
| 4 | Operación CMQ | Realizar revisión focalizada de los 35 eventos para segmentar tareas, lesiones y clasificaciones reportadas. | Diagnóstico y prevención | Responsable de operación y Seguridad e Higiene | 30 días | Casos y días de baja de la operación |
| 5 | Lesiones en tobillo | Revisar circulación, orden y limpieza y condiciones de tránsito en los eventos involucrados. | Preventiva | Supervisión operativa y Seguridad e Higiene | 45 días | Casos y días de baja por lesiones en tobillo |

### E. CONCLUSIONES Y SUPERVISIÓN HUMANA

1. **Dato observado:** Se registraron 60 casos, 1.522 días de baja y 976 días ILT durante el período analizado.
2. **Dato observado:** Las fracturas cerradas representan 5 casos, pero concentran 491 días de baja, por lo que constituyen el principal foco por gravedad.
3. **Interpretación:** La recurrencia de eventos clasificados como MMC y como falta de uso de tres puntos de apoyo justifica revisar preventivamente las tareas asociadas. La base no permite establecer una causa raíz común definitiva.
4. **Interpretación:** La operación CMQ concentra la mayor cantidad de casos y días de baja, aunque **Datos insuficientes** para afirmar que posee mayor riesgo relativo sin dotación u horas trabajadas.
5. **Recomendación:** Priorizar la investigación preventiva de fracturas y la revisión de controles para ascenso, descenso y manipulación manual de cargas.

Las interpretaciones, prioridades y recomendaciones deben ser revisadas por el responsable de Seguridad e Higiene antes de utilizarse para tomar decisiones o implementar acciones.