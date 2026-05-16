#### **1. TITLE:**  "*Distributed Edge-IoT Apparatus for Multi-Modal Physiological Diagnostics and Acoustic Signal Conditioning"*

#### 

#### **2. DESCRIPTION OF THE INVENTION:**

#### &#x20; 

##### **A. PROBLEM ADDRESSED BY THE INVENTION:**   



Current diagnostic systems are fragmented; existing systems focus on a single organ or disease. Standard systems (MRI, ECG, Spirometry) are both expensive and require physical presence at the clinic. Furthermore, Smartphone microphones are apt to environmental noise leading to inaccurate diagnosis. There is a critical research gap for the system  that combines both Active Hardware-Level Signal Isolation and Passive Continuous Monitoring to identify the interconnectedness of systemic health.



Current solutions face three primary challenges:



** Fragmentation:** Traditional voice-based tools focused on identifying a single disease (e.g., only Parkinson's), disregarding the coexisting of the relationship between the heart, lungs and brain.



** Environmental disturbance:** The microphones of smartphone capture unwanted noise and breathes leading to a disturbance in the data frequency (Jitter/Shimmer) which is necessary for medical data analysis.



** Data security:** Sending the audio data to the cloud for analysis proposes an important biometric privacy risk and due to network latency, it prevents real-time feedback.



##### **B. OBJECTIVE OF THE INVENTION:**



• Provide a single interface capable of detecting risks across three major physiological systems (neurological, respiratory, cardiovascular)

• Enable clinical-grade early screening using standard smartphone hardware without external sensors

• Implement local "edge" processing, ensuring sensitive medical voice data never leaves the user's device

• Detect sub-clinical vocal changes-invisible to the human ear-allowing for medical intervention years before physical symptoms manifest.





##### **C. STATE OF THE ART/ RESEARCH GAP/NOVELTY:  Describe your invention fulfil the research gap?**  

|**Sr. No.**|**Patent ID**|**Abstract**|**Research Gap**|**Novelty**|
|-|-|-|-|-|
|1|US9763617B2|<br />A system and a method for assessing a condition in a subject. Phones from speech of the subject are recognized, one or more prosodic or speech-excitation-source features of the phones are extracted, and an assessment of a condition of the subject, is generated based on a correlation between the features of the phones and the condition.<br />|Limited to stress; ignores mechanical lung efficiency.|Cross-domain correlation: maps vocal cord vibration to lung airflow.|
|2|US10010288B2|<br />Detection of neurological diseases such as Parkinson's disease can be accomplished through analyzing a subject's speech for acoustic measures based on human factor cepstral coefficients (HFCC). Upon receiving a speech sample from a subject, a signal analysis can be performed that includes identifying articulation range and articulation rate using HFCC and delta coefficients. A likelihood of Parkinson's disease, for example, can be determined based upon the identified articulation range and articulation rate of the speech.<br />|<br />Focuses solely on neurological motor decay.<br />|Integrated tri-system: combines motor-speech with respiratory and cardiac rhythm.|
|3|US20210298711A1|A mobile device application prompts and conducts audio and/or video tests using a microphone on a smartphone, tablet or laptop in order to record and analyze a patient's speech, cough, breathing and other sounds in order to diagnose the patient with Covid 19, another ailment, or as having normal ranges not indicative of disease. The mobile device's tests and protocols use program instructions, AI processing and other automated tools to facilitate the speed and reliability of the testing.|Reactive to acute illness; lacks chronic disease profiling.|Preventive scoring: designed for long-term chronic risk monitoring.|
|4|CN203555751U|The utility model discloses an abdominal bowel sound analyzer system based on time-frequency analysis, which uses a sound sensor to convert the bowel sound into an electrical signal, and then uses a preamplifier to amplify and a low-pass filter to filter out audio noise , using a high-precision acquisition module to convert it into a digital signal; finally, the CPU is used to analyze the characteristics of the digital signal, obtain the characteristic information and extract the number of bowel sounds, and then judge whether the patient is within the normal range or in a pathological state. Due to the analysis of the sampling instrument, the subjectivity of the doctor's judgment is overcome, the accuracy and efficiency of diagnosis are improved, and the workload of the doctor is reduced. At the same time, the utility model abdominal bowel sound analyzer system based on time-frequency analysis has the characteristics of small size, accurate detection and convenient operation.|<br />The existing bowel sound analyzer is limited to single-modality abdominal signal processing and lacks a hybrid framework for integrating continuous passive monitoring with high-fidelity active diagnostic sessions.<br />|<br />A Multi-Modal "Active-Passive" loop that uses a 3D-printed hardware shield for physical laminar flow rectification, enabling the synchronized fusion of neurological, respiratory, and cardiovascular biomarkers into a unified diagnostic score.<br />|



##### 

##### **D. DETAILED DESCRIPTION:**   



This system design represents a multi-stage method to diagnostic fidelity. By combining both physical signal conditioning with advanced machine learning, system extracts detailed medical data from common consumer devices.



1. **Hardware-level signal conditioning: The diagnostic shield:**



The key challenge in mobile diagnostics is "Acoustic Entropy", where surrounding noise and fluctuating waft screen insignificant health biomarkers. The diagnostic shield solves this physically rather than computer-based methods:



**• Rectifying Smoothing:** When user speaks or breathes into the device, the air is inherently chaotic. The internal Baffle Plates acts as streamlined "Straighteners", forcing the airflow into a smooth, orderly, and parallel movement.



**• Signal-to-Noise Enhancement:** By creating a filter chamber that blocks ambient noise (like background speech or surrounding noise) before it ever touches the microphone by ensuring that the raw signal entering the gateway is inherently cleaner.



**Evidence:** Fig1: Diagnostic Shield Internal Workflow, Fig2: Diagnostic Shield Setup Workflow



**2. The Edge Processing Gateway:**



Once the cleaned audio enters the mobile gateway, system employs Optimal Linear Filtering to perform final-stage adaptive noise cancellation. Unlike Noise reduction system, Optimal Linear Filtering continuously calculates the background noise floor and removes it from the signal, leaving only the clear audio or respiratory data. 



**Evidence:** Fig3: Wearable (Smartwatch) Device Workflow



**3. The Weighted Fusion Engine: Triple-stream Extraction:**



The main part of the invention is the CNN-LSTM (Convolutional Neural Network - Long Short-Term Memory) model. This model is excellent at identifying static patterns in the audio data, the LSTM allows this system to analyze timing and sequence of your audio over time.



** Stream 1: Neurological Health**



**Biomarkers:** Jitter (frequency variation) and Shimmer (amplitude variation)

**Diagnostic Awareness:** Detects the vocal tremors or unsteadiness in the audio data which is the early sign of neurological issues.



** Stream 2: Respiratory Issues**



**Biomarkers:** Spectral Centroid and Zero-Crossing Rate

**Diagnostic Awareness:** These indicators help to track airflow rate. A shift in the Spectral Centroid indicates a change in the lung volume helping to identify respiratory efficiency or obstruction 



** Stream 3: Cardiovascular stress**



**Biomarkers:** Speech tempo (pause density)

**Diagnostic Awareness:** The cardiovascular system directly affects the diaphragm and breath control which is also called RSA (Respiratory Sinus Arrhythmia). If the heart is tireless, it will increase the cardiac stress for which body will take pauses to preserve oxygen. The system will correlates these rhythmic patterns to CPET (Cardiopulmonary Exercise Testing).



**4. The Integration Logic:**



Despite providing the three diagnosis separately, we will use the Multi-sensor Fusion Engine and will assign a significant score to each of the stream.

For example: If the "Cardiovascular (Prosodic)" data shows high stress and the "Neurological Health (Acoustic)" data shows tremor, the system will show a Unified Health Risk Score. 

So, this fusion is far more critical because it avoids false alerts that caused by a single, isolated factor rather provides a more accurate "Big Picture" view of the patient's health. 



**Evidence:** Fig4: System Workflow Diagram, Part 1 of Fig4, Part 2 of Fig4, Part 3 of Fig4



##### **E. RESULTS AND ADVANTAGES:** 



• Greater Diagnostic Sensitivity: The invention by combining the active acoustic impedance of the Diagnostic Shield with passive prosodic signals from wearables will expose a link that a standard diagnostician might not have seen before between different aspects of physiology (for example relating abnormal heart rhythms to changes in a person's speech rate), so that an earlier intervention is carried out than a standard diagnostician would recommend.



• Improved User compliance (The "Zero-Effort" Concept): By implementing both active and passive data acquisition, user interaction with the system has been dramatically simplified. The active data collection through the diagnostic shield only takes moments but the continuous passive collection requires zero user effort. This allows for an unheard-of volume of longitudinal patient data collection.



• Privacy by Design: A major problem in health care currently is the potential for data breaches from sensitive health-related information. The system here greatly reduces risk by minimizing the amount of raw medical data that needs to be transferred over any external network by processing that raw data and extracting meaningful information using only edge-based computing.



• Clinical Utility: The system not only monitors but diagnoses health conditions in an intelligent manner by presenting the clinician with a Universal Health Score, acting as an effective triage method, and a dramatically reduced rate of false-positive alerts (only showing an alert when two or more biosignals independent from one another trigger the alarm).



##### **F. EXPANSION:**



Required parameters The system continually monitors the following variable categories in order to maintain its effectiveness and diagnostic accuracy:



**• Prosodic Data:** Fundamental Frequency ($F\_0$), Jitter, Shimmer, Articulation Rate, and Pause to Speech Ratio. 

**• Acoustic \& physiological Data:** Heart rate variability (RMSSD/SDNN), respiration rate/depth, acoustic impedance of the chest measured via the Diagnostic Shield, acoustic and physiological indicators (frequency) of coughs or bowel sounds, and SNR value of the recorded signals for correcting ambient background noise. 

**• Contextual Data:** 3-axis accelerometer value to establish a "level of user movement", time of day, and measured level of background ambient noise to adjust the detection threshold of passive monitoring devices. 



##### **G. WORKING PROTOTYPE/ FORMULATION/ DESIGN/COMPOSITION:**



** Status:** Design phase completed. 3D models (CAD/STL) for the Diagnostic Shield are ready for additive manufacturing.

** Technical Data:** All logic flowcharts (FIG 5-7) and system architectures (FIG 1-4) are finalized.

** Validation:** Implementation of the CNN-LSTM fusion model is currently in the algorithmic simulation stage. Full clinical validation and integration with a secondary UI (Clinician Portal) are estimated for completion within 180 days.



##### **H. EXISTING DATA:** 



Comparative data demonstrate an unshielded mobile microphone that experience signal clipping when it captures high-frequency respiratory transients (>3kHz). The implementation of this Diagnostic Shield will provide a linear frequency response (50Hz - 8kHz) by maintaining signal integrity sufficient for ZCR (Zero - Crossing - Rate) analysis, a requirement for early-stage respiratory detection obstructions that exists art cannot accurately measure.



#### **4. USE AND DISCLOSURE (IMPORTANT): Please answer the following questions:** 



|A. Have you described or shown your invention/ design to anyone or in any conference? |YES (  ) |NO (X) |
|-|-|-|
|B. Have you made any attempts to commercialize your invention (for example, have you approached any companies about purchasing or manufacturing your invention)?   |YES (  )|NO (X) |
|C. Has your invention been described in any printed publication, or any other form of media, such as the Internet? |YES (  )|NO (X) |
|D. Do you have any collaboration with any other institute or organization on the same? Provide name and other details. |YES (  )|NO (X) |
|E. Name of Regulatory body or any other approvals if required.  |YES (  )|NO (X) |





#### **5. KEYWORDS:** 



• Multi-modal physiological sensor system

• Acoustic signal conditioning hardware

• Distributed Edge-IoT health monitoring

• Triple-stream biomarker fusion 































































