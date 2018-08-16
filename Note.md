# Học Java

    *1 file .java không giới hạn số class trong 1 file. Tuy nhiên trong 1 file chỉ được có duy nhất 1 public class.*

    *Phân biệt chữ hoa và chữ thường*

**1. Định nghĩa cơ bản**

- Đối tượng: có trạng thái và hành vi.
- Lớp: mô tả trạng thái, hàng vi của đối tượng mà nó hỗ trợ.
- Phương thức: 1 phương thức đơn giản là 1 hành vi. Một lớp có thể bao gồm nhiều phương thức. Trong mỗi phương thức có những phép toán logic, dữ liệu được xử lý và tất cả các hành động được thực thi.
- Biến: mỗi đối tượng có một tập các biến duy nhất. Mỗi trạng thái của đối tượng được khởi tạo bởi giá trị và gán với những biến.

**2. Cú pháp cơ bản trong Java**

- Tên Class: nên viết hoa chữ cái đầu tiên và là 1 danh từ.
- Tên Interface: nên viết hoa chữ cái đầu tiền và là 1 tính từ.
- Tên phương thức: nên bắt đầu với chữ thường và là 1 động từ. Ví dụ public void actionPerformed()
- Tên biến: nên bắt đầu với chữ thường.  ví dụ: firstName, orderNumber ...
- Tên package: nên bắt đầu với chữ thường.  ví dụ: java, lang, sql, util ...
- Tên hằng: Nên bắt đầu với chữ hoa, ví dụ: RED, YELLOW, MAX_PRIORITY...
- Tên file chương trình: Tên file nên giống hệt tên class. 

    **Khi lưu file, nên sử dụng tên class và thêm hậu tố .java**

- Chương trình Java bắt đầu bởi phương thức main() cho tất cả các chương trình J2SE: public static void main(String args[]).
- Định danh (Identifer): bắt đầu với 1 chữ cái (A tới Z hoặc a tới z), ký tự $ hoặc ký tự _, identifier phân biệt chữ hoa chữ thường.
- Modigier: có 2 loại Access Modifier (default, public, protected, private) và Non-access Modifer (final, abstract, strctfp).
- Biến: 3 loại Biến Local, Biến của class (biến static), Biến đối tượng (không phải biến static).
- Mảng: lưu trữ nhiều biến với chung 1 kiểu dữ liệu. Bản thân 1 mảng cũng là 1 đối tượng trong bộ nhớ.
- Java Enums: có thể khai báo các enums như của riêng chính nó hoặc  bên trong một lớp. Các phương thức, biến, constructor cũng có thể được định nghĩa bên trong các enums. Enums giới hạn số lượng các biến bởi cách định nghĩa trước. Các biến trong dánh sách được liệt kê gọi là enums.
- Comment trong Java: /* ... */ ; // ; 
- Tính kế thừa trong java: khi muốn tạo 1 class mới mà đã có sẵn 1 class có 1 số đoạn code cần cho class mới, thì class mới có thể suy ra từ code đã tồn tại. Class đang tồn tại gọi là superclass, class được suy ra là subclass.
- Lệnh print và println: print giữ nguyên vị trí con trỏ trên cùng 1 dòng lệnh, println di chuyển con trỏ xuống dòng tiếp theo.

**3. JDK, JRE, JVM trong Java**
- JVM (Java Virtual Machine) là 1 máy ảo giúp máy tính chạy các chương trình Java. JVM thực hiện: tải code, kiểm tra code, thực thi code, cung cấp môi trường runtime.
- JRE (Java Runtime Environment) sử dụng để cung cấp môi trường runtime. JRE bao gồm  tập hợp các thư viện và các file khác mà JVM sử dụng tại runtime.
- JDK (Java Development Kit) bao gồm JRE và các Development Tool.

**4. Các kiểu biến trong Java**

*kieu_du_lieu bien [ = giatri][, bien [=giatri] ...]*
  VD: int a, b, c;
      byte A = 11;

**Biến Local**
- Được khai báo trong các phương thức, constructor, hoặc khối.
- Được thực thi nội bộ.
- Các biến local nên được khai báo và gán một giá trị trước khi sử dụng.

**Thuộc tính (biến instance)**
- Được khai báo trong 1 lớp, nhưng ở bên ngoài một phương thức, constructor hoặc khối bất kỳ nào.
- Thuộc tính có giá trị mặc định. Các số, giá trị mặc định là 0; với Boolean là false; với đối tượng là null. Các giá trị có thể được gán trong khi khai báo hoặc trong constructor.

**Biến Class/Static**
- Các biến class giống các biến static được khai báo với từ khóa static trong một lớp, nhưng ở bên ngoài một phương thức, constructor hoặc một khối.
- Chỉ có một bản sao của mỗi biến class cho mỗi lớp dù có bao nhiêu đối tượng được tạo từ nó.
- Các biến static hiếm khi được sử dụng ngoài việc được khai báo như là các hằng số.

**5. Kiểu dữ liệu trong Java**
- Có 2 kiểu dữ liệu có sẵn trong Java: Các kiểu dữ liệu gốc (Primitive); Các kiểu dữ liệu tham chiếu/đối tượng (không phải kiểu gốc Non-primitive).

<img src="https://2.pik.vn/2018f22b7e7a-e308-494d-827e-dc26e5557c28.jpg">

<img src="https://2.pik.vn/20180e11abee-bb47-4c24-a3cf-3f19b99d18fb.jpg">

- Có 8 kiểu dữ liệu gốc được hỗ trợ bởi Java.

    char: lưu dữ liệu kiểu ký tự hoặc số nguyên k âm, 2 byte.

    byte: lưu dữ liệu kiểu số nguyên, lưu khoảng trống trong các mảng lớn chủ yếu là các số nguyên, 1 byte.

    short: lưu dữ liệu kiểu số nguyên, lưu bộ nhớ như kiểu dữ liệu byte, 2 byte.

    int: lưu dữ liệu kiểu số nguyên, 4 byte.

    long: lưu dữ liệu kiểu số nguyên kích thước 8 byte, sd khi cần 1 dải giá trị rộng hơn int.

    float: lưu DL kiểu số thực, 4 byte.

    double: lưu DK kiểu số thực 8 byte.

    boolean: 1 bit, lưu DL có 2 trạng thái true hoặc false.

    object: giá trị mặc định null.

    literal: biểu diễn 1 giá trị cố định.

**6. Toán tử trong Java**
- Toán tử số học: + - * / % ++ --
- Toán tử quan hệ: == != > < >= <=
- Toán tử thao tác bit: & | ^ ~ << >> >>>>
- Toán tử logic: && || !
- Toán tử gán: = += -= *= /= %= <<= >>= &= ^= |=
- Toán tử hỗn hợp
- Toán tử điều kiện:

     bien x = (bieu_thuc) ? (giatri1 neu true) : (giatri2 neu false); 

     //hoặc sử dụng lệnh RETURN

    return (bieu_thuc) ? (giatri1 neu true) : (giatri2 neu false);
- Toán tử instanceof: sử dụng cho các biến tham chiếu đối tượng. Toán tử trả về kiểu true nếu toán hạng trái là biến thể hiện của toán hạng phải hoawjwctrar về true nếu đối tượng đang được so sánh là tham số tương thích với kiểu toán hạng phải.
- Thứ tự ưu tiên: 

<img src="https://2.pik.vn/20185b97a07c-a991-4c1f-931e-f6a180b63aeb.jpg">

<img src="https://2.pik.vn/2018b3112751-08df-4367-b296-0360eaee352d.jpg">

**7. Các kiểu vòng lặp**

<img src="https://2.pik.vn/2018e00a3576-bb83-4361-8b82-1698679cca1f.jpg">

<img src="https://2.pik.vn/201828bccadc-4914-4c48-9b15-3474d1696f8e.jpg">

**8. Lệnh if/else, switch/case**

<img src="https://2.pik.vn/2018a8010fc3-bc3d-4084-8728-d52a9fd35570.jpg">

**9. Number trong Java**
- Khi làm việc với Number, chúng ta sử dụng các kiểu dữ liệu gốc như byte, int, long, double,...
- Các phương thức của lớp Number trong Java

<img src="https://2.pik.vn/2018fb4a0d35-4541-4fed-995a-be76a647fb5a.jpg">

<img src="https://2.pik.vn/2018bfc50082-6f2e-4c09-8300-e260ef9f0d5a.jpg">

<img src="https://2.pik.vn/2018be35be08-f7d0-4abf-9a2b-618162f74aff.jpg">

<img src="https://2.pik.vn/20184f4fbefc-faea-4b0e-8c78-5bb6adefb7e4.jpg">

<img src="https://2.pik.vn/201855e857f0-8cac-4ad5-b441-257cc35f721b.jpg">

**10. Character trong Java**
- Khi làm việc với ký tự, sử dụng kiểu dữ liệu char gốc.
- Các ký tự ngắt trong Java:

<img src="https://2.pik.vn/2018914ebe32-b1d2-4e28-9273-6dc38ad8b789.jpg">

- Các phương thức của lớp Character trong Java:

<img src="https://2.pik.vn/2018b974be1b-3ab2-410d-8572-19b5409e668d.jpg">

<img src="https://2.pik.vn/20187f2bcb25-95ef-4db6-9dad-90fc98c9ebbe.jpg">

**10. Hướng đối tượng (OOP)**
- Đối tượng (Object): là thực thể mang tính vật lý và logic, đối tượng có trạng thái và hành vi.
- Lớp (class): là 1 nhóm các đối tượng có các thuộc tính chung.

*Đối tượng trong Java*
- Một đối tượng có 3 đặc trưng: trạng thái, hành vi, nhận diện
- Đối tượng là instance (kết quả) của một lớp.

*Lớp trong Java*
- Lớp là một template hoặc bản thiết kế từ đó đối tượng được tạo.
- Một lớp bao gồm: thành viên dữ liệu, phương thức, constructor, block, lớp và interface.
- Cú pháp:
            class ten_lop{
                thanh_vien_du_lieu;
                phuong_thuc;
            }
- Một lớp có thể có bất kỳ loại biến sau:

    Biến Local: được ĐN trong phương thức, constructor, block.

    Biến Instance: là biến trong 1 lớp nhưng ở bên ngoài bất kỳ phương thức nào.

    Biến class: đc khai báo với 1 lớp, bên ngoài bất kỳ phương thức nào với từ khóa static.

*Phương thức trong Java*
- Khá giống hàm, sd để trưng bày hành vi of 1 đối tượng.
- Sd từ khóa new để cấp phát bộ nhớ tại runtime.

*Constructor trong Java*
- Khi một đối tượng mới được tạo ra ít nhất một constructor sẽ được gọi.
- Construcotr có cùng tên với lớp đó.

*Phương thức trong Java*
- Phương thức là tập hợp các lệnh được nhóm cùng với nhau để thực hiện 1 hành động.
- Cú pháp:
    public static int tenPhuongThuc(int a, int b){
        // phần thân phương thức
    }
- Gọi phương thức trong Java: 2 cách: phương thức trả về 1 giá trị, phương thức không trả về giá trị nào.
- Void trong Java: tạo các phương thức mà không trả về giá trị nào.
- Truyền các tham số bởi giá trị trong Java: các tham số có thể được truyền bởi giá trị hoặc bởi tham chiếu. Truyền các tham số bởi giá trị nghĩa là gọi 1 phương thức với 1 tham số, thông qua điều này giá trị tham số được truyền tới tham số.
- Nạp chồng phương thức (Method overloading): một lớp có 2 hoặc nhiều phương thức cùng tên nhưng khác nhau về tham số nó được biết đên như là phương thức overloading.
- Sử dụng các tham số dòng lệnh (conman-line): khi muốn truyền thông tin vào trong 1 chương trình đang chạy, điều này được thực hiện bởi việc truyền các tham số dòng lệnh tới phương thức main(). 
- Constructor trong Java: 1 constructor khởi tạo 1 đối tượng khi nó được tạo. Nó cùng tên với lớp của nó và cú pháp tương tự như 1 phương thức, tuy nhiên các constructor không có kiểu trả về rõ ràng. Một nét đặc trưng là, bạn sẽ sử dụng một constructor để cung cấp các giá trị khởi tạo tới các biến instance được định nghĩa bởi lớp, hoặc để thực thi bất kỳ thủ tục khởi đầu nào khác được yêu cầu để tạo một đối tượng theo mẫu. Tất cả các lớp đều có các constructor, dù bạn có hay không định nghĩa nó, bởi vì Java tự động cung cấp một constructor mặc định mà khởi tạo tất cả biến thành viên về zero. Tuy nhiên, một khi bạn định nghĩa constructor cho riêng bạn, thì constructor mặc định sẽ không còn được sử dụng nữa. Thường thì, bạn sẽ cần một constructor mà chấp nhận một hoặc nhiều tham số. Các tham số được thêm tới một constructor theo cách tương tự như chúng được thêm tới một phương thức, vừa khai báo chúng bên trong dấu ngoặc đơn ở sau tên của constructor.
    // Một constructor
    class MyClass(){
        int x;

        // Sau đây là constructor
        MyClass(int i){
            x = i;
        }
    }
    => Gọi được constructor để khởi tạo các đối tượng sau:
    public class ConsDemo{
        public static void main(String args[]){
            MyClass t1 = new MyClass(10);
            MyClass t2 = new MyClass(20);
            System.out.println(t1.x + " " + t2.x);
        }
    }
- Các tham số biến (var-args): khả năng truyền một số các tham số biến cùng kiểu tới một phương thức, tham số trong phương thức được khai báo như sau: tenKieu... tenThamSo 
- Phương thức finalize() trong Java: định nghĩa một phương thức mà sẽ được gọi ngay trước khi hủy 1 đối tượng, có thể được sử dụng để chắc chắn rằng 1 đối tượng hoàn toàn kết thúc.

**Nạp chồng phương thức trong Java**
- Nạp chồng phương thức (Method Overloading) là một lớp có nhiều phương thức cùng tên nhưng có số tham số khác nhau.
- Có 2 cách nạp chồng phương thức: thay đổi tham số, thay đổi kiểu dữ liệu.
- Không thể nạp chồng phương thức bằng cách thay đổi kiểu trả về của phương thức, vì việc này gây ra tính lưỡng tính mơ hồ.
- Có thể nạp chồng phương thức main(), có thể có bất kỳ số lượng phương thức main nào trong 1 lớp bởi nạp chồng phương thức.
- Nạp chông phương thức và TypePromotion trong Java: một kiểu được promote thành 1 kiểu khác hoàn toàn nếu không tìm thấy kiểu dũ liệu nào được kết nối.

<img src="https://2.pik.vn/201818352f5f-4225-43a5-82b5-8b0ff2298d7b.jpg">

Trong sơ đồ trên, byte có thể được promote thành short, int, long, float, double. Kiểu short có thể được promote thành int,long, float, double. Kiểu char có thể được promote thành int, float, long, double...
- Overload: 2 hay nhiều hàm cùng tên mà khác số lượng tham số hoặc khác kiểu tham số.

**Constructor trong Java**
