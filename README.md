# WSI-Data-Curation-Pipeline
End-to-end workflow for dermatopathology dataset curation and standardization
# WSI Data Curation Pipeline for Dermatopathology

## Overview

This repository documents the end-to-end workflow used to curate a high-resolution dermatopathology dataset of whole slide images (WSIs) for machine learning research.

The focus is on the **data engineering and preparation process**, which is often underreported in computational pathology.

---

## Motivation

Reliable machine learning models depend on high-quality data. However, the process of transforming raw clinical data into structured, usable datasets is complex and rarely described in detail.

This repository aims to provide transparency into the steps required for building a medical imaging dataset.

---

## Pipeline Overview

The dataset was constructed through the following stages:

1. **Patient and Case Identification**
   - Retrieval using institutional identifiers (case numbers, H-numbers)

2. **Slide Retrieval**
   - Extraction of physical glass slides from clinical archives

3. **Slide Preparation**
   - Cleaning and preparation for digitization

4. **Slide Digitization**
   - Whole slide imaging at 20× and 40× magnification
   - Output formats: SVS, MRXS

5. **Pathologist Review**
   - Diagnostic verification
   - Assignment of diagnostic categories (BCC, SCC, mixed, normal)

6. **Quality Control**
   - Removal of low-quality or irrelevant slides
   - Artifact detection (focus, staining, completeness)

7. **Metadata Compilation**
   - Patient demographics
   - Diagnostic labels and subtypes
   - Anatomical site
   - Pathology reports (German + English)

8. **Anonymization**
   - Removal of patient identifiers
   - Use of study-specific IDs

9. **Standardization**
   - Conversion to DICOM format
   - Structured data organization

10. **Final Dataset Assembly**
   - Integration of images and metadata
   - Preparation for TCIA release

---

## Diagnostic Categories

The dataset includes the following diagnostic groups:

- **Basal Cell Carcinoma (BCC):**  
  Includes multiple histopathological subtypes such as nodular/solid, micronodular, infiltrative, and sclerodermiform variants.

- **Squamous Cell Carcinoma (SCC):**  
  Includes invasive SCC cases with associated subtypes where applicable.

- **Mixed BCC/SCC:**  
  Slides containing features of both tumor types.

- **Non-tumor (Normal skin):**  
  Includes a range of benign or non-malignant conditions such as solar elastosis, actinic damage, and scar tissue.

## Key Challenges

- Handling gigapixel whole slide images  
- Ensuring consistency across scanners and magnifications  
- Aligning metadata with image data  
- Maintaining data privacy and anonymization  
- Quality control at scale  

---

## Outcome

The final dataset consists of 2,95 whole slide images across multiple diagnostic categories, with structured metadata and standardized DICOM format, enabling reproducible machine learning research.

---

## Related Projects

-  Dataset (TCIA):  
  https://github.com/solmazhaddady/NMSC-TCIA-Dataset  

-  WSI to DICOM conversion:  
  https://github.com/solmazhaddady/WSI-to-DICOM-Converter  

---

## Author

Solmaz Haddady  
Johannes Kepler University Linz (JKU), Austria
