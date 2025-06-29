<script lang="ts">
import Settings from "virtual:icons/mynaui/cog-four-solid";
import HeartFull from "virtual:icons/mynaui/heart-solid";
import Share from "virtual:icons/mynaui/share-solid";

import type { Component } from "svelte";
import type { SvelteHTMLElements } from "svelte/elements";

let { imageUrl } = $props();

let heartState: "half" | "full" = $state("half");

function fillHeart() {
  heartState = "full";
  setTimeout(() => {
    heartState = "half";
  }, 3_000);
}
// bg-[url('{imageUrl}')]
</script>

<div
    class="
        h-screen
        container
        mx-auto
        bg-linear-90
        from-base-100
        via-base-300
        to-base-100
        bg-center
        bg-no-repeat
        bg-cover
        flex
        flex-col
        py-4
    "
>
  <div class="grow">
  </div>
  <div class="flex">
    <div class="flex flex-col grow pt-2 gap-2">
      <div>Title</div>
      <div class="max-h-28 overflow-scroll">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
      </div>
    </div>
    <div class="flex flex-col">
      <button
        class="btn btn-xl btn-ghost btn-circle"
        onclick={fillHeart}
      >
        <HeartFull
          color={heartState === 'half' ? 'white' : 'red'}
        />
      </button>
      <button class="btn btn-xl btn-ghost btn-circle">
        <Share />
      </button>
      <button class="btn btn-xl btn-ghost btn-circle">
        <Settings />
      </button>
    </div>
  </div>
</div>