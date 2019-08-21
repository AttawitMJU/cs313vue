<template>
<div>
    <h1>Product Detail Page</h1>
    <h2>รหัสสินค้า = {{product.id}}</h2>
    <h2>ราคา = {{product.price}}</h2>
    <h2>รายละเอียด = {{product.detail}}</h2>
</div>
</template>

<script>
export default {
    data() {
        return {
            id: this.$route.params.id,
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
    },
    computed: {
        // ค้นหาสินค้าที่อยู่ใน array [allproduct] 
        // ตาม id ที่ส่งมา, return = {product} เอาไปแสดงผล ^
        product() {
            return this.allproduct.find(product =>   product.id === this.id)
        },
    }
}
</script>

<style>

</style>
