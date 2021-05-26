#### **Facial Landmarks Detection Uisng dlib + openCv and with 5 point landmark**

_A. Using dlib frontal face detector and landmarkdetector_

**facial_landmarks.py**

Facial landmarks are used to localize and represent salient regions of the face, such as:

>* Eyes
>* Eyebrows
>* Nose
>* Mouth
>* Jawline
Detecting facial landmarks is therefore a two step process:

Step #1: Localize the face in the image.
Step #2: Detect the key facial structures on the face ROI.

The pre-trained facial landmark detector inside the dlib library is used to estimate the location of 68 (x, y)-coordinates that map to facial structures on the face.

**detect_face_parts.py**

Facial landmark detector implemented inside dlib produces 68 (x, y)-coordinates that map to specific facial structures. These 68 point mappings were obtained by training a shape predictor on the labeled iBUG 300-W dataset.
Using these coordinates extracted position of eye, eyebrows, nose , mouth and jawline.


**video_facial_landmarks.py**

The same dlib frontal face detector and shape detector is used in real time video.

_B. 5-point facial landmark detector_

5 point face landmarking model that is over 10x smaller than the 68 point model, runs faster, and works with both HOG and CNN generated face detections.
While the 68-point detector localizes regions along the eyes, eyebrows, nose, mouth, and jawline, the 5-point facial landmark detector reduces this information to:

2 points for the left eye
2 points for the right eye
1 point for the nose
