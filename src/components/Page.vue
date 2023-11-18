<template>
	<meta charset="utf-8">
	<div class="container">
		<div class="item">
			<div class="form-search">
				<input v-model="search_field">
				<button @click="send_request">Search</button>
			</div>
			<div class="result" v-if="result_not_empty">
				<ul>
					<li v-for="elm in search_result">{{ elm.value }}</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script setup>
	import {ref, computed} from 'vue';

	const api = import.meta.env.VITE_API_KEY;
	const secret = import.meta.env.VITE_SECRET_KEY;
	const search_field = ref("москва хабар");
	const search_result = ref([]);
	const result_not_empty = computed( () => search_result.value.length > 0);
	function send_request()
	{
		const url = 'https://suggestions.dadata.ru/suggestions/api/4_1/rs/suggest/address';
		const options = {
			method: "POST",
			mode: "cors",
			headers: {
				"Content-Type": "application/json",
				"Accept": "application/json",
				"Authorization": "Token " + api,
			},
			body: JSON.stringify({query : search_field.value}),
		
		};
		const handler1 = (res) => res.json();
		const handler2 = (res) => {search_result.value = res.suggestions};
		const handler3 = (res) => {alert('request error')};
		fetch(url, options).then(handler1).then(handler2).catch(handler3);
	}
</script>
<style></style>
