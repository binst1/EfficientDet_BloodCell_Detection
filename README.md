# 🔬 Blood Cell Detection - EfficientDet

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Framework-red.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Đồ án môn học **Nhập môn Thị giác máy tính (CS231)** - Trường Đại học Công nghệ Thông tin (UIT). Dự án tập trung vào việc tự động hóa quá trình phân tích huyết học bằng cách phát hiện và đếm tế bào máu từ ảnh hiển vi y tế.

## 🎯 Mục tiêu đồ án
Giải quyết bài toán đếm tế bào máu thủ công vốn gây quá tải cho kỹ thuật viên y tế. Hệ thống sử dụng kiến trúc **EfficientDet-D0** để:
* Phát hiện chính xác: **Hồng cầu (RBC)**, **Bạch cầu (WBC)**, và **Tiểu cầu (Platelets)**.
* Thống kê số lượng từng loại tế bào trong thời gian thực.
* Hỗ trợ bác sĩ trong việc chẩn đoán các bệnh lý về máu.

## 📊 Kết quả đạt được
Mô hình EfficientDet-D0 sau khi được tinh chỉnh đạt các chỉ số ấn tượng trên tập dữ liệu BCCD:
* **mAP@0.50:** 89.32%
* **mAP@0.50:0.95:** 68.61%
* **Điểm nổi bật:** Khả năng phát hiện Tiểu cầu (Platelets) siêu nhỏ với độ chính xác (AP) lên đến **76.79%**.

## 🏗️ Kiến trúc hệ thống
* **Backbone:** EfficientNet-B0 (Pre-trained).
* **Neck:** BiFPN (Bi-directional Feature Pyramid Network) giúp cân bằng các đặc trưng đa quy mô.
* **Pipeline:** Tiền xử lý dữ liệu với `Albumentations` (Resize, ColorJitter, RandomBrightness).

## 🚀 Demo
Bạn có thể chạy ứng dụng demo trực tiếp qua giao diện web được dựng bằng Gradio:
*(Hướng dẫn: Sau khi chạy file `EfficientDet_BCCD_final.ipynb`, copy link `gradio.live` được sinh ra để truy cập ứng dụng).*

## 🛠️ Công nghệ sử dụng
- **Ngôn ngữ:** Python
- **Framework:** PyTorch, EfficientDet (timm)
- **Xử lý ảnh:** OpenCV, Albumentations
- **Quản lý dữ liệu:** Roboflow (BCCD Dataset)
