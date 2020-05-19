# Refractoring-Lab

[Thực hành] Refactoring - tách biến
Mục tiêu
Luyện tập kỹ thuật tách biến.

Điều kiện:
- Vận dụng được kỹ thuật tách biến

Mô tả
Trong phần này, chúng ta sẽ áp dụng kỹ thuật tách biến dựa trên mã nguồn có sẵn.

Hướng dẫn
Bước 1: Chạy mã nguồn có sẵn

Tải mã nguồn tại: https://github.com/codegym-vn/php-cleancode-refactoring-variable-extraction.git

Mở file FizzBuzz.php, FizzBuzzMain.php và FizzBuzzTest.php để tìm hiểu mã nguồn và các test case.

Bước 2: Tách biến

Trong mã nguồn hiện tại, các biểu thức điều kiện if gây khó khăn khi đọc, do đó chúng ta có thể áp dụng kỹ thuật tách biến đối với các biểu thức này.

Mã nguồn sau khi tách biến.

public function __construct($number)
{
    $isFizz = $number % 3 == 0;
    $isBuzz = $number % 5 == 0;

    if($isFizz && $isBuzz) {
        $this->status =  "FizzBuzz";
    } elseif ($isFizz) {
        $this->status = "Fizz";
    } elseif ($isBuzz) {
        $this->status = "Buzz";
    } else {
        $this->status =  $number . "";
    }
}
Lưu ý: Sau mỗi bước tách biến thì cần chạy lại các test case để đảm bảo mã nguồn vẫn hoạt động tốt.

Tham khảo cách cài đặt và chạy PHPUnit: https://phpunit.de/getting-started/phpunit-7.html
