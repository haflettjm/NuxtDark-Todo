<script setup>
    import{ ref,onMounted} from 'vue'

    const 
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
            flexbox
            bg-slate-700
            p-8
            w-10/12
            h-10/12
            text-center
            rounded-md
        ">
            <h1>
                Todo App
            </h1>
            <div class="
                flex
                justify-center
                space-x-2
            ">
                <div>
                    <form>
                        Input Text...
                    </form>
                </div>
                <div>
                    <ul>
                        <li>
                            Todo 1
                        </li>
                    </ul>
                </div>
                <button>
                    click me!
                </button>
            </div>
        </div>
    </div>

</template>
