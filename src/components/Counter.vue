<template>
<div>
<h1>Counter: {{ counter }}</h1>
<button @click="decrement">Decremente</button>
<button @click="increment">Incremente</button>
</div>
</template>

<script>
import { mapState, mapMutations } from 'vuex'

export default{
    name: 'counter-j',
    computed:{
        ...mapState({
            counter:state => state.counter
        })     
    },
    methods: {
       ...mapMutations([
            'decrement',
            'increment'

       ])
    }
  }

</script>