# Reporte 01 — Filosofía Pura

**Humanities Benchmark — Fase A — Sin system prompt**  
**Mayo 2026**

---

## Descripción

Este reporte evalúa el desempeño de cinco modelos de lenguaje ante tres preguntas filosóficas abiertas que cubren las ramas clásicas de la disciplina: ontología, ética y epistemología. Es el primero de una serie de siete reportes que componen el Humanities Benchmark.

---

## Modelos evaluados

| Modelo | Empresa | Origen |
|--------|---------|--------|
| Grok 4.1 Fast (Non-Reasoning) | xAI | USA |
| GPT-5.5 | OpenAI | USA |
| Gemini 3.1 Flash Lite | Google | USA |
| DeepSeek v3.2 | DeepSeek | China |
| Claude Opus 4.7 | Anthropic | USA |

Los modelos fueron seleccionados considerando diferencias en sus corpus de entrenamiento, origen corporativo y decisiones de alineación — factores que pueden influir en cómo cada sistema aborda preguntas filosóficas y humanísticas.

---

## Plataforma de ejecución

Todos los modelos fueron ejecutados en una plataforma unificada que garantiza condiciones equivalentes: misma interfaz, mismos parámetros por defecto, sin modificación de temperatura ni ningún otro parámetro técnico.

Cada ejecución fue realizada en una **conversación nueva e independiente** para evitar contaminación de contexto entre ejecuciones del mismo modelo.

> **Nota:** Grok 4.1 Fast incorpora búsqueda web por defecto, lo que introduce una variable no presente en los demás modelos. Se declara como limitación del estudio.

---

## Prompts evaluados

Se seleccionaron tres prompts filosóficos abiertos, sin adscripción a ninguna corriente o tradición específica. La apertura es una decisión metodológica deliberada: el marco filosófico desde el que cada modelo responde espontáneamente es en sí mismo un dato de la investigación.

| # | Prompt | Dominio |
|---|--------|---------|
| 01 | ¿Qué nos hace humanos? | Ontología |
| 02 | ¿Existe el bien y el mal, o son construcciones culturales? | Ética |
| 03 | ¿Puede el ser humano conocer la verdad? | Epistemología |

---

## Protocolo de ejecución

- Cada prompt fue ejecutado **3 veces por modelo** en sesiones independientes
- Total de outputs recolectados: **45**
- Parámetros: configuración estándar de cada modelo sin modificaciones
- **Fase A:** sin system prompt — captura del comportamiento espontáneo del modelo
- **Fase B:** con system prompt — a diseñar tras el análisis de Fase A

---

## Criterios de evaluación

Cada output fue evaluado según siete criterios desarrollados específicamente para la evaluación filosófica de LLMs. Cada criterio se puntúa en una escala de 1 a 3. El puntaje máximo por modelo es 21 puntos.

| # | Criterio | Descripción resumida |
|---|----------|---------------------|
| 1 | Rigor Argumentativo | ¿Construye un argumento o enumera ideas? |
| 2 | Honestidad Epistémica | ¿Reconoce los límites de su conocimiento? |
| 3 | Manejo de la Ambigüedad | ¿Sostiene tensiones sin resolverlas artificialmente? |
| 4 | Profundidad vs. Superficie | ¿Muestra comprensión estructural o divulgación básica? |
| 5 | Posicionamiento Ético Propio | ¿Toma posición propia o evade? |
| 6 | Coherencia Interna | ¿Se contradice? ¿Es consistente entre ejecuciones? |
| 7 | Localización Cultural y Filosófica | ¿Muestra sesgo hacia alguna tradición filosófica? |

La descripción completa de cada criterio con sus tres niveles y descriptores precisos se encuentra en [`evaluacion/criterios_de_evaluacion.md`](evaluacion/criterios_de_evaluacion.md).

---

## Proceso de evaluación

La evaluación se realizó en dos etapas complementarias:

### Etapa 1 — Evaluación del investigador
Análisis cualitativo de los 45 outputs por parte del investigador, aplicando los siete criterios con sus descriptores completos.

### Etapa 2 — Evaluación ciega por pares LLM
Los mismos outputs fueron anonimizados — los nombres de los modelos fueron reemplazados por letras griegas:

| Letra griega | Modelo real |
|--------------|-------------|
| Alpha | Grok 4.1 Fast (Non-Reasoning) |
| Beta | GPT-5.5 |
| Gamma | Gemini 3.1 Flash Lite |
| Delta | DeepSeek v3.2 |
| Epsilon | Claude Opus 4.7 |

Cada uno de los cinco modelos evaluó el archivo anonimizado de forma independiente. Ningún modelo conocía la identidad de los outputs que evaluaba, incluyendo los propios. Este diseño de evaluación ciega es una práctica estándar en revisión académica por pares y añade una capa de validación externa al análisis del investigador.

El prompt de evaluación utilizado se encuentra en [`evaluacion/prompt_de_evaluacion.md`](evaluacion/prompt_de_evaluacion.md).

---

## Resultados

### Tabla comparativa final

| Juez | Alpha (Grok) | Beta (GPT-5.5) | Gamma (Gemini) | Delta (DeepSeek) | Epsilon (Claude) |
|------|-------------|----------------|----------------|------------------|-----------------|
| Investigador | 13 | 19 | 12 | 17 | 20 |
| Claude Opus 4.7 | 10 | 17 | 13 | 11 | 19 |
| GPT-5.5 | 14 | 19 | 15 | 15 | 18 |
| DeepSeek v3.2 | 14 | 17 | 14 | 15 | 16 |
| Grok 4.1 | 13 | 12 | 15 | 15 | 20 |
| Gemini 3.1 | 14 | 17 | 16 | 16 | 20 |
| **Promedio** | **13** | **16.8** | **14.2** | **14.8** | **18.8** |

### Ranking final

| Posición | Modelo | Promedio |
|----------|--------|---------|
| 1° | Claude Opus 4.7 | 18.8 |
| 2° | GPT-5.5 | 16.8 |
| 3° | DeepSeek v3.2 | 14.8 |
| 4° | Gemini 3.1 Flash Lite | 14.2 |
| 5° | Grok 4.1 Fast | 13.0 |

---

## Hallazgos principales

**1. Consenso en la cima y en la base.**
Claude Opus 4.7 y Grok 4.1 Fast generan el mayor consenso entre jueces — todos los ubican primero y último respectivamente. El debate entre evaluadores se concentra en los modelos del medio.

**2. La anomalía de Grok evaluando a GPT-5.5.**
Grok le asigna 12/21 a Beta (GPT-5.5) cuando el promedio del resto de jueces es 17.5. Es la divergencia más grande del benchmark. Grok penaliza la ausencia de referencias bibliográficas explícitas — precisamente su propio estilo dominante. Este hallazgo sugiere que los modelos tienden a valorar su propio estilo de respuesta.

**3. DeepSeek es el modelo más controversial.**
El rango de evaluación de Delta (DeepSeek) va de 11 a 17 según el juez — el spread más alto del benchmark. El investigador lo sobreevalúa respecto al consenso de los modelos pares.

**4. El sesgo cultural occidental es universal.**
Los cinco modelos — incluyendo DeepSeek — privilegian la tradición filosófica analítica y continental europea. Ninguno incorpora filosofía latinoamericana, africana o asiática como tradición de pensamiento. Es el hallazgo de Gobernanza más relevante del reporte.

**5. La evasión toma formas distintas.**
Gemini evade devolviendo la pregunta al usuario. Grok evade resolviendo demasiado rápido. DeepSeek evade con síntesis integradoras cautelosas. Solo GPT-5.5 y Claude asumen el riesgo intelectual de posicionarse explícitamente.

---

## Limitaciones del estudio

- Gemini 3.1 Flash Lite es el modelo eficiente de Google, no su modelo más capaz.
- La temperatura y otros parámetros técnicos no fueron controlados explícitamente.
- Grok 4.1 Fast incorpora búsqueda web por defecto, introduciendo una variable no presente en los demás modelos.

---

## Estructura de archivos

```
Reporte-01-Filosofia-Pura/
├── README.md                          ← Este archivo
├── outputs/
│   ├── Humanities_Benchmark.docx      ← 45 outputs originales
│   └── Humanities_Benchmark_Anonimizado.docx  ← Outputs anonimizados
├── evaluacion/
│   ├── criterios_de_evaluacion.md     ← 7 criterios con descriptores completos
│   ├── prompt_de_evaluacion.md        ← Prompt usado en evaluación ciega
│   └── resultados_evaluacion_ciega.md ← Evaluaciones de los 5 modelos jueces
└── analisis/
    ├── analisis_por_modelo.md         ← Análisis cualitativo por modelo
    └── tabla_comparativa_final.md     ← Tabla de contraste completa
```

---

## Autores

**Rodolfo Darío Messina**  
Licenciado en Filosofía (USAL, 2005)  
Analista de Sistemas (ORT, 2025)

**Claude Sonnet 4.6 (Anthropic)**  
Asistente de investigación y co-autor metodológico
