# Câu hỏi phỏng vấn React
> Tổng hợp câu hỏi phỏng vấn React kèm câu trả lời (bản dịch tiếng Việt từ ghi chú tiếng Anh), kèm vài câu về RESTful API.
## Mục lục

1. [React là gì? Vì sao dùng React thay vì Angular hoặc Vue?](#react-là-gì-vì-sao-dùng-react-thay-vì-các-framework-khác-như-angular-hoặc-vue)
2. [JSX](#jsx-là-gì-nó-khác-gì-javascript-thông-thường)
3. [Virtual DOM](#virtual-dom-là-gì-nó-hoạt-động-như-thế-nào)
4. [State và props](#sự-khác-nhau-giữa-state-và-props)
5. [Controlled và uncontrolled component](#controlled-và-uncontrolled-component-trong-react-là-gì)
6. [Các cách truyền dữ liệu giữa component](#có-bao-nhiêu-cách-để-truyền-dữ-liệu-giữa-các-component)
7. [React Component](#react-component-là-gì-có-bao-nhiêu-loại-component-trong-react)
8. [Xử lý sự kiện](#xử-lý-sự-kiện-trong-react-hoạt-động-như-thế-nào)
9. [RESTful API](#restful-api-là-gì)
10. [React Hooks](#react-hooks-là-gì-kể-tên-một-số-hook-hay-dùng)
11. [useEffect và componentDidMount](#sự-khác-nhau-giữa-useeffect-và-componentdidmount)
12. [Context API](#context-api-là-gì-khi-nào-nên-dùng-context-api-thay-vì-redux)
13. [Khi nào dùng Redux thay vì Context API](#khi-nào-dùng-redux-thay-vì-context-api)
14. [Tối ưu hiệu năng trong React](#làm-thế-nào-để-tối-ưu-hiệu-năng-trong-react)

---

## React là gì? Vì sao dùng React thay vì các framework khác như Angular hoặc Vue?

React là một thư viện JavaScript để xây dựng giao diện người dùng. Nó linh hoạt, nhanh nhờ Virtual DOM, và có cộng đồng rất lớn. Nó chỉ tập trung vào tầng view, nên nhẹ hơn Angular và được áp dụng rộng rãi hơn Vue.

## JSX là gì? Nó khác gì JavaScript thông thường?

JSX là phần mở rộng cú pháp của JavaScript cho phép bạn viết các cấu trúc giống HTML bên trong file JavaScript. Nó không phải HTML thật và không thể chạy trực tiếp trên trình duyệt. Trước khi thực thi, JSX được transpile thành JavaScript thuần mà React có thể render.

## Virtual DOM là gì? Nó hoạt động như thế nào?

Khi React render UI, nó tạo ra một Virtual DOM trong bộ nhớ để mô tả giao diện. Khi state thay đổi, React dựng một Virtual DOM mới, so sánh nó với cái cũ (diffing), và chỉ cập nhật những phần đã thay đổi của DOM thật bằng ReactDOM

## Sự khác nhau giữa state và props?

- State: Dữ liệu nội bộ của một component, có thể thay đổi bằng setState hoặc useState.
- Props: Dữ liệu được truyền từ component cha xuống component con, chỉ đọc (read-only), và component con không thể sửa.

## Controlled và uncontrolled component trong React là gì?

Trong controlled component, dữ liệu form được xử lý bởi state của React, còn trong uncontrolled component, dữ liệu form được xử lý bởi DOM và được truy cập thông qua ref.

## Có bao nhiêu cách để truyền dữ liệu giữa các component?

**Props:**
Cha truyền dữ liệu xuống các component con thông qua props.

**Callback props:**
Cha truyền một hàm làm prop; con gọi hàm đó để gửi dữ liệu ngược lại cho cha.

**Context API:**
Tạo một context → bọc các component bằng Provider → dùng dữ liệu bằng useContext.

**Lifting state up:**
Chuyển state dùng chung lên component cha chung gần nhất để các component anh em (sibling) có thể chia sẻ và cập nhật nó.

**Router / URL params:**
Truyền dữ liệu qua tham số route hoặc query string trên URL.

Trong React, dữ liệu có thể được truyền bằng props, callback props để giao tiếp từ con lên cha, Context API cho dữ liệu toàn cục, lifting state up cho state dùng chung giữa các sibling, và tham số router để truyền dữ liệu qua URL.

## React Component là gì? Có bao nhiêu loại Component trong React?

Component là một đoạn code độc lập, có thể tái sử dụng, trả về UI.

- Functional Component: Component dựa trên hàm, dùng Hooks, và là cách phổ biến nhất hiện nay.
- Class Component: Dùng một class extend React.Component.

## Xử lý sự kiện trong React hoạt động như thế nào?

-> React dùng Synthetic Event, bao bọc các sự kiện gốc của trình duyệt để đảm bảo nhất quán giữa các trình duyệt.
Thay vì gắn event listener vào từng phần tử, React dùng event delegation bằng cách gắn một listener duy nhất ở root.
Khi một sự kiện xảy ra, React tạo một SyntheticEvent và chuyển nó đến đúng handler của component.

## RESTful API là gì?

RESTful API là một Web API được thiết kế theo kiến trúc REST (Representational State Transfer) - tức là một API tuân thủ một tập các nguyên tắc và ràng buộc của REST, cho phép client và server giao tiếp qua HTTP một cách nhất quán, nhẹ và có khả năng mở rộng, bao gồm:

- Client-Server: Tách biệt rõ ràng giữa client và server.
- Stateless: Mỗi request độc lập; server không giữ trạng thái session.
- Cacheable: Response có thể được cache để tăng hiệu năng.
- Layered system: Client không cần biết nó đang gọi server nào.
- Uniform interface: URL rõ ràng, được chuẩn hóa.

-> Một web API tuân theo các quy tắc này được gọi là RESTful API.
-> RESTful API là một Web API tuân theo các nguyên tắc REST, dùng HTTP để cho phép giao tiếp stateless, có khả năng mở rộng và được chuẩn hóa giữa client và server.

## React Hooks là gì? Kể tên một số hook hay dùng.

React hooks là các hàm đặc biệt cho phép bạn dùng các tính năng của React - như state, lifecycle và context - bên trong functional component -> giúp code của bạn đơn giản, sạch hơn, dễ tái sử dụng hơn. Các hook phổ biến:

- useState: dùng để khai báo và cập nhật state bên trong function component.
- useEffect: dùng để xử lý side effect ((tác vụ phụ) là bất kỳ hành động nào xảy ra ngoài quá trình render UI.) như lấy dữ liệu (fetching data), đặt timer, cập nhật DOM, và dọn dẹp tài nguyên.
- useContext: bạn đọc dữ liệu từ context mà không cần truyền props qua nhiều cấp.
- useRef: lưu một giá trị có thể thay đổi (mutable) và được giữ nguyên (persist) [pɚˈsɪst] qua các lần render mà không làm component render lại. (không render lại Component khi giá trị useRef thay đổi)
- useMemo: ghi nhớ (memoize) kết quả của phép tính và chỉ tính lại khi các dependency thay đổi.
- useCallback: trả về một phiên bản đã được ghi nhớ (memoized) của một hàm để tránh render lại không cần thiết.

```
Mỗi lần bấm Increase Count → state count thay đổi → Parent render lại
Parent tạo handleClick mới
Child nhận props onClick mới → Child render lại, mặc dù UI của Child không thay đổi
Console log sẽ in “Child rendered” mỗi lần bấm
→ Đây là vấn đề performance nếu Child nặng hoặc nhiều component con
Parent render lại khi count thay đổi
Nhưng handleClick không được tạo mới vì useCallback đã ghi nhớ function
Child nhận props giống y hệt → Child KHÔNG render lại
Console log sẽ chỉ in một lần khi component mount, không in khi bấm Increase Count
```

- useReducer dùng để quản lý logic state phức tạp, thường là một lựa chọn nhẹ thay cho redux

useReducer hữu ích để quản lý logic state phức tạp và làm cho việc cập nhật state dễ dự đoán hơn.

-> React Hooks là các hàm cho phép bạn dùng state và các tính năng khác của React trong functional component. Các hook phổ biến gồm useState, useEffect, useContext, useRef, useMemo, useCallback, và useReducer.

## Sự khác nhau giữa useEffect và componentDidMount?

DOM biểu diễn một trang HTML dưới dạng cấu trúc cây để JavaScript có thể tương tác và sửa đổi trang một cách động.

- componentDidMount() trong class component chỉ chạy một lần sau khi component render.
- useEffect() mặc định chạy sau mỗi lần render, trừ khi bạn truyền vào dependency array.

-> componentDidMount chạy một lần sau khi một class component được mount (tức là đã đính vài Dom-> tức là sau khi render ở lần đầu tiên), còn useEffect có thể chạy sau mỗi lần render hoặc chạy có điều kiện tùy theo dependency array của nó.

## Context API là gì? Khi nào nên dùng Context API thay vì Redux?

Context API là một cách để chia sẻ dữ liệu toàn cục giữa nhiều component mà không cần truyền props xuống thủ công (prop drilling).

- Dùng Context khi:
  - Bạn chỉ cần chia sẻ state đơn giản như theme, ngôn ngữ, thông tin người dùng.
  - Bạn muốn tránh prop drilling trong các component lồng nhau sâu.
  - Logic state của bạn không quá phức tạp.

-> Context API cho phép chia sẻ dữ liệu toàn cục trong React mà không cần prop drilling và phù hợp nhất với state đơn giản, độ phức tạp thấp như theme hoặc thông tin người dùng.

## Khi nào dùng Redux thay vì Context API?

Dùng Redux khi:

- Ứng dụng của bạn có logic state phức tạp.
- Nhiều component cần cùng một dữ liệu.

-> Redux được dùng tốt nhất cho các ứng dụng có state phức tạp, dùng chung, cần dễ dự đoán (predictable) và truy cập được từ nhiều component, trong khi Context API phù hợp hơn với state toàn cục đơn giản

## Làm thế nào để tối ưu hiệu năng trong React?

- Chỉ render khi cần thiết
- Chỉ tính toán khi cần
- Chỉ tải những gì người dùng thực sự cần

-> Để tối ưu hiệu năng, ta nên chỉ render component khi cần thiết, chỉ tính các giá trị khi cần, và chỉ tải phần code mà người dùng thực sự cần.

## Nguồn tham khảo

- Ghi chú phỏng vấn cá nhân (bản gốc tiếng Anh, dán vào để dịch).
