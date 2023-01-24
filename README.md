
# Deep learning model for EEG-based attention detection

Full report can be found [here]("Dissertation_Final.pdf")

## Abstract

Attention is at the core of neurological/cognitive functions, and deficits in attention have been linked to Alzheimer's disease (AD), Attention deficit hyperactivity disorder (ADHD), Traumatic Brain Injuries (TBI) and Posttraumatic Stress Disorder (PTSD). ADD can have severe consequences on a student's learning efficacy if it goes untreated. Traditionally, detecting inattentiveness is commonly done by observing an individual's expressions. However, this method is often inaccurate and increases the burden on teachers.

Interestingly, the detection of human attention levels can be automated with the use of deep learning (DL). Electroencephalography (EEG) signals provide a great source of information relating to human attention that can be analysed by deep learning algorithms. 

As a result, this study a novel deep learning architecture for EEG-based attention detection that builds upon the current state-of-the-art. The model predicted scores for attention, interest and effort on EEG data set of 18 users. Intra- and inter-subject classification results were evaluated using five-fold cross-validation. Results showed that the proposed model outperformed
other deep learning and baseline models, where it was able to achieve an accuracy of 93% on a single user with binary classification

## EEG Dataset and Experimental Design

For EEG-based attention, interest and effort classification, this study used the Instrumented Digital and Paper Reading dataset [1]. The dataset’s researchers gave 25 participants 16 readings with five paragraphs each and recorded their EEG signals while they were reading. The researchers used Neurolectrics2 Enobio 8, an eight-channel, wireless EEG helmet with a sampling frequency of 500hz (Figure 5). They created their helmet using the International 10-20 scalp electrode placement system. Throughout the experiment, they calibrated the EEG signals for three two-minute pauses.

[EEG channel position]()


## CNN-RNN Model Architecture

## Results

### Baseline Model performance

### Deep Learning Model performance

## Conclusions

## Usage





