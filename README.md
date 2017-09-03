# Ajax
( Version:0.1 )

[ Türkçe kullanım klavuzu için tıklayınız.](https://github.com/furkansenturk/Javascript/blob/master/Ajax/Talimat.md)

Ajax function that will be developed to make Ajax simple to use

| Settings | Explanation|
| ------ | ------ |
| url | **URL** address to which the request will be sent |
| method | The HTTP method to use for the request (Ex: **POST**, **GET**) |
| data | Data to be sent to the server. GET is automatically appended to the URL for requests. Json data can be added if requested |
| response | Response from the server |
| responseType | The type of response from the server (Ex: **Json**) |

Examples of use:
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
