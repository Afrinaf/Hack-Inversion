# Hack-Inversion Competition
# Garbage Disposal Tracking and Eco-Sort Web App

## Overview
This web application helps users and administrators (municipalities) manage and track garbage disposal efficiently. It features a waste segregation module powered by a machine learning model to classify different types of waste, as well as a complaint system where users can report garbage issues in their area to the municipality by sharing their location.

### Key Features
- **User and Admin Login**: Users and admins have separate logins.
  - **User Login**: Users can:
    - Post complaints about garbage disposal issues by sharing their location.
    - Use a waste segregation module to classify waste into categories: Recyclable, Hazardous, Residual, and Food Waste.
  - **Admin Login**: Admins can:
    - View and manage complaints submitted by users.
    - Access a dashboard to manage user details and monitor the status of complaints.

- **Waste Segregation Module**: Users can upload or capture an image of waste, and the machine learning model will categorize it into:
  - **Recyclable Waste**
  - **Hazardous Waste**
  - **Residual Waste**
  - **Food Waste**

## Technologies Used
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: PHP (for user and admin management)
- **Machine Learning Model**: Python (for waste classification)
- **Libraries/Frameworks**:
  - **OpenCV**: For image processing and waste classification.
  - **cvzone**: For overlaying images and handling waste classification results.
  - **TensorFlow/Keras**: Pre-trained model used for classifying waste.
  
## Python Model Overview
The waste classification module uses a pre-trained machine learning model (`keras_model.h5`) to categorize waste. It reads input from the camera, processes the image, and returns the predicted class:
- **0**: Recyclable
- **1**: Hazardous
- **2**: Food Waste
- **3**: Residual Waste

Images of different waste categories and bins are used to visualize the waste and appropriate disposal bins in real-time.

### How it Works
1. The user captures an image of waste using their camera or uploads it.
2. The model processes the image and predicts the waste category.
3. The appropriate waste bin is displayed on the screen, indicating how the waste should be disposed of.


## Installation and Setup

### Requirements
- Python 3.x
- Flask
- TensorFlow/Keras
- OpenCV
- PHP (for backend)
- MySQL (for database)

### Steps to Run
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/GarbageDisposalApp.git
   cd GarbageDisposalApp
   ```
2. **Install Dependencies**:
   ```bash
   Install all the required libraries 
   ```
3. **Run the PHP Backend**:
   - Set up the PHP backend and MySQL database for user and admin management.
4. **Run the Python Waste Segregation Module**:
   ```bash
   python main.py
   ```
5. **Launch the Web Application**:
   - Access the app through `http://localhost` after starting both the PHP server.
   - admi username : ali
   - admin password :ali

## Future Enhancements
- Improve waste classification accuracy by training the model on a larger dataset.
- Add features for real-time tracking of garbage trucks.
- Implement notifications for users when their complaints are resolved.
- Enhance the UI for better user experience.

## License
This project is open-source and available under the MIT License.


