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

### AGGIUNTA DI UN NUOVO POST

Richiesta:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XPOST "my-json-server.typicode.com/checksound/my-blog/posts" 
    -d '{"title":"Tom e Jerry", "userId": 1}'
```

Risposta:

### MODIFICA DEL POST 1

Richiesta:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XPATCH "my-json-server.typicode.com/checksound/my-blog/posts/1" 
    -d '{"title":"Sleep"}'
```

Risposta:

### AGGIUNTA DI UN COMMENTO AL POST 1

Richiesta:
```bash
curl -i -H "Accept:application/json" 
    -H "Content-Type:application/json" 
    -XPOST "my-json-server.typicode.com/checksound/my-blog/posts/1/comments" 
    -d '{"body":"Terribile!!!"}'
```

Risposta:

### CANCELLAZIONE DEL POST 1

Richiesta:
```bash
 curl -i -H "Accept:application/json" 
        -H "Content-Type:application/json" 
        -XDELETE "my-json-server.typicode.com/checksound/my-blog/posts/1"
 ```

Risposta:
