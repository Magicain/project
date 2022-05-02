<template>
    <div>
        <h2>Список постов</h2>
        <post-item
        v-for="block in posts"
        :key="block.id"
        :block="block"
        />
    </div>
</template>

<script>
import postItem from '@/components/postItem.vue'
export default {
  components: { postItem },
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>

</style>