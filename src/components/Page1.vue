<template>
    <div class="fundo1" >
        <img style="height: 100%" src="../assets/squareFrameH.jpg" alt="Square image">
     
    </div>
    <div class="fundo2" >
        <img src="../assets/squareFrameV.jpg" alt="Square image">
     
    </div>
    <div class="scratch">
            <img style="height: 450px" src="../assets/scratch.png" alt="Square image">
        </div>
</template>

<style>
    @keyframes scratchanim {
        0%   {left:0%; top:0;}
        100% {left:100%; top:0;}
    }
    .fundo1{    
        background: green;
    }

.scratch {
        position: absolute;
        animation-name: scratchanim;
        animation-duration: 5s;
        animation-delay: 0s;
        animation-iteration-count: infinite;
        animation-direction: normal;
        z-index: 99;
        top: 35%;
}
    .fundo2.img{
        height: 100%
    }
    .fundo2{
        display:none;
}
    @media(max-width:1080px){
        
        .fundo1{
            display:none;
        }
        .fundo2{
        display:inline;
        }
        .fundo2.img{
        width: 100%
    }
    }
</style>

