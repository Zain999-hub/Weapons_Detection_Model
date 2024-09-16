# Weapons_Detection_Model
This project implements a YOLO (You Only Look Once) model designed to detect three types of weapons—Handgun, Knife, and Rifle—from digital media. The model is optimized for use in forensic analysis during electronic forensic investigations and crime scene investigations. By identifying weapons accurately and swiftly, the system helps investigators gather critical evidence, speeding up the investigation process while maintaining high accuracy. This project is especially relevant for law enforcement agencies and forensic teams looking to enhance their ability to analyze media from various sources during investigations.

## Dataset Stage:
To ensure robust model training, we curated a high-quality and diverse dataset containing 7,478 labeled images across three classes: Handgun, Knife, and Rifle. The images were carefully selected to represent various crime scenarios, offering a wide range of environments, lighting conditions, and angles. This diversity is crucial for the model's ability to generalize effectively, enabling it to accurately identify weapons in different settings. Each image meets the necessary standards for clarity and variation, providing a solid foundation for high accuracy in forensic analysis and crime scene investigations. The comprehensive nature of this dataset guarantees that the model can reliably detect weapons, even in complex and varied scenarios, making it an indispensable tool for law enforcement and forensic professionals.

## Training Stage:
We experimented with several optimizers, including AdamW, Adam, and SGD, before concluding that the SGD optimizer provided the best performance for the model. This decision was based on careful observation of the results, where SGD consistently outperformed the other optimizers.

The training process involved using the YOLOv8n model on the carefully selected dataset of 7,478 images. The model was trained over 300 epochs, with training progress monitored closely throughout. Initially, we started with 100 epochs to observe the model’s performance and adjust as needed. Based on the positive outcomes, we resumed training in two additional phases of 100 epochs each, carefully tracking the model's performance after every set. This gradual approach allowed us to fine-tune the model and ensure optimal results. By the end of the 300 epochs, the model demonstrated excellent prediction accuracy, effectively meeting our expectations for detecting weapons in forensic and crime scene investigations.

## confusion matrix:
![results](https://github.com/user-attachments/assets/92b4ea44-553c-4991-af96-ae2d46bb330c)
🔸Loss Trends:

    -Train Loss: Both box and classification losses continued to decline, indicating effective learning. The model minimized error while reaching optimal levels.
    -Val Loss: Validation loss showed consistent improvement, with minimal overfitting. This demonstrates strong generalization to unseen data, even after 300 epochs.
    
🔸Overfitting Control: The model maintained a balance between training and validation losses, showing that overfitting was successfully avoided. This was achieved through careful monitoring and incremental training in batches of 100 epochs.

The model achieved high accuracy and generalization while effectively avoiding overfitting, making it a valuable tool for weapon detection in forensic and crime scene investigations.
