<template>
    <div class=" py-10 px-12 max-w-xl mx-auto bg-slate-800 rounded-xl shadow-xl space-y-2 sm:flex sm:items-center sm:space-y-0 sm:space-x-6">
        <ol class="relative border-l border-gray-700">
            <li v-for="item in timelineItems" class="mb-10 ml-8">
                <span class="flex absolute -left-3 justify-center items-center w-6 h-6 rounded-full ring-8 ring-gray-900 bg-blue-900">
                    <svg aria-hidden="true" class="w-3 h-3 text-blue-600" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"></path></svg>
                </span>
                <h3 class="mb-1 text-lg font-semibold text-white">{{ item.name }}</h3>
                <time class="block mb-2 text-sm font-normal leading-none text-gray-300">{{ item.date }}</time>
                <p class="mb-4 text-base font-normal text-gray-400">{{ item.desc }}</p>  
            </li>
        </ol>
    </div>
</template>

<script>
    import axios from 'axios'
    const url = "https://yfjnf65svbuabqu32stbjn2la40uxryo.lambda-url.ap-northeast-1.on.aws/"
    export default {
        data () {
            return {
                timelineItems: []
            }
        },
        created () {
            axios.get(url).then((res) => {
                this.timelineItems = res.data
            })
        }
    }
</script>