## 关于

我认为每一个人都需要一个简历网页以介绍自己，可以作为面试时的加分项，也可以放置在您的个人网站之中。

这是一款响应式炫酷而优雅的个人简历网页，电脑与手机均适用，无需联网，纯前端HTML+CSS+JavaScript实现，可用于个人简历、个人网站、个人简介或学习使用，可以通过配置文件自动生成属于你自己的网页。

## 演示

[网页演示地址](https://iuoily.github.io/)

在手机或平板或电脑上查看该网页。



## 项目结构

Resume文件下：

- config文件包含了项目的配置文件。
- CSS文件下personal-info-main.css为主要的CSS代码，personal-info-animate.css为项目的动画CSS代码，其余CSS文件为引用库。
- JS文件下personal-info-main.js为主要的JS代码，其余js文件为引用库。
- images文件包含了可能用上的图片。
- svg文件下包含了一些图标。
- index.html为网页的入口。



## 配置

**在./config/config.js文件中配置您的信息以自动生成属于你自己的网页，遵循JavaScript对象声明规范，注意格式，对象变量中间不要漏写逗号，对象变量结尾不要多写逗号。**

```javascript
var config = {
    /*在这里配置你的基本信息，所有数据以字符串形式给出*/
    name: "刘波",
    sex: "男",
    age: "22",
    phone: "176****3432",
    email: "1427718414@qq.com.com",
    address: "现居湖北省武汉市",
    qq: "1427718414",
    log: "iuoily",
    excpect_work: "Java后端开发",


    /*在这里配置首页的座右铭集合*/
    motto: [
        "明天不一定会更好，但要坚信更好的明天一定会来。",
        "要做的事情总找得出时间和机会，不愿意做的事情也总能找得出借口。",
        "Gor For It!",
        "有智者立长志，无志者长立志。",
        "那些过去的眼泪终将风干在记忆里。",
        "真相，是为了剿灭幻想。",
        "我欲将心向明月，奈何明月照沟渠。",
        "春风得意马蹄疾，一日看尽长安花。",
        "天凉好个秋！",
        "老骥伏枥，志在千里。烈士暮年，壮心不已。",
        "老当益壮，宁移白首之心。穷且益坚，不坠青云之志。",
        "我们必须拿我们所有的， 去换我们所没有的",
        "蒹葭苍苍，白露为霜；所谓伊人，在水一方。",
        "数风流人物，还看今朝！"
    ],


    /*在这里配置首页的见面信息，你可以内嵌HTML标签以调整格式*/
    welcome: "青青子衿，悠悠我心<br>" +
             "但为君故，沉吟至今<br>" +
             "你好，我是刘波<br>" +
             "很高兴见到你!",


    /*在这里配置关于我的信息，你可以内嵌HTML标签以调整格式*/
    about: "<p>你好！我叫刘波，性别男，。我期望的工作岗位Java后端开发。</p>" +
        "<p>我有着较多的Java编程经验，计算机基础知识掌握扎实，能够在工作中很好的完成自己的任务。此外，我有着充满激情的工作态度，团队协同作战能力强，同时我也具备独立开发的能力，擅于发现并解决问题。我的执行力强、责任感高、集体荣誉感强、敢于担当，能够接受加班或出差等安排</p>" +
        "<p>十分期待与您的联系!</p>",



    /** 
    * 在这里配置你的技能点
    * ["技能点", 掌握程度, "技能条颜色"]
    */  
    skills: [
        ["Java", 80, "red"],
        ["Python", 77, "blue"],
        ["SQL", 75, "#1abc9c"],
        ["HTML5", 67, "rgba(0,0,0)"],
        ["CSS3", 60, "yellow"],
        ["JavaScript", 70, "pink"]
    ],


    /*这里填写你的技能描述，你可以内嵌HTML标签以调整格式*/
    skills_description: "<ul>" +
        "     <li>操作系统、计算机网络等编程基础知识良好。</li>" +
        "     <li>熟练掌握Java基础。</li>" +
        "     <li>熟悉JavaIO、多线程、集合等基础框架。</li>" +
        "     <li>了解JVM原理。</li>" +
        "     <li>熟悉Python语言开发基本知识。</li>" +
        "     <li>熟悉SQL语句编写以及调优。</li>" +
        "     <li>熟悉基本Linux命令操作。</li>" +
        "     <li>熟悉Spring、Mybatis、SpringBoot等框架的使用，了解其原理与机制。</li>" +
        "     <li>熟悉缓存、消息等机制。</li>" +
        "     <li>了解分布式系统的设计与应用。</li>" +
        "     <li>熟悉HTML、CSS、JavaScript以及相应前端知识。</li>" +
        " </ul>",


    /**
     * 这里填写你的个人作品展示
     * ["img"，"url", "ProjectName", "brief"]
     * img表示您的作品图片链接，url表示您的项目地址，ProjectName表示您的仓库或作品名称，brief是一句简短的介绍
     * 通过查看实际效果以调整字题长度
     */
    portfolio: [
        ["./images/pro-1.png", "http://#/", "个人博客", "这里记录了我的Java后端学习笔记<br>持续更新"],
        ["./images/pro-2.png", "https://#", "智能人机对战五子棋", "采用C++编写的智能五子棋人机对战<br>2021/7/23"],
        ["https://pic3.zhimg.com/80/v2-d9766956d5c85c2780e4c5008fd946ca_1440w.jpg", "https://github.com/happysnaker/StudentsManageSystem", "学生管理系统", "C语言+AVL树+多重双向表实现"]
    ],


    /**
     * 这里填写您的工作经历
     * ["日期"， "工作"， "介绍"]
     * 你可以内嵌HTML标签以排版格式
     */
    work: [
        //如果您内有工作经历，您可以采取下列写法
        // ["————————", "", "<p>暂无工作经历，期待您的联系。</p>"]

        ["2020/7/1 — 2021/8/10", "<br>阎王殿实习生",
            "<p><strong>阎王殿研发部</strong></p>" +
            "<p>随着阴历7月15中元节的到来，阎王殿的任务愈发庞大，我以及我所在小组主要负责阎王谱后台部分，拟在解决千万访问并发问题，经过不械努力，使得产品稳定、高效的运行。</p>" +
            "<p>随着阴历7月15中元节的到来，阎王殿的任务愈发庞大，我以及我所在小组主要负责阎王谱后台部分，拟在解决千万访问并发问题，经过不械努力，使得产品稳定、高效的运行。</p>"
        ],

        ["2020/7/1 — 2021/8/10", "<br>阎王殿实习生",
            "<p><strong>阎王殿研发部</strong></p>" +
            "<p>随着阴历7月15中元节的到来，阎王殿的任务愈发庞大，我以及我所在小组主要负责阎王谱后台部分，拟在解决千万访问并发问题，经过不械努力，使得产品稳定、高效的运行。</p>" +
            "<p>随着阴历7月15中元节的到来，阎王殿的任务愈发庞大，我以及我所在小组主要负责阎王谱后台部分，拟在解决千万访问并发问题，经过不械努力，使得产品稳定、高效的运行。</p>"
        ]
    ],


    /**
     * 这里填写你的其他经历
     * ["日期"， "经历"， "介绍"]
     * 建议填写您的校级及以上得奖经历或或其他证书
     */
    others: [
    ],


    /**
     * 在这里填写您的社交网络平台
     * ["img", "url", "desc"]
     * img是社交平台的图标，在./svg目录下我们已经准备好了 微博、简书、掘金、小红书、知乎、csdn、facebook、github、力扣、CF和qq的图标
     * url是您链接
     * desc是一段描述，将鼠标移入将会显示该描述
     * 建议您放置数量 <= 5
     */
    icon: [
        ["./svg/LeetCode.svg", "https://#/", "我的力扣主页"],
        ["./svg/github.svg", "https://github.com/iuoily", "我的GitHub主页"],
        ["./svg/博客.svg", "http://#", "我的个人博客"],
        ["./svg/掘金.svg", "https://#", "我的掘金主页"],
        ["./svg/知乎.svg", "https://#", "我的知乎主页"]
    ],


    //这是一些图片链接，建议您仅更改第二个头像图片
    url: [
        //背景图、头像、作品展示背景、其他经历背景
        "./images/intro-bg.jpg",
        "./images/2.jpg",
        "./images/work-bk.png",
        "./images/4.jpg"
    ]

}
```



**如果您不需要配置该文件，请注释掉./JS/personal-info-main.js文件中顶层4行代码.**

```function addScript(url) {
function addScript(url) {
    document.write("<script language=javascript src=./config/config.js></script>");
}
addScript();
```



## 参阅

### 引用库

[Bootstrap · The most popular HTML, CSS, and JS library in the world. (getbootstrap.com)](https://getbootstrap.com/)

[AOS - Animate on scroll library (michalsnik.github.io)](http://michalsnik.github.io/aos/)

[anime.js官网_免费、灵活的轻型JavaScript动画库 | animejs](https://www.animejs.cn/)

[jQuery](https://jquery.com/)



### 其他

[burc-li/timeLine: 纯CSS时间轴 (github.com)](https://github.com/burc-li/timeLine)

[VincentGarreau/particles.js: A lightweight JavaScript library for creating particles (github.com)](https://github.com/VincentGarreau/particles.js)


