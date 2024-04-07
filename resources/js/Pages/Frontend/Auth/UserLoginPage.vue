<script setup>
import GuestLayout from '../../../Layouts/GuestLayout.vue';

import { Link, Head, usePage, useForm } from '@inertiajs/vue3';
const list = usePage();

const form = useForm({
    email: '',
    password: '',
});

// Admin login function
function UserLogin() {
    form.post(route('user.login'), {
        onSuccess: () => {
            if (list.props.flash.status === true) {
                successToast(list.props.flash.message);
                form.reset();
            } else {
                errorToast(list.props.flash.message);
            }
        },
        onError: (errors) => {
            if (errors.email) {
                errorToast(errors.email);
            } else if (errors.password) {
                errorToast(errors.password);
            } else {
                errorToast(list.props.flash.message);
            }
        }
    });
}
</script>

<template>

    <Head>
        <title>Login</title>
    </Head>
    <GuestLayout>
       
        <!-- inner-apge-banner end -->

        <!-- login-section start -->
        <section class="login-section pt-120 pb-120" >
            <div class="container ">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="login-block text-center ">
                            <div class="login-block-inner">
                                <h3 class="title">login your account </h3>
                                <form class="login-form" @submit.prevent="UserLogin()">
                                    <div class="frm-group">
                                        <input type="email" placeholder="Enter your email" v-model="form.email">
                                    </div>
                                    <div class="frm-group">
                                        <input type="password" placeholder="Your Password" v-model="form.password">
                                    </div>
                                    <div class="frm-group">
                                       <button type="submit" class="cmn-btn w-100">Submit</button>
                                    </div>
                                    <div class="frm-group text-center">
                                        <span class="or">or</span>
                                    </div>
                                    <div class="frm-group text-center">
                                        <a href="" class="google"> Login with google</a>
                                    </div>
                                </form>
                                <div >
                                <p >
                                    <Link :href="route('show.user.registration')">Haven't your any account in here?</Link> <br>
                                    <a style="" href="#0">Forget password?</a>
                                </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- login-section end -->
    </GuestLayout>
</template>

<style scoped></style>
