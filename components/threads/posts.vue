<template>
    <div class="posts">
        <div class="post" v-for="(post,index) in posts" :key="index">
            <p>{{post.content}}</p>
            <span>{{post.user}}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        posts: Array
    }
}
</script>