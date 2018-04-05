<template>
    <div id="app">
        <add-comment></add-comment>
        <list-comment></list-comment>
    </div>
</template>

<script>
import AddComment  from './components/AddComment'
import ListComment from './components/ListComment'

export default {
    name: 'App',
    components: {
        AddComment, ListComment
    }
}
</script>