<template>
  <div>
    <h3>Hello From Child</h3>
    <slot :data="data" :hello="hello" />
  </div>
</template>

<script>
    export default {
        
        data: ()=>({
            data: 'This is from the child slot-scope'
        }),
        methods: {
            hello(){
                window.alert('THIS IS FROM THE CHILD')
            }
        }
    }
</script>

<style lang="scss" scoped>
</style>