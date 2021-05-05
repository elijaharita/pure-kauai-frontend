<template>
	<article class="featured-property">
		<section class="featured-property-image">
			<img :src="src" :alt="name" />
		</section>
		<section class="featured-property-description">
			<h3>{{ name }}</h3>
			<p><slot></slot></p>
		</section>
		<section class="featured-property-info">
			<div>
				<strong>From {{ price }} per night</strong>
				<div>Sleeps {{ sleeps }}</div>
			</div>
			<nuxt-link class="button-like" :to="to">View Property</nuxt-link>
		</section>
	</article>
</template>

<style scoped>
article {
    box-sizing: border-box;
    padding: 1rem;
}

h3 {
    text-align: left;
}

img {
    width: 40rem;
    height: 30rem;
    margin-bottom: 2rem;
}

.featured-property-info {
    display: flex;
    justify-content: space-between;
}

.featured-property-info {}
</style>

<script>
export default {
	props: ["src", "to", "name", "price", "sleeps"],
};
</script>