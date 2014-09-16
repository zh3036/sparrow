#bitchttpd

`bitchttpd` 是一个简单高效的http server，纯C语言开发，目前主要用在本人个人的网站。

###功能
* 支持目录的访问(自定义格式)
* 支持多线程（可配置工作线程数目）
* 支持sendfile, tcp_cock等高效操作
* 支持404， 500
* 支持304 not modified
* 支持异步的日志：
    * 支持零点自动切换日志文件
    * 完善清晰的格式
    * 多线程支持
* 支持epoll


###待续...
* bug:当目录下文件过大时，buf溢出问题
* 目录下输出的子目录和文件排序问题
*  close, clear , ev_unregister overlap some operations.

###note
* 2014-9-16: fix bug of image corrupt and segment err (http_code not init)
   
   
###粗略的性能测试(700请求，并发500，1G内存，1核cpu)

`毫无压力啊！！`对于本人用来托管博客文章之类的，妥妥的

`后续会有更高性能的测试和大文件的测试`

![性能](performance_test/性能测试1.PNG)
