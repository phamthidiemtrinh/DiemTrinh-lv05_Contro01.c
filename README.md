Diễm Trinh

# Báo cáo học con trỏ.

*Một số hãn chế khi sử dung biến tĩnh:*
- Cấp dư ô nhớ, lãng phí ô nhớ. 
- Cấp phát thiếu ô nhớ, chương trình lỗi

*Cách giải quyết:*  sử biến **con trỏ** , tận dụng các đặc điểm: 
- Chỉ phát sinh khi thực hiện chương trình.
- Không chứa dữ liệu mà chỉ chưa địa chỉ của dữ liệu hoặc địa chỉ ô nhớ
- Vùng nhớ luôn có kích thước cố định là 2 byte, không phụ vào kiểu dữ  liệu.

## 1. Định nghĩa biến con trỏ
* Là biến dùng để lưu địa chỉ, mỗi loại địa chỉ có một kiểu con trỏ tương ứng.
  **Ví dụ:** con trỏ kiểu int lưu địa chỉ biến kiểu int, con trỏ kiểu float lưu địa chỉ biến kiểu float.... 
* Luôn được cấp phát 2 byte vùng nhớ.  

## 2. Cách khai báo :  
*Có 2 loại con trỏ và cách khai báo:*
* Con trỏ không kiểu: Có thể chứa bất kỳ một địa chỉ nào   
   **Cú pháp:** `void *tên biến con trỏ ;`   
   *Ví dụ:* `void *p;` : khi đó P sẽ lưu trữ được địa chỉ của biến thuộc kiểu int, float, char, double...
* Con trỏ có kiểu : Chỉ lưu trữ được địa chỉ biến có kiểu dữ liệu tương ứng.    
    **Cú pháp:** `<kiểu dữ liệu> *tên biến con trỏ;`  
    *Ví Dụ:* `int *t` : khi đó biến t chỉ lưu trữ được **duy nhất** địa chỉ của biến thuộc kiểu int.  
   
## 3. Các phép toán:
Cho đoạn chương trình ví dụ:
