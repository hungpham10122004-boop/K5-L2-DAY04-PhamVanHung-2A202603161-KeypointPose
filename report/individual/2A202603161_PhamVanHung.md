# Báo cáo cá nhân — PhamVanHung-2A202603161





## 0. Thông tin học viên

- Họ tên: Phạm Văn Hùng
- MSSV: 2A202603161
- Email: **hungpham10122004@gmail.com**
- Link repository: **https://github.com/hungpham10122004-boop/K5-L2-DAY04-PhamVanHung-2A202603161-KeypointPose-Studentu**
- Phiên bản CVAT: 2.74.)
- Giờ bắt đầu: **[16:30]**
- Giờ kết thúc: **[18:50]**

## 1. Kiểm tra label (CP0)

Thông tin dưới đây được đọc từ trường `categories` trong JSON export. Tên label và thứ tự điểm được ghi lại theo chính file xuất; việc đối chiếu trực tiếp với Label Constructor trên CVAT và bảng chuẩn của lab vẫn cần học viên xác nhận.

| Label | Kiểu | Số điểm | Tên điểm đúng bảng của lab? | Đúng thứ tự? | Số cạnh |
|---|---|---:|---|---|---:|
| `person` | Skeleton | 17 | Có theo danh sách keypoints trong JSON; cần đối chiếu lại UI | Theo thứ tự trong JSON; cần đối chiếu bảng chuẩn | 19 |
| `face` | Skeleton | 13 | Có theo danh sách keypoints trong JSON; cần đối chiếu lại UI | Theo thứ tự trong JSON; cần đối chiếu bảng chuẩn | 13 |

- Danh sách điểm `person` trong JSON: `nose`, `left_eye`, `right_eye`, `left_ear`, `right_ear`, `left_shoulder`, `right_shoulder`, `left_elbow`, `right_elbow`, `left_wrist`, `right_wrist`, `left_hip`, `right_hip`, `left_knee`, `right_knee`, `left_ankle`, `right_ankle`.
- Danh sách điểm `face` trong JSON: `left_eye_outer`, `left_eye_inner`, `left_eye_upper`, `left_eye_lower`, `right_eye_outer`, `right_eye_inner`, `right_eye_upper`, `right_eye_lower`, `nose_tip`, `mouth_left`, `mouth_right`, `lip_upper`, `lip_lower`.
- Mẫu `person` dựng theo người quay mặt về camera (các điểm `left_*` nằm bên phải khung mẫu)? *lúc có lúc khôngiểblCon]**
- Cách đổi cờ `occluded` / `outside` cho*một điể* trên CVAT 2.74.1:** Ở mỗi object ở mỗi ảnh , bấm vào part,nếu muốn chuyển qua occluded thì bấm biểu tượng cái mắt (Switch hidden property) , nếu outside thì là biểu tượng cái khóa (switch lock property)**..

## 2. Số lượng đã gán và thời gian (CP1, CP2)

Kết quả đếm trực tiếp từ JSON export:

- Bộ `person`: 12 ảnh, 18 skeleton `person`; mỗi skeleton có 17 điểm (51 giá trị x/y/v).
- Bộ `face`: 8 ảnh, 8 skeleton `face`; mỗi skeleton có 13 điểm (39 giá trị x/y/v).

| Nhóm ảnh | Số ảnh | Số skeleton đã gán | Số người dưới 60 px (không gán) | Số poster / gương / màn hình bỏ qua | Thời gian (phút) |
|---|---:|---:|---:|---:|---:|
| `easy` | 5 | Chưa có mapping ảnh theo     0từ     0từ  g20hi nhận |
| `occluded` | 3 | Chưa có mapping ảnh theo     0từ     0từ  g20hi nhận |
| `back` | 2 | Chưa có mapping ảnh theo     0từ     0từa g20 ghi nhận |
| `small` | 1 | Chưa có mapping ảnh th    n0h     n0h   a20 ghi nhận |
| `crowd` | 1 | Chưa có mapping ảnh th    n1h     n0h   a30 ghi nhận |
| `faces`  08     n0h   a30 ghi nhận |
| **Tổng** | **20** |**1**xác**0**xác**140**ghi nhận** |

Phân bổ 18 skeleton `person`c từ JSON):

- `000000043500.jpg`: 2 skeleton
- `000000100510.jpg`: 1 skeleton
- `000000164659.jpg`: 1 skeleton
- `000000196283.jpg`: 1 skeleton
- `000000220045.jpg`: 1 skeleton
- `000000314154.jpg`: 1 skeleton
- `000000360811.jpg`: 2 skeleton
- `000000365099.jpg`: 1 skeleton
- `000000391222.jpg`: 2 skeleton
- `000000445187.jpg`: 1 skeleton
- `000000542160.jpg`: 3 skeleton
- `000000571665.jpg`: 2 skeleton

Phân bổ 8 skeleton `face`: mỗi ảnh có 1 skeleton — `face_10579.jpg`, `face_168953.jpg`, `face_204787.jpg`, `face_324513.jpg`, `face_421231.jpg`, `face_449454.jpg`, `face_505385.jpg`, `face_562485.jpg`.

- Số ảnh người đã xong ở mốc ph15n t2 điền] / 10**.
- Thời gian thực tế (phút60*ần tự điền]*80 **ầ ựđền·P *ần tự điền]**.
- Ảnh tốn thời gian nhấẢnh 542160.jpg vì nhiều ngườinh nà v saoCầntự m ả dựan quá trình làm thực tế]**.

## 3. Bảng ca khó (CP1, CP2)

Mục này cần ghi lại những điểm bạn thực sự phân vân giữa `v = 1` và `v = 0`, hoặc không chắc hướng trái/phải của người. JSON chỉ cho biết visibility cuối cùng, không thể xác định bạn đã phân vân ở điểm nào trong lúc annotate. Vì vậy| Ảnh | Người / mặt | Điểm | Cờ đã chọn | Phân vân giữa | Lý do chọn |
|---|---|---|---:|---|---|
| **542160.jpg** | 3/2| 15| 0| v=1 và v=0  | không thấy  | | n n): **[Cần tự viết theo các ca thực tế đã review]**.

## 5. Kiểm file xuất và kết quả tự kiểm (CP4)

Đã đọc trực tiếp `annotations/person_keypoints_default.json` trong từng ZIP và kiểm tra độ dài `keypoints`, các giá trị visibility, cũng như đối chiếu `num_keypoints` với số điểm có `v > 0`.

| File | Người / mặt kiểm (ảnh, thứ tự) | Số phần tử `keypoints` | Điểm `outside` ra `v = 0`, `occluded` ra `v = 1`? | `num_keypoints` khớp? |
|---|---|---:|---|---|
| `PhamVanHung_persons.zip` | `000000100510.jpg`, người #1 (annotation ID 3) | 51 | JSON có cả `v = 0` (9 điểm), `v = 1` (2 điểm) và `v = 2` (6 điểm); phù hợp quy ước COCO, nhưng chưa thể đối chiếu lại cờ trên UI | Có (`num_keypoints = 8`, bằng số điểm `v > 0`) |
| `PhamVanHung_persons.zip` | `000000314154.jpg`, người #1 (annotation ID 7) | 51 | JSON có `v = 0` (2 điểm), `v = 1` (3 điểm), `v = 2` (12 điểm); phù hợp quy ước COCO, nhưng chưa thể đối chiếu lại cờ trên UI | Có (`num_keypoints = 15`, bằng số điểm `v > 0`) |
| `PhamVanHung_faces.zip` | `face_324513.jpg`, mặt #1 (annotation ID 4) | 39 | JSON có `v = 1` (8 điểm) và `v = 2` (5 điểm), không có `v = 0`; chưa thể đối chiếu lại cờ trêneleton trên CVAT, chỉ sửa nếu xác định là lỗi trái/phải.

## 6. Ảnh chụp màn hình

1. Label `person` trong label constructor (đủ 17 điểm có tên):

   ![Label person](images/1_label_person.png)

2. Một người quay lưng đã gán, cờ đã đặt:

   ![Người quay lưng](images/2_nguoi_quay_lung.png)

3. Một khuôn mặt đã gán 13 điểm, phóng to vùng mắt:

   ![Khuôn mặt phóng to](images/3_mat_phong_to.png)

4. Một đoạn JSON xuất của một người (ảnh `000000314154.jpg`, người 1):

   ![JSON export](images/4_json_export.png)

Nguồn ảnh: COCO val2017 / Wikimedia Commons.

