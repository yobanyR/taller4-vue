<template>
    <div class="post-card">
        <h3>{{ title }}</h3><br>
        <img :src="image" alt="Imagen de la publicación" /> <br>
        <p>{{ summary }}</p> <br>
        <p>{{ text }}</p><br>
        <a v-for="(link, index) in links" :key="index" :href="link.url">{{ link.label }}</a><br>
        <post-button />
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PostButton from './PostButton.vue';

interface Link {
    label: string;
    url: string;
}

export default defineComponent({
    name: "PostCard",
    components: {
        PostButton
    },
    props: {
        title: {
            type: String,
            default: ""
        },
        summary: {
            type: String,
            default: ""
        },
        text: {
            type: String,
            default: ""
        },
        image: {
            type: String,
            default: ""
        },
        links: {
            type: Array as () => Link[],
            default: () => []
        }
    }
})
</script>




<style lang="scss" scoped>
.post-card {
    border-radius: 15px;
    padding: 10px;
    margin: 5px;
    border: solid 1px #ccc;
}
</style>
