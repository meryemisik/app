<template>
    <div id="login">
        <h1>Login</h1>
        <input type="text" name="username" v-model="input.username" placeholder="Username"  />  <br/>
        <input type="password" name="password" v-model="input.password" placeholder="Password" />  <br>
        <button type="button" class="btn btn-primary" @click="login()">Login</button>
    </div>
</template>

<script>
    export default {
        name: 'Login',
        data() {
            return {
                input: {
                    username: "",
                    password: ""
                }
            }
        },
        methods: {
            login() {
                if(this.input.username != "" && this.input.password != "") {
                  if(this.input.username == 'meryem' && this.input.password=='123'){
                    alert("Giriş başarılı");
                  }
                  else if(this.input.username!='meryem' && this.input.password =='123'){
                    alert("kullanıcı adı hatalı")
                  }
                  else if(this.input.username=='meryem' && this.input.password!='123' ){
                    alert("şifre hatalı")
                  }
                  else {
                    alert("Böyle bir kullanıcı yok");
                } 
                } 
            }
        }
    }
</script>

<style scoped>
    #login {
        width: 500px;
        border: 1px solid #CCCCCC;
        background-color: #FFFFFF;
        margin: auto;
        margin-top: 200px;
        padding: 20px;
    }
    button{
     margin-top: 1rem;
     width: 90%;
    }
    input{
      margin-top: 1rem;
      width: 90%;
      border:1px solid gainsboro;
      padding: 3px;
      border-radius: 5px;
    }
    h1{
      text-align: center;
    }
</style>