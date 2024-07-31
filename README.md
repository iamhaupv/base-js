DOM (Document Object Model) mô hình các đối tượng trong tài liệu HTML
- Thông qua DOM ta có thể truy xuất đến các thẻ HTML một cách dễ dàng
- DOM gồm 3 thành phần: Element, Attribute, Text
<a href='#'>Trang Facebook</a>
Trong đó: 
a: element, href: attribute, text: Trang Facebook
Nhiệm vụ của DOM 
- Truy xuất đến các thẻ HTML
- Thay đổi các thuộc tính của HTML
- Thay đổi CSS
- Tạo, xóa, thêm các thẻ HTML
Các loại DOM:
- DOM document: lưu trữ toàn bộ các thành phần trong tài liệu của web
- DOM element: truy xuất tới các thẻ HTML thông qua thuộc tính id, name, class, của thẻ HTML
- DOM HTML: thay đổi giá trị nội dung và giá trị thuộc tính của thẻ HTML
- DOM CSS: thay đổi định dạng CSS
- DOM Event: gắn các sự kiện nhưn onClick(), onBlur() và thẻ HTML
- DOM Listerner: lắng nghe sự kiện tác động lên thẻ HTML
- DOM navigate: dùng để quản lý, thao tác các thẻ HTML, thể hiện mối quan hệ cha con 
- DOM Nodes: có nhiệm vụ thao tác với các thẻ HTML thông qua đối tượng Object
=======================================================
DOM document 
Dùng getElementById để truy xuất tới thẻ HTML theo ID
- document.getElementById('id')
Dùng getElementsByTagName để tìm theo tên thẻ HTML, Tên thẻ a, div, p, span...
- Kết quả trả về 1 mảng các object
- var a = document.getElementsByTagName('p')
	a.classList.add('box')
Dùng getElementsByClassName để tìm theo tên class
- var a = document.getElementsByClassName('box')
Dùng querySelector để tìm theo CSS selector
- var a = document.querySelector('ul li a')
Dùng querySelectorAll
- var a = document.querySelectorAll('ul li a')
==========================================================
DOM HTML lấy nội dung trong thẻ HTML 
innerHTML: lấy luôn thẻ vào nội dung text 
textContent: chỉ lấy text có cả khoảng trắng
innerText: lấy text và tự động loại bỏ khoảng trắng thừa
- Thay đổi thuộc tính thẻ HTML:
document.getAttribute('name')
document.setAttribute('newName')
=============================================================
DOM CSS dùng để thêm thuộc tính css 
document.getElementById('name').style.fontSize='14px'
=======================
DOM Event là một tác động nào đó lên các đối tượng HTML. Qua đó ta có thể bắt được sự kiện và viết code js thực thi một chương trình nào đó (Chỉ lắng nghe được chứ không hủy bỏ được, chỉ gọi được 1 sự kiện)
- onLoad(): Khi trình duyệt đã load xong mọi thứ (img, js, css) thì những đoạn code nằm bên trong đó mới được chạy
- onBlur(): Kích hoạt khi một phần tử không còn được focus vào nữa
- onFocus(): Kích hoạt khi 1 phần tử được focus vào
- onKeyDown(): Kich hoat khi 1 phim duoc nhan // thực thi xong mới hiển thị 
- onKeyUp(): Kich hoat khi 1 phím dược nhả ra // hiển thị nội dung trước rồi mới thực thi
- onClick(): Kích hoạt trên con chuột vừa nhấn vào phần tử
- onChange(): Kích hoạt khi giá trị được thay đổi khác đi so với giá trị trước đó

===================================
DOM Events Listener
- Giống DOM Event nhưng khác ở chổ
- Một element có thể gọi được nhiều sự kiện, có thể hủy bỏ lắng nghe sự kiện bất kỳ
==================================
DOM navigation
- Thể hiện mối quan hệ cha con giữa các thẻ
- Các thuộc tính: 
parentNode: dùng để truy cập nút cha của nút được chỉ định trong cây DOM
childNodes: truy cập tất cả các node con của một phần tử nhất định (Có thể là văn bản chú thích)
firstElementChild: trả về phần tử là node con đầu tiên của phần tử cha 
lastElementChild: trả về phần tử là node cuối cùng của phần tử cha
nextElementSibling: trả về phần tử là node kế tiếp
previousElementSibling: trả về phần tử là node trước đó
nodeName: trả về tên một node
==============================================================================
DOM Nodes
- Tạo ra một node mới hoàn toàn và không liên quan tới những thẻ HTML đang hiển thị trên web
- var a = document.createElement('tagName')
- document.createTextNode() text node là một node đặt biệt nó không phải là thẻ HTML thông thường mà chỉ là 1 chuổi string
- var a = document.createTextNode('Nội dung String')
- appenChild() 	Dùng để thêm vào vị trí cuối cùng của đối tượng một thẻ HTML nào đó
- insertBefore() dùng để thêm một node vào đằng trước một node con nào đó 
- removeChild() dùng để xóa một node ra khỏi node hiện tại
- replaceChild() dùng để thay thế một node con nào đó bằng một node mới hoàn toàn

BOM Browser Object Model các đối tượng liên quan đến trình duyệt, giúp chúng ta biết được lịch sử lướt web, lưu các hành động và trạng thái người dùng trên trang.
Các loại BOM
- window
- screen
- location
- history
- navigator
- popup
- timing
- cookies

BOM window là một đối tượng có nhưng phương thức và thuộc tính được dùng để xử lý trình duyệt, window có cấp độ cao nhất.
- innerHeight: lấy chiều cao của tài liệu
- innerWidth: lấy chiều rộng của tài trang
- open: mở một cửa sổ mới
- close: đóng cửa sổ mà ta dùng lệnh open để mở
BOM sreen:
- sreen.height: lấy chiều cao của máy tính
- screen.width: lấy chiều rộng của máy tính
BOM location là đối tượng được dùng để xử lý các vấn đề liên quan đến URL của trang web
BOM history: dùng để quản lý lịch sử lướt web
BOM navigator dùng để kiểm tra các thông tin về người dùng như trình duyệt đang sử dụng là gì, hệ điêu hành, trình duyệt có bật cookie hay không...
BOM pupup alert, promt, confirm
BOM timing setTimeOut (1 lần duy nhât), setIntever (lặp lại nhiều lần)
Cookie (*) là dữ liệu được lưu trữ trong một file text, nằm trong máy tính, cookie được lưu trữ vĩnh viễn hay theo thời gian cụ thể là do bạn thiết lập, khi trình duyệt gửi thông tin lên server thì cookie sẽ được gửi kèm theo, key-value
Thao tác với cookie: gán giá trị lại cho cookie, xóa cookie chỉ cần set lại ngày hết hạn expires

Scope: là phạm vi truy cập, ngữ cảnh của đoạn code 
có 2 kiểu phạm vi: 
Toàn cục Global: biến global được sử dụng ở đâu cũng được
Cục bộ Local: Một biến được khai báo trong hàm được gọi là biến local chỉ được sử dụng ở trong hàm đó
Hoisting: sử dụng 1 biến xong sau đó mới cần khai báo biến đó, js sẽ tự di chuyển toàn bộ các khai báo biến lên đầu chương trình.
Kiểu dữ liệu: var (undefined) có tính hoisting, let, const không có tính hoisting (is not define
Hàm: Declaration funtion: có tính hoisting
expression funtion: không có tính hoisting
arrow funtion: không có tính hoisting
Strict mode là chế độ nghiêm ngặt nó bắt buộc lập trình viên phải tuân thủ theo quy tắc mà js đưa ra
This trỏ về đối tượng mà nó đang thuộc về
Khi gán hành động cho các sự kiện js thì this chính là đối tượng html được gán sự kiện đó
Modules là một file js, việc phân chia thành từng module và mỗi module có mỗi công dụng khác nhau giúp cho quá trình code nhanh hơn, mạch lạc, và tái sử dụng ở nhiều nơi
Export, import, as, mỗi mudule chỉ có 1 export defaul, export default thì không có {}
Fetch API: dùng để gọi lên server thong qua 1 số api để lấy dữ liệu từ server trả về 
api: hiểu đơn giản là một url cho phép fe có thể giao tiếp với be
async/await: cơ chế xử lý bất đồng bộ, được xây dựng dựa trên promise
async: khai báo hàm bất đồng bộ, tự động biến 1 hàm bình thường thành 1 promise
await: tạm dừng việc thực hiện các hàm async khi được đặt trước 1 promise thì nó sẽ đợi cho đến khi promise kết thúc và trả về kết quả, chỉ được sử dụng trong các hàm async
Call back là 1 hàm được truyền dưới dạng đối số cho 1 hàm khác, có thể được chạy sau khi những tính năng khác két thúc 
Promise dùng để giải quyết vấn đè call back hell
call back hell là có nhiều hàm lồng nhau, và giả  sử để chạy hàm 2 thì phải đợi hàm 1 thực thi xong, muốn chạy hàm 3 thì phải đợi hàm 2 thực thi xong, viết đơn giản hơn callback
promise có 3 trạng thái 
pending: khi promise đang chạy
fulfilled: khi promise đã chạy xong, kết quả là 1 giá trị
rejected: khi promise bị lỗi thì sẽ ở trạng thái này, kết quả là 1 object lỗi
promise.all giúp các promise được thực thi xong xong nhau, tổng thời gian chạy của các chương trình chỉ bằng thời gian chạy của 1 promise lâu nhât
Localstorage: là kho lưu trữ ở phía người dùng, lưu trữ vô thời hạn, dữ liệu sẽ được lưu trữ cho đế khi ta xóa lịch sử trình duyệt web, setItem, getItem, removeItem, clear, key
sessionstorage: là kho lưu trữ theo phiên, lưu trữ theo 1 phiên làm việc khi tắt browser thì dữ liệu bị mất
cookie: 4mb, localstorage: 5mb, sessionstorage: 10mb
clausure: là 1 hàm bên trong hàm khác(bao đóng)
BEM Block element modifier là quy ước đặt tên cho các tên lớp css

các kiểu dữ liệu trong js: nguyên thủy
null, undefine, Number, String, Synbol, Boolean
phức tạp object: là kiểu dữ liệu tham chiếu

Biến var:
Có phạm vi là global hoặc local (trong function).
Có thể tái khai báo trong cùng một scope.
Sử dụng tính chất hoisting (biến được đưa lên đầu scope trước khi thực thi code).
Biến let:
Có phạm vi là block scoped (chỉ có thể truy cập trong block bao quanh nó).
Không thể tái khai báo trong cùng một scope.
Không sử dụng tính chất hoisting.
Biến const:
Cũng có phạm vi là block scoped.
Không thể tái khai báo.
Không thể thay đổi giá trị sau khi khởi tạo.
Toán tử == (so sánh trừu tượng):
Cố gắng giải quyết các kiểu dữ liệu thông qua việc chuyển đổi kiểu dữ liệu trước khi so sánh.
Ví dụ: 3 == "3" trả về true, vì chuỗi "3" được chuyển thành số 3 trước khi so sánh.
Tuy nhiên, việc chuyển đổi kiểu dữ liệu này có thể gây ra nhầm lẫn.
Toán tử === (so sánh cân bằng nghiêm ngặt):
Trả về false nếu các giá trị khác nhau hoặc kiểu dữ liệu khác nhau.
Không thực hiện chuyển đổi kiểu dữ liệu.
Ví dụ: 3 === "3" trả về false, vì đây là 2 kiểu dữ liệu khác nhau.
