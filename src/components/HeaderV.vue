<template>
    <header>
        <h1>{{title}}</h1>
        <ButtonV 
        @btn-click="$emit
        ('toggle-add-task')" 
        :text="showAddTask ? 'Close' : 'Add Task'" 
        :color="showAddTask ? 'red' : 'green'"/>
    </header>
</template>

<script>
import ButtonV from './ButtonV.vue'

    export default{
        name: 'HeaderV',
        props: {
            title: String,
            showAddTask: Boolean
        },
        components:{
            ButtonV,
        },
    }
</script>

<style scoped>
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;
    }
    </style>