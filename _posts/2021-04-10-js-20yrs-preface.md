---
layout:       post
title:        "《JavaScript 二十年》推荐语"
author:       "Hux"
header-style: text
catalog:      true
tags:
    - Web
    - JavaScript
---

<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的视频博客</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        h1 {
            color: #333;
        }
        video {
            margin-top: 20px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <h1>欢迎来到我的视频博客</h1>

    <h2>选择本地视频文件播放</h2>
    <input type="file" id="videoInput" accept="video/*"/>
    <video id="videoPlayer" width="640" height="480" controls></video>

    <h2>通过本地服务器播放视频</h2>
    <video width="640" height="480" controls>
        <source src="http://localhost:8000/IMG_2307.mp4" type="video/mp4">
        您的浏览器不支持HTML5视频标签。
    </video>

    <script>
        // 本地文件选择和播放
        document.getElementById('videoInput').addEventListener('change', function() {
            const file = this.files[0];
            if (file) {
                const url = URL.createObjectURL(file);
                const videoPlayer = document.getElementById('videoPlayer');
                videoPlayer.src = url;
                videoPlayer.play(); // 自动播放选择的视频
            }
        });
    </script>
</body>
</html>



> 雪碧（doodlewind）邀请我给[《JavaScript 二十年》](https://zhuanlan.zhihu.com/p/373065151) 写的推荐序。

JavaScript 常常被戏称为一门偶然成功的玩具语言。而实际上，它出身名门，更是成长在聚光灯之下。纵观历史，有资格被标准化的编程语言甚少，它因此成为多方角力的战场，却也有幸同时得到业界与学界先驱的亲传。时至今日，我们甚至难言是它背负了太多妥协，还是这些妥协才成就了它呢。以史为鉴，或许你会有自己的答案。

— 黄玄，Facebook 软件工程师（编程语言、JS 引擎、前端基础设施）、中文前端社区活跃成员。
