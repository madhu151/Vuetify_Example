<template>
    <div>
        <v-btn  slot="activator" class="primary">Add button </v-btn>
        <v-card>
            <v-card-title>
                <h2>Add new Details</h2>
            </v-card-title>
            <v-card-text>
                <v-form class="px-3" ref="form1">
                    <v-text-field label="Title" v-model="title" :rules="inputRules1"></v-text-field>
                    <v-text-field label="Name" v-model="title" :rules="inputRules2"></v-text-field>
                    <v-date-picker v-model="pdate"></v-date-picker>
                </v-form>
            </v-card-text>
        </v-card>
    </div>
</template>

<script>
export default {
    name: 'MyComp',
    data() {
        return {
            inputRules1: [
                v=> v.length >=3 || 'Min Chars Should be above 3'  ,
                v=> v.length <= 15 ||  'Max Chars Should be above 15'         
            ]
        }
    },

}
</script>


