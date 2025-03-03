
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

## Hướng dẫn sử dụng

### Cài đặt yêu cầu

Trước khi chạy dự án, bạn cần cài đặt một số thư viện và công cụ sau:

1. **Python**: Đảm bảo rằng bạn đã cài đặt Python 3.x trên máy của mình.
2. **DuckDB**: Đây là cơ sở dữ liệu sử dụng trong dự án. Bạn có thể cài đặt DuckDB thông qua pip:
   ```bash
   pip install duckdb
   ```

3. **Các thư viện Python khác**: Các thư viện cần thiết có thể được cài đặt bằng cách sử dụng `requirements.txt`. Nếu file này có sẵn trong dự án, bạn có thể sử dụng lệnh sau:
   ```bash
   pip install -r requirements.txt
   ```

### Chạy ứng dụng

1. **Chạy quy trình ETL**: Để thực hiện quá trình ETL, bạn có thể chạy file `api_to_dw.py`. Đảm bảo rằng bạn đã cấu hình đúng các kết nối API và các thông số liên quan.
   
   Ví dụ:
   ```bash
   python api_to_dw.py
   ```

2. **Lên lịch các tác vụ ETL**: Thư mục `schedule` có thể chứa các script để tự động hóa quá trình ETL. Bạn có thể sử dụng cron jobs hoặc các công cụ lập lịch tác vụ tương tự để chạy các tác vụ này định kỳ.

3. **Xem và phân tích dữ liệu**: Bạn có thể sử dụng các notebook trong thư mục `notebook` để trực quan hóa và phân tích dữ liệu sau khi ETL hoàn tất.

## Kiến trúc dự án

- **Frontend**: Không có phần frontend trong dự án này.
- **Backend**: Các quy trình backend xử lý dữ liệu từ API và tương tác với cơ sở dữ liệu DuckDB.
- **Data Warehouse**: Dữ liệu được lưu trữ trong cơ sở dữ liệu DuckDB, cho phép truy vấn và phân tích sau này.

## Các tính năng chính

- **Trích xuất dữ liệu từ API**: Quá trình ETL trích xuất dữ liệu từ các API.
- **Chuyển đổi dữ liệu**: Dữ liệu được biến đổi để phù hợp với yêu cầu của Data Warehouse.
- **Tải dữ liệu vào Data Warehouse**: Dữ liệu sau khi được xử lý được tải vào cơ sở dữ liệu DuckDB.
- **Lập lịch tự động**: Quá trình ETL có thể được tự động hóa thông qua các tác vụ đã lên lịch.


