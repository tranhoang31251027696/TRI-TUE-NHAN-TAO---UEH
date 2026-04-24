# 🗺️ AI & Bản đồ không gian – Bài tập về nhà Buổi 1

Notebook Jupyter thực hành 15 bài tập ứng dụng AI và bản đồ không gian trong quản trị logistics & đô thị thông minh tại TP.HCM.

---

## 📋 Nội dung

| Bài | Chủ đề | Thư viện chính |
|-----|--------|---------------|
| 23.1 | Bản đồ tương tác vị trí UEH + 5 địa điểm lân cận | `folium` |
| 23.2 | Geocoding 10 địa chỉ + tính khoảng cách | `geopy`, `folium` |
| 23.3 | Heatmap mật độ đơn hàng + nhận xét quản trị | `folium.plugins.HeatMap` |
| 23.4 | Choropleth dân số / doanh thu các quận | `geopandas`, `folium` |
| 23.5 | Phân tích vùng phục vụ kho hàng (3/5/10 km) | `folium` |
| 23.6 | Mạng lưới giao thông đường bộ + thống kê | `osmnx` |
| 23.7 | Tìm đường ngắn nhất: Dijkstra vs A* | `osmnx`, `networkx` |
| 23.8 | Hệ thống gọi xe: ghép khách – tài xế gần nhất | `folium`, `scipy` |
| 23.9 | Phân cụm K-Means đề xuất vị trí kho | `sklearn`, `folium` |
| 23.10 | Bản đồ nguy cơ tắc nghẽn + tuyến đường thay thế | `networkx`, `folium` |
| 23.11 | Dự đoán nhu cầu gọi xe theo giờ / khu vực | `sklearn`, `folium` |
| 23.12 | Tối ưu tuyến giao hàng nhiều kho (MDVRP heuristic) | `scipy`, `folium` |
| 23.13 | Dashboard bản đồ đa lớp (điểm, vùng, tuyến) | `folium` |
| 23.14 | Mô phỏng xe di chuyển theo thời gian (AntPath) | `folium.plugins.AntPath` |
| 23.15 | Ứng dụng AI: đề xuất vị trí Hub vệ tinh last-mile | `sklearn`, `folium` |

---

## 🚀 Cài đặt & chạy

### 1. Clone repository
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Cài đặt thư viện
```bash
pip install folium geopy geopandas osmnx networkx scikit-learn scipy pandas numpy
```

> **Lưu ý:** Bài 23.2, 23.6, 23.7 cần kết nối internet để geocoding / tải dữ liệu OpenStreetMap.

### 3. Chạy notebook
```bash
jupyter notebook AI_BTVN_BUOI_1_revised.ipynb
```
Hoặc upload thẳng lên **Google Colab**.

---

## 🚀 Các tính năng và bài toán nổi bật
Trực quan hóa Dữ liệu Không gian (Spatial Visualization): * Xây dựng bản đồ tương tác đa lớp (multi-layer maps) với các Marker, FeatureGroup và LayerControl.

Vẽ biểu đồ nhiệt (Heatmap) và bản đồ phân vùng mật độ (Choropleth) để đánh giá tiềm năng thị trường theo khu vực.

Geocoding & Service Area Analysis: * Chuyển đổi địa chỉ văn bản thành tọa độ GPS (Geocoding).

Phân tích vùng phục vụ (Service Area) thông qua các bán kính phủ sóng để lên chiến lược giao hàng (same-hour delivery).

Phân tích Mạng lưới Giao thông (Network Routing): * Trích xuất và phân tích cấu trúc mạng lưới đường bộ bằng OSMnx.

Triển khai và so sánh hiệu năng của các thuật toán tìm đường đi ngắn nhất: Dijkstra (đảm bảo tối ưu tuyệt đối) vs A* (tối ưu hóa tốc độ phản hồi real-time với Heuristic).

Ứng dụng Machine Learning & Heuristic trong Logistics:

K-Means Clustering: Phân cụm tọa độ khách hàng để xác định vị trí trọng tâm (Centroids) tối ưu cho việc đặt các Hub vệ tinh last-mile, giúp giảm 20-35% chi phí vận chuyển.

Random Forest Regression: Xây dựng mô hình dự báo nhu cầu đặt xe/giao dịch không - thời gian (Spatio-temporal) để điều phối nguồn lực trước giờ cao điểm.

Nearest Neighbor Heuristic: Giải quyết bài toán ghép nối tài xế - khách hàng và tối ưu hóa lộ trình giao hàng đa điểm (MDVRP).

Dashboard Quản trị: Xây dựng bản đồ tổng hợp (Points, Lines, Polygons) hỗ trợ ra quyết định cạnh tranh và theo dõi luồng tuyến vận tải.

---

## 🛠️ Tech Stack (Công nghệ sử dụng)
Ngôn ngữ: Python

Xử lý & Mô hình hóa dữ liệu: pandas, numpy, scikit-learn, scipy

Phân tích Không gian & Đồ thị: geopandas, geopy, networkx, osmnx

Trực quan hóa Bản đồ: folium (kết hợp các plugins như HeatMap, AntPath, TimestampedGeoJson)

---

## 📁 Cấu trúc thư mục

```
.
├── 31251027696_AI_BTVN_BUOI_1.ipynb   # Notebook chính (15 bài)
└── README.md
```

> File `hcm_districts.geojson` và `hcm_districts.csv` được tạo tự động khi chạy bài 23.4.

---

## 🛠️ Yêu cầu môi trường

- Python >= 3.8
- Jupyter Notebook hoặc Google Colab
- Kết nối internet (bài 23.2, 23.6, 23.7)

---

## 📌 Ghi chú

- Tất cả dữ liệu địa lý là dữ liệu giả lập hoặc từ OpenStreetMap, chỉ phục vụ mục đích học tập.
- Bài 23.6 & 23.7: OSMnx >= v1.3 đã bỏ `ox.basic_stats()`, notebook đã cập nhật sang `ox.graph_to_gdfs()`.
