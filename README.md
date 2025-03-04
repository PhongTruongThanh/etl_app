
# ETL App

Dự án này là một ứng dụng ETL (Extract, Transform, Load) sử dụng các công cụ và thư viện Python để xử lý dữ liệu, chuyển đổi và tải lên một cơ sở dữ liệu Data Warehouse. Ứng dụng này có thể kết nối với API, thực hiện các phép toán ETL và lưu trữ dữ liệu vào cơ sở dữ liệu DuckDB.

## Nội dung dự án

Dự án này bao gồm các thành phần chính sau:

1. **SQL**: Chứa các file SQL liên quan đến quy trình ETL, bao gồm các truy vấn, bảng dữ liệu, và các lệnh tạo cơ sở dữ liệu.
2. **`__pycache__`**: Thư mục chứa các file bytecode của Python.
3. **`api_to_dw.py`**: File Python dùng để chuyển dữ liệu từ API vào Data Warehouse.
4. **`backend`**: Chứa các thành phần backend của ứng dụng, có thể là các logic xử lý dữ liệu và quản lý ứng dụng.
5. **`datawarehouse.duckdb`**: Cơ sở dữ liệu DuckDB nơi dữ liệu được lưu trữ sau khi quá trình ETL hoàn tất.
6. **`elt`**: Thư mục này có thể chứa các script ETL thực hiện việc truy xuất, biến đổi và tải dữ liệu.
7. **`notebook`**: Chứa các Jupyter notebook cho việc phân tích và trực quan hóa dữ liệu.
8. **`schedule`**: Thư mục liên quan đến việc lên lịch cho các tác vụ ETL hoặc các tác vụ định kỳ khác.

## Kiến trúc dự án

- **Frontend**: Không có phần frontend trong dự án này.
- **Backend**: Các quy trình backend xử lý dữ liệu từ API và tương tác với cơ sở dữ liệu DuckDB.
- **Data Warehouse**: Dữ liệu được lưu trữ trong cơ sở dữ liệu DuckDB, cho phép truy vấn và phân tích sau này.

## Các tính năng chính

- **Trích xuất dữ liệu từ API**: Quá trình ETL trích xuất dữ liệu từ các API.
- **Chuyển đổi dữ liệu**: Dữ liệu được biến đổi để phù hợp với yêu cầu của Data Warehouse.
- **Tải dữ liệu vào Data Warehouse**: Dữ liệu sau khi được xử lý được tải vào cơ sở dữ liệu DuckDB.
- **Lập lịch tự động**: Quá trình ETL có thể được tự động hóa thông qua các tác vụ đã lên lịch.

# Docs link: 
https://wise-bard-bd3.notion.site/ETL-Document-1acaceae7fe680ff9853c1b8e6219d0a?pvs=4
