# TRY JsonPlaceholder

Partendo dal servizio https://jsonplaceholder.typicode.com/ [My JSON Server](https://my-json-server.typicode.com/).

## ESEMPIO

`GET` my-json-server.typicode.com/checksound/my-blog/posts/1

```bash
curl -i -H "Accept:application/json" -H "Content-Type:application/json" -XGET "my-json-server.typicode.com/checksound/my-blog/posts"
```

```bash
curl -i -H "Accept:application/json" -H "Content-Type:application/json" -XPOST "my-json-server.typicode.com/checksound/my-blog/posts" -d '{"title":"La bella lava il fosso"}'
```




