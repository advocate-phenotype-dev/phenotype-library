# Heart Failure with Reduced Ejection Fraction (HFrEF)

## Clinical background

Heart failure with reduced ejection fraction (HFrEF) — historically termed
systolic heart failure — is defined by a left ventricular ejection fraction
(LVEF) below 40% in the setting of symptomatic heart failure. It accounts for
approximately half of all heart failure cases and carries substantial morbidity
and mortality, with five-year survival rates below 50% in population-based studies.

HFrEF is distinguished from heart failure with preserved ejection fraction
(HFpEF, LVEF >= 50%) and heart failure with mildly reduced ejection fraction
(HFmrEF, LVEF 40-49%) by both its pathophysiology and its evidence base for
disease-modifying therapy. Guideline-directed medical therapy including
ACE inhibitors or ARNIs, beta-blockers, MRAs, and SGLT2 inhibitors has
demonstrated mortality benefit specifically in HFrEF.

## Phenotype rationale

This phenotype identifies patients with a confirmed HFrEF diagnosis for use in:

- Trial-ready cohort identification (NCCT)
- Cardiovascular outcomes research
- Quality improvement and care gap analysis
- Learning health system applications

The definition requires both an ICD-10 diagnosis code and an objective LVEF
measurement below 40% on echocardiography, reducing reliance on administrative
coding alone and improving positive predictive value.

## Data sources

Derived from the OMOP Common Data Model (CDM v5.x) using:

- condition_occurrence: ICD-10-CM I50.x mapped to SNOMED concept 316139
- measurement: LOINC 18009-2 and 8806-2 (LVEF by echocardiography)

## Validation

Validated against the Advocate Health NEXUS/OMOP data warehouse using
OHDSI CohortDiagnostics. See validation/cohort_diagnostics/ for full output.

## Known limitations

- LVEF documentation completeness varies by site and encounter type
- Outpatient echocardiograms may lag index diagnosis date
- ICD-10 coding for HFrEF vs HFpEF subtype is inconsistent prior to 2018
