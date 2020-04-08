# TRY JsonPlaceholder

Partendo dal servizio https://jsonplaceholder.typicode.com/ [My JSON Server](https://my-json-server.typicode.com/).

<> Risorse disponibili:
* [users](http://my-json-server.typicode.com/checksound/my-blog/users)
* [posts](http://my-json-server.typicode.com/checksound/my-blog/posts)
* [comments](http://my-json-server.typicode.com/checksound/my-blog/comments)
* [db](http://my-json-server.typicode.com/checksound/my-blog/db)

Puoi utilizzare `GET`, `POST`, `PUT`, `PATCH` e `DELETE`. I cambiamenti non diventano persistenti tra le chiamate.

--------------------------------------------------

Sorgente: https://github.com/checksound/my-blog/blob/master/db.json

## ESEMPIO

[user 1](http://my-json-server.typicode.com/checksound/my-blog/users/1)

[commenti del post 1](http://my-json-server.typicode.com/checksound/my-blog/posts/1/comments)

### ELENCO POSTS

Richiesta:
```bash
curl -i -H "Accept:application/json" 
        -H "Content-Type:application/json" 
        -XGET "my-json-server.typicode.com/checksound/my-blog/posts"
```

Risposta:
```
HTTP/1.1 200 OK
Date: Wed, 08 Apr 2020 16:08:56 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 213
Set-Cookie: __cfduid=dd35f9d8791e28f9c19591b8bc5ac7cf11586362136; expires=Fri, 08-May-20 16:08:56 GMT; path=/; domain=.typicode.com; HttpOnly; SameSite=Lax
X-Powered-By: Express
Vary: Origin, Accept-Encoding
Access-Control-Allow-Credentials: true
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
X-Content-Type-Options: nosniff
ETag: W/"d5-Z4GVI93+NqaIxL6s73ykiOrj4zs"
Via: 1.1 vegur
CF-Cache-Status: DYNAMIC
Server: cloudflare
CF-RAY: 580d3ff84a0cf917-MXP
Connection: keep-alive

[
  {
    "id": 1,
    "title": "hello",
    "userId": 1
  },
  {
    "id": 2,
    "title": "La bella lava il fosso",
    "userId": 1
  },
  {
    "id": 3,
    "title": "hello from Samarate",
    "userId": 2
  }
]
```

### AGGIUNTA DI UN NUOVO POST

Richiesta:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XPOST "my-json-server.typicode.com/checksound/my-blog/posts" 
    -d '{"title":"Tom e Jerry", "userId": 1}'
```

Risposta:
```
HTTP/1.1 201 Created
Date: Wed, 08 Apr 2020 16:11:37 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 54
Set-Cookie: __cfduid=dd0bd1ace8ab4dcb852d8cf65aae9fcac1586362296; expires=Fri, 08-May-20 16:11:36 GMT; path=/; domain=.typicode.com; HttpOnly; SameSite=Lax
X-Powered-By: Express
Vary: Origin, X-HTTP-Method-Override, Accept-Encoding
Access-Control-Allow-Credentials: true
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
Access-Control-Expose-Headers: Location
Location: http://my-json-server.typicode.com/checksound/my-blog/posts/4
X-Content-Type-Options: nosniff
ETag: W/"36-ufqa60olxFpavelfjDJA+Nh1rzk"
Via: 1.1 vegur
CF-Cache-Status: DYNAMIC
Server: cloudflare
CF-RAY: 580d43e28dd6f913-MXP
Connection: keep-alive

{
  "title": "Tom e Jerry",
  "userId": 1,
  "id": 4
}
```

### MODIFICA DEL POST 1

Richiesta:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XPATCH "my-json-server.typicode.com/checksound/my-blog/posts/1" 
    -d '{"title":"Sleep"}'
```

Risposta:
```
HTTP/1.1 200 OK
Date: Wed, 08 Apr 2020 16:14:08 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 48
Connection: keep-alive
Set-Cookie: __cfduid=d925c5bb39ce241a6763bbe4ea1d624a41586362448; expires=Fri, 08-May-20 16:14:08 GMT; path=/; domain=.typicode.com; HttpOnly; SameSite=Lax
X-Powered-By: Express
Vary: Origin, Accept-Encoding
Access-Control-Allow-Credentials: true
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
X-Content-Type-Options: nosniff
Etag: W/"30-N/v/NEiJ2++x0WSFu0XYIcRe0eY"
Via: 1.1 vegur
CF-Cache-Status: DYNAMIC
Server: cloudflare
CF-RAY: 580d4795a8e2e8eb-MXP

{
  "id": 1,
  "title": "Sleep",
  "userId": 1
}
```

### AGGIUNTA DI UN COMMENTO AL POST 1

Richiesta:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XPOST "my-json-server.typicode.com/checksound/my-blog/posts/1/comments" 
    -d '{"body":"Terribile!!!"}'
```

Risposta:
```
HTTP/1.1 201 Created
Date: Wed, 08 Apr 2020 16:23:26 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 56
Set-Cookie: __cfduid=d37c77e89a44a780cb5d4edf3e65ba9341586363006; expires=Fri, 08-May-20 16:23:26 GMT; path=/; domain=.typicode.com; HttpOnly; SameSite=Lax
X-Powered-By: Express
Vary: Origin, X-HTTP-Method-Override, Accept-Encoding
Access-Control-Allow-Credentials: true
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
Access-Control-Expose-Headers: Location
Location: http://my-json-server.typicode.com/checksound/my-blog/posts/1/comments/3
X-Content-Type-Options: nosniff
ETag: W/"38-qObiDF5v4gxwmosFM6GlUIacOV8"
Via: 1.1 vegur
CF-Cache-Status: DYNAMIC
Server: cloudflare
CF-RAY: 580d55338b73431a-MXP
Connection: keep-alive

{
  "body": "Terribile!!!",
  "postId": "1",
  "id": 3
}
```

### CANCELLAZIONE DEL POST 1

Richiesta:
```bash
 curl -i -H "Accept:application/json" 
        -H "Content-Type:application/json" 
        -XDELETE "my-json-server.typicode.com/checksound/my-blog/posts/1"
 ```

Risposta:
```
HTTP/1.1 200 OK
Date: Wed, 08 Apr 2020 16:26:05 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 2
Set-Cookie: __cfduid=d259af6a2b18360a7a269bcb62dd3f4861586363165; expires=Fri, 08-May-20 16:26:05 GMT; path=/; domain=.typicode.com; HttpOnly; SameSite=Lax
X-Powered-By: Express
Vary: Origin, Accept-Encoding
Access-Control-Allow-Credentials: true
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
X-Content-Type-Options: nosniff
ETag: W/"2-vyGp6PvFo4RvsFtPoIWeCReyIC8"
Via: 1.1 vegur
CF-Cache-Status: DYNAMIC
Server: cloudflare
CF-RAY: 580d5916fe71e907-MXP
Connection: keep-alive

{}
```

Nel caso volessimo cancella un post che non esiste, ad esempio il post con id *8*.

Request:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XDELETE "my-json-server.typicode.com/checksound/my-blog/posts/8"
```


```
HTTP/1.1 404 Not Found
Date: Wed, 08 Apr 2020 16:32:06 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 2
Set-Cookie: __cfduid=dab4b28cfba19ef64fc7f1368301894de1586363526; expires=Fri, 08-May-20 16:32:06 GMT; path=/; domain=.typicode.com; HttpOnly; SameSite=Lax
X-Powered-By: Express
Vary: Origin, Accept-Encoding
Access-Control-Allow-Credentials: true
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
X-Content-Type-Options: nosniff
ETag: W/"2-vyGp6PvFo4RvsFtPoIWeCReyIC8"
Via: 1.1 vegur
CF-Cache-Status: DYNAMIC
Server: cloudflare
CF-RAY: 580d61e99efabe64-MXP
Connection: keep-alive

{}
```