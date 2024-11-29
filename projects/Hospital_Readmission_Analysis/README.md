# Insights Deep-Dive

![Screenshot 2024-11-29 105452](https://github.com/user-attachments/assets/feeb3b76-2ba9-4b5f-abfd-eef7620eabca)

## Patient Admissions & Readmissions:
1,135 patient admissions were identified from 28,000 encounters. <br><br>
396 unique patients were admitted, with a peak in unique admissions in 2014 and 2020.<br><br>
14% readmission rate within 30 days, which dropped below 5% during 2020-2021 due to COVID-19.<br><br>
The hospital has an opportunity to capitalize on the post-pandemic readmission drop by maintaining improved operational practices.<br><br>

## Length of Stay:
The average length of stay per visit is 7.3 hours.<br><br>
The average length of stay for admitted patients was 37 hours, while non-admitted patients averaged just under 45 minutes.<br><br>
Since the pandemic, the average length of stay for admissions has risen to 55 hours, compared to just over 24 hours pre-pandemic.<br><br>
Reducing admitted patients’ length of stay to pre-pandemic levels will be essential for improving patient throughput and resource allocation.<br><br>

## Cost Analysis:
The average cost per visit stands at $3.7k across all encounters.<br><br>
The average cost of stay for admissions is $7.8k, double that of non-admissions at $3.5k.<br><br>
Admission costs surged by 4.8x during the pandemic in 2020 due to COVID-19.<br><br>
Uninsured patients have higher average costs: $9.2k for admissions versus $7.3k for insured patients.<br><br>
The data suggests that uninsured patients have disproportionately higher medical costs, especially middle-aged adults with the highest average cost at $10.4k with 44% of admissions uninsured.<br><br>

## Insurance Coverage:
About 68% of procedures are covered by insurance, with 41% of those procedures covered by Medicare and 32% of all procedures uninsured.<br><br>
Patients ages 18-64 are the most likely to lack health insurance, experiencing higher average costs of stay, approximately $1k more than other demographics.<br><br>
For admissions, the average cost is $7.3k for insured patients and $9.2k for uninsured.<br><br>
For non-admissions, insured patients average $2.6k, while uninsured average $5.5k.<br><br>
This uninsured rate and increased costs highlight the need for improved insurance coverage and financial support to ensure equitable healthcare access and financial sustainability for the hospital.<br><br>

## Recommendations
<b>Sustain Low Readmission Rates:</b> MGH should continue to implement the changes introduced during the pandemic that helped reduce the readmission rate to below 5%.<br><br>
<b>Improve Patient Throughput:</b> Reducing the length of stay for admitted patients to pre-pandemic levels is critical for optimizing hospital resources and improving patient throughput.<br><br>
<b>Increase Insurance Coverage:</b> The hospital should work on initiatives to improve insurance coverage among patients, particularly for those in high-cost demographics such as middle-aged adults.<br><br>
<b>Support for Uninsured Patients:</b> Implementing financial assistance programs for uninsured patients could alleviate the burden of high medical costs and improve access to care.<br><br>

## Key Questions for Stakeholders Prior to Project Advancement
These are some questions I would've loved to ask stakeholders/project leads to learn more about their own needs/existing knowledge on the objective at hand.<br><br>
What interval do you use for measuring readmissions: 30, 60, or 90 days after a previous admission?<br><br>
Should readmissions be related to the same medical conditions or reasons as the initial admission?<br><br>
How are encounter entries recorded? Given that some admissions are logged exactly 24 hours apart, how should these be treated? Are these entries reset daily, or should they be considered continuous admissions?<br><br>

## Assumptions and Caveats
The readmission rates are based on a 30-day interval for returning patients with encounter class "inpatient".<br><br>
Encounters are considered readmissions regardless of previous reason for visit.<br><br>
Drop in readmission rate on 2020 onwards was assumed to be caused by the pandemic.<br><br>
Length of stay calculations only include encounters labeled as inpatient admissions.<br><br>
Cost data reflects a spike in expenses during the pandemic period (2020), which may not represent typical operational conditions.<br><br>


