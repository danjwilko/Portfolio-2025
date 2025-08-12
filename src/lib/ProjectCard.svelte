<!-- src/lib/ProjectCard.svelte -->
<script>
  export let title;
  export let intro;
  export let description;
  export let tech = [];
  export let link;
  export let image = '';
  export let iframe = '';
   export let video = '';
</script>

<a
  href={link}
  target="_blank"
   class="relative block bg-gray-800 border border-cyan-500 p-4 rounded-lg transform 
  transition duration-50 hover:scale-102 hover:scale-105 hover:shadow-lg hover:shadow-cyan-500/30"
>
  {#if image && !iframe}
    <div
      class="bg-cover bg-center w-full h-48 object-cover rounded mb-4"
      style="background-image: url('{image}');"
    ></div>
  {/if}
{#if video}
  <video
    src={video}
    class="w-full h-48 rounded mb-4 object-cover"
    autoplay
    loop
    muted
    playsinline
  ></video>
{/if}
{#if iframe}
<div class="flex justify-center items-center">
  <iframe
    src={iframe}
    class="w-full h-24 rounded mb-1 relative inset-0 opacity-90"
    frameborder="0"
    loading="lazy"
    title={`${title} preview`}
  ></iframe>
  </div>
{/if}

<div class="relative z-10">
  <h3 class="text-xl text-blue-400 font-semibold mb-2">{title}</h3>
  <p class="text-sm text-gray-300 mb-2">{intro}</p>
  <p class="text-sm text-gray-300">{description}</p>
  <p class="text-sm text-gray-400 mt-2">
    {#if tech.length > 0}
      <span class="font-semibold">Tech:</span> {tech.join(', ')}
    {/if}
  </div>
</a>
