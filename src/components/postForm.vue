<template>
    <div>
        <h2>Создание постов</h2>
        <form @submit.prevent class="form">
            <input 
                v-model="post.title"
                class="input" 
                type="text" 
                placeholder="Название"
            >
            <input
                v-model="post.body"
                class="input"
                type="textarea"
                placeholder="Описание"
            >
        <mybutton @click="creatPost">Добавить</mybutton>
        </form>
    </div>
</template>

<script>
import mybutton from './UI/mybuttons.vue';
export default {
  components: { mybutton },
    data() {
        return {
            post: {
                title: '',
                body: ''
            }
        }
    },
    methods: {
        creatPost() {
            this.post.id = Date.now();
            this.$emit('create', this.post);
            this.post = {
                title: '',
                body: ''
            }
        }
    }
}
</script>

<style scoped>
.input {
    border: 1px solid #89c400;
    padding: 1em;
    margin: 10px 0;
}
.form {
    display: flex;
    flex-direction: column;
}

</style>