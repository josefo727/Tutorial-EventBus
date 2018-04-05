<template>
    <div>        
        <input type="text" class="form-control" v-model="comment" v-on:keyup.enter="addComment">
    </div>
</template>

<script>
import EventBus from '../bus'

export default {
    name: 'AddComment',
    data () {
        return {
            comment: ""
        }
    },
    methods: {
        addComment: function() {
            EventBus.$emit('add-comment', this.comment)            
            this.comment = ''
        }
    }
}
</script>