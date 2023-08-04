<script setup>

    import{ ref, onMounted, reactive} from 'vue'
    const todos = reactive([])
    let input = ref("")
    const months = ref(['Janurary','Feburary', 'March','April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'])
    const days = ref([])
    const year = ref([])
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
            
            <!-- Add in date method here -->

            <div class="
                flex
                justify-evenly
                space-x-2
            ">
                <div>
                    <textarea id="message" rows="2"
                        v-model="input"
                        type="text" 
                        class=" 
                            block 
                            p-2
                            w-full 
                            text-sm 
                            text-black
                            bg-gray-50 
                            rounded-lg border 
                            border-gray-300 
                            focus:ring-blue-500 
                            focus:border-blue-500" 
                        placeholder="Enter Todo"
                    />
                    <!-- Add in date selector here -->
                    <h4>To be completed by:</h4>
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
                <div class="mx-6">
                    <h4 class="font-bold underline">Current Tasks:</h4>
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
