# HR SLA Breach Prediction

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-FF4B4B?logo=streamlit)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-success)

# Predictive Risk Intelligence for HR Operations












This project predicts HR operational ticket SLA breaches before they occur, enabling HR Operations teams to proactively identify high-risk cases and prioritize intervention.

Instead of reacting to missed SLAs, the solution combines business understanding, feature engineering and Machine Learning to support preventive operational decision-making.

---

# Executive Summary

| Category | Detail |
|----------|---------|
| Project Type | End-to-End Machine Learning |
| Industry | HR Operations / People Analytics |
| Business Problem | Predict SLA breaches before they occur |
| Dataset | 100,000+ operational tickets |
| Machine Learning Task | Binary Classification |
| Final Model | Random Forest (Optimized) |
| Target Metric | Recall (High-risk SLA Breaches) |
| Recall | ~80% |
| Business Objective | Prevent SLA violations through early intervention |
| Dashboard | Streamlit |
| Business Value | Risk Prediction · Operational Prioritization · Decision Support |


---

## 2. Problema de negocio

Los equipos de HR Operations gestionan un alto volumen de casos relacionados con procesos como onboarding, documentación, payroll, beneficios, cambios de datos, accesos internos y consultas de empleados.

Muchos de estos casos están sujetos a SLA, es decir, tiempos máximos esperados de resolución.

Cuando un caso incumple su SLA, puede generar:

- retrasos operativos,
- escalaciones,
- pérdida de confianza en el servicio,
- presión adicional sobre el equipo,
- peor experiencia del empleado,
- incumplimiento de KPIs internos.

El problema principal es que muchas veces los equipos detectan el riesgo demasiado tarde.

Por eso, la pregunta de negocio del proyecto es:

> ¿Podemos anticipar qué tickets tienen mayor probabilidad de incumplir su SLA antes de que ocurra?

---

## 3. Objetivo del proyecto

Construir un modelo predictivo capaz de clasificar tickets según su riesgo de incumplimiento SLA.

La variable objetivo del proyecto es:

| Variable | Valor | Significado |
|---|---:|---|
| `incumplio_sla` | 0 | El ticket cumplió el SLA |
| `incumplio_sla` | 1 | El ticket incumplió el SLA |

El objetivo operativo es pasar de una gestión reactiva a una gestión preventiva basada en riesgo.

---

## 4. Enfoque analítico

El proyecto sigue un flujo de trabajo orientado a negocio:

```text
Problema de negocio
↓
Entendimiento de datos
↓
Creación de variable objetivo
↓
Preparación del dataset final
↓
Entrenamiento de modelos
↓
Comparación de modelos
↓
Optimización
↓
Interpretación
↓
Recomendaciones de negocio


## Aplicación Streamlit

El proyecto incluye una aplicación interactiva desarrollada con Streamlit.

La app permite:

- Explorar el dataset final.
- Consultar KPIs operativos.
- Filtrar tickets por prioridad, canal y tipo.
- Visualizar patrones de incumplimiento SLA.
- Revisar métricas del modelo final.
- Simular la predicción de riesgo de incumplimiento SLA para un nuevo ticket.
- Obtener una recomendación operativa automática.
- Consultar conclusiones, limitaciones y próximos pasos.

### Ejecutar localmente

Desde la raíz del proyecto:

```bash
streamlit run app/app.py

La aplicación se abrirá en:

http://localhost:8501

Enlace publico: https://canva.link/mgiyjhi7zm3opox


