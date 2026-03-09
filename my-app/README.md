## React

这个在网上都能搜到的，简单写一下。

**step 1**

```bash
sudo nano /etc/hosts
```

然后：

1. 用键盘方向键移动到底部
2. 粘贴这行：`199.232.68.133 raw.githubusercontent.com`
3. 按 `Ctrl + X` 退出
4. 按 `Y` 确认保存
5. 按 `Enter` 确认文件名

**step 2**

```bash
NVM_SOURCE=https://gitee.com/mirrors/nvm.git bash -c "$(curl -fsSL https://gitee.com/mirrors/nvm/raw/master/install.sh)"
```

**step 3**

```bash
echo 'export NVM_NODEJS_ORG_MIRROR=https://npmmirror.com/mirrors/node' >> ~/.bashrc
source ~/.bashrc
```

**step 4**

```bash
nvm install --lts
npm install -g yarn
```

**step 5**

```bash
yarn create react-app my-app
cd my-app
echo "SKIP_PREFLIGHT_CHECK=true" > .env
yarn start
```

## END?

练习一：个人名片

1. 学习 html/css 基础。
2. 用下面的 html/css 修改网页。

**html**

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人名片</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="card">
        <div class="avatar">
            <img src="https://via.placeholder.com/120" alt="头像">
        </div>
        <h1 class="name">张三</h1>
        <p class="title">前端开发工程师</p>
        <p class="description">
            热爱编程，喜欢学习新技术。专注于创造优雅、高效的网页体验。
        </p>
        <div class="skills">
            <span class="skill-tag">HTML</span>
            <span class="skill-tag">CSS</span>
            <span class="skill-tag">JavaScript</span>
            <span class="skill-tag">React</span>
        </div>
        <div class="contact">
            <a href="#" class="contact-btn">联系我</a>
        </div>
    </div>
</body>
</html>
```

**css**

```css
/* 全局样式 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

/* 卡片样式 */
.card {
    background-color: white;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    padding: 40px;
    max-width: 400px;
    width: 100%;
    text-align: center;
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
}

/* 头像样式 */
.avatar {
    margin-bottom: 20px;
}

.avatar img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 4px solid #667eea;
    object-fit: cover;
}

/* 姓名 */
.name {
    font-size: 28px;
    color: #333;
    margin-bottom: 10px;
    font-weight: 600;
}

/* 职位 */
.title {
    font-size: 18px;
    color: #667eea;
    margin-bottom: 20px;
    font-weight: 500;
}

/* 描述 */
.description {
    color: #666;
    line-height: 1.6;
    margin-bottom: 25px;
    padding: 0 10px;
}

/* 技能标签 */
.skills {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    margin-bottom: 30px;
}

.skill-tag {
    background-color: #f0f0f0;
    color: #333;
    padding: 5px 15px;
    border-radius: 20px;
    font-size: 14px;
    transition: all 0.3s ease;
}

.skill-tag:hover {
    background-color: #667eea;
    color: white;
}

/* 联系按钮 */
.contact-btn {
    display: inline-block;
    background-color: #667eea;
    color: white;
    text-decoration: none;
    padding: 12px 30px;
    border-radius: 25px;
    font-weight: 500;
    transition: all 0.3s ease;
    border: 2px solid transparent;
}

.contact-btn:hover {
    background-color: transparent;
    border-color: #667eea;
    color: #667eea;
}

/* 响应式设计 */
@media (max-width: 480px) {
    .card {
        padding: 30px 20px;
    }
    
    .name {
        font-size: 24px;
    }
    
    .title {
        font-size: 16px;
    }
}
```
