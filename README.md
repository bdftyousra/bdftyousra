
<!DOCTYPE html>
<html>
<head>
<style>
/*

Tutorial:
https://www.roboleary.net/animation/2022/10/31/how-to-make-a-slick-animation-schitts-creek-title-sequence.html

Part of Title Sequences collection:
https://codepen.io/collection/nNmwgP

Source code:
https://github.com/robole/title-sequences

*/

@import url("https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600");

:root {
  --bar-scale-y: 0;
  --sparkle-color: rgb(253 244 215 / 40%);
}

@keyframes pop-word {
  to {
    transform: rotateX(0);
  }
}

@keyframes show {
  to {
    opacity: 1;
  }
}

@keyframes bar-scale {
  to {
    transform: scaleY(1);
  }
}

@keyframes sparkle {
  0% {
    transform: scale(0);
  }

  60% {
    transform: scale(1) translate(4px, 1px) rotate(8deg);
  }

  100% {
    transform: scale(0) translate(4px, 1px) rotate(8deg);
  }
}

@keyframes shimmer {
  to {
    text-shadow: 0 0 8px red;
  }
}

body {
  display: grid;
  height: 100vh;

  background-color: black;
  place-items: center;
}

h1 {
  color: white;
  font-family: "Playfair Display", Vidaloka, serif;
  font-size: 8rem;

  line-height: 0.85;
  perspective: 500px;
}

.word {
  display: block;

  animation: show 0.01s forwards, pop-word 1.5s forwards;
  animation-timing-function: cubic-bezier(0.14, 1.23, 0.33, 1.16);
  opacity: 0;

  transform: rotateX(120deg);
  transform-origin: 50% 100%;
}

.word:nth-of-type(2) {
  padding: 0 2rem;

  animation-delay: 1.5s;

  color: gold;
}





@media screen and (max-width: 600px) {
  h1 {
    font-size: 5rem;
  }


}

</style>
</head>
<body>

<h1>
  <span class="word">YOUSRA </span>
  <span class="word">BDFT</span>
</h1>
<img src="https://i.imgur.com/5geGv8j.png" alt="👋 Hi there!" title="👋 Hi there!"/>
</body>
</html>

