<template>
    <div class="main">
        <post-form
        @create="createPost"
        />
        <post-list
        :posts="posts"
        />
    </div>
</template>

<script>
import postForm from '@/components/postForm.vue';
import postList from '@/components/postList.vue';

export default {
  components: { postForm, postList },
    data() {
        return {
            posts: [
                {id: 1, title: 'JS', body: 'ntrcn ntkf cjj,otybz'},
                {id: 2, title: 'Vue', body: 'ghgjhk jg glgkg '},
                {id: 3, title: 'React', body: 'просто тект ни о чем'},
                {id: 4, title: 'React2', body: 'просто'},
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        }
    }
}
</script>

<style>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

.main {
    padding: 20px;
    font-family: 'Raleway', sans-serif;
}
h2 {
    font-weight: 600;
}

</style>>