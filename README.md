<head>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>

<div class="flower">
    <div class="f-wrapper">
        <div class="flower__line"></div>
        <div class="f">
            <div class="flower__leaf flower__leaf--1"></div>
            <div class="flower__leaf flower__leaf--2"></div>
            <div class="flower__leaf flower__leaf--3"></div>
            <div class="flower__leaf flower__leaf--4"></div>
            <div class="flower__leaf flower__leaf--5"></div>
            <div class="flower__leaf flower__leaf--6"></div>
            <div class="flower__leaf flower__leaf--7"></div>
            <div class="flower__leaf flower__leaf--8 flower__fall-down--yellow"></div>
        </div>
    </div>

    <div class="f-wrapper f-wrapper--2">
        <div class="flower__line"></div>
        <div class="f">
            <div class="flower__leaf flower__leaf--1"></div>
            <div class="flower__leaf flower__leaf--2"></div>
            <div class="flower__leaf flower__leaf--3"></div>
            <div class="flower__leaf flower__leaf--4"></div>
            <div class="flower__leaf flower__leaf--5"></div>
            <div class="flower__leaf flower__leaf--6"></div>
            <div class="flower__leaf flower__leaf--7"></div>
            <div class="flower__leaf flower__leaf--8 flower__fall-down--pink"></div>
        </div>
    </div>

    <div class="f-wrapper f-wrapper--3">
        <div class="flower__line"></div>
        <div class="f">
            <div class="flower__leaf flower__leaf--1"></div>
            <div class="flower__leaf flower__leaf--2"></div>
            <div class="flower__leaf flower__leaf--3"></div>
            <div class="flower__leaf flower__leaf--4"></div>
            <div class="flower__leaf flower__leaf--5"></div>
            <div class="flower__leaf flower__leaf--6"></div>
            <div class="flower__leaf flower__leaf--7"></div>
            <div class="flower__leaf flower__leaf--8 flower__fall-down--purple"></div>
        </div>
    </div>
    <div class="flower__glass"></div>
</div>

*,
*::after,
*::before{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

:root{
    --color-bg: linear-gradient(to top,#040214,#140707);
    --color-glass:linear-gradient(to left,#6c83ac,#150f167c);
    --color-water:linear-gradient(to left,#002b7c,#07033b);
}

body{
    background-image:var(--color-bg);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items:flex-end;
    overflow: hidden;
}

.flower{
    position: relative;
}

.flower__glass{
    width:20vmin;
    height: 30vmin;
    background-image: var(--color-glass);
    clip-path: polygon(0 0, 100% 0, 85% 100%, 15% 100%);
    opacity: .8;
    position: relative;
}

.flower__glass::after{
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: #182843;
    width: 100%;
    height: 2vmin;
}

.flower__glass::before{
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    background-image: var(--color-water);
    width: 100%;
    height: 15vmin;
}

.f-wrapper{
    position: absolute;
    left: 45%;
    bottom: 2vmin;
}

.f-wrapper--2{
    left: 50%;
    bottom: 5%;
    transform-origin: 10% left;
    transform: rotate(20deg);
}

.f-wrapper--3{
    left: 30%;
    bottom: 5%;
    transform-origin: 10% left;
    transform: rotate(-10deg);
}

.f-wrapper--3 .flower__line{
    height: 45vmin;
    position: relative;
}

.f-wrapper--3 .flower__line::after{
    content: '';
    position: absolute;
    left:0;
    top: 0;
    width: 6vmin;
    height: 6vmin;
    transform: translate(-69%,-30%) rotate(-5deg);
    border-radius:10vmin 10vmin 0 0;
    border: 2vmin solid  #104d4e;
    border-bottom: transparent;
    border-left: transparent;
}

.f-wrapper--3 .flower__line::before{
    content: '';
    position: absolute;
    left:-40%;
    top: -1%;
    width: 6vmin;
    height: 2vmin;
    transform-origin: right;
    transform: translate(-100%,-80%) rotate(-20deg);
    background-color: #104d4e;
    border-radius: 2vmin;
}

.f-wrapper--3 .flower__line{
    background-image: linear-gradient(to top,#142544,#104d4e);
}


.f-wrapper--2 .flower__line{
    height: 45vmin;
}

.f-wrapper--2 .f{
    transform: translateX(-50%) rotate(20deg);
}

.f-wrapper--3 .f{
    transform: translate(-350%,-50%) rotate(-120deg);
}

.f-wrapper--2 .flower__leaf:not(:first-child){
    width: 3.8vmin;
    height: 10vmin;
    background-image: linear-gradient(to bottom, #ff0000 ,#e61b1b, #c70404 99%);
}

.f-wrapper--3 .flower__leaf:not(:first-child){
    width: 3.8vmin;
    height: 10vmin;
    background-image: linear-gradient(to bottom, #e924ae ,#ff7eb4, #e95ea3 99%);
}

.f-wrapper--3 .flower__leaf--1{
    width: 8vmin;
    height: 10vmin;
    bottom: 2vmin;
    background-color: #e02b95;
}

.f-wrapper--2 .flower__leaf--1{
    width: 8vmin;
    height: 10vmin;
    bottom: 2vmin;
    background-color: #eb5252;
}

.f-wrapper--2 .f .flower__leaf--8{
    width: 10vmin;
    height: 9vmin;
    bottom: 3vmin;
    left: -30%;
    transform: rotate(-50deg);
    background-image: linear-gradient(to left bottom, #ff4343 ,#4d1337);;
}

.f-wrapper--3 .f .flower__leaf--8{
    width: 10vmin;
    height: 9vmin;
    left: -10% !important;
    background-image: linear-gradient(to left bottom, #fd37f3 ,#9e0096);;
}

.flower__line{
    width: 2vmin;
    height: 56vmin;
    background-image: linear-gradient(to left top,#82fdff 20%,#142544,#104d4e);
    border-radius: 4vmin;
}

.f{
    position: absolute;
    top: 1vmin;
    left: 50%;
    transform: translateX(-50%) rotate(-10deg);
    width: 2vmin;
    height: 2vmin;
}


.flower__leaf{
    position: absolute;
    left: 50%;
    bottom: 2vmin;
    transform: translateX(-50%);
    width: 5vmin;
    height: 14vmin;
    background-image: linear-gradient(to bottom, #00b7ff ,#468aca, #1a233a 99%);
    clip-path: ellipse(50% 50% at 50% 50%);
    transform-origin: center bottom;
    animation: open-flower 2s 1s backwards;
}

.flower__leaf--1{
    width: 10vmin;
    height: 12vmin;
    bottom: 3vmin;
    border-radius: 50% 50% 50% 50% / 80% 80% 20% 20%;
    background-color: #034a6b;
    background-image: none;
    animation: open-flowe--middle  1.4s 1s backwards;
}

.flower__leaf--2{
    transform: translateX(-50%) rotate(-30deg);
}
.flower__leaf--3{
    transform: translateX(-50%) rotate(-50deg);
}
.flower__leaf--4{
    transform: translateX(-50%) rotate(-70deg);
}

.flower__leaf--5{
    transform: translateX(-50%) rotate(30deg);
}

.flower__leaf--6{
    transform: translateX(-50%) rotate(50deg);
}

.flower__leaf--7{
    transform: translateX(-50%) rotate(70deg);
}

.flower__leaf--8{
    width: 13vmin;
    height: 11vmin;
    bottom: 6vmin;
    left: -30%;
    border-radius: none;
    clip-path: none;
    border-radius: 10vmin 2vmin 10vmin 2vmin;
    transform: rotate(-55deg);
    background-image: linear-gradient(to left bottom, #11e9de ,#007981,#005791 98%);
}

.flower__fall-down--yellow{
    animation: flower-fall-down-yellow  8s 1.2s linear forwards;
}

.flower__fall-down--pink{
    animation: flower-fall-down-pink  5s 1.2s linear forwards;
}

.flower__fall-down--purple{
    bottom: 4vmin;
    animation:flower-fall-down-purple  6s 1.2s linear forwards, flower-falling 6s 7.2s linear infinite;
}


@keyframes open-flower{
        0%{
            transform:  translateX(-50%) rotate(0);
        }
}

@keyframes open-flowe--middle {
    0%{
        opacity: 0;
        transform: translateX(-50%) scale(0);
    }
}

@keyframes flower-fall-down-pink {

    0%{
        transform: rotate(-55deg);
    }

    50%{
        transform: rotateX(-100deg);
    }

    100%{
        transform:translate(2vmin,28vmin);
    }

}

@keyframes flower-fall-down-yellow {

    0%{
        transform: rotate(-55deg);
    }

    50%{
        bottom: 3vmin;
        transform: rotateX(-100deg);
    }

    100%{
        transform:translate(2vmin,70vmin) rotate(150deg);
    }

}

@keyframes flower-fall-down-purple {

    0%{
        transform: rotate(-50deg);
    }

    25%{
        bottom: 1vmin ;
        transform: rotateX(-100deg);
        perspective: 0px;
    }

    50%{
        perspective: 0px;
        transform:translate(-30vmin,2vmin) rotate(90deg);
    }

    75%{
        perspective: 0px;
        transform:translate(-34vmin,-2vmin);
    }

    100%{
        transform-origin: center;
        transform:translate(-34vmin,-2vmin) rotateY(-80deg) rotateX(35deg);
    }

}

@keyframes flower-falling {
    0%,100%{
        transform-origin: center;
        transform:translate(-34vmin,-2vmin) rotateY(-80deg) rotateX(35deg);
    }

    25%{
        transform-origin: center;
        transform:translate(-34.4vmin,-2vmin) rotateY(-84deg) rotateX(35deg);
    }

    50%{
        transform-origin: center;
        transform:translate(-32vmin,-4.2vmin) rotateY(-80deg) rotateX(35deg);
    }

    75%{
        transform-origin: center;
        transform:translate(-36vmin,1.1vmin) rotateY(-80deg) rotateX(35deg);
    }
}
