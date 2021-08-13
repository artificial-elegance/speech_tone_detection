# speech_tone_detection

We made a tone detection CNN model for everyday speech, to aid individuals with autism in emotion detection and regulation.

The pretrained model used two datasets, RAVDESS (1499 audio file inputs from 24 different actors - 12 males and 12 females reading in neutral, calm, happy, sad, angry, fearful, disgust, surprised tones) and SAVEE (around 500 audio files recorded by 4 male actors). The model classifies female_angry, female_calm, female_fearful, female_happy. female_sad, male_angry, male_calm. male_fearful, male_happy, and male_sad voices. In our final output to the message box, we took out the gender being outputted, as the core relevant information to the user, an individual with autism, simply should be the emotion exhibited. 

The model utilizes the LibROSA library in Python to extract audio features, and a CNN model to classify between emotions. After tuning the model ourselves, we tested it out by predicting the emotions for the test data. From this, the model gave the max validation accuracy against test data around 70%.

Then, we tested the model on unseen, live voices -- our own. Using different emotions, the model predicted the outcomes fairly accurately, through a message box. We keep this running, with the users' emotions being outputted every 4 seconds, until it is canceled. You can see the results in the prerecorded demo.