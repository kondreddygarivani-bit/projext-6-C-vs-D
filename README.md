Cats vs Dogs Classifier — Transfer Learning with MobileNetV2
A deep learning image classifier that predicts whether an image is a cat or a dog using transfer learning on a pretrained MobileNetV2 model.

Results
Phase	Epochs	      Val Accuracy
Phase 1 —           Frozen base	5	~96%
Phase 2 —           Fine-tuned	5	98%

How it works
Load MobileNetV2 pretrained on 1.2M ImageNet images
Freeze base layers — keep learned features
Add custom classification head (cat vs dog)
Train top layers for 5 epochs
Unfreeze top 30 layers — fine-tune at low learning rate
Test on real images with confidence score

Tech Stack
Python · TensorFlow · Keras
MobileNetV2 (pretrained — ImageNet)
TensorFlow Datasets (cats_vs_dogs)
Matplotlib · NumPy · PIL

Dataset
TensorFlow Datasets — cats_vs_dogs

23,000 training images
80/20 train/val split
Key concepts used
Transfer Learning
Fine-tuning
Data Augmentation (flip, rotate, zoom)
Binary Cross-Entropy Loss
Adam Optimizer

Sample prediction
Upload any cat or dog image → get prediction + confidence %

