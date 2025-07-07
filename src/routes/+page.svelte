
<script>
  import ProjectCard from '../lib/ProjectCard.svelte';
  const projects = [
    {
      title: 'Alien Invasion Game',
      description: 'Python/PyGame arcade shooter built with OOP.',
      link: 'https://github.com/danjwilko/python-projects',
      video: '/Alien_invasion_demo_vid.mp4'
    },
    {
      title: 'BEEYOND FITNESS Website',
      description: 'The newly rebuilt BEEYOND FITNESS website, developed from scratch using SvelteKit and Tailwind CSS. Redesigned for modern styling, accessibility, and mobile responsiveness.',
      link: 'https://beeyondfitness.co.uk',
      image: '/BEEYOND-FITNESS-Site.png'
    },
    {
      title: 'TryHackMe: Junior Penetration Tester Pathway',
      description: 'Hands-on learning in offensive security, covering web, networking, enumeration, and exploitation. Progressing toward JPT1 and Security+ certification.',
      link: 'https://tryhackme.com/p/Danjwilko',
      iframe: "https://tryhackme.com/api/v2/badges/public-profile?userPublicId=1336195"
    },
    {
      title: 'BEEYOND FITNESS Legacy Website',
      description: 'The original version of the BEEYOND FITNESS website before its full redesign. Included basic styling and limited responsiveness, later replaced with a modern responsive build using Svelte and Tailwind.',
      link: 'https://cranky-cray-bb389b.netlify.app',
      image: '/OLD-BEEYOND-FITNESS-Site.png'
    }
  ];
</script>

<div class="min-h-screen bg-gray-900 text-gray-100 font-inter">
  <header class="text-center py-10 border-b border-gray-700">
    <h1 class="text-3xl font-bold text-blue-400">Daniel Wilkinson</h1>
    <p class="text-sm text-gray-400">Development & Cyber Security | OU Final-Year Student</p>
  </header>

  <main class="max-w-4xl mx-auto px-4 py-12">
    <section class="mb-16">
      <h2 class="text-2xl font-semibold border-b border-blue-500 pb-2 mb-4">About Me</h2>
      <p>
        Final-year OU Computing & IT student focusing on development and cyber security.
        Currently working through the TryHackMe JPT pathway and preparing for Security+ alongside degree studies and personal projects.
      </p>
    </section>

    <section class="mb-16">
      <h2 class="text-2xl font-semibold border-b border-blue-500 pb-2 mb-4">Projects</h2>
      <div class="grid md:grid-cols-2 gap-6">
        {#each projects as proj}
          <ProjectCard {...proj} />
        {/each}
      </div>
    </section>

    <section>
      <h2 class="text-2xl font-semibold border-b border-blue-500 pb-2 mb-4">Contact</h2>
      <p>
        Feel free to reach out for collaboration, questions, or just to connect!<br>
        GitHub: <a href="https://github.com/danjwilko" target="_blank" class="text-blue-400 hover:underline">danjwilko</a><br>
        LinkedIn: <a href="https://www.linkedin.com/in/daniel-j-wilkinson" target="_blank" class="text-blue-400 hover:underline">daniel-j-wilkinson</a>
      </p>
    </section>
  </main>

  <footer class="text-center text-xs text-gray-600 py-10 border-t border-gray-700">
    &copy; 2025 Daniel Wilkinson | Built with SvelteKit & TailwindCSS
  </footer>
</div>
