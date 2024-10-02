<script setup>
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
import {faDashboard, faPlus, faShare} from "@fortawesome/free-solid-svg-icons";
import Modal from "./components/Modal.vue";
import {ref} from "vue";

const boardShow = ref(false);

const showBoardModal = () => {
    boardShow.value = true;
}

const closeBoardModal = () => {
    boardShow.value = false;
}
</script>

<template>
    <div class="bg-white py-2 mx-auto container">
        <div class="flex flex-row">
            <div class="w-3/12 self-center">
                <img src="./assets/Logo.png" class="w-2/3 object-cover" alt="logo-image">
            </div>
            <div class="w-6/12 self-center">
                <div>
                    <form action="#" class="relative">
                        <div class="absolute top-[25%] left-2">
                            <svg width="25" height="24" viewBox="0 0 25 24" fill="none"
                                 xmlns="http://www.w3.org/2000/svg">
                                <g clip-path="url(#clip0_13_1839)">
                                    <path d="M18.531 16.617L22.814 20.899L21.399 22.314L17.117 18.031C15.5237 19.3082 13.542 20.0029 11.5 20C6.532 20 2.5 15.968 2.5 11C2.5 6.032 6.532 2 11.5 2C16.468 2 20.5 6.032 20.5 11C20.5029 13.042 19.8082 15.0237 18.531 16.617ZM16.525 15.875C17.7941 14.5699 18.5029 12.8204 18.5 11C18.5 7.132 15.367 4 11.5 4C7.632 4 4.5 7.132 4.5 11C4.5 14.867 7.632 18 11.5 18C13.3204 18.0029 15.0699 17.2941 16.375 16.025L16.525 15.875Z"
                                          fill="#777B84"/>
                                </g>
                                <defs>
                                    <clipPath id="clip0_13_1839">
                                        <rect width="24" height="24" fill="white" transform="translate(0.5)"/>
                                    </clipPath>
                                </defs>
                            </svg>
                        </div>
                        <input class="border border-gray-300 rounded-[5px] py-2 pl-8 text-[16px] font-poppins font-light w-1/2"
                               placeholder="Search your task here..."/>
                    </form>
                </div>
            </div>
            <div class="w-3/12">
                <div class="flex flex-row justify-between">
                    <div class="relative self-center">
                        <svg width="30" height="33" viewBox="0 0 30 33" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M29.2898 23.8034C28.4443 22.347 27.1874 18.2261 27.1874 12.8438C27.1874 9.61142 25.9034 6.51149 23.6178 4.22589C21.3322 1.94029 18.2323 0.65625 14.9999 0.65625C11.7676 0.65625 8.66768 1.94029 6.38208 4.22589C4.09648 6.51149 2.81244 9.61142 2.81244 12.8438C2.81244 18.2276 1.55408 22.347 0.708576 23.8034C0.49266 24.1736 0.378195 24.5943 0.376723 25.0229C0.375252 25.4515 0.486827 25.8729 0.700195 26.2447C0.913564 26.6164 1.22118 26.9253 1.59203 27.1402C1.96287 27.3551 2.38383 27.4684 2.81244 27.4688H9.02959C9.31078 28.8447 10.0586 30.0812 11.1465 30.9693C12.2344 31.8573 13.5956 32.3424 14.9999 32.3424C16.4043 32.3424 17.7655 31.8573 18.8534 30.9693C19.9413 30.0812 20.6891 28.8447 20.9703 27.4688H27.1874C27.6159 27.4682 28.0367 27.3547 28.4073 27.1396C28.778 26.9246 29.0854 26.6157 29.2985 26.244C29.5117 25.8723 29.6232 25.451 29.6216 25.0225C29.6201 24.594 29.5056 24.1735 29.2898 23.8034ZM14.9999 29.9062C14.244 29.906 13.5068 29.6715 12.8897 29.235C12.2726 28.7985 11.8059 28.1814 11.5539 27.4688H18.446C18.194 28.1814 17.7273 28.7985 17.1102 29.235C16.4931 29.6715 15.7558 29.906 14.9999 29.9062ZM2.81244 25.0312C3.98549 23.0142 5.24994 18.3403 5.24994 12.8438C5.24994 10.2579 6.27717 7.77794 8.10565 5.94946C9.93413 4.12098 12.4141 3.09375 14.9999 3.09375C17.5858 3.09375 20.0658 4.12098 21.8942 5.94946C23.7227 7.77794 24.7499 10.2579 24.7499 12.8438C24.7499 18.3357 26.0113 23.0096 27.1874 25.0312H2.81244Z"
                                  fill="black"/>
                        </svg>
                        <div class="w-[25px] h-[25px] bg-black rounded-full absolute top-[-10px] left-1/2 flex justify-center">
                            <span class="text-center text-white text-[13px] self-center">12</span>
                        </div>
                    </div>
                    <div class="flex-row flex bg-black rounded-3xl px-3 py-2 gap-4">
                        <img class="w-6 object-cover" src="./assets/user.png" alt="user-image">
                        <span class="text-white text-[14px] self-center font-bold">User name</span>
                        <div class="self-center">
                            <svg width="22" height="23" viewBox="0 0 22 23" fill="none"
                                 xmlns="http://www.w3.org/2000/svg">
                                <path d="M18.3613 9.23642L11.4863 16.1114C11.4225 16.1753 11.3466 16.2261 11.2632 16.2607C11.1797 16.2952 11.0902 16.3131 10.9999 16.3131C10.9095 16.3131 10.8201 16.2952 10.7366 16.2607C10.6532 16.2261 10.5773 16.1753 10.5135 16.1114L3.63849 9.23642C3.50948 9.10742 3.43701 8.93245 3.43701 8.75002C3.43701 8.56758 3.50948 8.39261 3.63849 8.26361C3.76749 8.13461 3.94246 8.06213 4.12489 8.06213C4.30733 8.06213 4.4823 8.13461 4.6113 8.26361L10.9999 14.6531L17.3885 8.26361C17.4524 8.19973 17.5282 8.14906 17.6117 8.1145C17.6951 8.07993 17.7846 8.06213 17.8749 8.06213C17.9652 8.06213 18.0547 8.07993 18.1381 8.1145C18.2216 8.14906 18.2974 8.19973 18.3613 8.26361C18.4252 8.32749 18.4758 8.40332 18.5104 8.48677C18.545 8.57023 18.5628 8.65968 18.5628 8.75002C18.5628 8.84035 18.545 8.9298 18.5104 9.01326C18.4758 9.09672 18.4252 9.17255 18.3613 9.23642Z"
                                      fill="#F4F5F7"/>
                            </svg>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="bg-default w-full">
        <div class="mx-auto">
            <div class="flex flex-wrap">
                <div class="w-[16%] bg-white pt-3">
                    <aside class="w-full px-5">
                        <ul class="flex flex-col gap-2">
                            <li>
                                <a href="#" class="text-[16px] flex flex-row text-[#090E18] gap-2">
                                    <svg class="text-[16px] self-center w-[16px] h-[16px]" viewBox="0 0 18 18"
                                         fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M0 10H8V0H0V10ZM0 18H8V12H0V18ZM10 18H18V8H10V18ZM10 0V6H18V0H10Z"
                                              fill="#090E18"/>
                                    </svg>
                                    <span>Dashboard</span>
                                </a>
                            </li>
                            <li>
                                <a href="#" class="text-[16px] flex flex-row text-[#090E18] gap-2">
                                    <svg class="self-center w-[20px] h-[20px]" viewBox="0 0 24 24" fill="none"
                                         xmlns="http://www.w3.org/2000/svg">
                                        <g clip-path="url(#clip0_120_192)">
                                            <path d="M8.68601 4.00001L11.293 1.39301C11.4805 1.20554 11.7348 1.10022 12 1.10022C12.2652 1.10022 12.5195 1.20554 12.707 1.39301L15.314 4.00001H19C19.2652 4.00001 19.5196 4.10536 19.7071 4.2929C19.8946 4.48044 20 4.73479 20 5.00001V8.68601L22.607 11.293C22.7945 11.4805 22.8998 11.7348 22.8998 12C22.8998 12.2652 22.7945 12.5195 22.607 12.707L20 15.314V19C20 19.2652 19.8946 19.5196 19.7071 19.7071C19.5196 19.8946 19.2652 20 19 20H15.314L12.707 22.607C12.5195 22.7945 12.2652 22.8998 12 22.8998C11.7348 22.8998 11.4805 22.7945 11.293 22.607L8.68601 20H5.00001C4.73479 20 4.48044 19.8946 4.2929 19.7071C4.10536 19.5196 4.00001 19.2652 4.00001 19V15.314L1.39301 12.707C1.20554 12.5195 1.10022 12.2652 1.10022 12C1.10022 11.7348 1.20554 11.4805 1.39301 11.293L4.00001 8.68601V5.00001C4.00001 4.73479 4.10536 4.48044 4.2929 4.2929C4.48044 4.10536 4.73479 4.00001 5.00001 4.00001H8.68601ZM12 15C12.7957 15 13.5587 14.6839 14.1213 14.1213C14.6839 13.5587 15 12.7957 15 12C15 11.2044 14.6839 10.4413 14.1213 9.87868C13.5587 9.31608 12.7957 9.00001 12 9.00001C11.2044 9.00001 10.4413 9.31608 9.87868 9.87868C9.31608 10.4413 9.00001 11.2044 9.00001 12C9.00001 12.7957 9.31608 13.5587 9.87868 14.1213C10.4413 14.6839 11.2044 15 12 15Z"
                                                  fill="#090E18"/>
                                        </g>
                                        <defs>
                                            <clipPath id="clip0_120_192">
                                                <rect width="24" height="24" fill="white"/>
                                            </clipPath>
                                        </defs>
                                    </svg>
                                    <span>Setting</span>
                                </a>
                            </li>
                            <li>
                                <a href="#" class="text-[16px] flex flex-row text-[#090E18] gap-2">
                                    <svg class="self-center w-[20px] h-[20px]" viewBox="0 0 24 24" fill="none"
                                         xmlns="http://www.w3.org/2000/svg">
                                        <g clip-path="url(#clip0_120_156)">
                                            <path d="M6.455 19L2 22.5V4C2 3.73478 2.10536 3.48043 2.29289 3.29289C2.48043 3.10536 2.73478 3 3 3H21C21.2652 3 21.5196 3.10536 21.7071 3.29289C21.8946 3.48043 22 3.73478 22 4V18C22 18.2652 21.8946 18.5196 21.7071 18.7071C21.5196 18.8946 21.2652 19 21 19H6.455ZM7 10V12H9V10H7ZM11 10V12H13V10H11ZM15 10V12H17V10H15Z"
                                                  fill="#090E18"/>
                                        </g>
                                        <defs>
                                            <clipPath id="clip0_120_156">
                                                <rect width="24" height="24" fill="white"/>
                                            </clipPath>
                                        </defs>
                                    </svg>
                                    <span>Chat Box</span>
                                </a>
                            </li>

                            <li>
                                <a href="#" class="text-[16px] flex flex-row text-[#090E18] gap-2">
                                    <svg class="self-center w-[20px] h-[20px]" viewBox="0 0 18 20" fill="none"
                                         xmlns="http://www.w3.org/2000/svg">
                                        <path d="M18 0.992V19.008C17.9979 19.2706 17.8926 19.5219 17.7068 19.7075C17.521 19.8931 17.2696 19.9982 17.007 20H0.993C0.729813 20 0.477391 19.8955 0.291196 19.7095C0.105001 19.5235 0.000265042 19.2712 0 19.008V0.992C0.00209465 0.72938 0.107418 0.478126 0.293218 0.292513C0.479017 0.1069 0.730378 0.00183004 0.993 0H17.007C17.555 0 18 0.444 18 0.992ZM8.293 11.122L5.818 8.646L4.404 10.061L8.293 13.95L13.95 8.293L12.536 6.879L8.293 11.121V11.122Z"
                                              fill="#090E18"/>
                                    </svg>

                                    <span class="grow">Task</span>


                                    <svg class="self-center w-[10px] h-[6px] justify-items-end" viewBox="0 0 10 6"
                                         fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M5.00005 3.879L8.71255 0.166504L9.77305 1.227L5.00005 6L0.227051 1.227L1.28755 0.166504L5.00005 3.879Z"
                                              fill="#090E18"/>
                                    </svg>

                                </a>
                                <ul class="pl-4 pt-4 flex flex-col gap-3">
                                    <li>
                                        <a href="#" class="text-[16px] flex flex-row text-[#777B84] gap-2">
                                            <svg class="self-center w-[20px] h-[20px]" viewBox="0 0 12 16" fill="none"
                                                 xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.376 8.41595L0.777 15.4819C0.701706 15.5321 0.61423 15.5608 0.523891 15.5651C0.433553 15.5694 0.343733 15.5492 0.263999 15.5065C0.184265 15.4638 0.117604 15.4003 0.0711136 15.3227C0.0246236 15.2451 4.67204e-05 15.1564 0 15.0659V0.933946C4.67204e-05 0.843504 0.0246236 0.754768 0.0711136 0.677189C0.117604 0.599611 0.184265 0.536094 0.263999 0.493405C0.343733 0.450717 0.433553 0.430454 0.523891 0.434775C0.61423 0.439097 0.701706 0.467841 0.777 0.517946L11.376 7.58395C11.4445 7.62961 11.5006 7.69147 11.5395 7.76404C11.5783 7.83661 11.5986 7.91764 11.5986 7.99995C11.5986 8.08225 11.5783 8.16329 11.5395 8.23585C11.5006 8.30842 11.4445 8.37029 11.376 8.41595Z"
                                                      fill="#777B84"/>
                                            </svg>

                                            <span class="text-[16px]">UI/UX Prototype Update</span>
                                        </a>
                                    </li>

                                    <li>
                                        <a href="#" class="text-[16px] flex flex-row text-[#777B84] gap-2">
                                            <svg class="self-center w-[20px] h-[20px]" viewBox="0 0 12 16" fill="none"
                                                 xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.376 8.41595L0.777 15.4819C0.701706 15.5321 0.61423 15.5608 0.523891 15.5651C0.433553 15.5694 0.343733 15.5492 0.263999 15.5065C0.184265 15.4638 0.117604 15.4003 0.0711136 15.3227C0.0246236 15.2451 4.67204e-05 15.1564 0 15.0659V0.933946C4.67204e-05 0.843504 0.0246236 0.754768 0.0711136 0.677189C0.117604 0.599611 0.184265 0.536094 0.263999 0.493405C0.343733 0.450717 0.433553 0.430454 0.523891 0.434775C0.61423 0.439097 0.701706 0.467841 0.777 0.517946L11.376 7.58395C11.4445 7.62961 11.5006 7.69147 11.5395 7.76404C11.5783 7.83661 11.5986 7.91764 11.5986 7.99995C11.5986 8.08225 11.5783 8.16329 11.5395 8.23585C11.5006 8.30842 11.4445 8.37029 11.376 8.41595Z"
                                                      fill="#777B84"/>
                                            </svg>

                                            <span class="text-[16px]">Product Development</span>
                                        </a>
                                    </li>

                                    <li>
                                        <a href="#" class="text-[16px] flex flex-row text-[#777B84] gap-2">
                                            <svg class="self-center w-[20px] h-[20px]" viewBox="0 0 12 16" fill="none"
                                                 xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.376 8.41595L0.777 15.4819C0.701706 15.5321 0.61423 15.5608 0.523891 15.5651C0.433553 15.5694 0.343733 15.5492 0.263999 15.5065C0.184265 15.4638 0.117604 15.4003 0.0711136 15.3227C0.0246236 15.2451 4.67204e-05 15.1564 0 15.0659V0.933946C4.67204e-05 0.843504 0.0246236 0.754768 0.0711136 0.677189C0.117604 0.599611 0.184265 0.536094 0.263999 0.493405C0.343733 0.450717 0.433553 0.430454 0.523891 0.434775C0.61423 0.439097 0.701706 0.467841 0.777 0.517946L11.376 7.58395C11.4445 7.62961 11.5006 7.69147 11.5395 7.76404C11.5783 7.83661 11.5986 7.91764 11.5986 7.99995C11.5986 8.08225 11.5783 8.16329 11.5395 8.23585C11.5006 8.30842 11.4445 8.37029 11.376 8.41595Z"
                                                      fill="#777B84"/>
                                            </svg>

                                            <span class="text-[16px]">Feature Development</span>
                                        </a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </aside>
                </div>
                <div class="w-[84%] bg-default px-4 py-3 pb-20 overflow-x-scroll">
                    <div>
                        <ul class="flex flex-row gap-2 text-[#161E2E] text-[16px] font-normal">
                            <li><a href="#">Task /</a></li>
                            <li><a href="#">All Task /</a></li>
                            <li><a href="#">Product Development</a></li>
                        </ul>
                    </div>

                    <div class="py-3">
                        <h2 class="font-bold text-[#161E2E] text-[36px]">Product Development</h2>
                    </div>

                    <div class="flex-row flex gap-4">
                        <p class="self-center text-[16px] text-[#777B84]">Create Date: 25 September 2024</p>
                        <p class="grow self-center text-[16px] text-[#777B84]">Due Date: 15 October 2024</p>
                    </div>

                    <div class="flex-row flex gap-4 pt-4">
                        <div class="grow self-start pb-10">
                            <p class="text-[16px] font-semibold text-[#10141C]">Member on Board</p>
                            <ul class="flex flex-row relative">
                                <li class="absolute left-0 top-0 w-8 h-8 rounded-full border border-white"><img
                                        src="./assets/member.png" alt="member"></li>
                                <li class="absolute left-4 top-0 w-8 h-8 rounded-full border border-white"><img
                                        src="./assets/member.png" alt="member"></li>
                                <li class="absolute left-8 top-0 w-8 h-8 rounded-full border border-white"><img
                                        src="./assets/member.png" alt="member"></li>
                                <li class="absolute left-12 top-0 w-8 h-8 rounded-full border border-white"><img
                                        src="./assets/member.png" alt="member"></li>
                                <li class="absolute left-16 top-0 w-8 h-8 rounded-full border border-white"><img
                                        src="./assets/member+.png" alt="member"></li>
                            </ul>
                        </div>

                        <p class="self-center text-[#25272B] text-[16px] font-medium">Share
                            <font-awesome-icon :icon="faShare"/>
                        </p>
                        <a href="#" @click="showBoardModal" class="self-center bg-[#BE1E2D] px-3 py-1 text-[14px] text-white rounded-md">New
                            Board</a>
                    </div>

                    <div class="w-full grid grid-cols-4 pt-4 gap-4">
                        <div class="basis-1/3">
                            <div class="bg-[#E9E9FF] p-2 flex flew-row rounded-md gap-2">
                                <h3 class="uppercase text-[16px] font-semibold self-center">To do</h3>
                                <div class="grow self-center">
                                    <div class="w-5 h-5 bg-white rounded-full flex justify-center grow-1">
                                        <span class="self-center text-[14px] font-bold">12</span>
                                    </div>
                                </div>
                                <div class="w-6 h-6 bg-[#F1F1FF] rounded-full text-center flex justify-center">
                                    <font-awesome-icon :icon="faPlus" class="text-[14px] self-center"/>
                                </div>
                            </div>

                            <div class="px-3 pt-3 mt-4 border-dotted border border-[#AEAEAE] rounded-lg">
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                   <div class="pt-2 pb-9 border-b border-gray-200">
                                       <ul class="flex flex-row relative">
                                           <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                               src="./assets/member.png" class="object-cover" alt="member"></li>
                                           <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                               src="./assets/member.png" class="object-cover" alt="member"></li>
                                           <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                               src="./assets/member.png" class="object-cover" alt="member"></li>
                                           <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                               src="./assets/member.png" class="object-cover" alt="member"></li>
                                       </ul>
                                   </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="basis-1/3">
                            <div class="bg-[#FFFBE9] p-2 flex flew-row rounded-md gap-2">
                                <h3 class="uppercase text-[16px] font-semibold self-center">Work In Progress</h3>
                                <div class="grow self-center">
                                    <div class="w-6 h-6 bg-white rounded-full flex justify-center grow-1">
                                        <span class="self-center text-[14px] font-bold">12</span>
                                    </div>
                                </div>
                                <div class="w-6 h-6 bg-[#F1F1FF] rounded-full text-center flex justify-center">
                                    <font-awesome-icon :icon="faPlus" class="text-[14px] self-center"/>
                                </div>
                            </div>

                            <div class="px-3 pt-3 mt-4 border-dotted border border-[#AEAEAE] rounded-lg">
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="basis-1/3">
                            <div class="bg-[#FFDCC7] p-2 flex flew-row rounded-md gap-2">
                                <h3 class="uppercase text-[16px] font-semibold self-center">Under Review</h3>
                                <div class="grow self-center">
                                    <div class="w-6 h-6 bg-white rounded-full flex justify-center grow-1">
                                        <span class="self-center text-[14px] font-bold">12</span>
                                    </div>
                                </div>
                                <div class="w-6 h-6 bg-[#F1F1FF] rounded-full text-center flex justify-center">
                                    <font-awesome-icon :icon="faPlus" class="text-[14px] self-center"/>
                                </div>
                            </div>

                            <div class="px-3 pt-3 mt-4 border-dotted border border-[#AEAEAE] rounded-lg">
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="basis-1/3">
                            <div class="bg-[#E3F5E4] p-2 flex flew-row rounded-md gap-2">
                                <h3 class="uppercase text-[16px] font-semibold self-center">complete</h3>
                                <div class="grow self-center">
                                    <div class="w-6 h-6 bg-white rounded-full flex justify-center grow-1">
                                        <span class="self-center text-[14px] font-bold">12</span>
                                    </div>
                                </div>
                                <div class="w-6 h-6 bg-[#F1F1FF] rounded-full text-center flex justify-center">
                                    <font-awesome-icon :icon="faPlus" class="text-[14px] self-center"/>
                                </div>
                            </div>

                            <div class="px-3 pt-3 mt-4 border-dotted border border-[#AEAEAE] rounded-lg">
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="bg-white rounded-lg shadow-lg p-3 flex flex-col mb-4">
                                    <h3 class="text-[16px] font-semibold">Bug Tracking and Fixing</h3>
                                    <p class="text-[16px] text-[#2E3033] font-normal">Log and track all bugs discovered during testing, and implement necessary fixes. users to gather initi</p>
                                    <div class="pt-2 pb-9 border-b border-gray-200">
                                        <ul class="flex flex-row relative">
                                            <li class="absolute left-0 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-4 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-8 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                            <li class="absolute left-12 top-0 w-7 h-7 rounded-full border border-white"><img
                                                src="./assets/member.png" class="object-cover" alt="member"></li>
                                        </ul>
                                    </div>
                                    <div class="flex flex-row justify-between mt-1">
                                        <div class="bg-[#FA8223] rounded-lg flex justify-between py-1 px-2 gap-1">
                                            <svg class="self-center w-3 h-3" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM2 6.75V14.25H14V6.75H2ZM3.5 8.25H5V9.75H3.5V8.25ZM3.5 11.25H5V12.75H3.5V11.25ZM6.5 8.25H12.5V9.75H6.5V8.25ZM6.5 11.25H10.25V12.75H6.5V11.25Z" fill="white"/>
                                            </svg>
                                            <p class="text-[14px] text-white self-center">02 Sep 2024</p>
                                        </div>
                                        <div class="self-center">
                                            <div class="flex justify-between gap-1">
                                                <svg class="self-center w-3 h-3" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7 5C6.44772 5 6 5.44772 6 6C6 6.55228 6.44772 7 7 7V5ZM15 7C15.5523 7 16 6.55228 16 6C16 5.44772 15.5523 5 15 5V7ZM7 9C6.44772 9 6 9.44771 6 10C6 10.5523 6.44772 11 7 11V9ZM11 11C11.5523 11 12 10.5523 12 10C12 9.44771 11.5523 9 11 9V11ZM20.782 13.908L21.673 14.362L21.673 14.362L20.782 13.908ZM19.908 14.782L20.362 15.673L19.908 14.782ZM19.908 1.21799L20.362 0.326981V0.32698L19.908 1.21799ZM20.782 2.09202L21.673 1.63803V1.63803L20.782 2.09202ZM2.09202 1.21799L2.54601 2.10899H2.54601L2.09202 1.21799ZM1.21799 2.09202L2.10899 2.54601V2.54601L1.21799 2.09202ZM2.20734 18.3861L2.78426 19.2029L2.78437 19.2028L2.20734 18.3861ZM6.16989 15.5865L5.59287 14.7698L5.59286 14.7698L6.16989 15.5865ZM1.09027 18.4776L1.90973 17.9044L1.90973 17.9044L1.09027 18.4776ZM2.10335 18.4483L1.65661 17.5536L1.6566 17.5537L2.10335 18.4483ZM1.42692 18.6856L1.28076 19.6749H1.28076L1.42692 18.6856ZM2.16983 18.412L1.63068 17.5697L1.63054 17.5698L2.16983 18.412ZM2.14376 18.4276L1.65674 17.5542L1.65668 17.5542L2.14376 18.4276ZM7.26828 15.034L7.45176 16.017L7.45176 16.017L7.26828 15.034ZM6.80048 15.1825L7.21786 16.0913L7.21786 16.0913L6.80048 15.1825ZM7 7H15V5H7V7ZM7 11H11V9H7V11ZM4.2 2H17.8V0H4.2V2ZM20 4.2V11.8H22V4.2H20ZM20 11.8C20 12.3766 19.9992 12.7488 19.9761 13.0322C19.9539 13.3038 19.9162 13.4045 19.891 13.454L21.673 14.362C21.8658 13.9836 21.9371 13.5904 21.9694 13.195C22.0008 12.8114 22 12.3436 22 11.8H20ZM17.8 16C18.3436 16 18.8114 16.0008 19.195 15.9694C19.5904 15.9371 19.9836 15.8658 20.362 15.673L19.454 13.891C19.4045 13.9162 19.3038 13.9539 19.0322 13.9761C18.7488 13.9992 18.3766 14 17.8 14V16ZM19.891 13.454C19.7951 13.6422 19.6422 13.7951 19.454 13.891L20.362 15.673C20.9265 15.3854 21.3854 14.9265 21.673 14.362L19.891 13.454ZM17.8 2C18.3766 2 18.7488 2.00078 19.0322 2.02393C19.3038 2.04612 19.4045 2.0838 19.454 2.10899L20.362 0.32698C19.9836 0.134186 19.5904 0.0628705 19.195 0.0305695C18.8114 -0.000777721 18.3436 0 17.8 0V2ZM22 4.2C22 3.65645 22.0008 3.18864 21.9694 2.80497C21.9371 2.40963 21.8658 2.01641 21.673 1.63803L19.891 2.54601C19.9162 2.59545 19.9539 2.69617 19.9761 2.96784C19.9992 3.25117 20 3.62345 20 4.2H22ZM19.454 2.10899C19.6422 2.20487 19.7951 2.35785 19.891 2.54601L21.673 1.63803C21.3854 1.07354 20.9265 0.614602 20.362 0.326981L19.454 2.10899ZM4.2 0C3.65645 0 3.18864 -0.000777721 2.80497 0.0305695C2.40963 0.0628705 2.01641 0.134187 1.63803 0.326981L2.54601 2.10899C2.59545 2.0838 2.69617 2.04612 2.96784 2.02393C3.25117 2.00078 3.62345 2 4.2 2V0ZM2 4.2C2 3.62345 2.00078 3.25117 2.02393 2.96784C2.04612 2.69617 2.0838 2.59545 2.10899 2.54601L0.326981 1.63803C0.134187 2.01641 0.0628705 2.40963 0.0305695 2.80497C-0.000777721 3.18864 0 3.65645 0 4.2H2ZM1.63803 0.326981C1.07354 0.614601 0.614601 1.07354 0.326981 1.63803L2.10899 2.54601C2.20487 2.35785 2.35785 2.20487 2.54601 2.10899L1.63803 0.326981ZM17.8 14H8.01639V16H17.8V14ZM2.78437 19.2028L6.74692 16.4032L5.59286 14.7698L1.63031 17.5694L2.78437 19.2028ZM0 17.7056C0 17.9004 -0.000996709 18.1154 0.0154464 18.295C0.0317577 18.4733 0.0748032 18.7704 0.270816 19.0507L1.90973 17.9044C1.96386 17.9818 1.98927 18.0514 2.00042 18.0909C2.01028 18.1258 2.00955 18.1393 2.00712 18.1127C2.00477 18.0871 2.00251 18.0443 2.00126 17.9717C2.00003 17.8997 2 17.8153 2 17.7056H0ZM1.6566 17.5537C1.56941 17.5972 1.50231 17.6304 1.44576 17.657C1.38865 17.6839 1.35586 17.6977 1.33782 17.7045C1.31922 17.7115 1.33421 17.7042 1.37166 17.6975C1.41332 17.6902 1.48435 17.6832 1.57308 17.6964L1.28076 19.6749C1.60412 19.7226 1.87711 19.6385 2.04307 19.576C2.20801 19.5138 2.38921 19.4233 2.55009 19.343L1.6566 17.5537ZM0.270815 19.0507C0.507292 19.3888 0.872596 19.6146 1.28076 19.6749L1.57308 17.6964C1.70913 17.7165 1.8309 17.7917 1.90973 17.9044L0.270815 19.0507ZM2 17.7056V4.2H0V17.7056H2ZM1.63042 17.5693C1.62554 17.5727 1.62228 17.575 1.61951 17.577C1.61821 17.5779 1.61728 17.5786 1.6166 17.579C1.61593 17.5795 1.61564 17.5797 1.61565 17.5797C1.61584 17.5796 1.62182 17.5754 1.63068 17.5697L2.70899 19.2542C2.74215 19.2329 2.77291 19.2109 2.78426 19.2029L1.63042 17.5693ZM2.55008 19.343C2.56287 19.3366 2.59646 19.3201 2.63084 19.3009L1.65668 17.5542C1.66568 17.5492 1.6721 17.5459 1.6725 17.5457C1.67253 17.5457 1.67224 17.5458 1.67153 17.5462C1.67082 17.5465 1.66983 17.547 1.66844 17.5477C1.66547 17.5492 1.66191 17.551 1.65661 17.5536L2.55008 19.343ZM1.63054 17.5698C1.63917 17.5643 1.64785 17.5591 1.65674 17.5542L2.63077 19.301C2.6573 19.2862 2.68349 19.2705 2.70913 19.2541L1.63054 17.5698ZM8.01639 14C7.67508 14 7.37861 13.9961 7.0848 14.0509L7.45176 16.017C7.52177 16.0039 7.60276 16 8.01639 16V14ZM6.74692 16.4032C7.08474 16.1645 7.15314 16.121 7.21786 16.0913L6.38311 14.2738C6.1115 14.3985 5.87161 14.5728 5.59287 14.7698L6.74692 16.4032ZM7.0848 14.0509C6.84264 14.0961 6.60696 14.171 6.3831 14.2738L7.21786 16.0913C7.29248 16.057 7.37104 16.032 7.45176 16.017L7.0848 14.0509Z" fill="#777B84"/>
                                                </svg>

                                                <p class="text-[14px] text-black self-center">02</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </div>
    <Modal :show="boardShow" max-width="sm">
        <div class="min-w-10 p-4">
            <form>
                <div class="flex flex-col">
                    <label class="text-[17px] pb-1">Board Name</label>
                    <input placeholder="Enter board name..." class="text-[#939DA7] text-[16px] font-light border border-gray-200 p-2 bg-[#E0E4E8] rounded-md"/>
                </div>
                <div class="flex flex-row justify-center gap-6">
                    <button type="button" @click="closeBoardModal" class="px-3 py-1 rounded-lg bg-[#E5E7EB] hover:bg-[#BE1E2D] hover:text-white text-[#6B7280] font-normal text-[16px] mt-3">Cancel</button>
                    <button class="px-3 py-1 rounded-lg bg-[#BE1E2D] text-white font-normal text-[16px] mt-3">Create</button>
                </div>
            </form>
        </div>
    </Modal>
</template>

<style scoped>

</style>
