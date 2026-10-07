# 🏎️ JetRacer Autonomous Car

Dự án điều khiển và tự hành cho mô hình xe **JetRacer** chạy trên nền tảng **NVIDIA Jetson**.

---

## 🛠️ Cấu trúc dự án

* **`car.py` & `config.py`**: Lớp điều khiển xe cấp cao (lái, ga) và cấu hình phần cứng.
* **`drivers/`**: Driver giao tiếp I2C/PWM (`PCA9685`, `Servo`, `ESC`, `INA219`).
* **`web_control/`**: Giao diện Web điều khiển từ xa, xem camera trực tuyến & thu thập dữ liệu (Dataset).
* **`line_following/`**: Chế độ bám làn đường bằng xử lý ảnh (OpenCV + PID).
* **`auto_car/`**: Tự hành bằng AI/Deep Learning (PyTorch & tối ưu TensorRT).

---

## 🚀 Hướng dẫn nhanh

### 1. Chạy Web Điều khiển & Thu thập dữ liệu
```bash
python3 web_control/main.py
```
👉 Truy cập giao diện web tại: `http://<IP_JETSON>:5000`

### 2. Chạy bám làn đường (Line Following)
```bash
python3 line_following/main.py
```


---

## ⚙️ Cấu hình phần cứng
Chỉnh sửa thông số kênh PWM, giới hạn góc lái, dải ga tại file [`config.py`](file:///home/baymax/Jetson/config.py).
