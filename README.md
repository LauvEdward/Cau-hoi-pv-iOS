# Câu hỏi phỏng vấn iOS

### Cơ bản

    1.  Hướng đối tượng có bao nhiêu tính chất? Các tính chất đó là gì?
    có 4 tính chất của hướng đối tượng:
    - tính đóng gói
    - tính đa hình
    - tính trừu tượng
    - tính kế thừa
    2.  Đối tượng là gì?
    là một object ngoài đời thực được mô với các hành vi và thuộc tính
    3.  Class là gì?
    là một lớp dùng để mô tả các đối tượng ngoài đời thực vào lập trình: với hành vi là các menthod, thuộc tính là properties.
    4.  Cho các ví dụ thực tế về đa hình trong hướng đối tượng?
    ví dụ một contructor init trong swift thì đa hình nó sẽ là có cùng một tên init nhưng lại có nhiều cách init khác nhau, tuỳ thuộc vào định nghĩa của     lập trình viên
    5.  CRUD là gì?
    6.  Trình bày về hiểu biết của em cho các hệ quản trị cở sở dữ liệu?
    7.  …

### Junior & middle

    1.  Kế thừa trong Switf là đơn hay đa thừa kế? Muốn đa thừa kế thì phải như thế nào?
    swift là đơn kế thừa, không thể kế thừa nhiều class với nhau được, thay oop bằng pop sẽ cho kế thừa nhiều protocol
    2.  Hướng đối tượng trong Swift có tính trừu tượng hay không?
    không, tính trừu tượng khai báo các phương thức và thuộc tính chứ k định nghĩa nó ra. swift không hỗ trợ tính trừu tượng trực tiếp, nhưng thay vào       đó chúng ta dùng protocol để triển khai chúng. 
    3.  Class & struct khác nhau như thế nào?
    - tính kế thừa
    - type: value type, reference type
    - hiệu suất truy suất: struct > class
    4.  Có bao nhiêu mức Access Control trong Swift? Hãy liệt kê chúng theo thứ tự giảm dần?
    có 5 mức: private, fileprivate, internal, public, open
        import MyModule
        func main() {
            // Khởi tạo các lớp và gọi các phương thức
            let privateInstance = PrivateClass()  // Lỗi: privateClass không thể truy cập từ module khác
            let fileprivateInstance = FilePrivateClass()  // Lỗi: fileprivateClass không thể truy cập từ module khác
            let internalInstance = InternalClass()
            let publicInstance = PublicClass()
            let openInstance = OpenClass()
            
            internalInstance.internalMethod()
            publicInstance.publicMethod()
            openInstance.openMethod()
        }
    
    5.  Quản lý bộ nhớ trong iOS như thế nào?
    
    6.  Property Wrappers trong Swift là gì? Liệt kê các loại Wrapper bạn hay sử dụng?
    7.  ARC và non-ARC là gì ( Automatic Reference Counting )?
    8.  Strong và weak là gì?
    
    9.  Trình bày iOS Application Lifecycle?
    10.  Sự khác nhau của AppDelegate & SenceDelegate?
    11.  Trình bày về mô mình MVC & MVVM trong iOS & Swift?
    12.  Sự kết nối giữa các thành phần trong MVC & MVVM.
    13.  Model được hiểu là như thế nào?
    14.  Trình bày các ưu điểm mà MVVM tối ưu hơn MVC? Trong đó, điểm nào là quan trọng nhất?
    15.  Định nghĩa các mẫu Design Pattern?
    16.  Liệt kê các mẫu Design Pattern mà bạn biết?
    17.  Thế nào là singleton? Có bao nhiều cách tạo một singleton?
    18.  Custom View là gì? Các cách custom view mà bạn sử dụng?
    19.  Thế nào re-usable trong iOS?
    20.  Retain cycle là gì? Cách để tránh chúng?
    21.  Trình bày về CoreData? Các thành phần của nó?
    22.  Realm là gì?
    23.  Các đối tượng nào dùng trong việc điều hướng trong iOS & Swift?
    24.  Storyboard là gì? Cách điều hướng trong Storyboard?
    25.  Decoding & Encoding trong Swift?
    26.  Trình bày cách tương tác với API & cách parse JSON?
    27.  Trình bày về các loại Map được dùng trong iOS?
    28.  Sự khác nhau giữa Local & Remote Push notification?
    29.  Các công cụ quản lý thư viện, như là Cocoapod, Carthage, Swift Package Manager … bạn đã sử dụng những loại nào? Ưu điểm của chúng?
    30.  …

Khi ứng viên không trả lời hết được các câu hỏi, thì một số câu hỏi sau để cứu vớt ứng viên.

    1.  Autolayout là gì? Trong đó các yếu tố nào ảnh hưởng chính?
    2.  Kéo thả Autolayout cho UIScrollview như thế nào?
    3.  Trình bày các loại Property trong Swift?
    4.  Có bao nhiều cách để thêm một function cho một class có sẵn?
    5.  Protocol là gì?
    6.  Phân biệt sự khác nhau giữa delegate & datasource?
    7.  Closure là gì?
    8.  Grand Central Dispatch là gì?
    9.  Các cách lưu trữ dữ liệu tại local?
    10.  Optional là gì?
    11.  …

### Senior

    1.  Đặc điểm chung của lập trình mobile là gì? Yếu tố nào quyết định tới ứng dụng mobile?
    2.  Liệt kê các cách passing data trong iOS & Swift?
    3.  Vì sao Swift được gọi là ngôn ngữ an toàn?
    4.  Generic là gì? Trình bày các loại cơ bản Generic trong Swift?
    5.  Trình bày khái niệm về Higher Order Function?
    6.  Định nghĩa Functional Programming?
    7.  Thành phần nào cấu tạo nên Functional Programming?
    8.  Bạn đã có kinh nghiệm về submit ứng dụng lên store chưa? Thời gian review của Apple trung bình là bao lâu?
    9.  Trình bày hiểu biết của bạn về các CI/CD đối với iOS?
    10.  Các vấn đề Fastlane?
    11.  Các ngôn ngữ hay framework Reactive Programming mà bạn đã dùng?
    12.  Thế nào là KVO?
    13.  Trình bày về các cách mà bạn đã debug trong iOS & Swift?
    14.  Trình bày các mô hình anh chị em của MVC?
    15.  Thế nào là callback & request được dùng trong các mô hình phổ biến hiện nay?
    16.  Trình bày về các mô hình nâng cao, như: MVVM-C, Viper …
    17.  Trình bày hiểu biết về Combine.
    18.  Bạn biết gì về SwiftUI?
    19.  Trình bày về SwiftUI App Life Cycle (mới)?
    20.  Sự khác nhau giữa UIKit AppDelegate và SwiftUI App?
    21.  Trình bày về Concurrency (mới & cũ) trong iOS & Swift?
    22.  Concurrent vs Serial DispatchQueue trong iOS & Swift?
    23.  Liệt kê các độ ưu tiên của một queue trong GCD?
    24.  Trình bày về các kĩ thuật testing trong iOS?
    25.  Phân biệt giữa Unit Test & UI Test?
    26.  Code coverage là gì? Chúng ta có bao nhiều level để thực hiện Testing và cho Code coverage?
    27.  Trình bày cách cách bạn giải quyết nhiều task bất đồng bộ cùng lúc với nhau?
    28.  Trình bày về async/await trong Swift?
    29.  AR & VR trong hệ sinh thái Apple?
    30.  Có bao nhiều cách định nghĩa hệ tọa độ trong ARKit?
    31.  Cách bạn Capture Videos và custom Camera?
    32.  …

Và nếu như ứng viên vào vị trí senior không như bạn kỳ vọng, thì hãy thử hack não với các lý thuyết thuật toán cơ bản.

    1.  Trình bày thuật toán tìm kiếm nhị phân? (tập trung để ý xem người được hỏi có chú ý điều kiện ban đầu hay không)
    2.  Thuật toán tìm lớp trưởng?
    3.  Bài toán tìm chuỗi con trong chuỗi mẹ?
    4.  Theo tư duy của máy tính thì 1 + 2 * 3 bằng bao nhiêu?
    5.  Thuật toán tìm đường đi ngắn nhất?
    6.  print(true && false || true || false && false) sẽ cho kết quả là gì? Giải thích nó?
    7.  …

### Câu hỏi để chém ứng viên

Khi bạn quá mệt mỏi với ứng viên. Bạn muốn kết thúc buổi phỏng vấn sớm, thì sẽ dùng một số câu hỏi đánh đố người phỏng vấn như sau:

    1.  View là gì?
    2.  Class là gì?
    3.  Object là gì?
    4.  Model là gì?
    5.  Function là gì?
    6.  Lập trình là gì?
    7.  Frame là gì?
    8.  Có bao nhiều thuật toán sắp xếp?
    9.  Programming paradigm là gì?

## Câu hỏi về thái độ và tư duy

    1.  3~5 năm tới bạn mong muốn làm gì? Em chuẩn bị gì cho nó?
    2.  Bạn có Github hay không?
    3.  Bạn có thích chia sẻ mã nguồn của các dự án?
    4.  Mã nguồn của một dự án trong công ty là của ai?
    5.  Bạn có thích lưu trữ mã nguồn các dự án mà bạn tham gia hay không?
    6.  Làm việc nhóm là như thế nào?
    7.  Thế nào là code xong 1 task?
    8.  Bạn sẽ viết test trước hay code trước?
    9.  Bạn cảm thấy như thế nào khi task của bạn luôn bị khách hàng thay đổi yêu cầu?
    10.  Giữ dev và tester khi có mâu thuẩn thì ai là người đúng? (hỏi ngu để xem ứng viên phản ứng ra sao)
    11.  1 Dev có khi nào lương cao hơn 1 PM hay không?
    12.  …

## Câu hỏi về Leader hay các vị trí cao hơn

    1.  Giao tiếp trong dự án là như thế nào?
    2.  Vai trò của Leader trong team là gì?
    3.  Cảm nhận về vai trò PM trong dự án?
    4.  Thế nào là một Senior developer?
    5.  Trình bày hiểu biết về các hệ thống API, Webserive … ?
    6.  Các mô hình quản lý dự án?
    7.  Scrum có làm dự án thành công hay không?
    8.  Mình muốn biết cách bạn triển khai một feature (với đầy đủ coding + testing) cho team của bạn là như thế nào?
    9.  Theo bạn thì coding guidelines cho một nền tảng thì sẽ bao gồm những gì trong đó? Và có thật sự phải tuân thủ coding guidelines không, hãy cho mình biết suy nghĩ của bạn về nó?
    10.  Công việc của techlead theo bạn sẽ làm những việc gì trong team Bạn có force team theo cách của bạn không?
    11.  Dependency Injection trong Swift
    12.  Bạn hiểu như thế nào về Race Conditions. Và trình bày các cách triệt tiêu Race Conditions trong lập trình.
    13.  Bạn trình bày về App Thining trong iOS là như thế nào. (hỏi cái này trước, đúng ý mới tiếp phần sau) Trong đó, cách nào bạn xem là tối ưu nhất cho việc giảm size ứng dụng?
    14.  Trình bày sự khác nhau cơ bản của Declarative vs Imperative Programming. Theo bạn thì tương lại lập trình sẽ theo phòng cách nào và tại sao?
    15.  Bạn có biết WWDC không? Hãy trình bày điều mà bạn hứng thú nhất trong WWDC mới nhất mà bạn đã xem?
    16.  Theo bạn thì tương lai của Swift & iOS như thế nào?
    17.  …
