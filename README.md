# roomescape
【密室逃脱】逃离邪恶女巫小屋
<p>游玩方式：将【物品】复制并输入文本框内后，点击确定或回车以验证其是否正确。有些地方需要输入密码。</p>
<p>游戏简介：你被邪恶的女巫抓起来了，快趁女巫不在逃走吧！</p>

# 攻略
<p>懒得写了，有需要再说吧！！！好麻烦啊！！！</p>
<body>
    <h1>下拉选择内容显示</h1>
    
    <label for="content-selector">请选择一个主题：</label>
    <select id="content-selector">
        <option value="" selected>-- 请选择 --</option>
        <option value="web-development">Web开发</option>
        <option value="data-science">数据科学</option>
        <option value="mobile-apps">移动应用开发</option>
        <option value="cloud-computing">云计算</option>
        <option value="ai-ml">人工智能</option>
    </select>
    
    <div id="content-display">
        <p>选择一个主题后，相关内容将显示在这里。</p>
    </div>

    <script>
        // 内容数据
        const contentData = {
            "web-development": {
                title: "Web开发",
                content: "Web开发是创建和维护网站的过程，包括前端(用户界面)和后端(服务器、数据库)开发。"
            },
            "data-science": {
                title: "数据科学",
                content: "数据科学是从数据中提取知识和见解的跨学科领域，涉及统计学、机器学习和数据分析。"
            },
            "mobile-apps": {
                title: "移动应用开发",
                content: "移动应用开发是为智能手机和平板电脑创建软件应用程序的过程，包括iOS和Android平台。"
            },
            "cloud-computing": {
                title: "云计算",
                content: "云计算是通过互联网按需提供计算服务(如服务器、存储、数据库)的模式。"
            },
            "ai-ml": {
                title: "人工智能",
                content: "人工智能是创建能够执行通常需要人类智能的任务的智能机器的计算机科学分支。"
            }
        };

        // 获取DOM元素
        const selector = document.getElementById('content-selector');
        const display = document.getElementById('content-display');

        // 监听下拉框变化
        selector.addEventListener('change', function() {
            const selectedValue = this.value;
            
            if (selectedValue && contentData[selectedValue]) {
                const data = contentData[selectedValue];
                display.innerHTML = `<h2>${data.title}</h2><p>${data.content}</p>`;
            } else {
                display.innerHTML = '<p>选择一个主题后，相关内容将显示在这里。</p>';
            }
        });
    </script>
</body>
