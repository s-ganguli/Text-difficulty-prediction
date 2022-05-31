# Milestone 2 (a Supervised ML, Unsupervised ML and NLP project)
# Text-difficulty-prediction
By Sharadwata Ganguli and Panini Mohan Mokrala

## <a href="https://github.com/s-ganguli/Text-difficulty-prediction/blob/main/SIADS695_MIlestone2_Project_Report_Team10_Final.pdf"> Project report here</a>


## Project Summary
For editors of simple Wikipedia articles, it would be quite valuable to know which parts of an article’s text to simplify before spending actual effort in simplifying the text. A text difficulty prediction algorithm would be effective for this task

We used a multi-step approach starting from Feature Engineering to Unsupervised & Supervised Learning, to create the text difficulty prediction algorithm. We used the
same Wikipedia text labeled training corpus for both unsupervised and supervised components Findings: Throughout our exercise, we found some interesting features in the Wikipedia text corpus. While the length of text that requires simplification is longer, this attribute isn’t significant enough to improve the accuracy by a lot. Our unsupervised learning algorithms helped us get the ‘denser’ feature space, that reveals a vastly similar distribution across training labels highlighting the need for us to understand how the labelling had been done. A simple illustration through UMAP illustrated that there is no clear distinct clustering structure. This overlapping nature of the sentence features across labels means that the classification algorithms will find it hard to codify the inherent patterns of sentences that
needs simplification and vice-versa. With the above-mentioned limitations, we are able to achieve a reasonable accuracy of 70% in validation dataset and 72% accuracy in test dataset. Some interesting observations supporting this argument are present in Failure analysis.

The Machine Learning algorithms that we have used to identify clusters or predict difficulty apply the same rule to each text consistently. However, the ground truth labels of text difficulty in the training corpus were presumably crowd sourced - this would mean that there could be inconsistency in the training labelling approach due to various biases of the labeling person(s). Thus, the ground truth labels could be subjective and using it to train models could end up replicating the biases of the human labelers. A potential next step could be to identify approaches to make the ground truth labels more consistent and thus reduce the subjectivity in the labeling

## Project Steps
For editors of simple Wikipedia articles, it would be valuable to be provided suggestions as to which parts of a text needs to be simplified. Given this context, we have developed a text difficulty prediction model (the supervised part) whose objective will be to accurately predict ‘need for simplicity’ of any input sentence. We explored setting up an app that can take real world examples and highlight if the sentence needs simplification. Simultaneously, an unsupervised part was used to augment the features for the supervised part as well as identify actual clusters in the text. We have used google colab & google drive platforms for coding, collaboration & data storage. We have used a set of Notebooks -these were run in the following sequence to follow the below Process flow:

1. Step1_Feature_Engineering_Part1 (<a href="https://github.com/s-ganguli/Text-difficulty-prediction/blob/main/Step1_Feature_Engineering_Part1.ipynb">Step1_Feature_Engineering_Part1.ipynb</a>)
2. Step1_Feature_Engineering_Part2 (<a href="https://github.com/s-ganguli/Text-difficulty-prediction/blob/main/Step1_Feature_Engineering_Part2.ipynb">Step1_Feature_Engineering_Part2.ipynb</a>)
3. Step2_Unsupervised_Learning (<a href="https://github.com/s-ganguli/Text-difficulty-prediction/blob/main/Step2_Unsupervised_Learning.ipynb">Step2_Unsupervised_Learning.ipynb</a>)
4. Step3_Supervised Learning (<a href="https://github.com/s-ganguli/Text-difficulty-prediction/blob/main/Step3_Supervised Learning.ipynb">Step3_Supervised Learning.ipynb</a>)
5. Step4_FastApi App/Python application (<a href="https://github.com/s-ganguli/Text-difficulty-prediction/blob/main/Step4_FastApi App_Python application.ipynb">Step4_FastApi App_Python application.ipynb</a>)


## Data Sets used
1. https://www.kaggle.com/c/umich-siads-695-fall21-predicting-text-difficulty/data
