# PROJECT_FACTS

## 1. Project Identity

**Project name:** HR SLA Breach Prediction  
**Project type:** End-to-end Machine Learning project  
**Domain:** HR Operations / People Analytics / Operations Analytics  
**Primary objective:** Anticipate the risk of SLA breaches in operational tickets and support proactive prioritization.  
**Final deliverables:** Machine Learning model, modular production code, Streamlit application, GitHub repository, README, documentation, and deployed demo.

---

## 2. Business Problem

HR Operations teams often react to SLA breaches after delays have already occurred.

The project aims to identify tickets with a higher probability of breaching their SLA before the breach happens, allowing operational teams to prioritize monitoring, follow-up, and preventive escalation.

---

## 3. Business User

**Primary users:**

- HR Operations teams
- Shared Services teams
- Team leads
- Operations managers
- Workforce and service delivery analysts

**Decision supported:**

Prioritize tickets according to estimated SLA breach risk.

---

## 4. Business Value

The project supports a transition from reactive ticket management to proactive operational prioritization.

Potential value includes:

- Earlier identification of high-risk tickets
- Better prioritization of operational workload
- Reduced risk of escalations
- Improved visibility of service performance
- Support for resource allocation and workload monitoring

The project does not demonstrate confirmed financial impact.

---

## 5. Dataset

**Source:** Customer support ticket dataset adapted for an HR Operations use case  
**Nature:** Adapted dataset; not real HR Operations production data  
**Primary raw file:** `data/raw/customer_support_tickets.csv`  
**Interim dataset:** `data/interim/tickets_hr_sla_interim.csv`  
**Processed dataset:** `data/processed/tickets_hr_sla_model_ready.csv`

The dataset contains ticket-related operational variables such as:

- Customer Age
- Product Purchased
- Ticket Type
- Ticket Subject
- Ticket Priority
- Ticket Channel

---

## 6. Target Variable

**Target name:** `incumplio_sla`

**Meaning:**

- `1`: the ticket is classified as an SLA breach
- `0`: the ticket is classified as SLA compliant

**Construction:**

The target was created using a business rule partially related to ticket priority.

**Critical methodological limitation:**

Ticket Priority is also used as a predictive feature. This creates a risk of circularity and target leakage because information used to construct the target is also available to the model as an input variable.

The project must therefore be presented as a methodological prototype rather than a production-ready prediction system.

---

## 7. Features

Main predictive variables used by the final model:

- Customer Age
- Product Purchased
- Ticket Type
- Ticket Subject
- Ticket Priority
- Ticket Channel

Categorical features were transformed before model training.

---

## 8. Data Preparation

The preparation workflow included:

- Data inspection
- Data cleaning
- Validation of missing values
- Validation of duplicates
- Category review
- Feature selection
- Categorical encoding
- Creation of the target variable
- Preparation of the final modeling dataset

---

## 9. Model Development

Models were compared using the same dataset split and evaluation framework.

The final selected model was:

**Optimized Random Forest Classifier**

Selection was based on the operational importance of detecting the highest possible number of SLA breaches while maintaining acceptable control of false alarms.

---

## 10. Final Model

**Model:** Optimized Random Forest Classifier  
**Production model file:** `models/modelo_random_forest_sla.pkl`

**Final model configuration:**

- `n_estimators = 200`
- `max_depth = 5`
- `class_weight = "balanced"`

The model was serialized using Joblib.

---

## 11. Final Metrics

Final validated metrics:

- **Accuracy:** 72.92%
- **Precision — SLA breach class:** 61.15%
- **Recall — SLA breach class:** 80.19%
- **F1-score — SLA breach class:** 69.39%

**Primary metric:** Recall for the SLA breach class

**Reason:**

A false negative is operationally more costly because it represents a ticket that is predicted as safe but later breaches its SLA.

---

## 12. Error Interpretation

### False Positive

A ticket predicted as an SLA breach that ultimately complies with the SLA.

**Operational consequence:**

Unnecessary monitoring or preventive follow-up.

### False Negative

A ticket predicted as SLA compliant that ultimately breaches the SLA.

**Operational consequence:**

The ticket may not receive timely prioritization or escalation.

False negatives are considered the more critical error.

---

## 13. Feature Importance

Ticket Priority appears as the dominant predictive variable.

This importance must not be interpreted as an independent operational discovery because the target was constructed using a rule partially related to priority.

This result reinforces the risk of methodological circularity.

---

## 14. Streamlit Application

**Application path:** `app/app.py`  
**Live demo:** https://hr-sla-breach-prediction.streamlit.app/

The application includes:

- Executive summary
- Dataset filters
- Exploratory analysis
- Model evaluation
- Final model metrics
- Feature importance
- SLA risk simulator
- Operational recommendations
- Methodological limitations
- Prioritized next steps

---

## 15. Risk Simulator

The simulator accepts ticket characteristics and returns:

- Binary prediction
- SLA breach probability
- Operational risk level
- Recommended operational action
- Interpretation of the result

The simulator is a decision-support prototype and must not be presented as an automated decision-making system.

---

## 16. Production Structure

Main production components:

- `app/app.py`
- `src/data_loader.py`
- `src/data_preprocessing.py`
- `src/evaluation.py`
- `src/feature_engineering.py`
- `src/metrics.py`
- `src/modeling.py`
- `src/prediction.py`
- `src/visualizations.py`
- `scripts/train_final_model.py`
- `models/modelo_random_forest_sla.pkl`
- `data/processed/tickets_hr_sla_model_ready.csv`

---

## 17. Reproducibility

The project includes:

- Relative file paths
- Modular production code
- Version-pinned dependencies
- Cross-platform virtual environment instructions
- Tested local installation
- Tested local execution
- Tested Streamlit deployment
- Repository cleanup
- GitHub hygiene
- MIT License

---

## 18. Technology Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Plotly
- Streamlit
- Joblib
- Jupyter Notebook
- Git
- GitHub

---

## 19. Methodological Limitations

Main limitations:

1. The dataset was adapted from customer support tickets and does not represent real HR Operations production data.
2. The target was created using a business rule rather than an independently observed SLA outcome.
3. Ticket Priority is used both in target construction and as a predictor.
4. The model has not been externally validated on new teams, regions, or time periods.
5. The project does not demonstrate causal relationships.
6. The project does not prove financial or operational impact.
7. The current model should not be used for automated employee or operational decisions.

---

## 20. Claims Allowed

The project may claim that:

- An end-to-end Machine Learning workflow was developed.
- Multiple classification models were compared.
- An optimized Random Forest was selected.
- The final model achieved 80.19% recall for the SLA breach class.
- A Streamlit application was developed and deployed.
- The project explicitly documents circularity and target leakage risk.
- The solution supports proactive prioritization as a prototype.

---

## 21. Claims Not Allowed

The project must not claim that:

- The model is production-ready.
- The model was trained on real HR Operations data.
- The model proves causal drivers of SLA breaches.
- The model reduces costs or SLA breaches in practice.
- The model can replace human operational judgment.
- The performance will generalize to other companies or teams.
- Ticket Priority is independently proven to cause SLA breaches.

---

## 22. Future Improvements

Priority improvements:

1. Use real HR Operations ticket data.
2. Create an SLA outcome label independent of ticket priority.
3. Add operational variables such as workload, queue size, assigned agent, reassignment count, region, team, and ticket age.
4. Use temporal or group-based validation.
5. Tune the decision threshold according to operational cost.
6. Add probability calibration.
7. Monitor drift and model performance.
8. Validate fairness and operational bias.
9. Integrate the model with a ticketing system through an API.
10. Add logging, versioning, and scheduled retraining.

---

## 23. Portfolio Positioning

**Recommended project title:**

HR SLA Breach Prediction | Machine Learning for HR Operations

**Professional positioning:**

An end-to-end Machine Learning project that combines operational analytics, predictive modeling, interpretability, Streamlit deployment, reproducibility, and transparent methodological risk documentation.

---

## 24. Final Status

- README reviewed and updated
- Streamlit application validated
- Local installation tested
- Cloud deployment tested
- Dependencies pinned
- Repository cleaned
- Duplicate artifacts removed
- MIT License added
- LinkedIn Projects updated
- LinkedIn Featured updated
- CV updated
- Interview narrative prepared

---

## 25. Final Definition

This project is a portfolio-grade Machine Learning prototype designed to demonstrate the full analytical workflow from business problem definition to deployed decision-support application.

Its strongest professional value lies not only in model performance, but also in the explicit treatment of methodological limitations, target leakage risk, reproducibility, product communication, and operational interpretation.