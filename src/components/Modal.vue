<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{sale: theme === 'sale'}">
            <slot></slot>
            <div class="actions">
                <slot name="accessLinks">
                    <a href="https://pt-support.vercel.app" target="_blank" rel="noreferrer noopener">Login</a>
                </slot>
                <br/>
                <slot name="infoLinks"></slot>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['theme'],
        methods:{
            closeModal(){
                this.$emit('close')
            }
        }
    }
</script>

<style>
.backdrop{
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}
.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: whitesmoke;
    border-radius: 10px;
}
.modal h1{
    color: #03cfb4;
    border: none;
    padding: 0;
}
.modal.sale {
    background: crimson;
    color: white;
}
.modal.sale h1{
    color: white;
}

</style>