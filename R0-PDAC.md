# Appendix II

The following second appendix lists the R printouts of this analysis.

## Tibbles
* `tcga`: Overall dataset with G and gender converted to numerical value (X becomes -1, gender is one for males).
* `tcgaR0`: Patients known to undergone a successful resection.
  * 108 patients are known to have R0 resections.
* `tcgaPDAC`: Successfully resected patients known to be diagnosed with PDAC.
  * 87 of the patients have PDAC, which represents 80% of the dataset.
* `tcgaNotOther`: PDAC patients under consideration not known to pass away due to other causes.
  * 84 of them are not excluded because of death reason.
* `tcgaOS`: PDAC patients under consideration confirmed to have passed away.
  * 47 of them passed away from the disease.
* `tcgaDFS`: PDAC patients with DFS information and known to have recurred.
  * 38 of the are known to have recurred.
* `tcgaDFSOS`: PDAC patients under consideration with both recorded OS and DFS.
  * 28 of them have both information.

## Specification of the Columns

```
> spec(tcga)
cols(
  `Study ID` = col_character(),
  `Patient ID` = col_character(),
  `Sample ID` = col_character(),
  `Diagnosis Age` = col_double(),
  `American Joint Committee on Cancer Metastasis Stage Code` = col_character(),
  `Neoplasm Disease Lymph Node Stage American Joint Committee on Cancer Code` = col_character(),
  `Neoplasm Disease Stage American Joint Committee on Cancer Code` = col_character(),
  `American Joint Committee on Cancer Publication Version Type` = col_character(),
  `American Joint Committee on Cancer Tumor Stage Code` = col_character(),
  `Alcohol Consumption Frequency` = col_double(),
  `Alcohol Exposure Intensity` = col_character(),
  `Alcohol History Documented` = col_character(),
  `Cancer Type` = col_character(),
  `Cancer Type Detailed` = col_character(),
  `Cause of death source` = col_character(),
  `Neoplasm American Joint Committee on Cancer Clinical Group Stage` = col_logical(),
  `Neoplasm American Joint Committee on Cancer Clinical Distant Metastasis M Stage` = col_logical(),
  `Neoplasm American Joint Committee on Cancer Clinical Regional Lymph Node N Stage` = col_logical(),
  `Neoplasm American Joint Committee on Cancer Clinical Primary Tumor T Stage` = col_logical(),
  `Daily Alcohol` = col_double(),
  `Days to Sample Collection.` = col_double(),
  `Last Alive Less Initial Pathologic Diagnosis Date Calculated Day Value` = col_double(),
  days_to_patient_progression_free = col_logical(),
  `Days to Sample Procurement` = col_logical(),
  days_to_tumor_progression = col_logical(),
  `Disease Free (Months)` = col_double(),
  `Disease Free Status` = col_character(),
  `Diabetes Onset Less Initial Pathologic Diagnosis Date Calculated Day Value` = col_double(),
  `Participant Personal Medical History Diabetes Mellitus Ind-3` = col_character(),
  `Disease code` = col_logical(),
  `Ethnicity Category` = col_character(),
  `Lymphomatous Extranodal Site Involvement Indicator` = col_logical(),
  `Family History Cancer Type` = col_character(),
  `Family History of Cancer` = col_character(),
  `Form completion date` = col_character(),
  `Fraction Genome Altered` = col_double(),
  `Neoplasm Histologic Grade` = col_character(),
  `Histologic Grading System Tier Category` = col_character(),
  `Neoplasm Histologic Type Name` = col_character(),
  `Tumor Other Histologic Subtype` = col_character(),
  `Chronic Pancreatitis Personal Medical History Indicator` = col_character(),
  `Chronic Pancreatitis Diagnosis Less Initial Pathologic Diagnosis Date Calculated Day Value` = col_double(),
  `Neoadjuvant Therapy Type Administered Prior To Resection Text` = col_character(),
  `Prior Cancer Diagnosis Occurence` = col_character(),
  `ICD-10 Classification` = col_character(),
  `International Classification of Diseases for Oncology, Third Edition ICD-O-3 Histology Code` = col_character(),
  `International Classification of Diseases for Oncology, Third Edition ICD-O-3 Site Code` = col_character(),
  `Informed consent verified` = col_character(),
  `Year Cancer Initial Diagnosis` = col_double(),
  `Invasive Adenocarcinoma Histology Diagnosis Indicator` = col_character(),
  `Is FFPE` = col_character(),
  `Longest Dimension` = col_double(),
  `Primary Lymph Node Presentation Assessment Ind-3` = col_character(),
  `Positive Finding Lymph Node Hematoxylin and Eosin Staining Microscopy Count` = col_double(),
  `Positive Finding Lymph Node Keratin Immunohistochemistry Staining Method Count` = col_double(),
  `Lymph Node(s) Examined Number` = col_double(),
  `First Pathologic Diagnosis Biospecimen Acquisition Method Type` = col_character(),
  `First Pathologic Diagnosis Biospecimen Acquisition Other Method Type` = col_character(),
  `First Pathologic Diagnosis Biospecimen Acquisition Method Type_1` = col_logical(),
  `Mutation Count` = col_double(),
  `New Neoplasm Event Post Initial Therapy Indicator` = col_character(),
  `Oct embedded` = col_logical(),
  `Oncotree Code` = col_character(),
  `Overall Survival (Months)` = col_double(),
  `Overall Survival Status` = col_character(),
  `Specimen Collection Method` = col_logical(),
  `Other Patient ID` = col_character(),
  `Other Sample ID` = col_character(),
  `Pathology Report File Name` = col_character(),
  `Pathology report uuid` = col_character(),
  `Patient Death Reason` = col_character(),
  `Primary Other Site of Disease Name` = col_character(),
  `Patient Primary Tumor Site` = col_character(),
  `Project code` = col_logical(),
  `Tissue Prospective Collection Indicator` = col_character(),
  `Race Category` = col_character(),
  `Did patient start adjuvant postoperative radiotherapy?` = col_character(),
  `Surgical Margin Resection Status` = col_character(),
  `Tissue Retrospective Collection Indicator` = col_character(),
  `Number of Samples Per Patient` = col_double(),
  `Sample Initial Weight` = col_double(),
  `Sample Type` = col_character(),
  `Sample type id` = col_double(),
  Sex = col_character(),
  `Shortest Dimension` = col_double(),
  `Tumor Tissue Site` = col_character(),
  `Person Cigarette Smoking History Pack Year Value` = col_double(),
  `Started Smoking Year` = col_double(),
  `Stopped Smoking Year` = col_double(),
  `Somatic Status` = col_character(),
  `Specimen Current Weight` = col_logical(),
  `Specimen Freezing Means` = col_logical(),
  `Specimen Second Longest Dimension` = col_double(),
  `Stage Other` = col_logical(),
  `Adjuvant Postoperative Targeted Therapy Administered Indicator` = col_character(),
  `Time between clamping and freezing` = col_logical(),
  `Time between excision and freezing` = col_logical(),
  `Tissue Source Site` = col_character(),
  `TMB (nonsynonymous)` = col_double(),
  `Patient Smoking History Category` = col_double(),
  `Primary Therapy Outcome Success Type` = col_character(),
  `Tumor resected max dimension` = col_double(),
  `Person Neoplasm Status` = col_character(),
  `Vial number` = col_character()
)
```
