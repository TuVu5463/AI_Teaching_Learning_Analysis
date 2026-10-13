# Phân tích & So sánh Khung Chương trình Đào tạo AI: Đại học Việt Nam và Thế giới

Dự án bài tập giữa kỳ môn Phân tích Dữ liệu. Repository thực hiện trọn vẹn quy trình Data Analysis Pipeline (Thu thập -> Tiền xử lý -> Khai phá -> Trực quan hóa) và xuất kết quả thành một **Dashboard tĩnh (`index.html`)** hiển thị trực tiếp trên trình duyệt.

---

## 1. Đặt vấn đề & Chủ đề nghiên cứu

### 📍 Đặt vấn đề
Trí tuệ Nhân tạo (AI) đang chuyển mình từ một nhánh nghiên cứu chuyên sâu thành hạt nhân của nền kinh tế số. Trước áp lực này, các trường đại học toàn cầu liên tục tái cấu trúc chương trình đào tạo. Việc đối sánh khung chương trình giảng dạy AI tại Việt Nam với các trường đại học hàng đầu thế giới sẽ giúp nhận diện khoảng cách về mặt lý thuyết, thực hành, tốc độ cập nhật công nghệ và định hướng ứng dụng.

### 🎯 Chủ đề cụ thể
> **"So sánh Khung chương trình đào tạo & Cấu trúc môn học AI giữa các trường Đại học tại Việt Nam và Thế giới."**

---

## 2. Dữ liệu & Phương pháp thu thập

Dự án khảo sát và phân tích dữ liệu chương trình đào tạo của **20 - 30 trường Đại học** (10-15 trường tại Việt Nam như UET, UIT, HUST, FPT, VinUni... và 10-15 trường thế giới như MIT, Stanford, CMU, NUS, NTU...):

* **Thu thập dữ liệu:** Sử dụng `requests` + `BeautifulSoup` cào dữ liệu syllabus/danh mục môn học từ website các trường ĐH, kết hợp khai thác `Coursera API` / `edX API`.
* **Tiền xử lý & Chuẩn hóa:** `pandas`, `numpy`
  * Chuẩn hóa đơn vị tín chỉ/thời lượng học.
  * Xử lý giá trị thiếu (missing values) ở các trường thông tin syllabus.
  * **Feature Engineering:** Tạo các cột mới như Tỷ lệ thực hành (`practical_ratio`), Phân loại nhóm môn (`ai_category`), Số lượng môn tiên quyết (`prereq_count`).

---

## 3. Công cụ & Hệ thống Biểu đồ tích hợp (`index.html`)

Toàn bộ kết quả được tổng hợp thành trang **Dashboard tĩnh (`index.html`)** tích hợp các biểu đồ tương tác cao.

### 🧰 Thư viện chính
* **Web Scraping & Processing:** `requests`, `beautifulsoup4`, `pandas`, `numpy`
* **Visualization:** `plotly`, `seaborn`, `matplotlib`, `folium`, `wordcloud`, `networkx`

### 📊 Danh mục Biểu đồ triển khai (Đáp ứng đầy đủ yêu cầu đề bài)

| STT | Dạng biểu đồ | Nội dung phân tích | Thư viện |
| :---: | :--- | :--- | :--- |
| **1** | **Boxplot / Violin Plot** | Phân bố số tín chỉ và tỷ lệ thời lượng thực hành giữa ĐH Việt Nam vs Thế giới. | `seaborn` / `plotly` |
| **2** | **Line / Area Chart** | Xu hướng tích hợp các môn AI mới (GenAI, LLM, MLOps) vào giảng dạy theo thời gian (2018 - 2026). | `plotly` |
| **3** | **Scatter Plot + Hồi quy** | Tương quan giữa **Số môn tiên quyết** và **Tỷ lệ bài tập lớn/thực hành** của môn học. | `seaborn` / `plotly` |
| **4** | **Heatmap Tương quan** | Mật độ phân bổ các nhóm môn học (`Math/Foundations`, `Classic ML`, `Deep Learning`, `Ethics`) theo Trường/Quốc gia. | `seaborn` / `plotly` |
| **5** | **Treemap / Sunburst & Bản đồ** | • **Treemap/Sunburst:** Tỷ trọng phân cấp các nhóm kiến thức trong ngành AI.<br>• **Folium Map:** Bản đồ không gian phân bố các đại học khảo sát. | `plotly`, `folium` |
| **6** | **WordCloud & Network Graph** | • **WordCloud:** Từ khóa công nghệ/thư viện nổi bật trong syllabus.<br>• **Network Graph:** Mạng lưới liên kết giữa các môn học và môn tiên quyết. | `wordcloud`, `networkx` |
| **⭐** | **Biểu đồ tương tác (3+)** | Sunburst phân cấp, Scatter plot hover chi tiết môn học, và Bản đồ Folium tương tác nhúng trực tiếp trên Dashboard. | `plotly`, `folium` |

---

## 4. Insight chính & Data Storytelling

Trang Dashboard trình bày báo cáo 1 trang theo mạch kể chuyện dữ liệu (Data Storytelling):

1. **Trọng tâm Đào tạo:** Đại học Việt Nam chú trọng nền tảng Toán và Cơ sở Khoa học Máy tính vững chắc, trong khi các trường thế giới cân bằng sớm hơn giữa lý thuyết và các môn ứng dụng chuyên sâu.
2. **Mạng lưới Môn học (Network Dependency):** Mạng lưới môn tiên quyết tại ĐH Thế giới có tính linh hoạt cao hơn, cho phép sinh viên tiếp cận các công cụ/ngôn ngữ lập trình AI từ năm 1–2.
3. **Tốc độ Cập nhật Công nghệ:** Các môn học về Large Language Models (LLMs) và Đạo đức AI (AI Ethics) bùng nổ tại các trường quốc tế từ 2023, và đang bắt đầu được tích hợp mạnh mẽ vào chương trình tại Việt Nam từ giai đoạn 2024-2026.
4. **Định hướng Cải tiến:** Đề xuất tăng tỷ lệ đồ án thực tế (**Practical Ratio**) và mở rộng các môn học liên ngành trong khung chương trình đại học tại Việt Nam.


---

## 🚀 Hướng dẫn mở và xem Báo cáo Dashboard

1. **Clone repository:**
   ```bash
   git clone https://github.com/TuVu5463/AI_Teaching_Learning_Analysis
   cd AI_Teaching_Learning_Analysis
