# Application4-copy2
#Website using flask

#Home
{%extends "layout.htm"%}
{%block content%}
<div class="home">
    <h1>My HomePage</h1>
    <p>This is a test website.</p>
</div>    
{%endblock%}

#About
{%extends "layout.htm"%}
{%block content%}
<div class="about">
    <h1>My About Page</h1>
    <p>This is a test website.</p>
</div>
{%endblock%}

#Layout
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flask App</title>
    <link rel="stylesheet" href={{url_for('static', filename='css/main.css')}}>
</head>
<body>
    <header>
        <div class="container">
            <h1 class="logo">ALIEN's Web App</h1>
            <strong><nav>
                <ul class="menu">
                    <li><a href="{{ url_for('home') }}">Home</a></li>
                    <li><a href="{{ url_for('about') }}">About</a></li>
                </ul>    
            </nav></strong>
        </div>
    </header>
    <div class="container">
        {%block content%}
        {%endblock%}
    </div>
</body>
</html>

#CSS
body{
    margin :0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    color: #444;
}

header{
    background-color: #DFB887;
    height: 35px;
    width: 100%;
    opacity: .9;
    margin-bottom: 10px;
}

header h1.logo{
    margin: 0;
    font-size: 1.7em;
    color: #fff;
    text-transform: uppercase;
    float: left;
}

header h1.logo:hover{
    color: #fff;
    text-decoration: none;
}

.container{
    width: 1200px;
    margin: 0 auto;
}

div.home{
    padding: 10px 0 30px 0;
    background-color: #E6E6FA;
    -webkit-border-radius: 6px;
        -moz-border-radius: 6px;
            border-radius: 6px;
}

div.about{
    padding: 10px 0 30px 0;
    background-color: #E6E6FA;
    -webkit-border-radius: 6px;
        -moz-border-radius: 6px;
            border-radius: 6px;
}

h2{
    font-size: 1.7em;
    font-weight: 100;
    margin-top: 40px;
    text-align: center;
    letter-spacing: -2px;
}

h3{
    font-size: 1.7em;
    font-weight: 100;
    margin-top: 30px;
    text-align: center;
    letter-spacing: -1px;
    color: #999;
}

.menu{
    float: right;
    margin-top: 8px;
}

.menu li{
    display: inline;
}

.menu li + li{
    margin-left: 35px;
}

.menu li a{
    color: #444;
    text-decoration: none;
}
