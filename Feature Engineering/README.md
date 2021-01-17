# Feature Engineering

The following features were added using the existing features of the dataset 
 - **answered_correctly_u_avg** : The average accuracy of the user till this interaction
 - **explanation_u_avg** : The percentage of questions for which the user has refered to the correct answer and its explanation
 - **community** : The cluster to which a question belongs
 - **answered_correctly_q_avg** : The average accuracy for the question till this interaction
 - **explanation_q_avg** : The percentage of questions for which users have refered to the correct answer and the explanation of this **question_id**
 - **elapsed_time_q_avg** : The average time taken to answer this question by all users who have answered it
 - **timestamp_u_recency_1** : The time elapsed since the user answered last question
 - **timestamp_u_recency_2** : The time elapsed since the user answered last but one question
 - **timestamp_u_recency_3** : The time elapsed since the user answered last but two question
 - **timestamp_u_incorrect_recency** : Time elapsed since the user answered a question incorrectly
 - **num_lectures** : The number of lectures attended by the user till this ineraction
 - **num_i** : The number of times the user has given **i** as the answer to a question (i = {0,1,2,3})
 - **answered_correctly_uq_count** : The number of times this question has been answered by this user till this intearction
 
## Dynamic Feature accumulation
Brief description of the features accumulated in each dictionary
 - **answered_correctly_u_count** : Number of questions answered by each student
 - **answered_correctly_u_sum** : Number of questions answered correctly by each student
 - **explanation_u_sum** : Number of explanations seen by each student
 - **timestamp_u** : Timestamps of last 3 user interactions of each student
 - **timestamp_u_incorrect** : Timestamp of last incorrectly answered question of each student
 - **lecture_count** : Number of lectures attended by each student
 - **answer_u_count** : Frequency of each answer given by each student
 - **answered_correctly_q_count** : Number of times each question is answered
 - **answered_correctly_q_sum** : Number of times each question is answered correctly
 - **elapsed_time_q_sum** : Total time taken to answer all occurences of each question
 - **explanation_q_sum** : Number of times an explanation is seen after answering each question
 - **answered_correctly_uq** : Number of times each question is answered by each student
 
The code for feature engineering is in Riiid Feature Engineering.ipynb
## References

The questions were clustered based on the **tags** information to get community feature (https://www.kaggle.com/spacelx/2020-r3id-clustering-question-tags)
