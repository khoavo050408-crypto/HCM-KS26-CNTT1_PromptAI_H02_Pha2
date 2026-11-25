# BÀI LÀM PHA 2 

- **Họ tên:** Võ Phan Đăng Khoa
- **Lớp:** HCM_KS26_CNTT1
- **Link repository Pha2:** https://github.com/khoavo050408-crypto/HCM-KS26-CNTT1_PromptAI_H02_Pha2.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
json
[
  {
    "ma_goi": "SVT",
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "FZ",
    "ngay_su_kien": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": null,
    "ghi_chu": "hỗ trợ xe lăn"
  },
  {
    "ma_goi": "VIP",
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "hỗ trợ tìm chỗ cho người khiếm thị"
  }
]

```

**Link trò chuyện:** https://share.gemini.google/VyFJfBZifKnT

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Dưới đây là chi tiết tính giá vé cho nhóm cổ động viên theo từng bước:

**Bước 1: Tiền người lớn**

* Nhóm có 5 người lớn, mua gói SVT (1.200.000 đồng/người lớn).
* Tiền người lớn = $5 \times 1.200.000 = 6.000.000$ đồng.

**Bước 2: Tiền trẻ em**

* Có 2 trẻ em trong độ tuổi từ 5 đến 11 (8 tuổi và 10 tuổi), mỗi trẻ tính 70% giá người lớn: $1.200.000 \times 70\% = 840.000$ đồng/trẻ.
* Bé 3 tuổi dưới 5 tuổi được miễn phí: $0$ đồng.
* Tiền trẻ em = $2 \times 840.000 + 0 = 1.680.000$ đồng.

**Bước 3: Tiền vé (tổng tiền người lớn + tiền trẻ em)**

* Tiền vé = $6.000.000 + 1.680.000 = 7.680.000$ đồng.

**Bước 4: Giảm giá nhóm (và tiền vé sau giảm)**

* Nhóm có 5 người lớn (đạt điều kiện từ 5 người lớn trở lên) nên được giảm 5% trên tiền vé.
* Số tiền được giảm = $7.680.000 \times 5\% = 384.000$ đồng.
* Tiền vé sau giảm = $7.680.000 - 384.000 = 7.296.000$ đồng.

**Bước 5: Phụ thu**

* Có 1 người lớn chọn khu ghế ưu tiên, phụ thu 300.000 đồng/người (không giảm giá).
* Phụ thu = $1 \times 300.000 = 300.000$ đồng.

**Bước 6: Tổng tiền**

* Tổng tiền = $7.296.000 + 300.000 = 7.596.000$ đồng.

[Kết quả : 7.596.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/aNfqRxU03qeR

### b) Kiểm tra kết quả AI

AI đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
"loai_su_co": "sai_khu_vuc",
"so_khach": 2,
"so_hiep_bi_anh_huong": 2,
"tom_tat": "2 khách vé SVT bị xếp sai sang khu không mái che khi mưa, ghế ướt trong 2 hiệp đầu."
}
```

**Link trò chuyện:** https://share.gemini.google/TjLd5FQxESPn

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **1. Đúng thông tin (50%)** | 0/5,0 | **Lỗi 1:**<br>

<br>1. Câu bị lỗi: "Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ."<br>

<br>2. Lý do sai: Giá vé gói Sân Vận Động (SVT) chuẩn của Ban tổ chức là 1.200.000 đồng/người lớn, không phải 1.000.000đ/người.<br>

<br>3. Câu sửa đề xuất: "Dạ chào anh, vé gói Sân Vận Động (SVT) bên em có giá 1.200.000 đồng/người lớn ạ."<br>

<br>

<br>**Lỗi 2:**<br>

<br>1. Câu bị lỗi: "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."<br>

<br>2. Lý do sai: Theo chính sách chuẩn của Ban tổ chức, huỷ vé từ 3 đến 6 ngày trước sự kiện chỉ được hoàn 50% (chỉ huỷ từ 7 ngày trở lên mới được hoàn 100%).<br>

<br>3. Câu sửa đề xuất: "Nếu anh huỷ vé trước trận đấu 3 ngày (thuộc khung từ 3 đến 6 ngày trước sự kiện), bên em sẽ hỗ trợ hoàn 50% giá trị vé ạ." | **Lỗi 1:**<br>

<br>1. Câu bị lỗi: "Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ."<br>

<br>2. Lý do sai: Giá vé gói Sân Vận Động (SVT) chuẩn của Ban tổ chức là 1.200.000 đồng/người lớn, không phải 1.000.000đ/người.<br>

<br>3. Câu sửa đề xuất: "Dạ chào anh, vé gói Sân Vận Động (SVT) bên em có giá 1.200.000 đồng/người lớn ạ."<br>

<br>

<br>**Lỗi 2:**<br>

<br>1. Câu bị lỗi: "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."<br>

<br>2. Lý do sai: Theo chính sách chuẩn của Ban tổ chức, huỷ vé từ 3 đến 6 ngày trước sự kiện chỉ được hoàn 50% (chỉ huỷ từ 7 ngày trở lên mới được hoàn 100%).<br>

<br>3. Câu sửa đề xuất: "Nếu anh huỷ vé trước trận đấu 3 ngày (thuộc khung từ 3 đến 6 ngày trước sự kiện), bên em sẽ hỗ trợ hoàn 50% giá trị vé ạ." |
| **2. Đầy đủ (30%)** | 1,0/3,0 | **Lỗi 1:**<br>

<br>1. Câu bị lỗi: "Anh cần gì cứ nhắn em nhé!" (và toàn bộ câu trả lời không đề cập đến thông tin đặt vé).<br>

<br>2. Lý do sai: Nhân viên chưa chủ động mời khán giả cung cấp ngày trận đấu và số lượng vé để hỗ trợ đặt vé theo yêu cầu của rubric.<br>

<br>3. Câu sửa đề xuất: "Để em hỗ trợ anh đặt vé trận bán kết nhanh chóng, anh vui lòng cho em xin ngày trận đấu dự kiến và số lượng vé anh cần đặt nhé ạ." | **Lỗi 1:**<br>

<br>1. Câu bị lỗi: "Anh cần gì cứ nhắn em nhé!" (và toàn bộ câu trả lời không đề cập đến thông tin đặt vé).<br>

<br>2. Lý do sai: Nhân viên chưa chủ động mời khán giả cung cấp ngày trận đấu và số lượng vé để hỗ trợ đặt vé theo yêu cầu của rubric.<br>

<br>3. Câu sửa đề xuất: "Để em hỗ trợ anh đặt vé trận bán kết nhanh chóng, anh vui lòng cho em xin ngày trận đấu dự kiến và số lượng vé anh cần đặt nhé ạ." |
| **3. Giọng điệu (20%)** | 1,0/2,0 | **Lỗi 1:**<br>

<br>1. Câu bị lỗi: "Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ."<br>

<br>2. Lý do sai: Cụm từ "xem rất đã luôn" mang tính suồng sã, khẩu ngữ quá mức, chưa giữ được sự chuyên nghiệp của chăm sóc khán giả sự kiện.<br>

<br>3. Câu sửa đề xuất: "Vé gói Sân Vận Động có tầm nhìn trực tiếp và trải nghiệm trọn vẹn tại sân dành cho khán giả ạ."<br>

<br>

<br>**Lỗi 2:**<br>

<br>1. Câu bị lỗi: "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."<br>

<br>2. Lý do sai: Trợ từ "nha" tạo cảm giác thân mật/suồng sã thiếu chuẩn mực trong tư vấn chính sách của Ban tổ chức.<br>

<br>3. Câu sửa đề xuất: "Nếu anh huỷ vé trước trận đấu 3 ngày, chính sách bên em áp dụng mức hoàn tiền 50% ạ." | **Lỗi 1:**<br>

<br>1. Câu bị lỗi: "Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ."<br>

<br>2. Lý do sai: Cụm từ "xem rất đã luôn" mang tính suồng sã, khẩu ngữ quá mức, chưa giữ được sự chuyên nghiệp của chăm sóc khán giả sự kiện.<br>

<br>3. Câu sửa đề xuất: "Vé gói Sân Vận Động có tầm nhìn trực tiếp và trải nghiệm trọn vẹn tại sân dành cho khán giả ạ."<br>

<br>

<br>**Lỗi 2:**<br>

<br>1. Câu bị lỗi: "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."<br>

<br>2. Lý do sai: Trợ từ "nha" tạo cảm giác thân mật/suồng sã thiếu chuẩn mực trong tư vấn chính sách của Ban tổ chức.<br>

<br>3. Câu sửa đề xuất: "Nếu anh huỷ vé trước trận đấu 3 ngày, chính sách bên em áp dụng mức hoàn tiền 50% ạ." |

Tổng điểm: 2/10
```

**Link trò chuyện:** https://share.gemini.google/6eVxWpcLss9V
