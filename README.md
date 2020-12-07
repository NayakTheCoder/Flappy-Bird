<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .top{
            position: absolute;
            width: 60px;
            height: 350px;
            top: 0;
            right: 0;
            background-color: red;
        }
        .bottom{
             position: absolute;
            width: 60px;
            height: 200px;
            bottom: 0;
            right: 0;
            background-color: red;
        }
    </style>
</head>
<body>
    <div id="contain">
 
    </div>
</body>
<script>
    let contain = document.getElementById("contain");
    let moveleft;
    let speed = 0;
    let speed1 = 0;
    function generatingobstacles(){

let position = 1200;
const obstacle = document.createElement("div");
const obstacle2 = document.createElement("div");
obstacle.className = "top";
obstacle2.className = "bottom";
contain.appendChild(obstacle);
contain.appendChild(obstacle2);

let topheight = Math.floor(Math.random()*381)+40;
        let bottomheight = Math.floor(Math.random()*231)+40;

obstacle.style.left = position + "px";
obstacle2.style.left = position + "px";

obstacle.style.height = topheight + "px";
       obstacle2.style.height = bottomheight + "px";

let moveleft = setInterval(function(){
    position -= 6;
    obstacle.style.left = position + "px";
    obstacle2.style.left = position + "px";

    
    /*if(position > 0&&position<66&&bottom<60){
        contain.removeChild(obstacle);
        clearInterval(moveleft);
        //alert("gameOver");
        gameOvertrue = true;
        over.innerHTML = "game over!!!";
        over.style.display = "block";
        dino.style.display = "none"
        contain.style.display = "none";
    }*/
},20);

setTimeout(generatingobstacles , 1000);
    
/*if(gameOvertrue === false){
   let randomTime = Math.random() * 4000;
    setTimeout(generatingobstacles , randomTime);
    
    }*/


}
generatingobstacles();
    /*function start(){
        const wall_1 = document.createElement("div");
        const wall_2 = document.createElement("div");

       /* wall_1.style.right = speed + "px";
        wall_2.style.right = speed + "px";*/

        /*contain.appendChild(wall_1);
        contain.appendChild(wall_2);

        let topheight = Math.floor(Math.random()*381)+40;
        let bottomheight = Math.floor(Math.random()*231)+40;

        moveleft = setInterval(function(){
             speed += 3;
             speed1 += 3
             wall_1.style.right = speed + "px";
             wall_2.style.right = speed1 + "px";
        } ,20);
      
        wall_1.style.height = topheight + "px";
        wall_2.style.height = bottomheight + "px";

        wall_1.className = "top";
        wall_2.className = "bottom";

        setTimeout(start , 2000);
    }*/
    
        //start();
    
</script>
</html>
