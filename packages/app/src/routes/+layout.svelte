<script lang="ts">
	import '../app.css';
	
	let { children } = $props();
</script>

<main class="w-screen h-screen">
    {@render children()}
</main>
