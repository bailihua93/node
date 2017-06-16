###安装koa

```
# 初始化package.json
npm init
# 安装koa2 
npm install koa
```

###hello world

```js
//index.js
const Koa = require("koa");
const app = new Koa();

app.use(async(ctx)=>{
    ctx.body = 'hello koa2'
});

app.listen(3000);

console.log('[demo] start-quick is starting at port 3000');
```
由于koa2是基于async/await操作中间件，目前node.js 7.x的harmony模式下才能使用，所以启动的时的脚本如下：
```js
node index.js
```