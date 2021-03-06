Tổng quát:
•	Hãy suy nghĩ đến các vấn đề bảo mật tất cả những gì trong đoạn mã (code) của bạn.
•	Đọc và làm theo những nguyên tắc hướng dẫn cho ngôn ngữ lập trình và kiểu phần mềm của bạn.
•	Tái sử dụng những đoạn mã đáng tin cậy (thư viện, mô-đun, etc,..).
•	Viết đoạn mã có chất lượng tốt, dễ đọc và dễ bảo trì (đoạn mã kém thì sẽ không an toàn).
Kiến trúc:
•	Tính mô-đun hóa: Chia chương trình thành các phần độc lập nhỏ hơn (nhỏ, các giao diện được xác định cho mỗi mô-đun hoặc chức năng).
•	Tính độc lập: Mỗi phần sẽ làm việc chính xác kể cả khi những phần khác bị lỗi (trả về kết quả sau, gửi yêu cầu với những tham số không hợp lệ.
•	Tính bảo vệ theo chiều sâu: Xây dựng nhiều lớp bảo vệ thay vì tin cậy vào một cơ chế bảo vệ. Ví dụ: xác thực dữ liệu đầu vào người dùng tại thời điểm đi vào, và kiểm tra lại tất cả giá trị được truyền đến những phần nhạy cảm của đoạn mã (như xử lý các tệp tin, etc.)
•	Tính đơn giản hóa: Những giải pháp phức tạp nhiều khi có thể trở lên không an toàn. 
Thiết kế:
•	Tạo các bộ phận bảo mật nhạy cảm của các đoạn mã nhỏ.
•	Nguyên tắc đặc quyền tối thiểu: Không yêu cầu đặc quyền nhiều hơn bạn cần. Ví dụ: chạy mã là quyền tối thiểu người dùng cần thiết (không chạy nó như là root). Hãy chắc chắn rằng tài khoản đó bạn sẽ chạy mã chỉ truy cập tập tin và thực hiện đặc quyền mà mã của bạn thực sự cần. Không kết nối tới một cơ sở dữ liệu với đặc quyền quản trị từ phần mềm của bạn.
•	Chọn mặc định an toàn: Ví dụ, một mật khẩu ngẫu nhiên mà người sử dụng có khả năng thay đổi hơn là một mật khẩu mặc định tiêu chuẩn mà nhiều người sẽ không bận tâm để thay đổi.
•	Từ chối theo mặc định: Ví dụ, khi xác nhận đầu vào người sử dụng chỉ chấp nhận các ký tự mà bạn mong đợi hơn là cố gắng để ngăn chặn tiếng nhân vật "xấu";
•	Hạn chế tiêu thụ tài nguyên, để hạn chế khả năng hoặc tác động của một tấn công từ chối dịch vụ.
•	Không an toàn: Ví dụ, nếu có một lỗi runtime khi kiểm tra quyền truy cập của người sử dụng, trong trường hợp người đó không có.
•	Trong phân phối hoặc các ứng dụng web không tin tưởng cho khách hàng: Đừng mong đợi việc xác nhận đầu vào người sử dụng, thực hiện kiểm tra an ninh hoặc xác thực người dùng - tất cả đều phải được thực hiện (một lần nữa) ở phía máy chủ; nhớ rằng các trường đáp ứng tiêu đề HTTP (cookies, user-agent, referrer ..) và các giá trị chuỗi truy vấn HTTP (từ các trường ẩn hoặc liên kết rõ ràng) có thể bị giả mạo/thao túng.
•	Mật mã học: Sử dụng tin cậy, các thuật toán công cộng, các giao thức và các sản phẩm. Đừng phát minh ra thuật toán mật mã hoặc các giao thức của riêng bạn, cũng không phải thực hiện những cái hiện có - tái sử dụng mã tin cậy.
Coding:
•	Không tin dữ liệu đầu vào: Dữ liệu đầu vào từ người sử dụng có khả năng độc hại cho chương trình: dữ liệu không đúng, không hợp lệ, sai loại dữ liệu… làm cho chương trình bị lỗi, không chạy đúng.
•	Kiểm tra tất cả dữ liệu đầu vào: Xem xét tất cả các trường hợp dữ liệu đầu vào có thể bị lỗi để đảm bảo chương trình chạy đúng không có lỗi. Kiểm tra dữ liệu theo các cấp độ sử dụng ví dụ tại thời điểm nhập dữ liệu và trước khi sử dụng.
•	Không giả định bất kỳ giả định gì về môi trường: đảm bảo rằng mã lệnh chạy đúng với tất cả các môi trường xác định trước
•	Hãy coi chừng điều kiện chủng tộc: Mã chạy của bạn có thể song song? nếu ai đó thực hiện hai trường hợp của chương trình tại cùng một thời điểm, hoặc thay đổi môi trường ở giữa thực hiện của nó?
•	Bắt các đoạn mã lệnh lỗi và ngoại lệ: Đừng cho rằng mọi thứ sẽ làm việc, phải kiểm soát được các ngoại lệ, các trường hợp lỗi của chương trình.
•	Fail gracefully: Trong trường hợp mà có mã lệnh lỗi mà không thể khắc phục được thì phải viết báo cáo chi tiết, cảnh bảo người quản trị, làm sạch hệ thống, thông báo cho người sử dụng.
•	Bảo vệ mật khẩu và các thông tin bảo mật: đảm bảo độ bảo mật cho người dung ví dụ: mã hóa mật khẩu dạnh MD5…
•	Hãy cẩn thận khi làm việc với tập tin: Nếu bạn muốn tạo ra nó, báo cáo một lỗi nếu nó đã tồn tại, khi bạn tạo nó thì thiết lập quyền tập tin. Nếu bạn mở 1 tập tin chỉ để đọc thì không yêu cầu quyền ghi tập tin, kiểm tra file bạn mở không phải liên kết với các hàm IsTat(),sử dụng tên đường dẫn tuyệt đối (cho cả hai lệnh và file); cẩn thận khi tên file (hoặc một phần của nó) đến từ một người sử dụng
•	Tập tin tạm thời: Tránh chúng bất cứ khi nào có thể. Pipes là một cách an toàn hơn và hiệu quả hơn trong giao tiếp thông tin giữa các quá trình. Nếu bạn thực sự cần các tập tin remporary, không thuộc đối với các cuộc tấn công liên kết tượng trưng (người nào đó đoán tên của tập tin tạm thời của bạn, và tạo ra một liên kết từ nó đến một tập tin ví dụ: /bin/bash, rằng chương trình của bạn sẽ ghi đè lên). Các file tạm thời phải có tên duy nhất mà khó đoán! (Sử dụng tmpfile() cho C/C++, lệnh shell mktemp vv);
•	Hãy cẩn thận với các cuộc gọi vỏ, chức năng eval v.v .: chức năng như đánh giá các đối số chuỗi như mã và giải thích nó, hoặc chạy nó trên vỏ. Nếu kẻ tấn công được quản lý để tiêm đầu vào nguy hiểm để lập luận rằng, bạn đang thực hiện mã của mình.
Sau khi cài đặt:
•	Xem qua code của bạn và để cho người khác xem xét nó
•	Khi một bug được tìm thấy, tìm kiếm những cái tương tự
•	Sử dụng những tool để xác định tới ngôn ngữ lập trình: test bộ nhớ, tìm bug, … 
•	Bật cảnh báo trình biên dịch/ phiên dịch và đọc chúng, vô hiệu hóa thông tin gỡ lỗi.

