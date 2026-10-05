# Câu hỏi phỏng vấn JavaScript
> Tổng hợp câu hỏi phỏng vấn JavaScript kèm câu trả lời (bản dịch tiếng Việt từ ghi chú tiếng Anh).

## Mục lục

- [Câu hỏi phỏng vấn JavaScript](#câu-hỏi-phỏng-vấn-javascript)
  - [Mục lục](#mục-lục)
  - [JavaScript là gì? Nó khác gì các ngôn ngữ lập trình khác?](#javascript-là-gì-nó-khác-gì-các-ngôn-ngữ-lập-trình-khác)
  - [Sự khác nhau giữa let, const và var là gì?](#sự-khác-nhau-giữa-let-const-và-var-là-gì)
  - [Giải thích sự khác nhau giữa == và === trong JavaScript.](#giải-thích-sự-khác-nhau-giữa--và--trong-javascript)
  - [Có những cách nào để khai báo một hàm trong JavaScript?](#có-những-cách-nào-để-khai-báo-một-hàm-trong-javascript)
  - [Sự khác nhau giữa global scope, function scope và block scope là gì?](#sự-khác-nhau-giữa-global-scope-function-scope-và-block-scope-là-gì)
  - [Sự khác nhau giữa function declaration và function expression là gì?](#sự-khác-nhau-giữa-function-declaration-và-function-expression-là-gì)
  - [Arrow function là gì và chúng khác gì hàm thông thường?](#arrow-function-là-gì-và-chúng-khác-gì-hàm-thông-thường)
  - [Object trong JavaScript là gì? Tạo object bằng cách nào?](#object-trong-javascript-là-gì-tạo-object-bằng-cách-nào)
  - [Sự khác nhau giữa shallow copy và deep copy là gì?](#sự-khác-nhau-giữa-shallow-copy-và-deep-copy-là-gì)
  - [Event loop trong JavaScript là gì?](#event-loop-trong-javascript-là-gì)
  - [Giải thích sự khác nhau giữa JavaScript đồng bộ và bất đồng bộ.](#giải-thích-sự-khác-nhau-giữa-javascript-đồng-bộ-và-bất-đồng-bộ)
  - [Callback function là gì?](#callback-function-là-gì)
  - [Dùng setTimeout() và setInterval() như thế nào?](#dùng-settimeout-và-setinterval-như-thế-nào)
  - [DOM là gì? Chọn phần tử bằng JavaScript như thế nào?](#dom-là-gì-chọn-phần-tử-bằng-javascript-như-thế-nào)
  - [Thay đổi nội dung của một phần tử HTML bằng JavaScript như thế nào?](#thay-đổi-nội-dung-của-một-phần-tử-html-bằng-javascript-như-thế-nào)
  - [Event bubbling và event delegation là gì?](#event-bubbling-và-event-delegation-là-gì)
  - [Xử lý lỗi trong JavaScript như thế nào?](#xử-lý-lỗi-trong-javascript-như-thế-nào)
  - [Sự khác nhau giữa try-catch và throw là gì?](#sự-khác-nhau-giữa-try-catch-và-throw-là-gì)
  - [Sự khác nhau giữa .call(), .apply() và .bind() (để điều khiển từ khóa this)](#sự-khác-nhau-giữa-call-apply-và-bind-để-điều-khiển-từ-khóa-this)
  - [Từ khóa new hoạt động như thế nào?](#từ-khóa-new-hoạt-động-như-thế-nào)
  - [Sự khác nhau giữa map(), filter(), reduce.](#sự-khác-nhau-giữa-map-filter-reduce)
  - [Promise trong JavaScript là gì?](#promise-trong-javascript-là-gì)
  - [async/await](#asyncawait)
  - [Garbage collection hoạt động như thế nào?](#garbage-collection-hoạt-động-như-thế-nào)
  - [Làm thế nào để ngăn chặn memory leak?](#làm-thế-nào-để-ngăn-chặn-memory-leak)
  - [Lazy loading là gì? Triển khai như thế nào?](#lazy-loading-là-gì-triển-khai-như-thế-nào)
  - [Sự khác nhau giữa localStorage, sessionStorage và cookies là gì?](#sự-khác-nhau-giữa-localstorage-sessionstorage-và-cookies-là-gì)

---

## JavaScript là gì? Nó khác gì các ngôn ngữ lập trình khác?

- JavaScript là ngôn ngữ lập trình dùng để làm cho trang web có tính tương tác. Nó chạy được cả trên trình duyệt lẫn trên server.
- Nó khác các ngôn ngữ lập trình khác ở chỗ:
  + Chạy trên trình duyệt (chạy trực tiếp trong các trình duyệt như Chrome, Firefox,... mà không cần cài đặt thêm gì)
  + Dynamic typing (nghĩa là bạn không cần khai báo kiểu của biến)
  + Single-threaded (nghĩa là xử lý một tác vụ tại một thời điểm) + event loop (JavaScript trở nên mạnh mẽ nhờ event loop, cho phép JS xử lý các tác vụ bất đồng bộ như gọi api, đọc file,... mà không chặn chương trình chính.
  + Không cần compile (JS không yêu cầu bước compile riêng, engine như V8 vẫn biên dịch JIT khi chạy)

## Sự khác nhau giữa let, const và var là gì?

Let, const và var là các từ khóa để khai báo biến trong JavaScript.

- Var:
  + Scope: Function scope -> biến nhìn thấy được trong toàn bộ hàm
  + Reassign: có thể gán giá trị mới.
  + Redeclare: có thể khai báo lại cùng một biến
  + Hoisting: JS đưa phần khai báo lên đầu, nhưng giá trị là undefined cho đến khi dòng đó được thực thi
- let:
  + Scope: block scope -> chỉ nhìn thấy được bên trong block
  + Reassign: có thể gán giá trị mới
  + Redeclare: không thể khai báo lại cùng một biến trong cùng scope
  + Hoisting: được hoisted nhưng nằm trong temporal dead zone -> không thể dùng trước khi khai báo.
- const:
  + scope: block scope
  + reassign: không thể gán giá trị mới
  + redeclare: không thể khai báo lại cùng một biến trong cùng scope
  + Hoisting: được hoisted nhưng nằm trong temporal dead zone

-> Hoisting nghĩa là JS đưa phần khai báo biến và hàm lên đầu scope của chúng trước khi thực thi code

## Giải thích sự khác nhau giữa == và === trong JavaScript.

==(loose equality) so sánh giá trị sau khi ép kiểu (type coercion).
===(strict equality) so sánh cả giá trị lẫn kiểu, không ép kiểu—hãy dùng === để kiểm tra cho đáng tin cậy.” -> An toàn và dễ dự đoán hơn.

## Có những cách nào để khai báo một hàm trong JavaScript?

- Function declaration:
  + Định nghĩa bằng từ khóa "function"
  + Có thể dùng nó trước dòng code mà nó được viết.

Ví dụ:

```js
declaration();
function declaration(){
 console.log(“This is function declaration”);
}
```

- Function expression:
  + Hàm được gán cho một biến
  + Không được hoisted -> phải gọi sau dòng mà nó được định nghĩa

```js
const expression = function(){
 console.log(“this is function expression”);
};
expression()// must be call after the line where it is defined.
```

- Arrow function:
  + cú pháp ngắn gọn

## Sự khác nhau giữa global scope, function scope và block scope là gì?

“Global scope truy cập được ở mọi nơi.
Function scope giới hạn biến trong hàm.
Block scope giới hạn biến bên trong {} "dấu ngoặc nhọn" khi khai báo bằng let hoặc const.”-

## Sự khác nhau giữa function declaration và function expression là gì?

- Function declaration:
  + Định nghĩa bằng từ khóa "function"
  + Có thể dùng nó trước dòng code mà nó được viết.
- Function expression:
  + Hàm được gán cho một biến
  + Không được hoisted -> phải gọi sau dòng mà nó được định nghĩa

## Arrow function là gì và chúng khác gì hàm thông thường?

- Arrow function dùng => (toán tử mũi tên) và cho phép cú pháp ngắn hơn hàm truyền thống -> hữu ích cho biểu thức ngắn gọn, callback, hàm inline
- Không có this riêng

- Không có đối tượng arguments (dùng rest parameter, cái này cũng là một mảng)

- không thể gọi bằng constructor.”

## Object trong JavaScript là gì? Tạo object bằng cách nào?

Object là một cấu trúc dữ liệu lưu trữ thông tin, bao gồm các cặp key-value
- key: tên thuộc tính
- value: dữ liệu

Có nhiều cách để tạo một object:
- Object literal
- Dùng new Object()
- Dùng constructor function
- Dùng class

## Sự khác nhau giữa shallow copy và deep copy là gì?

- shallow copy: chỉ sao chép các thuộc tính ở cấp cao nhất. Nếu object chứa object/mảng lồng bên trong, các object bên trong không được sao chép; chỉ sao chép tham chiếu

- Deep copy tạo ra một bản sao hoàn chỉnh, độc lập của toàn bộ cấu trúc.

## Event loop trong JavaScript là gì?

JavaScript chạy trên một thread duy nhất. Event loop đóng vai trò trung gian, liên tục kiểm tra xem call stack có trống không, và nếu trống thì lấy các tác vụ từ queue rồi đẩy chúng vào call stack để thực thi. in

## Giải thích sự khác nhau giữa JavaScript đồng bộ và bất đồng bộ.

JavaScript đồng bộ thực thi code từng dòng một và chặn việc thực thi tiếp theo, còn JavaScript bất đồng bộ cho phép các tác vụ chạy lâu chạy ngầm bằng callback, promise hoặc async/await mà không chặn main thread.

## Callback function là gì?

Callback function là một hàm được truyền làm đối số cho một hàm khác và được thực thi sau đó, thường là sau khi một tác vụ bất đồng bộ kết thúc hoặc khi một sự kiện xảy ra.

## Dùng setTimeout() và setInterval() như thế nào?

“setTimeout(fn, ms) chạy một hàm một lần sau khoảng trễ.
setInterval(fn, ms) chạy lặp lại theo khoảng thời gian chỉ định.”

## DOM là gì? Chọn phần tử bằng JavaScript như thế nào?

DOM là: DOM biểu diễn một trang HTML dưới dạng cấu trúc cây để JavaScript có thể tương tác và chỉnh sửa trang một cách động.
Chọn một phần tử như thế nào? Theo ID, theo tên thẻ, querySelector.

## Thay đổi nội dung của một phần tử HTML bằng JavaScript như thế nào?

Có hai cách để thay đổi nội dung phần tử:
- textContent:
  + Chỉ thay đổi phần text bên trong phần tử; mọi thứ đều là plain text

innerHTML:
  + Thay đổi phần HTML bên trong phần tử.
  + có thể chứa các thẻ, các thẻ này sẽ được render thành HTML

## Event bubbling và event delegation là gì?

- Event Bubbling: Khi một sự kiện xảy ra trên phần tử con, nó nổi lên (bubble) các phần tử cha cho đến khi chạm tới root.

- Event Delegation: Thay vì gắn event listener cho nhiều phần tử con, ta gắn một listener vào một phần tử cha chung.

## Xử lý lỗi trong JavaScript như thế nào?

Để xử lý lỗi trong JavaScript, ta dùng khối try-catch.
Khối try-catch dùng để xử lý các exception có thể xuất hiện, ngăn chương trình dừng đột ngột. Khối try chứa code có thể ném ra exception; nếu xảy ra, việc thực thi nhảy sang khối catch để xử lý.
-> Ngăn chương trình dừng đột ngột cho phép bạn hiển thị một thông báo thân thiện,

## Sự khác nhau giữa try-catch và throw là gì?

- try-catch để bao các lỗi xảy ra trong lúc thực thi code, bao gồm cả lỗi do code (như TypeError) và lỗi do throw.
- throw dùng để tạo ra một lỗi.

## Sự khác nhau giữa .call(), .apply() và .bind() (để điều khiển từ khóa this)

- call(thisArg, arg1, arg2, ...) → thực thi ngay lập tức, các đối số truyền riêng lẻ.
- .apply(thisArg, [argsArray]) → thực thi ngay lập tức, các đối số truyền dưới dạng mảng.
- .bind(thisArg, arg1, arg2, ...) → trả về một hàm mới, thực thi sau.

## Từ khóa new hoạt động như thế nào?

thực hiện 4 bước:
- Tạo một object rỗng mới.
- Đặt prototype của object thành prototype của constructor.
- Gọi hàm constructor với this trỏ tới object mới.
- Trả về object mới.

## Sự khác nhau giữa map(), filter(), reduce.

map → tạo một mảng mới bằng cách biến đổi từng phần tử
filter → tạo một mảng mới chỉ chứa các phần tử thỏa một điều kiện
reduce → rút gọn một mảng thành một giá trị duy nhất bằng cách tích lũy kết quả

## Promise trong JavaScript là gì?

Promise đại diện cho một giá trị có thể có sẵn ngay bây giờ, trong tương lai, hoặc không bao giờ. Các trạng thái: pending → fulfilled / rejected.

## async/await

async đánh dấu một hàm là bất đồng bộ.
await tạm dừng việc thực thi cho đến khi Promise được resolve

## Garbage collection hoạt động như thế nào?

JavaScript dùng garbage collection kiểu mark-and-sweep, trong đó các object không còn truy cập được từ root (là biến mà js engin chắc chắn còn dùng được) sẽ tự động bị xóa khỏi bộ nhớ.

## Làm thế nào để ngăn chặn memory leak?

- Tránh biến global.
- Xóa timer (setInterval, setTimeout).
- Gỡ event listener.
- Tránh giữ các tham chiếu không cần thiết trong closure.

## Lazy loading là gì? Triển khai như thế nào?

Chỉ tải nội dung khi cần để cải thiện hiệu năng. Trong React, ta dùng React.lazy() và Suspense để triển khai.
Suspense chỉ “chờ” những component / tài nguyên render theo kiểu bất đồng bộ.
Nếu component đó chưa sẵn sàng (chưa load xong),
React sẽ tạm thời render fallback để thay thế.

## Sự khác nhau giữa localStorage, sessionStorage và cookies là gì?

- localStorage: lưu tối đa ~5MB trên client, tồn tại sau khi đóng trình duyệt, dùng cho dữ liệu client lâu dài.
- sessionStorage: lưu tối đa ~5MB trên client, bị xóa khi đóng tab, dùng cho dữ liệu phiên tạm thời.
- cookies: lưu tối đa ~4KB, được gửi lên server cùng các request, có thể đặt thời hạn, dùng cho xác thực/session.
-> localstorage và sessionStorage khác giống nhau khi set, get properties, lưu dưới dạng key-value nhưng localStorage lưu dữ liệu lâu dài, còn sessionStorage chỉ tồn tại trong 1 tag duy nhất
-> Cookies là dữ liệu nhỏ được lưu ở browser và tự động gửi lên server trong mỗi request và có thể cấu hình các thuộc tính như HttpOnly, Secure, SameSite để kiểm soát bảo mật và phạm vi sử dụng. (cookies được lưu vào cookies jar, vì cookies gắn liền với domain )
