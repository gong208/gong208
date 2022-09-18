---
layout: post
title:  "Wechat Devtool 1"
date:   2022-09-16 12:00:00 0800
---
0. #Wechat Miniapplication: 

Wechat Miniapplication is literally an application based on Wehcat. Different from ordinary applications, it is said that these miniapplications can be used without downloading & installing. In fact, it is because they have a very small size (less than 2M) so that the users won't be aware of the process of downloading.
1. #[Wechat developer tool] (https://developers.weixin.qq.com/miniprogram/en/dev/devtools/devtools.html): a specially designed IDE for wechat miniapplications.
2. #The regular code structure of a miniapplication: 

<details><summary>pages</summary>
  It is recommended to create all the codes for each page of the application in this folder.
  
  <details><summary>  log</summary>
    
    
    This is an example folder for a log page in the application. In a page folder, there will usually be four files:
    
    log.js: .js file is responsible for the logical components of the page. Using javascript, developers can bind events to a button, pass parameters, etc.
    
    log.json: I haven't worked much about the .json files so far. As far as I know, it is resonsible for the page's "setup": page title, text style, background color...
    
    log.wxml: .wxml is derived from html. It sues a language syntax similar to html to create elements like ```<view></view>```, ```<button></button>``` on the page.
    
    log.wxss: wxss is derived from css. It works similarly. I use it to arrange the elements shown on the page, like position and flex display.
    
    
  </details>


</details>
  

<details><summary>utils</summary>
  util.js
</details>
 
 
<details><summary>app.js</summary>
  app.js file is responsible for the global logic. The APP() in it is the start point of the overall application code.
</details>


<details><summary>app.json</summary>
  A page can be displayed only after you add the link of the page into this file. app.json is responsible for the global setup. For example, you can set the primary background color or add the tab bars. 
</details>
 
<details><summary>app.wxss</summary>
  app.wxss works the same as the .wxss files of the pages, but it influences globally. The page wxss arrangement is prior to the global arrangement.
</details>
 
 
<details><summary>project.config.json</summary>
  This file contains the settings of a miniapplication project.
</details>



