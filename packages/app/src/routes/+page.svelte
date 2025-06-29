<script lang="ts">
async function fetchData() {
  const resp = await fetch("/api/data");
  return await resp.text();
}
</script>

<div class="w-full h-full p-4">
    <p>Move to <a href="demo">/demo</a></p>
</div>
