<script>
	export let data;

	let { supabase, session } = data;
	$: ({ supabase, session } = data);
</script>

<div class="flex flex-col items-center">
	<h1>Account</h1>
	{#if session}
		<p>Logged in as {session.user.email}</p>
	{:else}
		<p>Not logged in</p>
	{/if}
</div>
