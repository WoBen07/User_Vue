<template>
    <div>
        <form action="" @submit.prevent="submitData">
            <label>Name</label>
            <input type="text" v-model="enteredName">
            <label>Age</label>
            <input type="text" v-model="enteredAge">
            <button>Change User</button>
        </form>
        
    </div>
    
</template>
<script>
 export default {
    emits: ['add-user'],
    data(){
        return {
            enteredName: '',
            enteredAge: ''
        }
    },
    methods: {
        submitData(){
            this.$emit('add-user', this.enteredName, this.enteredAge)
        }
    }
 }
</script>
<style scoped>
div {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: aliceblue;
    border: 2px solid black;
}
form {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
button {
    margin-top: 10px;
}
</style>
