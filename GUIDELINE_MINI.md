# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` |Xe con chở người, xe bán tải |Cabin nhỏ, gầm thấp; bán tải cabin nhỏ vẫn là `car`, không phải `truck`|
| `truck` |  Xe tải chở hàng, xe đầu kéo  |Thùng hàng lớn hoặc đầu kéo; khác bán tải ở kích thước và thùng hàng  |
| `bus` | Xe buýt, minibus chở khách | Thân dài, nhiều cửa sổ dọc thân; khác `van` ở kích thước và số chỗ|
| `van` | Xe van, minivan chở hàng hoặc chở người| Thân hộp, cao hơn `car`, nhỏ hơn `bus`|

## Quy tắc chung

- Box bám sát vật thể nghĩa là: mỗi xe một box chữ nhật ôm sát phần thân xe nhìn thấy, không lấy thêm mặt đường, trời hay xe bên cạnh; hai xe chồng nhau thì mỗi xe một box riêng.
- Vật thể bị che khuất: vẫn vẽ box quanh phần nhìn thấy nếu nhận ra được lớp.
- Vật thể bị cắt bởi rìa ảnh: box chạm đúng rìa ảnh, không đoán phần nằm ngoài ảnh.
- Vật thể rất nhỏ/mơ hồ: nếu không xác định chắc lớp thì không tự đoán, ghi vào bảng ca mơ hồ.
## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_050` |Hai xe xám ở giữa ảnh, thân hộp, nóc cao, ở xa nên khó phân biệt van với car dạng SUV/MPV. |van, mỗi xe một box. |Cao và vuông hơn sedan xung quanh, nhỏ hơn xe buýt. |
| `drive_049` |Xe ở mép dưới và góc phải bị cắt bởi rìa ảnh, một xe hơi nhòe. |car, box chạm đúng rìa ảnh. |Theo quy tắc rìa ảnh, không đoán phần ngoài ảnh. Nóc thấp, không có thân hộp của van. |
| `drive_044` | Xe xám ở giữa-trái bị nhòe do chuyển động, khó xác định van hay car.|Không chắc thì bỏ qua và ghi vào bảng ca mơ hồ. |Theo quy tắc “mơ hồ thì không tự đoán”. |
