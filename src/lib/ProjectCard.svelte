<!-- src/lib/ProjectCard.svelte -->
<script>
  export let title;
  export let intro;
  export let description;
  export let tech = [];
  export let link;
  export let image;
  export let iframe = '';
   export let video = '';
   export let button_link;
</script>
<a
  href={link}
  target="_blank"
   class="relative block bg-gray-800 border border-cyan-500 p-4 rounded-lg transform 
  transition duration-50 hover:scale-102 hover:scale-105 hover:shadow-lg hover:shadow-cyan-500/30"
>
  {#if image && !iframe}
    <div class="w-full aspect-[16/9] mr-4 relative rounded">
      <picture>
         <img
      src={image}
      alt={`${title} preview`}
      loading="lazy"
      decoding="async"
      class="w-full h-full object-cover"
    >
      </picture>
    </div>
  {/if}
{#if video}
<div class="w-full aspect-[16/9] relative rounded">
  <video
    src={video}
    class=" w-full h-full object-cover rounded"
    autoplay
    loop
    muted
    playsinline
  ></video>
</div>
{/if}
</a>
<div>
  <div class="relative z-10">
  <h3 class="text-xl text-blue-400 font-semibold mb-2">{title}</h3>
  <p class="text-sm text-gray-300 mb-2">{intro}</p>
  <p class="text-sm text-gray-300">{description}</p>
  <p class="text-sm text-gray-400 mt-2"></p>
    {#if tech.length > 0}
      <span class="font-semibold">Tech:</span> {tech.join(', ')}
    {/if}
  </div>
{#if button_link}
<a href={button_link} target="_blank" rel="noopener noreferrer"
     class="mt-2 inline-flex items-center gap-1 bg-gray-700 hover:bg-gray-600 text-white py-1 px-3 rounded-lg text-sm transition mb-4">
    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
      <path d="M12 .5C5.65.5.5 5.65.5 12c0 5.1 3.29 9.4 7.85 10.93.57.1.78-.25.78-.55 0-.27-.01-1.17-.02-2.12-3.19.69-3.87-1.54-3.87-1.54-.52-1.33-1.28-1.69-1.28-1.69-1.05-.71.08-.7.08-.7 1.16.08 1.77 1.19 1.77 1.19 1.03 1.77 2.7 1.26 3.36.96.1-.75.4-1.26.73-1.55-2.55-.29-5.23-1.28-5.23-5.68 0-1.26.45-2.29 1.18-3.1-.12-.29-.51-1.47.11-3.07 0 0 .96-.31 3.15 1.18.91-.25 1.88-.38 2.85-.38.97 0 1.94.13 2.85.38 2.19-1.49 3.15-1.18 3.15-1.18.62 1.6.23 2.78.11 3.07.74.81 1.18 1.84 1.18 3.1 0 4.41-2.68 5.38-5.24 5.66.41.35.77 1.05.77 2.12 0 1.53-.01 2.76-.01 3.13 0 .3.21.66.79.55C20.71 21.4 24 17.1 24 12c0-6.35-5.15-11.5-12-11.5z" />
    </svg>
    View Code
  </a>
  {/if}
</div>
