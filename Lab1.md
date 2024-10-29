# 1. Phân tích kiến trúc 
Đề xuất sử dụng kiến trúc MVC (Model-Controller-View) vì:
* Tách biệt giữa các thành phần: Giúp dễ dàng thay đổi giao diện hoặc quy trình nghiệp vụ mà không ảnh hưởng đến các phần còn lại của hệ thống. 
* Dễ mở rộng và bảo trì: Các thay đổi trong nghiệp vụ tính lương hay yêu cầu mới của nhân viên có thể được triển khai dễ dàng nhờ vào sự tách biệt giữa Model, View, và Controller.
* Bảo mật và kiểm soát: Phân quyền truy cập cho phép nhân viên chỉ xem và chỉnh sửa dữ liệu của mình, đồng thời quản trị viên có quyền quản lý cao hơn trong hệ thống.

Biểu đồ kiến trúc

![Diagram](https://www.planttext.com/api/plantuml/png/T5D1JiCm4BplArQzvmS8LHIEY0gXtXTdHKCSEx9TeGZbPHnu4b-WTXh5TXmffvd9xcHcy_VpkxUEZBjq4cpRA3JQCa1FegKFnjtpwR33Rq2yFWkeQvPsmX6596lngUkb7fW35-5lJSU2J9tZnuiHPxByOcesAvA6ZfMRuH7YxGUjdD5Iijcmi0ZIaUBCeYsIiyaY-SgzDYwXKaEdXhyoA_CsvxbIIgIkh_flp0JJiWoSxTtW4KQOY0TIhHsiumxX1XsD_cJXbWMFvEYTVAcR55RLFKwbGZJIer7OiCutIDBcrpa7KTBeXYOTjEuaYD9xohi9aYZ3f0UygwhI7PHB2Uh2ISLb14tXU63FglQ_r3y0003__mC0)
# 2. Cơ chế phân tích
BankSystem: Hệ thống bên ngoài mà tất cả các giao dịch gửi tiền trực tiếp được gửi đến.

**Cơ chế phân tích**: Legacy Interface

Employee: Một nhân viên được trả lương theo giờ.

**Cơ chế phân tích**: Persistence, Security

Paycheck: Bản ghi về số tiền mà một nhân viên được trả cho một kỳ trả lương nhất định.

**Cơ chế phân tích**: Persistence, Security

ProjectManagementDatabase: Cơ sở dữ liệu cũ chứa thông tin liên quan đến các dự án và số hiệu chi phí.

**Cơ chế phân tích**: Legacy Interface

PurchaseOrder: Bản ghi về một giao dịch bán hàng do một nhân viên thực hiện.

**Cơ chế phân tích**: Persistence, Security

Timecard: Thẻ chấm công chứa thông tin về số giờ làm việc của một nhân viên trong một khoảng thời gian nhất định.

**Cơ chế phân tích**: Persistence, Security

Cần cơ chế Legacy Interface vì cần phải làm việc với các hệ thống đã có

Cần cơ chế Persistence vì cần phải lưu trữ dữ liệu của hệ thống

Cần cơ thế Sercurity vì cần bảo mật thông tin cho các nhân viên

# 3. Phân tích Create Administrative Report
Basic flow:

![Diagram](https://www.planttext.com/api/plantuml/png/T9B1JiCm38RlVWgh9pZi1JYWRIr2I0WXEhXxhRj5f4c9KwO-6mSUYLV0NTk9TUAGW_qxlpyx-VdwNaga4DlQ0iYxSHYyC40qqJ8ccptZCtN1MukhiZREI0mKVS05vlpHiYiOCqExGBMcrYIcmChwGm90HLztl0LRtxgIGeV92pS-n3V3XmH9yFxr0GhledQOj7G8BOTZHPu2EyNfS92Xf4XR4XvZ0JZsmCLjxuOtOnutNSDpQSqx3ScLo7hKYGKhfOmwPnZiPpVkwiRwZXaTrNmbrm1zNkKyLJKDh1uJsTXu4bSJ2MXuCioCD9PEqromwr8bej0d_rFof21O6NintAClA1hlpWZpFqO3nhYscJOtopmwFt2S-MMiZzEDoqA0fIvIFyyl0000__y30000)

Alternative Flow:

Requested Information Unavailable

![Diagram](https://www.planttext.com/api/plantuml/png/P50xKiD03Err2etxN2054s8OXex9XrxsAg1XlGfQcOpFHi6Hk09h6nUGKde_FNr_VcsoatdVHO3y9WbDCmEuU6Ii3g-CJpIOneYtePCasOrS3LUuv_UUKyju9_HYr9NLbhAqU8fwgG2e7NcJ2XhjKo0RiDhnMSsVXIyLKiQ7uoEqchmaB5WzZv5jOknhu5JE6N268P1JGvb_vmmmPU3gPdJ3DHuJVP14Qae3IIUrZbmqmOWMqinUuxsPsfLuDxRAZgqn-PBnNxgGYlUVX2ktcig3uYAVTu5BlG5WmocKj_y0003__mC0)

Invalid Format or Insufficient Information

![Diagram](https://www.planttext.com/api/plantuml/png/R911JiD034NtFeMLVI_G1Iga2B408GhitSHjhKxiud6eSZOM78ahC6ceX2gM_dxsj__tvzSY1tdqNGB8Ur5qommG4ecnUjanFj7WbX9Ujvsev70ASvpXYjzxrePnARHrwefqGraQt2GxLW3KZDnf2jRMQqi-OFNC1_Du4pvMI1dlNk-XCOtYSExLKvdOJyIg1jPope1J6reAMbFctpe3d3nmTZLkmpa-Mk31xKDQqIsoMh_TeUZ6lACGKnYnGazZStoGd4VoBtAnybQ37Rj_m4kofX99EbjCsfBBGmF0WhKjGVy0003__mC0)

# 4. Phân tích Create Employee Report
Basic flow

![diagram](https://www.planttext.com/api/plantuml/png/Z91D3e8m48NtdA9BIF02BDm0YMxK18th0eCsKehJbgHdS-6Hl8Ajf8aXNR2Sd-_DU_DvlKi-zi80aCsMd1c7Xc9R0KwiWOmWF3L8THbRgi1Fuy8MATa9ZV8gy05jIl8xnHiSDAy1asYXuwHFrA3eUulIcigVj4864_ZxRXBxObyaqO88-lk7GrTTAxUjZ3G8rlKHvoZbeD2io-7mO0199_0BizuwpuqOEeQyidWSV9KFbP51ADQPsNAbgDBI4by0003__mC0)

- Employee: Lớp này chịu trách nhiệm cung cấp thông tin của nhân viên và xác thực quyền truy cập khi yêu cầu cập nhật bảng chấm công.
- TimeCard: Đại diện cho từng bản ghi chấm công của nhân viên. Mỗi bản ghi chứa thông tin về số giờ làm, ngày làm việc, và mã công việc.
- PayrollDatabase: Chịu trách nhiệm lưu trữ thông tin của nhân viên và các bảng chấm công, đảm bảo rằng tất cả bản ghi chấm công được cập nhật và lưu trữ đúng cách.
- TimecardService: Chịu trách nhiệm quản lý yêu cầu cập nhật bảng chấm công của nhân viên, xử lý việc tạo mới hoặc cập nhật các bản ghi chấm công, và xác nhận trạng thái cập nhật tới nhân viên.

# 5.Hợp nhất kết quả phân tích
- Tổng quan hệ thống
    + Hệ thống Payroll của Acme được thiết kế nhằm đáp ứng yêu cầu về quản lý và xử lý thanh toán lương cho nhân viên, cũng như việc ghi      nhận và quản lý thông tin chấm công. Hệ thống hỗ trợ ba loại nhân viên (nhân viên theo giờ, nhân viên hưởng lương cố định, và nhân        viên có hoa hồng), cho phép họ nhập thông tin chấm công và yêu cầu thanh toán thông qua giao diện máy tính để bàn.
- Mối quan hệ giữa các lớp
    + Employee: Liên kết với TimeCard và PurchaseOrder, đại diện cho thông tin nhân viên.
    + TimeCard: Lưu trữ thông tin chấm công và liên kết với TimecardService.
    + PurchaseOrder: Lưu trữ thông tin giao dịch bán hàng và liên kết với PaymentService.
    + PayrollDatabase: Là cơ sở dữ liệu trung tâm, chứa thông tin toàn diện về nhân viên, bảng chấm công, và đơn mua hàng.
    + PaymentService: Xử lý các yêu cầu thanh toán và tính toán lương, liên kết với PayrollDatabase.
    + TimecardService: Quản lý các hoạt động liên quan đến bảng chấm công, liên kết với PayrollDatabase.
- Biểu đồ hợp nhất 2 ca sử dụng
  
![diagram](https://www.planttext.com/api/plantuml/png/X5HBRi8m4Dtd52DM89KBP561e5AxeKXGTUtOKneHn-dOHeggdgoB7gbNw8HFi4aeNcGnVlFUcu_p-_qpiKwGyxf8AY6tOeCmM8gQJ570ghOEzG0-4-0Z2s4jFEYgC3NYCTYSCJpDKrWvoijD45m8ZJtXgLA4rlRSiAp6qgthAixxIWBzTQvn9aX5-dFXEANv1i57uyc-6jgYuZlZioAydRqBsk32wmpfkjhIatmN5fz98TsMd6hZInUfnNI7ndAMo9Wr80ImOeUduePEfcsbenHs9bS1b93juWuRdY7gwjn-nfu6rAlUz7U5jCjbB2v58Nt1nHmn3UkPQjJf7q15Hl8Oh-5RnvtXIIwfpmBXXqVhNYh5DcA-E_Y_7wLn-LlTbzdZf5tWyVZ-l4qfwqj3odOnyGwaO7scStS0jladih2w5BGe-K4foEezEcRQSySZIKzj3N8kLkR2jNM6NzDLP5l8JMIdoWWUcZpwZXZITYSjy1H4svom7_s9VZysc_1u9bYgvaVq1m00__y30000)

- Chức năng
    + Employee: Lưu trữ thông tin của nhân viên, bao gồm ID, tên, địa chỉ, và phương thức thanh toán.
    + TimeCard: Ghi nhận và lưu trữ thông tin về số giờ làm việc của nhân viên theo từng ngày và mã công việc.
    + PurchaseOrder: Ghi nhận các giao dịch bán hàng của nhân viên hưởng hoa hồng, bao gồm ngày bán và số tiền bán.
    + PayrollDatabase: Lưu trữ thông tin toàn diện và cho phép truy xuất và cập nhật dữ liệu cho các lớp khác.
    + PaymentService: Tính toán và thực hiện thanh toán cho nhân viên dựa trên thông tin từ PayrollDatabase.
    + TimecardService: Quản lý các yêu cầu cập nhật bảng chấm công từ nhân viên và lưu trữ thông tin vào PayrollDatabase.
      
- Lợi ích của việc hợp nhất
    + Tính nhất quán: Hợp nhất các lớp liên quan giúp tạo ra một cấu trúc hệ thống nhất quán và dễ hiểu, giảm thiểu sự trùng lặp và giúp      tăng cường khả năng bảo trì.
    + Dễ dàng mở rộng: Cấu trúc này cho phép việc mở rộng hệ thống dễ dàng hơn, với khả năng tích hợp các chức năng mới trong tương lai 
    mà không làm gián đoạn các chức năng hiện tại.
    + Tăng cường bảo mật: Mỗi lớp có nhiệm vụ rõ ràng, giúp dễ dàng hơn trong việc kiểm soát quyền truy cập và bảo vệ dữ liệu của nhân 
    viên.
    + Quản lý hiệu quả: Hợp nhất các lớp liên quan giúp tối ưu hóa việc quản lý thông tin, từ đó nâng cao hiệu quả hoạt động của hệ thống.
- Kết luận
    + Việc hợp nhất kết quả phân tích cho hai ca sử dụng "Select Payment" và "Maintain Timecard" đã cung cấp cái nhìn toàn diện về hệ         thống quản lý bảng lương của Acme, Inc. Qua quá trình phân tích, chúng ta đã xác định rõ ràng các lớp phân tích, mối quan hệ giữa 
    chúng, cũng như chức năng và nhiệm vụ của từng lớp.
