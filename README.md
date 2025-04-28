# 🤟 ASL Sign Language Crossword using MobileNetV2

This project focuses on detecting American Sign Language (ASL) hand gestures using deep learning and then further use it to play a game of simple crossword. It includes data collection with OpenCV and MediaPipe, training a MobileNetV2-based image classification model, and evaluating its performance on a custom dataset of ASL signs (0-9 and A-Z). 

By integrating ASL recognition with interactive crossword puzzles, we aim to make language learning more engaging, intuitive, and enjoyable. Such playful learning experiences can contribute significantly to the cognitive and linguistic development of young users.

---

## 🛠️ Installation
```bash
git clone https://github.com/therealsheero/ASL-Detection.git
cd ASL-Detection
```

📦 Requirements
Install the required packages using:

```bash
pip install -r requirements.txt
```

## 🖐️ Data Collection
```bash
python Collect_Data.py 
```
**Controls**:
- `S` - Save frame
- `Q` - Quit
- Auto-cropping to hand region

## 🧠 Model Training
```bash
python train_pth.ipynb 
  --data_dir data 
  --model mobilenetv2 
  --epochs 20 
  --output asl_mobilenetv2_best.pth
```

**Training Results**:
```
Epoch 20/20 | Epoch 20: Train Acc: 1.0000, Val Acc: 0.9722
Test Accuracy: 98.3%
```

## ▶️ Real-Time Detection
```bash
python test.py 
```

## 📊 Performance
| Metric       | Value |
|--------------|-------|
| Accuracy     | 98.3% |

## 🌟 Key Files
- `Collect_Data.py`: Hand tracking + data saver
- `train_pth.ipynb`: Model training pipeline
- `test.py`: Live webcam detection
- `app_CSVCross.py`: ASL Crossword Application

## 📧 Contact
[E22CSEU0631@bennett.edu.in](mailto:E22CSEU0631@bennett.edu.in)
```
▶️ How to Use
This model can be integrated into a real-time webcam-based ASL interpreter using OpenCV and MediaPipe or cvzone. Load the model, capture hand ROI, preprocess it, and run predictions.

🚀 Future Work
Add real-time ASL detection app
Improve dataset diversity
Deploy on web or mobile using TensorFlow Lite or ONNX
```




