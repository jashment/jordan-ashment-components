<template>
<div>
    <div>
        <div id="serverDiv">
            <h4>Server Status: {{ status }}</h4>
        </div>
        <br>
        <button @click="changeStatus">Change Status</button>
    </div>
</div>
</template>

<script>
export default {
    data (){
        return {
            status: 'Normal'
        }
    },
    methods: {
        changeStatus() {
            alert('You are changing status of this server from: ' + this.status)
            if (this.status === 'Normal') {
                this.status = 'Critical'
            } else {
                this.status = 'Normal'
            }
        }
    }
}
</script>

<style scoped>
    div {
        float: left;
        margin: 1em;
        text-align: center;
        padding: .5em;
    }

    button {
        border: solid 1px black;
        border-radius: 10px;
        margin: auto;
        padding: 1em;
    }
    button:hover {
        background-color: gray;
        color: white;
    }
</style>

