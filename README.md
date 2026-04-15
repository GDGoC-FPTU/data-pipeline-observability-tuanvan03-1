[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574041&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** 26ai.tuandv@vinuni.edu.vn
**Student ID:** AI20K-0046
**Name:** Đoàn Văn Tuấn

---

## Mo ta

Trong labcode này, em đã xây dựng một pipeline ETL đơn giản để xử lý dữ liệu từ file JSON. Pipeline này bao gồm các bước:

1. **Extract**: Đọc dữ liệu từ file JSON.
2. **Validate**: Kiểm tra và loại bỏ dữ liệu không hợp lệ.
3. **Transform**: Chuẩn hóa category và tính giá giảm 10%.
4. **Load**: Lưu kết quả ra file CSV.

Đồng thời thực hiện so sánh và đánh giá trên 2 bộ dữ liệu processed_data và garbage để đưa ra những nhận định đúng đắn về vấn đề cần thiết phải xử lý dữ liệu thật tốt trước khi tiến hành làm các công việc tính toán thống kê, đưa vào DB hoặc đưa vào mô hình LLM, Agent.
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
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```
- Trước hết hoàn thành file solution, file này tạo ra bộ dữ liệu sạch cho processed_data theo như các yêu cầu đề ra. 
- Tạo file garbage_data sử dụng file generate_garbage.py
- Chạy so sánh 2 bộ dữ liệu processed_data và garbage_data bằng agent_simulation.py

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

Đã xử lý 5 records từ file raw, trong đó có 2 records bị loại bỏ do không hợp lệ. Kết quả được lưu vào file processed_data.csv.
Tạo ra 5 records nhiễu cho garbage_data.csv