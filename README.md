# Yoga-Posture-Detection
Yoga has become popular throughout the world. Lockdown months during the period of
COVID-19 has made it difficult for people to go outside for exercise and get proper
guidance and training from professionals in order to practice yoga with proper posture.
Most people, while practising yoga themselves, face difficulties in finding the incorrect
parts of their yoga poses by themselves. Practising yoga asanas in an improper way
may cause acute injuries. Yoga pose detection and analysis will help people not only in classifying the
pose but also in checking how well their pose is as compared to a perfect yoga pose
and will save people from the expenses to hire training professionals. 

## Proposed Solution:
*Our proposed solution is to utilise the OpenPose convolutional neural network (CNN) to
separate 25 key points of the human joint areas using the BODY_25 dataset from the
images and obtain the human skeletons of the user’s pose from these key points. For
pose estimation, we have prepared the deep learning model in order to train our dataset
of images of people performing different yoga postures consisting of 10 different yoga
postures. The obtained human skeletons are then classified to obtain the desired pose.
*For analysing the user’s pose, we have used ComparatorNet to compare the
coordinates of the various key points obtained from OpenPose CNN with the
coordinates of respective parts of the desired pose.
Before comparing the key points of the images, the coordinates of the images are
scaled and converted to a single vector form which is then normalized.
*ComparatorNet will compare each image from our dataset with every other image and
then will check whether they both belong to the same yoga pose or not. If both the
images represent the same yoga pose, then the ground truth is labelled as 1; otherwise,
it is labelled as 0.The similarity score will be used as a measure of the correctness of
the user’s pose. Based on the similarity score, the system can give real-time feedback
to the user about the correctness of the yoga posture.
*Using this system, the user can click a photo of himself/herself practising the pose. The
pose of the user is compared with the perfect pose, and the differences between the
two are calculated. Based on these differences of postures, feedback is provided, which
will tell the user up to what extent his/her pose matches the perfect pose so that he/she
can improve the pose.
*Our system will provide a cost-effective and feasible solution to individuals enabling
them to become more self-reliant and mitigating the risk of injuries caused due to
improper yoga form.

## Results:
Accuracy of the our model is 90%. 

## Surveys:
*An online survey regarding adverse effects of yoga in absence of proper guidance was
conducted among German yoga practitioners ( n  = 1702; 88.9% female;
47.2 ± 10.8 years) was conducted.
*One in five adult yoga users reported at least one acute adverse effect in their yoga
practice, and one in ten reported at least one chronic adverse effect, mainly
musculoskeletal effects. Adverse effects were associated with hand, shoulder and head
stands with yoga self-study without supervision. 

## Future Aspects:
1. Allow detection for multiple individuals simultaneously since there are a lot of
scenarios where single-person pose detection is not sufficient. Suppose, if
multiple people are practicing yoga together, then multiple individuals detection is
needed so that the pose of each individual can be analysed.
2. Expand the dataset to include more postures since our current model is
classifying for only 10 yoga postures.
3. Provide more detailed step by step real-time instructions to the user so that
he/she can easily rectify the posture.
4. Currently, we have done posture analysis which works with 2D images only by
identifying the key-points. We can expand it to 3D images also by using 3D
triangulation from multiple single views which might be a challenging task. 
