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

![Diagram](https://www.planttext.com/api/plantuml/png/T9D1JiCm44NtFiKeAv3e1P101HM9JL7LLc8zTQQjgMC7UnAKix7WI5m1sqbAqwQRA8hVd_d_M_dz_fbwHiTLeOK_A0FEUX8esJfuAKfj6o9H1a19LQ9Xo5QDPoeoG0_XTNYsSFQ39CCS3UweeF1jXemRz9G4Y_diMOX-BamUumYuXoLzLkGPs89qX4o0uAYqZaK40dVK_CCj40IAoIc4csNxOTsKT1VtahyTsHKyrYgdSxaGg1bEHi03P6lBgE7LLix3ktK7oc4RYa7eWcO2e3COeoLpx1JL15e5YtOBSezkHs2gOaFE1pw1awETfngLnescI_8o-apvKcDpXWAQFCHfM_6aWp5bJHXm6NwLJeTwGION8psV5VMbU0--9AcsAlGmx6s5DVKMA1zTVNB7FjAyxqUFHktnn6ehCMPAIGqMDBgXDtnLqctfgcWjfspHqp5PhnIaFS5RP_Sqt61Ek1E9Bk-pf3AduHd_g3y0003__mC0)

Alternative Flows
![Diagram](https://www.planttext.com/api/plantuml/png/R951JWCn34NtFeNL5KXm0HQeeYthgd01ap4GaKc2xIcQix7WI5m1PuO2ebqaIkptlntdy_rZgKPYGvz0Ns96ASf0mOhWfg-fZCnG7OWXLig6YxjHZVi5ag8V0GuKNbwt05xXZby7LaCh68J960c5Qn631ZZte_c5Py05qLWYuTbk3joFbIzmxIvwVgBMLie-TlnV3a393jxSOSoFHNgoM38EcVOK4pqa1iJZZjPHQw8HMSI7qBCgFJNokFZgkVYqsZk5focY2mBbm0bSCBSm9VnsgjHt5cz8Oy3RLDuSvEIUgya5IsMPklvhC1VVv0u79mDfwuvp1st1qlVscry0003__mC0)

Requested Information Unavailable
![Diagram](https://www.planttext.com/api/plantuml/png/T99DJWCn34RtESMdha222x105QL8tQ6M2rWP5rdaZyHJD6TZmP6u0Xw65gaCYqHHyZxxHSdd-yUoALNjOt3jHH9gRkp8QwvOnnBomEoA0UAbK58iTaDJZWjGWosTErAulXqtS8Cjl_RS59hXAvCo29LBhkf6mBXJvXUU00k8SXN2nNRQU1eAN-7UghJBcLwFDH-aOqZosGxPcfcvf0C5wSwBEaT1iVav_EPQlz_RrTXk9ccVQoILd1pmrzHQnQ8m255Qa_Hy5ldVRewtm6YpcnL0cPATKNCkgvnKKi-ueoOU3o6_6ScXCLQKF0VamlKeTgemMQrJXzv8J_RKbagT6uTRsZp-Woy0003__mC0)
