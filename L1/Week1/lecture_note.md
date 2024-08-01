# Welcome to Introduction to Clinical Data Science

- Week 1: Clinical Data Science
- Week 2: Clinical Data Types
- Week 3: Introduction to SQL
- Week 4: Introduction to R

# Introduction to Clinical Data Science

### Definition and Context

- **Data Science**: Combination of computer science, mathematics, domain knowledge, and communication skills.
- **Clinical Data Science**: Utilizes healthcare data to generate new knowledge and improve patient care.
- **Biomedical Data Science**: Encompasses biological systems to population health.

### Related Fields

- **Healthcare Data Science**: Similar to healthcare analytics; focuses on healthcare business rather than individual patient health.
- **Health Data Science**: Encompasses clinical and nonclinical data, including fitness, sleep, and wellness data.
- **Biomedical Informatics**: Interdisciplinary science translating data into knowledge and knowledge into action.

### Key Components of Clinical Data Science

- **Data Generation**: Derived from healthcare providers and health systems.
- **Knowledge Generation**: Using data to produce new insights.
- **Patient Care Improvement**: Applying insights to enhance future patient care.

### Overlapping and Emerging Terms

- **Healthcare Data Science vs. Health Data Science**: No consensus on differences; often overlapping in practice.
- **Health Data Science Education Programs**: Often align closely with biomedical data science.

### Informaticians’ Role

- **Broad Perspective**: Informaticians integrate data collection, management, and analysis.
- **System and Implementation Science**: Designing technology-based interventions for healthcare systems.
- **Knowledge to Action**: Emphasizes practical application of data insights.

### Importance of Social Science and Healthcare System Understanding

- **Social Science Knowledge**: Essential for implementing data science discoveries.
- **Healthcare System Insight**: Understanding the system impacts data usage and analysis.
- **Effective Implementation**: Requires careful attention to healthcare environment for adoption of discoveries.

### Course Focus

- **Tool and Method Teaching**: Developed by informaticians for clinical data analysis.
- **Impacting Change**: Emphasizes leveraging clinical data to effect practical improvements in patient care.

# Clinical Data Regulations

### Overview of HIPAA

- **HIPAA**: Health Insurance Portability and Accountability Act, established in 1996.
- **Privacy Rule**: Regulations on use and disclosure of Protected Health Information (PHI).
- **PHI**: Individually identifiable health information (e.g., demographic data, health data).

### Key Entities and Rules

- **Covered Entities**: Health plans, clearing houses, healthcare providers transmitting health information electronically.
- **Identified Data**: Clinical data containing PHI.
- **TPO (Treatment, Payment, Operations)**: Allowed uses of PHI without additional consent.

### Data Types and Use

- **Fully Identified Data**: Used for TPO purposes.
- **Psychotherapy Notes**: Exception to standard PHI use; require additional protections.
- **Limited Data Set**: Partial removal of PHI (e.g., 16 direct identifiers removed) requiring a Data Use Agreement.
- **De-identified Data**: Data with all 18 identifiers plus zip codes and dates removed. No privacy rule restrictions on its use.

### De-identification Methods

- **Safe Harbor Method**: Removal of 18 specific identifiers.
- **Expert Determination Method**: Expert assesses that re-identification risk is very small.
- **Date Shifting**: Dates in records are randomly shifted to maintain data utility while preserving privacy.

### Minimum Necessary Principle

- **Application**: Only the minimum amount of data necessary should be used for a given purpose.
- **Challenge**: Exploratory analyses may require more data than initially anticipated.

### Impact on Clinical Data Science

- **Data Limitations**: De-identified data limits analysis types, especially involving dates and text notes.
- **Ethical Responsibility**: Respect patient privacy and the potential impact of data use.
- **Historical Context**: Health data misuse has led to discrimination, emphasizing the importance of data protection.

### Practical Application

- **Quality Improvement Projects**: Often performed under TPO authorization.
- **Exploratory Analyses**: Challenges arise due to the minimum necessary principle.

### Conclusion

- **Respect and Regulation**: Understanding and adhering to HIPAA regulations is crucial.
- **Patient Trust**: Protecting health data is essential to maintain trust and ensure ethical data science practices.

# **Introduction to the MIMIC-III Data Set**

### Introduction

- **MIMIC**: Medical Information Mart for Intensive Care.
- **Developer**: MIT Lab for Computational Physiology.
- **Current Release**: Third data release.

### Data Overview

- **Patient Data**: Contains de-identified data for over 40,000 patients.
- **Location**: Data from Beth Israel Deaconess Medical Center's adult and pediatric critical units.
- **Research Support**: Used for epidemiology, clinical decision making, and electronic tool development.

### Identification and Tracking

- **Subject_ID**: Identifies each patient.
- **HADM_ID**: Tracks hospital admissions.
- **Tables**: Six tables record details of each hospital stay.
    - **ADMISSIONS:** unique hospitalizations
    - **ICDSTAYS**: unique ICU stays.
    - **PATIENT**: unique patients in data
    - **CALLOUT:** movement from ICU
    - **TRANSFERS:** movement in hospital

### Critical Care Data

- **Tables**: Data collected during critical care stored in eight tables.
    - **CAREGIVERS**: unique caregivers
    - **CHARTEVENTS**: all observations
    - **DATETIMEEVENTS**: all data observations
    - **NOTEEVENTS**: clinical notes
    - **INPUTEVENTS_CV:** fluid intake in CV
    - **INPUTEVENTS_MV:** fluid intake in MV
    - **PROCEDUREEVENTS_MV**: procedures in MV
    - **OUTPUTEVENTS**: fluids excreted

### Hospital Records

- **Additional Data Tables**: Data from the broader hospital record system in seven tables.
    - **CPTEVENTS, DIAGNOSES_ICD, PROCEDURES_ICD, DRGCODES**: Track billing data using structured codes.
    - **LABEVENTS, MICROBIOLOGYEVENTS**: Laboratory measurements.
    - **PRESCRIPTIONS**: Tracks medications ordered or prescribed.
- **Dictionary Tables**: Five tables provide code meanings (prefix D_).
    - **D_CPT**
    - **D_ICD_DIAGNOSES**
    - **D_ICD_PROCEDURES**
    - **D_ITEMS**
    - **D_LABITEMS**

### Educational Use

- **Demo Version**: Limited to 100 patients but includes real patient data.
- **Access Conditions**:
    - **Non-identification Agreement**: Users must agree not to identify patients.
    - **Alert Requirement**: Report potential identifiers to MIT.
    - **Code and Communication Care**: Avoid identifying individuals.
    - **Privacy and Sharing**: Keep data private and not share with others.
    - **Data Use Agreement**: Sign agreement before accessing data.

This structured note encapsulates the essential details and requirements for using the MIMIC database, aiding in understanding its scope, contents, and usage protocols.