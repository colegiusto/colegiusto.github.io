<script>
    import { page } from '$app/stores';
</script>

<h2>{$page.status} {$page.error.message.toLowerCase()}</h2>
<a href="/">click here to return to home</a>