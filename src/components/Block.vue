<template>
  <div class="block" v-if="showBlock">
      Click me
  </div>
</template>

<script>
export default {
    props : ['delay'],
    data() {
        return {
            showBlock: false,
        }
    },
    // cycle hook
    mounted() {
   
        // display block after delay
        setTimeout(() => {
            this.showBlock = true
            console.log(this.delay)
        }, this.delay)
    },
}
</script>

<style>
    .block {
        width: 400px;
        border-radius: 20px;
        background: #0faf87;
        color: white;
        text-align: center;
        padding: 100px 0;
        margin: 40px auto;
    }
</style>