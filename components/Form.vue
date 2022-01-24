<template>
  <form  action="" >
    <label for="name">Name</label>
    <Input type='text' placeholder="Enter your name" id="name"/>
    <label for="email">Email</label>
    <Input type='text' name="Email" value="email" id="email"/>
    <label for="date">Birth Date</label>
    <Input type='date' name="birthDate" id="birthDate"/>
    <p style="{margin-bottom: 1%}">
        <label for="gender">Gender</label>
        <select
        id="gender"
        v-model="gender"
        name="gender"
        >
            <option>male</option>
            <option>female</option>
        </select>
    </p>
    <Button text="Submit" color="green" />
  </form >
</template>

<script>
    import Button from "./Button.vue";
    import Input from "./Input.vue";
    import { email, required } from '@vuelidate/validators'
    import { useVuelidate } from '@vuelidate/core'
    export default {
        name: 'Form',
        data: () => ({
            name: '',
            email: '',
            birthDate: '',
            gender: ''
        }),
        setup: () => ({ v$: useVuelidate() }),
        validations () {
            return {
            form: {
                name: { required },
                email: { required, email },
                birthDate:{required}
            }
            }
        },
        components: {
            Input,
            Button,
        },
        methods: {
            submit: function() {
                console.log(this.name, this.email, this.birthDate, this.gender);

                this.name = '';
                this.email = '';
            }
        }
    }
</script>

<style scoped>
    form {
        margin-left: 6%;
    }
    select {
        height: 30px;
        margin-bottom: 1%;
    }
</style>