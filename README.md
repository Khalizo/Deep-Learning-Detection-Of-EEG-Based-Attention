
# Deep learning model for EEG-based attention detection

Full report can be found [here]("Dissertation_Final.pdf")

## Abstract

Attention is at the core of neurological/cognitive functions, and deficits in attention have been linked to Alzheimer's disease (AD), Attention deficit hyperactivity disorder (ADHD), Traumatic Brain Injuries (TBI) and Posttraumatic Stress Disorder (PTSD). ADD can have severe consequences on a student's learning efficacy if it goes untreated. Traditionally, detecting inattentiveness is commonly done by observing an individual's expressions. However, this method is often inaccurate and increases the burden on teachers.

Interestingly, the detection of human attention levels can be automated with the use of deep learning (DL). Electroencephalography (EEG) signals provide a great source of information relating to human attention that can be analysed by deep learning algorithms. 

As a result, this study a novel deep learning architecture for EEG-based attention detection that builds upon the current state-of-the-art. The model predicted scores for attention, interest and effort on EEG data set of 18 users. Intra- and inter-subject classification results were evaluated using five-fold cross-validation. Results showed that the proposed model outperformed
other deep learning and baseline models, where it was able to achieve an accuracy of 93% on a single user with binary classification

## EEG Dataset and Experimental Design

### Overview

For EEG-based attention, interest and effort classification, this study used the Instrumented Digital and Paper Reading dataset [1]. The dataset’s researchers gave 25 participants 16 readings with five paragraphs each and recorded their EEG signals while they were reading. The researchers used Neurolectrics2 Enobio 8, an eight-channel, wireless EEG helmet with a sampling frequency of 500hz (Figure 5). They created their helmet using the International 10-20 scalp electrode placement system. Throughout the experiment, they calibrated the EEG signals for three two-minute pauses.

[EEG_channels]("")

### Experimental Design
The experiment took place in a room with two desks and two main stations- the experimenter3 and the participant stations.

[Experiment_layout]("")

During the experiments, the experimenter asked participants to read a series of one-page documents written in English in a way consistent with how they would read texts for academic purposes; i.e.,reading for comprehension. Participants had to signal to the experimenter when they had finished reading the document. At that point, they walked to a nearby table to finish a questionnaire, in which they scored each paragraph of the document they had just read in terms of how interesting they found the paragraph (Interest), how much attention they were paying to it (Attention), and how hard the paragraph was to read (Effort).

### Dataset

The original dataset had 424 raw EEG data files that were generated from 25 participants. However, after cleaning the dataset, there were 18 users left with a total of 277 reading sessions.

[clean_dataset]("")

The EEG CSV files had ten columns: columns 1 – 8 represented the EEG signals from the eight channels while columns 9 & 10 were the timestamps and the adjusted UNIX timestamp in seconds. Each session had an associated JSON file that contained the start and end timestamps for each of the five paragraphs, along with their scores for attention, effort and interest.

## Data Pre-processing

The primary purpose of this study was to reduce the number of steps needed for EEG processing; hence the processing stage was kept to a minimum. However, based on the current literature [76], EEG processing steps such as bandpass filtering, window sampling and feature scaling were still necessary for effective DL- based analysis.

[workflow]()
 

## CNN-RNN Model Architecture

## Results

### Baseline Model performance

### Deep Learning Model performance

## Conclusions

## Usage





