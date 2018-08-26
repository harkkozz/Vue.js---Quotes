<template>
    <div class="row">
        <div>
            <app-quote v-for="(quote, index) in quotes" :key="quote" @click.native="removeQuote(index)">{{ quote }}</app-quote>
        </div>
    </div>
</template>

<script>
import Quote from './Quote.vue';
    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote
        },
        methods: {
            removeQuote(index){
                this.$emit('quoteDeleted', index)
            }
        }
    }
</script>

<style>
</style>
