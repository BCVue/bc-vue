<template>
    <div>
        <button class="btn" :class="{ButtonClass}">{{Text}}</button>
    </div>
</template>

<script>
export default {
    props:{
        Text:String,
        Class:String,
        Type:String
    },
    data() {
        return {
            ButtonClass:getButtonType()
        }
    },

    methods: {
        getButtonType(){
            switch(this.type){
                case "outLine":
                    return `outLine-${this.Class}`;
                case "backGround":
                    return `${this.Class}`;
                default:
                    return `${this.Class}`;
            }
        }
    }
}
</script>

<style lang="scss">
@import "../../assets/style/components/ComponentsBase/ButtonBase"
</style>

