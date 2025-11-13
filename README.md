# 🎯 LiveEdgeDetection  

LiveEdgeDetection is an **Android + Web document detection library** built on top of OpenCV. It detects documents in **live camera mode**, allows you to adjust the crop using 4 edges, and performs **perspective transformation** on the cropped image.  

It works best with a **dark background** 🌑📄

---

## ✨ Features Implemented (Android + Web)

- 📷 **Live Camera Document Scanning**  
- ✂️ **Adjustable Crop** using detected edges  
- 🔄 **Perspective Transformation** of scanned images  
- 🌐 **Web Viewer** for scanned images  
- ⚡ **Fast & Efficient** using OpenCV and JNI  
- 🖼 **Supports Multiple Image Formats**  

---

## 🖼 Screenshots / GIFs

![App Screenshot 1](screenshots/screenshot1.png)  
![App Screenshot 2](screenshots/screenshot2.png)  
![GIF Demo](screenshots/demo.gif)  

---

## ⚙️ Setup Instructions

### 1️⃣ Android Dependencies
- Install **OpenCV Android SDK**
- Add **JNI (C/C++) support** via NDK
- Configure `build.gradle`:
```gradle
dependencies {
    implementation project(':opencv')
}
