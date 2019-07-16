# Motivation:
To examine whether or not certain ER hospital admission features predict whether or not a hospital stay will be profitable or not.

# The Dataset:
#### For this project, I used the De-identified "HOSPITAL DISCHARGE DATASET (2012) FOR NY STATE." This dataset contains the following columns of information:

Health Service Area	- A description of the Health Service Area (HSA) in which the hospital is located. Blank for abortion records. (Capital/Adirondack, Central NY, Finger Lakes, Hudson Valley, Long Island, New York City, Southern Tier, Western NY).

Hospital County	- A description of the county in which the hospital is located. Blank for abortion records.

Operating Certificate Number - The facility Operating Certificate Number as assigned by NYS Department of Health. Blank for abortion records.
	
Facility ID	- Permanent Facility Identifier. Blank for abortion records.

Facility Name	- The name of the facility where services were performed based on the Permanent Facility Identifier (PFI), as maintained by the NYSDOH Division of Health Facility Planning. For abortion records ‘Abortion Record – Facility Name Redacted’ appears.

Age Group	- Age in years at time of discharge. Grouped into the following age groups: 0 to 17, 18 to 29, 30 to 49, 50 to 69, and 70 or Older.

Zip Code - The first three digits of the patient's zip code. Blank for: - population size less than 20,000 - abortion records, or - cell size less than 10 on population classification strata. “OOS” are Out of State zip codes.

Gender - Patient gender: (M) Male, (F) Female, (U) Unknown

Race - Patient race. Black/African American, Multi, Other Race, Unknown, White. Other Race includes Native Americans and Asian/Pacific Islander.

Ethnicity - Patient ethnicity. The ethnicity of the patient: Spanish/Hispanic Origin, Not of Spanish/Hispanic Origin, Multi, Unknown.

Length of Stay - The total number of patient days at an acute level and/or other than acute care level (excluding leave of absence days) (Discharge Date - Admission Date) + 1. Length of Stay greater than or equal to 120 days has been aggregated to 120+ days.

Type of Admission	- A description of the manner in which the patient was admitted to the health care facility: Elective, Emergency, Newborn, Not Available, Trauma, Urgent.

Patient Disposition	- The patient's destination or status upon discharge.

Discharge Year - The year (CCYY) of discharge.
	
CCS Diagnosis Code - AHRQ Clinical Classification Software (CCS) Diagnosis Category Code. More information on the CCS system may be found at the direct link: http://www.hcup-us.ahrq.gov/toolssoftware/ccs/ccs.jsp

CCS Diagnosis Description - AHRQ Clinical Classification Software (CCS) Diagnosis Category Description. More information on the CCS system may be found at the direct link: http://www.hcup-us.ahrq.gov/toolssoftware/ccs/ccs.jsp
	
CCS Procedure Code - AHRQ Clinical Classification Software (CCS) ICD-9 Procedure Category Code. More information on the CCS system may be found at the direct link: http://www.hcup-us.ahrq.gov/toolssoftware/ccs/ccs.jsp

CCS Procedure Description - AHRQ Clinical Classification Software (CCS) ICD-9 Procedure Category Description. More information on the CCS system may be found at the direct link: http://www.hcup-us.ahrq.gov/toolssoftware/ccs/ccs.jsp
	
APR DRG Code - The APR - DRG Classification Code

APR DRG Description - The APR-DRG Classification Code Description In Calendar Year 2011, Version 28 of the APR-DRG Grouper. http://www.health.ny.gov/statistics/sparcs/sysdoc/appy.htm
	
APR MDC Code - All Patient Refined Major Diagnostic Category (APR MDC) Code. APR-DRG Codes 001-006 and 950-956 may group to more than one MDC Code. All other APR DRGs group to one MDC category.

APR MDC Description - All Patient Refined Major Diagnostic Category (APR MDC) Description.
	
APR Severity of Illness Code - The APR-DRG Severity of Illness Code: 1, 2, 3, 4
	
APR Severity of Illness Description	- All Patient Refined Severity of Illness (APR SOI) Description. Minor (1), Moderate (2), Major (3) , Extreme (4).
	
APR Risk of Mortality	- All Patient Refined Risk of Mortality (APR ROM). Minor (1), Moderate (2), Major (3) , Extreme (4).
	
APR Medical Surgical Description - The APR-DRG specific classification of Medical, Surgical or Not Applicable.
	
Payment Typology 1 - A description of the type of payment for this occurrence.

Payment Typology 2 - A description of the type of payment for this occurrence.
	
Payment Typology 3 - A description of the type of payment for this occurrence.
	
Attending Provider License Number - The professional license number, issued by the New York State Department of Education, used to identify the physician or other health care professional primarily responsible for the care of the patient. Blank for abortion records.
	
Operating Provider License Number - The professional license number, issued by the New York State Department of Education, used to identify the physician or other health care professional who performed the principal procedure. Blank for abortion records.
	
Other Provider License Number - The professional license number, issued by the New York State Department of Education, used to identify the physician or other health care professional (other than the Attending Physician or Operating Physician) who was involved in the patient's care or treatment (e.g., consulting physician, second operating physician, nurse/midwife). Blank for abortion records.
	
Birth Weight - The neonate birth weight in grams; rounded to nearest 100g.

Abortion Edit Indicator - A flag to indicate if the discharge record contains any indication of abortion ("N" = No; "Y" = Yes).
	
Emergency Department Indicator - The Emergency Department Indicator is set based on the submitted revenue codes. If the record contained an Emergency Department revenue code of 045X, the indicator is set to "Y", otherwise it will be “N”.

Total Charges - Total charges for the discharge.

Total Costs - Total estimated costs for the discharge.

# Methods

Utilizing this dataset, I was able to calcluate estimated operating margins for each encounter and I distilled the dataset to relevant features that may affect cost as it relates to the hospital admission. 
I then tested Logistic Regression, Decision Tree, Random Forest, Gradient Boost, Adaboost, and XGBoost to find the best model to predict these features. I then used a waterfall graph to explore how the features interact to predict hospital admission/discharge profitability.

<a href="https://github.com/lpilossoph/Hospital-Admission-Analysis/blob/master/Final_Project3.ipynb">Link to Notebook</a>

# Use Cases

The ability to gain insight on which kinds of hospital admissions are most profitable has many use cases. Ideally, a tool like this could assist ambulances to direct patients to the appropriate hospital where their specialties match with the patient's diagnosis, increasing the chances of profitability. It also helps to provide insight into failing hospitals who could perhaps redirect their resources to deal with the specific needs of their patient population and community, thereby decreasing the chance of hospital operating margin deficits. 
