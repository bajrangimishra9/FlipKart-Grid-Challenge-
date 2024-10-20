# FlipKart-Grid-Challenge-


# Dataset Links:- 
1. fresh-and-stale-images-of-fruits-and-vegetables: https://www.kaggle.com/datasets/raghavrpotdar/fresh-and-stale-images-of-fruits-and-vegetables
2. fruit-and-vegetable-image-recognition: https://www.kaggle.com/datasets/kritikseth/fruit-and-vegetable-image-recognition



# **Introduction:**

# **1. Grocer Lens:** Product Attribute Extraction
Objective: To extract product details like weight, height, volume, and other relevant specifications from grocery product images.

Dataset Collection: The dataset was sourced from e-commerce platforms (Flipkart and Amazon) and includes the following key fields:

![image](https://github.com/user-attachments/assets/e6a19969-1d20-4491-82d2-25caa90291dd)


Image URL: Direct link to the product image.
Entity Name: Attribute to be extracted (e.g., weight, volume).
Group ID: Unique identifier grouping similar entities for classification.
Image Processing & Augmentation: Images were enhanced using rotation (0°, 90°, 180°, 270°) and contrast adjustments to improve text extraction. Text is extracted using EasyOCR, followed by regex-based unit extraction and correction of OCR misinterpretations.

# Workflow:

Text extraction using EasyOCR.

![image](https://github.com/user-attachments/assets/45194b9b-3cb7-43c8-9c1b-c2ba85fd1aeb)


Unit extraction and conversion using regex.
Parallel processing with ThreadPoolExecutor for efficiency.
Fuzzy matching and Logistic Regression were used to train a model for matching extracted data with expected values.
Evaluation:

A Logistic Regression model was trained, achieving high accuracy through cross-validation.
Visualizations using scatter plots were employed to compare predicted vs. actual values.

![image](https://github.com/user-attachments/assets/fda7781e-ffb8-43c1-ab38-7359c584b3ef)


![image](https://github.com/user-attachments/assets/fef88720-10d8-4c3b-a602-f3a6267e9053)

# **2. FruitVeggieVision:** Fruit and Vegetable Classification
Objective: To classify images of fruits and vegetables and predict their specific type.

Dataset Collection: The dataset, sourced from Kaggle, contains images categorized into different classes (e.g., apple, banana, carrot). It was divided into training, validation, and test sets to ensure model generalization.

![image](https://github.com/user-attachments/assets/502e48e4-e21d-4c0f-bc8b-cf0c70a42e22)


Data Augmentation: Real-time augmentation techniques such as rescaling, rotation, flipping, zooming, and brightness adjustments were applied to increase data variability and enhance model robustness.

Model Architecture: A CNN-based model was built using the following layers:

Rescaling, Convolutional, and MaxPooling layers for feature extraction.
Dropout layers to reduce overfitting.
Dense layers to predict class probabilities.
Model Training:

The model was compiled with the Adam optimizer and trained on 30 epochs, achieving a final accuracy of 97%.
A classification report showed strong precision and recall across classes, though slight misclassifications were observed between similar classes like corn and sweetcorn.
Evaluation:

A confusion matrix was used to identify class-specific misclassifications.
The model demonstrated effective learning, with both training and validation accuracy increasing over time.

![image](https://github.com/user-attachments/assets/2b6b8ee6-e7ce-4cd4-a2f9-2eaa124eb387)


![image](https://github.com/user-attachments/assets/33254372-228c-4f08-a8bb-151f98a39434)


![image](https://github.com/user-attachments/assets/1802f618-f703-42f7-b244-e6b074192f47)

![image](https://github.com/user-attachments/assets/9460b1fb-5868-458a-b246-7bfea26c1091)


# **3. FreshTrack Vision:** Freshness Detection
Objective: To classify fruits and vegetables as fresh or stale based on images.

Dataset Collection: The dataset contains images of six fresh and six stale categories (e.g., fresh apple, stale apple) from the Kaggle fresh-and-stale images dataset.

![image](https://github.com/user-attachments/assets/c82d2dcb-f4d9-413d-b7de-d46f0345962c)


Data Augmentation: The dataset was augmented using random transformations, including rotation, width/height shifts, shear, and zoom, enhancing model generalization.

Model Architecture: A CNN-based model with Conv2D and MaxPooling layers was constructed to extract features, followed by a fully connected layer and dropout to avoid overfitting. The output layer used softmax activation to predict 12 categories.

Model Evaluation:

Training Accuracy: 91.88% across all categories.
Freshness Accuracy: 94.66%, with a strong ability to differentiate fresh vs. stale items.
Model Performance:

Training loss decreased consistently over time, while accuracy improved steadily.
The model performed well in distinguishing between fresh and stale categories.

![image](https://github.com/user-attachments/assets/53014fa3-3556-48c8-adc8-020720183a03)


![image](https://github.com/user-attachments/assets/e481b99d-7e82-437f-b83f-4704943d87b4)


![image](https://github.com/user-attachments/assets/1e0e3889-1792-4404-a070-7f464079cee9)


![image](https://github.com/user-attachments/assets/14dc1daf-faab-40a0-9628-aa4bfb154e90)


![image](https://github.com/user-attachments/assets/dba3c181-7293-4cbe-99e3-2508dff222c1)



Conclusion:

This project successfully developed AI models capable of analyzing grocery product images to extract key specifications, classify fruits and vegetables, and assess product freshness. By leveraging advanced image processing techniques, convolutional neural networks, and data augmentation strategies, the models achieved 100% accuracy in text extraction, 97% accuracy in fruit and vegetable classification, and 94.66% in freshness detection. These solutions offer significant potential for automating product analysis in e-commerce, supply chains, and quality assurance systems, enabling efficient and accurate decision-making processes.
