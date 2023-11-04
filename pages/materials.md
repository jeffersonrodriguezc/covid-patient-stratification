# **A COVID-19 PATIENT SEVERITY STRATIFICATION USING A 3D CONVOLUTIONALSTRATEGY ON CT-SCANS**
---
## Materials

A retrospective study is herein presented with the main purpose of characterizing infection severity of the COVID-19 disease on CT-scans. Patient records were reviewed from March 2020 to August 14, 2020. Each patient underwent chest tomography and PCR testing for SARS-CoV-2. The patients were categorized according to the RT-PCR results as COVID-19 patients (with positive RT-PCR) and non-COVID-19 patients (with at least two negative RT-PCR tests and CT-scans without findings). A total of 350 patients, with equal distribution for the 2 categories, were selected. The demographic information and comorbidities distribution is shown below.

[comment]: # (poner tabla 1)

![dataset](https://gitlab.com/FranklinSierra95/covid-patient-stratification/-/raw/master/images/tabla1-dataset.PNG)

The CT-scans were also annotated according to the presence of the severe acute respiratory syndrome (SARS), defined by the Colombian consensus on care, diagnosis, and management of SARS cov-2 / COVID-19 infection. The severity of lung involvement in Chest CT for COVID-19 disease was assessed by 2 expert radiologists. The severity analysis takes into account the extension of pathological findings in each lung lobe according to the involvement percentage as follows:

[comment]: # (poner tabla 2)

![severity](https://gitlab.com/FranklinSierra95/covid-patient-stratification/-/raw/master/images/tabla2-severity.PNG)

Subsequently, to obtain the overall condition (Global CT Score), the scores of each lung lobe were summed up according to  (Marco Francone, “Chest ct score incovid-19 patients:  correlation with disease severity andshort-term prognosis,”European radiology, pp. 1–10,2020). The Global CT Score is on a scale of 0-25 points. Each point indicates 4 percentage units of lung involvement.