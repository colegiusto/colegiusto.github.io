<script>
    import { page } from '$app/stores';
</script>

<h1>{$page.status} {$page.error.message.toLowerCase()}</h1>
<a href="/">click here to return to home</a>