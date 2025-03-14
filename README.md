<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Animation</title>
    <style>
        .box {
            width: 100px;
            height: 100px;
            background-color: blue;
            position: absolute;
            top: 50px;
            left: 0;
        }
    </style>
</head>
<body>
    <button onclick="moveBox()">Move</button>
    <div class="box" id="box"></div>

    <script>
        function moveBox() {
            let box = document.getElementById("box");
            let position = 0;
            let interval = setInterval(frame, 10);

            function frame() {
                if (position >= 300) {
                    clearInterval(interval);
                } else {
                    position++;
                    box.style.left = position + "px";
                }
            }
        }
    </script>
</body>
</html>
