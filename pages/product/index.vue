<template>
<div>
    <h1>Product Page</h1>
    <div class="container">
        <div class="card m-5" v-for="prd in allproduct" :key="prd.id">
            <img class="card-img-top" :src="prd.image" alt="">
            <div class="card-body">
                <h4 class="card-title">#{{prd.id}} - {{prd.name}}</h4>
                <p class="card-text">{{prd.detail}}</p>
            </div>
            <div class="card-footer text-muted">
                <!-- <a href="/product/1">รายละเอียด</a> -->
                <nuxtLink :to="{ name: 'product-id', params: { id: prd.id } }">
                    รายละเอียด
                </nuxtLink>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            // รายการสินค้าทั้งหมด
            allproduct: [{
                    id: '1',
                    name: 'Yamaha FSX5',
                    price: 10000,
                    detail: 'The guitar retains the original FG headstock shape, adorned with the iconic tuning fork logo. The traditional truss rod cover is emblazoned with Since 1966 to mark the launch of the first FG models.',
                    image: 'https://usa.yamaha.com/files/FG5_p_0004_400x299_268cd5d62f273ccefac0b65fcd7f0046.jpg'
                },
                {
                    id: '2',
                    name: 'Gibson Les Paul Standard 2019',
                    price: 150000,
                    detail: 'Seafoam Green, Blueberry Burst, Heritage Cherry Sunburst',
                    image: 'https://www.musicarms.net/wp-content/uploads/2019/01/Gibson-Les-Paul-Standard-2019-Pic-2-768x512.jpg'
                },
                {
                    id: '3',
                    price: 57000,
                    name: 'Fender American Performer Stratocaster RW',
                    detail: 'American Performer Stratocaster RW',
                    image: 'https://www.musicarms.net/wp-content/uploads/2019/03/fender-american-performer-stratocaster-Pic-6-768x512.jpg'
                }
            ]
        }
    }

}
</script>

<style>

</style>
