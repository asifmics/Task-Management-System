<script setup>
import { RouterLink } from 'vue-router'

</script>

<template>
    <div class="h-screen flex justify-center">
        <div class="w-4/12 bg-white rounded-lg drop-shadow-md border-gray-200 border self-center p-4">
            <h2 class="text-center text-lg pb-3 capitalize">User Registration Form  </h2>
            <div>
                <form>
                    <div class="flex flex-col">
                        <label class="text-[17px] pb-1">Name:</label>
                        <input placeholder="Enter user name here" class="text-[#939DA7] text-[16px] font-light border border-gray-200 p-2 bg-[#E0E4E8] rounded-md"/>
                    </div>
                    <div class="flex flex-col mt-2">
                        <label class="text-[17px] pb-1">Email:</label>
                        <input placeholder="Enter user email here" class="text-[#939DA7] text-[16px] font-light border border-gray-200 p-2 bg-[#E0E4E8] rounded-md"/>
                    </div>
                    <div class="flex flex-col mt-2">
                        <label class="text-[17px] pb-1">Password:</label>
                        <input placeholder="Enter user password here" class="text-[#939DA7] text-[16px] font-light border border-gray-200 p-2 bg-[#E0E4E8] rounded-md"/>
                    </div>
                    <div class="flex flex-col mt-2">
                        <label class="text-[17px] pb-1">Confirm password:</label>
                        <input placeholder="Enter confirm password here" class="text-[#939DA7] text-[16px] font-light border border-gray-200 p-2 bg-[#E0E4E8] rounded-md"/>
                    </div>
                    <div class="flex flex-col mt-2">
                        <label class="text-[17px] pb-1">User image:</label>
                        <input type="file" class="text-[#939DA7] text-[16px] font-light border border-gray-200 p-2 bg-[#E0E4E8] rounded-md"/>
                    </div>
                    <div class="flex flex-row justify-center gap-6">
                        <RouterLink to="/login" class="grow px-3 py-1 rounded-lg hover:text-sky-500 text-[#6B7280] font-normal text-[16px] mt-3 underline">I already a user </RouterLink>
                        <button class="px-3 py-1 rounded-lg bg-[#BE1E2D] text-white font-normal text-[16px] mt-3">Register</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>