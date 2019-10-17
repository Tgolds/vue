<template>
    <div>
        <input type="text" v-model="a">
        <button @click="b">提交</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            a : ''
        }
    },
    methods: {
        b(){
            localStorage.setItem('aaaaa',this.a)
            this.$router.push({
                path:'/users'
            })
        },
        c(){
            this.a = localStorage.getItem('aaaaa')
        }
    },
    created(){
        this.c()
    }
}
</script>

<style lang="stylus" scoped>

</style>