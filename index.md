<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>Выбор случайного цвета</title>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>
 
            <script type="text/javascript">
                $(document).ready(function() {
                
                $("#addBlock").click(function () {
                    var randName = GetNumber(1, 700);
                    $('#blocks').prepend("<div class='block " + randName +"'>" + randName + "</div>");
                    
                    $('.' + randName).css("background", "#" + GetNumber(0, 9) + GetNumber(0, 9) + GetNumber(0, 9) + GetNumber(0, 9) + GetNumber(0, 9) + GetNumber(0, 9));
                                     
                });
                    
                    function GetNumber (min, max) {
                        return Math.floor(Math.random() * (max-min+1)) + min;
                    }    
                        });
          
            </script>
<style>
    .block {
        width: 200px;
        height: 200px;
        margin-bottom: 20px;
        border-radius: 5px;
        text-align: center;
    }     
</style>
    
</head>
<body>
     <button id="addBlock">Добавить блок</button><br />
     <div id="blocks"></div>
    
</body>
</html>
