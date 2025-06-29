<script lang="ts">
async function fetchData() {
  const resp = await fetch("/api/data");
  return await resp.text();
}
</script>

<div class="prose max-w-none">
    <p>Move to `/demo`</p>
</div>
