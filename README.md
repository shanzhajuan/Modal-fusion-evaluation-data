# Shopping system evaluation data
evaluation data of multimodal shopping system

## Evaluation data of the Dialogue System
./eva_dialogue.xlsx

It consists 12 conversations, 27 cake matching tasks and 66 conversation rounds that are obtained by manual labeling. 

It is in Chinese because the system is built for native Chinese users.
## Evaluation data of multimodal fusion method
### fusion data of test set
- ./test set for fusion/multi_data.npy: array type; shape: (N,5,3). N=2000.

  It contains N sets of multimodal data. Each set of data contains the emotion classification results for 5 modalities.
  
  the order of the 5 modalities are: expression, pose, gesture, contact force, speech.
- ./test set for fusion/multi_label.npy: array type; shape: (N,1). N=2000.
  
  It is labels for N sets of multimodal data. The value of each set is 0 or 1 or 2, where 0 means NEGATIVE emotion, 1 means POSITIVE emotion, and 2 means NEUTRAL.

  multi_data.npy and multi_label.npy contain 359 two-modality fusions (2-modals), 781 three-modality fusions (3-models), 652 four-modality fusions (4-models), and 208 five-modality fusions (5-models).

  For the sake of data balance, we additionally added 300 2-modals data and 500 5-modals data:
  
 ./test set for fusion/multi_data2.npy; ./test set for fusion/multi_label2.npy

./test set for fusion/multi_data5.npy; ./test set for fusion/multi_label5.npy

 It is worth noting that the tests mentioned in the paper used only half of these that randomly selected.
  
### user-based evaluation data 
- ./fusion methods on test set/multi_data_user.npy: array type; shape: (N,5,3). N=20.
  
  It contains N sets of multimodal data. Each set of data contains the emotion classification results for 5 modalities.
  
  the order of the 5 modalities are: expression, pose, gesture, contact force, speech.
- ./fusion methods on test set/multi_label_user.npy: array type; shape: (N,1).
  
  It is labels for N sets of multimodal data. The value of each set is 0 or 1 or 2, where 0 means NEGATIVE emotion, 1 means POSITIVE emotion, and 2 means NEUTRAL.
