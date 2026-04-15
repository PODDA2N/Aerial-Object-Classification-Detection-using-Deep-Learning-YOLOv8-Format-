# Aerial-Object-Classification-Detection-using-Deep-Learning-YOLOv8-Format-

📊Bird vs Drone Classification & Detection using Deep Learning (YOLOv8 Format)

Project Overview

This project presents an end-to-end computer vision solution to classify and detect birds and drones using deep learning techniques. It combines Custom CNN, Transfer Learning, and Object Detection (YOLOv8) along with a Streamlit web application for real-time predictions.
The solution will help in security surveillance, wildlife protection, and airspace safety where accurate identification between drones and birds is critical. The project involves building a Custom CNN classification model, leveraging transfer learning, and optionally implementing YOLOv8 for real-time object detection. The final solution will be deployed using Streamlit for interactive use.
Wildlife Protection
Detect birds near wind farms or airports to prevent accidents.
Security & Defense Surveillance
Identify drones in restricted airspace for timely alerts.
Airport Bird-Strike Prevention
Monitor runway zones for bird activity.
Environmental Research
Track bird populations using aerial footage without misclassification.

Industries like aviation, defense, and industrial security often face false alarms due to birds being misidentified as drones. On the other hand, missing an actual drone threat can have serious consequences. This inspired me to build an end-to-end AI solution to solve this problem.
In today’s world of aerial surveillance and airspace security, distinguishing between birds and drones is not just a technical challenge — it’s a critical business need.
•  Real-time video detection (CCTV / drone feed)
•  Edge deployment for low-latency systems
•  Multi-object aerial classification.

Project Workflow

🔹 Understand the Dataset
•	Inspect dataset folder structure
•	Check number of images per class
•	Identify class imbalance
•	Visualize sample images

🔹 Data Preprocessing
•	Normalize pixel values to [0, 1]
•	Resize images to a fixed size (224×224 for classification)

🔹Data Augmentation
•	Apply transformations: rotation, flipping, zoom, brightness, cropping

🔹Model Building (Classification)
•	Custom CNN: Conv layers, pooling, dropout, batch normalization, dense output layer.
•	Transfer Learning: Load models like ResNet50, MobileNet, EfficientNetB0 and fine-tune

🔹 Model Training
•	Train both models
•	Use EarlyStopping & ModelCheckpoint
•	Track metrics: Accuracy, Precision, Recall, F1-score

🔹 Fine-Tuning Strategy
•	Initially trained only the added layers
•	Gradually unfroze top layers of the base model
•	Fine-tuned the model on the bird vs drone dataset
•	Optimized performance using validation data

🔹Model Evaluation

•	Evaluate test results with confusion matrix & classification report
•	Plot accuracy/loss graphs

🔹Model Comparison
•	Compare accuracy, training time, and generalization performance.

📊 Accuracy & Loss Graphs Matter (Business Perspective)

📈 Accuracy Graph Explanation: 
🔹 Training Accuracy
Measures how well the model learns from training data
🔹 Validation Accuracy
Measures performance on unseen data.
Business Insight:
•	If both training & validation accuracy increase → model is reliable.
•	If training accuracy is high but validation is low → risk of false alarms in production.

📈 Loss Graph Explanation:
The loss graph shows how well the model minimizes prediction errors.
🔹 Training Loss
Error on training dataset
🔹 Validation Loss
Error on unseen validation dataset
Business Insight:
•	Decreasing loss → model improving
•	Increasing validation loss → model may fail in real-world scenarios.

Object Detection with YOLOv8:

⚙️ Steps Performed
•  Installed YOLOv8 (Ultralytics)
•  Converted dataset into YOLO format (images & labels)
•  Created data.yaml configuration file
•  Trained YOLOv8 model
•  Validated model performance
• Ran inference on test and new imagesModel Training.

Custom CNN & Transfer Learning

•	Data Augmentation applied (rotation, flipping, zoom, brightness)
•	Optimizer: Adam
•	Loss Function: Binary Crossentropy
•	Metrics: Accuracy

YOLOv8

•	Model: yolov8n / yolov8s
•	Epochs: 10–30
•	Image Size: 640
________________________________________
📊 Model Evaluation
The models were evaluated using:
•	Accuracy
•	Precision
•	Recall
•	F1-score
•	Confusion Matrix
Comparison was performed between:
•	Custom CNN
•	Transfer Learning models
________________________________________
 Results Visualization
•	Accuracy vs Epochs
•	Loss vs Epochs
•	Confusion Matrix Heatmap
________________________________________
 Streamlit Deployment
A simple and interactive web application was built using Streamlit.
Features:
•	Upload image 📤
•	Classify image (Bird / Drone)
•	Display confidence score
•	Show YOLOv8 detection results with bounding boxes
