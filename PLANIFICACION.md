# Planificación del proyecto: Open edX Analytics

**Grupo de investigación:** Sistemas Basados en el Conocimiento (KBS) · UTPL
**Horizonte:** semanas 1 a 14 (19 de octubre de 2026 al 7 de febrero de 2027)

## 1. Equipo

| Integrante | Rol |
|---|---|
| Pablo Ordóñez | Líder del proyecto |
| Eduardo Peñarreta | Desarrollador |
| Michael Carrión | Desarrollador |
| Emilio Poma | Desarrollador |

## 2. Resumen

Plataforma de analítica educativa que procesa, caracteriza y visualiza patrones temporales de interacción registrados en cursos Open edX. Se trabaja solo con datos sintéticos o autorizados y seudonimizados. Los indicadores de actividad **no se interpretan automáticamente como aprendizaje o rendimiento**.

## 3. Alcance de la primera versión

| Componente | Entregable |
|---|---|
| Ingesta | Lectura de eventos JSON/JSONL con validación de campos y marcas temporales |
| Preparación | Normalización de eventos y dataset analítico documentado |
| Indicadores | Conteos de eventos, frecuencia de interacción y actividad por curso/período |
| Análisis | Tendencias temporales y diferencias entre categorías de eventos |
| Visualización | Tablero interactivo con filtros y reportes agregados exportables |

## 4. Tecnologías

Python, Pandas o Polars, PostgreSQL, SciPy, Plotly, Streamlit y GitHub.

## 5. Cronograma por semanas

| Semana | Fechas | Actividades | Entregable |
|---|---|---|---|
| 1 ✅ | 19 oct – 8 nov | Creación del repositorio (19 oct), recepción de la información del proyecto (29 oct), lectura de la propuesta y organización del equipo. Incluye feriados del 2 y 3 de noviembre | Repositorio inicial y README |
| 2 | 9 – 15 nov | Revisión de la estructura de eventos de Open edX; definición del esquema de datos de entrada | Documento del esquema de eventos |
| 3 | 16 – 22 nov | Generación de datos sintéticos (JSON/JSONL); definición del método de seudonimización | Dataset sintético de ejemplo |
| 4 | 23 – 29 nov | Módulo de ingesta: lectura de archivos y validación de campos y marcas temporales | Módulo de ingesta con pruebas |
| 5 | 30 nov – 6 dic | Diseño de base de datos en PostgreSQL; normalización de eventos | Modelo de datos y script de carga |
| 6 | 7 – 13 dic | Construcción del dataset analítico y su documentación (diccionario de datos) | Dataset analítico documentado |
| 7 | 14 – 20 dic | Definición del catálogo de indicadores (qué miden y qué **no** significan) e inicio de su implementación | Catálogo de indicadores v1 |
| 8 | 21 – 27 dic | Implementación de indicadores: conteos, frecuencia y actividad por curso/período. Semana de Navidad: carga liviana | Módulo de indicadores con pruebas |
| 9 | 28 dic – 3 ene | Análisis de tendencias temporales y diferencias entre categorías de eventos (SciPy). Semana de Año Nuevo: carga liviana | Notebook de análisis exploratorio |
| 10 | 4 – 10 ene | Prototipo del tablero en Streamlit: carga de archivo, selección de curso y período | Tablero base funcional |
| 11 | 11 – 17 ene | Visualizaciones con Plotly, filtros interactivos y exportación de reportes agregados | Tablero completo con reportes |
| 12 | 18 – 24 ene | Pruebas de integración, validación con datos sintéticos, corrección de errores | Versión candidata (release v0.9) |
| 13 | 25 – 31 ene | Informe exploratorio y de limitaciones; documentación y reproducibilidad del repositorio | Informe y README final |
| 14 | 1 – 7 feb | Revisión final, preparación de la presentación y entrega | Entrega final (release v1.0) |

## 6. Hitos

| Hito | Semana | Criterio de cumplimiento |
|---|---|---|
| H1: Base del proyecto | 3 | Repositorio, esquema de eventos y datos sintéticos listos |
| H2: Pipeline de datos | 6 | Ingesta, normalización y dataset analítico funcionando |
| H3: Indicadores y análisis | 9 | Catálogo de indicadores implementado y análisis exploratorio realizado |
| H4: Tablero | 11 | Tablero interactivo con filtros y reportes exportables |
| H5: Entrega | 14 | Informe, repositorio reproducible y presentación finales |

## 7. Productos esperados

- Procesador de eventos y dataset analítico documentado.
- Catálogo de indicadores con definiciones.
- Tablero interactivo y reportes agregados.
- Informe exploratorio, limitaciones y repositorio reproducible.

## 8. Distribución de responsabilidades

| Área | Responsable | Apoyo |
|---|---|---|
| Coordinación, seguimiento y tablero | Pablo Ordóñez | Emilio Poma |
| Datos sintéticos, ingesta y validación | Eduardo Peñarreta | Michael Carrión |
| Base de datos y dataset analítico | Michael Carrión | Eduardo Peñarreta |
| Indicadores y análisis | Emilio Poma | Michael Carrión |
| Documentación e informe | Todo el equipo | Pablo Ordóñez consolida |

## 9. Riesgos y mitigación

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| No disponer de datos reales autorizados | Alta | Medio | Trabajar con datos sintéticos desde la semana 3 |
| Estructura de eventos más compleja de lo previsto | Media | Alto | Empezar por un subconjunto de tipos de evento y ampliar |
| Interpretar actividad como aprendizaje | Media | Alto | Incluir en el catálogo y el tablero qué no significa cada indicador |
| Menor disponibilidad en feriados (semanas 8 y 9) | Alta | Medio | Adelantar trabajo en las semanas 6 y 7 y dejar tareas livianas e individuales en esas semanas |
| Retraso en el tablero | Media | Medio | Prototipo temprano en la semana 10 y priorizar filtros esenciales |
| Falta de reproducibilidad | Baja | Alto | Fijar dependencias y documentar la instalación desde la semana 1 |

## 10. Metodología de trabajo

- Control de versiones con GitHub: rama `main` protegida y ramas por funcionalidad.
- Revisión de código mediante *pull requests* (mínimo una aprobación).
- Reunión de seguimiento semanal `[día y hora]`.
- Tablero de tareas en GitHub Projects.

## 11. Consideraciones éticas

- Solo se usan datos sintéticos o autorizados y seudonimizados.
- No se incluyen datos reales en el repositorio.
- No se realizan inferencias individuales sobre aprendizaje, abandono o rendimiento.
