<script>
import { ref } from 'vue'

export default {
    data() {
        return {
            hideElement: false,
        };
    },
    mounted() {
    setTimeout(() => {
      this.hideElement = true;  // Attiva la classe 'none' dopo 4 secondi
    }, 4000);
  }
};
</script>



<template>
    <nav class="nav">
        <img class="bannerImg" src="https://i0.wp.com/www.parrocchiarescaldina.it/wp-content/uploads/2019/01/cropped-Moraine-Lake-4K-Ultra-HD-Wallpaper-4878x3225.jpg?ssl=1" alt="">
        <div :class="{ textBlurOut: hideElement }" class="containerInnerBanner">
            <div class="innerContainerBanner">
                <h1>La mia prima app con Vite!</h1>
            </div>
        </div>
    </nav>
</template>



<style>
.textBlurOut {
	-webkit-animation: textBlurOut 1.2s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
	        animation: textBlurOut 1.2s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
}
 @-webkit-keyframes textBlurOut {
  0% {
    -webkit-filter: blur(0.01);
            filter: blur(0.01);
  }
  100% {
    -webkit-filter: blur(12px) opacity(0%);
            filter: blur(12px) opacity(0%);
  }
}
@keyframes textBlurOut {
  0% {
    -webkit-filter: blur(0.01);
            filter: blur(0.01);
  }
  100% {
    -webkit-filter: blur(12px) opacity(0%);
            filter: blur(12px) opacity(0%);
  }
}
.nav {
    position: relative;
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 100vh;
    background-color: #ffffff;
}
.containerInnerBanner {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 80%;
    height: 90vh;
    background-color: #ffffffa4;
    border-radius: 2rem;
}
.innerContainerBanner {
    position: relative;
    top: 50%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    color: #655fe371;
    font-size: 3rem;

}
.innerContainerBanner {
	-webkit-animation: innerContainerBanner 2.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: innerContainerBanner 2.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
}
 @-webkit-keyframes innerContainerBanner {
  0% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-transform-origin: 50% 50%;
            transform-origin: 50% 50%;
    text-shadow: none;
  }
  100% {
    -webkit-transform: translateY(-50px);
            transform: translateY(-50px);
    -webkit-transform-origin: 50% 50%;
            transform-origin: 50% 50%;
    text-shadow: 0 1px 0 #433d3d, 0 2px 0 #433d3d, 0 3px 0 #433d3d, 0 4px 0 #433d3d, 0 5px 0 #433d3d, 0 6px 0 #433d3d, 0 7px 0 #433d3d, 0 8px 0 #433d3d, 0 9px 0 #433d3d, 0 50px 30px rgba(0, 0, 0, 0.3);
  }
}
@keyframes innerContainerBanner {
  0% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-transform-origin: 50% 50%;
            transform-origin: 50% 50%;
    text-shadow: none;
  }
  100% {
    -webkit-transform: translateY(-50px);
            transform: translateY(-50px);
    -webkit-transform-origin: 50% 50%;
            transform-origin: 50% 50%;
    text-shadow: 0 1px 0 #a4a0e612, 0 2px 0 #a4a0e612, 0 3px 0 #a4a0e612, 0 4px 0 #a4a0e612, 0 5px 0 #a4a0e612, 0 6px 0 #a4a0e612, 0 7px 0 #a4a0e612, 0 8px 0 #a4a0e612, 0 9px 0 #a4a0e612, 0 50px 15px rgba(0, 0, 0, 0.3);
  }
}




.bannerImg {
    filter: grayscale(37%) sepia(17%) blur(1px) hue-rotate(44deg) saturate(180%) contrast(133%) invert(24%);
-webkit-filter: grayscale(37%) sepia(17%) blur(1px) hue-rotate(44deg) saturate(180%) contrast(133%) invert(24%);
-moz-filter: grayscale(37%) sepia(17%) blur(1px) hue-rotate(44deg) saturate(180%) contrast(133%) invert(24%);
	-webkit-animation: bannerImg 20s ease-out infinite alternate-reverse both;
	        animation: bannerImg 20s ease-out infinite alternate-reverse both;
}
 @-webkit-keyframes bannerImg {
  0% {
    -webkit-transform: scale(1) translateY(0);
            transform: scale(1) translateY(0);
    -webkit-transform-origin: 50% 84%;
            transform-origin: 50% 84%;
  }
  100% {
    -webkit-transform: scale(1.25) translateY(15px);
            transform: scale(1.25) translateY(15px);
    -webkit-transform-origin: bottom;
            transform-origin: bottom;
  }
}
@keyframes bannerImg {
  0% {
    -webkit-transform: scale(1) translateY(0);
            transform: scale(1) translateY(0);
    -webkit-transform-origin: 50% 84%;
            transform-origin: 50% 84%;
  }
  100% {
    -webkit-transform: scale(1.25) translateY(15px);
            transform: scale(1.25) translateY(15px);
    -webkit-transform-origin: bottom;
            transform-origin: bottom;
  }
}

</style>