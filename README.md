## Smart-Attendance-System-OpenCV

# Smart Attendance System using Face Recognition:
- This project is a smart attendance system that utilizes the power of face recognition to automate the process of recording attendance.
- The system is capable of recognizing individuals based on their faces and marking their attendance in a CSV file, along with the time they logged in.

# Features:
- Automatically detects and recognizes faces using a webcam feed.
- Compares detected faces with a set of pre-fed images to identify known individuals.
- Marks the attendance of recognized individuals by logging their names and login times.
- Provides real-time visual feedback by drawing rectangles around detected faces and displaying recognition results on the webcam feed.
  
# How it Works:
- Pre-stored images of known individuals are stored in a folder (in this case: "ImagesAttendance" folder in my system). 
  Create a similiar folder in yours accordingly.
- The system generates face encodings for these known images using the face_recognition library.
- The program captures video from the webcam and detects faces in real-time using OpenCV.
- Detected faces are compared with the known face encodings to recognize individuals.
- If a match is found, the individual's name is displayed on the webcam feed, and their attendance is logged.
- If a close match is found but not a perfect match, the attendance is still logged.
- If no match is found, "Unknown" is displayed on the webcam feed.

# Setup and Usage:
1. Clone this repository to your local machine.
2. Open PyCharm and go to "File" > "Open" to open the cloned repository folder.
3. In PyCharm, create a virtual environment for the project:
   - Click on "File" > "Settings" (or "PyCharm" > "Preferences" on macOS).
   - In the left pane, navigate to "Project: <your_project_name>" > "Python Interpreter".
   - Click on the gear icon and select "Add" to create a new virtual environment.
   - Choose the location and base interpreter for the virtual environment.
4. Install the required dependencies:
   - Open the terminal within PyCharm.
   - Run the command: `pip install -r requirements.txt`.
5. Add images of known individuals to the "ImagesAttendance" folder.
6. Run the script:
   - Open the `attendance_system.py` script in PyCharm.
   - Right-click within the script and select "Run 'attendance_system'".
   - The webcam feed will display real-time face recognition results.
7. The program will automatically mark attendance and display recognized names on the webcam feed.

# Note:
- Make sure to have a working webcam connected to your machine.
- Adjust the threshold values and parameters in the script as needed for your environment.
- Feel free to contribute or modify the project according to your requirements!
