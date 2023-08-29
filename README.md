- 👋 Hi, I’m Jake T.  ,and this is my Vampeyer git page.

I am now a graduate of the code louisville summer  2022 cohort !!!! 



- 👀 I’m interested in .... coding to earn cash/ teslas/ and miniature single electronic VTols. 
- 🌱 I’m currently learning ... blockchain development for the environment
- 💞️ I’m looking to collaborate on ... My Enviro Securus project with an fullstack environmentalist type
- 📫 How to reach me ... check out my page , download it , links provided!

<!---
Vampeyer/Vampeyer is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>

  <link rel="stylesheet" href="index.css">
<style> 
.clock {
  --_ow: clamp(5rem, 60vw, 40rem);
  --_w: 88cqi;
  --_r: calc((var(--_w) - var(--_sz)) / 2);
  --_sz: 12cqi;

  background: #222;
  block-size: var(--_ow);
  border-radius: 24%;
  container-type: inline-size;
  display: grid;
  font-family: ui-sans-serif, system-ui, sans-serif;
  inline-size: var(--_ow);
  margin-inline: auto;
  place-content: center;
}

.clock-face {
  aspect-ratio: 1;
  background: var(--_bgc, #FFF);
  border-radius: 50%;
  block-size: var(--_w);
  font-size: 6cqi;
  font-weight: 700;
  list-style-type: none;
  inline-size: var(--_w);
  padding: unset;
  position: relative;
}

.clock-face time {
  --_x: calc(var(--_r) + (var(--_r) * cos(var(--_d))));
  --_y: calc(var(--_r) + (var(--_r) * sin(var(--_d))));
  display: grid;
  height: var(--_sz);
  left: var(--_x);
  place-content: center;
  position: absolute;
  top: var(--_y);
  width: var(--_sz);
}

.clock-face time:nth-child(1) { --_d: 270deg; }
.clock-face time:nth-child(2) { --_d: 300deg; }
.clock-face time:nth-child(3) { --_d: 330deg; }
.clock-face time:nth-child(4) { --_d: 0deg; }
.clock-face time:nth-child(5) { --_d: 30deg; }
.clock-face time:nth-child(6) { --_d: 60deg; }
.clock-face time:nth-child(7) { --_d: 90deg; }
.clock-face time:nth-child(8) { --_d: 120deg; }
.clock-face time:nth-child(9) { --_d: 150deg; }
.clock-face time:nth-child(10) { --_d: 180deg; }
.clock-face time:nth-child(11) { --_d: 210deg; }
.clock-face time:nth-child(12) { --_d: 240deg; }

.arm {
  background-color: var(--_abg);
  border-radius: calc(var(--_aw) * 2);
  display: block;
  height: var(--_ah);
  left: calc((var(--_w) - var(--_aw)) / 2);
  position: absolute;
  top: calc((var(--_w) / 2) - var(--_ah));
  transform: rotate(0deg);
  transform-origin: bottom;
  width: var(--_aw);
}
.seconds {
  --_abg: rgb(255, 140, 5);
  --_ah: 40cqi;
  --_aw: 1cqi;
  animation: turn 60s linear infinite;
  animation-delay: var(--_ds, 0ms);
}

.minutes {
  --_abg: #333;
  --_ah: 35cqi;
  --_aw: 2.5cqi;
  animation: turn 3600s steps(60, end) infinite;
  animation-delay: var(--_dm, 0ms);
}

.hours {
  --_abg: #333;
  --_ah: 30cqi;
  --_aw: 2.5cqi;
  animation: turn 43200s linear infinite; /* 60 * 60 * 12 */
  animation-delay: var(--_dh, 0ms);
  position: relative;
}

.hours::before {
  background-color: #fff;
  border: 1cqi solid #333;
  border-radius: 50%;
  content: "";
  display: block;
  height: 4cqi;
  position: absolute;
  bottom: -3cqi;
  left: -1.75cqi;
  width: 4cqi;
}

html {
  display: grid;
  height: 100%;
}
body {
  background-image: linear-gradient(175deg, rgb(128, 202, 190), rgb(85, 170, 160), rgb(60, 139, 139));
  padding-block-start: 2em;
}
p {
  display: none;
  font-family: ui-sans-serif, system-ui, sans-serif;
  text-align: center;
}

@keyframes turn {
  to {
    transform: rotate(1turn);
  }
}

@supports not (left: calc(1px * cos(45deg))) {
  time {
    left: 50% !important;
    top: 50% !important;
    transform: translate(-50%,-50%) rotate(var(--_d)) translate(var(--_r)) rotate(calc(-1*var(--_d)));
  }
  p { display: block; }
}

</style>
  
</head>
<body>
  
<p><small>CSS sin() and cos() does <strong>NOT</strong> work in your browser.</small></p>
<div class="clock">
  <div class="clock-face" id="app">
    <time datetime="12:00">12</time>
    <time datetime="1:00">1</time>
    <time datetime="2:00">2</time>
    <time datetime="3:00">3</time>
    <time datetime="4:00">4</time>
    <time datetime="5:00">5</time>
    <time datetime="6:00">6</time>
    <time datetime="7:00">7</time>
    <time datetime="8:00">8</time>
    <time datetime="9:00">9</time>
    <time datetime="10:00">10</time>
    <time datetime="11:00">11</time>
    <span class="arm seconds"></span>
    <span class="arm minutes"></span>
    <span class="arm hours"></span>
  </div>
</div>


<script src="index.js" >  

/* to set current time */
const time = new Date();
const hour = -3600 * (time.getHours() % 12);
const mins = -60 * time.getMinutes();
app.style.setProperty('--_dm', `${mins}s`);
app.style.setProperty('--_dh', `${(hour+mins)}s`);

</script>
</body>
</html>


















