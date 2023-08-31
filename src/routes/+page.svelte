<script>
// @ts-nocheck




	const pages = ['home', 'projects', 'songs', 'contact']

    const liked_songs = [
    {
        title: 'Icee pop',
        id: '1zKOagmkCtXuGmCivG8HZE',
        artist: 'Nic D',
        genre: 'singer-songwriter pop'
    },
    {
        title: 'Right Now',
        id: '2PneyQbePKwFGOtI86xckP',
        artist: 'Confetii',
        genre: 'LA Pop'
    },
    {
        title: 'Love your voice',
        id: '4hyVrAsoKKjxAvQjPRt0ai',
        artist: 'JONY',
        genre: 'Russian pop, Russian dance'
    }
    ];

  
    
    const icon = [
    'https://media.discordapp.net/attachments/1058462242359738439/1146861120984989716/NXNEW.png?width=150&height=150'];

    const projects = [{
        title: 'Coming Soon',
        icon: icon[0],
        description: 'More coming soon'
    },
    {
        title: 'Coming Soon',
        icon: icon[0],
        description: 'More coming soon'
    },
    {
        title: 'Coming Soon',
        icon: icon[0],
        description: 'More coming soon'
    }
    ];

    
    const smedia = [
    'https://media.discordapp.net/attachments/1141520661949464629/1146298033546469396/25231.png?width=150&height=150'
        ,
    'https://media.discordapp.net/attachments/1141520661949464629/1146298033743597659/pngtree-instagram-icon-instagram-logo-png-image_3584853.png?width=150&height=150'
        ,
    'https://media.discordapp.net/attachments/1141520661949464629/1146298033970085908/1690643591twitter-x-logo-png.png?width=150&height=150'
        ,
    'https://media.discordapp.net/attachments/1141520661949464629/1146298034225946624/174857.png?width=150&height=150'];

    const contacts = [{
        title: 'Github',
        handle: '@nex4s',
        icon: smedia[0],
        link: 'https://github.com/nex4s'
    },
    {
        title: 'Instagram',
        handle: '@nex4s',
        icon: smedia[1],
        link: 'https://instagram.com/@nex4s_'
    },
    {
        title: 'LinkedIn',
        handle: '@jmn3x',
        icon: smedia[3],
        link: 'https://www.linkedin.com/in/jmn3x/'
    }];

    function scrollToSection(sectionId) {
    const section = document.getElementById(sectionId);
    section.scrollIntoView({ behavior: 'smooth' });
  }


  //OctoKit.js 
  (async() => {

  /*
const octokit = new Octokit({ auth: `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` });
const response = await octokit.repos.listForAuthenticatedUser();
console.log(response.data);
*/

})

</script>

<html class="h-full bg-black" lang="en">
    <div>
        <nav class="flex justify-center relative h-60 bg-transparent">
          <ul class="mt-5">
            {#each pages as page}
            <li class="inline-block mr-10 text-white">
                <button class="h-15 bg-transparent border-none text-white text-lg font-sans font-semibold transition-all delay-500 duration-500 hover:text-red" on:click={() => scrollToSection(`${page}-section`)}>{page}</button>

            </li>
            {/each}
          </ul>
        </nav>
      
        <div id="home-section" class="max-h-full overflow-y-auto -mt-40 text-center">
          <div class="mt-3">
            <h1 class="text-6xl text-white font-semibold">
              I'm <span class="text-red-500">Nexus</span>
            </h1>
            <h2 class="mt-2 text-2xl text-white font-semibold">And I do code</h2>
          </div>
          <img class="rounded-2xl mt-4 mx-auto h-43 bg-transparent" src="https://media.discordapp.net/attachments/1058462242359738439/1146861121253417120/old_nexus.png?width=300&height=300" alt="">
          <p class="mt-3 text-white">Hey, I'm Nexus, a coffee-loving coder specializing in HTML, CSS, JavaScript, and now Svelte.</p>
        </div>
      
        <section class="text-34 text-center text-white font-semibold mt-10" id="projects-section">
            <h3 class="section-heading text-white text-3xl ">Projects</h3>

            <div class="flex justify-center">
              <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 mx-auto mt-5">
                {#each projects as project}
                <div class="backdrop-blur-sm rounded-xl relative bg-opacity-70 bg-gray-900 p-6 w-80 mb-20 song">
                  <img src={project.icon} alt="thumbnail" class="h-95 mx-auto rounded-3xl">
                  <div class="flex flex-col">
                    <h4 class="text-red-500 text-center font-semibold text-18 mb-4 song-title">{project.title}</h4>
                    <p class="text-red text-center font-semibold text-250x song-description">{project.description}</p>
                  </div>
                </div>
                {/each}
              </div>
            </div>
          </section>
          
          
          
      
        <!-- Song section -->
      
        <section class="text-34 text-center font-semibold" id="songs-section">
            <h3 class="section-heading text-white text-3xl ">Favorite Songs</h3>
            <div class="overflow-hidden">
              <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 mt-5">
            <!--
                grid-cols-1 specifies that there should be 1 column by default.
                md:grid-cols-2 specifies that there should be 2 columns on medium-sized screens and above.
                lg:grid-cols-3 specifies that there should be 3 columns on large-sized screens and above.
                gap-4 adds a gap of 1rem between each grid item.
             -->
                {#each liked_songs as song}
                <iframe title="{song.title}" style="border-radius:12px" src="https://open.spotify.com/embed/track/{song.id}?utm_source=generator&theme=1" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                {/each}
              </div>
            </div>
          </section>
          
 <!-- Contact section -->
 <section class="text-34 text-center text-white font-semibold mt-10" id="contact-section">
    <h3 class="section-heading text-white text-3xl ">Contact Me</h3>

    <div class="flex justify-center flex-wrap gap-2 mx-auto mt-5">
        {#each contacts as contact}
        <div class="backdrop-blur-sm rounded-xl relative bg-opacity-70 bg-gray-900 p-6 w-80 mb-20 song">
            <img src={contact.icon} alt="thumbnail" class="h-10 mr-4 rounded-3xl">
            <div class="flex flex-col">
                <div class="text-center">
                    <h4 class="text-white font-semibold text-lg song-title -mt-8">
                        <a href="{contact.link}">{contact.handle}</a>
                    </h4>
                </div>
            </div>
        </div>
        {/each}
    </div>
</section>

      
</html>

