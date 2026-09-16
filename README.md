<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>CSS Grid Layout</title>

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #111;
            min-height: 100vh;

            display: flex;
            justify-content: center;
            align-items: center;

            padding: 30px;
        }

        /* MAIN GRID */

        .container {
            width: 100%;
            max-width: 1350px;
            height: 650px;

            display: grid;

            /* 5 columns */
            grid-template-columns:
                1fr
                1fr
                0.67fr
                1fr
                0.96fr;

            /* 3 rows */
            grid-template-rows:
                1.05fr
                1.25fr
                0.80fr;

            gap: 14px;
        }


        /* BOX COLORS */

        .red {
            background: #ef291f;
        }

        .blue {
            background: #16b8d4;
        }

        .tan {
            background: #ccb97e;
        }

        .white {
            background: #eeeeee;
        }


        /* =========================
           LEFT RED
           ========================= */

        .box1 {
            grid-column: 1;
            grid-row: 1 / 3;
        }


        /* =========================
           TOP BLUE
           ========================= */

        .box2 {
            grid-column: 2;
            grid-row: 1;
        }


        /* =========================
           TOP RED
           ========================= */

        .box3 {
            grid-column: 3 / 5;
            grid-row: 1;
        }


        /* =========================
           RIGHT WHITE
           ========================= */

        .box4 {
            grid-column: 5;
            grid-row: 1;
        }


        /* =========================
           MIDDLE WHITE
           ========================= */

        .box5 {
            grid-column: 2 / 4;
            grid-row: 2;
        }


        /* =========================
           MIDDLE TAN
           ========================= */

        .box6 {
            grid-column: 4;
            grid-row: 2;
        }


        /* =========================
           BOTTOM TAN
           ========================= */

        .box7 {
            grid-column: 1 / 3;
            grid-row: 3;
        }


        /* =========================
           BOTTOM BLUE
           ========================= */

        .box8 {
            grid-column: 3 / 5;
            grid-row: 3;
        }


        /* =========================
           RIGHT RED
           ========================= */

        .box9 {
            grid-column: 5;
            grid-row: 2 / 4;
        }


        /* RESPONSIVE */

        @media (max-width: 800px) {

            body {
                padding: 15px;
            }

            .container {
                height: 80vh;

                gap: 8px;

                grid-template-columns:
                    1fr
                    1fr
                    0.67fr
                    1fr
                    0.96fr;
            }
        }

    </style>

</head>


<body>

    <div class="container">

        <!-- LEFT TALL RED -->
        <div class="red box1"></div>

        <!-- TOP BLUE -->
        <div class="blue box2"></div>

        <!-- TOP RED -->
        <div class="red box3"></div>

        <!-- RIGHT WHITE -->
        <div class="white box4"></div>

        <!-- MIDDLE WHITE -->
        <div class="white box5"></div>

        <!-- MIDDLE TAN -->
        <div class="tan box6"></div>

        <!-- BOTTOM TAN -->
        <div class="tan box7"></div>

        <!-- BOTTOM BLUE -->
        <div class="blue box8"></div>

        <!-- RIGHT TALL RED -->
        <div class="red box9"></div>

    </div>

</body>

</html>
