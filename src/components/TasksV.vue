<template>
<div :key="task.id" v-for="task in tasks">
    <TaskV @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task" />
</div>
</template>

<script>
import TaskV from './TaskV'

    export default {
        name : 'TasksV',
        props: {
            tasks: Array,
        },
        components:{
            TaskV,
        },
        emits:['delete-task','toggle-reminder'],
    }
</script>