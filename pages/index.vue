<script setup>
import{ ref, onMounted} from 'vue'
const todos = ref(["todo1", "todo2", "todo3"])
</script>
<template>
    <div class="
            flex
            container
            mx-auto  
            justify-center
            content-center 
            w-full
            h-full
        ">
        <div class="
            my-8
            justify-center
            bg-slate-700
            p-8
            w-10/12
            h-10/12
            text-center
            rounded-md
        ">
            <h1 class="my-2">
                Todo App
            </h1>
            <div class="
                flex
                justify-center
                space-x-2
            ">
                <div>
                    <input v-model="text" placeholder="Enter Todo Here...">
                </div>
                <div>
                    <ul>
                        <li v-for="item in todos">
                            {{item}}
                        </li>
                    </ul>
                </div>

            </div>
            <button class="
                    bg-yellow-300
                    p-4
                    rounded-md
                    my-8
                ">
                    click me!
            </button>
        </div>
    </div>

</template>
