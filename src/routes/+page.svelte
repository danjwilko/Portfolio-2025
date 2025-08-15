
<script>
  import ProjectCard from '../lib/ProjectCard.svelte';
  const projects = [
  
  {
    title: 'Learning Log Web Application',
    description: 'A Django web application for tracking learning topics and progress, adapted from Python Crash Course. Features user authentication, topic and entry creation, and a clean Bootstrap-based UI. Updated and deployed to PythonAnywhere after resolving deprecated instructions from the original tutorial.',
    tech: ["Python", "Django", "HTML", "Bootstrap", "Git", "PythonAnywhere deployment"],
    link: 'https://danjwilko.pythonanywhere.com',
    image: '/Learning-Log.png',
    button_link:'https://github.com/danjwilko/learning_log'
  },
  {
    title: 'BEEYOND FITNESS Website',
    description: 'Rebuilt the BEEYOND FITNESS business site from scratch using SvelteKit and Tailwind CSS. Designed for modern styling, accessibility, mobile responsiveness, and improved SEO performance.',
    tech: ["SvelteKit", "Tailwind CSS", "HTML", "Git", "Netlify deployment"],
    link: 'https://beeyondfitness.co.uk',
    image: '/BEEYOND-FITNESS-Site.png',
    button_link: 'https://github.com/danjwilko/Beeyond-fitness-2025'
  },
  {
    title: 'TryHackMe: Junior Penetration Tester Pathway',
    description: 'Hands-on cybersecurity learning covering web exploitation, network analysis, enumeration, privilege escalation, and vulnerability assessment. Progressing toward JPT1 and Security+ certification.',
    link: 'https://tryhackme.com/p/Danjwilko',
    image: '/Tryhackmebanner.png',
  },
  
  {
    title: 'Alien Invasion',
    intro: 'Arcade-style space shooter built with Pygame. Developed following a guided project in Python Crash Course and expanded with gameplay tweaks. Implemented OOP principles, collision detection, alien fleet generation, and score tracking. Demonstrates understanding of game loops, event handling, and sprite management.',
    tech: ["Python", "Pygame", "OOP", "Git"],
    link: 'https://github.com/danjwilko/python-projects',
    video: '/Alien_invasion_demo_vid.mp4',
    button_link:'https://github.com/danjwilko/python-projects'
  },
  {
    title: 'BEEYOND FITNESS Legacy Website',
    description: 'The original BEEYOND FITNESS site, built with basic HTML/CSS and minimal responsiveness. Served as the foundation for a complete redesign using SvelteKit and Tailwind CSS.',
    link: 'https://cranky-cray-bb389b.netlify.app',
    image: '/OLD-BEEYOND-FITNESS-Site.png',
    button_link: 'https://github.com/danjwilko/BEEYOND-FITNESS-PROJECT'
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
