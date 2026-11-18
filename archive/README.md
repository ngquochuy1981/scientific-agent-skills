# Thư mục Lưu trữ Kỹ năng Khoa học (Skills Archive)

Thư mục này lưu trữ **145 kỹ năng chuyên ngành nghiên cứu khoa học chuyên sâu** (Sinh học, Hóa dược, Vật lý lượng tử, Thiên văn, Y sinh...) được tách ra từ kho gốc K-Dense nhằm tinh gọn repository, giúp AI Agent tập trung 100% vào các kỹ năng **Quản trị Kinh doanh, Tối ưu hóa Vận tải - Logistics và Phân tích Dữ liệu Điều hành**.

---

## 📁 Cấu trúc lưu trữ

```text
archive/
├── skills/                             # 145 thư mục skills được lưu trữ an toàn
│   ├── 13c-metabolic-flux/
│   ├── biopython/
│   ├── qiskit/
│   ├── rdkit/
│   └── ...
├── tests/                              # 127 bộ test suites tương ứng
│   ├── biopython/
│   ├── qiskit/
│   └── ...
├── skill-requirements-archived.toml    # Cấu hình môi trường Python cô lập của các skill lưu trữ
└── README.md                           # Tài liệu này
```

---

## 🔄 Hướng dẫn khôi phục một skill về lại `skills/` (nếu cần)

Nếu sau này anh muốn sử dụng lại bất kỳ skill nào (ví dụ `biopython`):

1. **Di chuyển skill về thư mục `skills/`:**
   ```bash
   mv archive/skills/<tên-skill> skills/
   ```

2. **Di chuyển bài test về thư mục `tests/` (nếu skill có test):**
   ```bash
   mv archive/tests/<tên-skill> tests/
   ```

3. **Cập nhật `tests/skill-requirements.toml`:**
   Mở file `archive/skill-requirements-archived.toml`, sao chép khối `[skills.<tên-skill>]` và dán vào cuối file `tests/skill-requirements.toml`.

4. **Kiểm tra tính hợp lệ:**
   ```bash
   uv run --python 3.13 --with pytest python -m pytest tests/_meta -q
   ```
