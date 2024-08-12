**Hướng dẫn sử dụng source code!**
## 1. Cài Đặt Visual Studio Code

### 1.1. Tải và Cài Đặt VSCode

1. Truy cập trang [Visual Studio Code](https://code.visualstudio.com/).
2. Tải phiên bản phù hợp với hệ điều hành của bạn (Windows, macOS, hoặc Linux).
3. Cài đặt VSCode theo hướng dẫn trên trang web.

### 1.2. Cài Đặt Các Extension Cần Thiết

Mở VSCode và cài đặt các extension sau:

1. **ESP-IDF**: Tìm kiếm và cài đặt "Espressif IDF" từ Marketplace.
2. **C/C++**: Tìm kiếm và cài đặt "C/C++" từ Microsoft.
3. **Python**: Tìm kiếm và cài đặt "Python" từ Microsoft.

## 2. Clone Project Từ GitHub

### 2.1. Clone Repository

Mở terminal và chạy lệnh sau để clone repository từ GitHub:

```sh
git clone https://github.com/duvanan13/Smartplug.git
```

### 2.2. Mở Project Trong VSCode

1. Mở VSCode.
2. Chọn **File** > **Open Folder**.
3. Duyệt đến thư mục chứa project bạn vừa clone và mở nó.

## 3. Cài Đặt ESP-IDF

1. Mở VSCode và nhấn `Ctrl+Shift+P` để mở Command Palette.
2. Gõ `ESP-IDF: Configure ESP-IDF extension` và chọn tùy chọn này.
3. Làm theo hướng dẫn để cấu hình đường dẫn đến thư mục ESP-IDF và các công cụ liên quan.

## 4. Chạy Project ESP-IDF Trong VSCode

### 4.1. Build và Flash Project

1. Mở terminal trong VSCode (`Ctrl+``).
2. Config flash memory
    ```sh
    idf.py menuconfig
    ```
    Tìm tới **Serial flasher config**: thay đổi **Flash size** = 4MB
    
3. Config Partition Table
    ```sh
    idf.py menuconfig
    ```
    Tìm tới **Partition Table**: chọn **Custom partition table CSV** sau đó nhập *partitions_two_ota2.csv*
    
4. Chạy lệnh sau để build project:

    ```sh
    idf.py build
    ```

5. Chạy lệnh sau để flash project lên thiết bị:

    ```sh
    idf.py flash
    ```

### 4.2. Monitor

Để monitor output từ thiết bị, chạy lệnh:

```sh
idf.py monitor
```

Chúc bạn thành công!
