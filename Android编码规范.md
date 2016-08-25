##基本要求
* 除了注释，代码中不出现中文
* 每个类都需要写上作者、时间，重要的类要写生相应的注释
* 重要的方法要加上相应的注释说明，方便以后维护

##命名
**大驼峰命名：每个单词的第一个字母都需要大写**

**小驼峰命名：除了第一个单词外，每一个单词的第一个字母大写**

**命名的基本原则**
* 不使用汉语拼音
* 除了常见的英文缩写，尽量少使用缩写
* 名称不宜过长


###1. 包命名
* 小写字母
* 连续的单词直接连接起来，不使用下划线

###2. Java类命名
* 大驼峰命名 UserListAdapter；
* 除常见的缩写单词以外，不使用缩写，缩写的单词每个字母都大写 RequesURLList；
* 公共的工具类建议以 Utils、 Manager 为后缀，如 LogUtils；
* activity 命名以Activity结尾，例如 MainActivity;
* fragment 命名以 Fragment 结尾，例如 ChatFragment;
* adapter 命名以 Adapter 结尾，例如 EventItemAdapter;

###3. 变量命名
* 成员变量命名
  - 小驼峰命名
  - 类级别成员变量使用`m`开头， 静态变量使用`s`开头
  - 方法变量，不使用`m`编码风格
* 常量命名
  - 单词每个字母都大写
  - 单词之间下划线连接
* 控件变量命名
  - 小驼峰命名
  - 适用上面的`m`规则
  - 对应的控件id的命名`空间缩写_逻辑名称`，单词均小写，用下划线连接，例如：`tv_post_title`
  - 常见的控件缩写如下：
  

    控件 | 缩写
    ------------ | -------------
    Linearlayout |	ll
    RelativeLayout |	rl
    TextView |	tv
    EditText	| et
    Button |	btn
    ImageView |	iv
    CheckBox |	chb
    ListView |	lv
    GridView |	gv
    RadioButton |	rb

* 方法命名
  - 小驼峰命名
  - Getter 和 Setter 方法，推荐使用自动生成的，写起来也很方便
  - 方法名应当保证见名知义的原则
  
* 布局文件命名
  - activity、fragment 布局文件名以对应的类别名称为前缀，逻辑名称放在其后，以下划线连接，例如 activity_home、fragment_chat_list，方便查找；
  - ListView、GridView 的 item 布局文件建议以 list_item、gird_item为前缀，加上对应的逻辑名称，例如 list_item_post、grid_item_photo；
  - Dialog的布局文件以 dialog 为前缀，逻辑名称放在其后，下划线连接，例如 dialog_warnning;
  - 包含项布局命名以 include 开头，在加上对应的逻辑名称，例如 include_foot
  - 控件的 id 命名参见控件变量命名；

* 资源命名
  - 图标资源以 ic 为前缀，例如 ic_chat ，指聊天图标；
  - 背景图片以 bg 为前缀，例如 bg_login ，指的是登录页的背景图；
  - 按钮图片以 btn 为前缀，例如 btn_login ，指的是登录按钮的图片，不过这只有一种状态，需要加上状态的可以在后面添加，例如 btn_login_pressed ，表示登录按钮按下的图片；
  - 当使用 shape 和 selector 文件为背景或者按钮时，命名参照以上说明；

