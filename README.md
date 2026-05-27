# 🧠 AI & Logic Mờ (Fuzzy Logic) – Bài tập về nhà Buổi 2

Notebook Jupyter thực hành các hệ thống điều khiển mờ (Fuzzy Control Systems) ứng dụng trong định giá vận tải hành khách, chiến lược chiết khấu thương mại điện tử và tối ưu hóa logistics.

---

## 📋 Nội dung

| Bài | Chủ đề | Thư viện chính |
| --- | --- | --- |
| **2.11** | Hệ thống tính giá cước Grab-Bike & Tiền thưởng tài xế | `skfuzzy`, `numpy` |
| **2.12** | Chiến lược chiết khấu cho cửa hàng Shopee (Tổng quát) | `skfuzzy` |
| **2.13** | Kế hoạch bán hàng & Chiết khấu sản phẩm xa xỉ (Luxury) | `skfuzzy` |
| **2.14** | Tối ưu hóa ghép đơn (Batching) & Ưu tiên giao hàng | `skfuzzy` |

---

## 🚀 Cài đặt & chạy

### 1. Cài đặt thư viện

Hệ thống sử dụng thư viện **scikit-fuzzy** để xây dựng các tập mờ và hệ thống luật.

```bash
pip install -U scikit-fuzzy numpy

```

### 2. Chạy notebook

Mở file bằng **Jupyter Notebook** hoặc upload lên **Google Colab**:

```bash
31251027696_AI_BTVN_BUOI_2.ipynb

```

---

## 🚀 Các tính năng và bài toán nổi bật

### Xây dựng Hàm liên thuộc (Membership Functions):

* Sử dụng các dạng hàm đa dạng: **Triangular** (`trimf`) và **Trapezoidal** (`trapmf`) để định nghĩa các mức độ (Thấp, Trung bình, Cao).
* Thiết lập các biến ngôn ngữ (Antecedents & Consequents) với dải giá trị (Universe) phù hợp cho từng bài toán thực tế (Rating 1-5 sao, Giao thông 0-100%,...).

### Hệ thống Luật Mờ (Fuzzy Rule Base):

* Triển khai hàng chục quy tắc logic `IF...AND...THEN` để mô phỏng tư duy ra quyết định của con người.
* **Bài toán Grab:** Kết hợp các yếu tố ngoại cảnh (Thời tiết, Giao thông) và hành vi (Đúng giờ) để tính toán giá và thưởng công bằng.
* **Bài toán Shopee:** Cân bằng giữa biên lợi nhuận và áp lực cạnh tranh để đưa ra mức Discount tối ưu giúp giữ chân khách hàng nhưng không lỗ vốn.

### Giải mờ & Ra quyết định (Defuzzification):

* Sử dụng phương pháp trọng tâm (**Centroid**) để chuyển đổi kết quả từ tập mờ sang giá trị số cụ thể (Crisp output).
* Hệ thống cho phép nhập dữ liệu real-time để dự đoán kết quả ngay lập tức (ví dụ: Giá cước dự kiến khi trời mưa và kẹt xe).

---

## 🛠️ Tech Stack (Công nghệ sử dụng)

* **Ngôn ngữ:** Python
* **Tính toán số học:** `numpy`
* **Logic mờ:** `scikit-fuzzy` (Bộ công cụ chuyên dụng cho hệ thống điều khiển mờ)

---

## 📁 Cấu trúc thư mục

```
.
├── 31251027696_AI_BTVN_BUOI_2.ipynb   # Notebook chứa toàn bộ mã nguồn
└── README.md                          # Hướng dẫn và mô tả dự án

```

---

## 🛠️ Yêu cầu môi trường

* Python >= 3.8
* Cài đặt thư viện `scikit-fuzzy` trước khi chạy các cell code.
* Notebook đã được xử lý các lỗi **KeyError** bằng cách mở rộng vùng chồng lấn (overlap) giữa các tập mờ, đảm bảo mọi giá trị đầu vào đều được bao phủ bởi ít nhất một luật.

---

## 📌 Ghi chú

* **Bài 2.14:** Đã hiệu chỉnh lại biến `traffic` (Low: 0-6, Medium: 3-8) để tránh lỗi tính toán khi dữ liệu rơi vào các điểm biên.
* Các mô hình có thể dễ dàng mở rộng bằng cách thêm các luật (rules) mới mà không cần thay đổi cấu trúc mã nguồn chính.