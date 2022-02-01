<script lang="ts">
    function onButtonClick() {
        Notification.requestPermission(function () {
            console.info('requested permission.', {arguments});
        })
    }
</script>

<h1>Welcome to SvelteKit</h1>

Click this <button on:click={onButtonClick}>button</button> to trigger <code>Notification.requestPermission()</code>
