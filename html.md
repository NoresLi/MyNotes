# HTML5与HTML4的区别
### HTML5中的语法改变
#### 内容类型（ContentType）
	首先，HTML5的文件扩展符与内容类型保持不变。也就是说，扩展符仍然为“.html”或者“.htm”,
	内容类型（ContentType）仍然为“text/html”。
#### DOCTYPE声明
	DOCTYPE声明是HTML文件中必不可少的，它位于文件第一行。在HTML4中，她的声明方法如下：
	<!DOCTYPE html PUBLIC "-// W3C// DTD XHTML 1.0 Transitional// EN""http:// www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
	在HTML 5中，刻意不使用版本声明，一份文档将会适用所有版本的HTML。HTML 5中的DOCTYPE声明方法（不区分大小写）如下：
	<!DOCTYPE html>
	
#### 指定字符编码
	在HTML 4中，使用meta元素的形式指定文件中的字符编码，如下所示：
	<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
	在HTML 5中，可以使用对<meta>元素直接追加charset属性的方式来指定字符编码，如下所示：
	<meta charset="UTF-8">
	两种方法都有效，可以继续使用前面一种方式（通过content元素的属性来指定），但是不能同时混合使用两种方式。
	从HTML 5开始，对于文件的字符编码推荐使用UTF-8。

### 新增的元素和废除的元素
#### 新增的结构元素
	在HTML 5中，新增以下与结构相关的元素。
	(1) section元素
	section元素表示页面中的一个内容区块，比如章节、页眉、页脚或页面中的其他部分。
	它可以与h1、h2、h3、h4、h5、h6等元素结合使用，标示文档结构。
	HTML 5中的代码示例：
	<section>...</section>
	HTML4中的代码示例：
	<div>...</div>
	
	(2) article元素
	article元素表示页面中的一块与上下文不相关的独立内容，譬如博客中的一篇文章或报纸中的一篇文章。
	HTML 5中的代码示例：
	<article>...</article>
	HTML4中的代码示例：
	<div>...</div>
	
	(3) aside元素
	aside元素表示article元素的内容之外的、与article元素的内容相关的辅助信息。
	HTML 5中的代码示例：
	<aside>...</aside>
	HTML4中的代码示例：
	<div>...</div>
	
	(4) header元素
	header元素表示页面中一个内容区块或整个页面的标题。
	HTML 5中的代码示例：
	<header>...</header>
	HTML4中的代码示例：
	<div>...</div>
	
	(5) footer元素
	footer元素表示整个页面或页面中一个内容区块的脚注。
	一般来说，它会包含创作者的姓名、创作日期以及创作者联系信息。
	HTML 5中的代码示例：
	<footer>...</footer>
	HTML4中的代码示例：
	<div>...</div>
	
	(6) nav元素
	nav元素表示页面中导航链接的部分。
	HTML 5中的代码示例：
	<nav>...</nav>
	HTML4中的代码示例：
	<div>...</div>
	
	(7) figure元素
	figure元素表示一段独立的流内容，一般表示文档主体流内容中的一个独立单元。
	使用figcaption元素为figure元素组添加标题。
	HTML 5中的代码示例：
	<figure>
	<figcaption>PRC</figcaption>
	<p>The People's Republic of China was born in 1949...</p>
	</figure>
	HTML4中的代码示例：
	<dl>
	<h1>PRC</h1>
	<p>The People's Republic of China was born in 1949...</p>
	</dl>
	
	(8) main元素
	main元素表示网页中的主要内容。
	主内容区域意指与网页标题或应用程序中本页面主要功能直接相关或进行扩展的内容。
	HTML 5中的代码示例：
	<main>...</main>
	HTML4中的代码示例：
	<div>...</div>

#### 新增的其他元素
	除了结构元素外，在HTML5中，还新增以下元素。
	(1) video元素
	video元素用于定义视频，比如电影片段或其他视频流。
	HTML 5中的代码示例：
	<video src="movie.ogg" controls="controls">video元素</video>
	HTML 4中的代码示例：
	<object type="video/ogg" data="movie.ogv">
       <param name="src" value="movie.ogv">
	</object>
	
	(2) audio元素
	audio元素用于定义音频，比如音乐或其他音频流。
	HTML 5中的代码示例：
	<video src="someaudio.wav">audio元素</video>
	HTML 4中的代码示例：
	<object type="application/ogg" data="someaudio.wav">
    	<param name="src" value="someaudio.wav">
	</object>
	
	(3) embed元素
	embed元素用来插入各种多媒体，格式可以是Midi、Wav、AIFF、AU、MP3等。
	HTML 5中的代码示例：
	<embed src="horse.wav" />
	HTML 4中的代码示例：
	<object data="flash.swf"  type="application/x-shockwave-flash"></object>
	
	(4) mark元素
	mark元素主要用来在视觉上向用户呈现那些需要突出显示或高亮显示的文字。
	mark元素的一个比较典型的应用就是在搜索结果中向用户高亮显示搜索关键词。
	HTML 5中的代码示例：
	<mark></mark>
	HTML 4中的代码示例：
	<span></span>
	
	(5) progress元素
	progress元素表示运行中的进程，可以使用progress元素来显示JavaScript中耗费时间的函数的进程。
	HTML 5中的代码示例：
	<progress></progress>
	这是HTML 5中的新增功能，故无法用HTML 4代码来实现。
	
	(6) mark元素
	meter元素表示度量衡，仅用于已知最大值和最小值的度量。
	必须定义度量的范围，既可以在元素的文本中，也可以在min/max属性中定义。
	HTML 5中的代码示例：
	<meter></meter>
	HTML 4中的代码示例：
	这是HTML 5中的新增功能，故无法用HTML 4代码来实现。
	
	(7) time元素
	time元素用于表示日期或时间，也可以同时表示两者。
	HTML 5中的代码示例：
	<time></time>
	HTML 4中的代码示例：
	<span></span>
	
	(8) ruby元素
	ruby元素表示ruby注释（中文注音或字符）。
	HTML 5中的代码示例：
	<ruby>漢 <rt><rp>(</rp>ㄏㄢˋ<rp>)</rp></rt></ruby>
	这也是HTML 5中的新增功能。
	
	(9) rt元素
	rt元素表示字符（中文注音或字符）的解释或发音。
	HTML 5中的代码示例：
	<ruby>漢 <rt> ㄏㄢˋ </rt></ruby>
	这是HTML 5中的新增功能。

	(10) rp元素
	rp元素在ruby注释中使用，以定义不支持ruby元素的浏览器所显示的内容。
	HTML 5中的代码示例：
	<ruby>漢 <rt><rp>(</rp>ㄏㄢˋ<rp>)</rp></rt></ruby>
	这是HTML 5中的新增功能。
	
	(11) wbr元素
	wbr元素表示软换行。wbr元素与br元素的区别是：br元素是此处必须换行，而wbr元素意思就是浏览器窗口或
	父级元素的宽度足够宽时（没必要换行时），不进行换行，而当宽度不够时，主动在此处进行换行。
	wbr元素好像对字符型的语言用处比较大，但是对于中文，貌似没多大用处。
	HTML 5中的代码示例：
	<p> To learn AJAX, you must be fami<wbr>liar with the XMLHttp<wbr>Request Object. </p>
	这是HTML 5中的新增功能。
	
	(12) canvas元素
	canvas元素表示图形，比如图表和其他图像。这个元素本身没有行为，仅提供一块画布，但把一个绘图API展现给客户端JavaScript，以使脚本能够把想绘制的东西绘制到这块画布上。
	HTML 5中的代码示例：
	<canvas id="myCanvas" width="200" height="200"></canvas>
	HTML 4中的代码示例：
	<object data="inc/hdr.svg" type="image/svg+xml" width="200" height="200">
	</object>
	
	(13) command元素
	command元素表示命令按钮，比如单选按钮、复选框或按钮。
	HTML 5中的代码示例：
	<command onclick=cut()" label="cut">
	这是HTML 5中的新增功能。
	
	(14) details元素
	details元素表示用户要求得到并且可以得到的细节信息。它可以与summary元素配合使用。summary元素提供标题或图例。
	标题是可见的，用户点击标题时，会显示细节信息。summary元素应该是details元素的第一个子元素。
	HTML 5中的代码示例：
	<details>
	   <summary>HTML5</summary>
	   This document teaches you everything you have to learn about HTML5.
	</details>
	
	(15) datalist元素
	datalist元素表示可选数据的列表，与input元素配合使用，可以制作出输入值的下拉列表。
	HTML 5中的代码示例：
	<datalist></datalist>
	这是HTML 5中的新增功能。
	
	(16) datagrid元素
	datagrid元素表示可选数据的列表，它以树形列表的形式显示。
	HTML 5中的代码示例：
	<datagrid></datagrid>
	这是HTML 5中的新增功能。
	
	(17)keygen元素
	keygen元素表示生成密钥。
	HTML 5中的代码示例：
	<keygen>
	这是HTML 5中的新增功能。
	
	(18)output元素
	output元素表示不同类型的输出，比如脚本的输出。
	HTML 5中的代码示例：
	<output></output>
	HTML 4中的代码示例：
	<span></span>
	
	(19)source元素
	source元素为媒介元素（比如<video>和<audio>）定义媒介资源。
	HTML 5中的代码示例：
	<source>
	HTML 4中的代码示例：
	<param>
	
	(20) menu元素
	menu元素表示菜单列表。当希望列出表单控件时使用该标签。
	HTML 5中的代码示例：
	<menu>
	  <li><input type="checkbox" />Red</li>
	  <li><input type="checkbox" />blue</li>
	</menu>
	在HTML 4中，menu元素不被推荐使用。
	
	(21) dialog元素
	dialog元素表示对话框。
	HTML 5中的代码示例：
	<dialog></dialog>

#### 新增的input元素的类型
	HTML 5中新增很多input元素的类型，现列举如下：
	·email：email类型表示必须输入e-mail地址的文本输入框。
	·url：url类型表示必须输入URL地址的文本输入框。
	·number：number类型表示必须输入数值的文本输入框。
	·range：range类型表示必须输入一定范围内数字值的文本输入框。
	·Date Pickers：HTML 5拥有多个可供选取日期和时间的新型输入文本框。
	·date：选取日、月、年。
	·month：选取月、年。
	·week：选取周和年。
	·time：选取时间（小时和分钟）。
	·datetime：选取时间、日、月、年（UTC时间）。
	·datetime-local：选取时间、日、月、年（本地时间）。
	
#### 废除的元素
	由于各种原因，在HTML 5中废除了很多元素，简单介绍如下。
	1.能使用CSS替代的元素
	对于basefont、big、center、font、s、strike、tt、u等元素，由于它们的功能都是纯粹为画面展示服务的，而HTML 5中提倡把画面展示性功能统一放在CSS样式表中统一编辑，所以将这些元素废除，使用编辑CSS、添加CSS样式表的方式进行替代。其中font元素允许由“所见即所得”的编辑器进行插入，s元素、strike元素可以由del元素进行替代，tt元素可以由CSS的font-family属性进行替代。
	2.不再使用frame框架
	对于frameset元素、frame元素与noframes元素，由于frame框架对网页可用性存在负面影响，在HTML 5中已不支持frame框架，只支持iframe框架，或者由服务器方创建的由多个页面组成的复合页面的形式，同时将这三个元素废除。
	3.只有部分浏览器支持的元素
	对于applet、bgsound、blink、marquee等元素，由于只有部分浏览器支持这些元素，特别是bgsound元素以及marquee元素，只被Internet Explorer所支持，所以在HTML 5中被废除。其中applet元素可由embed元素或object元素进行替代，bgsound元素可由audio元素进行替代，marquee可以由JavaScript编程的方式所替代。
	4.其他被废除的元素
	其他被废除元素还有：
	·废除rb元素，使用ruby元素替代。
	·废除acronym元素，使用abbr元素替代。
	·废除dir元素，使用ul元素替代。
	·废除isindex元素，使用form元素与input元素相结合的方式替代。
	·废除listing元素，使用pre元素替代。
	·废除xmp元素，使用code元素替代。
	·废除nextid元素，使用GUIDS替代。
	·废除plaintext元素，使用"text/plian"MIME类型替代。

### 新增的属性和废除的属性
#### 新增的属性
	1.表单相关的属性
	新增的与表单相关的元素如下：
	·可以对input（type=text）、select、textarea与button元素指定autofocus属性。它以指定属性的方式让元素在画面打开时自动获得焦点。
	·可以对input元素（type=text）与textarea元素指定placeholder属性，它会对用户的输入进行提示，提示用户可以输入的内容。
	·可以对input、output、select、textarea、button与fieldset指定form属性，声明它属于哪个表单，然后将其放置在页面上任何位置，而不是表单之内。
	·可以对input元素（type=text）与textarea元素指定required属性。该属性表示在用户提交的时候进行检查，检查该元素内一定要有输入内容。
	·为input元素增加了几个新的属性：autocomplete、min、max、multiple、pattern与step。同时还有一个新的list元素与datalist元素配合使用。datalist元素与autocomlete属性配合使用。multiple属性允许在上传文件时一次上传多个文件。
	·为input元素与button元素增加了新属性formaction、formenctype、formmethod、formnovalidate与formtarget，它们可以重载form元素的action、enctype、method、novalidate与target属性。为fieldset元素增加了disabled属性，用于把它的子元素设为disabled（无效）状态。
	·为input元素、button元素、form元素增加了novalidate属性，该属性可以取消提交时进行的有关检查，表单可以被无条件提交。
	·为所有可使用标签（label元素）的表单元素（包括非隐藏的input元素（type属性值不等于hidden）、button元素、select元素、textarea元素、meter元素、output元素、progress元素以及keygen元素）定义一个labels属性，属性值为一个NodeList对象，代表该元素所绑定的标签元素所构成的集合。
	·可以在标签（label元素）内部放置一个表单元素，并且通过该标签的control属性访问该表单元素。
	·针对input元素与textarea元素，在HTML 5中增加SelectionDirection属性。当用户在这两个元素中用鼠标选取部分文字时，可以使用该属性来获取选取方向。当用户正向选取文字时，该属性值为“forward”，当用户反向选取文字时，该属性值为“backward”。当用户没有选取任何文字时，该属性值为“forward”。
	·对复选框（checkbox元素）添加indeterminate属性，以说明复选框处于“尚未明确是否选取”状态。
	·对类型为image的input元素添加用于指定图片按钮中图片高度的height属性与图片宽度的width属性。
	·对textarea元素新增用于限定可输入文字个数的maxlength属性与用于指定表单提交时是否在文字换行处添加换行符的wrap属性。
	
	2.链接相关的属性
	新增的与链接相关的属性如下：
	·为a与area元素增加了media属性、download属性以及ping属性，其中media属性规定目标URL是为什么类型的媒介/设备进行优化的，download属性用于让用户下载目标链接所指向的资源，而不是直接打开该目标链接，这些属性均只能在href属性存在时使用。
	·为area元素增加了hreflang属性与rel属性，以保持与a元素、link元素的一致。
	·为link元素增加了新属性sizes。该属性可以与icon元素结合使用（通过rel属性），该属性指定关联图标（icon元素）的大小。
	·为base元素增加了target属性，主要目的是保持与a元素的一致性。
	
	3.其他属性
	除了上面介绍的与表单和链接相关的属性外，HTML 5还增加了下面的属性：
	·为ol元素增加start属性与reversed属性，其中start属性定义列表的开始编号，reversed属性指定列表倒序显示。
	·为meta元素增加charset属性，因为这个属性已经得到广泛支持，而且为文档的字符编码的指定提供了一种比较良好的方式。
	·为menu元素增加了两个新的属性——type与label。label属性为菜单定义一个可见的标注，type属性让菜单可以以上下文菜单、工具条、与列表菜单三种形式出现。
	·为style元素增加scoped属性，用来规定样式的作用范围，譬如只对页面上某个树起作用。
	·为script元素增加async属性，它定义脚本是否异步执行。
	·为html元素增加属性manifest，开发离线Web应用程序时它与API结合使用，定义一个URL，在这个URL上描述文档的缓存信息。
	·为iframe元素增加三个属性——sandbox、seamless与srcdoc，用来提高页面安全性，防止不信任的Web页面执行某些操作。

#### 废除的属性
|HTML4中使用的属性|使用该属性的元素|HTML5中的替代方案|
|---------------|---------------|---------------|
|rev			|link,a			|rel			|
|charset		|link,a 		|使用Content-type头元素|
|shape、coords	|a				|使用area元素代替a元素|
|longdesc		|img.iframe		|使用a元素链接到较长描述|
|target 		|link			|多余属性，被省略 |
|nohref 		|area			|多余属性，被省略 |
|profile		|head			|多余属性，被省略 |
|version		|html			|多余属性，被省略 |
|name   		|img			|id				|
|scheme			|mate			|只为某个表单域使用scheme|
|archive、classid、codebase、codetype、declare、standby|object|使用data与type属性类调用插件|
|valuetype、type|param  		|使用name与value属性|
|axis、abbr		|td，th			|title属性		|
|scope			|td				|使用Content-type头元素|
|align	 		|caption、input、legend、div、h1、h2、h3、h4、h5、h6、p|使用CSS样式表替代|
|alink、link、text、vlink、background、bgcolor|body|使用CSS样式表替代|
|alink、bgcolor、border、cellpadding、cellspacing、frame、rules、width|table|使用CSS样式表替代|
|align、char、charoff、height、nowrap、valign|tbody、thead、tfoot|使用CSS样式表替代|
|align、bgcolor、char、charoff、height、nowrap、valign、width|td、th|使用CSS样式表替代|
|align、bgcolor、char、charoff、valign|tr|使用CSS样式表替代|
