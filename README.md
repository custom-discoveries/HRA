#  <p align="center">Welcome to HRA Repository</p>

<img width="1028" alt="image" src="https://github.com/user-attachments/assets/e2ad3209-271e-4e18-9128-a6ae71b6c2ea">


HRA is a repository that defines TigerGraph Graph database schema for capturing a user Health Risk Assessments.

The data to load into the database is defined in the GraphData/ directory. 

The src/ directory contains 3 python programs. CreateUserProfile.py program generates a list of Persons and associated attributes, like gender, birthdays etc. The second program, CreateClinicalProfile.py will generate a clinical profile of a member, with a sample of a member’s risks.  The third program, app_profile.py file is a Streamlit app that analysis the data generated by the other programs to see how well your data is 'balanced.'

## Directory Structure
> DDLs/  
>> Data/  
>>> loadVertexData[1].gsql  

>> Queries/  
>>> calculateBodyMass[2].gsql  
    determineBloodPressure[7].gsql  
    determineCholesterol[6].gsql  
    determineDibetic[4].gsql  
    determineHRA[1].gsql  
    determineRisk[8].gsql  
    determineSmoker[3].gsql  
    determineVaccine[5].gsql  
    initializeGraph.gsql

>>Schema/
 >>>defineSchema.gsql  

>GraphData/
 >>>BodyMass-Index.csv  
 ClinicalProfiles.csv  
 PersonProfiles.csv  
 Vaccines.csv  

>src/  
>>>CreateClinicalProfile.py  
>>>CreateUserProfile.py  
>>>app_profile.py  

## Scripts
>installPythonEnvironment.sh - Bash script to setup python environment  
requirements.txt - File that describes Python dependencies  
runClinicalProfiler.sh - Runs app_profile program to analysis generated data files  
runDataProfiler.sh - Runs the CreateClinicalprofile.py program that generates clinical profiles  
runUserProfiler.sh - Runs the CreateUserProfile.py program that generate a user profile, including first and last name, birthday, age, gender.  
