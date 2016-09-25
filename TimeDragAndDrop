# DragAndDrop
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.2/jquery.min.js"></script>
    <script src="https://code.jquery.com/ui/1.11.4/jquery-ui.js"></script>

    <style>
        #subj{
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: orange;
            text-align: center;

        }
        #time{
            text-align: center;

        }


    </style>
</head>
<body>
<div id="subj">
    <br>Your time is <br>
    <div id="time"></div></div>

<script>
    var t;
    function dragAndDrop(elem){
        elem.onmousedown=function (e) {

            var gcs=getComputedStyle(elem);
            var top0=cutTwo(gcs.top);
            var left0=cutTwo(gcs.left);

            var mx0=e.clientX;
            var my0=e.clientY;

            elem.style.cursor="pointer";

            elem.onmousemove=function (ev) {

                elem.style.top=(top0+(ev.clientY-my0)+"px");
                elem.style.left=(left0+(ev.clientX-mx0)+"px");

            }
            var dmu =document.onmouseupouseup;
            document.onmouseup=function () {
                elem.style.cursor="default";
                elem.onmousemove=null;
                document.onmouseup=dmu;


            }


            }








    }

    function cutTwo(str) {
    return parseInt(str.substr(0, str.length-2));
    }

    dragAndDrop(document.getElementById("subj"));

    setInterval(function(){
        var d=new Date();

        t=(addzero(d.getHours())+":"+addzero(d.getMinutes())+":"+addzero(d.getSeconds()));
        document.getElementById("time").innerHTML=t;
    },1000);
    function addzero(v){
        var str="";
        if (v<10)str="0";
        return str+v.toString();
    }






</script>




</body>
</html>
