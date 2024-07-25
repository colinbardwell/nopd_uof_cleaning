This is a log of changes and resources used as cleaning was performed on a snapshot of the NOPD Use of Force Incidents dataset.
The dataset includes initial reviews - subject to change, updated nightly

Pulled data on July 1st, 2024. Imported into Excel.

Goals: Clean dataset, identify questions for analysis

OBSERVATIONS and CORRECTIONS

	General Observations: 
		- Columns that should have one value occasionally have multiple. In those cases, the first value is kept.
		- Missing data will be addressed more thoroughly with Python, as there are lots individual columns with null values as well as rows with large swathes of data missing.

	- Originating Bureau: 
		- 5 incidents are blank in this field, all of which are missing more division information. 
			- The quantity of missing data across columns for these incidents would for them to be removed from analysis.
		- 1 row changed from ISB - Investigative Services Bureau | FOB - Field Operations Bureau to ISB - Investigative Services Bureau
		- 6 row changed from MSB - Management Service Bureau to MSB - Management Services Bureau
		- 2 rows changed from "Office of the Superintendant" to "Office of the Superintendent".
		- 36 rows changed from "ISB - Investigations and Support Bureau" to "ISB - Investigation and Support Bureau"
		- 27 rows changed from "ISB - Investigative Services Bureau to "ISB - Investigation and Support Bureau"
		- FTN2019-0284 changed from "PIB - Public Integrity Bureau" to "FOB - Field Operations Bureau"
		- FTN2021-0244 and FTN2023-0320 changed from "ISB - Investigation and Support Bureau" to "FOB - Field Operations Bureau"
		- FTN2022-0241 and FTN2018-0394 changed from "MSB - Management Services Bureau" to "FOB - Field Operations Bureau"
		- FTN2021-0202, FTN2018-0377 changed from "FOB - Field Operations Bureau" to "ISB - Investigation and Support Bureau"		
		- FTN2022-0002 changed from "FOB - Field Operations Bureau" to "PSAB - Prof Standards & Accountability Bureau"
		- FTN2018-0378 changed from "FOB - Field Operations Bureau" to "PIB - Public Integrity Bureau"


	- Division level: 
		- 6 incidents have two reported division levels, separated by |. Kept first division level.
		- 103 rows changed from "SOD" to "Special Operations Division"
		- 5 rows changed from "ADD", 4 from "Administrative Duties Services", 1 from "Administrative Support Unit" to "Administrative Duties Division"
		- 10 rows changed from "ED & TRN", 2 from "Education/Training & Recruitment Division" to "Education and Training Division"		
		- 11 rows changed from "Districts", 3 to "8th District", 4 to "6th District", 3 to "5th District", and 1 to "7th District"
		- 10 rows changed from "CID", 1 from "CID JUV", 1 from "Criminal Investigation Section" to "Criminal Investigations Division"
		- 4 rows changed from "SID" to "Special Investigations Division"
		- 1 row changed from "Integrity", 1 from "Integrity Criminal" to "PIB"
		- 1 row changed from "Alternative Police Response" to "Criminal Investigations Division"
		- 3 rows changed from "CE & CL" to "Crime Lab and Evidence Division"
		- FTN2019-0070 and FTN2017-0034 changed from "ISB Staff" to "Special Investigations Division"
		- 5 rows changed from "ISB Staff" to "Unknown"
		- FTN2022-0241 changed from "MSB" to "Unknown"
		- FTN2016-0020 and FTN2021-0232 changed from "Administrative Duties Division" to "Unknown"
		- 1 row changed from "Not Nopd" to "Unknown"
		- FTN2019-0012 changed from "Unknown" to "5th District"
		- 8 rows changed from "Force Investigation Team" to "PIB"

	- Division:
		- 1 row changed from "Administration" to "Admin"
		- 11 rows changed from "Unknown Division" to "Unknown"
		- FTN2019-0314 and FTN2018-0257 changed from "ISB Staff" to "Unknown"
		- 5 rows changed from "FOB" to "Unknown"
		- 91 rows changed from DIU (Persons, Property, SPEC, and Staff) to "D.I.U."
		- 20 rows changed from "1st District" to "Unknown"
		- 24 rows changed from "2nd District" to "Unknown"
		- 27 rows changed from "3rd District" to "Unknown"
		- 18 rows changed from "4th District" to "Unknown"
		- 29 rows changed from "5th District" to "Unknown"
		- 22 rows changed from "6th District" to "Unknown"
		- 45 rows changed from "7th District" to "Unknown"
		- 78 rows changed from "8th District" to "Unknown"
		- 46 rows changed from "Task Force A" to "Task Force"
		- FTN2017-0052, FTN2017-0101, FTN2017-0100 changed from "Unknown" to "Task Force"
		- FTN2022-0195 changed from "Unknown" to "Tactical Section"
		- 64 rows changed from "Tact 1" to "Tactical Section"
		- 1 row changed from "Tact 2" to "Tactical Section"
		- 3 rows changed from "Intelligence" to "Intelligence Section"
		- 1 row changed from "Juvenile" to "Juvenile Section"
		- 1 row changed from "Narcotics" to "Narcotics Section"
		- 4 rows changed from "Special Victims  Section" to "Special Victims Section"
		- 5 rows changed from "Sex Crimes Child Abuse", 2 from "Sex Crimes" to "Special Victims Section"
		- 3 rows changed from "Homicide" to "Homicide Section"
		- 1 row changed from "Integrity", 1 from "Investigations", 6 from "PIB", 2 from blank to "Force Investigation Team"
		- 50 rows changed from "1st Platoon" to "A Platoon"
		- 68 rows changed from "2nd Platoon" to "B Platoon"
		- 41 rows changed from "3rd Platoon" to "C Platoon"
		- 64 rows changed from "Second Watch" to "Evening Watch"
		- 1 row changed from "Traffic" to "Traffic Section"
		- 6 rows changed from "Day Beats" to "Day Watch"
		- 2 rows changed from "Traffic" to "Traffic Section"
		- 1 row changed from "CID Staff" to "Staff"



	- Unit:
		- Two incidents have the | delimiter in front of their unit.
			- The first is marked as "duplicate investigation" in disposition in addition to some other quality issues, so the whole row will be dropped for this analysis. 
		- FIT Criminal Investigations is input in one row, while FIT/Crim is in another. The division level is changed to PIB for both, and Criminal Investigations changed to be the unit.
		- 3 rows changed from "General Assignments Other" to "Gen Assignment Other". The corresponding division is changed as well.
		- 1 row changed from "k" to "K-9 Section". The division is listed as K9 Section and is changed to "Other Support" to match the other K-9 Section instances.
		- 3 rows changed from "Unknown" to "Unknown Assignment"
		- 3 "Shooting" related units changed to "Shooting Squad"
		- 1 "Squad C | Day Watch" changed to "Squad C"
		- 2 "Patrol" units input as "pat" and "patr" changed
		- 1 row changed from "Motorcycle 1" to "Motorcycle 1st Platoon"
		- 2 rows changed from "Support Staff" to "Staff"
		- 1 row changed from "Night Watch | Gen Assignment Other" to "Gen Assignment Other"
		- 1 row changed from "Day Watch | Tact 1" to "Tact 1"
		- 5 rows changed from "A Platoon" to "A"
		- 1 row changed from "Admin Unit" to "Admin"
		- 1 row changed from "A Section" to "A"
		- 48 rows changed from "DIU Persons DIU" to "Persons"
		- 39 rows changed from "DIU Property DIU" to "Property"
		- 1 row changed from "DIU SPEC Other" to "SPEC"
		- 3 rows changed from "DIU Staff DIU" to "Staff"
		- FTN2024-0060 and FTN2021-0237 changed from "A" to "Unknown"
		- FTN2021-0206 changed from "B" to "Unknown"
		- 74 rows changed from "Task Force A" to "A"
		- 3 rows changed from "Task Force B" to "B"
		- 4 rows changed from "Patrol", 19 from blank to "A"
		- 1 row changed from "Squad B" to "B"
		- FTN2016-0050, FTN2019-0099 changed from "Patrol" and "Staff" to "Unknown"
		- 32 rows changed from blank to "Unknown" (no Task Force Unit value), 1 from "1st Platoon" to "Unknown"
		- 18 rows changed from "Task Force A" to "Unknown", having divisions such as "A Platoon" and "Narcotics" as opposed to "Task Force"
		- 3 rows changed from "3rd Platoon" to "Unknown", under division "Juvenile Section"
		- 67 rows changed from "Tact 1" to "1st Platoon"
		- 1 row changed from "Tact 2" to "2nd Platoon"
		- 5 rows changed from blank to "Child Abuse"
		- 2 rows changed from "Domestic Violence", 1 from "Sex Crimes Platoon 1" to "Sex Crimes"
		- 2 rows changed from "Domestic Violence Unit" to "Domestic Violence"
		- 6 rows changed from "Adminstrative Staff" to "Admin"
		- 6 rows changed from "patrol" to "Patrol"
		- 1 row changed from "Sex Crimes Platoon 1" to "Sex Crimes"


	- Working Status
		- 1 row changed from "Overtime" to "Regular Working"
		- 3 rows changed from "Regular Working | Unknown Working Status" to "Regular Working"
		- 1 row changed from "Regular Workingre" to "Regular Working"
		- 2 rows changed from "RUI 2012-0947-C" to "Unknown Working Status"
		- 2 rows changed from "DUI 2009-0665-R" to "Unknown Working Status"
		- 3 rows changed from "AWP - Off Duty" to "Off Duty" 
		- 1 row changed from "Detailed Temporarily" to "Paid Detail"
		- 2 rows changed from "Re-Assigned" to "Regular Working"

	- Shift
		- 2 rows changed from "8a-4p" to "Between 7am-3pm"
		- 1 row changed from "Between 7am-3pm | Unknown Shift Hours" to "Between 7am-3pm"
		- 1 row changed from "Between 3pm-11pm | Unknown Shift Hours" to "Between 3pm-11pm"

	- Investigation Status
		- Verified "Suspended" and "Initial" status; no blank cells
		- Most initial investigations (11/15) are pending on incidents that are over a year old.
		- 1 suspended investigation among all incidents, from 2/25/2017 (FTN2017-0103)

	- Disposition
		- 2 rows dropped: 1 with "Cancel FIT FTN", 1 with "Cancelled" (both have missing officer identification data)
		- 1 row changed from "UOF Not Justified With Policy Violations" to "UOF Not Justified"
		- 1 row contains "UOF Force Used Against Officer"? Left as-is for now. Useful demonstration of quality issues/need to investigate individual incidents to understand context.

	- Service Type
		- Most non-FOB incidents have Service Type values that may indicate that the wrong Originating Bureau was input for these incidents.
		- Officers in the Education and Training Division within the Management Services Bureau are responding to calls for service and stopping pedestrians?
		- Multiple officers assigned to administrative duties used force to arrest subjects?
		- 3 rows changed from "Arresting | Call for Service" to "Call for Service"
		- 2 rows changed from "Pedestrian Stop | Arresting" to "Pedestrian Stop"
		- 1 row changed from "Traffic Stop | Arresting" to "Traffic Stop"
		- Changed to "Other":
			- 1 row  each, "Tactical Search" and "Transport"
			- 4 rows "Special Event"
			- 6 rows "Not Used" 
			- 20 rows "Flagged Down"

	- Light Condition
		- 1 row changed from " | Good" to "Good"
		- 1 row changed from "Poor | Good" to "Poor"
		
	- Weather Condition
		- 1 row changed from " | Clear Conditions" to "Clear Conditions"
		- 1 row changed from "Other | Clear Conditions" to "Other"
		- 1 row changed from "Rainy Conditions - Light | Clear Conditions" to "Rainy Conditions - Light"

	- Subject Arrest Charges
		- Only 8 rows have values, all with different charges. The rest are blank.

	- Use of Force Reason
		- Changed to "Other":
			- 1 row "Possibly armed subject"
			- 1 row "Battery on Reporting Person"
			- 1 row "Felony Stop"
			- 1 row "Other-Create Distance"
			- 1 row "Other-Resisting
			- 1 row "Felony Vehicle stop"
			- 1 row "Escorting/Handcuffed"
		- Changed to "refuse verbal commands":
			- 2 rows "refuse verbal commands | Resisting Lawful Arrest"
			- 1 row "refuse verbal commands | Battery on Police Officer"
		- 1 row changed from "Building clearing" to "Room Clearing"
		- 20 rows standardized to "Room Clearing" (all capitalization errors)
		- 1 row changed from "Weapon Discharged" to "Weapon Exhibited"
		- 799 rows changed from "refuse verbal commands" to "Refusal of Verbal Commands"


QUESTIONS:

	How has disposition trended over time?
	
	How have Use of Force Reasons changed over time/by division? 
	
	What Service Types are most involved in Use of Force incidents?

	2021 annual report compared to cleaned data
		How many force incidents with no arrest?
		Could I visualize tables for more accessible insights?
		Chart 1: Should not include CEW Exhibited as the data is meaningless past 2018 and clutters the chart
		Table 1: Why have arrests gone down 50% in past 5 years, use of force only down 32%?
			 How many force incidents with no arrest?
	

References:

https://www.nola.com/news/police-response-times-spike-during-nopd-shift-changes-analysis-shows/article_1f67b3d6-fa6f-5477-ab55-b10ffcb978cc.html
 - "Like most police agencies, the NOPD operates on a three-platoon system. First Watch starts at 6:25 a.m., 35 minutes before the graveyard shift is over, and it ends at 3 p.m., overlapping the Second Watch by 35 minutes. Third Watch starts at 10:25 p.m., with the same 35-minute overlap."

https://nola.gov/nopd/about-us/bureaus/

https://nola.gov/getattachment/NOPD/Policies/Chapter-41-1-2-Uniformed-Patrol-Platoon-Structure-Assignments-AWP-Days-EFFECTIVE-1-14-18.pdf/

https://nola.gov/getattachment/NOPD/NOPD-Consent-Decree/Chapter-1-3-Use-of-Force.pdf/

https://nola.gov/nopd/about-us/bureaus/field-operations/special-operations-division/

https://nola.gov/nopd/documents/investigation-support-bureau-(isb)-flowchart/

https://nola.gov/nola/media/NOPD/Consent%20Decree/2021-Use-of-Force-Annual-Report.pdf

