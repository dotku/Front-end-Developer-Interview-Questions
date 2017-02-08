# Front-end-Developer-Interview-Questions-and-Answers

> 原 Questions 的作者是不允许发布答案的，我这里则公布我的参考答案，未必是正确的，欢迎指错。

## General Question  

> 这个问题基本略过，随机应变吧，基本上是积极向上的内容就行  
> \*\* 记得准备一些问题来问考官，比如职位的基本情况，类似参与的人员有多少，项目的目的，时间长短之类的，以表示你对该职位的重视和深远的考量

## HTML Questions:
- What does a doctype do?
> doctype 是用来定义文档信息的，主要是指版本信息

- What's the difference between full standards mode, almost standards mode and quirks mode?
> standards mode? 其实默认下不是 standard，而是 quirks 模式，所以你需要添加 doctype 来声明文档模式，否则一堆 bug 等着你了。  
> almost standards 是 Mozilla 1.x 浏览器的产物，和微软的 quirks 模式(IE 5.0 的产物)差不多的东西。

- What's the difference between HTML and XHTML?
XHTML 是 HTML 的分支版本，被誉为是 HTML 4.x，对 HTML 有较严格的控制，比如起始标签 <div> 和结尾标签 </div> 
不对称的话，就会整个页面报错，被认为是不必要的严谨，所以在 HTML5 中就取消了该限制。(当然，我觉得还有更多的原因，不过 
XHTML 有点像 HTML 标准的玄武纪，有很多创新的想法，是 HTML5 的基石，虽然死的也很快）

- Are there any problems with serving pages as application/xhtml+xml?
参考 HTML and XHTML 的问题，基本上就是兼容方面的隐患。

- How do you serve a page with content in multiple languages?
在 HTML 范畴，使用 lang='xx' 属性设置，从用户使用角度来讲的话，JavaScript 方面有更多的相关方案。

- What kind of things must you be wary of when design or developing for multilingual sites?
> 比如字体大小，中文 8px 基本上无法看，至少需要 12px 的大小。
> 文化差异问题，即时使用相同的语言文字，不同地方的人使用的用语也不同；除此之外，时间货币格式等也有差异

- What are data- attributes good for?
最大的好处是可以添加一些额外的信息，而不需要显示出来，比如一个物品的 id 等，这样在编写程序的时候解析起来也方便。

- Consider HTML5 as an open web platform. What are the building blocks of HTML5?
> Video Audio, eg video
> Graphic, eg. canvas
> Layout Structure, eg. section
> Local Storage

- Describe the difference between a cookie, sessionStorage and localStorage.
> Cookie is a string stores in the browser, could setup the expired time, usually it is used for sotre user information
> sessionStorage only alive during the browser open period, it would destory when browser close.
> localStorage can only be destored by force, it won't automatically desapre; it could save more data than cookie does.

- Describe the difference between `<script>`, `<script async>` and `<script defer>`.
> Script normal mode, downloand and run one by one
> Async, several file will donwload at the same time
> defer, move the current file to the final, esp for the application files; 
garentee they will run after lib script files are all downloaded.

- Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
> Style should go first; other wise user would see unstyled View at first.    
> Script on the last, so user could see the View in less waiting time.  
> Exception:  
> You try to have different theme for the webpage, so we need dynatically load css file.  
> If some Script library take longer time, it could be placed in head, so the js code rest could use the lib function immidately.

- What is progressive rendering?
> It is the technologies for reanding the conent of page as quickly as possiable, such as lazy loading.

- Have you used different HTML templating languages before?
> There are several templating language, such as twig, mushtash, jade, underscore, embedjs, handlebarjs, and ect.
