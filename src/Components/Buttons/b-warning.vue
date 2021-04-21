<template>
    <button-base :Text="{Text}" :Class="warning"/>
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

