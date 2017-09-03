# Ajax

ajax isteğini basit bir şekilde kullanabilmek için geliştirmekte olduğum ajax fonksiyonu

| Ayar | Açıklama |
| ------ | ------ |
| url | İsteğin gönderileceği **URL** adresi |
| method | istek için kullanılacak HTTP yöntemi (Örn: **POST**, **GET**) |
| data | Sunucuya gönderilecek veriler GET istekleri için otomatik olarak dizeye eklenir. İstenildiği takdirde Json tipinde de değer girilebilir |
| response | Sunucudan gelen yanıt |
| responseType | Sunucudan gelen yanıtın tipi (Örn: **Json**) |

Kullanım örnekleri:
```js
ajax({
    url         : "ajax.php",
    method      : "POST",
    response    : function(e){
        document.getElementById("sonuc").innerHTML = e;
    }
});
```
```js
ajax({
    url         : "ajax.php",
    method      : "POST",
    data        : {"id":10,"s":"merhaba"},
    response    : function(e){
        document.getElementById("sonuc").innerHTML = e;
    }
});
```
```js
ajax({
    url         : "ajax.php",
    method      : "POST",
    data        : "id=5&s=merhaba",
    responseType: "Json",
    response    : function(e){
        document.getElementById("sonuc").innerHTML = e;
    }
});
```
