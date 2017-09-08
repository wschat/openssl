# php openssl 加密、签名


#### 注：需要 extension=php_openssl.dll 扩展



> 对称加密 

~~~
$token='需要加密的内容';	// array | string
$key='秘钥';	// array | string

string $crypted=Rsa::encode($token,$key); //加密

string|array Rsa::decode($crypted,$key); //解密
~~~





> 非对称加密 

~~~
$token='需要加密的内容';	// array | string

string $crypted=Rsa::ssl_encode($token); //加密

string|array Rsa::ssl_decode($crypted); //解密

~~~


> 签名 

~~~
$token='需要签名的内容';	// array | string

string $crypted=Rsa::sign_encode($token); //私匙签名

number Rsa::sign_decode($token,$signature); //公匙签名验证  (1：成功 | 0：失败 | -1：错误)

~~~

---
[https://github.com/wschat/openssl](https://github.com/wschat/openssl)
