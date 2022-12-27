<script setup>
import {ref, watch, onMounted} from 'vue';
import { RouterLink, RouterView } from 'vue-router'

const cart = ref([])


watch(cart, (newVal) => {
    localStorage.setItem('cart', JSON.stringify(cart.value))
}, {
deep: true
})

onMounted(()=>{
    if(localStorage.getItem('cart')){
        try {
            cart.value = JSON.parse(localStorage.getItem('cart'))
        } catch (error) {
            localStorage.removeItem('cart')
        }
    }
})

const add1 = () => {
    cart.value.push({
        name: 'APPLE MACBOOK AIR (M2, 2022) MLY43PP/A',
        price: 93990.00
    })
}
const add2 = () => {
    cart.value.push({
        name: 'LENOVO YOGA 782UF0004PH ARCTIC GREY',
        price: 83995.00
    })
}
const add3 = () => {
    cart.value.push({
        name: 'Acer Swift 5 SF514-56T-53TL Mist Green',
        price: 62999.00
    })
}
const add4 = () => {
    cart.value.push({
        name: 'Huawei MateBook 14s Space Gray',
        price: 56999.00
    })
}
const add5 = () => {
    cart.value.push({
        name: 'Apple MacBook Pro (13-inch, M2, 2022) MNEQ3PP/A',
        price: 90990.00
    })
}
const add6 = () => {
    cart.value.push({
        name: 'HP Pavilion 14-DV1020TU Warm Gold',
        price: 47490.00
    })
}
const add7 = () => {
    cart.value.push({
        name: 'Acer Swift 3 SF314-43-R06N Silver',
        price: 39999.00
    })
}
const add8 = () => {
    cart.value.push({
        name: 'Huawei MateBook D14 NBB-WAH9 Mystic Silver',
        price: 37999.00
    })
}

function removeItem(id) {
    this.cart.splice(id,1)
}

</script>

<template>
    <div class="container-lg">
        <div class="row">
            <div class="col-md-12">
                <nav aria-label="breadcrumb">
                <ol class="breadcrumb">
                    <li class="breadcrumb-item"><RouterLink to="/">Home</RouterLink></li>
                    <li class="breadcrumb-item"><RouterLink to="/">PC</RouterLink></li>
                    <li class="breadcrumb-item active" aria-current="page">Notebooks</li>
                </ol>
                </nav>
            </div>
            <div class="container-sm mt-3">
                <div class="col-md-12 d-flex justify-content-between p-0">
                    <h1>NOTEBOOKS</h1>
                <button class="btn btn-success btn-sm" data-bs-toggle="modal" data-bs-target="#exampleModal" style="height:35px">
                    cart <i class="bi bi-cart"></i>
                </button>
                </div>
                <div class="row mt-5 d-flex justify-content-between">
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/8/183892_2022.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">APPLE MACBOOK AIR (M2, 2022) MLY43PP/A</a>
                                <p class="fw-lighter" style="font-size: 13px">13.6-inch, M2 Chip, 8-Core CPU, Midnight, 512GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 93,990</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add1()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/8/185289_2022_7.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">LENOVO YOGA 782UF0004PH ARCTIC GREY</a>
                                <p class="fw-lighter" style="font-size: 13px">16-inch 2.5K, Intel Core i5-12500H, 16GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 83,995</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add2()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/8/184436_2022_4.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">Acer Swift 5 SF514-56T-53TL Mist Green</a>
                                <p class="fw-lighter" style="font-size: 13px">14-inch WQXGA, Intel Core i5-1240P, 8GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 62,999</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add3()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/7/177709_2020.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">Huawei MateBook 14s Space Gray</a>
                                <p class="fw-lighter" style="font-size: 13px">14-inch 2.5K, 11th Gen Intel Core i5-11300H, 8GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 56,999</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add4()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/8/183817_2022.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">Apple MacBook Pro (13-inch, M2, 2022) MNEQ3PP/A</a>
                                <p class="fw-lighter" style="font-size: 13px">13-inch, M2 Chip, 8-Core CPU, Silver, 512GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 90,990</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add5()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/8/181200_2022.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">HP Pavilion 14-DV1020TU Warm Gold</a>
                                <p class="fw-lighter" style="font-size: 13px">14-inch, Intel Core i5 1155G7, 8GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 47,490</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add6()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/8/181322_2022.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">Acer Swift 3 SF314-43-R06N Silver</a>
                                <p class="fw-lighter" style="font-size: 13px">14-inch Full HD, AMD Ryzen 5 5500U, 8GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 39,999</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add7()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3 mb-3">
                        <div class="col-md-12" style="background-color: #ffff;">
                            <img class="w-100 mt-3" src="https://d1rlzxa98cyc61.cloudfront.net/catalog/product/cache/1801c418208f9607a371e61f8d9184d9/1/7/176477_2020.jpg" alt="">
                            <div class="container">
                                <a href="#" class="fw-bold text-dark">Huawei MateBook D14 NBB-WAH9 Mystic Silver</a>
                                <p class="fw-lighter" style="font-size: 13px">14-inch Full HD, Intel Core i5-10210U, 8GB</p>
                                <p class="fw-lighter mb-1" style="font-size: 13px">P 37,999</p>
                                <button class="btn btn-success btn-md w-100 mb-3" v-on:click="add8()">Add to cart <i class="fa fa-shopping-cart" aria-hidden="true"></i></button>
                            </div>
                        </div>
                    </div>
                </div>          
            </div>
        </div>
    </div>
    <!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title fs-5" id="exampleModalLabel">Cart</h5>
        <button type="button" class="btn btn-close" data-bs-dismiss="modal" aria-label="Close">x</button>
      </div>
      <div class="modal-body">
        <table class="table">
          <thead>
            <tr>
              <th>#</th>
              <th>Item</th>
              <th>Price</th>
              <th>Remove</th>
            </tr>
        </thead>
        <tbody v-for="(item, index) in cart" :key="id">
            <tr>
                <td>{{ index+1 }}</td>
                <td>{{ item.name }}</td>
                <td>{{ item.price }}</td>
                <td class="text-center"><button class="btn btn-sm" v-on:click="removeItem(index)"><i class="bi bi-x-circle-fill"></i></button></td>
            </tr>
        </tbody>
        </table>
        <p class="text-center" v-if="!cart.length">You have no item added in the cart</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-success">Check Out</button>
      </div>
    </div>
  </div>
</div>
    <RouterView/>
</template>