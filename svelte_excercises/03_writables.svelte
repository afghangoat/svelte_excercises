<script lang="ts">
	import {writable} from "svelte/store";

	const user = writable({ icon: "User icon placeholder"});
</script>

{$user.icon}