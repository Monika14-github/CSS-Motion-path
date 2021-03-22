# CSS-Motion-path
....html....
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <div class="wrapper">
  <div class="obj"></div>
<!--  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 515.8 168.1">
  <path stroke="#000" stroke-miterlimit="10" d="M.4 84.1s127.4 188 267.7 0 247.3 0 247.3 0"/>
</svg> -->
</div>
  </body>
</html>
....css.....
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 2rem;
  min-height: 100vh;
  background-color: blueviolet;
  display: flex;
  justify-content: center;
}

.wrapper {
  width: 500px;
  margin: 1rem;
}

.obj {
  offset-path: path('M.4 84.1s127.4 188 267.7 0 247.3 0 247.3 0');
  offset-distance: 0;
  animation: move 2000ms infinite alternate;
  width: 1.2rem;
  height: 1.2rem;
  border-radius: 50%;
  background-color: greenyellow;
}

@keyframes move {
  to {
    offset-distance: 100%;
  }
}
