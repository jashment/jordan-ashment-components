<template>


    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <a @click="changeStatus">
                <li class="list-group-item" v-for="i in 5">Server #{{ i, }}</li><span>{{status}}</span>
            </a>
        </ul>
    </div>
</template>

<script>
export default {
    data: function (){
        return {
            status: 'Normal'
        }
    },
    methods: {
        changeStatus() {
            this.status = 'Critical'
        }
    }
}
</script>

<style scoped>
    div {
        border: 1px solid blue;
    }
</style>
