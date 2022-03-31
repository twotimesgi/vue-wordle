<template>
    <div class="table">
        <RigaWord v-for="(row, index) in 5" :key="index" :targetWord="targetWord" :input="input" :i="i"/>
    </div>
</template>

<script>
import RigaWord from './RigaWord.vue';

export default {
  components: { RigaWord },
  name: 'FieldComp',
  props: {
    targetWord: String,
    i: Number,
    input: Array
  }
}
</script> 

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
}

.table{
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 40px;
}

#reset{
    padding: 8px 40px;
    font-size: 25px;
}
@keyframes shake {
    from{
        transform: translateX(-1%);
    }
    to{
        transform: translateX(1%);
    }
}


@keyframes grow {
    from{
        transform: scale(1.1);
    }
    to{
        transform: scale(1.0);
    }
}

</style>
