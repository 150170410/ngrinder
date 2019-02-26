<template>
    <div id="login-container">
        <vue-headful title="Login"/>
        <div class="logo">
            <img src="/img/logo_ngrinder_a.png" width="400" alt="nGrinder logo">
        </div>
        <div class="content">
            <form action="/form_login" method="POST">
                <fieldset>
                    <div class="login">
                        <div class="lgn_ipt">
                            <input v-focus type="text" class="span2 input" name="j_username" id="j_username" placeholder="User ID"><br>
                            <input type="password" class="span2 input" name="j_password" id="j_password" placeholder="Password">
                        </div>
                        <input id="loginBtn" type="image" src="/img/login.gif" alt="Login" class="btn_lgn">
                    </div>

                    <div class="prompt">
                        <input id="remember_me" type="checkbox" class="checkbox" name='_spring_security_remember_me'>
                        <span>Remember Me</span>
                        <select id="native_language" name="native_language">
                            <option value="en">English</option>
                            <option value="kr">한국어</option>
                            <option value="cn">中文</option>
                        </select>
                    </div>

                    <div class="prompt">
                        <select id="user_timezone" name="user_timezone"></select>
                    </div>
                    <div class="prompt">
                        <a id="sign_up" class="pointer-cursor">Sign Up</a>
                    </div>
                </fieldset>
            </form>
            <copyright :nGrinderVersion="nGrinderVersion"></copyright>
        </div>
    </div>
</template>

<script>
    import Component from 'vue-class-component';
    import Base from 'Base.vue';
    import Copyright from 'Copyright.vue';
    import vueHeadful from 'vue-headful';

    @Component({
        name: 'login',
        components: { Copyright, vueHeadful },
    })
    export default class Login extends Base {

    }
</script>

<style lang="less" scoped>
    body {
        overflow-y: hidden;
        background-color: white
    }

    #login-container {
        .logo {
            margin-top: 150px;
            text-align: center;
        }

        .content {
            height: 635px;
            margin-top: 30px;
            padding-top: 30px;
            background-color: #f5f4f2;

            fieldset {
                border: 0;

                .lgn_ipt {
                    display: inline-block;
                    input {
                        height: 30px;
                        margin-bottom: 5px;
                    }
                }

                .login {
                    text-align: center;
                    input {
                        border: 1px solid #e0e0e0;
                    }
                }

                .btn_lgn {
                    display: inline-block;
                    margin-left: 20px;
                    vertical-align: top;
                    margin-top: 0;
                }

                .prompt {
                    text-align: center;
                    margin-top: 5px;
                    height: 30px;

                    #remember_me {
                        margin-top: -4px;
                    }

                    #native_language {
                        margin-left: 60px;
                        width: 80px;
                    }

                    #user_timezone {
                        width: 240px;
                    }

                    #sign_up {
                        margin-left: 200px;
                    }

                    select {
                        width: 75px;
                    }
                }
            }
        }
    }

    .select2-result-label {
        text-overflow: ellipsis;
        display:block;
        white-space:nowrap;
        overflow:hidden;
    }
</style>
