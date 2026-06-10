[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112850&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** student@example.com
**Name:** Hikigaya

---

## Mo ta

Bài lab số 10 hướng dẫn xây dựng một pipeline ETL cơ bản và kiểm chứng tầm quan trọng của Data Quality. Quá trình bao gồm việc trích xuất (Extract) dữ liệu từ file JSON, kiểm tra và làm sạch (Validate) các bản ghi lỗi, biến đổi (Transform) định dạng và lưu trữ (Load) vào file CSV. Ngoài ra, tiến hành mô phỏng (Agent Simulation) để thấy sự khác biệt khi AI dùng dữ liệu sạch và dữ liệu rác.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

- Quá trình Validate dữ liệu: 3 bản ghi hợp lệ được giữ lại, 2 bản ghi bị loại (do giá trị nhỏ hơn hoặc bằng 0, hoặc thiếu danh mục).
- Pipeline đã xuất thành công 3 bản ghi hợp lệ vào file `processed_data.csv`.
- Thử nghiệm mô phỏng (`agent_simulation.py`) chứng minh rằng AI Agent chỉ đưa ra quyết định chính xác (mua Laptop giá $1200) khi được cung cấp bộ dữ liệu sạch. Dữ liệu rác (Garbage data) dẫn đến những suy luận sai lệch hoàn toàn.
