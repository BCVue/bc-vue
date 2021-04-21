<template>
    <button-base :Text="{Text}" :Class="danger"/>
</template>

<script>
import ButtonBase from '../../ComponentsBase/ButtonBase.vue'


export default {
  components: { ButtonBase },
    props:{
        Text:String
   }
}
</script>

