# CORRIDA 3 — V3

Fecha: 11/09/2026
Entrada: misma base real de accidentes laborales utilizada en las Corridas 1 y 2.
Contrato: System Prompt V3 + mismo User Prompt V1.
Iteración aplicada: anonimización explícita de empresas, unidades de negocio y operaciones mediante identificadores genéricos.

## SALIDA ORIGINAL
### A. VALIDACIÓN DE LA BASE

| Ítem | Resultado |
|---|---|
| Registros analizados | 60 |
| Período analizado | 02/01/2026 al 30/07/2026 |
| Registros duplicados | 0 duplicados exactos. 4 personas aparecen en 2 registros, pero no hay legajo para validar reincidencia. |
| Datos faltantes relevantes | Sin valores faltantes en las 15 columnas de los 60 registros. Datos insuficientes para dotación, horas trabajadas y exposición. |
| Calidad general de datos | Buena para conteos, distribución y días de baja/ILT. Los campos numéricos de días coinciden con sus campos de origen, no presentan valores negativos y los días ILT no superan los días de baja. |
| Limitaciones detectadas | Se detectaron campos identificatorios personales, que no se reproducen. Las denominaciones organizacionales se reemplazaron por identificadores genéricos. Julio puede continuar acumulando días de baja. La clasificación de causa raíz es general y requiere validación humana. |

### B. INDICADORES PRINCIPALES

| Indicador | Resultado |
|---|---|
| Total de accidentes | 60 |
| Días de baja | 1.522 |
| Días ILT | 976 |
| Promedio de días perdidos por caso | 25,4 días de baja |
| Operación con mayor cantidad de casos | Operación_006: 35 casos (58,3%) |
| Operación con mayor impacto | Operación_006: 551 días de baja |
| Tipo de lesión más frecuente | Contusiones: 32 casos (53,3%) |
| Parte del cuerpo más afectada | Hombro: 7 casos. Tobillo: mayor impacto, con 282 días de baja en 9 casos. |
| Evolución temporal | Máximo de casos: enero, 12. Máximo de días de baja: marzo, 410. |
| Categoría de causa raíz más frecuente | MMC: 19 casos y 423 días de baja |
| Lesión de mayor impacto | Fractura cerrada: 5 casos, 491 días de baja y promedio de 98,2 días por caso |
| Tasa de frecuencia o gravedad | Datos insuficientes. No se informan horas trabajadas ni dotación. |

### C. FOCOS DE RIESGO PRIORIZADOS

| Prioridad | Foco de riesgo | Evidencia observada | Frecuencia | Impacto/gravedad | Nivel de riesgo | Confianza |
|---|---|---|---:|---|---|---|
| 1 | Eventos clasificados como “No uso de los tres puntos de apoyo” | 13 casos, 463 días de baja y 305 días ILT. Incluye 2 fracturas cerradas con 224 días de baja. | 21,7% | 35,6 días de baja promedio por caso | Alto | Media |
| 2 | Fracturas cerradas | 5 casos concentraron 491 días de baja y 413 días ILT. | 8,3% | 98,2 días de baja promedio por caso | Alto | Alta |
| 3 | Manipulación manual de cargas (MMC) | 19 casos, la categoría más frecuente, con 423 días de baja. | 31,7% | 22,3 días de baja promedio por caso | Alto | Media |
| 4 | Orden y limpieza | 10 casos y 303 días de baja. Cuatro eventos en tobillo suman 210 días de baja. | 16,7% | 30,3 días de baja promedio por caso | Alto | Media |
| 5 | Operación_006 | Concentró 35 casos y 551 días de baja. | 58,3% | 15,7 días de baja promedio por caso | Alto por frecuencia | Alta |
| 6 | Operación_001 | Registró 11 casos y 382 días de baja, con 34,7 días promedio por caso. | 18,3% | Impacto elevado respecto del promedio general | Alto por gravedad | Alta |

### D. PLAN DE ACCIÓN

| Prioridad | Riesgo identificado | Acción propuesta | Tipo de acción | Responsable sugerido | Plazo | Indicador de seguimiento |
|---|---|---|---|---|---|---|
| 1 | No uso de los tres puntos de apoyo | Revisar tareas de ascenso, descenso y acceso; realizar observaciones preventivas e investigar los eventos de mayor baja. | Correctiva y preventiva | Seguridad e Higiene y jefatura operativa | 30 días | Casos y días de baja asociados a esta categoría |
| 2 | Fracturas cerradas | Realizar investigación humana de los 5 eventos y verificar controles existentes en las tareas involucradas. | Investigación y correctiva | Seguridad e Higiene | 30 días | Casos de fractura cerrada y días de baja asociados |
| 3 | MMC | Revisar tareas con manipulación de cargas, métodos de trabajo y necesidad de capacitación específica. | Preventiva y capacitación | Seguridad e Higiene y supervisión operativa | 45 días | Casos MMC y días de baja por MMC |
| 4 | Orden y limpieza | Implementar verificaciones periódicas de orden, tránsito y condiciones de superficies, priorizando eventos con afectación de tobillo. | Preventiva | Supervisión operativa | 30 días | Casos vinculados a orden y limpieza; casos con lesión de tobillo |
| 5 | Operación_006 | Revisar las tareas y condiciones presentes en la operación, desagregando los eventos por categoría disponible. | Diagnóstico focalizado | Responsable de Operación_006 y Seguridad e Higiene | 30 días | Casos y días de baja de Operación_006 |
| 6 | Operación_001 | Investigar los eventos de mayor duración y validar si hay patrones operativos comunes. | Investigación y correctiva | Responsable de Operación_001 y Seguridad e Higiene | 30 días | Días de baja promedio y total de la operación |

### E. CONCLUSIONES Y SUPERVISIÓN HUMANA

1. **Dato observado:** Se registraron 60 casos, 1.522 días de baja y 976 días ILT entre enero y julio de 2026.

2. **Dato observado:** Operación_006 concentró la mayor cantidad de casos y días de baja. Operación_001 presentó un promedio de días de baja superior al promedio general.

3. **Interpretación:** Los eventos clasificados como falta de uso de tres puntos de apoyo, MMC y orden y limpieza reúnen alta frecuencia y/o impacto, por lo que justifican revisión prioritaria.

4. **Interpretación:** Las fracturas cerradas fueron poco frecuentes, pero concentraron una proporción relevante de los días de baja, por lo que no deben quedar relegadas frente a focos de mayor cantidad de casos.

5. **Recomendación:** Validar mediante investigación humana las categorías de causa raíz, los eventos de mayor impacto y cualquier posible reincidencia antes de definir controles específicos.

Las interpretaciones, prioridades y recomendaciones deben ser revisadas por el responsable de Seguridad e Higiene antes de utilizarse para tomar decisiones o implementar acciones.