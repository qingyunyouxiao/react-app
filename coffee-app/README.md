## React 2

继续学习。

**step 1**

```bash
yarn create coffee-app coffee-app
cd coffee-app
echo "SKIP_PREFLIGHT_CHECK=true" > .env
yarn start
```

**step 2**

App.js

```jsx
import './App.css';

function App() {
  return (
    <div className="App">
      {/* 标题栏 */}
      <h1>Wombat Coffee Roasters</h1>
      {/* 导航栏 */}
      <ul className="nav-list">
        <li><a href="/">Home</a></li>
        <li><a href="/coffees">Coffees</a></li>
        <li><a href="/brewers">Brewers</a></li>
        <li><a href="/specials">Specials</a></li>
      </ul>
    </div>
  );
}

export default App;
```

App.css

```css
/* 全局基础样式 */
.App {
  margin: 20px;
  font-family: Arial, sans-serif;
}

/* 标题样式 */
h1 {
  font-weight: bold;
  margin-bottom: 20px;
}

/* 列表样式 */
.nav-list {
  list-style-type: disc; /* 实心圆点列表项 */
  margin-left: 40px; /* 列表缩进 */
  padding: 0;
}

/* 列表项样式 */
.nav-list li {
  margin: 5px 0;
}

/* 链接样式 */
.nav-list a {
  color: #0000ee; /* 经典蓝色链接色 */
  text-decoration: underline;
}

/* 鼠标悬浮效果 */
.nav-list a:hover {
  color: #551a8b;
}
```

作者样式覆盖用户代理样式。

**step 3**

App.css

```css
/* 全局基础样式 */
.App {
  margin: 20px;
  font-family: Arial, sans-serif;
}

/* 标题样式 */
h1 {
  font-weight: bold;
  color: #2f4f4f;
  margin-bottom: 20px;
}

/* 列表样式 */
.nav-list {  
    margin-top: 10px;
    list-style: none;
    padding-left: 0;
}

/* 列表项样式 */
.nav-list li {
  display: inline-block;
}

/* 链接样式 */
.nav-list a {
  color: white;
  background-color: #13a4a4;  /* 原始绿色 */
  padding: 5px 15px;
  border-radius: 2px;
  text-decoration: none;
  margin-right: 5px;
  transition: all 0.3s ease;  /* 添加过渡效果 */
}

/* 鼠标悬浮效果 */
.nav-list a:hover {
  background-color: #8B4513;  /* 鼠标悬停时变为咖啡色 */
  /* 可以添加轻微放大效果 */
  transform: scale(1.05);
}
```