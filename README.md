QR Code Scanner 📷🔍
This Python script scans an image file for a QR code, decodes the data, and saves the results (image name and QR code data) to a CSV file in an output folder. 🚀
Prerequisites ✅

Python 3.x 🐍
OpenCV (cv2) library 📸
CSV module (built-in) 📋
OS module (built-in) 🗂️

Install the required library:
pip install opencv-python

Directory Structure 📁
Ensure the following structure:
project_folder/
│
├── img/
│   └── img.jpg        # Input image containing a QR code 🖼️
├── output/
│   └── qrcodes.csv    # Output CSV file (created if it doesn't exist) 📄
├── script.py          # The Python script 🖥️

How It Works ⚙️

Loads an Image: The script reads an image file (e.g., img/img.jpg) using OpenCV. 📥
Detects QR Code: Uses OpenCV's QRCodeDetector to detect and decode any QR code in the image. 🔎
Extracts Image Name: Retrieves the base name of the image file (without the folder path). 📛
Saves to CSV: If a QR code is found, the script appends the image name and QR code data to output/qrcodes.csv. 💾
Output: Prints the QR code data and confirmation of saving to the CSV file. If no QR code is found, it prints a message indicating so. 🖨️

Usage 🚀

Place your image file (e.g., img.jpg) in the img/ folder. 📤
Ensure the output/ folder exists (the script will create qrcodes.csv if it doesn't exist). 📂
Run the script:python script.py



Example Output 📜
If a QR code is detected:
QR Code Data: https://example.com 🌐
✅ Saved to output Folder: (img.jpg, https://example.com)

If no QR code is found:
No QR code found. 😕

CSV Format 📊
The qrcodes.csv file will have the following structure:
image_name,qr_code_data
img.jpg,https://example.com

Notes 📝

Ensure the image contains a valid QR code. ✔️
The script appends to the CSV file (mode="a") to avoid overwriting existing data. 🔄
The image path in the script (img/img.jpg) should match the location of your input image. 🗺️
