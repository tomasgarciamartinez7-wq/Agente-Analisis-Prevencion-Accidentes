# ANÁLISIS ECONÓMICO — Agente de Análisis y Prevención de Accidentes Laborales

## 1. Modelo utilizado

Las tres corridas fueron realizadas utilizando GPT-5.6 Terra con nivel de razonamiento Ligero.

Se seleccionó este modelo por ser la alternativa de menor costo disponible en la interfaz utilizada durante el desarrollo y las pruebas del agente.

Las tres ejecuciones demostraron que su capacidad fue suficiente para procesar la base, calcular indicadores, identificar focos de riesgo y generar recomendaciones y planes de acción estructurados.

Los problemas encontrados durante las primeras corridas estuvieron relacionados con la especificidad de las instrucciones de confidencialidad y pudieron corregirse mediante iteraciones del contrato, sin necesidad de utilizar un modelo de mayor capacidad y costo.

## 2. Metodología de estimación

La interfaz utilizada para realizar las pruebas no informa el consumo exacto de tokens correspondiente a cada ejecución.

Por ese motivo, los valores presentados son estimaciones realizadas a partir del volumen del System Prompt, User Prompt, información procesada y extensión de las salidas.

Los costos se calcularon utilizando como referencia las tarifas API oficiales de GPT-5.6 Terra vigentes al momento de elaborar el trabajo.

Por lo tanto, los valores deben interpretarse como una estimación económica y no como la facturación efectiva de las ejecuciones realizadas en ChatGPT/Codex.

## 3. Estimación por corrida

| Corrida | Tokens de entrada estimados | Tokens de salida estimados | Costo entrada | Costo salida | Costo total estimado |
|---|---:|---:|---:|---:|---:|
| Corrida 1 — V1 | 7.800 | 1.350 | USD 0,0156 | USD 0,0162 | USD 0,0318 |
| Corrida 2 — V2 | 8.000 | 1.550 | USD 0,0160 | USD 0,0186 | USD 0,0346 |
| Corrida 3 — V3 | 8.300 | 1.750 | USD 0,0166 | USD 0,0210 | USD 0,0376 |
| Promedio | 8.033 | 1.550 | USD 0,0161 | USD 0,0186 | USD 0,0347 |

Tarifas utilizadas como referencia:

- Entrada: USD 2 por millón de tokens.
- Salida: USD 12 por millón de tokens.

## 4. Proyección de utilización

Tomando como referencia un costo promedio estimado de USD 0,0347 por análisis:

### Escenario habitual — 1 análisis semanal

- Corridas por semana: 1
- Corridas por año: 52
- Costo semanal estimado: USD 0,035
- Costo anual estimado: USD 1,80

### Escenario intensivo — 5 análisis semanales

- Corridas por semana: 5
- Corridas por año: 260
- Costo semanal estimado: USD 0,17
- Costo anual estimado: USD 9,02

## 5. Evaluación económica

El costo variable estimado del procesamiento es bajo en relación con el objetivo del sistema.

El agente permite automatizar una primera etapa de validación, cálculo, identificación de patrones, priorización y elaboración de recomendaciones que de otra manera requeriría análisis manual.

La utilización del modelo de menor costo disponible en el entorno de prueba permite mantener un costo reducido sin comprometer la funcionalidad requerida.

## 6. Conclusión

GPT-5.6 Terra con razonamiento Ligero resultó suficiente para el alcance definido.

Las pruebas mostraron que mejorar la precisión del contrato permitió corregir los principales problemas encontrados sin recurrir a un modelo de mayor capacidad.

El costo promedio teórico estimado es de aproximadamente USD 0,035 por corrida, con un costo anual cercano a USD 1,80 para un escenario de una ejecución semanal.