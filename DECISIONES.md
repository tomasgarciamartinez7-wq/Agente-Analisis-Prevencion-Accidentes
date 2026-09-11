# DECISIONES — Agente de Análisis y Prevención de Accidentes Laborales

## Objetivo del documento

Este documento registra las principales decisiones tomadas durante el desarrollo y prueba del agente, incluyendo los problemas detectados en las corridas reales, las modificaciones realizadas sobre el contrato y los resultados obtenidos después de cada iteración.

El criterio utilizado fue modificar una parte del contrato por vez, manteniendo la misma base de datos y el mismo User Prompt, para poder observar con mayor claridad el efecto de cada cambio.

---

## Versión inicial — V1

### Objetivo

Construir un agente capaz de analizar una base de accidentes laborales, validar los datos disponibles, calcular indicadores, identificar focos de riesgo y generar recomendaciones y un plan de acción para revisión del área de Seguridad e Higiene.

### Resultado de la Corrida 1

La primera corrida logró realizar el análisis solicitado y respetó la estructura definida en el contrato.

Entre otros resultados, calculó cantidad de accidentes, días de baja y días ILT, identificó focos de riesgo y generó recomendaciones y un plan de acción.

También respetó una restricción importante: ante la ausencia de horas trabajadas o dotación, indicó que existían “Datos insuficientes” para calcular tasas comparables.

### Problema detectado

La propia salida informó que la base contenía campos personales y que requería anonimización adicional. Sin embargo, el agente continuó procesando la información y reprodujo denominaciones reales de operaciones en los resultados.

Por lo tanto, la restricción general de no exponer información confidencial resultó insuficiente.

---

## Iteración 1 — V1 a V2

### Pieza modificada

RESTRICCIONES.

### Cambio realizado

Se incorporó una validación previa de anonimización. Se indicó al agente que verificara la existencia de nombres de personas, documentos, nombres reales de empresas u operaciones u otros identificadores confidenciales antes de iniciar el análisis.

También se estableció que esa información no debía reproducirse y que, si no era posible realizar un procesamiento seguro, debía solicitarse revisión humana antes de continuar.

### Motivo del cambio

Evitar que el agente continuara exponiendo información confidencial después de haber detectado que la base no se encontraba suficientemente anonimizada.

### Resultado de la Corrida 2

La modificación produjo una mejora parcial.

El agente detectó que existían nombres y apellidos en la base e indicó expresamente que no serían reproducidos. Sin embargo, continuó mostrando la denominación real de una operación.

La iteración permitió comprobar que la protección de datos personales había mejorado, pero que la instrucción todavía era ambigua respecto de las denominaciones organizacionales.

---

## Iteración 2 — V2 a V3

### Pieza modificada

RESTRICCIONES.

### Cambio realizado

Se estableció expresamente que toda denominación de empresa, unidad de negocio u operación debía considerarse confidencial, salvo indicación contraria del usuario.

Además, se instruyó al agente a reemplazar esas denominaciones por identificadores genéricos consecutivos, por ejemplo `Empresa_001` u `Operacion_001`, sin reproducir el valor original ni generar una tabla de equivalencias.

### Motivo del cambio

La Corrida 2 demostró que la instrucción anterior protegía los datos personales, pero no garantizaba la anonimización de las denominaciones organizacionales.

### Resultado de la Corrida 3

La modificación funcionó según lo esperado.

El agente no reprodujo nombres de personas ni denominaciones reales de las operaciones. Las operaciones fueron presentadas mediante identificadores genéricos, como `Operación_006` y `Operación_001`, sin incluir información que permitiera vincular esos identificadores con sus denominaciones originales.

Al mismo tiempo, el agente mantuvo la capacidad de calcular indicadores, identificar focos de riesgo, generar un plan de acción y señalar las limitaciones de los datos.

---

## Decisión final

Se adopta V3 como versión final del contrato del agente.

Las tres corridas muestran una evolución verificable:

**V1:** análisis funcional, pero protección insuficiente de información confidencial.

**V2:** mejora en la protección de datos personales, pero anonimización incompleta de operaciones.

**V3:** anonimización de personas y denominaciones organizacionales manteniendo la utilidad analítica del sistema.

La experiencia mostró que una instrucción general de confidencialidad no era suficiente. Fue necesario convertirla en reglas operativas concretas que definieran qué información debía considerarse confidencial y qué debía hacer exactamente el agente antes de mostrarla.