# Medical Appointment No Shows


## Dataset

For this project, I selected the "Medical Appointment No Shows" dataset for analysis. The dataset was downloaded from Kaggle as a csv file.This dataset shows the information on patients who booked about 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment.
This analysis aims to find out reasons why some patients did not show up after making an appointment.
The following are the column names and their siginficance.
1. Patient ID - This indicates the identification number of the patient.

2. Appointment ID -This shows the identification number of the appointment made by the patient.

3. Gender - This is either of the two sexes (Male or Female) . The Female gender is in greater proportion because the female               takes more care of their health than the male individual.

4. Scheduled Day -This is the day the patients have to see the doctor.

5. Appointment Day - This is the day when the patients call to book a medical appointment.

6. Age - This is the length of time the patients has lived.

7. Neighbourhood - This indicates the location of the hospital where the appointment takes place.

8. Scholarship - This is the Bolsa Familia scholarship (Family allowance) which is the social welfare program of the Government              of Brazil. It is either a patient is on this scholarship or not (True or False).

9. Hipertension - This tells us if the patient has a pre-existing health condition of hypertension or not (True or False).

10. Diabetes -  This tells us if the patient has diabetes as a pre-existing health condition or not (True or False).

11. Alcoholism - This indicates if a patient is able  or not able to control drinking due to both a physical and emotional                    dependence on alcohol (True or False).

12. Handicap - This indicates if a patient has a disadvantage resulting from impairment or disability that limits the social                  role of an individual (True or False).

13. SMS-received - This specifies if a patient received an appointment reminder via SMS on their phones or not (True or False).

14. No-show - This tells us whether a patient showed up for the appointment or not. "No" means the patient showed up and "yes" means the patient did not show up.

### Question(s) for Analysis 

1. What percentage of patients did not show up for their medical appointments?
2. Which gender showed up for medical appointments more?
3. Did patients with underlying health conditions miss their medical appointments more than patients without any underlying health condition?
4. Which day of the week do patients book appointments most?
5. Which day of the week has the most appointments?
6. Do people who receive an appointment reminder via sms still miss their appointments?
7. How many patients on scholarship missed their medical appointments?
8. Did patients with shorter wait days show up more?


## Summary of Findings

The following are the summary of the findings and results that have been performed in relation to the questions provided at the beginnning of the analysis.

1. The data set as 110527 rows/observations and 14 columns/features with no null values and no duplicate rows.

2. There are incorrect data types in this dataset.The columns "ScheduledDay" and "AppointmentDay" are in object instead of datetime. These data types were changed to datetime.

3. The column "Age" has a negative value which is out of normal range.Instead of dropping the row where the age has a negative value, the negative value was replaced with a positive number.

4. The column "Handcap" has 5 unique values instead of 2 unique values.The 2 unique values indicates whether a patient is handicapped or not(0 = False and 1 = True). The addition of other unique values (2,3,4) could indicate the different types of handicaps or could be an error during data entry.So,these values were replaced with True(1).

5. 20.2% of patients who booked a medical appointment did not show up.

6. 65% female patients and 35% male patients booked a medical appointment.The female gender (64.9%) showed up more than the male gender(35.1%). This is because female patients take care of their health more than male patients. So, the female gender are more likely to show up.

7. There are less patients with underlying health conditions who booked a medical appointment. Patients with underlying health conditions such as hypertension, diabetes, alcoholism, and handicap are more like to miss their appointments.

8. Medical appointments are most likely fixed on Wednesdays. Medical appointments are less likely fixed on Saturdays.

9. 67.9% of patients did not receive SMS while 32.1% of patients received SMS.Patients who did not receive SMS are more likely to show up for their appointments.

10. Patients that are not on scholarship are likely to miss their medical appointments.

11. Patients with longer wait days are less likely to show up for medical appointments.

#### Additional research can be done at the following points

The duration each patient has to wait before their medical appointment.
The health insurance coverage.
More patients.

#### Limitations of my exploration on this dataset are:

The column "Age" has a negative value which is out of normal range.Instead of dropping the row where the age has a negative value, the negative value was replaced with a positive number.
5 patients were booked for an appointment on days before the scheduled day and did not show up.
There were 5 unique values in the handicap columns instead of 2. The values greater than 1 were replaced with 1.
