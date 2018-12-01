<template>
  <section class="thread">
    <h2>{{thread.title}}</h2>
    <div class="posts">
        <div class="post">
            {{thread.description}}
        </div>
    </div>
    <form name="post-answer">
        <h3>Post an answer</h3>
        <textarea name="answerText"></textarea>
        <button>Post answer</button>
    </form>
  </section>
</template>

<script>
import threads from '~/assets/threads.json';
//console.log("threads",threads);
export default {
    asyncData(context) {
        console.log("Slug ",context.params.slug);
        var slug = context.params.slug;
        var _threads = threads.filter(t => t.slug === slug);
        return {
            thread: _threads[0]
        }
    }
}
</script>
