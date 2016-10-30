Diễm Trinh

# Báo cáo học con trỏ.

*Một số hạn chế khi sử dung biến tĩnh:*
- Cấp dư ô nhớ, lãng phí ô nhớ. 
- Cấp phát thiếu ô nhớ, chương trình lỗi

*Cách giải quyết:*  sử biến **con trỏ** , tận dụng các đặc điểm: 
- Chỉ phát sinh khi thực hiện chương trình.
- Không chứa dữ liệu mà chỉ chưa địa chỉ của dữ liệu hoặc địa chỉ ô nhớ

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

` printf("xap xep day \n");  

      for (i=0;i<n-1;i++)  
         for (j=i+1;j<n;j++)  
         {
             if (*(p+i)> *(p+j))   
             {
                 t=*(p+i);  
                 *(p+i)=*(p+j);  
                 *(p+j)=t;  
             }
         }
    for (i=0;i<n;i++)  
        printf("%d   ",*(p+i));
printf("\n"); `  
- phép so sánh `*(p+i)>*(p+j)` : nghĩa là lấy giá trị của a[i] so sánh với a[j]
- phép toán gán: `t=*(p+i)` : nghĩa là  t=a[i];       
                 `*(p+i)=*(p+j): nghĩa là a[i]=a[j];
- phép  truy nhập bộ nhớ
- phép tăng giảm địa chỉ.
- ngoài ra còn có các phép toán +;-;*;/....

## 4.Con trỏ và mảng.
*Ví dụ:*

` int a[10],i,*p,min,max,n,t,j,s;

    p=a;
    scanf("%d",&n);
    for (i=0;i<n;i++)
         scanf ("%d",(p+i));
  `
- `p=a` nghĩa là p lưu trữ địa chỉ cả mảng a, p=&a;p=&a[0];
- p+i : (trỏ tới phần tử a[i]) p+i=&a[i]
- đối với mảng nhiều chiều, việc xử lí địa chỉ vói con trỏ phức tạp hơn nhiều so với mảng một chiều.

