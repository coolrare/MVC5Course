【ASP.NET MVC 5 開發實戰】練習專案
==================================

開發工具
------------

- [Visual Studio Community 2015](https://go.microsoft.com/fwlink/?LinkId=691978&clcid=0x404)
    - 請更新到 [Visual Studio 2015 Update 3](https://www.visualstudio.com/news/releasenotes/vs2015-update3-vs)
    - 若安裝英文版的人，也可以額外安裝 [Visual Studio 2015 語言套件 - 繁體中文](https://www.microsoft.com/zh-tw/download/details.aspx?id=48157)。
    - 建議安裝的 Visual Studio 擴充套件
        - [Web Essentials 2015.3](http://vswebessentials.com/)
        - [tangible T4 Editor 2.3.0 plus modeling tools for VS 2015](https://visualstudiogallery.msdn.microsoft.com/784cf592-b797-4d4d-ad33-331fcf63faad)
- [SQL Server Data Tools](https://msdn.microsoft.com/zh-tw/library/mt204009.aspx)
    - 請點擊【[從這裡下載適用於 Visual Studio 2015 的 SQL Server Data Tools](https://msdn.microsoft.com/mt186501)】下載安裝檔。
- [SQL Server Management Studio](https://msdn.microsoft.com/zh-tw/library/mt238290.aspx)
    - 請點擊【[下載 SQL Server Management Studio (16.5.1)](https://go.microsoft.com/fwlink/?linkid=837453)】下載安裝檔。

版控工具
------------

- [Git for Windows](https://git-scm.com/)
- [GitHub Desktop](https://desktop.github.com/)
- [TortoiseGit](https://tortoisegit.org/)

關於 LocalDB
------------
  
* SQL Server 2012 LocalDB (SQL Server 11.0.3000)
	* 伺服器名稱: **``(localdb)\v11.0``**
	*  [SQL Server 2012 Express LocalDB (SqlLocalDB) 深入剖析](http://blog.miniasp.com/post/2012/09/03/SQL-Server-2012-Express-LocalDB-Quick-Start.aspx)
* SQL Server 2014 LocalDB (SQL Server 12.0.2456.0)
	* 伺服器名稱: **``(localdb)\MSSQLLocalDB``**
* SQL Server 2016 LocalDB (13.0.2151.0)
	* 伺服器名稱: **``(localdb)\MSSQLLocalDB``**
* SQL Server Data Tools (SSDT) LocalDB (SQL Server 13.0.2151)
	* 伺服器名稱: **``(localdb)\ProjectsV13``**
* LocalDB 各版本示意圖
<br>![image](https://cloud.githubusercontent.com/assets/88981/23688176/c0cf8f1a-03ed-11e7-85ee-9d31bdb1d8ae.png)



建立 ASP.NET MVC 5 專案步驟說明
-------------------------------

1. [檔案] / [新增] / [專案]

	![image](https://cloud.githubusercontent.com/assets/88981/4964338/795bee9c-6793-11e4-9e8d-ebc2026c8dfa.png)

2. 選擇 [Web] 分類的 [ASP.NET Web Application (.NET Framework)]，設定專案 [名稱] 並勾選 [加入原始碼控制中]

	![image](https://cloud.githubusercontent.com/assets/88981/23688347/ffaed578-03ee-11e7-9a49-e5cf4cedff7d.png)


3. 選擇 [MVC] 專案範本，勾選 [Web API] 核心參考，並取消勾選 [雲端中的主機]

	![image](https://cloud.githubusercontent.com/assets/88981/23688405/629ff036-03ef-11e7-9ebf-cd2fdbd54290.png)


專案 NuGet 套件介紹
-------------------

以下是 Visual Studio 2015 Update 3 內建的 ASP.NET MVC 5 專案範本的 NuGet 套件介紹。

### [ 後端套件 ]

* ASP.NET MVC 5.2.3
  - 官網: http://www.asp.net/mvc
  - 專案位址: http://aspnetwebstack.codeplex.com/
  - 範例專案: http://aspnet.codeplex.com/SourceControl/latest
* ASP.NET Web API 5.2.3
  - 官網: http://www.asp.net/web-api
  - 專案位址: http://aspnetwebstack.codeplex.com/
  - 範例專案: http://aspnet.codeplex.com/SourceControl/latest
* ASP.NET Identity 2.2.1
  - 官網: http://www.asp.net/identity
  - 專案位址: https://aspnetidentity.codeplex.com/
  - 範例專案: http://aspnet.codeplex.com/SourceControl/latest
* Entity Framework 6.1.3
  - 官網: http://www.asp.net/entity-framework
  - 專案位址: https://entityframework.codeplex.com/
* Microsoft.AspNet.Web.Optimization 1.1.3
  - 用來將 javascript, js 最小化 (minification) 與 打包 (bundling) 的工具
  - ASP.NET Optimization introduces a way to bundle and optimize CSS and JavaScript files.
  - 專案位址: https://aspnetoptimization.codeplex.com/
  - 官方文件: https://aspnetoptimization.codeplex.com/documentation
  - NuGet 套件: https://www.nuget.org/packages/Microsoft.AspNet.Web.Optimization
  - 相關連結
    * [Bundling and Minification | The ASP.NET Site](http://www.asp.net/mvc/overview/performance/bundling-and-minification)
    * [c# - Bundler not including .min files - Stack Overflow](http://stackoverflow.com/questions/11980458/bundler-not-including-min-files)
    * [kenhaines.net | WebGrease: As seen in Visual Studio 2012](http://kenhaines.net/post/2012/06/09/WebGrease-As-seen-in-Visual-Studio-2012.aspx)
    * [Web Optimization in Visual Studio 2012 RC | Howard Dierking](http://codebetter.com/howarddierking/2012/06/04/web-optimization-in-visual-studio-2012-rc/)
* Microsoft.Web.Infrastructure 1.0.0.0
  - 用來在執行時期動態註冊 HTTP modules (相依於 Microsoft.AspNet.Web.Optimization 套件)
* WebGrease 1.5.2
  - 用來最佳化 javascript, css 與圖片檔案 (相依於 Microsoft.AspNet.Web.Optimization 套件)
  - WebGrease is a suite of tools for optimizing javascript, css files and images.
  - 專案位址: https://webgrease.codeplex.com/
* Antlr 3.4.1.9004
  - 用來解析 CSS 語法的工具 (相依於 WebGrease 套件) [ [說明](http://stackoverflow.com/questions/20412234/what-is-the-purpose-of-antlr-package-in-visual-studio-2013-asp-net-project) ]
* Newtonsoft.Json (Json.NET) 6.0.4
  - 提供 .NET 環境操作 JSON 資料 (相依於 WebGrease 套件)
  - 官網: http://james.newtonking.com/json
  - 專案位址: https://github.com/JamesNK/Newtonsoft.Json
* OWIN 1.0
  - 官網: http://owin.org/
* Microsoft.Owin 3.0.1 (Katana)
  - 專案位址: http://katanaproject.codeplex.com/
  - [其他 Katana 相關套件](http://katanaproject.codeplex.com/wikipage?title=Packages)
  	- Microsoft.Owin.Host.SystemWeb<br>
  	  OWIN server that enables OWIN-based applications to run on IIS using the ASP.NET request pipeline.
	- Microsoft.Owin.Security<br>
	  Common types which are shared by the various authentication middleware components.
	- Microsoft.Owin.Security.Cookies<br>
	  Middleware that enables an application to use cookie based authentication, similar to ASP.NET's forms authentication.
	- Microsoft.Owin.Security.Facebook<br>
	  Middleware that enables an application to support Facebook's OAuth 2.0 authentication workflow.
	- Microsoft.Owin.Security.Google<br>
	  Contains middlewares to support Google's OpenId and OAuth 2.0 authentication workflows.
	- Microsoft.Owin.Security.MicrosoftAccount<br>
	  Middleware that enables an application to support the Microsoft Account authentication workflow.
	- Microsoft.Owin.Security.OAuth<br>
	  Middleware that enables an application to support any standard OAuth 2.0 authentication workflow.
	- Microsoft.Owin.Security.Twitter<br>
	  Middleware that enables an application to support Twitter's OAuth 2.0 authentication workflow.
* Microsoft.Net.Compilers 1.0.0
	- 此為 C# 6.0 以上的 .NET 編譯器 ("Roslyn") (The .NET Compiler Platform)
	- 專案位址: https://github.com/dotnet/roslyn
* Microsoft.CodeDom.Providers.DotNetCompilerPlatform 1.0.0
	- 此為 .NET 編譯器的 CodeDOM 提供者，用來提供解析 C# / VB.NET 原始碼的服務。

### [ 前端套件 ]

* Bootstrap 3.0.0
	* 官網: http://getbootstrap.com/
* jQuery 1.10.2
	* 官網: http://www.jquery.com/
	* 專案位址: http://github.com/jquery/jquery 
* jQuery Validation 1.11.1
	* 官網: http://jqueryvalidation.org/
	* 專案位址: https://github.com/jzaefferer/jquery-validation 
* Microsoft.jQuery.Unobtrusive.Validation 3.2.3
	* 用來與 ASP.NET MVC 5 表單驗證功能搭配使用的 JS 函式庫
	* 套件位址: https://www.nuget.org/packages/Microsoft.jQuery.Unobtrusive.Validation/
	* 版本說明: http://go.microsoft.com/fwlink/?LinkId=389866  
* Modernizr 2.6.2
	* 官網: http://modernizr.com/
* Respond 1.2.0
	* 專案位址: https://github.com/scottjehl/Respond 

## 課前學習資源

- [邊做邊學 ASP.NET MVC 4 - YouTube](https://www.youtube.com/playlist?list=PL_dAxk7-NoFt9ccYrIjFma1p8iLsQqweq)
    - 強烈建議這個系列影片可以先看過，跟著做一遍，上課會更有感覺！(本影片也適用於 ASP.NET MVC 5 版本)
- [ASP.NET MVC 5 新功能探索 - YouTube](https://www.youtube.com/playlist?list=PL_dAxk7-NoFtMR6s_aW_zAKHpIsCIzTNa)
    - 建議這個影片也可以先看過，了解一下 ASP.NET MVC 5 與 ASP.NET MVC 4 的差異之處 (其實差不多)
- [C# Fundamentals: Development for Absolute Beginners | Channel 9](https://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners) 
    - 如果有學員尚未接觸過 C# 程式語言，建議可以先看這個免費的教學課程。
    - 課程雖然是英文發音，但有**完整繁體中文字幕**，建議搭配中文字幕觀看！
- [HTML5 & CSS3 Fundamentals: Development for Absolute Beginners | Channel 9](https://channel9.msdn.com/Series/HTML5-CSS3-Fundamentals-Development-for-Absolute-Beginners)
    - 如果有學員不太有網頁開發經驗，建議可以先看這個免費的教學課程。
    - 課程雖然是英文發音，但有**完整繁體中文字幕**，建議搭配中文字幕觀看！
- [30 天精通 Git 版本控管](https://github.com/doggy8088/Learn-Git-in-30-days/blob/master/zh-tw/README.md)
    - 因為課程進行中的原始碼都會以 GitHub 分享給學員，各位自行實作的練習專案也建議用 Git 進行版本控管。
- [Windows 8 小技巧: 繁體中文語言如何變更預設輸入法(英文)](http://blog.miniasp.com/post/2012/06/30/Windows-8-Tips-How-to-change-default-input-method-for-languages.aspx)
    - Windows 8 之後的微軟注音輸入法，真的難用到爆炸，建議參考本文進行設定，否則 Visual Studio 2015 的開發體驗會受到影響。

相關連結
--------

* [ASP.NET MVC | The ASP.NET Site](https://www.asp.net/mvc)
* [The Will Will Web | ASP.NET MVC](http://blog.miniasp.com/category/ASPNET-MVC.aspx)
* [The Will Will Web | Visual Studio / C# / ASP.NET MVC / SQL Server 新手上路之學習資源整理](http://blog.miniasp.com/post/2015/07/03/Learning-Resources-for-CSharp-Visual-Studio-ASP-NET-MVC-SQL-Server.aspx)
* [ASP.NET MVC Guidance](https://docs.microsoft.com/en-us/aspnet/mvc/)
* [What's New in ASP.NET MVC 5](https://docs.microsoft.com/en-us/aspnet/mvc/mvc5)
* [What's New in ASP.NET MVC 4](https://docs.microsoft.com/en-us/aspnet/mvc/mvc4)
* [What's New in ASP.NET MVC 3](https://docs.microsoft.com/en-us/aspnet/mvc/mvc3)
* [Announcing the Release of ASP.NET MVC 5.1, Web API 2.1 and Web Pages 3.1](http://blogs.msdn.com/b/webdev/archive/2014/01/20/announcing-the-release-of-asp-net-mvc-5-1-asp-net-web-api-2-1-and-asp-net-web-pages-3-1.aspx)
* [Announcing the Release of ASP.NET MVC 5.2, Web API 2.2 and Web Pages 3.2](http://blogs.msdn.com/b/webdev/archive/2014/07/02/announcing-the-release-of-asp-net-mvc-5-2-web-api-2-2-and-web-pages-3-2.aspx)
* [Getting Started with Entity Framework 6 Code First using MVC 5](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application)
* [Getting Started with Entity Framework 5 Code First using MVC 4](http://www.asp.net/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application)
