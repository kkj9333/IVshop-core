# IVshop-core
###  IVshop -minecraft的物品交易所
0.引言
IVshop是一款以inventorymenu作为UI的bds服务端商店插件，功能非常强大。
其以假数据包作为交互载体，调用玩家的背包UI，并提供商店的操作界面，相比传统表单UI，不仅更加简洁直观，而且反应速度更快，操作更便捷！电脑端只需鼠标点击即可完成各种操作，win10玩家福利！
查询操作多线程优化，实验测试表明上万商品查询只需0.3s！且不干涉bds主线程。
支持购买和回收功能，也支持玩家出售和全物品回收委托功能！！！
内含丰富的操作设置，实现了商品筛选，搜索，批量补货，折扣等功能，从不同角度满足不同玩家的需求！
同时插件支持多种语言（中文/英文），甚至可以自行扩展语言翻译！

关键词：多功能商店，背包UI，多线程优化，多语言

下面将从几个方面来介绍这款插件：
1.主菜单
指令：/ivshop (mainmenu)
这里是插件的中心入口处，可以前面购买，回收，我的商店界面，这里会提供插件的交互操作帮助。
 
关于操作功能区域划分
玩家背包的热键部分（最底下一行）被定义为操作功能区，一般包含各种操作；
玩家背包的背包部分（中间三行）被定义为商品展示区，商品会在这里展示；
玩家背包的装备部分（左上角四格）被定义为菜单选项区，一般是调整设置和一些跳转操作；
玩家背包的副手部分（副手）是特殊功能区，一般是返回上级菜单所用。
2.我的商店
指令：/ivshop myshop
这里可以进行对商店的各种操作。
1.	可以进行商店信息编辑，编辑自己商店名称，介绍，商店图标等信息，op可以设置成op商店。
2.	可以浏览自己商店出售的商品，并进行编辑，补货，下架操作，可以上架新商品，可以发布折扣（可限定时长）。可以设置商品私有化（商品无法被搜索到）。
 
商店信息编辑
商店的信息可以进行编辑，用于对商店的描述，商店的默认信息会在第一次打开商店时自动生成，点击商店头像即可进行进一步编辑。玩家可以编辑商店名称，描述，商店图标，op可以设置该商店为OP商店。
 
 
商店交易记录
Ivshop提供商店日志记录，玩家可以查阅自己的商店交易记录日志。
 
###出售部分###
上架新商品
玩家可以上传物品作为出售商品，出售商品会出现在出售商店界面中。
点击上架按钮跳转到上架界面，此时会还原成你的背包UI，可以选中一个物品进行上架。本插件十分人性化，物品上架时会根据上传物品信息自动填入相关商品信息，一般情况下您只需要输入单个售价即可。
 
 
商品调整
您可以在商品展示区调整自己的商品信息，请注意调整数量会将多余的物品返还到您的背包里，调整数量为0时，一旦提交，该商品将被下架！
 
 
商品补货
不同于商店插件，本插件的出售时以商品为单元，因此如同大多数电商平台一样，即使物品被销售一空，只要商店主人不下架该商品，商品依旧存在，因此可以实现对商品的补货操作。
操作流程非常简单，只需点击补货按钮，然后系统会自动计算你可以进行补货的物品，你只需要选择自己想要上传的物品并点击提交即可。
 
 
 
发布折扣
您可以对自己商店的物品发布折扣，这个折扣作用范围是根据上架商品时输入的物品标签决定的，您也可以随时更改此标签。折扣分为两种，一种是直减，一种是百分比折扣，折扣存在时间长度限制，以发布折扣的时间戳作为起点，当到达规定时长后，折扣将被删除。
 
 
计分板离线经济获取
同时对于计分板经济模式，点击商店日志记录按钮也可获得玩家不在线时商店经营所获得的钱！
 
切换至回收商店
玩家可以从出售商店切换到自己的回收商店，只需点击切换按钮即可。
 
###回收部分###
 
物品委托
玩家可以花费一定金钱来进行物品委托，委托物品会出现在回收商店界面中。
点击发布回收委托按钮，此时会还原成自己的背包，选择你想要进行委托的物品，点击后跳转到委托编辑界面，您可以设置您的委托物品名称，委托描述，委托数量，委托出价，以及一些筛选设置（包含筛选特殊值耐久值，筛选附魔，筛选nbt等）。
您也可以进行全物品委托。此概念是指您从所有（包含未用有）的物品中发布委托，实现委托物品自由这也是本插件超脱其他同类插件的地方之一。
在进行全物品委托前你需要关闭物品合成按钮（创造模式无需），然后点击发布委托按钮，此时会多出一个新的按钮，点击后可以从所有物品中选择物品发布回收委托。
在编辑后你的委托后，点击提交，如金钱足够，委托即可申请成功。
op玩家创建委托时不需要金钱。
 
 
 
取出物品
回收委托建立后，回收物品展示区会出现你的委托物品，如果已经回收了一部分物品，你可以点击取出按钮，选择相应的委托物品来完成取货操作。
 
 
委托更改
Ivshop允许玩家随时更改自己的委托，重新设置委托的信息。
只需在商品展示区点击对应物品即可。两次委托的差价会被返回或收取。
切换至出售商店
玩家可以从回收商店切换到自己的出售商店，只需点击切换按钮即可。
 
3.购买菜单
指令1：/ivshop buy 全局
指令2：/ivshop buybyshop 按玩家显示商店
这里可以进行商品购买操作。
 
购买商品
点击商品展示区的物品进行购买，并提交相应购买信息即可。
 
筛选商店
点击按钮即可按玩家商店筛选并显示商店。
 
4.回收菜单
指令1：/ivshop reclcle全局
指令2：/ivshop rebyshop 按玩家显示回收商店

 
回收物品
点击商品展示区一个物品来进行回收操作，系统会根据委托自动筛选你可以回收槽和数量，选择你要进行回收的物品进行回收即可。
 
 
筛选商店
功能类似，不再赘述。
5.筛选器和商品搜索
筛选器
指令：/ivshop filter
Ivshop提供了商品检索筛选功能，可以筛选商品的一些属性，如果筛选器不为默认值，玩家所有的搜寻过程都会启用筛选器并使用其对商品进行筛选。筛选器只在服务器运行期间有效。
 
商品搜索
指令： /ivshop search [searchtype] (filterstring) (checkshopitemtag) (checkshopitemdesc)
Ivshop支持对商品进行简单检索功能，可以从商店检索商品
 
此功能计划作为表单gui并会加入到购买菜单和回收菜单界面的功能区中，可以点击即可进行搜索。
 
6.辅助功能
快捷翻页
商店物品超过一定数量时会进行分页，玩家只需点击即可进行翻页。
 
PE辅助-只读模式
为手机版玩家设计的辅助阅读器，可以实现只读化阅读商品信息，防误触。
 
计分板离线经济获取
指令：/ivshop getoffscores
获取离线的计分板金钱，效果通我的商店里的计分板离线经济获取。
7.配置文件
配置文件会自动生成在插件同级的ivshop目录里。现作简单说明：
Moneymode 经济运行模式，默认为0 计分板。设置为1时启用LLmoney经济。
Tax 税率 玩家交易时会收取税 默认为0。 值域0-100。
Moneyname 启用计分板经济时的对接计分板名称，默认为money。
8.关于
op商店和op
在ivshop中，op商店可以无限出售和回收商品，同时出售的金钱不会转移到主人，回收的物品不会被保存。
op建立回收委托时不需要花费金钱。
可能存在遗漏的特性以后说明。
插件作者
插件唯一作者为starkc。
ivshop交流群：379178988。
预计加入功能
目前还有尚未完善的功能，如商店设置点击无效是因为此功能还在开发中（不一定成品是这个功能）；
预计还需加入的功能有：功能区内置物品检索，自动更新检测
。。。
9.存在问题
目前插件存在一些特性：
在背包UI的热键内的物品为你背包内的真实物品（上传物品操作）时，其可以被丢出，但是假数据包发送的假物品不能被丢出；
在背包UI操作时，物品变更会更新显示的背包UI甚至会导致整个背包UI刷新。
由于LL表单的问题，滑块显示上限总是比最小大于1，这样就会导致一些数量上的调整错误，不过我在内部做了处理，实际数量不会出错。
这些特性虽然无伤大雅，但是视觉效果不好，如果能够解决会尽量解决。使用中如发现其他问题可以在交流群找作者反馈。


