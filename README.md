Utilizing a Convolutional Neural Network (CNN) architecture, this model is designed to categorize trash into three distinct classes: metal, plastic, and other.

The CNN model serves as an efficient solution for classifying images of various trash items. It adheres to the trash policy established by The American University in Cairo.

Initially, a comprehensive dataset of trash images was compiled from online sources as well as existing repositories such as GitHub and Roboflow. The dataset was bifurcated into metal and plastic categories. However, due to the vast diversity within the broader category of "other" trash types, the decision was made not to train the model explicitly on this subset. The concern stemmed from the potential impact of this extensive domain on the model's accuracy.

Instead, the model was trained exclusively on images of metal and plastic trash. To address instances where the classification isn't definitive, a threshold mechanism was implemented. If the model's confidence score falls within a certain range (e.g., around 0.5), indicating uncertainty between metal and plastic, the item is automatically categorized as "other." It's important to note that this classification process occurs post-model inference, where the model provides a confidence score between 0 and 1 for each class.

Preprocessing and normalization techniques were applied to standardize each image into a compatible NumPy array format. Augmentation methods were also employed to diversify and augment the dataset, enhancing the model's robustness.

Transfer learning, a technique involving fine-tuning an already trained CNN model, was leveraged to refine the model's performance. Remarkably, this approach led to achieving an impressive accuracy rate of 99%.

Moving forward, the model was deployed on a raspberry pi and used its camera as the input for the model. 
Attached below is a video of the model successfully identifying a plastic waste while running on the pi. 

https://github.com/user-attachments/assets/978ea665-294a-4e29-aac0-d43586373774



