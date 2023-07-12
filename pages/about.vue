<template>
    <div>
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. In, corporis minima assumenda libero, maiores laudantium accusantium atque reprehenderit asperiores ipsum saepe dicta a consequatur recusandae nemo neque ipsa laboriosam explicabo.</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam assumenda quaerat quisquam? Porro pariatur provident nam quis distinctio assumenda dolorum ea nemo fuga similique? Voluptatibus ea nihil doloremque atque recusandae.</p>
        <div>{{ data }}</div>
    </div>
</template>

<script setup>
    const { data } = await useFetch('/api/kode?name=Mario', {
        method: 'post',
        body: { age: 30 }
    })
</script>

<style lang="css" scoped>
h2{
    margin-bottom: 20px;
    font-size: 36px;
 }
 p{
    margin: 20px 0
 }
</style>