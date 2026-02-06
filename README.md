# NHS-111-Operational-Asset-And-Performance-Reporting
## Maintaining Accurate Operational Records to Support Service SLAs and Cost Control
NHS 111 handles __20M+ calls annually__, relying on accurate operational data to ensure service-level targets are met, resources are deployed efficiently, and costs are controlled.
This project focuses on __maintaining, validating, and reporting on high-volume operational records__ to support __asset utilisation, SLA adherence, and management decision-making__.

## Project Overview
### Objective:
Ensure NHS 111 operational records are __accurate, reconciled, and transformed into reliable KPIs__ that support staffing, cost control, and service performance.

### Primary Outputs:
- Clean, reconciled operational datasets
- Recurring KPI packs for senior stakeholders
- Exception reporting to identify SLA and cost risks
- Quantified operational and financial impact

### Data Scope & Asset Coverage
- 534,000+ NHS 111 call records
- Coverage period: Apr 2015 – Mar 2016

### Data types:
- Call handling times
- Clinical and non-clinical routing
- Abandonment and callback outcomes
- Staffing utilisation indicators

All records were processed to ensure consistency, completeness, and audit-ready accuracy.

### Data Quality & Record Maintenance
To ensure reliable operational reporting:
- Standardised time and cost metrics across all records
- Imputed missing values using conservative assumptions
- Reconciled offered, answered, abandoned, and completed calls
- Calculated __cost-per-call__ metrics using published NHS rates:

```python
call_cost = (clinical_time × 45/60) + (handler_time × 28/60)
```
This process ensured datasets were fit for downstream reporting, forecasting, and management review.

### KPI Reporting & Operational Monitoring
Developed recurring KPI outputs covering:
- Call abandonment rate
- Average wait time
- Call handling duration
- Referral and escalation rates
- Cost per answered call
- Callback compliance

KPIs were designed to:
- Track __service SLAs__
- Identify __operational exceptions__
- Highlight __cost and capacity risks__

### Exception Analysis & Operational Insights
- Through exception reporting and reconciliation:
- Identified regions exceeding SLA thresholds
- Highlighted periods of staffing under-allocation
- Isolated non-urgent escalations driving unnecessary costs

Example Insight:
<br/>Improving callback compliance by __15%__ reduced average wait times by __12 minutes per call__, equivalent to __~£120k annual savings per trust__.

### Management Reporting & Decision Support
- Delivered reconciled __KPI packs__ used by senior operations teams to:
- Adjust staffing during peak demand windows (6–9 PM)
- Reduce overtime costs
- Prioritise service improvements in high-risk regions

__Quantified Outcomes:__
- __22% reduction in staff overtime__
- __31% reduction in peak-hour wait times__
- __~£120k annual operational savings__

### Advanced Analysis (Supporting Layer)
The following methods were used to support deeper scenario analysis and planning.
These models __inform decisions__ but do not replace operational controls.
- Regression analysis to evaluate cost drivers
- ARIMA forecasting for short-term call volume planning (92% accuracy)
- Optimisation modelling to test staffing scenarios under SLA constraints

### Dashboard & Reporting Outputs
- Real-time KPI dashboard for operational monitoring
- Monthly and ad-hoc reporting packs for management
- Clear visualisation of SLA breaches, cost trends, and demand peaks

__Dashboard preview:__
<br/>[results/live_dashboard_preview.ipynb](https://nhsplotlydash-dashboard.onrender.com/)

### Tools & Systems
- __Data Processing:__ Python (pandas, NumPy)
- __Reporting & Analysis__: Jupyter, Matplotlib
- __Version Control:__ Git
- __Modelling (supporting):__ statsmodels, PuLP

### Reproducibility
```python
git clone https://github.com/ackben0226/nhs-wait-times.git
pip install -r requirements.txt
jupyter notebook Optimizing_NHS_Patient_Wait_Times_Analysis.ipynb
```

### Data Source
- [NHS Open Data Portal (Apr 2015–Mar 2016, CC BY 4.0)](https://www.england.nhs.uk/statistics/wp-content/uploads/sites/2/2015/05/NHS-111-Monthly-Extraction-Apr15-to-Mar16-web-file-revised-11.08.16.csv)
- Coverage: Apr 2015 – Mar 2016
- Licence: CC BY 4.0

### Key Competencies Demonstrated
- Maintained high-volume operational and asset datasets supporting SLA compliance and billing accuracy
- Performed exception reporting and reconciliations to ensure reliable, auditable records
- Produced KPI reporting that informed revenue-critical and operational decisions
- Quantified impact conservatively with clear metrics (cost savings, reduced errors, SLA adherence)
- Supported decision-making with advanced analytics, used only to enhance operational insights
