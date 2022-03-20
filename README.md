# markdown - 更简洁、更高效
###  本文档来源于HBuilderX的Markdown语法帮助文档
=================================================

强烈建议开发者认真阅读本文档，掌握md及HBuilderX对md的强大支持。
_窄屏幕下，可按Alt+滚轮横向滚动_

很多人只把markdown用于网络文章发表，这糟蹋了markdown。
markdown不止是HTML的简化版，更重要的是txt的升级版、word的轻量版、笔记的最佳载体。
作为一种简单的格式标记语言，不同于txt的无格式，不同于HTML的复杂标记，也不同于word的鼠标调整样式。markdown通过简单的几个字符键入，就可以快捷的定义文档的样式。
比如在行首敲一个“#”，就把这行定义为了1级标题，并且在HBuilderX里有直观完善的着色，这样无需发布为web页面，可直接当word用。
掌握markdown，你可以完全抛弃txt和笔记软件的编辑器，并且在大多数场景下替代掉复杂臃肿的word。享受简洁之美、享受效率提升。
而HBuilderX，可以被称为最强大的markdown书写工具了。

下面的示例列举了markdown语法及对应的HBuilderX使用技巧：

开始前，可以先按下文档结构图的快捷键Alt+w（Mac是Ctrl+w），浏览本文的大纲。

# 标题语法
markdown的标题是行首以#号开头，空格分割的，不同级别的标题，在HX里着色也不同。如下：
# 标题1
## 标题2
### 标题3
#### 标题4
##### 标题5
###### 标题6

标题使用技巧：
1. Emmet快速输入：敲h2+Tab即可生成二级标题【同HTML里的emmet写法，不止标题，HX里所有可对应tag的markdown语法均支持emmet写法】。仅行首生效
2. 智能双击：双击#号可选中整个标题段落
3. 智能回车：行尾回车或行中Ctrl+Enter强制换行后会自动在下一行补#。而连续2次回车后将自动补的#去掉。(体验同word)
4. 回车后再次按Tab可递进一层标题，再按Tab切换列表符
5. 在# 后回车，可上插一个空标题行【同word】，或任意位置按Ctrl+Shift+Enter也可以上插空标题行
6. 折叠：
	- 点标题前的-号可折叠该标题段落，快捷键是Alt+-（展开折叠是Alt+=）
	- 多层折叠时折叠或展开子节点，快捷键是Alt+Shift+-或=
	- 全文全部折叠或展开，快捷键是Ctrl+Alt+Shift+-或=
	- 折叠其他区域，快捷键是Alt+Shift+o。这对长文档管理非常有用，可以专注于当前章节
	- 可以在菜单-跳转-折叠中随时找到这些功能

# 列表
markdown的列表支持有序列表、无序列表以及特殊的任务列表。
同样也是在行前加一个特殊符号，并空格后再跟列表文字内容。

## 有序列表
有序列表就是有顺序的列表，依靠行前的数字标记顺序。
1. 有序列表1 【设置或取消有序列表符的快捷键：Ctrl+Alt+1，可选中多行批量设置序号；支持多光标批量设置列表符，即按Ctrl+鼠标左键添加多光标】
2. 有序列表2 【列表后回车会自动补序号】
4. 有序列表3 【智能双击：双击前面的数字，可重新对数字排序，修正序号错误，并选中有序列表段落（左边的4是故意写错让你体验的）】

## 无序列表
无序列表就是列表不排序，无序列表因书写随意而被更广泛的使用。
无序列表有3种前缀，HX里分别用于表示1级列表、2级列表、3级列表。
- 无序列表1 【快捷键：Ctrl+Alt+-；智能双击：双击-号可选中整段无序列表；再次按Tab会更换二级列表符】
* 无序列表2	
	* Emmet：li后敲Tab可生成*号列表符，行首生效
	* 快捷键：Ctrl+Alt+8【8即*对应的数字】，支持多光标批量设置列表符，即按Ctrl+鼠标左键添加多光标
	* 智能双击：双击*号可选中整段无序列表
	* 智能回车：行尾回车或行中Ctrl+Enter强制换行后会自动续列表；连续按回车会清除列表符；再次按Tab会更换列表符；在列表符后回车或行尾Shift+回车，上一行留出列表符
	* *号常用于二级列表，列表符后继续Tab，可切换列表符
+ 无序列表3 【快捷键：Ctrl+Alt+=；常用于三级列表；其他同上】

## 任务列表
任务列表非常实用，管理待办、已办非常便利。
[ ] 任务列表-未完成任务 【快捷键：Ctrl+Alt+[】
[x] 任务列表-已完成任务 【快捷键：Ctrl+Alt+]】
	1. 智能双击：双击方括号内可切换勾选状态，把任务标记为完成或未完成；双击方括号右侧可选中任务列表段落
	2. 智能回车：回车后自动补任务列表前缀符号；连续按回车清除前缀符号；在列表符后回车或行尾Shift+回车，上一行留出列表符
- [ ] 如需发布到web渲染，需增加无序列表- 的前缀

以上三种列表，均支持批量修改列表符，有如下方式建议依次学习尝试：
1. 选中多行，按快捷键Ctrl+Alt+“1”或“-”或“[”或“]”，批量设置列表符
2. 如果需要跳行设置有序或无序列表，通过Ctrl+鼠标左键点中目标多行（可不连续），产生多光标，然后按快捷键Ctrl+Alt+“1”或“-”或“[”或“]”，可跳行设置列表符，尤其是有序列表，数字也会跳行加1
3. 按Alt+鼠标选中行首那列（列选择），这样每行行首都有光标，然后再键入或删除列表符即可批量操作
4. 选中多行，按快捷键Ctrl+Shift+\（其实就是Ctrl+|），可以在每行行首添加一个光标

## 引用列表
> 引用1
> 引用2
快捷键：Ctrl+Alt+Shift+.
智能双击：双击>号可选中整段引用列表
智能回车：行尾回车或行中Ctrl+Enter强制换行后会自动续列表；连续按回车会清除列表符；在列表符后回车或行尾Shift+回车，上一行留出列表符

# 文字样式语法
**加粗** 【快捷键：Ctrl+B，支持多光标；Emmet：b后敲Tab】
__加粗2__
_倾斜_【Emmet：i后敲Tab；前后包围：选中文字按Ctrl+\是在选区两侧添加光标，可以继续输入_】
*倾斜*
~~删除线~~
``` 单行代码 ```
包围插入：先选中文字内容，然后按_*~`等符号，会自动在2侧加包围
智能双击：双击语法区前面的定义符号，选中包含定义符的整段文字
去包围：选中整段文字后，按Ctrl+Shift+]，可去除2侧包围符号

引号括号虽然不属于markdown语法，但也支持相同的包围、选择、去包围操作。
引号括号智能双击选择时略特殊的是：双击引号括号内侧，选中引号括号里的内容(不含引号括号)；按下Alt+双击引号括号内侧，则选中包含符号的整段文字

HBuilderX还支持以下对2侧文本高效处理的手段
1. 选中文字按Ctrl+\是在选区两侧添加光标，可以继续输入~~，会在2侧同时输入
2. 向2侧扩大选择：【Win:Alt+Shit+→ 、Mac:Ctrl++Shit+→】；由2侧向内减少选择：【Win:Alt+Shit+← 、Mac:Ctrl++Shit+←】

[链接文字](http://dcloud.io)
1. Emmet：a后敲Tab
2. 打开链接：Alt+鼠标单击；如果是本地文件，可通过Shift+Alt+单击，在另一分栏打开文件
3. 智能粘贴：粘贴URL会自动变成超链接格式；粘贴本地文件进来也会自动创建引用链接
4. 智能双击：双击语法区开头，即[左侧，选中包含定义符的整段文字

![图片描述文字](logo.jpg)
1. Emmet：img后敲Tab
2. 智能粘贴：粘贴剪切板里的图形时会自动保存为本md文档的附件；删除文档中的图片语法，保存md文档时会自动删除对应的图片附件；粘贴图片文件时自动变成链接引用格式；
3. 悬浮预览：鼠标移到图片语法上，本地图片会自动显示出来
4. 智能双击：双击语法区开头，即!左侧，选中包含定义符的整段文字

# 表格 

|		|		|		|
|--	|--	|--	|
|		|		|		|
|		|		|		|

1. Emmet：table3*3后敲Tab，表示生成3行3列的表格，行首生效
2. md表格对齐是传统md的痛点，按下Ctrl+K可以自动整理表格格式（暂未兼容不同缩放模式和字体的情况）
3. 支持从excel、wps、word、number的表格中复制粘贴表格进来（不支持合并单元格和单元格换行）

# 分割线
------------- 【Emmet：hr后敲Tab】
*************
=============

# 代码区
``` javascript
	var a = document
```
Emmet：code后敲Tab，行首生效
智能双击：双击语法区开头，即!左侧，选中包含定义符的整段文字
支持代码直接高亮着色，这应该是只有HBuilderX才有的功能。注意需要在代码区开头指定语言类型

# 注释
<!--注释--> 
快捷键：Ctrl+/
智能双击：双击注释首尾的定义符，选中整段注释

# 其他emmet快捷输入
day后敲Tab，当前日期。注意day需在行首或前面有空格
time后敲Tab，当前时间。注意time需在行首或前面有空格

# 文档结构图
文章很长时，word里有文档结构图，HBuilderX也有。
菜单视图-文档结构图，快捷键Alt+W(mac是ctrl+W)，轻松管理长文档

# 运行、预览和打印PDF
对md文件点工具栏或菜单里的浏览器运行，可以使用外部浏览器预览此md文件，会自动渲染为HTML。
点右上角的预览【快捷键Alt+p】，可在HBuilderX右侧预览该md文档的HTML渲染结果。
在浏览器中点打印，选择打印到PDF，可将md输出为PDF格式。（注意在打印选项里去掉页眉页脚）

# 一键分享
markdown拥有迷人的输入体验，但分享并不方便，尤其是缺少免费、稳定、高速的图床。
[uniCloud](https://unicloud.dcloud.net.cn/)提供了免费、稳定、高速的服务器和cdn。
HBuilderX，基于uniCloud，提供了markdown的一键分享功能。

利用uniCloud的前端网页托管，将markdown稳定转成了HTML网页，并发布为在线的URL。您可以把URL发送给任何想要分享的人。
同时markdown里涉及的图片也会自动上传到前端网页托管里免费cdn中。

更多见: [MarkDown一键分享使用说明](https://ask.dcloud.net.cn/article/37573)

# 其他常用但你可能不知道的快捷操作技巧
- Ctrl+鼠标左键添加多光标，然后敲字或粘贴，可批量处理。Ctrl+鼠标左键拖选，可选中多个选区。
- Ctrl+鼠标右键删除多光标
- 不选内容按Ctrl+C或X可复制或剪切整行
- 选中2个选区后，按Ctrl+Shift+X，可互换选区内容。如无选区，只是2个光标，则互换2行
- Ctrl+上下键可上下移动行
- Ctrl+Insert可重复插入当前行，如果有选中内容，可重复插入选中内容
- Ctrl+Shift+K可合并多行（是格式化Ctrl+K的反操作）
- 删除
	* 按Ctrl+D可删除选中行，支持多光标
	* Shift+Del删除到行尾
	* Shift+Backspace删除到行首
- 选择
	* Ctrl+E选相同词(mac是Command+D)，连续按可选中多词进一步操作，比替换更方便
	* Ctrl+L可连选多行，Ctrl+Shift+L也是选择行，但不选行首尾的空白字符
	* Ctrl+=可逐级放大选区
	* 双击标题、列表符可选中相应段落
	* 双击英文引号、括号内侧，可选中内部内容
	* 双击缩进符，可选中同缩进段落
	* 双击连字符比如-或_，可选中相连的词，比如双击这里试试，uni-app
- 查找
	* Ctrl+P查找文件
	* Ctrl+Alt+F可在当前目录的所有文档中搜索指定关键字(mac是Command+Shift+f)
	* 选中文字按F3，查找下一个，Shift+F3找上一个
- 云同步：HBuilderX+markdown用于云同步笔记的技巧，请参考[http://ask.dcloud.net.cn/article/13097](http://ask.dcloud.net.cn/article/13097)

都学会了吗？
markdown语法其实很简单，认真学半小时就能掌握。
HBuilderX的极客操作则需要不停反复练习，熟练掌握这些技巧，你将成为高效极客！

