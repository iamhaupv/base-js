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

