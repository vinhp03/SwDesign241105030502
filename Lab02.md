# 1. Use case Login

## 1.1 Cơ chế phân tích 
Account: Chứa tài khoản bao gồm name và password

**Cơ chế phân tích:** Security

Dùng Security vì cần bảo mật thông tin của các actor

## 1.2 Phân tích Login
Các lớp phân tích:

* Boundary: Login GUI
* Controller: Login Controller
* Entity: Accounts

Biểu đồ tương tác:

Basic flow:

![Diagram](https://www.planttext.com/api/plantuml/png/R90z3i8m38LtdyBgpWKO4AX22AaRAdj83Qf84nIxGZq6uWISemCBuXwSW2lW_crCoNlVoxELR_jSifWeTUK0-5nwZ849G4fnXCdk_S3NxTFUCGkdqYS0nag8c3D5E8JQ5oOscFGGD_asGSFT2JPuYS6DA1sKezW7iXJ8wuG6LzPgYG1qXJXRT6znZcilAhsfw2-u6EPhY0Lqfh8iLJJi07fNP-nLUszSMHYXATltJMckhINcO-rWIRxGJ_W1003__mC0)

Alternative Flows: 

![Diagram](https://www.planttext.com/api/plantuml/png/R90nZW8n34LxdyAQVY-m1GADq0ffEWIzD-D54S51YKTeZh7Y19o3OXl4FJZ1NW676QYe4l_dF2VvF_zDirBIRXS0yjOBffWPGBq6ncfvFU7bztO-OXCtNYe0SXeJhZ8d-8wTj9Hwh1uGlrQB2YcN5LmKJJ6Cg1wgmEdHqDJ0OXDwd3bd4WKeGloObBFuYNDHAuLs_1RiAUT3J2sKq5XJ6nhk0BQtPFHQlARWMr8UmQ0PUd_81tv9og0diHVM98u3J5bQ-vix0000__y30000)

# 2. Use case Maintain Employee Information
## 2.1 Cơ chế phân tích
Employ: Thông tin của 1 nhân viên

**Cơ chế phân tích:** Persistence, Security

Cần cơ chế Persistence vì cần phải lưu trữ dữ liệu của hệ thống

Cần cơ thế Sercurity vì cần bảo mật thông tin cho các nhân viên
## 2.2 Phân tích Maintain Employee Information
Các lớp phân tích: 
* Boundary: EmployeeInformation GUI
* Controller: EmployeeInformation Controller
* Entity: EmployeeInformation
Biểu đồ tương tác:

![Diagram](https://www.planttext.com/api/plantuml/png/b5InRjim4Dtv5GSlMHfqrr0aa9B2GpjKzGVGr2aYJ94gHINGs2bpq2zensv5XmBsaC51_qDVq5_eKJ9aoRBJL80aKdptxjsxW_vi7YzAnwshSiLOkP8Qh2cHCIUTGfZ5lx_2qqEp-GBlkDIERhZA2sLgH9ZhrDYSEsaqdCDb5FL7CyQuSCR2eaJBbgRI2RSrp8w6lbtCPy1B_sR2Q6UDEe4CkrE5jWs8GuQQTDPzNiPyGZX_uyaWW1WL2eS9N2O9S3t0tLXJ5Urd1dHvE4MrqG5ym4yLbWw8dVO31IrsdEAgnHoJEoIEGuA65hd37djMmZnwHHeT5BmM6OeL9AZaBTgwZQKW2ksfWv750yIkripSWSQxFG9rSjAGHP5uBKSywKuENPcOSg1aaERGaxREiHa1N4kTx4jRrfvmN580aImBnUlJveuDekhuBOvbdS77Z1XSrgmVGMVRdpae6cPzGnjUmR9P_w3rquDiDfyhMD7hNaDcclKl0MBxhVBeUvs1bTll15nwW6kPkN9xOTT-mjlF4zl-MGIgSYyQtXlt75ldR2BJ52qrmhls6aAk1QgEZ0AVQtj4Y-DjxqxOOSAuG27JUkJgIthzWbR_HwUzsTE9fDz1Acq-a3wPY5szFI_R6JwTsSx48HSR-7b13_-7_0i00F__0m00)
