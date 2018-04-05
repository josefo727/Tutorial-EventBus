<template>
    <div>
        <hr>
        <ul class="list-unstyled">
            <li v-for="comment in comments" v-text="comment"></li>
        </ul>
    </div>
</template>

<script>
import EventBus from '../bus'

export default {
    name: 'ListComment',
    data () {
        return {
            comments: []
        }
    },
    created: function() {
        EventBus.$on('add-comment', (item) => {
            this.comments.push(item)
        });
    }
}
</script>