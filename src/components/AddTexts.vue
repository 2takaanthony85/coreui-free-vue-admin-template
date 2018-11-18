<template>
    <b-row>
        <b-col sm='12' md="8">
            <b-card header="title">
                <p>Hello World</p>
                <b-button class="up-button" @click="addText">＋</b-button>
                <div v-for="(val, index) in values" :key="index">
                    <text-input :value="val" :num="index"></text-input>
                </div>
            </b-card>
        </b-col>
    </b-row>
</template>

<script>
import TextInput from './TextInput.vue'

export default {
    name: 'add-texts',
    components: {
        TextInput
    },
    data: function () {
        return {
            values: ['a', 'b', 'c', 'd']
        }
    },
    methods: {
        addText: function () {
            this.values.push('')
        }
    }
}
</script>

<style lang="scss">
.up-button {
    margin-bottom: 10px;
}
</style>
