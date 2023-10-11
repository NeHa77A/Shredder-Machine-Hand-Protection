# Shredder Machine Hand Protection
##  Problem

According to data from the Consumer Product Safety Commission, over 2,000 people were treated in hospitals for business and office machine-related injuries in 2007. A significant portion of these injuries resulted from mishaps with paper shredders, particularly lacerations to fingers. These injuries can range from minor cuts to severe amputations and can lead to lasting physical and psychological trauma.

## solution
we will delve into a comprehensive solution that combines data science, TensorFlow Object Detection (TFOD), and OpenCV to enhance safety around these machines. The solution aims to create a "Safety Line" for warnings and a "Borderline" for shutting down the machine when necessary.

### Tech Stack Selection

Programming Language: Python 3.6 is chosen for its versatility and strong support in the data science and machine learning communities.

Deep Learning Framework: TensorFlow is selected due to its robustness and extensive support for object detection.

Image Processing: OpenCV and imutils are used for video frame extraction and image processing.

Audio Feedback: The 'playsound' library can be used to provide audible warnings or notifications to workers.

## Training
1. Data Collection: Start by collecting video data from the specific industrial environment where the shredder is used. This data will serve as the basis for model training.

2. Frame Extraction: Using OpenCV, convert the video into frames. These frames are the building blocks for model training.

3. Annotation: Manually annotate the frames, marking the location of hands in each frame. This annotated data is crucial for training the model.

4. Model Training: Utilize TensorFlow Object Detection to build and train a model that can recognize hands in the frames. The model should be capable of real-time processing to provide immediate feedback.

5. Safety Line & Borderline: Implement a "Safety Line" that triggers warnings when a hand approaches the shredder. If a hand crosses the "Borderline," the machine is automatically shut down.

### Run 
create conda env
```base
conda create -p venv python=3.6 -y
```

activate conda env
```base
conda activate venv/
```

install all requirements
```base
pip install -r requirements.txt
```

Run Python file
```base
python hand_detection.py
```

for closing enter q key