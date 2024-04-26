<template>
    <div class="container">
        <BoxContent />
        <BoxContent />
        <BoxContent />
        <BoxContent />
    </div>
</template>

<script>
import BoxContent from './BoxContent.vue'

    export default{
        components:{BoxContent}
    }
</script>

<style scoped>
.container{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly
}
</style>