# Machine-Learning-Fairness-Income-Level-Classification
+ Project summary: Given some information about a person, your task is to predict if the person's annual income level is greater than 50K$ or not. Rather than purely maximizing prediction accuracy, I would try to maximize accuracy while achieving the fairness requirement. Specifically, my model must follow a relaxed version of demographic parity for the binary sensitive attribute "gender".
+ Notations: A=gender, Ŷ=prediction on the income level, Y=ground-truth income level
+ Evaluation:        
Accuracy:= ℙ[Ŷ =Y]   
DDP:= |ℙ[Ŷ =1|A=0]−ℙ[Ŷ =1|A=1]|   
Th:= 0.1   
If DDP>Th,Bias:= 7^(DDP−Th)−1, else, Bias:= 0   
Score:= Accuracy−Bias  

+ Final Score:             
Logistic Regression: 80.0% accuracy, 0.05 DDP Value, 0.80 Score  
XGBoost: 86.5% accuracy, 0.17 DDP Value, 0.75 Score   
Random Forest: 86.7% accuracy, 0.20 DDP Value, 0.70 Score   
1 XGBoost + 1 Logistic Regression: 82.2% accuracy, 0.07 DDP Value, 0.82 Score   
2 XGBoost + 1 Logistic Regression: 83.6% accuracy, 0.095 DDP Value, 0.84 Score
