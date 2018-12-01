<template>
    <div class="post-answer">
        <h3>Post an answer</h3>
        <textarea name="answerText" v-model="content"></textarea>
        <button @click="postAnswer">Post answer</button>
    </div>
</template>

<script>
import axios from 'axios';
import apiPosts from '~/plugins/api/posts.js';
//console.log(apiPosts);

export default {
    props: {
        'thread': String,
    },
    data() {
        return {
            content: ''
        }
    },
    methods: {
        postAnswer () {
            var url = process.env.apiEndpoint+'/Threads.json';

            var postContent = this.content;
            var slug = this.thread;

            axios.post(url, {
                "slug": slug,
                "content": postContent, //"Her er en ny post jeg har satt opp",
                "user": "Bedeho"
            }).then(r => {
                console.log("Response ",r);
                // r.status === 200 // Successfull
                    // Id = r.data.name
            }).catch(e => {
                console.error(e);
            });
            
            // Call generate after post is successful
        }
    }
}
</script>