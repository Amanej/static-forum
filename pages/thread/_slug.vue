<template>
  <section class="thread">
    <h2>{{thread.title}}</h2>
    <Posts :posts="thread.posts" />
    <Answer :thread="thread.slug" />
    {{thread.slug}}
  </section>
</template>

<script>
import threads from '~/assets/threads.json';

import Answer from '~/components/forms/answer.vue';
import Posts from '~/components/threads/posts.vue';

export default {
    components: {
        Answer,
        Posts
    },
    asyncData(context) {
        //console.log("Slug ",context.params.slug);
        var slug = context.params.slug;
        var _threads = threads.filter(t => t.slug === slug);
        //console.log(_threads[0].posts);
        return {
            thread: _threads[0]
        }
    }
}
</script>
