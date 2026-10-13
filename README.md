# Phân tích dữ liệu Dạy và Học AI ở Đại học Việt Nam và Thế giới

Dự án bài tập giữa kỳ thực hiện trọn vẹn quy trình Phân tích Dữ liệu, kết quả cuối cùng được tổng hợp trực quan thành một **Dashboard tĩnh (HTML)** chạy trực tiếp trên trình duyệt.

---

## 1. Đặt vấn đề & Chủ đề nghiên cứu

### 📍 Đặt vấn đề
Sự bùng nổ của Trí tuệ Nhân tạo (AI) đặt ra thách thức và cơ hội lớn cho giáo dục đại học. Việc so sánh chương trình đào tạo, xu hướng phát triển và mức độ đáp ứng thực tế giữa các trường đại học tại Việt Nam và thế giới giúp nhìn nhận rõ khoảng cách và định hướng cải tiến.

### 🎯 Chủ đề cụ thể
> **"Dạy và học AI ở đại học Việt Nam và thế giới: So sánh xu hướng, chương trình đào tạo và mức độ đáp ứng nhu cầu thực tế."**

---

## 2. Công cụ, Thư viện & Cấu trúc Dashboard (File `index.html`)

Dự án sử dụng Python để xử lý dữ liệu và xuất ra một trang dashboard tĩnh độc lập (`index.html`). Khi mở file này bằng trình duyệt web, người dùng có thể tương tác trực tiếp với toàn bộ biểu đồ tổng hợp.

### 🧰 Thư viện sử dụng
* **Thu thập & Tiền xử lý:** `requests`, `BeautifulSoup`, `pandas`, `numpy` (làm sạch dữ liệu, xử lý missing values, tạo cột đặc trưng).
* **Trực quan hóa & Xuất Dashboard:** `plotly` (hoặc `altair`/`bokeh`) để tạo các biểu đồ tương tác nhúng vào trang HTML.
* **Hỗ trợ bổ trợ:** `seaborn`, `matplotlib`, `wordcloud`, `networkx`, `folium`.

### 📊 Các dạng biểu đồ tích hợp trên Dashboard (`index.html`)
1. **Phân bố dữ liệu:** Histogram, Boxplot, Violin plot (thống kê phân phối điểm số, thời lượng khóa học).
2. **Xu hướng theo thời gian:** Line chart và Area chart (sự phát triển số lượng môn học AI qua các năm).
3. **Mối quan hệ & Hồi quy:** Scatter plot kết hợp đường hồi quy (tương quan giữa học phí/thời gian học và mức độ hiệu quả).
4. **Ma trận tương quan:** Heatmap tương quan giữa các biến số chính.
5. **Cấu trúc & Không gian:** Treemap / Sunburst hoặc Bản đồ tương tác (phân bổ trung tâm đào tạo AI).
6. **Phân tích văn bản:** WordCloud / Network Graph (từ khóa công nghệ AI phổ biến).
7. **Biểu đồ tương tác:** Tối thiểu 3 biểu đồ tương tác trực tiếp (Filter, Hover, Zoom) tích hợp sẵn trên giao diện HTML.

---

## 3. Kết luận & Insight rút ra

Từ Dashboard trực quan trên `index.html`, các kết luận chính được rút ra:
* **Khác biệt về chương trình:** Các trường đại học trên thế giới có xu hướng tập trung mạnh vào các môn chuyên sâu và ứng dụng thực tế sớm hơn, trong khi đại học Việt Nam đang trong quá trình chuẩn hóa khối kiến thức nền tảng.
* **Tốc độ phát triển:** Số lượng khóa học AI ghi nhận sự tăng trưởng mạnh mẽ trong giai đoạn gần đây, phản ánh nhu cầu cấp thiết của thị trường lao động công nghệ.
* **Từ khóa trọng tâm:** Các công nghệ như Machine Learning, Deep Learning, và Large Language Models chiếm tỷ trọng áp đảo trong từ vựng chuyên ngành được giảng dạy.

---

## 🚀 Hướng dẫn mở và xem báo cáo
1. Clone hoặc tải repository về máy.
2. Mở thư mục dự án và tìm file **`index.html`**.
3. Nhấp đúp chuột vào file `index.html` (hoặc kéo thả vào trình duyệt Chrome/Edge/Firefox bất kỳ) để trải nghiệm Dashboard tương tác hoàn chỉnh.
