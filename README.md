🩺 Lung Disease Classification from Chest X-Ray Images

This project builds a simple machine-learning pipeline to classify lung diseases using chest X-ray images. Instead of deep learning, the system uses handcrafted features: First Order Statistics (FOS) and Gray Level Co-occurrence Matrix (GLCM). All images are preprocessed using grayscale conversion, resizing (224×224), and CLAHE for contrast enhancement.

After extracting FOS and GLCM features, a Z-Score Masking method is applied to remove low-importance features, with the best threshold selected using GridSearchCV. The final classification is done using Support Vector Machine (SVM) with several kernels tested.

The dataset contains 4000 X-ray images across four classes: Normal, TBC, Pneumonia, and COVID-19. The best performance comes from the combined FOS + GLCM model, achieving 91% accuracy and AUC scores up to 0.99.

This repository includes scripts for preprocessing, feature extraction, feature selection, and model training, along with sample results. The project is simple, easy to follow, and serves as a clean example of classical machine-learning applied to medical imaging.
