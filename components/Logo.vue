<template>
  <div class="px-3">
    <div class="glitch" data-text="charlie">charlie levine</div>
  </div>
</template>

<style lang="scss">
.glitch {
  color: white;
  font-size: 10vw;
  position: relative;
  margin: 0 auto;
}
@keyframes noise-anim {
  $steps: 12;
  @for $i from 0 through $steps {
    #{percentage($i*(1/$steps))} {
      $top: random(100);
      $bottom: random(101 - $top);
      $topWithPercent: $top * 1%;
      $bottomWithPercent: $bottom * 1%;
      clip-path: inset(#{$topWithPercent} 0 #{$bottomWithPercent} 0);
    }
  }
}
.glitch::after {
  content: attr(data-text);
  position: absolute;
  left: 2px;
  text-shadow: -1px 0 red;
  top: 0;
  color: white;
  background: black;
  overflow: hidden;
  animation: noise-anim 2s infinite linear alternate-reverse;
}

@keyframes noise-anim-2 {
  $steps: 12;
  @for $i from 0 through $steps {
    #{percentage($i*(1/$steps))} {
      $top: random(100);
      $bottom: random(101 - $top);
      $topWithPercent: $top * 1%;
      $bottomWithPercent: $bottom * 1%;
      clip-path: inset(#{$topWithPercent} 0 #{$bottomWithPercent} 0);
    }
  }
}
.glitch::before {
  content: attr(data-text);
  position: absolute;
  left: -2px;
  text-shadow: 1px 0 blue;
  top: 0;
  color: white;
  background: black;
  overflow: hidden;
  animation: noise-anim-2 15s infinite linear alternate-reverse;
}
</style>
