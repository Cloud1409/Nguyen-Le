# Nguyen-Le
!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
    <title>Document</title>
<style>
    *{
        margin: 0;
        padding :0;
    }
    body{
        position: relative;
        background-color: rgb(243, 232, 232);
        overflow: hidden;
    }
    h1{
        font-size: 100px;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        color: rgb(86, 44, 204);
        text-align: center;
        display: block;
        padding-top: 100px;
        font-style: italic;
        font-weight: bold;
    }
    p{
        color: red;
        text-align: center;
        font-size: 80px;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        font-weight: bold;
    }
</style>
<script>
    function getRandom(min,max){
        return Math.floor(Math.random()*(max-min)+min);
    }
    $(document).ready(function(){
        setInterval(function(){
        var screenHeight = $(document).height();
        var screenWidth = $(document).width();
        var startleft = getRandom(0,screenWidth);
        var timerun = getRandom(4000,6000);
        var opacityR = Math.random()*(1-0.2)+0.2;
        var sizeR = getRandom(4,50);
        var endleft = getRandom(startleft-200,startleft+200);
        var snow= document.createElement('span');
        $(snow).addClass('snow-item fa fa-heart').css({
            'position':'absolute',
            'top':0,
            'color':'#ff0000',
            'left':startleft,
            'z-index':'auto',
            'opacity':opacityR,
            'display':'block',
            'font-size':sizeR+'px'
        })
        .appendTo('body')
        .animate({
            'top':screenWidth-sizeR,
            'left':endleft,
        },{
            duration: timerun,
            easing:'linear',
            conplete: function(){
                $(this).fadeOut('fast',function(){
                    $(this).remove();
                });
            }
        });
    },500);
});
</script>
</head>
<body>
   <h1><div class="fa fa-smile-o"></div></h1>
    <h1>Alone</h1>
    <p>14</p>
    <p>09</p>
</body>
</html>
 
