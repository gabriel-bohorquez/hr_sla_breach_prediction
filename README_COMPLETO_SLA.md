# HR SLA Breach Prediction

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-FF4B4B?logo=streamlit)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-success)

# Predictive Risk Intelligence for HR Operations

*(Aquí colocaremos la imagen principal del proyecto.)*

This project develops a Machine Learning solution capable of predicting Service Level Agreement (SLA) breaches in HR Operations before they occur.

Rather than reacting to delayed cases, the solution helps operational teams identify high-risk tickets early, prioritize interventions and support preventive decision-making through predictive analytics.

The project follows an end-to-end analytics workflow, including data preparation, business rule engineering, model comparison, hyperparameter optimization, model interpretation and deployment through an interactive Streamlit application.

---

# Executive Summary

| Category | Detail |
|----------|---------|
| Portfolio Suite | HR Operations Intelligence Suite |
| Module | Predictive Risk Intelligence |
| Project Type | End-to-End Machine Learning |
| Business Domain | HR Operations |
| Business Problem | Predict SLA breaches before they occur |
| Target Variable | `incumplio_sla` |
| Machine Learning Task | Binary Classification |
| Final Model | Optimized Random Forest |
| Model Selection Strategy | Recall-oriented optimization |
| Recall (Class 1) | 80.19% |
| Deployment | Streamlit |
| Business Value | Preventive Operations · Risk Prioritization · Decision Support |


---


## Business Problem

HR Operations teams process thousands of operational requests every day, including onboarding, payroll, employee documentation, benefits administration and HR support cases.

Many of these requests are governed by Service Level Agreements (SLAs). Missing these deadlines can generate operational bottlenecks, unnecessary escalations, lower employee satisfaction and additional workload for HR teams.

The challenge is that operational teams often identify SLA risks too late, when the deadline is already close or has already been missed.

### Business Question

> **Can we identify high-risk HR tickets early enough to prioritize intervention before an SLA breach occurs?**

This project addresses that question using Machine Learning to estimate the probability of SLA breach before the operational deadline is reached.

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


