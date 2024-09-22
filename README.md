# ToDo-list
This is simple Todo list using HTML CSS JS
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            background-color: aqua;
        }
        h1{
            font-family:'Courier New', Courier, monospace;
            font-weight: bolder;
        }
        input{
            height: 50px;
            width: 500px;
            border: 8px solid blue;
            font-size: x-large;
            background-color: black;
            color: aliceblue;
        }
        #list{
            border: 8px solid black;
            background-color: darkgrey;
            height: 100%;
            width: 500px;
            font-size: x-large;
        }
    </style>
</head>
<body>
    <h1>Write your Work to do in a day below:</h1>
    <input type="text" id="write" placeholder="Write Here">
    <ul id="list" style="list-style-type: decimal;">
          <h1>Your Todo list</h1>
    </ul>
</body>
<script>
    const w=document.querySelector('#write');
    const l=document.querySelector('#list');
    w.addEventListener("keyup",function(event){
        if(event.key=="Enter"){
            let list=document.createElement("li");
            let butt=document.createElement("button")
            list.innerHTML=`${this.value}`;
            butt.style.height="50px";
            butt.style.width="150px";
            butt.innerText='Task Completed';
            butt.style.backgroundColor="blue";
            butt.style.border="5px solid black";
            butt.style.backgroundColor="blue";
            butt.style.fontSize="large";
            let br=document.createElement("br");
            l.appendChild(list);
            l.appendChild(butt);
            l.appendChild(br);
            butt.addEventListener('click',function(event){
                list.innerHTML='';
                butt.innerHTML='';
                butt.style='';
        
            })

            this.value=''
        }
    })
</script>
</html>
