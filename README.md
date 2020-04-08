# TRY JsonPlaceholder

Partendo dal servizio https://jsonplaceholder.typicode.com/ [My JSON Server](https://my-json-server.typicode.com/).

[users](http://my-json-server.typicode.com/checksound/my-blog/users)

[user 1](http://my-json-server.typicode.com/checksound/my-blog/users/1)

[posts](http://my-json-server.typicode.com/checksound/my-blog/posts)

[comments](http://my-json-server.typicode.com/checksound/my-blog/comments)

[commenti del post 1](http://my-json-server.typicode.com/checksound/my-blog/posts/1/comments)

[db](http://my-json-server.typicode.com/checksound/my-blog/db)

You can use GET, POST, PUT, PATCH and DELETE. Changes aren't persisted between calls.

## ESEMPIO

`GET` my-json-server.typicode.com/checksound/my-blog/posts/1

```bash
curl -i -H "Accept:application/json" -H "Content-Type:application/json" -XGET "my-json-server.typicode.com/checksound/my-blog/posts"
```

```bash
curl -i -H "Accept:application/json" -H "Content-Type:application/json" -XPOST "my-json-server.typicode.com/checksound/my-blog/posts" -d '{"title":"La bella lava il fosso"}'
```




