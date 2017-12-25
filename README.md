# AIRNativeExtension

>AIR Native Extensions (ANE) là tiện ích cho phép các nhà phát triển bổ sung năng có tính tương tác cao, mang đến trải nghiệm người dùng tốt hơn cho các ứng dụng Flex của họ bằng cách sử dụng các thư viện được viết bằng Objective-C hoặc Java để truy cập trực tiếp đến API mà Apple/Google cung cấp cho nhà phát triển.

>Như vậy, một project Flex có thể có nhiều ANE khác nhau, mỗi ANE được xây dựng bằng ActionScript3 API và phần native code (Java cho Android và Objective-C cho iOS).

### Wiki

[SE-AIRNativeExtension Wiki](https://github.com/se-ane/SE-AIRNativeExtension/wiki)

### Lưu ý

>Swift 3.0: Adobe chưa có bất kỳ hỗ trợ chính thức nào liên quan đến việc hỗ trợ Swift trên nền tảng iOS, trái lại với việc Apple luôn khuyến khích các nhà phát triển ứng dụng migrate sang Swift càng nhanh càng tốt. Objective-C sẽ sớm không còn nằm trong danh sách hỗ trợ của Apple.

>Kotlin: Tương tự như với trường hợp của Swift, Google và JetBrains đang khuyến khích các nhà phát triển trên Android chuyển sang sử dụng Kotlin cùng với hệ sinh thái Android. Tuy vậy, do đặc tính riêng của Kotlin mà việc sử dụng Kotlin cùng với ANE dễ hơn rất nhiều so với trường hợp của Swift. Do vậy, việc phát triển ANE cùng với Kotlin nên được củng cố.

Để tìm hiểu về ANE, nhóm dự định sẽ thực hiện các công việc sau:

* Tìm hiểu và nắm được các khái niệm cơ bản của ANE, cách giao tiếp giữa AIR application với ANE và với thiết bị.

* Dựa trên tutorial của Adobe để code 1 ANE: VolumeController (ANE này được phát triển để giúp các ứng dụng chạy trên nền AIR có thể bắt được sự kiện thay đổi volume của thiết bị, và kiểm soát việc thay đổi volume này).

* Tiến hành code 1 ANE: Vibration (ANE này hỗ trợ cơ chế rung của điện thoại khi cần).

* Tiến hành code 1 ANE tiếp theo: AccountController hoặc FileChooser.
