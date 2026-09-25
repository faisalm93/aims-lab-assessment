##  Task Summaries

### Task 1: Scientific Review
* **Article:** Petkeviciene J, et al. *"Anthropometric measurements in childhood and prediction of cardiovascular risk factors in adulthood: Kaunas cardiovascular risk cohort study."* *BMC Public Health*. 2015;15:218.
* **Key Findings:** 
  * Childhood BMI and skinfold thickness independently predict adult metabolic syndrome, hyperglycaemia, and elevated CRP ($p < 0.05$) even after adjusting for adult weight gain.
  * Vascular risks (hypertension, elevated triglycerides, low HDL) are predominantly driven by adult BMI gain rather than childhood adiposity alone.
* **Methodological Highlights:** Addressed 35-year tracking coefficients ($r = 0.41 - 0.56$), collinearity between childhood BMI and adult BMI gain, and sample attrition risks (46.8% final retention).

---

### Task 2: Statistical Analysis
* **Dataset Size:** 29,999 individual records across 21,449 households (1,575 recorded hypertension cases; 5.25% prevalence).
* **Statistical Framework:**
  * **Pearson's $\\chi^2$ Test of Independence:** Screened categorical features against binary chronic target flags.
  * **Cramér's $V$:** Quantified practical effect sizes to distinguish true association strength from sample-size-induced statistical significance ($V \\ge 0.10$ threshold).
  * **Benjamini-Hochberg (BH) Procedure:** Controlled False Discovery Rate (FDR) across tests ($p_{\\text{BH}} < 0.05$).
* **Core Outcomes:**
  * **Strong Predictors:** Recorded diabetes ($V = 0.339$), Union/Location ($V = 0.232$), Age Group ($V = 0.204$), and Current BP Category ($V = 0.196$).
  * **Negligible Effects:** Pulse, Income Class, BMI, and Oxygen Saturation were statistically significant due to $N$, but had negligible effect sizes ($V < 0.07$).
  * **Target Leakage Warning:** BP categories and diagnosis-derived glucose status should be omitted from prospective predictive models.

---

##  Getting Started & Execution

### 1. Prerequisites
Ensure you have Python 3.9+ installed on your system.

### 2. Installation
Clone the repository and install required packages:

```bash
git clone [https://github.com/faisaladam/aims-lab-assessment.git](https://github.com/faisaladam/aims-lab-assessment.git)
cd aims-lab-assessment
pip install -r requirements.txt
