# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-E402
**Name:** Đoàn Văn Tuấn
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1200. | 10 | Data da duoc xu ly, vi the ket qua tra loi da loai bo di nhung ket qua khong hop le|
| Garbage Data (`garbage_data.csv`) | Agent: Based on my data, the best choice is Nuclear Reactor at $999999. | 1 | Data chua duoc xu ly, vi the ket qua tra loi bi nhieu, khong hop ly trong thuc te.|

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Viet nhan xet cua ban o day — it nhat 50 tu)

(Hay phan tich cac van de nhu Duplicate IDs, wrong data types, outliers, null values
va giai thich tai sao chung anh huong den ket qua cua Agent.)
- Việc dữ liệu trùng lặp ID dẫn đến khi query, kết quả retrieval không đúng, không chính xác hoặc thừa thãi, dẫn đến gây sai hoặc bối lỗi cho LLM.
- Việc sai Data type có thể gây đến những lỗi tính toán và so sánh sau này trước khi đưa vào LLM.
- Outlier làm sai kết quả tính toán hoặc làm model đưa ra những kết quả thiên lệch.
- Null values làm sai kết quả tính toán, gây lỗi cho hệ thống.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

Em đồng ý với nhận định trên, vì dữ liệu đầu vào là yếu tố quan trọng nhất trong pipeline dữ liệu, nếu dữ liệu đầu vào không chính xác thì kết quả đầu ra cũng sẽ không chính xác.
