<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Geometric Desig </title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #8B1538, #2D1B69);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
        }

        .container {
            width: 350px;
            height: 550px;
            background: linear-gradient(135deg, #FF8C42, #FF7A35);
            border-radius: 25px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        /* Top left curved section with diagonal lines */
        .top-left-section {
            position: absolute;
            top: 0;
            left: 0;
            width: 160px;
            height: 160px;
            background: #2D3561;
            border-radius: 0 0 160px 0;
        }

        /* Diagonal lines over the curved section */
        .diagonal-lines {
            position: absolute;
            top: 20px;
            left: -10px;
            width: 180px;
            height: 180px;
        }

        .line {
            width: 120px;
            height: 6px;
            background: #2D3561;
            margin: 10px 0;
            transform: rotate(-45deg);
            transform-origin: left center;
        }

        /* Red triangle - top center */
        .red-triangle {
            position: absolute;
            top: 70px;
            left: 200px;
            width: 0;
            height: 0;
            border-left: 25px solid transparent;
            border-right: 25px solid transparent;
            border-bottom: 40px solid #E74C3C;
        }

        /* Top right circle */
        .circle-top-right {
            position: absolute;
            top: 50px;
            right: 30px;
            width: 70px;
            height: 70px;
            background: #2D3561;
            border-radius: 50%;
        }

        /* Middle right large circle */
        .circle-middle-right {
            position: absolute;
            top: 180px;
            right: 30px;
            width: 100px;
            height: 100px;
            background: #2D3561;
            border-radius: 50%;
        }

        /* Left side concentric circles */
        .concentric-container {
            position: absolute;
            bottom: 200px;
            left: 50px;
            width: 90px;
            height: 90px;
        }

        .concentric-ring {
            position: absolute;
            border: 5px solid #2D3561;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .ring-1 { width: 18px; height: 18px; }
        .ring-2 { width: 36px; height: 36px; }
        .ring-3 { width: 54px; height: 54px; }
        .ring-4 { width: 72px; height: 72px; }
        .ring-5 { width: 90px; height: 90px; }

        /* Red L-shaped element */
        .l-element {
            position: absolute;
            bottom: 100px;
            left: 30px;
        }

        .l-vertical-part {
            width: 18px;
            height: 160px;
            background: #E74C3C;
            position: absolute;
            bottom: 0;
            left: 0;
        }

        .l-horizontal-part {
            width: 100px;
            height: 18px;
            background: #E74C3C;
            position: absolute;
            bottom: 0;
            left: 0;
        }

        /* Small blue square */
        .blue-square {
            position: absolute;
            bottom: 160px;
            right: 100px;
            width: 22px;
            height: 22px;
            background: #2D3561;
        }

        /* Right side horizontal line */
        .horizontal-line-right {
            position: absolute;
            bottom: 170px;
            right: 40px;
            width: 50px;
            height: 4px;
            background: #2D3561;
        }

        /* Bottom dashed circle with inner red circle */
        .dashed-circle-container {
            position: absolute;
            bottom: 60px;
            right: 70px;
            width: 70px;
            height: 70px;
            border: 3px dashed #2D3561;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .inner-red-circle {
            width: 35px;
            height: 35px;
            background: #E74C3C;
            border-radius: 50%;
        }

        /* Middle horizontal lines */
        .horizontal-line-1 {
            position: absolute;
            bottom: 140px;
            left: 160px;
            width: 70px;
            height: 3px;
            background: #2D3561;
        }

        .horizontal-line-2 {
            position: absolute;
            bottom: 125px;
            left: 160px;
            width: 50px;
            height: 3px;
            background: #2D3561;
        }

        /* Bottom long horizontal line */
        .bottom-line {
            position: absolute;
            bottom: 30px;
            left: 30px;
            width: 180px;
            height: 5px;
            background: #2D3561;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Top left curved section -->
        <div class="top-left-section"></div>
        
        <!-- Diagonal lines crossing the curved section -->
        <div class="diagonal-lines">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>

        <!-- Red triangle at top -->
        <div class="red-triangle"></div>

        <!-- Top right circle -->
        <div class="circle-top-right"></div>

        <!-- Middle right large circle -->
        <div class="circle-middle-right"></div>

        <!-- Concentric circles on left -->
        <div class="concentric-container">
            <div class="concentric-ring ring-1"></div>
            <div class="concentric-ring ring-2"></div>
            <div class="concentric-ring ring-3"></div>
            <div class="concentric-ring ring-4"></div>
            <div class="concentric-ring ring-5"></div>
        </div>

        <!-- Red L-shaped element -->
        <div class="l-element">
            <div class="l-vertical-part"></div>
            <div class="l-horizontal-part"></div>
        </div>

        <!-- Small blue square -->
        <div class="blue-square"></div>

        <!-- Right side horizontal line -->
        <div class="horizontal-line-right"></div>

        <!-- Dashed circle with inner red circle -->
        <div class="dashed-circle-container">
            <div class="inner-red-circle"></div>
        </div>

        <!-- Middle horizontal lines -->
        <div class="horizontal-line-1"></div>
        <div class="horizontal-line-2"></div>

        <!-- Bottom horizontal line -->
        <div class="bottom-line"></div>
    </div>
</body>
</html>
