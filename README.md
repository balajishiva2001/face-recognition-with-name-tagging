Face‑Recognition‑With‑Name‑Tagging

A simple yet effective system that detects faces, recognizes known individuals, and tags them with meaningful names in images or live video.
Built with Python, OpenCV, and the face_recognition library.

------------------------------------------------------------
🚀 Features
------------------------------------------------------------
- Face detection using camera or image input
- Face recognition by comparing to a set of known individuals
- Automatic naming of recognized people (filename → human‑readable name)
- Tags drawn on image/video (bounding boxes + names)
- Unknown faces labeled as “Unknown #1”, “Unknown #2”, etc.
- Easy to extend: just add more labeled face images to the known/ folder

------------------------------------------------------------
🧰 Tech Stack
------------------------------------------------------------
- Python 3.x
- OpenCV (cv2)
- face_recognition
- NumPy

------------------------------------------------------------
📁 Project Structure
------------------------------------------------------------
```
face‑recognition-with-name‑tagging/
├── known/                  # Folder to store known persons’ face images
│   ├── john_doe.jpg
│   ├── jane‑smith.png
│   └── …
├── face_recognize_and_name.py  # Main script
├── README.txt                  # This file
└── requirements.txt            # Required Python libraries
```
Note: The known/ folder should contain one or more clear & front‑facing photos per person.
Use filenames that reflect the person’s name, e.g. john_doe.jpg or jane‑smith.png.

------------------------------------------------------------
▶️ How to Run
------------------------------------------------------------
1. Install dependencies
   pip install face_recognition opencv-python numpy

2. Prepare known faces
   Create a folder named known/ in the project directory and place labeled images there.

3. Run with webcam input
   python face_recognize_and_name.py --source webcam

4. Run with single image
   python face_recognize_and_name.py --source image --image-path path/to/photo.jpg

5. Quit the webcam window by pressing q.

------------------------------------------------------------
🧠 How It Works
------------------------------------------------------------
- Loads each image in known/, detects faces, and computes a face‑encoding vector.
- For an input image or video frame, detects and encodes all visible faces.
- Each detected face‑encoding is compared to known encodings.
- The closest match (below a threshold) is tagged with the person’s meaningful name.
- Unknown faces are labeled as “Unknown #n”.

------------------------------------------------------------
📈 Future Improvements
------------------------------------------------------------
- Support bulk processing of images or videos.
- Use a face database or metadata file instead of just folders.
- Add voice announcements of recognized names.
- Integrate with security cameras or Raspberry Pi.
- Add face tracking across frames.

------------------------------------------------------------
📄 License
------------------------------------------------------------
Specify your license here (e.g., MIT License) or remove this section if internal use only.

------------------------------------------------------------
👤 Author
------------------------------------------------------------
Balaji Shiva  
GitHub: https://github.com/balajishiva2001
