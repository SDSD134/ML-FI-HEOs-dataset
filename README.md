# MachieneLearning-A<sub>2</sub>B<sub>2</sub>O<sub>7</sub>-type HECs-Dataset

This is the repository for dataset that was used in the paper: Multi-dimensional anisotropic feature interaction with machine learning to predict the thermal conductivity of A<sub>2</sub>B<sub>2</sub>O<sub>7</sub>-type high-entropy ceramics.

In this work, the data sets were gathered from published papers. The dataset comprises 192 experimental data samples, each including the chemical formula and Thermal conductivity values, and is available in the supplementary Information. Below are the data descriptions of other data set files


## 1. data_with_ABO_merged_file.csv

This file gives the second type interaction of the A<sub>2</sub>O<sub>3</sub> and B<sub>2</sub>O<sub>4</sub> for the same chemical component which is shown in Fig.2(a). Using the single element feature, the average value and disorder value of the six types of features of A<sub>2</sub>O<sub>3</sub> and B<sub>2</sub>O<sub>4</sub> are calculated, and then the feature interaction of the above values is carried out. Each type of interaction includes addition, subtraction, multiplication, division, and root mean square.

As shown in data_with_ABO_merged_file.csv, A total of 84 features were obtained, of which 60 groups were derived from the feature interactions between A<sub>2</sub>O<sub>3</sub> and B<sub>2</sub>O<sub>4</sub>, and 24 groups were derived from the mean and disordered values of A<sub>2</sub>O<sub>3</sub> and B<sub>2</sub>O<sub>4</sub>.


## 2. data_with_AB_merged_file.csv

This file gives the first type interaction of A-site and B-site within the same chemical composition, as shown in Fig.2(a). Using the single element feature, the average value and disorder value of the six types of features of A-site and B-site are calculated, and then the feature interaction of the above values is carried out. Each type of interaction includes addition, subtraction, multiplication, division, and root mean square.

As shown in data_with_AB_merged_file.csv, A total of 84 features were obtained, of which 60 groups were derived from the feature interactions between A-site and B-site, and 24 groups were derived from the mean and disordered values of sites A and B.


## 3. data_with_ION_merged_file.csv

This file gives the third type interaction of the cations and anions for the same chemical component which is shown in Fig.2(a).  Using the single element feature, the average value and disorder value of the six types of features of cations and anions are calculated, and then the feature interaction of the above values is carried out. Each type of interaction includes addition, subtraction, multiplication, division, and root mean square.

As shown in data_with_ION_merged_file.csv, A total of 84 features were obtained, of which 60 groups were derived from the feature interactions between cations and anions, and 24 groups were derived from the mean and disordered values of cations and anions.


## 4. data_without_duplicates_clean_all.csv

This file gives a summary set of feature interactions, including the same chemical component among different features, the A-site and B-site, the A<sub>2</sub>O<sub>3</sub>and B<sub>2</sub>O<sub>4</sub>, the cations and anions. A total of 563 features were obtained. Some column features were removed because of data overlap.


## 5. Gradient_Boosting_Feature_Importances.csv

Through the Gradient Boosting Regressor with Recursive Feature Elimination and Cross-Validation as a feature selection model, the top 10 interaction features were determined, which were shown in Gradient_Boosting_Feature_Importances.csv.


## 6. multi_element_weighted_features_DIFF.csv

This file gives the fourth type of interaction for the same chemical component among different features which is shown in Fig.2(b). First, the single-element features are used to calculate the average value(M) and disorder value(S) of the six types of features for the obtained chemical components, and then the above values are subjected to feature interaction. While no matter what kind of feature interaction, each interaction involved addition, subtraction, multiplication, division, and root-mean-square. In total, we obtained 342 features, as shown in multi_element_weighted_features_DIFF.csv, out of which 330 sets came from different feature interactions of the same component and 12 sets came from the average value and disorder value of the same component.


## 7. normalized_data_training.csv

This file shows the chemical components and thermal conductivity values of the input machine learning model, as well as the values corresponding to the most important 8 interaction features determined by the Gradient Boosting Regressor with Recursive Feature Elimination and Cross-Validation method. This file is mainly used for model training and prediction to evaluate the performance of five different classes of models(KNN、RF、SVM、ANN、XGB) as well as to optimize the tuned optimal XGB model.


## 8. normalized_data_predicting.csv

This file gives the thermal conductivity value of (La<sub>0.2</sub>Nd<sub>0.2</sub>Sm<sub>0.2</sub>Yb<sub>0.2</sub>Y<sub>0.2</sub>)<sub>2</sub>Zr<sub>2</sub>O<sub>7</sub> prepared by the solid-phase sintering method. The chemical component and the corresponding interactive eigenvalue are used as input to the machine learning model to predict its corresponding thermal conductivity value, and the model performance is evaluated by the difference between the predicted value
and the experimental value.


## 9. single_element_feature.csv

This file is a feature set for a single chemical element. In A<sub>2</sub>B<sub>2</sub>O<sub>7</sub>-type HECs, A-site can accommodate up to 17 rare earth (RE) elements and B-site includes elements like Zr, Hf, Sn, Ti, and Ce. When oxygen is combined with A-site and B-site, they can formA<sub>2</sub>B<sub>2</sub>O<sub>7</sub>-type HECs. Thus, 24 single-element features were placed in single.csv. Each element contains the basic chemical and physical properties including relative atomic mass(m), atomic density(p), ionic radius(r), electronegativity(x), phonon velocity(v), and Young's modulus(e).

