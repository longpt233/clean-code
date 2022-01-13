### Chương 1

### Chương 2: Đặt tên biến 
> -  đặt tên biến phải có ý nghĩa
> -  ý nghĩa chỉ số. ví dụ proxys[0] không mang ý nghĩa
> -  tên phân biệt. nên dùng Product, thay vì tách thêm ProductInfo hoặc ProductData

### Chương 3: Hàm 
> -  Nên chia nhỏ hàm 
> -  Hàm chỉ làm 1 việc
> -  Đối số có thể xem xét truyền qua đối tượng nếu quá dài ..
> -  không được làm thay đổi biến toàn cục, 
> -  không gọi các hàm không liên quan mục đích hàm (ví dụ hàm checkTrue(obj) mà trong đó lại mở connection mới chẳng hạn), 
> -  không nên làm ảnh hưởng đối số truyền vào 
> -  nên chỉ có 1 câu lệnh return trong hàm 
> -  không nên có break, continue trong vòng lặp

### Chương 4: cmt 
 
> -  việc cmt thể hiện sự thất bại trong việc diễn dải code
> -  thay vì cmt, có thể tách hàm và nó mang thông điệp trong tên hàm đó 

##### Cho phep
> -  cho phép cmt pháp lý (author ..)
> -  cho phép cmt cung cấp thêm thông tin cho hàm 
> -  cho phép cmt giải thích giải thích mục đích, lý giải cách xử lý vấn đề 
> -  cho phép cmt cảnh báo khi dùng 1 hàm 
> -  cho phép cmt TODO 
> -  cho phép cmt giải thích các trường hợp 

##### khong cho phep
> -  không cho phép các cmt đánh dấu (kết thúc, mở đầu, ), quá dài….

### Chương 5: Định dạng code 

> -  khởi tạo instance nên được đặt ở đầu class 
> -  Hàm phụ thuộc nên đặt gần nhau 


### Chương 6: Đối tượng và cấu trúc dữ liệu 

> -  nên đặt private vì không muốn có ai khác phụ thuộc vào nó. hạn chế tạo các phương thức getter/setter 
thao tác qua interface 
> -  Code theo cấu trúc dữ liệu làm bạn khó thêm dữ liệu mới vì phải thay đổi toàn bộ hàm >< Code theo hướng đối tượng làm bạn khó thêm hàm vì phải thay đổi tất cả các class chịu
> -  Hàm không nên gọi các phương thức khác của phương thức khác. ví dụ ```ctxt.getOptions().getScratchDir().getAbsolutePath()``` vì sẽ k biết được là ai đang gọi, nên viết thành : 
```
Options opts = ctxt.getOptions();
File scratchDir = opts.getScratchDir();
final String outputDir = scratchDir.getAbsolutePath();
```


### Chương 7: Xử lý lỗi 
> -  nên sử dụng throw để try catch lỗi 
> -  không nên trả về null, không nên truyên null 

### Chương 8: Ranh giới 

### Chương 9: Kiểm thử 

### Chương 10: Lớp 
> -   Lớp nên nhỏ, đủ trách nhiệm giống như việc hàm chỉ làm đủ chức năng bên trên 

### Chương 11: Hệ thống 
> -  Tách biệt việc xây dựng một hệ thống với việc sử dụng nó: 
```
    chuyển hết init sang main 
    factories 
    Dependency Injection
```
