<template>
    <section>
        <header><h1>Assignment 2</h1></header>
        <div>
            <active-user
            :key="user.id" 
            :name="user.name" 
            :age="user.age"
            ></active-user>
            <user-data
            @add-user="addUser"
            ></user-data>
        </div>
    </section>
</template>

<script>
import ActiveUser from './components/ActiveUser.vue'
import UserData from './components/UserData.vue'
    export default {
        components: {ActiveUser, UserData},
        data(){
            return {
                user:
                    {
                        id: 'test',
                        name: 'test',
                        age: '23'
                    }
            }
        },
        methods: {
            addUser(name, age){
                this.user.name = name;
                this.user.age = age;
            }
        }
    }
</script>

<style scoped>

</style>
