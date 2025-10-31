<script>
    export default { 
        data(){
            return{
                message: 'Choose your favourite fruit:',
                fruit1 : 'apple',
                fruit2 : 'orange',
                fruit3 : 'peach',
            }
        }
    }
</script>

<template>
    <div id="app">
        {{ message }} </br>
        {{ fruit1 }} <input type="radio" name="fruit">
        {{ fruit2 }} <input type="radio" name="fruit">
        {{ fruit3 }} <input type="radio" name="fruit">
        <h3>Using Array</h3>
        
    </div>
</template>

<style scoped>
</style>