# Học Java

## Mục Lục

[1. Định nghĩa cơ bản](#Dinhnghiacoban)

[2. Cú pháp cơ bản trong Java](#CuphapcobantrongJava)

[3. JDK, JRE, JVM trong Java](#JDK,JRE,JVMtrongJava)

[4. Các kiểu biến trong Java](#CackieubientrongJava)

[5. Kiểu dữ liệu trong Java](#KieudulieutrongJava)

[6. Toán tử trong Java](#ToantutrongJava)

[7. Các kiểu vòng lặp](#Cackieuvonglap)

[8. Lệnh if/else, switch/case](#Lenhif/else,switch/case)

[9. Number trong Java](#NumbertrongJava)

[10. Character trong Java](#CharactertrongJava)

[11. Hướng đối tượng (OOP)](#Huongdoituong(OOP))

[12. Nạp chồng phương thức trong Java](#NapchongphuongthuctrongJava)

[13. Constructor trong Java](#ConstructortrongJava)

[14. Từ khóa Static](#TukhoaStatic)

[15. Từ khóa this trong Java](#TukhoathistrongJava)

[16. Tính kế thừa - Từ khóa extends và implenments](#Tinhkethua-Tukhoaextendsvaimplement)

[17. Quan hệ HAS-A (tham chiếu) trong Java](#QuanheHAS-A(thamchieu)trongJava)

[18. Ghi đè phương thức (Overriding)](#Ghidephuongthuc(Overriding))

[19. Kiểu trả về covariant trong Java](#KieutravecovarianttrongJava)


    *1 file .java không giới hạn số class trong 1 file. Tuy nhiên trong 1 file chỉ được có duy nhất 1 public class.*

    *Phân biệt chữ hoa và chữ thường*

<a name="Dinhnghiacoban"></a>

**1. Định nghĩa cơ bản**

- Đối tượng: có trạng thái và hành vi.
- Lớp: mô tả trạng thái, hàng vi của đối tượng mà nó hỗ trợ.
- Phương thức: 1 phương thức đơn giản là 1 hành vi. Một lớp có thể bao gồm nhiều phương thức. Trong mỗi phương thức có những phép toán logic, dữ liệu được xử lý và tất cả các hành động được thực thi.
- Biến: mỗi đối tượng có một tập các biến duy nhất. Mỗi trạng thái của đối tượng được khởi tạo bởi giá trị và gán với những biến.

<a name="CuphapcobantrongJava"></a>

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

<a name="JDK,JRE,JVMtrongJava"></a>

**3. JDK, JRE, JVM trong Java**
- JVM (Java Virtual Machine) là 1 máy ảo giúp máy tính chạy các chương trình Java. JVM thực hiện: tải code, kiểm tra code, thực thi code, cung cấp môi trường runtime.
- JRE (Java Runtime Environment) sử dụng để cung cấp môi trường runtime. JRE bao gồm  tập hợp các thư viện và các file khác mà JVM sử dụng tại runtime.
- JDK (Java Development Kit) bao gồm JRE và các Development Tool.

<a name="CackieubientrongJava"></a>

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

<a name="KieudulieutrongJava"></a>

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

<a name="ToantutrongJava"></a>

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

<a name="Cackieuvonglap"></a>

**7. Các kiểu vòng lặp**

<img src="https://2.pik.vn/2018e00a3576-bb83-4361-8b82-1698679cca1f.jpg">

<img src="https://2.pik.vn/201828bccadc-4914-4c48-9b15-3474d1696f8e.jpg">

<a name="Lenhif/else,switch/case"></a>


**8. Lệnh if/else, switch/case**

<img src="https://2.pik.vn/2018a8010fc3-bc3d-4084-8728-d52a9fd35570.jpg">

<a name="NumbertrongJava"></a>

**9. Number trong Java**
- Khi làm việc với Number, chúng ta sử dụng các kiểu dữ liệu gốc như byte, int, long, double,...
- Các phương thức của lớp Number trong Java

<img src="https://2.pik.vn/2018fb4a0d35-4541-4fed-995a-be76a647fb5a.jpg">

<img src="https://2.pik.vn/2018bfc50082-6f2e-4c09-8300-e260ef9f0d5a.jpg">

<img src="https://2.pik.vn/2018be35be08-f7d0-4abf-9a2b-618162f74aff.jpg">

<img src="https://2.pik.vn/20184f4fbefc-faea-4b0e-8c78-5bb6adefb7e4.jpg">

<img src="https://2.pik.vn/201855e857f0-8cac-4ad5-b441-257cc35f721b.jpg">

<a name="CharactertrongJava"></a>

**10. Character trong Java**
- Khi làm việc với ký tự, sử dụng kiểu dữ liệu char gốc.
- Các ký tự ngắt trong Java:

<img src="https://2.pik.vn/2018914ebe32-b1d2-4e28-9273-6dc38ad8b789.jpg">

- Các phương thức của lớp Character trong Java:

<img src="https://2.pik.vn/2018b974be1b-3ab2-410d-8572-19b5409e668d.jpg">

<img src="https://2.pik.vn/20187f2bcb25-95ef-4db6-9dad-90fc98c9ebbe.jpg">

<a name="Huongdoituong(OOP)"></a>

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

<a name="NapchongphuongthuctrongJava"></a>

**12. Nạp chồng phương thức trong Java**
- Nạp chồng phương thức (Method Overloading) là một lớp có nhiều phương thức cùng tên nhưng có số tham số khác nhau.
- Có 2 cách nạp chồng phương thức: thay đổi tham số, thay đổi kiểu dữ liệu.
- Không thể nạp chồng phương thức bằng cách thay đổi kiểu trả về của phương thức, vì việc này gây ra tính lưỡng tính mơ hồ.
- Có thể nạp chồng phương thức main(), có thể có bất kỳ số lượng phương thức main nào trong 1 lớp bởi nạp chồng phương thức.
- Nạp chông phương thức và TypePromotion trong Java: một kiểu được promote thành 1 kiểu khác hoàn toàn nếu không tìm thấy kiểu dũ liệu nào được kết nối.

<img src="https://2.pik.vn/201818352f5f-4225-43a5-82b5-8b0ff2298d7b.jpg">

Trong sơ đồ trên, byte có thể được promote thành short, int, long, float, double. Kiểu short có thể được promote thành int,long, float, double. Kiểu char có thể được promote thành int, float, long, double...
- Overload: 2 hay nhiều hàm cùng tên mà khác số lượng tham số hoặc khác kiểu tham số.

<a name="ConstructortrongJava"></a>

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

<a name="TukhoaStatic"></a>

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

<a name="TukhoathistrongJava"></a>

**15. Từ khóa this trong Java**
- Trong Java, this là một biến tham chiếu mà tham chiếu tới đối tượng hiện tại.
- Sử dụng từ khóa this trong Java:

    SD để tham chiếu biến instance của lớp (khi biến cục bộ và biến instance giống nhau thì cần sd từ khóa this).

    this() sd để triệu hồi Constructor của lớp hiện tại.

    SD để triệu hồi ngầm định phương thức lớp hiện tại.

    Có thể đc truyền như 1 tham số trong lời gọi phương thức.

    Có thể đc truyền như 1 tham số trong lời gọi Constructor.

    SD để trả về instance của lớp hiện tại.

<a name="Tinhkethua-Tukhoaextendsvaimplement"></a>

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

<a name="QuanheHAS-A(thamchieu)trongJava"></a>

**17. Quan hệ HAS-A (tham chiếu) trong Java** 
- Có những quan hệ chủ yếu dựa vào cách sử dụng, nó xác định có hay không 1 lớp cụ thể HAS-A, quan hệ này giúp chúng ta giảm được dư thừa trong code cũng như tránh các bug.
- Nếu một lớp có 1 tham chiếu thực thể, nó được biết đến như 1 lớp có quan hệ HAS-A.
- Sử dụng HAS-A làm tăng tính tái sử dụng code, khi không có mqh IS-A thì HAS-A là lựa chọn tốt nhất.
- Tính kế thừa nên chỉ được sử dụng nếu mqh IS-A được duy trì thông qua suốt vòng đời của đối tượng có liên quan, nếu không thì quan hệ HAS-A là lựa chọn tốt nhất.
- VD: lớp Employee có 1 đối tượng là Address, đối tượng này chứa thông tin riêng như city, state, country,... còn lớp Employee chứa các thông tin chung như id, name...

<a name="Ghidephuongthuc(Overriding)"></a>

**18. Ghi đè phương thức (Overriding)**
- Nếu lớp con có cùng phương thức như đã được khai báo trong lớp cha thì đó là Overriding.
- Overriding được sd để cung cấp trình triển khai cụ thể của 1 phương thức mà đã được cung cấp bởi lớp cha của nó.
- Overriding được sd để thu được tính đa hình tại runtime.
- Quy tắc: phương thức cùng tên như trong lớp cha; phương thức phải có cùng tham số như trong lớp cha; phải là quan hệ IS-A (kế thừa).
- Không thể ghi đè phương thức static, bởi vì phương thức static được gắn kết với lớp trong khi đó phương thức instance được gắn kết với đối tượng. Static thuộc sở hữu Class Area và instance thuộc sở hữu Heap Area.
- Phương thức main cũng là phương thức static nên không thể ghi đè phương thức main.
- Sự khác nhau giữa nạp chồng và ghi đè:

<img src="https://2.pik.vn/2018f77a2a7a-bae3-4752-9819-3af3a85dd171.jpg">

<a name="KieutravecovarianttrongJava"></a>

**19. Kiểu trả về covariant trong Java**
- Kiểu trả về covariant xác định rằng kiểu trả về có thể thay đổi trong lớp con, tức là một phương thức có thể trả về kiểu hẹp hơn khi phương thức đó được override ở class con.
- Có thể ghi đè phương thức bằng cách thay đổi kiểu trả về nếu lớp con ghi đè bất cứ phương thức nào mà có kiểu trả về là không phải kiểu gốc.

<a name="Tukhoasuper"></a>

**20. Từ khóa super**
- Từ khóa super trong java là 1 biến tham chiếu được sd để tham chiếu đến đối tượng lớp cha gần nhất; bất cứ khi nào tạo instance của lớp con, 1 instance của lớp cha được tạo ngầm định, được tham chiếu bởi biến super.
- Sự sd từ khóa super trong Java: super được sử dụng để tham chiếu biến instance của lớp cha gần nhất; super() đc sd để triệu hồi Constructor của lớp cha gần nhất; super được sử dụng để triệu hồi phương thức của lớp cha gần nhất.
- super được sử dụng để tham chiếu biến instance của lớp cha gần nhất: khi 2 lớp cha và con có cùng thuộc tính chung, biến instance của lớp con được tham chiếu bởi instance theo mặc định, nhưng mình phải tham chiếu đến biến instance của lớp cha,nên dùng từ khóa super để phân biệt giữa biến instance của lớp cha và lớp con.
- super() đc sd để triệu hồi Constructor của lớp cha gần nhất: super() được tự động thêm vào trong mỗi Constructor của lớp bởi Compiler. Constructor mặc định được cung cấp bởi Compiler nhưng nó cũng thêm super() cho lệnh đầu tiên. Nếu bạn đang tạo constructor cho riêng mình và bạn không có this() hoặc super() như là lệnh đầu tiên, thì Compiler sẽ cung cấp super() như là lệnh đầu tiên của Constructor đó.
- super được sử dụng để triệu hồi phương thức của lớp cha gần nhất, nó nên được sd trong lớp con mà có chứa cùng phương thức như lớp cha.

<a name="Tukhoafinal"></a>

**21. Từ khóa final**
- Từ khóa final trong Java được sử dụng để hạn chế người dùng; nó có thể được sử dụng trong nhiều ngữ cảnh: với biến, với phương thức, với lớp.
- Có thể áp dụng với các biến, 1 biến final không có giá trị nào là biến final trống hoặc biến final không được khởi tạo; nó chỉ có thể được khởi tạo trong COnstructor; biến final trống cũng có thể là static mà sẽ chỉ được khởi tạo trong khối static.
- Nếu tạo bất cứ biến nào là final, sẽ không thể thay đổi giá trị của biến final(là hằng số).
- Phương thức final trong Java: nếu tạo bất cứ phương thức nào là final, thì không thể ghi đè nó.
- Lớp final trong Java: nếu tạo bất cứ lớp nào là final thì không thể kế thừa nó.
- Phương thức final có được kế thừa nhưng không thể ghi đè.
- Biến final không được khởi tạo tại thời điểm khai báo được gọi là biến final trống. Nếu muốn tạo 1 biến mà được khởi tạo tại thời điểm tạo đối tượng và 1 khi nó đã được khởi tạo thì không thể bị thay đổi, thì biến final trống là hữu ích trong trường hợp này. Biến final trống chỉ có thể khởi tại trong Constructor.
- Biến static final không đc khởi tạo tại thời điểm khai báo thì đó là biến static final trống, nó chỉ có thể đc khởi tạo trong khối static.
- Tham số final: nếu khai báo bất cứ tham số nào là final thì không thể thay đổi giá trị của nó.
- Không thể khai báo 1 constructor final thì constructor không bao giờ được kế thừa.

<a name="TinhdahinhtrongJava"></a>

**22. Tính đa hình trong Java**
- Đa hình là 1 khái niệm mà có thể thực hiện 1 hành động đơn theo nhiều cách khác nhau. Có 2 kiểu đa hình trong Java: đa hình tại compile time (nạp chồng phương thức) và đa hình runtime (ghi đè phương thức).
- Cần phải biết có cách nào truy cập 1 đối tượng qua các biến tham chiếu? Một biến tham chiếu có thể chỉ là 1 kiểu. Khi được khai báo, kiểu của biến tham chiếu này không thể thay đổi.
- Biến tham chiếu có thể được gán cho các đối tượng khác cung cấp mà không được khai báo final. Kiểu của biến tham chiếu sẽ xác định phương thức mà có thể đc triệu hồi trên đối tượng.
- Một biến tham chiếu có thể được hướng đến bất kỳ đối tượng với kiểu khai báo hoặc bất kỳ kiểu con nào của biến khai báo. Một biến tham chiếu có thể khai báo như là 1 class hoặc interface.
- Đa hình tại runtime trong Java: là 1 tiến trình trong đó 1 lời gọi tới 1 phương thức được ghi đè đưuọc xử lý tại runtime thay vì tại compile time. Trong tiến trình này, 1 phương thức được ghi đè được gọi thông qua biến tham chiếu của 1 lớp cha; việc quyết định phương thức được gọi dựa trên đối tượng nào đang đc tham chiếu bởi biến tham chiếu.
- Upcasting: khi biến tham chiếu của lớp cha tham chiếu tới đối tượng  của lớp con thì đó là Upcasting.

    VD: 

    class A{}

    class B extends A{}

    A a=new B();//đây là upcasting

- Đa hình tại runtime trong Java với thành viên dữ liệu: phương thức bị ghi đè không là thành viên dữ liệu vì thế đa hình tại runtime không thể có được bởi thành viên dữ liệu.

<a name="Gankettinhvaganketdong(DynamicBinding)"></a>

**23. Gắn kết tĩnh và Gắn kết động (Dynamic Binding)**
- Binding (gắn kết) là kết nối 1 lời gọi phương thức tới thân phương thức.
- Có 2 kiểu Binding là: Static Binding và Dynamic Binding (late binding).
- Khái niệm Type: 

    1. Biến có 1 kiểu, nó có thể là kiểu gốc hoặc kiểu khác (không phải kiểu gốc): int data=30; //biến data kiểu int

    2. Tham chiếu có 1 kiểu:

        class Dog{

            public static void main(String args[])

            Dog d1;//d1 là kiểu của Dog }

    3. Đối tượng có 1 kiểu. Đối tượng là 1 instance của lớp java cụ thể, nhưng nó cũng là 1 instance của lớp cha.

        class Animal{}

        class Dog extends Animal{

            public static void main(String args[])

            {Dog d1=new Dog();}//d1 là 1 instance của lớp Dog nhưng nó cũng là 1 instance của Animal

        }

- Static Binding: khi kiểu của đối tượng được quyết định tại compile time thì đó là static binding. Nếu có bất cứ phương thức private, final hoặc static nào trong 1 lớp thì đó là static binding. Do đó không thể ghi đè kết quả với lập trình hướng đối tượng trong Static Binding.
- Dynamic Binding: khi kiểu của đối tượng được quyết định tại runtimr thì đó là Dynamic Binding.

<a name="ToantuInstanceof"></a>

**24. Toán tử Instanceof**
- Dùng để kiểm tra xem đối tượng có là instance của kiểu cụ thể: lớp hoặc lớp con hoặc interface hay không.
- Toán tử instanceof còn đc biết đến như là toán tử so sánh kiểu bỏi nó so sánh instance với kiểu, nó trả về true hoặc false.

    class Simple{

        public static void main(Sring args[]){

            Simple s=new Simple();

            System.out.println(s instanceof Simple); //true
        }
    }

- Một đối tượng của kiểu lớp con cũng là 1 kiểu của lớp cha. VD: nếu Dog kế thừa Animal thì đối tượng của Dog có thể được tham chiếu bởi lớp Dog hoặc lớp Animal.   
- Nếu áp dụng toán tử instanceof với bất cứ biến nào có giá trị null, thì nó trả về false.
- Downcasting với toán tử instanceof trong Java: khi kiểu lớp con tham chiếu tới đối tượng của lớp cha thì đó là downcasting. Nếu thực hiện trực tiếp, Compiler sẽ cho 1 lỗi biên dịch. Nếu thực hiện bởi typecasting (ép kiểu) thì ClassCasrException được ném tại runtime. Nhưng nếu sử dụng toán tử instanceof thì downcasting là có thể.

    Dog d=new Animal(); gây lỗi tại thời gian biên dịch vì Dog là lớp con của Animal

    Dog d=(Dog)new Animal(); //biên dịch thành công nhưng ClassCastException bị ném tại runtime

<a name="TinhTruuTuong"></a>

**25. Tính trừu tượng**
- Tính trừu tượng trong Java hướng đến khả năng tạo một đối tượng trừu tượng trong lập trình hướng đối tượng. Một lớp trừu tượng là 1 lớp không được khởi tạo. Tất cả các chức năng khác của lớp vẫn tồn tại, và tất cả các trường, phương thức, và hàm khởi tạo đều được truy cập với 1 cách giống nhau. Bạn không thể tạo một đối tượng với 1 lớp trừu tượng hóa.
- Nếu 1 lớp là lớp trừu tượng và nó không được khởi tạo, lớp này không được sử dụng trừ khi nó là lớp con.
- Lớp Abstract: sử dụng từ khóa abstract để khai báo 1 lớp abstract, từ khóa này xuất hiện trước từ khóa class trong khai báo lớp.
- Phương thức Abstract: nếu muốn 1 lớp chứa 1 phương thức cụ thể nhưng muốn triển khai thực sự phương thức đó để đưuọc quyết định bởi các lớp con thì có thể khai báo phương thức đó trong lớp cha dạng abstract. Từ khóa abstract được sử dụng để khai báo 1 phương thức dạng abstract. Một phương thức gồm 1 chữ số, không có thân phương thức. Phương thức abstract sẽ không có định nghĩa, chữ số của nó được theo sau bởi dấu chấm phảy, không có dấu ngoặc móc ôm theo sau.
- Khai báo 1 phương thức dạng abstract tạo 2 kết quả:

    1. Lớp phải được khai báo abstract, nếu 1 lớp chứa 1 phương thức abstract thì lớp đó cũng phải là abstract.

    2. Bất kỳ lớp con nào phải hoặc override phương thức abstract hoặc khai báo abstract chính nó.

- Một lớp con mà kế thừa 1 phương thức abstract phải ghi đè nó. Nếu nó không thì nó phải là abstract và bất kỳ lớp con nào của chúng phải override nó.
- Một lớp con phải triển khai phương thức abstract nếu không bạn sẽ có 1 cấu trúc phân cấp của các lớp abstract mà không thể được khởi tạo.

<a name="AbstractClass"></a>

**26. Abstract Class**
- Tính trừu tượng là 1 tiến trình ẩn các chi tiết trìn triển khai và chỉ hiện thị tính năng tới người dùng, nó chỉ hiển thị các thức quan trọng tới người dùng và ẩn các chi tiết nội tại. Tính trừu tượng giúp bạn trọng tâm hơn vào đối tượng thay vì quan tâm đến cách nó thực hiện.
- Một lớp được khai báo là abstract thì đó là lớp trừu tượng, nó cần được kế thừa và phương thức của nó được triển khai, nó không thể được khởi tạo.

    abstract class A{}

- Phương thức được khai báo là abstract và không có trình triển khai thì đó là phương thức trừu tượng. Phương thức abstract không có thân phương thức, không có định nghĩa, được theo sau bởi dấu chấm phảy, không có dấu ngoặc móc ôm theo sau

    abstract void printStatus();

- Lớp trừu tượng có thành viên dữ liệu, phương thức trừu tượng, constructor và có thể cả phương thức main().
- Nếu bạn đang kế thừa bất cứ lớp trừu tượng nào mà có phương thức trừu tượng, thì bạn phải cung cấp trình triển khai của các phương thức của lớp trừu tượng này.
- Lớp trừu tượng cũng có thể được sử dụng để cung cấp một số trình triển khai của Interface. Trong tình huống này, người dùng cuối cùng không thể bị bắt buộc phải ghi đè tất cả phương thức của Interface đó.
- Các phương thức của interface là abstract 100%, trong abstract class có thể có phương thức không phải abstract. Trong thiết kế phần mềm, interface thường được dùng để chỉ 2 hay nhiều class cùng làm việc gì đó, trong khi abstract class thường hướng đến quan hệ cha-con trong lập trình hướng đối tượng.

<a name="Interface"></a>

**27. Interface**
- Interface là một kỹ thuật để thu được tính trừu tượng hoàn toàn và đa kế thừa trong Java. Interface trong Java cũng biễu diễn mối quan hệ IS-A. Nó không thể được khởi tạo giống như lớp trừu tượng.
- Các trường của Interface là public, static và final theo mặc định và các phương thức là public và abstract.
- Một Interface trong Java là một tập hợp các phương thức trừu tượng (abstract). 
- Một interface không phải là một lớp. Một lớp mô tả các thuộc tính và hành vi của một đối tượng. Một interface chứa các hành vi mà một class triển khai.
- Trừ khi một lớp triển khai interface là lớp trừu tượng abstract, còn lại tất cả các phương thức của interface cần được định nghĩa trong class.
- Khi ghi đè các phương thức được định nghĩa trong interface, có một số qui tắc sau:

    Các checked exception không nên được khai báo trong phương thức implements, thay vào đó nó nên được khai báo trong phương thức interface hoặc các lớp phụ được khai báo bởi phương thức interface.

    Signature (ký số) của phương thức interface và kiểu trả về nên được duy trì khi ghi đè phương thức (overriding method).

    Một lớp triển khai chính nó có thể là abstract và vì thế các phương thức interface không cần được triển khai.

- Khi triển khai interface, có vài quy tắc sau:

    Một lớp có thể triển khai một hoặc nhiều interface tại một thời điểm.

    Một lớp chỉ có thể kế thừa một lớp khác, nhưng được triển khai nhiều interface.

    Một interface có thể kế thừa từ một interface khác, tương tự cách một lớp có thể kế thừa lớp khác.

- Phân biệt lớp abstract và interface: cả lớp abstract và interface đc sử dụng để thu đc tính trừu tượng, từ đó chúng ta có thể khai báo các phương thức trừu tượng. Cả lớp trừu tượng bà interface không thể được khởi tạo. Nhưng cũng có các điểm khác nhau giữa lớp trừu tượng và interface như sau:

<img src="https://2.pik.vn/2018ee75c852-f174-404f-9ef3-608842788522.jpg">


<a name="PackagetrongJava"></a>

**28. Package trong Java**
- Một package trong Java là một nhóm các kiểu lớp, Interface và package con tương tự nhau. Package trong Java có thể được phân loại thành: Package đã xây dựng sẵn và package do người dùng định nghĩa. Có nhiều package đã xây dựng sẵn như java, lang, awt, javax, swing, net, io, util, sql, … 
- Package được sử dụng trong Java để ngăn cản việc xung đột đặt tên, điều khiên truy cập, giúp việc tìm kiếm/lưu trữ và sử dụng lớp, interface, enumeration, annotation dễ dàng hơn.
- Một vài các package có sẵn trong Java như: java.lang (các lớp cơ bản), java.io (các lớp input và output cơ bản).
- Lợi thế của package: đc sd để phân loại các lớp và các interface để chúng có thể được duy trì dễ dàng hơn; cung cấp bảo vệ truy cập; xóa bỏ các xung đột về đặt tên.
- Từ khóa import trong Java: nếu 1 class sd 1 class khác cùng package, tên package không cần đc sd; lớp trong cùng package tìm thấy nhau mà không cần cú pháp đặc biệt nào.
- VD: 1 lớp Boss đc thêm vào 1 package payroll đã chứ Employee. Lớp Boss có thể ám chỉ đến lớp Employee mà không cần sd tiền tố payroll. Nếu xảy ra trường hợp Boss không nằm trong payroll package, lớp Boss phải sd 1 trong những kỹ thuật sau thể tham chiếu đến class thuộc package khác:

    payroll.Employee //sd tên đầy đủ of class có thể đc sd

    import payroll.*; //Package có thể được nhập bởi sử dụng từ khóa import và wild card (*). 

    import payroll.Employee; //1 class có thể import chính nó với từ khóa import

- Một class file có thể chứa bất kỳ số lệnh import nào, lệnh import phải xuất hiện sau mỗi lệnh khai báo package và trước từ khóa khai báo lớp.
- Cách truy cập package từ package khác: 

    Sử dụng tenpackage.*: tất cả các lớp và interface của package này có thể truy cập, trừ các package con. Từ khóa import được sử dụng để làm cho các lớp và interface của package khác có thể truy cập tới package hiện tại.

     Sd tenpackage.tenlop: chỉ có lớp đc khai báo của package này có thể truy cập.

     Sd tên đầy đủ: chỉ có lớp đc khai báo của package này có thể truy cập. Bây giờ không cần import, nhưng cần sd tên đầy đủ mỗi khi đang truy cập lớp hoặc interface. Nói chung, nó đc sd khi 2 package cùng tên lớp.

- Nếu import 1 package, thì tất cả các lớp và interface của package đó sẽ đc import ngoại trừ lớp và interface của package con. Do đó, cần phải import cả các package con.

- Package con trong Java (subpackage) là package nằm bên trong package khác. Ví dụ: Sun Microsystem đã định nghĩa một package có tên là java chứa nhiều lớp như System, String, Reader, Writer, Socket, … Những lớp này biểu diễn một nhóm cụ thể, ví dụ như các lớp Reader và Writer là cho hoạt động I/O, các lớp Socket và ServerSocket là cho lập trình mạng, …. Vì thế, Sun đã lại phân loại java package thành các subpackage như lang, net, io, … và đặt các lớp liên quan tới IO vào io package, …

<a name="CackieuModifier"></a>

**29. Các kiểu Modifier**
- Modifier là các từ khóa mà bạn thêm vào những định nghĩa để thay đổi ý nghĩa of chúng.
- Có hàng loạt các modifier bao gồm: Access Modifier trong Java; Non-Access Modifier trong Java.
- Để sử dụng 1 Modifier, bao từ khóa của nó trong định nghĩa của 1 lớp, phương thức hoặc biến. Modifier đặt trước phần còn lại của lệnh.
- Access Modifier: Java cung cấp 1 số Access Modifier để thiết lập chỉ định truy cập cho các lớp, các biến, các phương thức và constructor. Có 4 mức độ truy cập là: Default (truy cập trong nội bộ package); Private (truy cập trong nội bộ lớp); Public (thành phần công khai, truy cập tự do từ bên ngoài); Protected (thành phần được bảo vệ, bị hạn chế truy cập từ bên ngoài).
- Non-Access Modifier: Static Modifier (tạo các phương thức lớp và các biến); Final Modifier (kết thúc sự thi hành của các lớp, các phương thức và các biến); Abstract Modifier (tạo các lớp và các phương thức trừu tượng); Synchronized Modifier và Volatile Modifier (sử dụng cho các Thread).

<a name="Non-AccessModifier"></a>

**30. Non-Access Modifier**
- Static Modifier: 

    Biến static: từ khóa static đc sd để tạo các biến sẽ tồn tại 1 cách độc lập trong bất kỳ instance được tạo cho lớp đó. Chỉ có 1 bản sao biến static tồn tại cho dù có nhiều instance của lớp. Các biến static cũng đc biết đến như là các biến class. Các biến local không thể được khai báo là static.

    Phương thức static: từ khóa static đc sd để tạo các phương thức sẽ tồn tại 1 cách độc lập trong bất kỳ instance được tạo cho lớp đó.

- Final Modifier:

    Biến final: 1 biến final có thể được khởi tạo 1 cách rõ ràng chỉ 1 lần. Một biến tham chiếu được khai báo final có thể không bao giờ được tái gán để tham chiếu tới 1 đối tượng khác. Tuy nhiên, dữ liệu trong đối tượng có thể bị thay đổi; vì thế trạng thái của đối tượng có thể bị thay đổi nhưng không phải là tham chiếu. Với các biến, final modifier thường đc sd với static để tạo 1 hằng số cho 1 biến class.

    Phương thức final: 1 phương thức final không thể bị overriding bởi bất kỳ lớp phụ nào. Final Modifier ngăn cản 1 phương thức bị sửa đổi trong 1 lớp phụ. Mục đích chính của phương thức final là nội dung của phương thức không nên bị thay đổi bởi bên ngoài.

    Lớp final: để ngăn cản lớp bị phân lớp thành lớp phụ. Nếu 1 lớp được đánh dấu là final, thì k có lớp nào có thể kế thừa bất kỳ đặc điểm nào từ lớp final đó.

- Abstract Modifier:

    Lớp abstract: nếu 1 lớp đc khai báo là abstract thì mục đích duy nhất cho lớp này là để kế thừa. Một lớp k thể vừa abstract vừa final. Một lớp abstract có thể chứa cả các phương thức abstract cũng như các phương thức thông thường.

    Phương thức abstract: là phương thức đc khai báo mà không có bất kỳ sự triển khai nào. Thân phương thức này đc cung cấp bởi lớp phụ. Các phương thức abstract có thể không bao giờ là final. Bất kỳ lớp nào mà kế thừa một lớp abstract phải triển khai tất cả phương thức abstract của lớp cha, trừ khi lớp phụ này cũng là một lớp abstract. Nếu một lớp chứa một hoặc nhiều phương thức abstract, thì lớp đó phải được khai báo là abstract. Một lớp abstract không cần chứa các phương thức abstract. Phương thức abstract kết thúc với một dấu chấm phảy. Ví dụ: public abstract sample();

- Synchronized Modifier: đc sd để chỉ rằng 1 phương thức có thể đc truy cập bởi chỉ 1 thread tại 1 thời điểm. Synchronized Modifier có thể đc áp dụng với bất kỳ 1 trong 4 mức độ Access Modifier nào.
- Transient Modifier: 1 biến instance đc đánh dấu là transient để chỉ ràng JVM bỏ qua biến cụ thể khi xếp thứ tự đối tượng đang chứa nó. Modifier này đc bao trong lệnh mà tạo biến đó, đứng trước lớp hoặc kiểu dữ liệu của biến đó.
- Volatile Modifier: đc sd để chỉ cho JVM biết 1 thread đang truy cập biến đó phải luôn luôn sát nhập bản sao biến private của riêng nó với bản sao master trong bộ nhớ. Truy cập 1 biến volatile đồng bộ tất cả bản sao của các biến trong bộ nhớ chính. Volatile chỉ có thể đc áp dụng tới các biến instance mà là kiểu đối tượng hoặc private. Một tham chiếu đối tượng Volatile có thể là null.

<a name="AccessModifier"></a>

**31. Access Modifier**
- Access Modifier xác định phạm vi có thể truy cập của thành viên dữ liệu, phương thức, constructor hoặc lớp.

<img src="https://2.pik.vn/201809baa6c8-f956-424e-9c51-37cc902d1587.jpg">

- Private Access Modifier: các phương thức, biến và constructor mà được khai báo private chỉ có thể đc truy cập trong chính lớp được khai báo đó; Lớp và interface không thể là private; Các biến được khai báo private có thể được truy cập bên ngoài lớp nếu phương thức public getter có mặt trong lớp đó; Sử dụng Private Access Modifier trong Java là cách chủ yếu để một đối tượng bao đóng chính nó và ẩn dữ liệu với bên ngoài.

    Quy tắc: nếu tạo bất cứ constructor nào là private, thì không thể tạo instance của lớp đó từ bên ngoài lớp.

- Default Access Modifier: không khai báo 1 cách rõ ràng 1 Access Modifier cho 1 lớp, trường, phương thức...Nói cách khác, nếu không sử dụng bất cứ Modifier nào, thì theo mặc định nó đc xem như là default. Default Modifier chỉ có thể truy cập bên trong package.

    VD: tạo 2 package là pack và mypack. Lớp pack có class A. Chúng ta truy cập lớp A từ bên ngoài package của nó. Khi lớp A không public, thì nó k thể được truy cập từ bên ngoài package.

- Protected Access Modifier: có thể truy cập bên trong package và bên ngoài package nhưng chỉ thông qua tính kế thừa. Protected Access Modifier có thể đc áp dụng trên thành viên dữ liệu nhưng không thể áp dụng trên lớp. Các biến, phương thức và constructor đc khai báo protected trong 1 lớp cha (superclass) chỉ đc truy cập bởi các lớp cha trong package khác hoặc bất kỳ lớp nào bên trong package đó của lớp đc protected.

    Protected Access Modifier không thể được áp dụng cho lớp và interface. Các phương thức và trường có thể được khai báo protected, tuy nhiên, các phương thức và trường trong một interface không thể được khai báo là protected.

    Chế độ protected cung cấp cho lớp phụ cơ hội để sử dụng phương thức hoặc biến helper, trong khi ngăn cản 1 lớp không liên quan từ việc cố gắng sử dụng nó.

<img src="https://2.pik.vn/201837c3c55d-c06e-4107-b732-8ca34e6eed86.jpg">

- Access Modifier với Overriding: Nếu đang ghi đè bất cứ phương thức nào, phương thức đc ghi đè (vd: đc khai báo trong lớp con) phải không nhiều giới hạn. Default Modifier nhiều giới hạn hơn Protected.

- Access Modifier và tính kế thừa trong Java: các quy tắc bắt buộc cho các phương thức đc kế thừa:

    Các phương thức đc khai báo public trong 1 lớp cha cũng phải public trong tất cả các lớp phụ.

    Các phương thức đc khai báo protected trong 1 lớp cha phải là protected hoặc public trong các lớp phụ, không thể là private.

    Các phương thức được khai báo mà không có điều khiển truy cập (không sd modifier nào) có thể đc khai báo private trong các lớp phụ.

    Các phương thức đc khai báo private không đc kế thừa, do đó không có quy tắc nào cho chúng.

<a name="Tinhbaodong"></a>

**32. Tính bao đóng**
- Tính bao đóng trong Java là 1 tiến trình đóng gói code và dữ liệu lại với nhau vào trong 1 đơn vị unit đơn.
- Chúng ta có thể tạo một lớp được bao đóng hoàn toàn trong Java bằng việc tạo tất cả thành viên dữ liệu của lớp là private. Bây giờ, chúng ta sử dụng phương thức setter và getter để thiết lập và lấy dữ liệu trong nó. Lớp Java Bean là ví dụ về một lớp được bao đóng hoàn toàn.
- Tính bao đóng là kỹ thuật tạo 1 trường của lớp private và cung cấp khả năng truy cập trường này qua các phương thức public. Nếu 1 trường đc khai báo private, nó không thể đc truy cập bởi bên ngoài lớp do đó có thể che dấu các trường có lớp này. Vì lý do này, tính bao đóng được ám chỉ như việc dấu dữ liệu (data hiding).
- Tính bao đóng có thể được mô tả như là một tấm bảo vệ code để tránh code và dữ liệu của bạn bị truy cập một cách ngẫu nhiên bởi các code khác bên ngoài class. Truy cập dữ liệu và code được điều khiển một cách chặt chẽ bởi một interface.
- Bởi cung cấp phương thức setter hoặc getter, bạn có thể làm cho lớp là read-only hoặc write-only. Nó cung cấp cho bạn sự điều khiển thông qua dữ liệu. Giả sử bạn muốn thiết lập giá trị của id là lớn hơn 100, thì bạn có thể viết biểu thức logic bên trong phương thức setter.
- Tất cả các lớp có thể có chế độ chỉ đọc hoặc chỉ ghi (chỉ có hàm getter hoặc setter).
- Một lớp có thể có toàn bộ điều khiển thông qua những gì được lưu giữ trong các trường của nó.
- Người sử dụng của class không biết cách các class lưu trữ dữ liệu. Một class có thể thay đổi kiểu dữ liệu của một trường và người dùng class không cần sự thay đổi trong code.

<a name="LopObjecttrongJava"></a>

**33. Lớp Object trong Java**
- Theo mặc định, lớp Object là lớp cha của tất cả các lớp trong Java; hay nó là lớp cao nhất của Java. Lớp Object là khá lợi ích nếu bạn muốn tham chiếu bất cứ đối tượng nào có kiểu mà bạn không biết. Chú ý rằng biến tham chiếu của lớp cha có thể tham chiếu tới đối tượng lớp con, và được gọi là Upcasting.
- VD: phương thức getObject() mà trả về 1 đối tượng nhưng nó có thể là bất cứ kiểu nào như Employee, Student,...Chúng ta có thể sd tham chiếu lớp Object để tham chiếu tới đối tượng đó: Object obj=getObject(); //kb đối tượng nào sẽ đc trả về từ phương thức này
- Lớp Object cung cấp 1 số hành vi chung cho tất cả các đối tượng, nhưn đối tượng có thể đc so sánh, có thể đc mô phỏng, thông báo,...

<img src="https://2.pik.vn/2018577829ff-bd9d-48c7-b853-8dbba9924805.jpg">

- Phương thức của lớp Object trong Java: 

<img src="https://2.pik.vn/20181c8568b6-25bd-489f-8c95-f29ae095ad0a.jpg">

<img src="https://2.pik.vn/20181c8568b6-25bd-489f-8c95-f29ae095ad0a.jpg">

- Lớp Object là một lớp mặc định của Java và là lớp đặc biệt. Tất cả các class khác trong Java phải kế thừa nó. Nhưng để cho gọn chúng ta hay ẩn đi, ví dụ không cần viết class Student extends Object, thực tế là vẫn mặc định extends.

<a name="Nhanbandoituong"></a>

**34. Nhân bản đối tượng**
- Nhân bản đối tượng là 1 cách để tạo 1 bản sao của đối tượng. Để thực hiện, sd phương thức clone(). Java.lang.Cloneable Interface phải được triển khai bởi lớp mà có đối tượng cần nhân bản chúng ta muốn tạo. Nếu bạn không triển khai Cloneable Interface, phương thức clone() sẽ tạo CloneNoSupportedException.
- Phương thức clone() được định nghĩa trong lớp Object. Cú pháp:

protected Object clone() throws CloneNotSupportedException

- Phương thức clone() tiết kiệm các tiến trình xử lý phụ để tạo bản nhân bản của 1 đối tượng. Nếu thực hiện nó bởi từ khóa new, điều này sẽ tốn nhiều tiến trình xử lý hơn, và đó là lý do vì sao sd nhân bản đối tượng.
- Phương thức clone() sao chép các giá trị của một đối tượng sang đối tượng khác. Do đó, chúng ta không cần viết code tường minh để sao chép giá trị từ đối tượng này sang đối tượng khác.
- Nếu bạn tạo đối tượng khác với từ khóa new và gán giá trị của đối tượng khác cho nó, thì điều này tốn nhiều tiến trình xử lý hơn trên đối tượng này. Do đó để tiết kiệm các tiến trình xử lý phụ, chúng ta nên sử dụng phương thức clone().

<a name="Mang(Array)"></a>

**35. Mảng (Array)**
- Mảng trong Java là 1 đối tượng chứa các phần tử có kiểu dữ liệu giống nhau. Nó là 1 cấu trúc dữ liệu, tại đó ta có thể lưu trữ các phần tử tương tự nhau. Chúng ta chỉ có thể lưu trữ 1 tập hợp cố định các phần tử trong 1 mảng trong Java.
- Mảng trong Java là dựa trên chỉ mục (index), phần tử đầu tiên của mảng được lưu trữ tạo chỉ mục 0.
- Lợi thế của mảng trong Java: tối ưu hóa code (có thể thu nhận và sắp xếp dữ liệu 1 cách dễ dàng); truy cập ngẫu nhiên (có thể lấy bất cứ dữ liệu nào tại bất cứ chỉ mục nào).
- Hạn chế của mảng trong Java: giới hạn kích cỡ (chỉ có thể lưu trữ kích cỡ cố định số phần tử trong mảng). Để xử lý vấn đề này, Collection Framework đc sd trong Java.
- Có 2 kiểu mảng trong Java: mảng 1 chiều, mảng đa chiều.
- Khai báo biến mảng trong Java: 

    kieu_du_lieu[] bien_tham_chieu_mang; //cách ưu tiên

    kieu_du_lieu bien_tham_chieu_mang[]; //k phải cách ưu tiên

- Tạo mảng trong Java: sử dụng toán tử new

    bien_tham_chieu_mang = new kieu_du_lieu[kich_co_mang];

    //tạo mảng bởi sd kiểu dữ liệu new kieu_du_lieu[kich_co_mang]; gán tham chiếu của mảng mới đc tạo tới biến bien_tham-chieu_mang

- Khai báo 1 biến mảng, tạo 1 mảng, gán tham chiếu của mảng tới biến có thể đc tổ hợp trong 1 lệnh:

    kieu_du_lieu[] bien_tham_chieu_mang = new kieu_du_lieu[kich_co_mang]

    kieu_du_lieu[] bien_tham_chieu_mang = {giatri0, ...gaitriN}

    vd: double[] a=new double[10];

- Các phần tử mảng được truy cập thông qua index – chỉ mục. Chỉ mục của mảng được tính toán từ 0 tới (N-1).
- Mảng 1 chiều trong Java: Khi xử lý các phần tử mảng, chúng ta thường sử dụng hoặc vòng lặp for hoặc vòng lặp foreach bởi vì tất cả phần tử trong một mảng là cùng kiểu và kích cỡ mảng đã biết.
- Truyền mảng tới phương thức trong Java: có thể truyền mảng tới phương thức để tái sử dụng cùng tính logic của phương thức đó trên bất cứ mảng nào.
- Mảng 2 chiều và đa chiều trong Java: dữ liêu đc lưu trữ trong hàng và cột dựa trên chỉ mục. Cú pháp:

    kieu_du_lieu[][] bien_tham_chieu_mang;

    kieu_du_lieu [][]bien_tham_chieu_mang;

    kieu_du_lieu bien_tham_chieu_mang[][];

    kieu_du_lieu []bien_tham_chieu_mang[];

    vd: int[][] arr=new int[3][3]; //3 hàng và 3 cột

- Tên lớp của mảng trong Java: trong java mảng là 1 đối tượng. Với đối tượng Array, 1 lớp ủy nhiệm đc tạo có tên có thể thu đc bởi phương thức getClass(), getName() trên đối tượng đó.   
- Có thể sao chép 1 mảng này sang mảng khác bởi phương thức arraycopy của lớp System. Cú pháp:

    public static void arraycopy(

        Object src, int srcPos, Object dest, int destPos, int length

    )

- Cộng 2 ma trận trong Java
- Lớp Array trong Java: lớp java.util.Arrays chứa nhiều phương thức static đa dạng để xếp thức tự và tìm kiếm các mảng, so sánh các mảng và điền các phần tử vào mảng.

<img src="https://2.pik.vn/20180dc70f09-8ab7-44c6-a6f0-1cee6d2d52fd.jpg">

<a name="LopWrapper"></a>

**36. Lớp Wrapper**
- Lớp Wrapper cung cấp kỹ thuật để chuyển đối kiểu gốc primitive thành đối tượng và từ đối tượng thành kiểu gốc. 
- Từ J2SE 5.0, đặc điểm autoboxing và unboxing sẽ tự động chuyển đổi primitive thành object (là autoboxing) và từ object thành primitive (là unboxing).
- Một trong 8 lớp của java.lang package là lớp Wrapper trong Java. Bảng dưới đây liệt kê danh sách 8 lớp Wrapper:

<img src="https://2.pik.vn/2018c4527416-87e4-46a7-8a1b-6ff9cca386cc.jpg">

<a name="GoiboigiatritrongJava"></a>

**37. Gọi bởi giá trị trong Java**
- Chỉ có gọi bởi giá trị trong Java, không có gọi bởi tham chiếu. Nếu chúng ta gọi 1 phương thức đang truyền 1 giá trị thì đó là gọi bởi giá trị. Các thay đổi được thực hiện trong phương thức được gọi, sẽ không bị tác động trong phương thức đang gọi.

<a name="TukhoaStictfptrongJava"></a>

**38. Từ khóa Strictfp trong Java**
- Từ khóa strictfp đảm bảo rằng bạn sẽ lấy cùng KQ trên mỗi nền tảng nếu bạn thực hiện các hoạt động trong giá trị số thực dấu chấm động. Phần sau dấu thập phân Precision có thể khác nhau giữa các nền tảng, và đó là lý do tại sao ngôn ngữ lập trình Java cung cấp từ khóa stricfp, để có thể nhận đc cùng kết quả trên mỗi nền tảng. Vì thế, bây giờ bạn sẽ có sự điều khiển tốt hơn với phép toán về số thực.
- Từ khóa strictfp có thể đc áp dụng trên các phương thức, các lớp, và interface.

    strictfp class A{} //strictfp áp dụng trên lớp

    strictfp interface M{}  // áp dụng trên interface

    class A{ strictfp void m() } // áp dụng trên phương thức

- Từ khóa strictfp không có thể đc áp dụng trên các phương thức trừu tượng, các biến hoặc các constructor

    class B{ strictfp abstract void m() };
    // sự tổ hợp không hợp lệ của các modifier

    class B{ strictfp int data=10; }
    // modifier strictfp không đc phép ở đây

    class B{ strictfp B() {}}
    //modifier strictfp không đc phép ở đây

<a name="Date&Time"></a>

**39. Date & Time**
- Java cung cấp lớp Date có sẵn trong java.util package, lớp này tóm lược ngày tháng và thời gian hiện tại.
- Lớp Date hỗ trợ hai constructor. Constructor đầu tiên khởi tạo đối tượng với ngày và thời gian hiện tại: Date()
- Constructor sau chấp nhận một tham số bằng số mili giây đã trôi qua từ nửa đêm ngày 1/1/1970: Date(long millisec)
- Một khi bạn có một đối tượng Date có sẵn, bạn có thể gọi bất kỳ phương thức hỗ trợ nào để thao tác với ngày tháng này:

<img src="https://2.pik.vn/2018795dc286-55b7-4630-b1ce-fcc9fe55f03f.jpg">

<img src="https://2.pik.vn/20182f2535b7-0866-4d5d-a81d-5d596b4e2c9f.jpg">

- Nhận Date & Time hiện tại: có thể sd một đối tượng Date đơn giản với phương thức toString() để in date và time hiện tại.
- So sánh Date trong Java: có 3 cách:

    Sử dụng getTime() để nhận số mili giây đã trôi qua từ nửa đêm 1/1/1970 cho cả hai đối tượng và sau đó so sánh hai giá trị này.

    Sử dụng các phương thức before(), after() và equals(). Bởi vì tháng thứ 12 ở trước tháng thứ 18, ví dụ, new Date(99, 2, 12).before(new Date(99, 2, 18)) trả về true.
    
    Sử dụng phương thức compareTo(), mà được định nghĩa bởi Comparable interface và được thi hành bởi Date.

- Định dạng Date bởi sd SimpleDateFormat: SimpleDateFormat là một lớp cố định (cụ thể) để định dạng và parse các date theo một phương thức nhạy cảm với locale. SimpleDateFormat cho phép bắt đầu chọn bất kỳ pattern đã được định nghĩa bởi người dùng cho định dạng date-time.
- Mã hóa định dạng SimpleDateFormat: Để xác định định dạng thời gian, sử dụng một chuỗi time mẫu. Trong pattern này, tất cả chữ cái ASCII được dự trữ (dành riêng) như là các ký tự pattern, mà được định nghĩa như sau:

<img src="https://2.pik.vn/20183267ee2f-9882-493c-8e61-56b6792318a4.jpg">

<img src="https://2.pik.vn/2018dc3f689c-218d-439c-bbf1-a4b6dcf5bf0e.jpg">

- Định dạng Date sd printf: Định dạng date và time có thể được thực hiện một cách đơn giản bởi sử dụng phương thức printf trong Java. Bạn sử dụng một định dạng hai chữ cái, bắt đầu với t và kết thúc với một trong các ký tự trong bảng dưới.
- Các ký tự biến đổi Date và Time:

<img src="https://2.pik.vn/2018320eb0e1-08e1-438a-992b-ca81d93aecd7.jpg">

<img src="https://2.pik.vn/20189a7dd3cf-c37b-4177-803a-d37e3dada613.jpg">

<img src="https://2.pik.vn/201808d4617f-61ab-4d42-b9ef-577a2a5d3d5c.jpg">

- Parse các String vào trong các Date trong Java: Lớp SimpleDateFormat có một số phương thức bổ sung, đáng kể nhất là parse(), mà parse một chuỗi theo định dạng được lưu giữ trong đối tượng SimpleDateFormat đã cho. 

<a name="RegularExpressiontrongJava"></a>

**40. Regular Expression trong Java**
- Java cung cấp java.util.regex package cho pattern so khớp với các Regular Expression. Các Regular Expression trong Java là tương tự với Ngôn ngữ lập trình Perl và rất dễ dàng để học.
- Một Regular Expression là một dãy liên tục của các ký tự đặc biệt mà giúp bạn so khớp hoặc tìm kiếm chuỗi hoặc tập hợp các chuỗi khác, sử dụng một cú pháp riêng biệt trong một pattern. Chúng có thể được sử dụng để tìm, chỉnh sửa và thao tác text và dữ liệu.
- Gói java.util.regex chủ yếu chứa 3 lớp sau:

    Lớp Pattern: Một đối tượng Pattern là một phép biểu diễn được biên dịch của một Regular Expression. Lớp Pattern không cung cấp một public constructor nào. Để tạo một pattern, bạn đầu tiên phải gọi một trong các phương thức biên dịch static chung của nó, mà sau đó sẽ trả về một đối tượng Pattern. Những phương thức này chấp nhận một Regular Expression như là tham số đầu tiên.

    Lớp Matcher: Một đối tượng Matcher là phương tiện mà thông dịch pattern và thực hiện so khớp các hoạt động với một chuỗi đầu vào. Như lớp Pattern, Matcher không định nghĩa một public constructor nào. Bạn nhận được một đối tượng Matcher bằng việc gọi phương thức matcher trên một đối tượng Pattern.

    PatternSyntaxException: Một đối tượng PatternSyntaxException là một exception (ngoại lệ) chưa được kiểm tra mà chỉ dẫn một lỗi cú pháp trong mẫu Regular Expression.

- Capture các Group trong Java: là một cách coi nhiều ký tự như là một đơn vị đơn. Chúng được tạo bằng việc xác định vị trí của các ký tự để được nhóm vào trong một tập hợp các dấu ngoặc đơn. Ví dụ, Regular Expression (dog) tạo một group đơn chứa các chữ cái là "d", "o" và "g". Để tìm bao nhiêu group có mặt trong Expression đó, bạn gọi phương thức groupCount trên một đối tượng Matcher. Phương thức groupCount trả về một int minh họa số Capturing Groups có mặt trong mẫu của đối tượng Matcher. Cũng có một group đặc biệt, là group 0, mà luôn luôn biểu diễn toàn bộ expression. Group này không được bao gồm trong kết quả của phương thức groupCount.

<a name="FilevaI/O"></a>

**41. File và I/O**
- Về cơ bản, dùng InputStream để đọc các file (file ảnh, phim....), còn dùng FileReader sẽ tốt hơn khi đọc các đoạn text (file txt...). Nên nhớ file docx không phải là file binary mà là file nhị phân.
- Gói I/O chứa gần như tất cả các lớp cần để thực hiện input và output trong Java.
- Một stream có thể đc ĐN như 1 dãy liên tục dữ liệu, Input Stream đc sd để đọc dữ liệu từ 1 nguồn, Output Stream đc sd để ghi dữ liệu tới 1 đích đến.
- Byte Stream trong Java đc sd để thực hiện input và output của các byte (8 bit). Hai lớp thường đc sd nhiều nhất là FileInputStream và FileOutPutStream.
- Standart Stream: tất cả các ngôn ngữ lập trình cung cấp sự hỗ trợ cho I/O chuẩn, tại đây chương trình của người sd có thể nhận đầu vào từ 1 bàn phím và sau đó tạo KQ trên màn hình mt.

    Đầu vào chuẩn (Standard Input): đc sd để truyền DL tới chương trình của người sd và thường thì 1 bàn phím đc sd như là đầu vào chuẩn và đc biểu diễn như System.in

    Đầu ra chuẩn (Standard Output): sd để hiển thị KQ đầu ra từ chương trình, thường thì 1 màn hình máy tính đc sd như đầu ra chuẩn và đc biểu diễn như System.out

    Lỗi chuẩn(Standard Error): đc sd để hiển thị các lỗi trong chương trình của ng dùng, thường thì 1 màn hình máy tính đc sd như lỗi chuẩn và đc biểu diễn như System.err

- Đọc và ghi file trong Java: Input Stream đc sd để đọc dữ liệu từ 1 nguồn, Output Stream được sd để ghi dữ liệu tới đích.
Dưới đây là 1 cấu trúc có thứ tự của các lớp dderr xử lý các luồng Input và Output:

    <img src="https://2.pik.vn/2018f3f98718-668b-47f5-963e-c7f45390bf08.jpg">

- FileInputStream: luồng này đc sd để đọc dữ liệu từ các file. Các đối tượng có thể đc tại bởi sử dụng từ khóa new và có 1 số kiểu constructor có sẵn.

    InputSream f=new FileInputStream("C:/java/hello); //constructor nhận tên file như là 1 chuỗi để tạo đối tượng Input Stream để đọc file.


    Constructor nhận 1 đối tượng File để tạo 1 đối tượng Input Stream để đọc file. Đầu tiên tạo 1 đối tượng file bởi sd phương thức File() như sau:

    File f=new File("C:/java/hello");

    InputStream f=new FileInputStream(f);

    Khi có đối tượng InputStream, có 1 danh sách các phương thức có thể đc sd để đọc stream hoặc để thực hiện hoạt động nào khác trên stream này:

    <img src="https://2.pik.vn/20184d98e8b1-9306-4423-b3a6-679a97eb0080.jpg">

- FileOutputStream: đc sd để tạo file và ghi dữ liệu vào trong nó. Luồng này sẽ tạo 1 file, nếu nó chưa tồn tại, trước khi mở nó để ghi output. Dưới đây là 2 constructor có thể đc sd để tạo 1 đối tượng FileOutputStream trong Java:

    Constructor sau nhận một tên file như là một chuỗi để tạo một đối tượng output stream để ghi file:

    OutputStream f=new FileOutputStream("C:/java/hello");

    Constructor sau nhận một đối tượng file để tạo một đối tượng output stream để ghi file:

    File f=new File("C:java/hello");

    OutputStream f=new FileOutputStream(f);

    <img src="https://2.pik.vn/201807d14932-dc50-4e5c-8f3a-3cc80d47b24e.jpg">

- Thư mục trong Java: Một thư mục là File mà có thể giữ một danh sách các file và thư mục khác. Sd đối tượng file để tạo các thư mục, liệt kê các file có sẵn trong 1 thư mục.
- Tạo thư mục: 

    Phương thức mkdir() tạo 1 thư mục, trả về true nếu thành công, false nếu thất bại.

    Phương thức mkdirs() tạo cả 1 thư mục và tất cả các thư mục cha of nó.

- Liệt kê thư mục trong Java: có thẻ sd phương thức list() đc cung cấp bởi đối tượng File để liệt kê tất cả các file và thư mục có sẵn trong 1 thư mục.

<a name="ByteArrayInputStream"></a>

**42. ByteArrayInputStream**
- Lớp ByteArrayInputStream cho phép 1 bộ đệm (buffer) trong bộ nhớ để được sử dụng như là 1 InputStream. Nguồn Input này là 1 mảng byte. Có những mẫu constructor sau để tạo đối tượng ByteArrayInputStream. 

    Nhận 1 mảng byte như là tham số: 
    
ByteArrayInputStream bArray=new ByteArrayInputStream(byte [] a)

    Form khác nhận 1 mảng các byte, và hai int, với off là byte đầu tiên để đc đọc và len là số byte để đc đọc:

ByteArrayInputStream bArray=new ByteArrayInputStream(byte [] a, int off, int len)
- Khi có đối tượng ByteArrayInputStream thi có 1 số phương thức có thể đc sd để đọc stream hoặc để thực hiện các hoạt động khác trên stream đó.

<img src="https://2.pik.vn/20187a5e08a5-f3ae-42b7-8898-947e0703001f.jpg">

