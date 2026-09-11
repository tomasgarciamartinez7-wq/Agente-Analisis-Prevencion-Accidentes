# Agente de Análisis y Prevención de Accidentes Laborales

## Qué construí

Desarrollé un sistema agéntico para analizar bases de accidentes laborales y apoyar la gestión preventiva de Seguridad e Higiene.

El agente recibe una base de accidentes en formato Excel, valida la información disponible, calcula indicadores, identifica patrones y focos de riesgo y genera recomendaciones preventivas y correctivas junto con un plan de acción priorizado.

El sistema está diseñado como herramienta de apoyo a la toma de decisiones. No reemplaza el criterio profesional del responsable de Seguridad e Higiene y no ejecuta automáticamente las recomendaciones generadas.

## Objetivo

Analizar una base de accidentes laborales para identificar patrones, focos de riesgo y eventos de mayor impacto, y generar recomendaciones preventivas y correctivas junto con un plan de acción priorizado para apoyar la toma de decisiones del área de Seguridad e Higiene, manteniendo la aprobación humana sobre las recomendaciones finales.

## Cómo funciona

El flujo general del sistema es:

1. El usuario proporciona una base de accidentes laborales en formato Excel.
2. El agente valida la estructura y calidad de los datos.
3. Calcula los indicadores que pueden obtenerse válidamente con la información disponible.
4. Identifica patrones y focos de riesgo.
5. Prioriza los principales riesgos según frecuencia e impacto.
6. Propone acciones preventivas, correctivas y de capacitación.
7. Genera un plan de acción con responsables, plazos e indicadores de seguimiento sugeridos.
8. La salida es revisada por el responsable humano antes de tomar decisiones o implementar acciones.

Cuando la información disponible no permite realizar un cálculo o sostener una conclusión, el agente debe indicarlo expresamente como “Datos insuficientes”.

## Contrato del agente

El contrato fue construido utilizando seis componentes:

- Rol.
- Contexto.
- Tarea.
- Restricciones.
- Formato de salida.
- Ejemplos.

Durante el desarrollo se utilizaron tres versiones del System Prompt.

### V1

Primera versión funcional del contrato.

El agente logró realizar el análisis, pero durante la primera corrida se detectó un problema de confidencialidad: identificó que la base contenía información que requería anonimización adicional y, aun así, reprodujo denominaciones reales de operaciones.

### V2

Se incorporó una validación previa de anonimización y una regla para no reproducir identificadores confidenciales.

La segunda corrida mostró una mejora parcial: los nombres de personas dejaron de reproducirse, pero todavía apareció la denominación real de una operación.

### V3 — versión final

Se incorporó una regla explícita para considerar confidenciales las denominaciones de empresas, unidades de negocio y operaciones y reemplazarlas por identificadores genéricos.

La tercera corrida confirmó el funcionamiento esperado: las operaciones fueron presentadas mediante identificadores como `Operacion_001` y `Operacion_006`, sin exponer las denominaciones originales ni generar tablas de equivalencia.

La historia completa de estas decisiones se encuentra documentada en `DECISIONES.md`.

## Corridas reales

Se realizaron tres corridas utilizando la misma base real de accidentes y el mismo User Prompt.

Mantener constante la entrada y modificar únicamente el contrato permitió observar con mayor claridad el efecto de cada iteración.

### Corrida 1 — V1

Resultado: análisis funcional, pero protección insuficiente de información confidencial.

### Corrida 2 — V2

Resultado: mejora en la protección de datos personales, pero anonimización incompleta de las denominaciones organizacionales.

### Corrida 3 — V3

Resultado: anonimización satisfactoria de personas y operaciones, manteniendo la capacidad analítica y la estructura de salida.

Las entradas y salidas originales se encuentran preservadas en la carpeta `corridas/`.

## Herramientas

El sistema utiliza como entrada una base de accidentes laborales en formato Excel.

El agente posee capacidad de lectura, validación, análisis y generación de recomendaciones.

No posee permisos para:

- modificar la base original;
- escribir en sistemas corporativos;
- enviar comunicaciones automáticamente;
- ejecutar acciones;
- aplicar sanciones;
- tomar decisiones médicas, legales o laborales.

## Supervisión humana

El sistema utiliza un esquema de autonomía limitada.

- L0: decisiones disciplinarias, médicas, legales o determinación de responsabilidades. Fuera del alcance.
- L1: lectura, validación, conteos e indicadores. Ejecución automática.
- L2: patrones, focos de riesgo y recomendaciones. El agente propone y una persona revisa.
- L3: plan de acción. Requiere aprobación humana antes de su implementación.
- L4: ejecución automática o modificación de sistemas. No habilitada.

El Responsable de Seguridad e Higiene debe validar las interpretaciones, prioridades y recomendaciones antes de utilizarlas para tomar decisiones.

El detalle se encuentra en `GOBERNANZA_Y_RIESGO.md`.

## Riesgos principales

Los principales modos de falla considerados son:

- exposición accidental de información confidencial;
- inferencia de causas no demostradas por los datos;
- comparaciones entre operaciones sin información de exposición;
- problemas de calidad de datos;
- recomendaciones que no sean aplicables al contexto operativo real.

El sistema fue diseñado para declarar sus limitaciones y mantener la decisión final bajo supervisión humana.

## Análisis económico

Las pruebas se realizaron con GPT-5.6 Terra utilizando razonamiento Ligero, que fue el modelo de menor costo disponible en la interfaz utilizada durante el desarrollo.

Como la interfaz no informa el consumo exacto de tokens por ejecución, se realizó una estimación transparente del consumo y del costo.

El costo teórico promedio estimado fue de aproximadamente USD 0,035 por corrida.

En un escenario de una ejecución semanal, el costo anual estimado es de aproximadamente USD 1,80.

Los cálculos, supuestos y metodología se encuentran documentados en `ANALISIS_ECONOMICO.md`.

## Qué funciona

- Lectura y análisis de una base de accidentes.
- Validación de estructura y calidad de datos.
- Cálculo de indicadores descriptivos.
- Identificación de patrones y focos de riesgo.
- Diferenciación entre frecuencia e impacto.
- Priorización de riesgos.
- Generación de recomendaciones preventivas y correctivas.
- Propuesta de acciones de capacitación.
- Generación de un plan de acción.
- Declaración de datos insuficientes.
- Separación entre datos observados, interpretaciones y recomendaciones.
- Anonimización de denominaciones organizacionales en la salida.
- Supervisión humana antes de implementar acciones.

## Qué falta o qué no hace

El sistema no calcula tasas que requieran denominadores no incluidos en la base, como horas trabajadas o dotación.

No determina automáticamente causas raíz cuando los datos no permiten demostrarlas.

No ejecuta las recomendaciones generadas.

No reemplaza una investigación profesional de Seguridad e Higiene.

No toma decisiones disciplinarias, médicas o legales.

## Qué aprendí

El principal aprendizaje del proyecto fue que un agente no mejora únicamente utilizando un modelo más potente.

Las primeras corridas demostraron que instrucciones generales como “no exponer información confidencial” pueden resultar insuficientes.

Fue necesario observar el comportamiento real del sistema, identificar el fallo y transformar una restricción general en reglas operativas concretas.

La evolución V1 → V2 → V3 permitió mejorar el comportamiento del agente manteniendo el mismo modelo y la misma entrada.

También resultó relevante definir explícitamente qué puede hacer el agente de manera autónoma, qué debe revisar una persona y qué decisiones deben permanecer completamente fuera de su alcance.

## Estructura del repositorio

```text
.
├── README.md
├── DECISIONES.md
├── ANALISIS_ECONOMICO.md
├── GOBERNANZA_Y_RIESGO.md
├── prompts/
│   ├── system_prompt.md
│   ├── system_prompt_V1.md
│   ├── system_prompt_V2.md
│   ├── system_prompt_V3.md
│   └── user_prompt.md
└── corridas/
    ├── corrida_1/
    │   ├── entrada.md
    │   └── salida.md
    ├── corrida_2/
    │   ├── entrada.md
    │   └── salida.md
    └── corrida_3/
        ├── entrada.md
        └── salida.md
Confidencialidad y datos
Las corridas se realizaron con datos reales de trabajo.
La base original utilizada para las pruebas no se publica en este repositorio porque contiene información confidencial.
Las salidas permitieron detectar este riesgo durante el propio desarrollo del agente y dieron origen a las iteraciones V2 y V3.
La versión final del contrato establece reglas explícitas de anonimización para impedir que nombres de personas, empresas u operaciones sean expuestos en las salidas.
Autor
Tomás García Martínez
MBA UCEMA
Programación de y con Agentes de IA
2026