<script lang="ts">
	import { Navbar } from '$lib';
	import 'remixicon/fonts/remixicon.css';
	import '../app.css';

	let { children } = $props();
</script>

<Navbar></Navbar>
{@render children()}
