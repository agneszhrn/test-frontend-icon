<template>
    <div>
        <div class="form-login">
            <h3>Login to your Account</h3>
            <form action="">
                <label for="email">Email Address</label><br>
                <input type="email" v-model="email" class="form-group" id="email" name="email" placeholder="email@example.org" required><br>
                
                <label for="pass">Password</label><br>
                <input type="password" v-model="password" class="form-group" id="pass" name="pass" placeholder="********" minlength="8" required><br>
                    
                <button type="submit button" class="button" v-on:click="login">
                    Login
                </button>
            </form>
        </div>
        <div class="alternative">
        <div style="margin-bottom: 10px;">
            <a>
                Don't have an account? 
                <span>
                    <router-link class="link" to="/register">Register</router-link>
                </span>
            </a>
        </div>
        <div>
            <a>
                Forgotten your password? 
                <span>
                    <router-link class="link" to="/register">Recover Password</router-link>
                </span>
            </a>
        </div>
    </div>
    </div>
</template>

<script>
    // import axios from "axios"
    export default {
        name: 'Login',
        data() {
            return {
                email: '',
                password: ''
            }
        },
        methods: {
            login() 
            {
                if(this.$data != null){
                    console.log(
                        "Email Address: "+this.email+"\n",
                        "Password: "+this.password
                    )
                }else{
                    alert("Login berhasil!")
                }
            }
            // async register() 
            // {
            //     let result = await axios.post("http://localhost:3000/user",{
            //         firstname: this.firstname,
            //         lastname: this.lastname,
            //         email: this.email,
            //         password: this.password
            //     });

            //     console.warn(result);
            //     if(result.status==201) {
            //         alert("Sign up done");
            //     }
            // }
        }
    }
</script>

<style>
    
</style>