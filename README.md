# html5-通知信息
###之前的一些老方案：
       1）浏览器定时器刷新title或则界面内容
       2）后台推动前台试试显示

###关键技术
window.Notification


###支持情况
   pc端支持好些，移动端支持较差，具体情况请google
   
   
###调用语法
  一、调用方式：
   1）链式：Notification.requestPermission().then(function(permission) { ... });
   2）回调模式：Notification.requestPermission(callback);
 二、回调处理方式
     通知信息处理方式：new Notification(title, options)
     title表示标题 
     options为其他参数，具体如下：
       |---|---|
       |属性名	|释义|
       |dir	|默认值是auto, 可以是ltr或rtl，有点类似direction属性。表示提示主体内容的水平书写顺序。|
       |lang	|提示的语言。没看出来有什么用。大家可以忽略之~|
       |body	|提示主体内容。字符串。会在标题的下面显示。|
       |tag	|字符串。标记当前通知的标签。|
       |icon	|字符串。通知面板左侧那个图标地址。|
       |data	|任意类型和通知相关联的数据。|
       |vibrate|	通知显示时候，设备震动硬件需要的振动模式。所谓振动模式，指的是一个描述交替时间的数组，分别表示振动和不振动的毫秒||数，一直交替下去。例如[200, 100, 200]表示设备振动200毫秒，然后停止100毫秒，再振动200毫秒。|
       |renotify	|布尔值。新通知出现的时候是否替换之前的。如果设为true，则表示替换，表示当前标记的通知只会出现一个。注意都这里“当|前标记”没？没错，true参数要想其作用，必须tag需要设置属性值。|
       |silent	|布尔值。通知出现的时候，是否要有声音。默认false, 表示无声。|
       |sound	|字符串。音频地址。表示通知出现要播放的声音资源。|
       |noscreen|	布尔值。是否不再屏幕上显示通知信息。默认false, 表示要在屏幕上显示通知内容。显示桌面通知|
       |sticky	|布尔值。是否通知具有粘性，这样用户不太容易清除通知。默认false,| |表示没有粘性。根据我自己的猜测，应该和position的sticky属性值类似。|
       
### 注意事项
    需要在http协议下使用，file://貌似不行
     


