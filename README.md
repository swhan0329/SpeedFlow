# 🚀 SpeedFlow: Optical Flow-based Vehicle Speed Estimation

**SpeedFlow** is a lightweight, AI-free vehicle speed estimation project that utilizes **Farneback Optical Flow** to analyze motion from CCTV footage. It provides **real-time speed visualization** with **flow vectors, heatmaps, and km/h conversion**, making it ideal for research, traffic monitoring, and computer vision applications.

---

## 📌 Features

✅ **Real-time vehicle speed estimation** using **Farneback Optical Flow**  
✅ **Motion flow visualization** with arrow vectors and speed heatmaps  
✅ **Frame-by-frame speed conversion** from pixels to real-world km/h  
✅ **Lightweight, AI-free implementation** (pure OpenCV-based)  
✅ **Customizable parameters** for accuracy tuning (FPS, px-to-meter scaling)  

---

## 📂 Project Structure

```
📂 SpeedFlow
 ├── 📜 README.md        # Project overview & setup instructions
 ├── 📜 requirements.txt # Dependencies (OpenCV, NumPy)
 ├── 📂 src              # Source code
 │   ├── speed_estimator.py  # Main script for Optical Flow speed detection
 │   ├── utils.py        # Helper functions (visualization, calibration)
 ├── 📂 samples          # Example vehicle footage for testing
 ├── 📜 LICENSE          # Open-source licensing info
```

---

## ⚙️ Installation & Setup

1️⃣ Clone the repository  
```bash
git clone https://github.com/swhan0329/SpeedFlow.git
cd SpeedFlow
```

2️⃣ Install dependencies  
```bash
pip install -r requirements.txt
```

3️⃣ Run the speed estimation script  
```bash
python src/speed_estimator.py --video samples/car_video.mp4
```

---

## 🎯 How It Works

1. **Extracts frames** from the input video
2. **Computes Optical Flow (Farneback method)** between consecutive frames
3. **Visualizes movement** using motion vectors & heatmaps
4. **Converts pixel displacement to real-world speed (km/h)**

> 💡 Example speed calculation:  
> If a vehicle moves **50 pixels per frame**, and **1 px ≈ 0.2 meters**, at **30 FPS**:  
> `Speed = (50 px × 0.2 m/px) × 30 fps = 10 m/s = 36 km/h`

---

## 🛠 Customization & Tuning

You can fine-tune the speed estimation by adjusting:
- **`px_to_meter`** (pixel-to-meter conversion factor)
- **`step`** (grid spacing for flow vector visualization)
- **`arrow_length`** (vector scale for optical flow arrows)

---

## 🔥 Future Improvements

🔹 **Support for Lucas-Kanade Optical Flow** for better feature tracking  
🔹 **Kalman Filtering** for smoother speed estimation  
🔹 **Camera calibration tools** for automatic real-world scale conversion  
🔹 **Multi-object tracking integration** for multiple vehicle analysis  

---

## 📜 License

This project is licensed under the **MIT License**. Feel free to modify and contribute!

---

## 💬 Contact & Contributions

🔗 **GitHub Issues & PRs Welcome!**  
💌 **Email:** swhan0329@gmail.com

🚀 If you find this project useful, don't forget to ⭐ star the repo! Happy coding! 🚗💨

