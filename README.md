# TEAVELER.github.io
<!DOCTYPE html>
<html>
  <head>
    <link href="styles/style.css" rel="stylesheet">
    <link href="https://fonts.font.im/css?family=Open+Sans" rel="stylesheet" type="text/css">

    <meta charset="utf-8">
    <title>第一次实验</title>
    
  </head>
  <body>
    <h1>鬼灭 美爆了！</h1>
    <img src="images/firefox-icon.png" alt="Firefox 标志：一个标志的美女">

    <p>Mozilla 是一个全球社区，这里聚集着来自五湖四海的</p>

    <ul>
      <li>技术人员</li>
      <li>思考者</li>
      <li>建造者</li>
    </ul>

    <p>我们致力于让 Internet 保持活力，保持畅通，人人皆可贡献，人人皆可创造。我们坚信：开放平台的协作对于人的发展至关重要，也决定着我们共同的未来。</p>

    <p>为了达成我们共同的理想，我们遵循一系列的价值观和理念，请参阅 <a href="https://www.mozilla.org/zh-CN/about/manifesto/">Mozilla 宣言</a>。</p>
  </body>
</html>
let myImage = document.querySelector('img');

myImage.onclick = function() {
    let mySrc = myImage.getAttribute('src');
    if(mySrc === 'images/firefox-icon.png') {
      myImage.setAttribute('src', 'images/firefox2.png');
    } else {
      myImage.setAttribute('src', 'images/firefox-icon.png');
    }
}
let myButton = document.querySelector('button');
let myHeading = document.querySelector('h1');
function setUserName() {
    let myName = prompt('请输入你的名字。');
    if(!myName) {
      setUserName();
    } else {
      localStorage.setItem('name', myName);
      myHeading.textContent = 'Mozilla 酷毙了，' + myName;
    }
  }
  
  if(!localStorage.getItem('name')) {
    setUserName();
  } else {
    let storedName = localStorage.getItem('name');
    myHeading.textContent = 'Mozilla 酷毙了，' + storedName;
  }
  myButton.onclick = function() {
    setUserName();
 }
 html {
  font-size: 10px;
  font-family: 'Noto Sans SC', sans-serif;
  background-color: #00879f8e;
}

body {
  width: 600px;
  margin: 0 auto;
  background-color: #d8bc1e86;
  padding: 0 40px 20px 40px;
  border: 5px solid black;
}

h1 {
  font-size: 60px;
  text-align: center;
  margin: 0;
  padding: 20px 0;
  color: #00539F;
  text-shadow: 3px 3px 1px black;
}

p, li {
  font-size: 16px;
  line-height: 2;
  letter-spacing: 1px;
}

img {
  display: block;
  margin: 0 auto;
}


   
