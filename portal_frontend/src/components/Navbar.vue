<template>

<div class="bg-white text-gray-600 py-3.5 px-6 shadow md:flex justify-between items-center">
    <div class="flex items-center">
        <span class="text-gray-900 text-xl mr-1">
            <i class="bi bi-messenger"></i>
        </span>
        <h1 class="text-xl">We Portal</h1>
    </div>
    <span class="absolute md:hidden">
        <i></i>
    </span>

    <ul class="md:flex md:items-center md:px-0 px-3 md:pb-0 pb-10 md:static absolute bg-gray-900
    md:w-auto w-full top-14 duration-700 ease-in" :class="[open ? 'left-0' : 'left-[-100%]']">
        
        <li class="md:mx-4 md:my-0 my-6" v-for="link in Links">
            <a :href="link.link" class="text-xl hover:text-green-500">{{link.name}}</a>
        </li>

        <Button>Login</Button>
        
    </ul>
    
</div>

</template>

<script>
import Button from './Button.vue';


export default {
    components:{
        Button
    },

    setup(){
        let open = ref(false)
        let Links = [
            {name : "Home" , link : "#"},
            {name : "About" , link : "#"},
            {name : "Pricing" , link : "#"},
            {name : "Contact" , link : "#"},
        ]

        return {Links,open}
    }
}
</script>