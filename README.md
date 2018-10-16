# Netflix

> A Netflix emulator

## Github Address
[https://github.com/NetflixCTO/Netflix](https://github.com/NetflixCTO/Netflix)

## Build Setup

``` bash
# install dependencies
npm install

# before start
make sure you have installed mongodb and the service is running

Then modify the content on server/config/index.js

And then src/common/js/mixin.js
Modify the default link under the addBase method

Then you can start

# server with hot reload at localhost:3333
npm start

# build
make sure install parcel in gobal
npm run build

# test after build
npm run exec
```

## Showcase
### Frontend
[FrontPage][1]

[PlayPage][1]

admin：admin@qq.com
password: 123456

**add movie attention**
The video and poster addresses need to be http/https protocol and do not support ed2k.

for example:

poster address：
https://img1.doubanio.com/view/photo/l_ratio_poster/public/p2519994468.webp

video address:
http://vt1.doubanio.com/201805241616/ca24dfd1d36cc84406e361b2c8a90d23/view/movie/M/402300311.mp4


## Screenshots
### FrontPage
![此处输入图片的描述][4]
### Detail
![此处输入图片的描述][5]


## Structure
```
    .
├── server                                      // back-end server
|   ├── config                                  // user configuration
|   ├── crawler                                 // crawler script
|       └── trailer-list                        // movie information crawler
|       └── video                               // video and poster crawler
|   ├── database                                // database correlation
|       └── schema                              // schema configuration
|       └── init                                // database initialization
|   ├── lib                                     // Toolkit
|       └── decorator                           // routing
|       └── util                                // common tool
|   ├── middlewares                             // Middleware
|       └── parcel                              // integrated parcel
|       └── common                              // general Middleware
|       └── router                              // routing Middleware
|   ├── routes                                  // back-end routing configuration
|       └── movie                               // request movie related API
|       └── user                                // background management related API
|   ├── service                                 // back-end services
|       └── movie                               // movie API related services
|       └── user                                // login service
|   ├── tasks                                   // process management
|       └── api                                 // request detailed data
|       └── movie                               // data crawler process
|       └── qiniu                               // upload static resource process
|       └── trailer                             // video poster crawler process
├── src                                         // front-end project core document
│   ├── base                                    // common components
|       └── no-result                           // no result component
│   ├── common                                  // public static resources
|       └── image                               // public picture
|       └── js                                  // public JS
|           └── mixin                           // mixin
│   ├── components                              // component
|       └── home                                // home page
|       └── home-content                        // The main content of home
|       └── login                               // login page
|       └── management                          // backend management page
|       └── movie-detail                        // movie details page
|       └── player                              // video player
|       └── toolbar                             // head and left navigation
|   ├── router                                  // front-end routing
|   ├── store                                   // vuex
|       └── index                               // store入口
│   ├── App.vue                                 // component access
│   ├── main.js                                 // front-end entry file
├── index.html                                  // template HTML file
├── start.js                                    // project entry file
.

```


  [1]: https://daxiv.com/
  [2]: https://daxiv.com/detail/5bc28a71f758a50006137653
  [3]: https://ws1.sinaimg.cn/large/e8323205gy1frmi81dy3fj20qe0ftq3n.jpg
  [4]: https://ws1.sinaimg.cn/large/e8323205gy1frmj7tnjjmj213v0jn13t.jpg
  [5]: https://ws1.sinaimg.cn/large/e8323205gy1frmj82b4amj213t0joaht.jpg
  [6]: https://ws1.sinaimg.cn/large/e8323205gy1frmj7wcfp8j21400jnq3k.jpg
  [7]: https://ws1.sinaimg.cn/large/e8323205gy1frmj804qquj213w0jngpy.jpg
