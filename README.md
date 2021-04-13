<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="style.css" />
    <title>練習</title>
  </head>
  <body>
    <p>ようこそ<span id="name">テスト</span>さん！</p>
    <p>あなたの運勢は<span id="result">大吉</span>です！</p>
    <img src="omikuji.png">
    <script type="text/javascript" src="omikuji.js"></script>
  </body>
</html>

img {
    height: 100px;
  }
  #name {
    color: blue;
  }
  
  #result {
    color: green;
  }
  
  var name;
var username;
var userresult;

username = prompt("お名前を教えて下さい。");
preusername = "名無し";
if (username == "") {
    document.getElementById("name").innerHTML = preusername;
} else {
    document.getElementById("name").innerHTML = username;
}


var rand = Math.floor( Math.random() * 5);
if (rand == 0) {
  userresult = "大吉";
}
if (rand == 1) {
  userresult = "中吉";
}
if (rand == 2) {
  userresult = "小吉";
}
if (rand == 3) {
  userresult = "吉";
}
if (rand == 4) {
  userresult = "凶";
}
document.getElementById("result").innerHTML = userresult;
