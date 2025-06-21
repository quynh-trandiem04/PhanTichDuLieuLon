# 🏞️ Hệ Thống Lakehouse Xử Lý Dữ Liệu Không Khí – Nhóm 3 (Big Data Analytics)

## 🏫 Trường Đại học Sư phạm Kỹ thuật TP.HCM  
**Khoa Công nghệ Thông tin**  
**Môn học**: Phân tích dữ liệu lớn  
**GVHD**: Th.S Lê Thị Minh Châu  
**Học kỳ II – Năm học 2024–2025**

---

## 📌 Mô tả dự án

Đồ án triển khai hệ thống xử lý dữ liệu chất lượng không khí tại TP.HCM theo kiến trúc **Lakehouse**, sử dụng cả dữ liệu **batch** (CSV) và **streaming** (API). Hệ thống tích hợp các công cụ như **Kafka, Spark, Airflow, HDFS, Delta Lake**, kết hợp **Power BI** để trực quan hóa, chạy trên cục bộ **Ubuntu** và sau đó dùng **Azure Databricks** để triển khai trên Cloud.  
Dự án hướng tới xây dựng pipeline dữ liệu tự động, kết hợp với mô hình học máy như **Random Forest**, **SARIMA** để phân loại và dự báo chỉ số PM2.5, hỗ trợ ra quyết định môi trường.

---

## 🧩 Thành viên nhóm 3

| MSSV      | Họ và tên                 |
|-----------|---------------------------|
| 21151305  | Nguyễn Thị Hồng Thơ       |
| 22133046  | Trần Diễm Quỳnh           |
| 23133060  | Phạm Quỳnh Thư            |
| 23133015  | Nguyễn Ngọc Hiếu Hảo      |
| 22133037  | Vy Gia Nghi               |

---

## 📋 Phân công công việc nhóm

| Thành viên              | Công việc chính                                                                 |
|-------------------------|---------------------------------------------------------------------------------|
| **Nguyễn Thị Hồng Thơ** | - Cài đặt Kafka<br>- Thu thập dữ liệu streaming từ API<br>- Xử lý 3 lớp dữ liệu<br>- Xây dựng mô hình SARIMA |
| **Trần Diễm Quỳnh**     | - Xử lý dữ liệu lớp Silver<br>- Trực quan hóa dữ liệu bằng Power BI<br>- Cài đặt Airflow<br>- Thiết lập ETL tự động cho dữ liệu batch |
| **Phạm Quỳnh Thư**      | - Xây dựng Lakehouse trên Azure Databricks<br>- Xây dựng mô hình Random Forest và CatBoost<br>- So sánh dự đoán PM2.5 |
| **Nguyễn Ngọc Hiếu Hảo**| - Cài đặt Kafka & Airflow<br>- Thiết lập pipeline ETL cho batch và streaming |
| **Vy Gia Nghi**         | - Đưa dữ liệu vào HDFS<br>- Xử lý lớp Bronze và Silver<br>- Trực quan bằng Power BI<br>- Viết báo cáo, tổng hợp nội dung |

---

## 🧠 Chức năng chính

- Thu thập dữ liệu không khí từ API và file CSV
- Xử lý và làm sạch dữ liệu qua 3 lớp: **Bronze – Silver – Gold**
- Huấn luyện mô hình:  
  - **Random Forest** phân loại mức độ ô nhiễm  
  - **SARIMA** dự báo PM2.5 theo chuỗi thời gian
- Lưu trữ kết quả mô hình ở **Platinum Layer**
- Tự động hóa pipeline với **Apache Airflow**
- Trực quan hóa dữ liệu bằng **Power BI**
- Mở rộng triển khai trên **Azure + Databricks**

---

## 🔧 Công nghệ sử dụng

- **Apache Kafka** – Ingest dữ liệu thời gian thực  
- **Apache Spark (PySpark)** – Xử lý dữ liệu & huấn luyện ML  
- **Apache Airflow** – Orchestrate pipeline ETL  
- **HDFS + Delta Lake** – Lưu trữ phân tán có ACID  
- **Power BI** – Trực quan hóa dữ liệu  
- **Azure + Databricks** – Triển khai cloud  

---

## 🚀 Cách triển khai hệ thống

1. **Cài đặt Kafka, Spark, Airflow và HDFS** theo hướng dẫn trong file `docs/setup.md`
2. **Chạy các DAG trong Airflow** để tự động ingest, xử lý và lưu dữ liệu
3. **Huấn luyện mô hình ML** từ lớp Silver → Platinum
4. **Truy xuất kết quả** từ Delta Table để trực quan hóa trên Power BI
5. **Triển khai mở rộng** trên Azure bằng Databricks + Storage Gen2

---

## 📚 Tài liệu đính kèm

- Báo cáo đồ án (PDF)
- File DAG Airflow
- Script xử lý PySpark và mô hình ML
- ERD kiến trúc dữ liệu Lakehouse
- Dashboard Power BI
- Tập dữ liệu mẫu

---
