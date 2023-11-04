# **A COVID-19 PATIENT SEVERITY STRATIFICATION USING A 3D CONVOLUTIONALSTRATEGY ON CT-SCANS**
---
## 3D convolutional architectures for covid-19 patient stratification on ct-scans

Two 3D convolutional architectures were previously trained to predict different COVID-19 severity levels. The general pipeline includes: (1) the lung parenchyma segmentation, (2) severity classification of the masked CT-scans and (3) visual attention map computation by the retro-propagation of the predictions to the CT original domain.

### Parenchyma segmentation

CT-scans were normalized according to Hounsfield Units window (with centre WL=-400 and width WW=1400). Then, an automatic and coarse lung parenchyma segmentation was obtained by using a standard 2D U-Net. At processing time, the segmentation process is carried out to mask out regions that are not related to the lungs. Only CT-slices whose segmentation corresponds to at least the 5\%  of the whole image is preserved for further analysis.

### 3D CNN architectures

The two selected 3D convolutional architectures were adjusted to discriminate patterns related to the disease degree. To adjust models was followed a transfer learning scheme from pre-trained weights captured on a large dataset of natural sequences. The architectures are described as follows:

* #### Long Term convolutional nets (LTC)

This architecture recovers local volumetric features through 3D convolutions, which hierarchically increase complexity representation to stand out main radiological patterns

* #### Inflated 3D ConvNet (I3D)

This architecture properly learns volumetric low-level features from an inception inflated version backbone (from 2D to 3D). The inception modules capture non-linear relationships, allowing a deep and relatively compact representation from successive branch convolutions

#### Explainable attention maps

In this work, the explainable GradCAM method was adapted to compute attention maps from both severity classification architectures. The GradCAM computes attribution maps by back-propagating the prediction class through multiple layers until it reaches the input layer. Interestingly enough, these maps could correlate and localize some radiological findings such as consolidations.

![cover image](https://gitlab.com/FranklinSierra95/covid-patient-stratification/-/raw/master/images/hallazgos_clases_todas.png)