---
layout: slide
title: "Monkey Dancing on a Pole"
---

<style>
.monkey-stage {
  position: relative;
  width: 360px;
  height: 320px;
  margin: 1.5rem auto;
  border-radius: 24px;
  background: linear-gradient(180deg, #1d1b3a 0%, #3f2c70 45%, #f4a261 45%, #f4a261 65%, #264653 100%);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.35);
  overflow: hidden;
}

.monkey-stage::after {
  content: "";
  position: absolute;
  bottom: 45px;
  left: -40px;
  width: 440px;
  height: 220px;
  background: radial-gradient(circle at 50% 0%, rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0));
  opacity: 0.7;
  pointer-events: none;
  animation: spotlight 5s ease-in-out infinite;
}

.pole {
  position: absolute;
  bottom: 40px;
  left: 50%;
  transform: translateX(-50%);
  width: 18px;
  height: 240px;
  background: linear-gradient(180deg, #dfe5ef 0%, #f9f9f9 30%, #bfc6d1 60%, #f0f3f8 100%);
  border-radius: 12px;
  box-shadow: inset 0 0 12px rgba(0, 0, 0, 0.2);
}

.stage-floor {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 60px;
  background: radial-gradient(circle at 50% 0%, rgba(255, 255, 255, 0.4), rgba(244, 162, 97, 0));
}

.monkey {
  position: absolute;
  top: 75px;
  left: 50%;
  width: 150px;
  height: 180px;
  transform-origin: 25px 90px;
  animation: monkey-dance 4s ease-in-out infinite;
}

.monkey .head {
  position: absolute;
  top: 0;
  left: 55px;
  width: 90px;
  height: 90px;
  background: #8d5524;
  border-radius: 70% 70% 60% 60%;
  box-shadow: inset 0 -8px 0 rgba(0, 0, 0, 0.12);
}

.monkey .face {
  position: absolute;
  bottom: 10px;
  left: 12px;
  width: 66px;
  height: 55px;
  background: #f1c27d;
  border-radius: 50px 50px 45px 45px;
}

.monkey .ear {
  position: absolute;
  top: 18px;
  width: 34px;
  height: 34px;
  background: #8d5524;
  border-radius: 50%;
}

.monkey .ear::after {
  content: "";
  position: absolute;
  top: 6px;
  left: 6px;
  width: 22px;
  height: 22px;
  background: #f1c27d;
  border-radius: 50%;
}

.monkey .ear.left {
  left: -12px;
}

.monkey .ear.right {
  right: -12px;
}

.monkey .eye {
  position: absolute;
  top: 32px;
  width: 12px;
  height: 16px;
  background: #2d2d2d;
  border-radius: 50%;
}

.monkey .eye.left {
  left: 24px;
}

.monkey .eye.right {
  right: 24px;
}

.monkey .mouth {
  position: absolute;
  bottom: 16px;
  left: 50%;
  width: 26px;
  height: 12px;
  background: transparent;
  border-bottom: 4px solid #c66b3d;
  border-radius: 0 0 50% 50%;
  transform: translateX(-50%);
}

.monkey .body {
  position: absolute;
  top: 80px;
  left: 48px;
  width: 72px;
  height: 80px;
  background: #7a431d;
  border-radius: 50px 50px 46px 46px;
  box-shadow: inset 0 -6px 0 rgba(0, 0, 0, 0.15);
}

.monkey .belly {
  position: absolute;
  top: 18px;
  left: 12px;
  width: 48px;
  height: 50px;
  background: #f3c78f;
  border-radius: 45px 45px 40px 40px;
}

.monkey .arm {
  position: absolute;
  top: 95px;
  width: 18px;
  height: 80px;
  background: #7a431d;
  border-radius: 18px;
  transform-origin: top center;
}

.monkey .arm.left {
  left: 22px;
  transform: rotate(60deg);
  animation: arm-left 4s ease-in-out infinite;
}

.monkey .arm.right {
  right: 12px;
  transform: rotate(-110deg);
  animation: arm-right 4s ease-in-out infinite;
}

.monkey .leg {
  position: absolute;
  bottom: 0;
  width: 18px;
  height: 76px;
  background: #7a431d;
  border-radius: 20px;
  transform-origin: top center;
}

.monkey .leg.left {
  left: 40px;
  transform: rotate(22deg);
  animation: leg-left 4s ease-in-out infinite;
}

.monkey .leg.right {
  right: 42px;
  transform: rotate(-60deg);
  animation: leg-right 4s ease-in-out infinite;
}

.monkey .tail {
  position: absolute;
  bottom: 12px;
  right: -34px;
  width: 18px;
  height: 110px;
  border: 8px solid #7a431d;
  border-color: #7a431d transparent transparent transparent;
  border-radius: 50% 50% 0 0;
  transform-origin: top left;
  transform: rotate(30deg);
  animation: tail-swish 2.5s ease-in-out infinite;
}

@keyframes monkey-dance {
  0% {
    transform: translateX(-50%) rotate(-22deg);
  }
  50% {
    transform: translateX(-50%) rotate(24deg);
  }
  100% {
    transform: translateX(-50%) rotate(-22deg);
  }
}

@keyframes arm-left {
  0%, 100% {
    transform: rotate(60deg);
  }
  50% {
    transform: rotate(25deg);
  }
}

@keyframes arm-right {
  0%, 100% {
    transform: rotate(-110deg);
  }
  50% {
    transform: rotate(-60deg);
  }
}

@keyframes leg-left {
  0%, 100% {
    transform: rotate(22deg);
  }
  50% {
    transform: rotate(-30deg);
  }
}

@keyframes leg-right {
  0%, 100% {
    transform: rotate(-60deg);
  }
  50% {
    transform: rotate(-10deg);
  }
}

@keyframes tail-swish {
  0%, 100% {
    transform: rotate(30deg);
  }
  50% {
    transform: rotate(-10deg);
  }
}

@keyframes spotlight {
  0%, 100% {
    opacity: 0.4;
    transform: translateY(0);
  }
  50% {
    opacity: 0.8;
    transform: translateY(-10px);
  }
}
</style>

<div class="monkey-stage">
  <div class="pole"></div>
  <div class="monkey">
    <div class="head">
      <div class="ear left"></div>
      <div class="ear right"></div>
      <div class="face"></div>
      <div class="eye left"></div>
      <div class="eye right"></div>
      <div class="mouth"></div>
    </div>
    <div class="body">
      <div class="belly"></div>
    </div>
    <div class="arm left"></div>
    <div class="arm right"></div>
    <div class="leg left"></div>
    <div class="leg right"></div>
    <div class="tail"></div>
  </div>
  <div class="stage-floor"></div>
</div>

The energetic dancer loops around the pole, bringing the slide to life!
