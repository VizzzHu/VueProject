<template>
    <div class="quote-head">
        <span>Quotes Added</span>
        <div class="progress">
            <div 
                class="progress-bar"
                role="progressbar"
                aria-valuenow="60"
                aria-valuemin="0"
                aria-valuemax="100"
                :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">
                {{ quoteCount }} / {{ maxQuotes }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        quoteCount: Number,
        maxQuotes: Number,
    },
}
</script>

<style scoped>
.quote-process-bar {
  width: 90%;
  height: 30px;
  border: 1px solid gray;
  margin: 5px 10px;
}
</style>
