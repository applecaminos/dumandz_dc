<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="container-sm mt-4">
        
        <div class="row">
            <div class="col-md-12">
                <div class="row">
                    <div class="container mx-auto">
                        <div class="container d-flex mb-3">
                            <img class="w-50" src="https://d1rlzxa98cyc61.cloudfront.net/wysiwyg/pages/laptop-freeshipping-2022-image1-updated.jpg" alt="">
                            <img class="w-50" src="https://d1rlzxa98cyc61.cloudfront.net/wysiwyg/pages/laptop-freeshipping-2022-image2.jpg" alt="">
                        </div>
                        <hr>
                        <!-- <p class="mb-3 text-start">NAVIGATIONS</p> -->
                        <div class="container d-flex">
                            <RouterLink to="/notebooks" class="btn btn-outline-dark p-3" style="font-size: 4rem; margin-right: 5px;"><i class="fa fa-laptop" aria-hidden="true"></i></RouterLink>
                            <RouterLink to="/notebooks" class="btn btn-outline-dark p-3" style="font-size: 4rem; margin-right: 5px;"><i class="fa-solid fa-computer"></i></RouterLink>
                            <a class="btn btn-outline-dark p-3" style="font-size: 4rem; margin-right: 5px;"><i class="fa fa-television" aria-hidden="true"></i></a>
                            <a class="btn btn-outline-dark p-3" style="font-size: 4rem; margin-right: 5px;"><i class="fa fa-headphones" aria-hidden="true"></i></a>
                            <a class="btn btn-outline-dark p-3" style="font-size: 4rem; margin-right: 5px;"><i class="fa fa-laptop" aria-hidden="true"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <RouterView/>
</template>