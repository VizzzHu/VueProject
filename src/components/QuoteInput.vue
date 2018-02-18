<template>
	<div>
		<span>Quote:</span>
		<div>
			<textarea class="quote-input-textarea" rows="5" v-model="newQuote"></textarea>
		</div>
		<button class="quote-input-btn" @click="addAQuote">Add Quote</button>
	</div>

	
</template>

<script>
export default {
	data: function() {
		return {
			newQuote: '',
		};
	},
	props: {
		addQuote: Function,
	},
	methods: {
		addAQuote() {
			if (!this.newQuote) {
				alert('Plese input a quote!');
				return;
			}
			
			this.addQuote(this.newQuote);
			this.newQuote = '';
		},
		// inputQuote(event) {
		// 	this.newQuote = event.target.value;
		// },
	},
}
</script>

<style scoped>
.quote-input-textarea {
	width: 50%;
}
</style>
