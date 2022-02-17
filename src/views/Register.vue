<template>
    <div>
        <div class="form-register">
            <h3>Create Your Account</h3>
            <form action="">
                <label for="fname">First Name</label><br>
                <input type="text" v-model="firstname" class="form-group" id="fname" name="fname" placeholder="Joko" required><br>
                
                <label for="lname">Last Name</label><br>
                <input type="text" v-model="lastname" class="form-group" id="lname" name="lname" placeholder="Shidqi" required><br>
                
                <label for="email">Email Address</label><br>
                <input type="email" v-model="email" class="form-group" id="email" name="email" placeholder="email@example.org" required><br>
                
                <label for="pass">Password</label><br>
                <input type="password" v-model="password" class="form-group" id="pass" name="pass" placeholder="********" minlength="8" required><br>
                
                <input type="checkbox" id="checkbox" name="checkbox" required>
                <label for="checkbox" class="checkbox">To register with us please tick to agree to our
                    <span style="color:#478ccc ">Terms and Conditions</span>
                </label><br>
                
                <button type="submit button" class="button" v-on:click="register">
                    Register
                </button>
            </form>
        </div>
        <div class="alternative">
            <div style="margin-bottom: 10px;">
                <a>
                    Already have an account? 
                    <span>
                        <router-link class="link" to="/" style="color: white; text-decoration: none;">Sign In</router-link>
                    </span>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
    // import axios from "axios"
    export default {
        name: 'Register',
        data() {
            return {
                firstname: '',
                lastname: '',
                email: '',
                password: ''
            }
        },
        methods: {
            register() 
            {
                if(this.$data != null){
                    console.log(
                        "First Name: "+this.firstname+"\n",
                        "Last Name: "+this.lastname+"\n",
                        "Email Address: "+this.email+"\n",
                        "Password: "+this.password
                    )
                }else{
                    alert("Registrasi berhasil!")
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
            //         console.warn("Registrasi berhasil")
            //         alert("Registrasi berhasil");
            //     }else{
            //         console.warn("Registrasi tidak berhasil")
            //         alert("Registrasi tidak berhasil")
            //     }
            // }
        }
    }
</script>

<style>

</style>