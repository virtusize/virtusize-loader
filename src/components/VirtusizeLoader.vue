<template>
  <transition name="fade">
    <div class="vs-loader" v-if="visible">
      <div class="squeezer">
        <div class="vbottom"></div>
        <div class="vtop"></div>
      </div>
      <p class="loader-label" v-if="label">{{label}}</p>
    </div>
  </transition>
</template>

<script>
export default {
  props: {
    label: {
      type: String
    },
    visible: {
      type: Boolean,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.vs-loader {
  display: flex;
  align-items: center;
  justify-content: center;
  animation: none;
  background: #fafafa;
  border: 0;
  border-radius: 0;
  height: 100%;
  left: 0;
  padding: 30px;
  position: absolute;
  text-align: center;
  top: 0;
  width: 100%;
  z-index: auto;

  .loader-label {
    font-size: 11px;
    font-weight: 600;
    color: #3a3a3a;
    margin: 0;
    line-height: 3px;
  }

  .panel {
    background: #fff;
  }

  .fade-leave-active,
  .fade-leave {
    transition: opacity 0.15s cubic-bezier(0.06, 0.59, 0.32, 0.99);
  }
  .fade-enter {
    opacity: 1;
  }
  .fade-leave-to {
    opacity: 0;
  }
  .squeezer {
    -webkit-transform: rotate3d(0, 1, 0, 45deg);
    -moz-transform: rotate3d(0, 1, 0, 45deg);
    -ms-transform: rotate3d(0, 1, 0, 45deg);
    -o-transform: rotate3d(0, 1, 0, 45deg);
    transform: rotate3d(0, 1, 0, 45deg);
    display: inline-block;
    width: 67px;
    height: 35px;
    position: relative;
    overflow: hidden;
  }

  .vtop {
    box-sizing: border-box;
    border: 6px solid #000;
    width: 28px;
    height: 28px;
    border-top-color: transparent;
    border-left-color: transparent;
    position: absolute;
    top: -14px;
    left: 19px;
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    transform: rotate(45deg);
    -webkit-animation: toppulse 0.7s infinite alternate linear;
    -moz-animation: toppulse 0.7s infinite alternate linear;
    -o-animation: toppulse 0.7s infinite alternate linear;
    animation: toppulse 0.7s infinite alternate linear;
  }

  .vbottom {
    border: 6px solid #16c6b9;
    width: 28px;
    height: 28px;
    border-top-color: transparent;
    border-left-color: transparent;
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    transform: rotate(45deg);
    position: absolute;
    box-sizing: content-box;
    top: -20px;
    left: 13px;
    -webkit-animation: bottompulse 0.7s infinite alternate linear;
    -moz-animation: bottompulse 0.7s infinite alternate linear;
    -o-animation: bottompulse 0.7s infinite alternate linear;
    animation: bottompulse 0.7s infinite alternate linear;
  }
}

@-webkit-keyframes toppulse {
  0% {
    border-width: 6px;
  }
  50% {
    border-width: 6px;
  }
  82% {
    border-width: 0;
  }
  100% {
    border-width: 0;
  }
}
@-moz-keyframes toppulse {
  0% {
    border-width: 6px;
  }
  50% {
    border-width: 6px;
  }
  82% {
    border-width: 0;
  }
  100% {
    border-width: 0;
  }
}
@-o-keyframes toppulse {
  0% {
    border-width: 6px;
  }
  50% {
    border-width: 6px;
  }
  82% {
    border-width: 0;
  }
  100% {
    border-width: 0;
  }
}
@keyframes toppulse {
  0% {
    border-width: 6px;
  }
  50% {
    border-width: 6px;
  }
  82% {
    border-width: 0;
  }
  100% {
    border-width: 0;
  }
}

@-webkit-keyframes bottompulse {
  0% {
    top: -28px;
  }
  10% {
    top: -28px;
  }
  33% {
    top: -20px;
  }
  100% {
    top: -20px;
  }
}
@-moz-keyframes bottompulse {
  0% {
    top: -28px;
  }
  10% {
    top: -28px;
  }
  33% {
    top: -20px;
  }
  100% {
    top: -20px;
  }
}
@-o-keyframes bottompulse {
  0% {
    top: -28px;
  }
  10% {
    top: -28px;
  }
  33% {
    top: -20px;
  }
  100% {
    top: -20px;
  }
}
@keyframes bottompulse {
  0% {
    top: -28px;
  }
  10% {
    top: -28px;
  }
  33% {
    top: -20px;
  }
  100% {
    top: -20px;
  }
}
</style>
