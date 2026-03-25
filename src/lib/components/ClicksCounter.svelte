<script>
    console.log('Hello world!');
    let count = $state(0);
    let doubled = $derived(count * 2);
</script>

<h3>Clicks Counter</h3>

<button onclick={() => count++}>
    clicks: {count}
</button>

<span>
    doubled: {doubled}
</span>