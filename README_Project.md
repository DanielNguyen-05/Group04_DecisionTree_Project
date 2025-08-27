# Dự án CSC14003: Nghiên cứu Cây Quyết Định
## Phân tích bài báo: "A cautionary tale on fitting decision trees to data from additive models: generalization lower bounds"

Dự án này là một phần của môn học CSC14003 - Nhập môn Trí tuệ Nhân tạo. Mục tiêu của dự án là phân tích sâu và thực hiện lại các thí nghiệm trong bài báo nghiên cứu của Tan, Y. S., Agarwal, A., & Yu, B. (2021) để kiểm chứng các kết luận lý thuyết về những hạn chế của cây quyết định khi áp dụng trên dữ liệu có cấu trúc cộng tính.

### Thông tin Nhóm
- **Nhóm:** 04
- **Thành viên:**
    - Lê Nhật Khôi - 23127004
    - Nguyễn Hải Đăng - 23127165
    - Võ Ngọc Bích Trâm - 23127271
    - Phan Quốc Thịnh - 23127486

---

### Cấu trúc Thư mục

Toàn bộ dự án được tổ chức theo cấu trúc thư mục dưới đây để đảm bảo tính rõ ràng và khoa học:

```
Group04_DecisionTree_Project/
|-- 01_Report/
|   |-- main_report.pdf         # File báo cáo chính
|   |-- references.bib          # File BibTeX chứa tài liệu tham khảo
|   `-- figures/                # Thư mục chứa các hình ảnh dùng trong báo cáo
|-- 02_Experiments/
|   |-- source_code/            # Toàn bộ mã nguồn để chạy thực nghiệm
|   `-- results/                # Thư mục lưu kết quả thực nghiệm 
|-- 03_Presentation/
|   |-- slides.pdf              # File trình chiếu cho buổi báo cáo cuối kỳ
|   `-- demo_materials/         # (Nếu có) Các tài liệu demo khác
`-- README_Project.md           # File hướng dẫn này
```

---

### Hướng dẫn Cài đặt và Thiết lập Môi trường

Để có thể chạy lại các thực nghiệm của chúng tôi, vui lòng thực hiện theo các bước sau.

#### 1. Yêu cầu cần có:
- **Python**: Phiên bản 3.8 trở lên.
- **Git**: Để sao chép (clone) mã nguồn dự án.

#### 2. Sao chép Dự án
Mở terminal hoặc command prompt và chạy lệnh sau:
```bash
git clone https://github.com/DanielNguyen-05/Group04_DecisionTree_Project.git
cd Group04_DecisionTree_Project
```

#### 3. Cài đặt các Thư viện cần thiết
Chúng tôi khuyến khích sử dụng một môi trường ảo (virtual environment) để tránh xung đột thư viện.

**Tạo môi trường ảo (tùy chọn nhưng được khuyến nghị):**
```bash
python -m venv venv
source venv/bin/activate  # Trên Linux/macOS
# Hoặc
venv\Scripts\activate  # Trên Windows```

**Cài đặt các gói phụ thuộc:**
Tất cả các thư viện cần thiết đã được liệt kê trong file `requirements.txt`. Chạy lệnh sau để cài đặt:
```bash
pip install -r 02_Experiments/source_code/requirements.txt
```
Các thư viện chính bao gồm:
- `numpy`
- `scikit-learn`
- `matplotlib`
- `pandas`
- `seaborn`

---

### Hướng dẫn Chạy Thực nghiệm

Các kịch bản thực nghiệm được viết bằng Python và đặt trong thư mục `02_Experiments/source_code/Simulations`.

Để chạy từng thực nghiệm tương ứng với mỗi biểu đồ trong bài báo, hãy chạy các file script riêng lẻ:

**Tái tạo Hình 5.1 (Mô hình tuyến tính, đặc trưng Boolean):**
Truy cập vào file linear_model_boolean.ipynb và bấm nút `Run All`

**Tái tạo Hình 5.2 (Mô hình tuyến tính, đặc trưng Liên tục - Uniform):**
Truy cập vào file linear_model_cts_features.ipynb và bấm nút `Run All`


**Tái tạo Hình 5.3 (Mô hình tổng bình phương, đặc trưng Liên tục - Uniform):**
Truy cập vào file sum_of_squares.ipynb và bấm nút `Run All`


### Xem Kết quả
Sau khi chạy thành công các kịch bản thực nghiệm, tất cả các biểu đồ kết quả (dưới dạng file `.png`) sẽ được tự động thể hiện ra dưới code trong các file

Các file kết quả sẽ được đặt tên tương ứng với biểu đồ mà chúng tái tạo, ví dụ: `figure_boolean.png`, `figure_linear.png`,...

---

### Tài liệu tham khảo
- **Bài báo gốc:** Tan, Y. S., Agarwal, A., & Yu, B. (2021). *A cautionary tale on fitting decision trees to data from additive models: generalization lower bounds*. arXiv preprint arXiv:2110.09626. [Link to paper](https://arxiv.org/abs/2110.09626)