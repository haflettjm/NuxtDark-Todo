<script setup>

    import{ ref, onMounted, reactive} from 'vue'
    const todos = reactive([])
    let input = ref("")
    const addTodo = (input) =>{
        todos.push(input)
    }

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
            p-4
            w-10/12
            h-10/12
            text-center
            rounded-md
        ">
            <h1 class="my-2 text-xl font-bold">
                Todo App
            </h1>
            <div class="
                flex
                justify-center
                space-x-2
            ">
                <div class="flex-col">
                    <div>
                        <input 
                            class="
                                text-black
                                rounded
                                p-4
                                " 
                            v-model="input"
                            type="text" 
                            placeholder="Enter Todo Here...">
                    </div>
                    <div>
                        <button 
                        v-on:click="addTodo(input)"
                        class="
                            bg-green-300
                            text-slate-700
                            p-4
                            font-bold
                            rounded-md
                            my-8
                        ">
                            submit
                        </button>
                    </div>
                </div>
                <div>
                    <ul>
                        <li v-for="item in todos">
                            {{ item }}
                        </li>
                    </ul>
                </div>  
            </div>
        </div>
    </div>

</template>
