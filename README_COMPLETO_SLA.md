# HR SLA Breach Prediction

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-FF4B4B?logo=streamlit)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-success)

> Part of the **HR Operations Intelligence Suite** — a portfolio of end-to-end analytics solutions designed to optimize, predict and support decision-making across HR Operations.

# Predictive Risk Intelligence for HR Operations

![HR SLA Breach Prediction Dashboard](images/dashboard.png)

This project develops an end-to-end Machine Learning solution that predicts Service Level Agreement (SLA) breaches before they occur, enabling HR Operations teams to proactively identify high-risk operational cases.

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


# Business Problem

## Business Context

HR Operations teams process thousands of operational requests every day, including onboarding, payroll, employee data updates, internal access requests and benefits administration. Most of these processes are governed by Service Level Agreements (SLAs) that define the maximum acceptable resolution time for each ticket.

Maintaining SLA compliance is essential to ensure operational efficiency, service quality and employee satisfaction.

---

## Operational Challenge

In high-volume environments, supervisors usually identify potential SLA breaches only after operational delays have already occurred.

This reactive approach often leads to:

- SLA violations and missed service commitments.
- Escalations from employees and internal stakeholders.
- Increased operational pressure on HR teams.
- Reduced employee experience.
- Lower confidence in HR service delivery.
- Additional effort to recover delayed cases.

The main challenge is not detecting delayed tickets, but identifying **which active cases are most likely to become delayed before the SLA is breached.**

---

## Business Question

> **Can we proactively identify high-risk operational tickets before they violate their SLA?**

Answering this question would allow HR Operations teams to prioritize resources based on risk instead of reacting after service failures occur.

---

## Why Machine Learning?

Historical operational data contains patterns that traditional rule-based monitoring cannot easily capture.

Machine Learning makes it possible to:

- learn historical risk patterns;
- estimate the probability of SLA breaches for new tickets;
- prioritize interventions using predictive evidence;
- support operational decisions with consistent and scalable risk assessment.

Rather than replacing human judgment, the model acts as an early warning system that helps teams focus attention where it is needed most.

---

## Expected Business Impact

If deployed in a real HR Operations environment, the solution could contribute to:

- Earlier identification of high-risk tickets.
- Better prioritization of operational workload.
- Reduction of preventable SLA breaches.
- More efficient allocation of HR resources.
- Improved employee service quality.
- Data-driven operational decision-making.

---

# Project Objective

The objective of this project is to develop an explainable Machine Learning solution capable of identifying HR operational tickets with the highest probability of violating their Service Level Agreement (SLA).

Rather than predicting delays as an isolated technical exercise, the model is designed to support operational prioritization by enabling earlier interventions on high-risk cases.

The final objective is to transform historical operational data into actionable decision support for HR Operations teams.

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


