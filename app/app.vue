<template>
	<div>
		<NuxtRouteAnnouncer />

		<ul>
			<li v-for="site in sites" :key="site.id">
        <!-- No type issue -->
				<p>{{ site.url }}</p>

        <!-- Has type issues -->
				<NuxtLink :href="`https://${site.url}`">
					{{ site.url }}
				</NuxtLink>
			</li>
		</ul>
	</div>
</template>

<script setup lang="ts">
const sites = [
	{ id: 1, url: 'example.com' },
	{ id: 2, url: 'example2.com' },
	{ id: 3, url: 'example3.com' },
	{ id: 4, url: 'example4.com' },
] as const;
</script>
