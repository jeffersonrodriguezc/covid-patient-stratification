# **A COVID-19 PATIENT SEVERITY STRATIFICATION USING A 3D CONVOLUTIONALSTRATEGY ON CT-SCANS**
---
## Description

### Overview
The main diagnostic test for SARS-CoV2 is the RT-PCR but recent studies have reported a large variance between 58% and 96%. Image-based diagnosis tools could help to support early detection of SARS-CoV2. Several approaches have been proposed to support diagnostic decisions for COVID-19 disease on CT-scans. Some of them, are based on the manual selection of clinically relevant slices. Nonetheless these approaches **only discriminate among disease classes, not disease severity**. Additionally, the **selection of clinically relevant CT slices is a tedious task**, that might be impractical on clinical routine. More recently, 3D convolutional approaches have been adapted to learn from complete CT-scans.

### Complexity
Although quantifying disease patterns could reduce inter-reader variability in diagnosis, the expert radiologist diagnosis on CT-scans has been reported to have a sensitivity between 61% and  99%, but with a low specificity of around 33% (Buyun Xu, et al., “Chest ct for detect-ing covid-19: a systematic review and meta-analysis ofdiagnostic accuracy,” (2020)). Hence, the automatic quantification of disease patterns could reduce such inter-reader variability in the diagnosis.

The severity quantification from CT-scans has been started to be explored, for instance by introducing a corona score to measure disease progression from activation maps that correlate burden opacity regions (Ophir  Gozes, “Rapid  ai  devel-opment cycle for the coronavirus (covid-19) pandemic:Initial results for automated detection, patient monitor-ing using deep learning ct image analysis,” 2020). Other authors have measure disease progression using the percentage of infection (POI) and the average infection from Hounsfield unit values (HU), based on regional infection annotations (Fei Shan, “Lung infection quan-tification of covid-19 in ct images with deep learning,”2020).



### Aims and contributions

This work explores the use of volumetric convolutional architectures to stratify among 5 different COVID-19 levels. These architectures learn complete CT visual representation, without using explicit finding segmentations, retrieving also explainable attentions maps that could complement the diagnosis task. Three contributions can be described for this work:

* A volumetric and convolutional representation of complete CT-scans  (anisotropic 3D volumes) that allows stratifying the patients according to the lung infection severity by the COVID-19 disease.

* A set of explainable volumetric attention maps that represent main CT regions taken into account for the model to give a particular prediction. These maps can highlight radiological findings and lung regions, providing complementary information during COVID-19 diagnosis.

* A new dataset is also introduced with a total of 350 CT-scans, categorized by two expert radiologists, according to the level of pneumonia affectation related to COVID-19 disease.

### Evaluation Scheme

This work evaluated the performance of 3D-CNN architectures in two different classification tasks: a binary classification (COVID-19 / non-COVID-19) and the severity of disease stratification. In both experiments a 4-fold stratified cross-validation scheme was used. The performance of the deep learning models was evaluated by computing the precision, recall and F1-score metrics. The folds were stratified by patient and class, so there was no patient overlap between the folds used for training and testing. For the severity classification, the folds were stratified by patient and severity category.

[comment]: # (poner tabla 3)

![results](https://gitlab.com/FranklinSierra95/covid-patient-stratification/-/raw/master/images/tabla3-results.PNG)