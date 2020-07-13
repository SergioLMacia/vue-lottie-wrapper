<template>
  <div class="lottie-wrapper">
    <lottie-player 
        ref="lottieRef" 
        :id="id" 
        :src="src" 
        :autoplay="autoplay"
        :background="background"
        :controls="controls"
        :count="count"
        :direction="direction"
        :hover="hover"
        :loop="loop"
        :mode="mode"
        :renderer="renderer"
        :speed="speed"
    >
    </lottie-player>
  </div>
</template>
<style scoped>
.lottie-wrapper {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
}
</style>	
<script>
import "@lottiefiles/lottie-player";
import { create } from "@lottiefiles/lottie-interactivity";
export default {
  name: "Lottie",
  props: {
    id: { type: String, required: true,  default: "lottieRef"},
    expandedOptions: { type: Object, required: false},
    src: {type: String, required: true},
    autoplay:{type:Boolean, default: false},
    background:{type:String, default: undefined},
    controls:{type:Boolean, default: false},
    count:{type:Number, default: undefined},
    direction:{type:Number, default: 1},
    hover:{type:Boolean, default: false},
    loop:{type:Boolean, default: false},
    mode:{type:String, default: 'PlayMode.Normal' },
    renderer:{type:String, default: 'svg'},
    speed:{type:Number, default: 1},
  },
  data() {
    return {
      myRef: null
    };
  },
  mounted() {
    let component = this;
    this.myRef = this.$refs.lottieRef;
    this.myRef.addEventListener("load", function(e) {
      create({
        player: "#" + component.id,
        ...component.expandedOptions
      });
    });
  }
};
</script>