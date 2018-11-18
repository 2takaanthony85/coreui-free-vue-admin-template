<template>
    <b-form-input class="row-text" type="text" v-model="currentVal"></b-form-input>
</template>

<script>
export default {
    name: 'text-input',
    props: [
        'value',
        'num'
    ],
    data: function () {
        return {
            val: '',
            index: 0
        }
    },
    created () {
        this.val = this.value
        this.index = this.num
    },
    computed: {
        currentVal: {
            get: function () {
                return this.val
            },
            set: function (newValue) {
                //console.log(newValue)
                this.$emit('updateVal', newValue, this.index)
            }
        }
    }
}
</script>


<style lang="scss">
.row-text {
    margin-bottom: 5px;
}
</style>