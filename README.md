# Binary Classification of Rice

Binary Classifier to sort Grains of rice into 2 species.
you can have fun moving things around on colab by following the link but make sure to make your own copy first for your changes to be saved!


#

## Project Flow

1. Explore Dataset
   1. Normalize for multiple features w/ Z-score
   2. Set random seed
   3. Split training(80%), validation(10%) & test(10%) datasets
2. Create Binary Classifier to sort
   1. One w/ the main features
   2. Another w/ all features
3. Evaluate Model Performance
   1. Individually &
   2. Comparing AUC & ROC of both models

## Dataset

The Cinar & Koklu 2019 Osmancik and Cammeo Rice Dataset.
Contains:
- measurements of rice derived from their images
- data on 2 species of Turkish rice
  - Osmancik
  - Cammeo
- lengths & area in px

### Features

- Area
- Convex Area
- Perimeter
- Major Axis Length
- Minor Axis Length
- Extent
- Eccentricity

### Exploring the Data

2D and 3D plots of some features, colour coded by class:

1. Perimeter x Convex Area
<img width="1296" height="457" alt="Screenshot 2026-03-25 at 5 08 46 PM" src="https://github.com/user-attachments/assets/4ac4fc34-8497-47b4-b271-60bfa6b3c13a" />

2. Eccentricity x Area
<img width="1272" height="472" alt="Screenshot 2026-03-25 at 5 09 12 PM" src="https://github.com/user-attachments/assets/b6dd7507-c8d2-4e4b-890f-80620bd1a96e" />

3. Minor Axis x Major Axis Length
<img width="1252" height="470" alt="Screenshot 2026-03-25 at 5 09 36 PM" src="https://github.com/user-attachments/assets/b614d57f-0325-46ca-bcbe-4b4f349d8e3b" />

4. Extent x Perimeter
<img width="1255" height="451" alt="Screenshot 2026-03-25 at 5 10 00 PM" src="https://github.com/user-attachments/assets/32998acd-c622-460a-9a18-bba764407bd7" />

5. Major Axis Length x Eccentricity
<img width="1252" height="466" alt="Screenshot 2026-03-25 at 5 10 18 PM" src="https://github.com/user-attachments/assets/40b19609-e078-483c-a028-1a321e95932c" />

6. Major Axis Length x Area x Eccentricity
<img width="880" height="445" alt="Screenshot 2026-03-25 at 5 10 48 PM" src="https://github.com/user-attachments/assets/4f9c2d63-a8f8-4fe5-b730-ed3e4688ed30" />

7. Major Axis Length x Area x Eccentricity 

<img width="976" height="446" alt="Screenshot 2026-03-25 at 5 11 52 PM" src="https://github.com/user-attachments/assets/d5d5dd0c-ec95-4487-b30b-0f470a8c1fa2" />

- Major Axis Length
- Area
- Eccentricity   <br>
seem to be the most informative in differentiating the 2 classes.  <br>
There's a distinct class boundary in the plane of these 3 features.

## The Model

- Logistic Regression
  - Sigmoid Function   <br>
w/ keras

## Model Performance

### Comparing both Models

Since a lot of the features are interrelated, it doesn't seem to make much of a difference when we add the other 4 features for the second model.  <br>
There isn't much of an improvement in model quality and they both seem to do pretty well.

### Testing on Unseen Data

Model performs similarly well on unseen data as well.

## Citation

Cinar, I. and Koklu, M., (2019). “Classification of Rice Varieties Using Artificial Intelligence Methods.” International Journal of Intelligent Systems and Applications in Engineering, 7(3), 188-194.

DOI: https://doi.org/10.18201/ijisae.2019355381
