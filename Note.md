# Học Java

## Mục Lục

[1. Định nghĩa cơ bản](#1)

[2. Cú pháp cơ bản trong Java](#2)

[3. JDK, JRE, JVM trong Java](#3)

[4. Các kiểu biến trong Java](#4)

[5. Kiểu dữ liệu trong Java](#5)

[6. Toán tử trong Java](#6)

[7. Các kiểu vòng lặp](#7)

[8. Lệnh if/else, switch/case](#8)

[9. Number trong Java](#9)

[10. Character trong Java](#10)

[11. Hướng đối tượng (OOP)](#11)

[12. Nạp chồng phương thức trong Java](#12)

[13. Constructor trong Java](#13)

[14. Từ khóa Static](#14)

[15. Từ khóa this trong Java](#15)

[16. Tính kế thừa - Từ khóa extends và implenments](#16)

[17. Quan hệ HAS-A (tham chiếu) trong Java](#17)

[18. Ghi đè phương thức (Overriding)](#18)


    *1 file .java không giới hạn số class trong 1 file. Tuy nhiên trong 1 file chỉ được có duy nhất 1 public class.*

    *Phân biệt chữ hoa và chữ thường*

<a name="1. Định nghĩa cơ bản"></a>

**1. Định nghĩa cơ bản**

- Đối tượng: có trạng thái và hành vi.
- Lớp: mô tả trạng thái, hàng vi của đối tượng mà nó hỗ trợ.
- Phương thức: 1 phương thức đơn giản là 1 hành vi. Một lớp có thể bao gồm nhiều phương thức. Trong mỗi phương thức có những phép toán logic, dữ liệu được xử lý và tất cả các hành động được thực thi.
- Biến: mỗi đối tượng có một tập các biến duy nhất. Mỗi trạng thái của đối tượng được khởi tạo bởi giá trị và gán với những biến.

<a name="2. Cú pháp cơ bản trong Java"></a>

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

<a name="3. JDK, JRE, JVM trong Java"></a>

**3. JDK, JRE, JVM trong Java**
- JVM (Java Virtual Machine) là 1 máy ảo giúp máy tính chạy các chương trình Java. JVM thực hiện: tải code, kiểm tra code, thực thi code, cung cấp môi trường runtime.
- JRE (Java Runtime Environment) sử dụng để cung cấp môi trường runtime. JRE bao gồm  tập hợp các thư viện và các file khác mà JVM sử dụng tại runtime.
- JDK (Java Development Kit) bao gồm JRE và các Development Tool.

<a name="4. Các kiểu biến trong Java"></a>

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

<a name="5. Kiểu dữ liệu trong Java"></a>

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

<a name="6. Toán tử trong Java"></a>

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

<a name="7. Các kiểu vòng lặp"></a>

**7. Các kiểu vòng lặp**

<img src="https://2.pik.vn/2018e00a3576-bb83-4361-8b82-1698679cca1f.jpg">

<img src="https://2.pik.vn/201828bccadc-4914-4c48-9b15-3474d1696f8e.jpg">

<a name="8. Lệnh if/else, switch/case"></a>


**8. Lệnh if/else, switch/case**

<img src="https://2.pik.vn/2018a8010fc3-bc3d-4084-8728-d52a9fd35570.jpg">

<a name="9. Number trong Java"></a>

**9. Number trong Java**
- Khi làm việc với Number, chúng ta sử dụng các kiểu dữ liệu gốc như byte, int, long, double,...
- Các phương thức của lớp Number trong Java

<img src="https://2.pik.vn/2018fb4a0d35-4541-4fed-995a-be76a647fb5a.jpg">

<img src="https://2.pik.vn/2018bfc50082-6f2e-4c09-8300-e260ef9f0d5a.jpg">

<img src="https://2.pik.vn/2018be35be08-f7d0-4abf-9a2b-618162f74aff.jpg">

<img src="https://2.pik.vn/20184f4fbefc-faea-4b0e-8c78-5bb6adefb7e4.jpg">

<img src="https://2.pik.vn/201855e857f0-8cac-4ad5-b441-257cc35f721b.jpg">

<a name="10. Character trong Java"></a>

**10. Character trong Java**
- Khi làm việc với ký tự, sử dụng kiểu dữ liệu char gốc.
- Các ký tự ngắt trong Java:

<img src="https://2.pik.vn/2018914ebe32-b1d2-4e28-9273-6dc38ad8b789.jpg">

- Các phương thức của lớp Character trong Java:

<img src="https://2.pik.vn/2018b974be1b-3ab2-410d-8572-19b5409e668d.jpg">

<img src="https://2.pik.vn/20187f2bcb25-95ef-4db6-9dad-90fc98c9ebbe.jpg">

<a name="11. Hướng đối tượng (OOP)"></a>

**11. Hướng đối tượng (OOP)**
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
- Các tham số biến (var-args): khả năng truyền một số các tham số biến cùng kiểu tới một phương thức, tham số trong phương thức được khai báo như sau: tenKieu... tenThamSo 
- Phương thức finalize() trong Java: định nghĩa một phương thức mà sẽ được gọi ngay trước khi hủy 1 đối tượng, có thể được sử dụng để chắc chắn rằng 1 đối tượng hoàn toàn kết thúc.

<a name="12. Nạp chồng phương thức trong Java"></a>

**12. Nạp chồng phương thức trong Java**
- Nạp chồng phương thức (Method Overloading) là một lớp có nhiều phương thức cùng tên nhưng có số tham số khác nhau.
- Có 2 cách nạp chồng phương thức: thay đổi tham số, thay đổi kiểu dữ liệu.
- Không thể nạp chồng phương thức bằng cách thay đổi kiểu trả về của phương thức, vì việc này gây ra tính lưỡng tính mơ hồ.
- Có thể nạp chồng phương thức main(), có thể có bất kỳ số lượng phương thức main nào trong 1 lớp bởi nạp chồng phương thức.
- Nạp chông phương thức và TypePromotion trong Java: một kiểu được promote thành 1 kiểu khác hoàn toàn nếu không tìm thấy kiểu dũ liệu nào được kết nối.

<img src="https://2.pik.vn/201818352f5f-4225-43a5-82b5-8b0ff2298d7b.jpg">

Trong sơ đồ trên, byte có thể được promote thành short, int, long, float, double. Kiểu short có thể được promote thành int,long, float, double. Kiểu char có thể được promote thành int, float, long, double...
- Overload: 2 hay nhiều hàm cùng tên mà khác số lượng tham số hoặc khác kiểu tham số.

<a name="13. Constructor trong Java"></a>

**13. Constructor trong Java**
- 1 constructor khởi tạo 1 đối tượng khi nó được tạo. Nó cùng tên với lớp của nó và cú pháp tương tự như 1 phương thức, tuy nhiên các constructor không có kiểu trả về rõ ràng. Một nét đặc trưng là, bạn sẽ sử dụng một constructor để cung cấp các giá trị khởi tạo tới các biến instance được định nghĩa bởi lớp, hoặc để thực thi bất kỳ thủ tục khởi đầu nào khác được yêu cầu để tạo một đối tượng theo mẫu. Tất cả các lớp đều có các constructor, dù bạn có hay không định nghĩa nó, bởi vì Java tự động cung cấp một constructor mặc định mà khởi tạo tất cả biến thành viên về zero. Tuy nhiên, một khi bạn định nghĩa constructor cho riêng bạn, thì constructor mặc định sẽ không còn được sử dụng nữa. Thường thì, bạn sẽ cần một constructor mà chấp nhận một hoặc nhiều tham số. Các tham số được thêm tới một constructor theo cách tương tự như chúng được thêm tới một phương thức, vừa khai báo chúng bên trong dấu ngoặc đơn ở sau tên của constructor.
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
- Khi một đối tượng mới được tạo ra ít nhất một constructor sẽ được gọi.
- Construcotr có cùng tên với lớp đó.
- Constructor là 1 kiểu phương thức đặc biệt được sử dụng để khởi tạo đối tượng, constructor được triệu hồi tại thời gian tạo đối tượng, nó xây dựng giá trị, cung cấp dữ liệu cho đối tượng.
- Mỗi lớp có ít nhất một constructor, các constructor có cùng tên với lớp đó.
- Quy tắc tạo constructor: có 2 loại constructor: loại mặc định k có tham số (nóBlank Space cung cấp giá trị mặc định như 0, null,... tùy thuộc vào kiểu dữ liệu), constructor được tham số hóa (cung cấp giá trị khá nhau cho các đối tượng riêng biệt).

    Constructor mặc định: *ten_lop(){}* (nếu không có constructor nào được xác định trong một lớp thì Compliler tự động tạo một constructor mặc định).

    Constructor được tham số hóa.

- Nạp chồng constructor trong Java: một lớp có thể có bất cứ số lượng Constructor nào mà khác nhau về danh sách tham số. Phân biệt các constructor bằng việc phân tích số tham số trong danh sách và kiểu của chúng.
- Sự khác nhau giữa Constructor và Phương thức trong Java

<img src="https://2.pik.vn/2018fa59f11e-fb40-4861-96e4-81291b74e138.jpg">

- Copy Constructor trong Java: k có Copy Constructor như trong C++. Tuy nhiên, có thể sao chép các giá trị của một đối tượng tới đối tượng khác. Có 3 cách thực hiện việc sao chép các giá trị: Bởi Constructor; Bởi gán các giá trị của một đối tượng vào trong đối tượng khác; Bởi phương thức clone() của lớp Object.
- Sao chép các giá trị mà không sử dụng Constructor: bằng cách gán các giá trị của đối tượng đó vào trong đối tượng khác. Trong trường hợp này, không cần tạo Constructor.
- Constructor trả về giá trị, đó là instance(sự thể hiện) của lớp hiện tại, bạn không thể sử dụng kiểu trả về tuy vậy nó trả về một giá trị.
- Constructor có thực hiện các tác vụ khác ngoài khởi tạo. Giống như quá trình tạo đối tượng, bắt đầu một Thread, gọi phương thức,... bạn có thể thực hiện bất cứ hoạt động nào trong Constructor như khi bạn thực hiện trong phương thức.

<a name="14. Từ khóa Static"></a>

**14. Từ khóa Static**
- Sử dụng để quản lý bộ nhớ.
- Có thể áp dụng từ khóa static với biến (cũng ddc gọi là biến lớp, biến class), phương thức (cũng đc gọi là phương thức lớp), khối, các lớp đc lặp.
- Static thuộc về lớp chứ không thuộc về instance(sự thể hiện) của lớp.
- Khi khai báo biến là static, thì biến đó là biến tĩnh hay biến static. Biến static giúp chương trình sử dụng hiệu quả hơn (tiết kiệm bộ nhớ).
- Phương thức Static trong Java: Nếu áp dụng từ khóa static với bất kỳ phương thức nào, thì phương thức đó được gọi là phương thức static; Một phương thức static thuộc lớp chứ không phải đối tượng của lớp; Phương thức static có thể ddc triệu hội mà không cần tạo 1 instance của 1 lớp; Phương thức static có thể truy cập thành viên dữ liệu static và có thể thay đổi giá trị của nó.
- Hạn chế của phương thức static:

    Không thể sử dụng thành viên dữ liệu non-static hoặc gọi trực tiếp phương thức non-static.

    Từ khóa this và super không thể được sử dụng trong ngữ cảnh static.

- Phương thức main trong Java là static vì đối tượng là không cần thiết để gọi phương thức static nếu nó là phương thức non-static, JVM đầu tiên tạo đối tượng và sau đó gọi phương thức main() mà có thể gây ra vấn đề cấp phát bộ nhớ phụ.
- Khối static trong Java: được sử dụng để khởi tạo thành viên dữ liệu static, nó được thực thi trước phương thức main tại thời gian tải lớp.
- Có thể thực thi 1 chương trình mà không có phương thức main(), một trong các cách là khối static trong phiên bản trước của JDK, không trong JDK 1.7.

<a name="15. Từ khóa this trong Java"></a>

**15. Từ khóa this trong Java**
- Trong Java, this là một biến tham chiếu mà tham chiếu tới đối tượng hiện tại.
- Sử dụng từ khóa this trong Java:

    SD để tham chiếu biến instance của lớp (khi biến cục bộ và biến instance giống nhau thì cần sd từ khóa this).

    this() sd để triệu hồi Constructor của lớp hiện tại.

    SD để triệu hồi ngầm định phương thức lớp hiện tại.

    Có thể đc truyền như 1 tham số trong lời gọi phương thức.

    Có thể đc truyền như 1 tham số trong lời gọi Constructor.

    SD để trả về instance của lớp hiện tại.

<a name="16. Tính kế thừa - Từ khóa extends và implenments"></a>

**16. Tính kế thừa - Từ khóa extends và implenments**
- Tính kế thừa trong Java là một kỹ thuật mà trong đó 1 đối tượng thu được tất cả thuộc tính và hành vi của đối tượng cha.
- Có thể tạo các lớp mới mà được xây dựng dựa trên các lớp đang tồn tại.
- Khi kế thừa từ 1 lớp đang tồn tại, có thể tái sử dụng các phương thức và các trường của lớp cha, cũng có thể bố sung thêm các phương thức và các trường khác.
- Tính kế thừa biến diễn mỗi quan hệ IS-A, hay mph cha-con.
- Từ khóa extends và implements có thể định nghĩa 1 kiểu là loại IS-A của loại khác; sử dụng từ khóa, chúng ta có thể tạo ra 1 đối tượng sử dụng thuộc tính của đối tượng khác. Chúng ta sử dụng từ khóa extends của lớp con để có thể kế thừa các thuộc tính của lớp cha trừ các thuộc tính private.
- Sử dụng tính kế thừa: để ghi đè phương thức (method overriding) do đó có thể thu được tính đa hình tại runtime, để làm tăng tính tái sử dụng code.
- Từ khóa extends chỉ ra rằng bạn đang tạo 1 lớp mới từ một lớp đang tồn tại:

    class ten_lop_con extends ten_lop_cha{

        // các phương thức và các trường

    }

- Các loại kế thừa trong Java: có 3 loại single(đơn), multilevel(nhiều tầng), hierarchical(có cấu trúc); trong lập trình Java đa kế thừa(multiple) và kế thừa lai(hybrid) chỉ được hỗ trợ thông qua interface.
- Đa kế thừa không được hỗ trợ trong Java thông qua lớp (để giảm tính phức tạp và làm đơn giản hóa ngôn ngữ), khi 1 lớp kế thừa từ nhiều lớp thì đây là đa kế thừa.
- Trong Java chỉ hỗ trợ kế thừa đơn, nghĩa là 1 lớp không thể kế thừa từ nhiều hơn 1 lớp.
- Mặc dù vậy, một lớp vẫn có thể implements một hoặc nhiều interface, điều này loại bỏ khả năng không thể đa kế thừa trong Java.
- Từ khóa implements được sử dụng bởi các lớp mà kế thừa từ interface. Interface có thể không bao giờ được kế thừa bởi các lớp.

    VD:

    public ỉnterface A {}

    public class B implements A{}

    public class C extends B{}

*Lớp final là lớp không thể kế thừa* 

<a name="17. Quan hệ HAS-A (tham chiếu) trong Java"></a>

**17. Quan hệ HAS-A (tham chiếu) trong Java** 
- Có những quan hệ chủ yếu dựa vào cách sử dụng, nó xác định có hay không 1 lớp cụ thể HAS-A, quan hệ này giúp chúng ta giảm được dư thừa trong code cũng như tránh các bug.
- Nếu một lớp có 1 tham chiếu thực thể, nó được biết đến như 1 lớp có quan hệ HAS-A.
- Sử dụng HAS-A làm tăng tính tái sử dụng code, khi không có mqh IS-A thì HAS-A là lựa chọn tốt nhất.
- Tính kế thừa nên chỉ được sử dụng nếu mqh IS-A được duy trì thông qua suốt vòng đời của đối tượng có liên quan, nếu không thì quan hệ HAS-A là lựa chọn tốt nhất.
- VD: lớp Employee có 1 đối tượng là Address, đối tượng này chứa thông tin riêng như city, state, country,... còn lớp Employee chứa các thông tin chung như id, name...

<a name="18. Ghi đè phương thức (Overriding)"></a>

**18. Ghi đè phương thức (Overriding)**
- Nếu lớp con có cùng phương thức như đã được khai báo trong lớp cha thì đó là Overriding.
- Overriding được sd để cung cấp trình triển khai cụ thể của 1 phương thức mà đã được cung cấp bởi lớp cha của nó.
- Overriding được sd để thu được tính đa hình tại runtime.
- Quy tắc: phương thức cùng tên như trong lớp cha; phương thức phải có cùng tham số như trong lớp cha; phải là quan hệ IS-A (kế thừa).
- Không thể ghi đè phương thức static, bởi vì phương thức static được gắn kết với lớp trong khi đó phương thức instance được gắn kết với đối tượng. Static thuộc sở hữu Class Area và instance thuộc sở hữu Heap Area.
- Phương thức main cũng là phương thức static nên không thể ghi đè phương thức main.
- Sự khác nhau giữa nạp chồng và ghi đè:

<img src="https://2.pik.vn/2018f77a2a7a-bae3-4752-9819-3af3a85dd171.jpg">

<a name="19. Kiểu trả về covariant trong Java"></a>

**19. Kiểu trả về covariant trong Java**

















