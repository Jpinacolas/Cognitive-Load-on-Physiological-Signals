[README.md](https://github.com/user-attachments/files/25604105/README.md)
## *A Comprehensive Analysis of the Influence of Cognitive Load on Physiological Signals in Virtual Reality*

Authors: Jorge Pina, Edurne Bernal-Berdun, Daniel Martin, Sandra Malpica, Carmen Real, Alberto Barquero, Pablo Armañac-Julián, Jesus Lazaro, Alba Martín-Yebra, Belen Masia and Ana Serrano

Affiliations: Universidad de Zaragoza - I3A, CIBER-BBN

Our dataset is free to use for any research purposes. Any possible inquiries on its content can be directed at **jpinac (at) unizar (dot) es**.

If you use our dataset for a publication, please cite our work following the bibtex provided in the project page:

https://graphics.unizar.es/projects/CL_Biosignals/

Data is also available in the following Zenodo link: https://zenodo.org/records/18669059

We offer physiological and performance data collected from 36 users. This is provided for four different conditions, resulting of the combinations of high and low cognitive load conditions and 90° and 360° search areas. For each user, you can find:

* Electrocardiogram (ECG)
* Respiration (ImP)
* Electrodermal Activity (EDA)
* Photoplethysmography (PPG)
* Gaze Data
* Pupil Size
* Performance Scores
* Inertial Measurements

Additionally, we also include subjetive measurements in the form of the following questionnaires:

* Demographics
* Shortened Simulator Sickness Questionnaire (SSQ)
* NASA TLX

---

The *signals* folder contains .zip files named *ecg-resp*, *eda-ppg*, *HMDgaze* and *Varjogaze*.

* ecg-resp.zip contains a set of 36 .csv files, one for each participant.

1st column: Timestamps in Unix system (ms)

5th-9th columns: ECG derivations obtained from Shimmer3-ECG (mV)

8th column can be interpreted as respiration estimation (Impedance Pneumography). 9th column should not be used, as the Vx electrode was not placed consistently.

* eda-ppg.zip contains a set of 32 .csv files. Some of the patients are missing eda-ppg data due to technical issues with the sensor during the experiments.

1st column: Timestamps in Unix system (ms)

2nd-4th columns: Accelerometer data in the 3 axis (m/s^2)

7th and 8th columns: Skin Conductance (uS) and Skin Resistance (kOhms)

9th-11th columns: Gyroscope data in the 3 axis (deg/s)

12th-14th columns: Magnetometer data in the 3 axis (local_flux)

15th column: Photoplethysmography data (mV)

* HMDgaze.zip contains a set of 36 .csv files, one for each participant.

1st column: Frame number from the experiment application

3rd column: Log timestamp in Varjo system (mS)

4th and 5th columns: Headset position vector and rotation

6th column: Status of the gaze data captured (VALID or INVALID)

7th and 8th columns: Combined gaze forward vector and position of both eyes

9th column: Inter-pupillary distance (mm)

10th-15th columns: Eye data validity, forward vector, position vector, pupil/iris diameter ratio, pupil diameter (mm) and iris diameter (mm) for the left eye

16th-21st columns: Same data but for the right eye

22nd column: Estimated distance at which the user is focusing their gaze (capped at 2 meters)

23rd column: Estimation of how focused was the gaze of the user (from 0 to 1)

* Varjogaze.zip contains a set of 35 .csv files. One of the participants was not registered during the experiment due to technical issues.

These files contain similar information regarding gaze, including Unix-system timestamps. These are the log files obtained automatically from the VarjoBase application. Further information can be found in the Varjo documentation.

The *questionnaires* folder contains .zip files named *SSQ*, *NASA_TLX* and *Demographic*.

* SSQ.zip contains 72 files (2 per participant)

Shortened Sickness Questionnaires prompting about General discomfort, Headache, Eye strain and Nausea before and after the experiment

Possible answers: Absent, Mild, Moderate, Severe

* NASA_TLX.zip contains 108 files (3 per participant)

NASA TLX questionnaire prompting about cognitive load perceived for the main visual task, the secondary auditory task, and the combination of both

Possible answers: 1 to 20 for each category

* Demographic.zip contains 36 files, one for each participant

Demographics questionnaire prompting about personal data like age, sex, gender or languages spoken; conditions like visual impairements, auditory impairements or heart conditions; and habits like videogame or VR experience, day-to-day multitasking or average media speed consumption.

Data is partially anonymized to follow the ethics regulation of the Comité de Ética de la Investigación de la Comunidad Autónoma de Aragón (CEICA).

The *trial_data.zip* file contains 36 .csv files, one for each participant.

Each row of a file contains data on a particular object find during the experiment (a trial).

1st column: Condition of the trial. 5 - Relaxation, 0 - Low Cognitive Load 90º, 1 - High Cognitive Load 90º, 2 - Low Cognitive Load 360º, 3 - High Cognitive Load 360º

3rd and 4th columns: Start and end timestamps of the trial in Unix system

5th column: Whether the object was actually found (1 - yes, 0 - no)

These can be used to compute the start and end of each condition segment (start of the first trial - end of the last trial)

The *controller_data.zip* file contains 36 .csv files, one for each participant.

Each row represents a button A press from the user, holding its Unix system timestamp.

This can be used together with the *numberTimestamps.csv* file to compute ratios on secondary task performance. The latter file contains the information in seconds of when each number appears from the start of the audio, which can be compared with the button press timestamps to obtain reaction times.

---
