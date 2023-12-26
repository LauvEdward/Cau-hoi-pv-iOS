# Câu hỏi phỏng vấn iOS

### Cơ bản

    1. Hướng đối tượng có bao nhiêu tính chất? Các tính chất đó là gì?
    Hướng đối tượng có 4 tính chất chính:
    Tính đóng gói (Encapsulation): Bảo vệ dữ liệu bên trong một đối tượng và chỉ cho phép truy cập thông qua các phương thức công cộng.
    Tính đa hình (Polymorphism): Một phương thức có thể thực hiện nhiều hành động khác nhau tùy thuộc vào đối tượng gọi phương thức đó.
    Tính trừu tượng (Abstraction): Tạo ra các lớp và đối tượng trừu tượng để mô tả các đối tượng trong thế giới thực.
    Tính kế thừa (Inheritance): Sử dụng lại các thuộc tính và phương thức của một lớp trong lớp mới mà không cần viết lại.
    2. Đối tượng là gì?
    Đối tượng là một thực thể có thể được định nghĩa bằng cách mô tả các thuộc tính (dữ liệu) và phương thức (hành vi) mà đối tượng đó có.
    3. Class là gì?
    Một class là một khuôn mẫu để tạo ra các đối tượng. Nó định nghĩa cách mà các thuộc tính và phương thức được tạo ra trong các đối tượng.
    4. Ví dụ về đa hình trong hướng đối tượng?
    Ví dụ về đa hình có thể là sử dụng cùng một phương thức draw() trên các lớp con khác nhau để vẽ các hình đồng thời như hình vuông, hình tròn, ...
    5. CRUD là gì?
    CRUD là một viết tắt trong lập trình và quản trị cơ sở dữ liệu, nó đại diện cho:
    Create (Tạo): Tạo mới một bản ghi hoặc đối tượng.
    Read (Đọc): Đọc dữ liệu từ cơ sở dữ liệu hoặc từ nguồn dữ liệu khác.
    Update (Cập nhật): Cập nhật thông tin của một bản ghi hoặc đối tượng đã tồn tại.
    Delete (Xóa): Xóa bản ghi hoặc đối tượng khỏi cơ sở dữ liệu.

### Junior & middle

    1.  Kế thừa trong Switf là đơn hay đa thừa kế? Muốn đa thừa kế thì phải như thế nào?
    swift là đơn kế thừa, không thể kế thừa nhiều class với nhau được, thay oop bằng pop sẽ cho kế thừa nhiều protocol
    2.  Hướng đối tượng trong Swift có tính trừu tượng hay không?
    không, tính trừu tượng khai báo các phương thức và thuộc tính chứ k định nghĩa nó ra. swift không hỗ trợ tính trừu tượng trực tiếp, nhưng thay vào đó chúng ta dùng protocol để triển khai chúng. 
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
    Trong iOS, bộ nhớ được quản lý tự động thông qua ARC (Automatic Reference Counting). ARC tự động theo dõi số lượng tham chiếu đối với đối tượng và giải phóng bộ nhớ khi không còn tham chiếu nào đến đối tượng đó.
    6.  Property Wrappers trong Swift là gì? Liệt kê các loại Wrapper bạn hay sử dụng?
    Property Wrappers là một tính năng của Swift giúp đơn giản hóa việc quản lý các thuộc tính. Các loại Property Wrappers bao gồm @Published, @State, @Binding, @ObservedObject, @EnvironmentObject...
    7.  ARC và non-ARC là gì ( Automatic Reference Counting )?
    ARC (Automatic Reference Counting) là mô hình quản lý bộ nhớ tự động của Swift, giúp tự động giải phóng bộ nhớ khi không còn đối tượng nào tham chiếu đến nó.Non-ARC (non-Automatic Reference Counting) yêu cầu lập trình viên tự quản lý bộ nhớ bằng cách thêm và loại bỏ tham chiếu thủ công.
    8.  Strong và weak là gì?
    strong: Tăng tham chiếu lên đối tượng, ngăn chặn việc giải phóng bộ nhớ cho đến khi không còn tham chiếu nào.weak: Giảm tham chiếu lên đối tượng, cho phép giải phóng bộ nhớ khi không còn tham chiếu strong nào.
    9.  Trình bày iOS Application Lifecycle?
    Lifecycle của iOS bao gồm các sự kiện như applicationDidFinishLaunching, applicationWillResignActive, applicationDidEnterBackground, applicationWillEnterForeground, và applicationDidBecomeActive.
    10.  Sự khác nhau của AppDelegate & SenceDelegate?
    AppDelegate: Quản lý toàn bộ ứng dụng và chứa các phương thức lifecycle. SceneDelegate: Quản lý các scene (cửa sổ) trong ứng dụng khi chia sẻ trên các thiết bị iPad và khi sử dụng đa nhiệm.
    11.  Trình bày về mô mình MVC & MVVM trong iOS & Swift?
    MVC (Model-View-Controller): Mô hình phân tách ứng dụng thành ba thành phần chính: Model (dữ liệu), View (giao diện), và Controller (logic xử lý). MVVM (Model-View-ViewModel): Mở rộng MVC bằng cách thêm ViewModel, giúp tách biệt logic xử lý và giao diện.
    12.  Sự kết nối giữa các thành phần trong MVC & MVVM.
    MVC: Controller quản lý sự tương tác giữa Model và View. MVVM: ViewModel giữ dữ liệu và logic xử lý, giao tiếp với View thông qua binding.
    13.  Model được hiểu là như thế nào?
    Model là thành phần chịu trách nhiệm lưu trữ dữ liệu và cung cấp các phương thức để truy xuất và cập nhật dữ liệu.
    14.  Trình bày các ưu điểm mà MVVM tối ưu hơn MVC? Trong đó, điểm nào là quan trọng nhất?
    Tách biệt logic xử lý và giao diện. Dễ kiểm thử và tái sử dụng. Hỗ trợ binding giữa ViewModel và View.
    15.  Định nghĩa các mẫu Design Pattern?
    Design Pattern là các mô hình giải quyết các vấn đề lập trình phổ biến. Ví dụ: Singleton, Observer, Factory, Delegate, Strategy, Command, v.v.
    16.  Liệt kê các mẫu Design Pattern mà bạn biết?
    Singleton, Observer, Factory, Delegate, Strategy, Command, Builder, MVC, MVVM, Prototype, Adapter, Decorator, State, Composite, Proxy, và nhiều mẫu khác.
    17.  Thế nào là singleton? Có bao nhiều cách tạo một singleton?
    Singleton là một mẫu thiết kế cho phép chỉ có một đối tượng duy nhất của một lớp tồn tại. Có nhiều cách để tạo singleton, bao gồm cách thông thường, sử dụng dispatch_once, và sử dụng property.
    18.  Custom View là gì? Các cách custom view mà bạn sử dụng?
    Custom View là việc tạo ra một lớp View tùy chỉnh để đáp ứng nhu cầu cụ thể của ứng dụng. Cách custom view bao gồm việc sử dụng Interface Builder, vẽ tự động (drawRect), và việc quản lý layout và constraints.
    19.  Thế nào re-usable trong iOS?
    Re-usable là khả năng sử dụng lại thành phần (View, Controller, Model) trong nhiều phần của ứng dụng hoặc trong các dự án khác nhau.
    20.  Retain cycle là gì? Cách để tránh chúng?
    Retain cycle là một vòng lặp tham chiếu giữa các đối tượng, dẫn đến rò rỉ bộ nhớ. Để tránh retain cycle, sử dụng weak hoặc unowned khi tham chiếu giữa các đối tượng.
    21.  Trình bày về CoreData? Các thành phần của nó?
    CoreData là một framework cho phép lưu trữ và quản lý dữ liệu trong ứng dụng iOS và macOS. Các thành phần bao gồm Managed Object Model, Persistent Store Coordinator, Managed Object Context, và các lớp Entit
    22.  Realm là gì?
    Realm là một cơ sở dữ liệu nhúng, nhẹ, dễ sử dụng cho iOS và Android.
    23.  Các đối tượng nào dùng trong việc điều hướng trong iOS & Swift?
    UINavigationController, UITabBarController, UISplitViewController, và UIViewController.
    24.  Storyboard là gì? Cách điều hướng trong Storyboard?
    Storyboard là một file XML chứa giao diện người dùng của ứng dụng. Điều hướng trong Storyboard được thực hiện bằng cách sử dụng Segues và các Identifier.
    25.  Decoding & Encoding trong Swift?
    Decoding là quá trình chuyển đổi dữ liệu JSON thành các đối tượng Swift. Encoding là quá trình chuyển đổi các đối tượng Swift thành dữ liệu JSON.
    26.  Trình bày cách tương tác với API & cách parse JSON?
    Tương tác với API sử dụng URLSession hoặc thư viện như Alamofire. Parse JSON sử dụng JSONDecoder hoặc JSONSerialization.
    27.  Trình bày về các loại Map được dùng trong iOS?
    MapKit là framework của Apple cho bản đồ. Google Maps API cũng được sử dụng.
    28.  Sự khác nhau giữa Local & Remote Push notification?
    Local Push Notification được tạo và gửi từ ứng dụng. Remote Push Notification được gửi từ máy chủ.
    29.  Các công cụ quản lý thư viện, như là Cocoapod, Carthage, Swift Package Manager … bạn đã sử dụng những loại nào? Ưu điểm của chúng?
    CocoaPods: Quản lý thư viện và dependencies, dễ sử dụng.
    Carthage: Quản lý dependencies, cài đặt bằng mã nguồn.
    Swift Package Manager: Quản lý dependencies, được tích hợp với Swift.

Khi ứng viên không trả lời hết được các câu hỏi, thì một số câu hỏi sau để cứu vớt ứng viên.

    1.  Autolayout là gì? Trong đó các yếu tố nào ảnh hưởng chính?
    Autolayout là một cơ chế trong iOS để tạo ra giao diện linh hoạt trên nhiều kích thước màn hình. Các yếu tố ảnh hưởng chính bao gồm các ràng buộc (constraints) như chiều cao, chiều rộng, vị trí, và quy tắc ưu tiên giữa các phần tử giao diện.
    2.  Kéo thả Autolayout cho UIScrollview như thế nào?
    Để sử dụng Autolayout cho UIScrollView, bạn cần đảm bảo rằng nội dung bên trong nó (content view) có kích thước rộng và cao được ràng buộc với UIScrollView và các cạnh của nó. Ngoài ra, thiết lập ràng buộc của UIScrollView với kích thước màn hình cũng là quan trọng.
    3.  Trình bày các loại Property trong Swift?
    Có hai loại Property trong Swift: Stored Property (lưu trữ giá trị) và Computed Property (tính toán giá trị). Cả hai đều có thể là var hoặc let.
    4.  Có bao nhiều cách để thêm một function cho một class có sẵn?
    Có hai cách chính: sử dụng extension để mở rộng chức năng của một lớp hoặc sử dụng subclassing để tạo ra một lớp con mới và thêm chức năng vào đó.
    5.  Protocol là gì?
    Protocol là một phần của Swift giúp định nghĩa một bộ quy tắc (yêu cầu) mà các lớp hoặc struct có thể tuân thủ. Nó định nghĩa các phương thức, thuộc tính và các nhiệm vụ liên quan mà một kiểu dữ liệu phải thực hiện.
    6.  Phân biệt sự khác nhau giữa delegate & datasource?
    Delegate: Thường được sử dụng để thông báo sự kiện hoặc truyền dữ liệu từ một đối tượng tới một đối tượng khác. Ví dụ: UITableViewDelegate. Datasource: Thường được sử dụng để cung cấp dữ liệu cho một đối tượng. Ví dụ: UITableViewDataSource.
    7.  Closure là gì?
    Closure là một khối mã Swift độc lập có thể được truyền và sử dụng trong mã của bạn. Nó giống như một hàm không tên và có thể được chuyển làm tham số hoặc lưu trữ trong biến.
    8.  Grand Central Dispatch là gì?
    Grand Central Dispatch (GCD) là một API trong Swift giúp quản lý và thực hiện các công việc đồng thời (concurrent) một cách dễ dàng. Nó giúp tận dụng tốt tài nguyên hệ thống.
    9.  Các cách lưu trữ dữ liệu tại local?
    Có nhiều cách để lưu trữ dữ liệu tại local trong iOS, bao gồm UserDefaults, File System, Core Data, SQLite, và Realm.
    10.  Optional là gì?
    Optional là một kiểu dữ liệu trong Swift giúp xử lý giá trị có thể nil. Kiểu Optional được ký hiệu bằng dấu chấm than (?).


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

Và nếu như ứng viên vào vị trí senior không như bạn kỳ vọng, thì hãy thử hack não với các lý thuyết thuật toán cơ bản.

    1.  Trình bày thuật toán tìm kiếm nhị phân? (tập trung để ý xem người được hỏi có chú ý điều kiện ban đầu hay không)
    2.  Thuật toán tìm lớp trưởng?
    3.  Bài toán tìm chuỗi con trong chuỗi mẹ?
    4.  Theo tư duy của máy tính thì 1 + 2 * 3 bằng bao nhiêu?
    5.  Thuật toán tìm đường đi ngắn nhất?
        // Định nghĩa một đỉnh trong đồ thị
        struct Vertex {
            let name: String
            var edges: [Edge]
        }
        
        // Định nghĩa một cạnh và trọng số của nó
        struct Edge {
            let neighbor: Vertex
            let weight: Int
        }
        
        // Định nghĩa đồ thị với một mảng các đỉnh
        struct Graph {
            let vertices: [Vertex]
        
            // Hàm tìm đường đi ngắn nhất từ một đỉnh đến tất cả các đỉnh khác
            func dijkstra(startingVertex: Vertex) -> [String: Int] {
                var distances: [String: Int] = [:]
        
                for vertex in vertices {
                    distances[vertex.name] = Int.max
                }
        
                distances[startingVertex.name] = 0
        
                var unvisitedVertices = Set(vertices)
        
                while !unvisitedVertices.isEmpty {
                    let currentVertex = unvisitedVertices.min { distances[$0.name] ?? Int.max < distances[$1.name] ?? Int.max }!
        
                    unvisitedVertices.remove(currentVertex)
        
                    for edge in currentVertex.edges {
                        let potentialDistance = distances[currentVertex.name]! + edge.weight
        
                        if potentialDistance < distances[edge.neighbor.name]! {
                            distances[edge.neighbor.name] = potentialDistance
                        }
                    }
                }
        
                return distances
            }
        }
    
        // Ví dụ sử dụng thuật toán Dijkstra
        let vertexA = Vertex(name: "A", edges: [])
        let vertexB = Vertex(name: "B", edges: [])
        let vertexC = Vertex(name: "C", edges: [])
        let vertexD = Vertex(name: "D", edges: [])
        
        vertexA.edges = [Edge(neighbor: vertexB, weight: 1), Edge(neighbor: vertexC, weight: 3)]
        vertexB.edges = [Edge(neighbor: vertexA, weight: 1), Edge(neighbor: vertexC, weight: 1), Edge(neighbor: vertexD, weight: 4)]
        vertexC.edges = [Edge(neighbor: vertexA, weight: 3), Edge(neighbor: vertexB, weight: 1), Edge(neighbor: vertexD, weight: 1)]
        vertexD.edges = [Edge(neighbor: vertexB, weight: 4), Edge(neighbor: vertexC, weight: 1)]
        
        let graph = Graph(vertices: [vertexA, vertexB, vertexC, vertexD])
        let distancesFromA = graph.dijkstra(startingVertex: vertexA)
        
        print("Distances from A:", distancesFromA)
    6.  print(true && false || true || false && false) sẽ cho kết quả là gì? Giải thích nó?
    Kết quả: true
    Giải thích: Trong biểu thức logic, && có độ ưu tiên cao hơn ||, nên biểu thức được đánh giá từ trái sang phải. true && false là false, sau đó false || true là true, và cuối cùng true || false && false cũng là true.

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
