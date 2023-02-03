<template>
    <div v-for="task in tasks" :key="task.id">
        <!-- <h3>{{ task.text }}</h3> -->
        <Task @toggle-reminder="$emit('toggle-reminder',task.id)" :task="task"  />
    </div>
</template>
<script>
 import Task from './Task'
    export default{
        name:'Tasks-component',
        props:{
            tasks: Array
        },
         components:{
            Task
         },
         emits:['delete-task','toggle-reminder']
}
</script>
<style>

</style>
