# 📊 Clinical Codebook and Data Dictionary

## 1. Dataset Overview
This dataset contains clinical, demographic, lifestyle, and oral health information from a cross-sectional observational cohort of 196 women. 

*   **Total Subjects:** 196
*   **Total Variables (Raw):** 38
*   **Missing Data:** All variables have <5% missingness. Missing values in the processed dataset were handled using Multiple Imputation by Chained Equations (MICE).

> **Note on Privacy:** Due to GDPR and institutional ethics regulations, the raw dataset cannot be shared. The variables described below refer to the structure of the data prior to the anonymization and encoding steps performed in the computational pipeline.

---

## 2. Variable Descriptions and Encoding

### Demographics
| Variable Name | Type | Description | Encoding / Range |
| :--- | :--- | :--- | :--- |
| **SubjectID** | String | Unique identifier for each subject | E.g., SSVM001 |
| **Group** | Categorical | Diagnosis cohort | `SjS` = Sjögren's, `No-SjS` = Control |
| **Age** | Numeric | Age of the subject at examination | 26 – 87 years |
| **Menstrual_status**| Categorical | Menopausal stage | `Pre` = Premenopausal, `Post` = Postmenopausal |
| **Genre** | Categorical | Sex of the subject | `Female` (100% of cohort) |

### Lifestyle & Habits
| Variable Name | Type | Description | Encoding / Range |
| :--- | :--- | :--- | :--- |
| **Sport** | Ordinal | Frequency of exercise | 0: Almost daily, 1: 3x/week, 2: Occasional, 4: Rarely, 5: Never |
| **Meals/day** | Numeric | Number of meals consumed per day | Integer |
| **Special_Diet** | Categorical | Type of diet followed | 0: Low fat, 1: Low carb, 2: Mediterranean, 3: High-protein, 4: Keto, 5: Paleo, 6: Vegetarian, 7: Vegan, 8: Others |
| **Sugar_Intake** | Binary | High sugar consumption | 0: No, 1: Yes |
| **Sugar_between_meals**| Binary | Sugar intake between meals | 0: No, 1: Yes |
| **Smoking** | Binary | Current smoking status | 0: No, 1: Yes |
| **Cigarettes/day** | Numeric | Number of cigarettes smoked/day | 3: Social smoker (Categorical exception) |
| **Former_cigarettes** | Binary | Former smoking status | 0: No, 1: Yes |
| **Caffeine** | Binary | Caffeine consumption | 0: No, 1: Yes |
| **Alcohol_drinks** | Binary | Alcohol consumption | 0: No, 1: Yes |

### Comorbidities & Medication
| Variable Name | Type | Description | Encoding / Range |
| :--- | :--- | :--- | :--- |
| **Cardiovascular** | Binary | Presence of cardiovascular conditions | 0: No, 1: Yes |
| **Neoplasia** | Binary | Presence of neoplasms | 0: No, 1: Yes |
| **Gastrointestinal** | Binary | Presence of GI conditions | 0: No, 1: Yes |
| **Diabetes** | Binary | Presence of Diabetes Mellitus | 0: No, 1: Yes |
| **Autoimmune** | Binary | Presence of other autoimmune diseases | 0: No, 1: Yes |
| **Immunosuppressants** | Binary | Active use of immunosuppressants | 0: No, 1: Yes |
| **Corticosteroids** | Binary | Active use of corticosteroids | 0: No, 1: Yes |
| **Hyposalivation_med** | Binary | Active use of xerogenic drugs | 0: No, 1: Yes |

### Oral & Dental Health
| Variable Name | Type | Description | Encoding / Range |
| :--- | :--- | :--- | :--- |
| **N_Teeth** | Numeric | Total number of present teeth | 0 – 28 |
| **Sound** | Numeric | Number of healthy teeth | Integer |
| **Decay** | Numeric | Number of decayed teeth | Integer |
| **Missing** | Numeric | Number of missing teeth | Integer |
| **Filling** | Numeric | Number of dental fillings | Integer |
| **CAO (DMFT)** | Numeric | Decayed, Missing, Filled Teeth index | Sum of Decay + Missing + Filling |
| **PROTESIS** | Binary | Presence of an oral prosthesis | 0: No, 1: Yes |
| **IPC** | Ordinal | Community Periodontal Index | 0: Healthy, 1: Bleeding, 2: Calculus, 3: Pocket 4-5mm, 4: Pocket ≥6mm, X: Excluded, 9: Not recorded |
| **N_Oral_mucosa_disorder**| Numeric| Number of oral mucosal lesions | Integer |

### Salivary Function
| Variable Name | Type | Description | Encoding / Range |
| :--- | :--- | :--- | :--- |
| **SA_Flow** | Numeric | Unstimulated (Resting) salivary flow | mL/min |
| **ST_Flow** | Numeric | Stimulated salivary flow | mL/min |
| **SA_Hyposalivation** | Binary | Unstimulated hyposalivation (≤0.1 mL/min)| 0: No, 1: Yes |
| **ST_Hyposalivation** | Binary | Stimulated hyposalivation (≤0.7 mL/min) | 0: No, 1: Yes |