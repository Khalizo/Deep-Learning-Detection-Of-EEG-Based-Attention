This README.txt file was generated on 2020-04-04 by MARIO A MORENO ROCHA

GENERAL INFORMATION

1. Title of Dataset: INSTRUMENTED DIGITAL AND PAPER READING DATASET

2. Author Information
	A. Principal Investigator Contact Information
		Name: MARIO A MORENO ROCHA
		Institution: SACHI LAB, UNIVERSITY OF ST ANDREWS, ST ANDREWS, SCOTLAND, UK
		Address: SCHOOL OF COMPUTER SCIENCE, JACK COLE BUILDING, NORTH HAUGH, ST ANDREWS, FIFE KY16 9SX, SCOTLAND, UK
		Email: mamr3@st-andrews.ac.uk

	B. Associate or Co-investigator Contact Information
		Name: DR MIGUEL A NACENTA 
		Institution: UNIVERSITY OF VICTORIA, BRITISH COLUMBIA, CANADA 
		Address: 3800 FINNERTY ROAD, VICTORIA BC, V8P 5C2, CANADA
		Email: nacenta@uvic.ca

	C. Alternate Contact Information
		Name: DR JUAN YE
		Institution: SCHOOL OF COMPUTER SCIENCE, UNIVERSITY OF ST ANDREWS, ST ANDREWS, SCOTLAND, UK
		Address: SCHOOL OF COMPUTER SCIENCE, JACK COLE BUILDING, NORTH HAUGH, ST ANDREWS, FIFE KY16 9SX, SCOTLAND, UK
		Email: jy31@st-andrews.ac.uk

3. Date of data collection: AUGUST AND SEPTEMBER, 2019.  PREPROCESSING DURING OCTOBER, 2019   

4. Geographic location of data collection: ST ANDREWS, FIFE, SCOTLAND, UK 

5. Information about funding sources that supported the collection of the data: This work was supported by the University of St Andrews.


SHARING/ACCESS INFORMATION

1. Licenses/restrictions placed on the data: c) Creative Commons — Attribution 4.0 International — CC by 4.0

2. Links to publications that cite or use the data: 

3. Links to other publicly accessible locations of the data: Inactive DOI: https://doi.org/10.17630/80f522b6-6d23-4751-9023-21a1e3d0eb5a

4. Links/relationships to ancillary data sets: N/A

5. Was data derived from another source? NO

6. Recommended citation for this dataset: "Moreno Rocha, M. A., Nacenta, M., McCaffery, W., Ye, J., Lei, Y., Zhiping, W., 2019, Instrumented Digital and Paper Reading (dataset). Dataset. University of St Andrews Research Portal. https://doi.org/10.17630/80f522b6-6d23-4751-9023-21a1e3d0eb5a" 


DATA & FILE OVERVIEW

1. File List: 

THE PRESENT DATASET CONTAINS THREE FOLDERS:

i. DEMOGRAPHIC AND ANNOTATION DATASET: this .xlsx spreadsheet contains the relevant demographic data for all 25 participants in our study.  Also, it includes the participant evaluation for every paragraph read during our experiment for three factors: Interest, Attentiveness and Effort.  Those values are important to correlate with the Flesch–Kincaid readability score.  Please refer to the paper for more details.

ii. EXPERIMENT DATASET: the folder contains all the data collected during our experiments.  There were 25 participants, each one with the data obtained during 16 readings in our tests, organised in consecutive folders.  Each folder contains the data generated through the readings of two apparatus used in our study, an Eye-tracking and an EEG helmet.  Video feed has not been included as the dataset is anonymised.        

iii. OPENFACE DATASET: this folder includes, amongst other data, the HOG files obtained through the processing of the participant's videos, (not included) using OpenFace, a Python and Torch implementation of face recognition with deep neural networks (https://cmusatyalab.github.io/openface/#openface).  The histogram of oriented gradients (HOG) is a feature descriptor used in computer vision and image processing for the purpose of object detection. 

2. Relationship between files, if important: all three folders contain information derived from the same data collection from our experiments.  The first two folders contain the original, organised data collected, processed to obtain the different values for each paragraph (Interest, Attentiveness and Effort), whereas the third one contains data pre-processed with OpenFace. 

3. Additional related data collected that was not included in the current data package: neither dataset contains the videos of the participants in our tests collected as this dataset is the anonymised version of the data.

4. Are there multiple versions of the dataset? No.
	

METHODOLOGICAL INFORMATION

1. Description of methods used for collection/generation of data: 

During our experiments, the experimenter asked participants to read a series of one-page documents written in English in a way consistent with how they would read texts for academic purposes; i.e., reading for comprehension.  Participants had to signal to the experimenter when they had finished to read the document.  At that point, they walked to a nearby table to finish a questionnaire, in which they rated each paragraph of the document they had just read in terms of how interesting they found the paragraph (Interest), how much attention they were paying to it (Attentiveness), and how hard the paragraph was to read (Effort).  More information, along with the detailed script of the testing, could be found in the paper.

2. Methods for processing the data: 

A succinct recollection of the methods used were:

i. ORGANISATION: the original collected data were kept organised in folders.  Duplicate files, test files and redundant data were deleted and the final folder organisation was created.

ii. ANNOTATION: during the tests, the participant filled in forms in which they could evaluate every paragraph of the 16 readings made.  Those annotations had to be filled in in the dataset as a separated, off-line process.  The complied data is present at the DEMOGRAPHIC AND ANNOTATION DATASET, while the resulting data are in the EXPERIMENT DATASET folders.

iii. HOG PROCESSING: later on, we processed the the 400 videos generated during the tests (that is, 25 participants, each one with 16 videos of the participant reading).  We used OpenFace to obtain multiple data points form the participants' faces and the HOG files described beforehand.

3. Instrument- or software-specific information needed to interpret the data: 

i. DEMOGRAPHIC AND ANNOTATION DATASET: 

*.xlsx: for this, you can use Microsoft Excel (or any other spreadsheet, as Apple Numbers) to open this file.  No special libraries required.

ii. EXPERIMENT DATASET: this dataset contains a number of files.  You can use the following software to interpret the data:

*.json: these files could be open with any .txt editor (such as TextEdit).  We normally used Microsoft Visual Studio 2019 on Windows to open and analyse the files.

*.cvs: again, you can use Microsoft Excel (or any other spreadsheet) to open and use this file.  you can use Microsoft Excel (or any other spreadsheet) to open and use this file.  We used IBM SPSS Statistics 26 to analyse these files.

*.txt: these files could be open with any .txt editor (such as TextEdit).    

iii. OPENFACE DATASET: again, this dataset contains a number of files.  You can use the following software to interpret the data:

*.ini: this is a initialisation file for Windows or MS-DOS. Such files are plain text files that contain settings that dictate how a program—should operate.  You can use Notepad++ to open and visualise this file.

*.txt: these files could be open with any .txt editor (such as TextEdit). 

*.csv: you can use Microsoft Excel (or any other spreadsheet) to open and use this file.  We used IBM SPSS Statistics 26 to analyse these files.

*.hog: to interpret the .hog files, OpenFace provides a Mathworks MATLAB script.  We used MATLAB_R2019b Update 4 to work these files.  The HOG features are written as a binary file in the dataset and can be read in using the ./matlab_runners/Demos/Read_HOG_files.m script to Matlab.  See ./matlab_runners/Demos/feature_extraction_demo_vid.m 
for an example. Once the script is finished, the HOG features are stored in hog_data variable 

For a more detailed explanation, go to: https://github.com/TadasBaltrusaitis/OpenFace/tree/master/matlab_runners

4. Standards and calibration information, if appropriate: the main apparatus for the data collection were the eye tracking and the EEG helmet.  Here are the calibration information for these:

EYE TRACKING: we used the Tobii AB eyeX gaze tracker.  For each reading, the participant had to calibrate the eyetracking apparatus every time (16 times for participant).  In this way we could assure that the readings were exact.  We developed a Microsoft Visual Studio 2019 on Windows software which collected all the data.  For the calibration, we used the two step process built within the hardware.

EEG: we used the Neurolectrics Enobio 8, an eight-channel, wireless EEG helmet.  We devised and created our own helmet using the International 10-20 scalp electrode placement system.  Throughout the experiment, we calibrate the EEG for three two-minute pauses.  

For the experiments, we used the following electrode position:

Channel Position1 	Fp12 	Fp23 	Fz4 	Cz5 	PO76 	O17 	O28 	PO8A1 	Left earA2 	Right ear  

You can read our paper for more information.  

5. Environmental/experimental conditions: the experiment took place in a room with two desks and two main stations, the researcher (PC computer with a monitoring screen) and the participant station (big screen with the Tobbi eye tracking, a video camera and the Neurolectrics EEG helmet on the participant).  

PRECONDITIONS FOR THE EXPERIMENT:
i. The 0.30 room has to be clean and uncluttered from anything but the required instruments and equipment for the experiments.ii. On the adjacent desk there must be pens and a cup of water for the participant.iii. All documents required for the experiment must be on the file cabinet provided (described on the paper).iv. The researcher must be present 15 minutes before the arrival of the participant.v. EEG must be charged (at least 80%). Main computer must be switched on and plugged in as well.

POSTCONDITIONS FOR THE EXPERIMENT:

i. An incident logbook must be filled in.ii. All generated documents (Participant Information, Consent Forms, reading printouts, etc) must be filled in the File cabinet provided.iii. Make sure all the files from the experiment were recorded and saved accordingly.iv. Back up information every day.v. Leave the laboratory set up ready for the next experiment.

For detailed conditions, as well as the placement of the equipment, you can consult our paper.

6. Describe any quality-assurance procedures performed on the data: we revised the completeness of the data when we did the ANNOTATION process (described above).  Also, we revised several times the size and number of files present on the folders. Also, we checked randomly several participant's folders and everything was in place.    

7. People involved with sample collection, processing, analysis and/or submission: apart from MARIO A MORENO ROCHA, Dr MIGUEL A NACENTA, my supervisor, followed closely all the process described here.


DATA-SPECIFIC INFORMATION FOR: 

i. DEMOGRAPHIC AND ANNOTATION DATASET [USERS 001-025.XLSX]

This Microsoft Excel file contains all the demographic information that the participant gave at the beginning of the experiment.  Also, you can find the annotation for every paragraph the participant read during the experiment.  

1. Number of variables: 17

2. Number of cases/rows: 2001

3. Variable List: 

There are 80 records for each participant (that is, 16 documents, five paragraphs each, 80 records):

1. PARTICIPANTID: participant unique identifier, a consecutive number, from User001 up to User025.  	
2. PARTICIPANTAGE: participant age, in years.
3. PARTICIPANTSEX: participant sex, either Male or Female, as specified by the participant.  
4. PARTICIPANTEDUCATIONLEVEL: participant education level, from the following series: [No formal qualifications; Undergraduate degree (BA/BSc/other); College/A levels, Secondary school/GCSE; Graduate degree (MA/MSc/MPhil/other); Doctorate degree (PhD/MD/other)].
5. PARTICIPANTACADEMICAREA: participant academic area, from the following series: [Social Sciences (as in Anthropology, Economics, Human Geography, Law, Political Science, Psychology, Sociology); Natural Sciences (as in Biology, Chemistry, Earth Sciences, Space Sciences, Physics); Formal Sciences (as in Computer Science, Mathematics, Statistics); Applied Sciences (as in Engineering and Technology, Medicine and Health); Other].	
6. PARTICIPANTMOTHERTONGUE: participan mother tongue, as single language as specified by the participant.	
7. PARTICIPANTREADINGHOURS: the number of hours the participant stated read weekly on academic proposes.  	
8. DOCUMENTID: the document unique identifier.  It contains three letters: [I as in Interesting, B as in Boring; E as an Easy document or D as a Difficult document (according the Flesch–Kincaid readability score); and T as Technology related document or S as in a Social Sciences document] and a consecutive number [from 00 up to 15].   
9. DOCINTEREST: document interest, either [Interesting; Boring] as described before.  Those values were assigned to each document by the researchers.  More details on the paper.
10. DOCDIFFICULTY: document difficulty, either [Easy; Difficult], according to the Flesch–Kincaid readability score.  The score values were set as < 12 considered Easy and >14 considered Difficult. 
11. DOCTOPICAREA: document topic area, either [Technology; Social Sciences].	
12. DOCFLESCHKINCAID: the Flesch–Kincaid readability score of the document.  
13. PAPERORDIGITAL: paper or digital, if the document read was on screen (Digital) or printed (Paper).
14. PARAGRAPHID: paragraph number, from [0 .. 4].  All documents had five paragraphs.
15. INTEREST: the paragraph interest rated by the participant, [1..5], in which 1 is low and 5 is high.
16. ATTENTIVENESS: the paragraph attention required, rated by the participant, [1..5], in which 1 is low and 5 is high.
17. EFFORT: the effort the participant needed to read the paragraph, as rated by the participant, [1..5], in which 1 is low and 5 is high.

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


ii. EXPERIMENT DATASET/EXPERIMENT ANONYMISED VERSION

USER001_GROUP_TEST_30-08-2019--10-07-00 [TESTLIST.JSON]	

This .json file contains the concentrated information for all the files used for the reading tests of one users.  It contains the detailed path of the files used and those generated as well.  This file is required for the ANNOTATION of the files.

1. Number of variables: 7

2. Number of cases/rows: 16

3. Variable List: 

This is the description of the 7 variables found in one user, and also, repeated for the 25 users:

1. ISPAPER: this variable describes if the reading was made on Paper or Digital (on screen).  The possible answers are into the following series" [TRUE,FALSE].
2. INDEX: this value is invariably 0.
3. NAME: name of the reading file, from this series: [IET_00, BET_01, IDT_02, BDT_03, IES_04 , BES_05, IDS_06, BDS_07, IET_08, BET_09, IDT_10, BDT_11, IES_12, BES_13, IDS_14, BDS_15]
4. STIMULIPATH: the path in which the document was located during the experiment, e.g.:"C:\\MMAD\\TESTGROUPS\\GROUP_TEST\\IET_00.RTF".
5. USERID: the participant unique identifier, from this series: [USER001 .. USER025].
6. TESTDIR: the path in which the data was saved during the experiment, e.g.: "C:\\MMAD\\SUBJECTS\\USER001_GROUP_TEST_30-08-2019--10-07-00\\USER001_TEST0_IET_00_30-08-2019".
7. NUMRECORDINGS: number of video recordings made, this number was invariably 1.

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001_GROUP_TEST_30-08-2019--10-07-00 [USER001_GROUP_TEST_30-08-2019--10-0700_U1567156023_BASELINE0_EEG_RAWEEGDATA.CSV]

This .CSV file contains the raw EEG reading data collected while the participant was on an idle position, as part of the needed calibration.  This file is repeated three times (at the beginning of the test, after eight documents read, and finally at the end of the 16 documents read).  This data is collected as a baseline information to compare with other EEG readings.

1. Number of variables: 10

2. Number of cases/rows: 24093

3. Variable List: 

1. C1: raw EEG data collected though channel 1 (Fp1), e.g., 134335.9688									2. C2: raw EEG data collected though channel 2 (Fp2), e.g., 60980.51563
3. C3: raw EEG data collected though channel 3 (Fz), e.g., 186279.8438
4. C4: raw EEG data collected though channel 4 (Cz), e.g., 44292.74219
5. C5: raw EEG data collected though channel 5 (PO7), e.g., 134157.9063
6. C6: raw EEG data collected though channel 6 (O1), e.g., 109575.2813	
7. C7: raw EEG data collected though channel 7 (O2), e.g., 130719.1484
8. C8: raw EEG data collected though channel 8 (PO8), e.g., 174432.4375
9. TIMESTAMP: timestamp of the collection of data from Windows 10, e.g., 573601.3592	 
10. ADJUSTEDUNIX: an adjusted timestamp from the computer clock, e.g., 1567155485

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001_TEST0_IET_00_30-08-2019 [USER001INFO.TXT]

This .TXT file contains the identifier of the participant and its test.

1. Number of variables: 2

2. Number of cases/rows: 1

3. Variable List: 

1. USER001: the participant unique identifier, from this series: [USER001 .. USER025].
2. GROUP_TEST: the reading group used for the test.  This will be invariably GROUP_TEST.

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001_TEST0_IET_00_30-08-2019 [RECORDINGLIST.JSON]

This .JSON file includes the information regarding the processing of the participant's reading data collected, along with the complete path for the files during the test.  These files were produced as part of the preprocessing for the ANNOTATION.  Every similar folder has its own.

1. Number of variables: 8  

2. Number of cases/rows: 1

3. Variable List: 

1. ISPAPER: this variable indicate if the test was conducted in paper (TRUE) or digitally on screen (FALSE): [TRUE; FALSE].
2. ISCALIBRATED: this indicate that the reading test was eye tracking calibrated.  This is invariably TRUE.
3. DATADIR: the complete path directory of the files recorded for the test, e.g.: "C:\\MMAD\\SUBJECTS\\USER001_GROUP_TEST_30-08-2019--10-07-00\\USER001_TEST0_IET_00_30-08-2019\\USER001_TEST0_IET_00_30-08-2019_RECORDING0",
4. USERID: the participant unique identifier, from this series: [USER001 .. USER025].
5. TESTNAME: name of the reading file, from this series: [IET_00, BET_01, IDT_02, BDT_03, IES_04 , BES_05, IDS_06, BDS_07, IET_08, BET_09, IDT_10, BDT_11, IES_12, BES_13, IDS_14, BDS_15]
6. VIDEOQPCSTARTTIME: start timestamp from the video recording (not present at this dataset).  E.g, 837197.0,
7. VIDEOQPCENDTIME": end timestamp from the video recording (not present at this dataset).  E.g,896228.0,
8. INDEX: this value is invariably 0. 

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001_TEST0_IET_00_30-08-2019_RECORDING0 [ANNOTATIONS.JSON]

This .JSON file contains the annotation areas created according to the eye tracking collected data.  Then, every area of focus and gaze recorded turned into a polygon to be then annotated.  These are the polygon areas and its annotations.  Remember, all documents had five paragraphs.  Further information on the paper. 

1. Number of variables: 9

2. Number of cases/rows: 5

3. Variable List: 

1. USER: the participant unique identifier, from this series: [USER001 .. USER025].
2. TEST: name of the reading file, from this series: [IET_00, BET_01, IDT_02, BDT_03, IES_04 , BES_05, IDS_06, BDS_07, IET_08, BET_09, IDT_10, BDT_11, IES_12, BES_13, IDS_14, BDS_15]
3. POINTS: the polygon position points for the paragraph.  In this case it was: [ "X 659 Y 138", "X 1256 Y 137", "X 1254 Y 227", "X 659 Y 234"]
4. NAME: the paragraph number, form this series: [PARAGRAPH 0 .. PARAGRAPH 5].
5. INTEREST: the participant evaluation of the paragraph according on how interesting the found the reading.  Values are [1..5], in which 1 is low and 5 is high.
6. ATTENTIVENESS: the participant evaluation of the paragraph according on how attentive participant were during the reading.  Values are [1..5], in which 1 is low and 5 is high.
7. EFFORT: 1, the participant evaluation of the paragraph according on how much effort he put to understand the reading.  Values are [1..5], in which 1 is low and 5 is high.
8. TIMERANGESTART: start timestamp from the video recording (not present at this dataset).  E.g,837197.0
9. TIMERANGEEND: end timestamp from the video recording (not present at this dataset).  E.g., 844019.0

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A
 

USER001_TEST0_IET_00_30-08-2019 [META.TXT]

A .TXT file containing the information for the participant reading test, for quality assurance proposes.

1. Number of variables: 6

2. Number of cases/rows: 1

3. Variable List: 

1. CURRENT USER: the participant unique identifier, from this series: [USER001 .. USER025].
2. CURRENT USER: the reading group used for the test.  This will be invariably GROUP_TEST.
3. TEST NAME: name of the reading file, from this series: [IET_00, BET_01, IDT_02, BDT_03, IES_04 , BES_05, IDS_06, BDS_07, IET_08, BET_09, IDT_10, BDT_11, IES_12, BES_13, IDS_14, BDS_15]
4. TEST NUMBER: test number, form the following series: [0..14]
5. TEST MEDIUM: this variable describes if the reading was made on Paper or Digital (on screen).
6. ORIGINAL TEST PATH: complete path in which the document read was located in the computer during the tests.  E.g., C:\MMAD\TESTGROUPS\GROUP_TEST\IET_00.RTF
7. ORIGINAL GROUP PATH: complete path in which the document group read was located in the computer during the tests.  E.g., C:\MMAD\TESTGROUPS\GROUP_TEST

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001_TEST0_IET_00_30-08-2019 [USER016D_TEST7_BDS_07_05-09-2019_RECORDING0_U1567705699_EEG_RAWEEGDATA.CSV]

Same description as the [USER001_GROUP_TEST_30-08-2019--10-0700_U1567156023_BASELINE0_EEG_RAWEEGDATA.CSV] above.  This time, the .CSV file contains the raw EEG reading data collected while the participant was reading a document. This file is repeated 16 times per user (one every document read during the test).


USER001_TEST0_IET_00_30-08-2019 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_CLEANFIXATIONDATA.CSV]

This .CSV file contains the eye tracking clean fixation data from the participant reading a document. It includes the Begin, Data and End of the data stream generated. 

1. Number of variables: 5

2. Number of cases/rows: 2968

3. Variable List: 

1. STREAM: the different states of the data stream, from the following series: [Begin; Data; End]. 	
2. X: coordinates point on the X axis. E.g., 1178.475.	
3. Y: coordinates point on the Y axis. E.g., 208.3219.
4. LSLTIMESTAMP: start timestamp from the data stream data recording.  E.g.,838847.2.	
5. ADJUSTEDUNIX: end timestamp from the data stream data recording, from the computer clock. E.g.,1567155510.

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A

	
USER001_TEST0_IET_00_30-08-2019 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_RAWFIXATIONBEG.CSV]

This .CSV file contains the eye tracking raw fixation data from the beginning of the test in which the participant was reading a document. This file is repeated 16 times per user (one every document read during the test).

1. Number of variables: 6

2. Number of cases/rows: 152

3. Variable List: 

1. DATATYPE: the state of the beginning of the data stream.  This value is invariably Begin.	
2. X: coordinates point on the X axis. E.g.,1178.475514
3. Y: coordinates point on the Y axis. E.g.,208.3219253 
4. DEVICETIMESTAMP: the time stamp generated by the Tobii AB eyeX gaze tracker. E.g., 1474472.86206263	 
5. LSLTIMESTAMP: start timestamp from the beginning of data stream data recording.  E.g. 838847.176937
6. ADJUSTEDUNIX: start timestamp from the data stream data recording, from the computer clock. E.g.1567155510

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001_TEST0_IET_00_30-08-2019 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_RAWFIXATIONDAT.CSV]

Same description as the [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_RAWFIXATIONBEG.CSV] above.  This time, the .CSV file contains the clean eye tracking data stream collected while the participant was reading a document. This file is repeated 16 times per user (one every document read during the test).


USER001_TEST0_IET_00_30-08-2019 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_RAWFIXATIONEND.CSV]

Same description as the [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_RAWFIXATIONBEG.CSV] above.  This time, the .CSV file contains the end of the clean eye tracking data stream collected while the participant was reading a document. This file is repeated 16 times per user (one every document read during the test).


USER001_TEST0_IET_00_30-08-2019 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_EYETRACKER_RAWGAZEDATA.CSV]

This .CSV file contains the eye tracking raw gaze data from the test in which the participant was reading a document. This file is repeated 16 times per user (one every document read during the test).

1. Number of variables: 5

2. Number of cases/rows: 3443

3. Variable List: 

1. X: coordinates point on the X axis. E.g.,848.7473279
2. Y: coordinates point on the Y axis. E.g.,190.8110353 
3. DEVICETIMESTAMP: the time stamp generated by the Tobii AB eyeX gaze tracker. E.g.,1472807.464
4. LSLTIMESTAMP: start timestamp from the beginning of data stream data recording.  E.g., 837151.9355
6. ADJUSTEDUNIX: start timestamp from the data stream data recording, from the computer clock. E.g., 1567155509

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


iii. OPENFACE DATASET/OPENFACE ANONYMISED VERSION

[DESKTOP.INI]

This .INI file is a file extension for an initialisation file format, used by Microsoft Windows and created by OpenFace while processing the videos (not present in this dataset).  INI files are plain text (ASCII) and are used to set parameters for the operating system and some programs. In Windows, two common INI files are SYSTEM. 

1. Number of variables: 400

2. Number of cases/rows: 1

3. Variable List: 

1. LOCALIZEDFILENAMES: contains the complete path for the 400 videos processed by OpenFace.  E.g., User002_test0_IET_00_30-08-2019_recording0_U1567167152_VIDEO__Q998238_Q1073712.avi=@User002_test0_IET_00_30-08-2019_recording0_U1567167152_VIDEO__Q998238_Q1073712.avi,0.

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001 [DESKTOP.INI]

This .INI file is a file extension for an initialisation file format, used by Microsoft Windows and created by OpenFace while processing the videos (not present in this dataset).  INI files are plain text (ASCII) and are used to set parameters for the operating system and some programs. In Windows, two common INI files are SYSTEM. 

For more information, go to: https://github.com/TadasBaltrusaitis/OpenFace/blob/master/README.md

1. Number of variables: 1

2. Number of cases/rows: 1

3. Variable List: 

1. INPUT: the complete path of the input video file processed by OpenFace.  E.g., C:\MMAD\SUBJECTS\USER001_GROUP_TEST_30-08-2019--10-07-00\USER001_TEST0_IET_00_30-08-2019\USER001_TEST0_IET_00_30-08-2019_RECORDING0\USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.WMV
2. INPUT FULL PATH:C: the complete path of the output files processed by OpenFace.  E.g.,\MMAD\SUBJECTS\USER001_GROUP_TEST_30-08-2019--10-07-00\USER001_TEST0_IET_00_30-08-2019\USER001_TEST0_IET_00_30-08-2019_RECORDING0\USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.WMV
3. CAMERA PARAMETERS:standard camera parameters.  E.g., 250,250,160,120
4. OUTPUT HOG:the complete path of the HOG file processed by OpenFace. E.g.,USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.HOG
5. OUTPUT VIDEO: the complete path of the video file processed by OpenFace (not present at this dataset).  E.g., USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.AVI
6. OUTPUT ALIGNED DIRECTORY: the complete path of the aligned directory processed by OpenFace. USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228_ALIGNED
7. OUTPUT CSV: the complete path of the CSV file processed by OpenFace. E.g,USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.CSV
8. GAZE: gaze value used.  E.g, 1
9. AUS: aus value used.  E.g., 1
10. LANDMARKS 2D: two dimension landmarks used.  E.g., 1
11. LANDMARKS 3D: three dimension landmarks used.  E.g.,1
12. POSE: number of poses detected.  E.g., 1
13. SHAPE PARAMETERS: shape parameters used.  E.g., 1

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.CSV]

The two projects that process data are FaceLandmarkImg and FeatureExtraction and their output is explained in detail in this page. FaceLandmarkImg is intended for individual images and FeatureExtraction for sequence (image sequence/webcam/video) analysis that contain a single face, while FaceLandmarkVidMulti is intended for sequences containing multiple faces. Their output format is the same.

For more information go to: https://github.com/TadasBaltrusaitis/OpenFace/wiki/Output-Format

1. Number of variables: 714

2. Number of cases/rows: 1560

3. Variable List: (from the OpenFace Output Format):

BASIC

frame the number of the frame (in case of sequences)

face_id the face id (in case of multiple faces), there is no guarantee that this is consistent across frames in case of FaceLandmarkVidMulti, especially in longer sequences

timestamp the timer of video being processed in seconds (in case of sequences)

confidence how confident is the tracker in current landmark detection estimage

success is the track successful (is there a face in the frame or do we think we tracked it well)

GAZE RELATED

gaze_0_x, gaze_0_y, gaze_0_z Eye gaze direction vector in world coordinates for eye 0 (normalized), eye 0 is the leftmost eye in the image (think of it as a ray going from the left eye in the image in the direction of the eye gaze)

gaze_1_x, gaze_1_y, gaze_1_z Eye gaze direction vector in world coordinates for eye 1 (normalized), eye 1 is the rightmost eye in the image (think of it as a ray going from the right eye in the image in the direction of the eye gaze)

gaze_angle_x, gaze_angle_y Eye gaze direction in radians in world coordinates averaged for both eyes and converted into more easy to use format than gaze vectors. If a person is looking left-right this will results in the change of gaze_angle_x (from positive to negative) and, if a person is looking up-down this will result in change of gaze_angle_y (from negative to positive), if a person is looking straight ahead both of the angles will be close to 0 (within measurement error).

eye_lmk_x_0, eye_lmk_x_1,... eye_lmk_x55, eye_lmk_y_1,... eye_lmk_y_55 location of 2D eye region landmarks in pixels. The landmark index can be found below

eye_lmk_X_0, eye_lmk_X_1,... eye_lmk_X55, eye_lmk_Y_0,... eye_lmk_Z_55 location of 3D eye region landmarks in millimeters.

POSE

pose_Tx, pose_Ty, pose_Tz the location of the head with respect to camera in millimeters (positive Z is away from the camera)

pose_Rx, pose_Ry, pose_Rz Rotation is in radians around X,Y,Z axes with the convention R = Rx * Ry * Rz, left-handed positive sign. This can be seen as pitch (Rx), yaw (Ry), and roll (Rz). The rotation is in world coordinates with camera being the origin.

Lines in au intensities and au occurrences correspond to predicted Action Unit presence and intensities respectively. For more details see here

Where the landmarks are no longer in pixel values but in millimetres and we also report head pose and gaze (this however needs accurate estimates of fx,fy,cx,cy. This functionality is useful for batch image processing where the camera is the same and we want to know pose and gaze.

LANDMARKS LOCATIONS IN 2D

x_0, x_1, ... x_66, x_67, y_0,...y_67 location of 2D landmarks in pixels, the landmark index can be seen below

LANDMARKS LOCATIONS IN 3D

X_0, ... X_67, Y_0,...Y_67, Z_0,...Z_67 location of 3D landmarks in millimetres, the landmark index can be seen below. For this to be accurate need to have good estimates for fx,fy,cx,cy

RIGID AND NON-RIGID SHAPE PARAMETERS

Parameters of a point distribution model (PDM) that describe the rigid face shape (location, scale and rotation) and non-rigid face shape (deformation due to expression and identity). For more details look at chapter 4.2 of my Thesis for more details.

p_scale, p_rx, p_ry, p_rz, p_tx, p_ty - scale, rotation and translation terms of the PDM

p_0, p_1, ... p_33 - non-rigid shape parameters

FACIAL ACTION UNITS

Facial Action Units (AUs) are a way to describe human facial expression, more details on Action Units can be found here

Note that AUs are most accurate in videos of one person if there is a range of expressions observed, they are not as accurate with FaceLandmarkImg and FaceLandmarkVidMulti

The system can detect the intensity (from 0 to 5) of 17 AUs:

AU01_r, AU02_r, AU04_r, AU05_r, AU06_r, AU07_r, AU09_r, AU10_r, AU12_r, AU14_r, AU15_r, AU17_r, AU20_r, AU23_r, AU25_r, AU26_r, AU45_r

And the presense (0 absent, 1 present) of 18 AUs:

AU01_c, AU02_c, AU04_c, AU05_c, AU06_c, AU07_c, AU09_c, AU10_c, AU12_c, AU14_c, AU15_c, AU17_c, AU20_c, AU23_c, AU25_c, AU26_c, AU28_c, AU45_c

4. Missing data codes: No data is missing in this dataset.

5. Specialised formats or other abbreviations used: N/A


USER001 [USER001_TEST0_IET_00_30-08-2019_RECORDING0_U1567156289_VIDEO__Q837197_Q896228.HOG]

To interpret these .hog files, OpenFace provides a Mathworks MATLAB script.  We used MATLAB_R2019b Update 4 to work these files.  The HOG features are written as a binary file in the dataset and can be read in using the ./matlab_runners/Demos/Read_HOG_files.m script to Matlab.  
See ./matlab_runners/Demos/feature_extraction_demo_vid.m  for an example. Once the script is finished, the HOG features are stored in hog_data variable 

For a more detailed explanation, go to: https://github.com/TadasBaltrusaitis/OpenFace/tree/master/matlab_runners
It is also possible to control the size of the similarity aligned faces, using the -simsize <pixel width and height> and -simscale <scale> command line arguments, you can get the following results:

Default parameters - size 112 and scale 0.7

For more information go to: https://github.com/TadasBaltrusaitis/OpenFace/wiki/Output-Format and https://github.com/TadasBaltrusaitis/OpenFace/wiki/Command-line-arguments.

*** EOF ***












