某某阁小说app接口抓包分析
<!-- more -->

### 配置获取

```js
  // 此接口返回host地址和一些广告配置，广告用不上忽略即可
  // host 地址包含小说图片的host和小说目录内容等的host
  // 如下面接口中的 https://scxs.pysmei.com 和 https://imgapixs.pysmei.com

  https://sdk.qzbonline.com/ver9/shuhuajs/sdk/ioszh_shuhuajs_conf.html
  https://sdk.qzbonline.com/prov8/ymqxs/sdk/ios_ymqxs_conf.html
  https://sdk.qzbonline.com/prov8/ymqxs/sdk/ios_ymqxs_conf2.html
  https://sdk.qzbonline.com/prov8/fqhyxs/sdk/ioszh_fqhyxs_conf_jh.html
  https://sdk.qzbonline.com/ver9/shuhuajs/sdk/ioszh_shuhuajs_conf.htm
```

### 小说首页

```js

  // {sex} 可取值 man、lady

  https://scxs.pysmei.com/ver9/base/fq/scxs_{sex}.html
  https://scxs.pysmei.com/prov8/base/{sex}_fqhyxs.html
  https://scxs.pysmei.com/prov8/base/{sex}.html
  https://scxs.pysmei.com/prov8/base/{sex}2.html
```

### 轮播图

```js
  // {sex} 可取值 man、lady
  https://scxs.pysmei.com/prov8/base/banner_{sex}.html

```

### 所有分类

```js
  https://scxs.pysmei.com/Categories/BookCategory.html
```

### 分类排行榜

```js
  // 此处{id}为所有分类接口获取的分类id
  // {type}取值为 hot 热门、 new 新书、 over 完本、 vote 榜单、 collect 收藏、 commend 推荐
  // {page} 搜索结果页码，从1开始

  https://scxs.pysmei.com/Categories/{id}/{type}/{page}.html
```

### 书单列表

```js
  // {sex} 可取值 man、lady
  // {type}取值为 hot 热门、 new 新书、 over 完本、 vote 榜单、 collect 收藏、 commend 推荐
  // {page} 搜索结果页码，从1开始

  https://scxs.pysmei.com/shudan/{sex}/all/{type}/{page}.html
```

### 书单详情

```js
  // {id}为书单列表接口返回的书单id
  https://infosxs.pysmei.com/shudan/detail/{id}.html
```

### 小说详情

```js
  // {id} 小说id，比较特殊，举例说明
  // 接口返回id为 122001，则此处的{id}为 id前三位 + 1 即 122 + 1 = 123，然后拼接 ‘/’ ，加上小说的id，
  // 则此处的{id}为  123/122001
  // 如果接口返回的小说的id小于等于 3位数，如 122，则 / 前端数字统一为 1
  // 则此处的{id}为 1/122

  https://infosxs.pysmei.com/BookFiles/Html/{id}/info.html
```

### 小说图片

```js
  // {id} 图片id，小说详情接口中返回
  https://imgapixs.pysmei.com//BookFiles/BookImages/{id}
```

### 小说目录

```js
  // 此处的{id} 同详情的{id}

  https://infosxs.pysmei.com/BookFiles/Html/{id}/index.html
```

### 小说搜索

```js
  // {sw} 搜索词
  // {page} 搜索结果页码，从1开始

  https://souxs.leeyegy.com/search.aspx?key={sw}&page={page}&siteid=app2
```

### 热搜列表

```js
  https://scxs.pysmei.com//StaticFiles/NewHotBook.html
```
