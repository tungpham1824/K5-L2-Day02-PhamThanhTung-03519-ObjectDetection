# Báo cáo cá nhân — Ngày 2 Object Detection

Đổi tên file theo `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md`. Điền kết quả thật, xóa dòng hướng dẫn khi nộp. Xem [quy định nộp](../../SUBMISSION.md).

## 1. Thông tin học viên

- Họ tên:Phạm Thanh Tùng 
- MSSV:03159        
- Email:tungpham1824@gmail.com
- Lớp:K5-L2A
- Link repo bài làm: https://github.com/tungpham1824/K5-L2-Day02-PhamThanhTung-03519-ObjectDetection.git
- Link Colab đã chạy:https://colab.research.google.com/drive/1aF--4NcgiNCJki9rooyk0P837ioOGS7q

## 2. Schema và mini guideline

Dẫn tới [GUIDELINE_MINI.md](../../GUIDELINE_MINI.md). Tóm tắt ba ca mơ hồ đã quyết định, cách áp dụng schema và phần cần giảng viên làm rõ.

## 3. Annotation và self-QC

- Số file nhãn train: 50
- Kết quả checker và lỗi đã xử lý:ĐẠT cấu trúc
- Danh sách ít nhất 10 ảnh đã rà bằng mắt: drive_050, drive_049, drive_044, drive_053, drive_057, drive_026, drive_027, drive_003, drive_019, drive_024
- Lỗi bỏ sót/box/class phát hiện khi rà và cách sửa:
- Commit khóa nhãn ban đầu: 11f318d

## 4. Gold QC và rework

| Chỉ số | Trước sửa | Sau sửa nếu có |
|---|---:|---:|
| TP |295 |551 |
| FP |216 |47 |
| FN |358 |102  |
| Precision |0.5773 |0.9214	 |
| Recall | 0.4518| 0.8438|
| F1 |0.5069| 0.8809	|
| mean_iou_of_matches |0.8006|0.8059|
| passed | false| true|

Dẫn tới `outputs/annotation_evaluation.json` trong repo. Nếu rework, ghi ảnh, lỗi đã kiểm, quyết định sửa/giữ và lý do. Không suy nguyên nhân chỉ từ FP/FN. Không có rework thì ghi rõ.

## 5. Kết quả YOLO

- Runtime, GPU/CPU, phiên bản Ultralytics và Torch: Google Colab, GPU Tesla T4 (CUDA:0), Python 3.13.16, Ultralytics 8.4.208, Torch 2.14.1+cu130. Huấn luyện 50 epoch mất khoảng 1.3 phút.
- Các tham số thay đổi so với notebook nếu có và lý do: Không đổi
- Đường dẫn best checkpoint trong phiên chạy: Day2-Lab/outputs/yolo26_runs/vehicle_annotation/weights/best.pt

| Chỉ số trên 10 ảnh eval | Giá trị |
|---|---:|
| Precision |0.5159903074053054 |
| Recall | 0.6464539007092198|
| mAP50 |0.5499556013782938 |
| mAP50–95 |0.3083999605341409 |

Đặt cả 2 folder `assets/eval_predictions/` và `assets/yolo26_runs/` (giải nén từ `day2_colab_outputs.zip`) cạnh báo cáo và dẫn link tương đối. Không chỉ ghi số; chỉ ra ít nhất một ảnh và vật thể cụ thể.

Trả lời bốn câu hỏi cuối notebook:

1. bus, recall 0.500 ,  drive_053.jpg và drive_057.jpg
2. cần kiểm độ khít box
3. van/car và bus/van (precision bus 0.151, van 0.435).
4. để tránh rò rỉ và mAP cao giả tạo. Trong notebook, eval là validation để tính metric từng epoch và chọn best.pt, nên không phải test set độc lập

## 6. Khó khăn và cách xử lý

| Bước/thời điểm | Lỗi quan sát | Cách đã thử | Kết quả/còn thiếu |
|---|---|---|---|
| Bước	Lỗi quan sát	Cách đã thử	Kết quả/còn thiếu
Gán nhãn ảnh cao tốc|Xe nhòe khó xác định lớp |Không đoán, ghi ca mơ hồ| |

## 7. Tự đánh giá theo rubric

Đối chiếu [RUBRIC.md](../../RUBRIC.md): phần nào đã có kết quả, phần nào còn thiếu hoặc chưa kiểm được. Không tự nhận hoàn thành bước chưa chạy.

## 8. Công cụ AI và tài liệu tham khảo

Ghi công cụ đã dùng, dùng ở bước nào và phần đã tự kiểm tra; không dùng thì ghi rõ. Liệt kê nguồn ngoài repo được sử dụng. Không ghi mật khẩu/token hoặc đính kèm gold train.
