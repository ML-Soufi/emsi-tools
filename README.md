This file is mandatory in all Holberton School projects

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://ajax.googleapis.com/ajax/libs/jqueryui/1.10.3/themes/smoothness/jquery-ui.css" rel="stylesheet" type="text/css"/>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.10.3/jquery-ui.min.js"></script>

    <title>Document</title>
    <style>
        #container{
            display: block;
            position: relative;
            height: 200px;
            width: 70%;
            border: solid 1px red;
        }

        #slide{
            display: block;
            position: absolute;
            height: 20px;
            width: 20px;
            background: red; 
        }

        #slide1{
            display: block;
            position: absolute;
            height: 20px;
            width: 20px;
            background: black; 
        }

        #slide2{
            display: block;
            position: absolute;
            height: 20px;
            width: 20px;
            background: green; 
        }
    </style>
</head>
<body>
    <div id="container">
        <div id="slide" class="toDrag"></div>
        <div id="slide1" class="toDrag"></div>
        <div id="slide2" class="toDrag"></div>
    </div>
    <script>
        $( ".toDrag" ).draggable({
            containment: '#container',
            drag: function(event) {
                var top = $(this).position().top;
                var left = $(this).position().left;
            },
        });
    </script>
</body>
</html>
