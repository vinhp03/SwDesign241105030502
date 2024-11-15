# Subsystem context diagrams

- Hệ thống PrintService
  
![diagram](https://www.planttext.com/api/plantuml/png/j5FBQiCm4BphAnPV-Y0nxTKO4vhq46WX4EXTaJUEg2ovqhh1jFco7lf9_ONAJXt7YNEi3WBjZ7PdPwMVh--98swfp1KZIGfXOQMc9TftAH0Oku8PhgL642OlZ4PD3jP6ARELEeFdbobmApQIK51faHLSlF8C8PWQJTRpqC8Jhz06yC70Bw6uSx3WLGqUaU9O70v9yaTkbiMt4XtvAqx9ulgcGNPinxfYSqrerzmBxjMIX_2yrzLHygAEjwanBvIf4ETf14loI3O2nnMtLGGpKwuKZY35j1GaZNPjx2Q21sCKSZsWx55xLwiB5jH5VUFOSFfDdqlfiBwaBdukhSCor6WvOJhpcuVzFg1sMQvSvGZp4wd7viMnQrbzoVzavU41MbIyOMzauO3hT3zVla_1pfzK62OdWu-WT7Y9sWuaEfZbMFzw_3aUmqd2LeE3hQGDQvC4Ts5u6y00t-sDmXHMLKU_hxd9mB-8G5XijB09whJ-fxy0003__mC0)

- Hệ thống ProjectManagementDatabase

![diagram](https://www.planttext.com/api/plantuml/png/j9EnJiCm48PtFyMDHA8la05LfKXqG49YOBuwHmXrxCXt6Ih4ap7qaVeAjOEfqZHf9IIy9F9zvyl_HTv_x-OiwAMjZP9A304yU_T1MfxGOaarMLcYu1gPb58GbZR8F4t1PqV5LP8aB1Plg6wCsnAjYXnUn5Usp7Be0SU-jYbGA5KUNUjvfFSMcX-Wl_KUuLVdDnGsbwvT6mep5iuPGjkT_zNBy90EFOyr0lrMJYtWrZjZxfsL-2H_cdxGsrd8BiNCqZUcAPKLyc-e2LRNVF_5zVzvZWdEtSncTqUTEQ3Mn4ny1GpL67U2clQY1l87qq4ywWsFKkazGE4VLwLbTK5_hs7ioip95l5ogGC0003__mC0)

# Analysis class to design element map
|Analysis Class|Analysis Class|
|--------------|--------------|
|Employee|EmployeeEntity|
|TimeCard|TimeCardEntity|
|PaymentMethod|PaymentMethodEntity|
|PayrollService|PayrollProcessor|
|EmployeeRepository|EmployeeDataAccess|
|TimecardRepository|TimecardDataAccess|
|PaymentRepository|PaymentDataAccess|
|ReportGenerator|ReportGeneratorComponent|

# Design element to owning package map
|Design Element|Owning Package|
|--------------|--------------|
|EmployeeEntity|Data Access::Employee Management|
|TimeCardEntity|Data Access::Employee Management|
|PaymentMethodEntity|DataAccess::Payment|
|PayrollProcessor|Business Services::Payroll Processing|
|ReportGeneratorComponent|Presentation::Report::Payroll|
|EmployeeDataAccess|DataAccess::Employee|
|TimecardDataAccess|DataAccess::Employee|
|PaymentDataAccess|DataAccess::Payment|
|PayrollUI|Presentation::Payroll|
|SalaryCalculator|BusinessLogic::Payroll|
|PayrollReportGenerator|Presentation::Report::Payroll|

# Architectural MVC and their dependencies
![diagram](https://www.planttext.com/api/plantuml/png/T991JiCm44NtFiMe-ru15OKAiQXK0MK_SaOGCR6ZyLHLX3XP5pqILy1fANLYnqk_B__vV_npFAs2ekY-PTEX_SHtWiLRGuS5V1c8npA605linJFldiotkUagxtIu9Ycgj-8jXU0bGS_KUT57SYIe8_A2ZD9No7RFPvGwFQ0YtDlXkR7LkktOzqI3uC8J-DgqP57g8en3jkGqOQdXnjV4Crvhfuts4vyg-cJWpsD3-k6lDBhyjmdBvLtM5fZiPf3bIMU4UUePOTv0KJPTML4qtHwOmhnfZ4iRO0hJNaFSAZq76C-Q9aZx1RCYLyVl_0i00F__0m00)


