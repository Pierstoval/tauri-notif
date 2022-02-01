<script lang="ts">
    import {requestPermission} from '@tauri-apps/api/notification';

    function onButtonClick() {
        requestPermission().then((response) => {
            if (response === "granted") {
                console.log("OK")
            } else {
                console.log("Permission is " + response);
            }
        }).catch(e => {
            console.info('Error: ', e);
        });
    }
</script>

<h1>Welcome to SvelteKit</h1>

Click this <button on:click={onButtonClick}>button</button> to trigger <code>Notification.requestPermission()</code>
