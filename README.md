<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Animation Effects</title>
  <style>
    * {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }

    body {
      display: flex;
      min-height: 100vh;
      justify-content: center;
      align-items: center;
      background: #000;
    }

    .container {
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      -webkit-box-reflect: below 2px linear-gradient(transparent, #0005);
    }

    .container .box {
      position: relative;
      width: 300px;
      height: 300px;
      background: linear-gradient(
        45deg,
        #00f376 10%,
        transparent 10%,
        transparent 50%,
        #00f376 50%,
        #00f376 60%,
        transparent 60%,
        transparent 100%
      );
      background-size: 40px 40px;
      transform: rotate(calc(var(--i) * 90deg));
      animation: animate 0.3s linear infinite;
    }

    @keyframes animate {
      0% {
        background-position: 0;
      }
      100% {
        background-position: 40px;
      }
    }

    @media only screen and (max-width: 768px) {
      .container .box {
        width: 200px;
        height: 200px;
      }
    }

    @media only screen and (max-width: 480px) {
      .container .box {
        width: 150px;
        height: 150px;
      }
    }
  </style>
</head>

<body>
  <div class="container">
    <div class="box" style="--i:1;"></div>
    <div class="box" style="--i:2;"></div>
  </div>
</body>

</html>
