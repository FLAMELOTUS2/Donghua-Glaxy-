<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Donghua Galaxy</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
    background:#0f0f0f;
    font-family:Arial, sans-serif;
    color:#fff;
}

header{
    text-align:center;
    padding:25px;
    background:linear-gradient(90deg,#ff0000,#990000);
}

header h1{
    font-size:28px;
}

.container{
    max-width:1300px;
    margin:auto;
    padding:20px;
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:25px;
}

.card{
    background:#1c1c1c;
    border-radius:12px;
    overflow:hidden;
    transition:0.3s;
    box-shadow:0 0 15px rgba(255,0,0,0.2);
}

.card:hover{
    transform:translateY(-8px);
    box-shadow:0 0 25px rgba(255,0,0,0.6);
}

.card img{
    width:100%;
    height:220px;
    object-fit:cover;
}

.card-content{
    padding:15px;
}

.card-content h2{
    font-size:18px;
    margin-bottom:10px;
}

.episodes{
    display:flex;
    flex-wrap:wrap;
    gap:8px;
}

.episodes a{
    background:#ff0000;
    padding:6px 12px;
    border-radius:20px;
    text-decoration:none;
    color:#fff;
    font-size:13px;
    transition:0.3s;
}

.episodes a:hover{
    background:#cc0000;
}
</style>
</head>
<body>

<header>
<h1>🔥 Donghua Episode List</h1>
</header>

<div class="container">

<!-- Card 1 -->
<div class="card">
<img src="https://image2url.com/r2/default/images/1771058183506-43ecf5b9-b619-4e11-80c9-01d84c30a296.jpg">
<div class="card-content">
<h2>Battle Through The Heavens</h2>
<div class="episodes">
<a href="player.html?id=x9yxge2">Ep 186</a>
<a href="player.html?id=x9abc123">Ep 185</a>
<a href="player.html?id=x9xyz456">Ep 184</a>
</div>
</div>
</div>

<!-- Card 2 -->
<div class="card">
<img src="https://via.placeholder.com/400x250">
<div class="card-content">
<h2>Soul Land</h2>
<div class="episodes">
<a href="player.html?id=x9aaa111">Ep 141</a>
<a href="player.html?id=x9bbb222">Ep 140</a>
<a href="player.html?id=x9ccc333">Ep 139</a>
</div>
</div>
</div>

<!-- Card 3 -->
<div class="card">
<img src="https://via.placeholder.com/400x250">
<div class="card-content">
<h2>Perfect World</h2>
<div class="episodes">
<a href="player.html?id=x9ddd444">Ep 257</a>
<a href="player.html?id=x9eee555">Ep 256</a>
<a href="player.html?id=x9fff666">Ep 255</a>
</div>
</div>
</div>

<!-- Card 4 -->
<div class="card">
<img src="https://via.placeholder.com/400x250">
<div class="card-content">
<h2>Throne of Seal</h2>
<div class="episodes">
<a href="player.html?id=x9ggg777">Ep 198</a>
<a href="player.html?id=x9hhh888">Ep 197</a>
<a href="player.html?id=x9iii999">Ep 196</a>
</div>
</div>
</div>

</div>

