# Gait analysis

## Introduction

Gait analysis is a comprehensive assessment of the way an individual walks or runs, used primarily to highlight any abnormalities in gait patterns that could be indicative of underlying health issues. This type of analysis meticulously captures biomechanical data to evaluate different aspects such as stride length, speed, and body symmetry during movement. Technological advancements have enabled sophisticated methodologies in gait analysis, utilising sensors and cameras to provide precise, quantitative data. This analysis is crucial not only in sports and rehabilitation but also in diagnosing conditions like Parkinson's disease, arthritis, and musculoskeletal disorders, where changes in gait can be some of the first signs of disease progression.

In the context of Ambient Assisted Living (AAL), gait analysis holds significant relevance as it offers a non-intrusive means of continuous monitoring that can alert caregivers and healthcare providers to changes in an older person's mobility and balance. Regular monitoring of gait can identify early signs of decline in physical function, which is often a precursor to falls —a major risk for elderly individuals. Integrating gait analysis into AAL systems leverages technology to ensure safety and support for older people, enabling early intervention and facilitating aging in place with dignity. This technology not only enhances the ability to live independently but also supports preventive health measures, improving overall quality of life.

Computer vision for gait analysis is a significant advancement in assessing walking patterns, utilising image processing and machine learning to detect and analyse human motion. This technology captures real-time video data, which is then processed to extract key information about gait characteristics such as stride length, gait speed, and postural control. The application of computer vision in gait analysis allows for precise and accurate assessment without the need for physical contact or invasive markers on the body. This approach is particularly useful in settings where continuous monitoring is essential, offering an efficient, scalable, and less obtrusive method to assess mobility and balance. Consequently, computer vision has become an invaluable tool in clinical diagnostics, rehabilitation, and elderly care, providing insights that can guide treatment plans, monitor recovery, and prevent falls by identifying potential mobility issues before they result in serious injuries.

## The PsyMo dataset

The [PsyMo dataset](https://github.com/cosmaadrian/psymo) is a comprehensive multi-modal dataset designed to investigate psychological traits manifested in walking patterns. Developed by researchers from the University Politehnica of Bucharest, it features data from 312 participants who walked in seven different styles, captured from six camera angles. In addition to motion data, the dataset includes self-reported psychological traits from six different questionnaires covering aspects like personality, self-esteem, fatigue, aggression, and mental health. PsyMo, which stands for Psychological traits from Motion, offers anonymised data including silhouettes, 2D and 3D human skeletons, and 3D SMPL human meshes, making it a rich resource for both psychological and gait analysis research.

The Psymo dataset was presented at the 2024 IEEE/CVF Winter Conference on Applications of Computer Vision (WACV). The paper is available [here](https://openaccess.thecvf.com/content/WACV2024/papers/Cosma_PsyMo_A_Dataset_for_Estimating_Self-Reported_Psychological_Traits_From_Gait_WACV_2024_paper.pdf).

## Lab session - Implementing deep learning for gait analysis using the PsyMo dataset 

This lab session aims to provide students with practical experience in applying deep learning techniques to analyze gait patterns using the PsyMo dataset. The session will focus on developing models that can interpret variations in walking styles associated with different psychological traits.

### Tasks

1. Data exploration:
    * Familiarise yourself with the dataset structure.
    * Visualise different modalities of gait data (silhouettes, skeletons). See folder *semantic_data*.
    * Analyse files with labels (metadata_labels_v3.csv, metadata_raw_scores_v3.csv, walks-v2.csv).

2. Preprocessing:
   
    * Implement data cleaning and normalisation techniques.
    * Generate training and testing splits ensuring a balanced representation of walking styles and psychological traits. 
   
   > The authors propose subjects with IDs from 0-250 should be used for training, and evaluation ought to be performed on subjects with IDs from 251-312, corresponding to an 80:20 training-evaluation split. However, in most cases, you will not have enough computing capabilities to train the whole dataset. Therefore, I recommend that for implementation and preliminary tests, you use a reduced subset, following the same percentages. For instance, subjects with IDs 0-8 for training, and 251-252 for evaluation. You can adjust these numbers based on your computing capability.

3. Model building:
   
    * Choose an appropriate deep learning architecture.
    * Develop a model to correlate gait patterns with psychological traits.
    * Utilise transfer learning, if applicable, to leverage pre-trained models on similar tasks.

   > Here, you need to propose a deep learning architecture to correlate gait patterns with psychological traits. You have here several alternatives: 
   > 1. Use an existing model (like [OpenGait](https://github.com/ShiqiYu/OpenGait), [GaitGraph](https://github.com/tteepe/GaitGraph2) or any of the others used by the authors) - See Table 2 in their paper.
   > 2. Propose a new model. For instance, using Video Vision Transformers, Graph Convolutional Networks, 3D ConvNets, Inflated 3D ConvNets,...) - See the module on [Video-based human action/activity recognition](https://jazorinl.github.io/tava/HAR/).
   > The authors propose two evaluation methodologies: (i) run-level and (ii) subject-level. For run-level evaluation, the model performance is evaluated for each walking sequence, irrespective of the subject. Performance in terms of precision, recall, weighted F1 score should be reported for all combinations of walking variations and viewpoints. This protocol is similar to a typical gait classification task (i.e. input walking sequence, output classes). For subject-level evaluation, the goal is to correctly identify the psychometric attributes for each subject, considering all available variations or runs. For instance, a naive baseline for subject-level evaluation is to use the run-level model and report the majority predicted classes for a questionnaire for all the runs of a subject. Methods for subject-level evaluation may consider the identity of the subject to be known at test time - a scenario possible in the real-world, as a part of a larger pipeline for gait recognition and classification. The same metrics as in run-level evaluation should be used.
   > 3. Merge an existing model with some additional inputs.

4. Training:

    * Train the model using the prepared dataset.

5. Evaluation:

    * Evaluate the model performance using appropriate metrics (e.g., accuracy, F1-score).

6. Discussion and Reporting:

    * Interpret the results and discuss the implications of the findings.
    * Prepare a brief report summarising the methodology, results, and potential improvements.

## Timeline

* This lab session will take place on **Wednesday 30 April 4pm to 9pm** and on **Wednesday 7 May 4pm to 6pm**.
* Dedicate a maximum of 16.5 hours to this work. This includes time at home. If you are not able to finish all the tasks, please, report it in the final report.
* If you work more than those 16.5 hours, please, specify the amount of time worked.
* Code (for instance, a link to a Colab notebook) and brief report must be provided through the Evaluation option at UACloud by **Wednesday 8 May 11.59pm**. 

