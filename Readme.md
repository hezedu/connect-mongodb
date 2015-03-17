#autoDestroy
[原作](https://github.com/treygriffith/connect-mongodb)在没有设maxAge的情况下，session数据不会自动销毁。

我增加了个autoDestroy选项，现在可以了。
##npm
`npm install connect-mongodb-autodestroy`

##例：
```javascript
    store: new MongoStore({
        url: "mongodb://" + conf.mongodb.host + ':' + conf.mongodb.port + '/' + conf.mongodb.db,
        username: conf.mongodb.username,
        password: conf.mongodb.password,
        collection: conf.mongodb.session_C,
        reapInterval: 1000 * 60 * 60 * 12,
        autoDestroy: 1000 * 60 * 60 * 24 * 2  // 新增项。
    }),
```
