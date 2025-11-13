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

![Use Darker Background](use_darker_bg.png)  
![Move Closer](move_closer.png)  
![Move Away](move_away.png)  
![Adjust Angle](adjust_angle.png)  
![Hold Still](hold_still.png)  
![Adjust Crop](adjust_crop.png)  

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
