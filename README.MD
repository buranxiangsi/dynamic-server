```js
    const fs = require("fs")
    //结构：一个数组
    //读数据库
    const usersString = fs.readFileSync("/users.json").toString()
    const usersArray = JSON.parse(usersString) //反序列化得到数组

    //写数据库
    const user3 = {id: 3, name: 'tom', password: 'yyy'}
    usersArray.push(user3)
    const string = JSON.stringify(usersArray) //序列化，得到字符串
    fs.writeFileSync('./db/users.json', string) //写入字符串
```
