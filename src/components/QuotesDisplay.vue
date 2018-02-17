<template>
	<div class="quotes-display">
		<span>Quotes display</span>
		<div v-for="quote in quotes" :key="quote" class="quote-box">{{ quote }}</div>
	</div>
	
</template>

<script>
export default {
	props: {
		quotes: Array,
	},
}
</script>

<style scoped>
.quotes-display {
  width: 100%;
  height: 50vh;
  border: 1px solid black;
}

.quote-box {
	border: 1px solid gray;
}
</style>
