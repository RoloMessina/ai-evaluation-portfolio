# Humanities Benchmark

**Serie de evaluación filosófica y humanística de modelos de lenguaje de gran escala (LLMs)**

---

## Sobre el proyecto

El Humanities Benchmark es una serie de reportes que evalúa el desempeño de modelos de lenguaje ante preguntas de las disciplinas humanísticas. A diferencia de los benchmarks técnicos dominantes en el campo — que miden capacidades en código, matemática y razonamiento lógico formal — este proyecto evalúa comprensión filosófica, rigor argumentativo y honestidad epistémica.

El diferencial metodológico es la formación del evaluador: el proyecto está conducido desde una perspectiva de Humanidades y Filosofía, lo que permite distinguir entre respuestas filosóficamente sólidas y respuestas que simulan solidez a través de la acumulación enciclopédica.

---

## Modelos evaluados

Cinco modelos fueron seleccionados con criterio de diversidad de corpus. Los modelos fueron seleccionados considerando diferencias en sus corpus de entrenamiento, origen corporativo y decisiones de alineación — factores que pueden influir en cómo cada sistema aborda preguntas filosóficas y humanísticas.

| Modelo | Empresa | Origen |
|--------|---------|--------|
| Grok 4.1 Fast (Non-Reasoning) | xAI | USA |
| GPT-5.5 | OpenAI | USA |
| Gemini 3.1 Flash Lite | Google | USA |
| DeepSeek v3.2 | DeepSeek | China |
| Claude Opus 4.7 | Anthropic | USA |

---

## Estructura de la serie

La serie está compuesta por siete reportes que cubren las principales disciplinas humanísticas:

| Reporte | Disciplina | Estado |
|---------|-----------|--------|
| 01 | Filosofía Pura | ✅ Completado |
| 02 | Historia e Interpretación | 🔜 Pendiente |
| 03 | Literatura y Lenguaje | 🔜 Pendiente |
| 04 | Arte y Estética | 🔜 Pendiente |
| 05 | Ética Aplicada y Gobernanza AI | 🔜 Pendiente |
| 06 | Antropología y Cultura | 🔜 Pendiente |
| 07 | Síntesis: ¿Qué modelo comprende mejor lo humano? | 🔜 Pendiente |

> El Reporte 05 incorporará como caso 5a un piloto ya publicado sobre salud mental y modelos de lenguaje.

---

## Metodología general

### Prompts
Cada reporte utiliza tres prompts abiertos, sin adscripción a ninguna corriente o tradición específica. La apertura es una decisión metodológica deliberada: el marco filosófico desde el que cada modelo responde espontáneamente es en sí mismo un dato de la investigación.

### Protocolo de ejecución
- Cada prompt es ejecutado **3 veces por modelo** en sesiones independientes
- Plataforma unificada: **Outlier Playground**
- Parámetros: configuración estándar sin modificaciones
- **Fase A:** sin system prompt — captura del comportamiento espontáneo
- **Fase B:** con system prompt — a diseñar tras el análisis de Fase A

### Criterios de evaluación
Siete criterios desarrollados específicamente para la evaluación filosófica de LLMs:

1. Rigor Argumentativo
2. Honestidad Epistémica
3. Manejo de la Ambigüedad
4. Profundidad vs. Superficie
5. Posicionamiento Ético Propio
6. Coherencia Interna
7. Localización Cultural y Filosófica

### Proceso de evaluación
La evaluación se realiza en dos etapas complementarias:

- **Etapa 1 — Evaluación del investigador:** análisis cualitativo aplicando los siete criterios
- **Etapa 2 — Evaluación ciega por pares LLM:** los outputs son anonimizados con letras griegas (Alpha, Beta, Gamma, Delta, Epsilon) y entregados a cada modelo para evaluación independiente

---

## Estructura del repositorio

```
Humanities-Benchmark/
│
├── README.md                          ← Este archivo
│
└── Reporte-01-Filosofia-Pura/
    ├── README.md                      ← Nota metodológica del reporte
    ├── outputs/
    │   ├── Humanities_Benchmark.docx
    │   └── Humanities_Benchmark_Anonimizado.docx
    ├── evaluacion/
    │   ├── criterios_de_evaluacion.md
    │   ├── prompt_de_evaluacion.md
    │   └── resultados_evaluacion_ciega.md
    └── analisis/
        ├── analisis_por_modelo.md
        └── tabla_comparativa_final.md
```

---

## Autores

**Rodolfo Darío Messina**  
Licenciado en Filosofía (USAL, 2005)  
Analista de Sistemas (ORT, 2025)

**Claude Sonnet 4.6 (Anthropic)**  
Asistente de investigación y co-autor metodológico

Serie iniciada en mayo de 2026.
