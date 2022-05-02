<template>
    <div class="post">
        <div>
            <div class="title"><strong style="color:#999">НАЗВАНИЕ : </strong>  {{ block.title }}</div>
            <div class="description"> <span> Описание : </span> {{ block.body }}</div>
        </div>
        <div class="block__btns">
            <mybutton>Удалить</mybutton>
        </div>
    </div>
</template>

<script>
import mybutton from '@/components/UI/mybuttons'
export default {
    components: { mybutton },
    props: {
        block: {
            type: Object,
            required: true
        }
    }

}
</script>

<style>
.title {
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
    margin-bottom: 10px;
}
.description {
    color: #333;
}
.description span {
    padding: 0.75em;
    display: inline-block;
}
.post {
    padding: 2em;
    margin: 1em 0;
    border: 1px dashed #89c400;
    font-size: 0.875rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>