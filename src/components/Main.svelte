<script>
    import Step from './Step.svelte';

    let steps = [
        {name:'Fonsecar', icon:'fa-solid fa-car', href:'https://github.com/FbrFonseca/Next-js-fonsecar'},
        {name:'Bank app', icon:'fa-solid fa-university', href:'https://github.com/FbrFonseca'},
        {name:'School app', icon:'fa-solid fa-graduation-cap', href:'https://github.com/FbrFonseca'},
    ];

    let benefits = [
        {name: 'a computer science student', 
        description: 'in the 3rd year of my degree, a tech enthisiast and have been amazed by what technology can lead us since the first time my brother let me play with his super nintendo.'},
        {name: 'a full stack developer', 
        description: 'to be 😅. I know, it sounds a bit too much to say it right now, but i am working my way become one. I am experimenting and testing as much as i can with a veriety of techs including C#, JavaScript, PHP, Python, WordPress and others.'},
        {name: 'an excellent communicator', 
        description: 'As an international student, I not only learn to get along with people from different backgrounds but also to explore it. I enjoy traveling, hiking, meeting new people, and I am always up for a good laugh 🍻.'},
    ];

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
        
            <h2 class="font-semibold text-4xl sm:text-5xl md:6xl">
                Hi! I'm <span class="poppins text-violet-400">Fabricio</span>
                Fonseca <br>Full Stack <span class="poppins text-violet-400">Developer</span>
            </h2>

            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favourite tech</span> includes JavaScript, React.js Next.js Node.js, Svelte!
            </p>

            <a 
                href="https://www.linkedin.com/in/fpfonseca"
                target="_blank"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
            >
                <div 
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />

                <h4 class="relative z-9">Get in touch &rarr;</h4>

            </a>
        </div>

        <div class="relative grid place-items-center">
            <img src={"images/profile.png"} alt="Profile image" class="object-cover z-[2] max-h-[100vh] blueShadow"/>
        </div>

    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        
        <div class="flex flex-col gap-2 text-center">

            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavours.
            </h6>

            <h3 
                class="font-semibold text-3xl sm:text-4xl md:text-5xl"
            >Curious to <span class="poppins text-violet-400">see</span>
             my work?
            </h3>
        
        </div>

        <!-- <a 
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid
                border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10
                hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a> -->
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            
            <Step step={steps[0]}>
                <p>Car rent web app built using 
                <strong class="text-violet-400">React.js, Next.js, Node.js & Tailwind.css!</strong>
                The aim of this project was to practice my skills creating in a resposive web
                page, exploring the new possibilites of Next.js 13.
                </p>
            </Step>
                
            <Step step={steps[1]}>
                <p>Coded in <strong class="text-violet-400">C# and WPF in the .Net framework</strong> as part
                    of a class project. This app include the fundamental functions
                    needed to operate bank, including cryptografy and record of
                    users, administrators and transactions history in a MSSQL
                    database.
                </p>
            </Step>

            <Step step={steps[2]}>
                <p>In this class project, I coded a
                    college management application that can be used to administer
                    staff, students, classes and grades.<strong class="text-violet-400"> C# and Windows Forms
                    in the .NET framework & MSSQL</strong> database were used in this
                    assignment.                
                </p>
            </Step>
       
        </div>

    </section>

    <section dir="about" id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col
    gap-16 sm:gap-20 md:gap-24 relative">
        
        <div class="flex flex-col gap-2 text-center relative before:absolute 
        before:top-0 before:left-0 before:w-2/3 before:h-1.5
        before:bg-violet-700 after:absolute 
        after:bottom-0 after:right-0 after:w-2/3 after:h-1.5
        after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about </span>me.
            </h3>
        </div>
        
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
           
            {#each benefits as benefit, index}

                <div class="flex gap-6 sm:gap-8">

                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index+1}
                    </p>

                    <div class="flex flex-col gap-6 sm:gap-8">

                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>

                        <p>{benefit.description}</p>

                    </div>

                </div>
           
            {/each}
       
        </div>

        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-500 poppins">Complete</span> Package</h5>

        <div class="flex flex-col gap-10 max-w-[800] text-base font-bold p-4 rounded mx-auto w-full bg-white">
            <div class="">
              <div class="skill-name text-slate-950">HTML</div>
              <div class="skill-bar bg-slate-700">
                <div class="skill-per bg-violet-400" style="max-width:90%"></div>
              </div>
            </div>
          
            <div class="">
              <div class="skill-name text-slate-950">CSS</div>
              <div class="skill-bar bg-slate-700">
                <div class="skill-per bg-violet-400" style="max-width:75%"></div>
              </div>
            </div>
          
            <div class="">
              <div class="skill-name text-slate-950">Javascript</div>
              <div class="skill-bar bg-slate-700">
                <div class="skill-per bg-violet-400" style="max-width:95%"></div>
              </div>
            </div>
            
            <div class="">
                <div class="skill-name text-slate-950">Node.js</div>
                <div class="skill-bar bg-slate-700">
                  <div class="skill-per bg-violet-400" style="max-width:80%"></div>
                </div>
            </div>

            <div class="">
                <div class="skill-name text-slate-950">React.js</div>
                <div class="skill-bar bg-slate-700">
                    <div class="skill-per bg-violet-400" style="max-width:85%"></div>
                </div>
            </div>

            <div class="">
                <div class="skill-name text-slate-950">C#</div>
                <div class="skill-bar bg-slate-700">
                    <div class="skill-per bg-violet-400" style="max-width:97%"></div>
                </div>
            </div>

            <div class="">
                <div class="skill-name text-slate-950">SQL</div>
                <div class="skill-bar bg-slate-700">
                    <div class="skill-per bg-violet-400" style="max-width:85%"></div>
                </div>
            </div>
    
            <div class="pb-4">
                <div class="skill-name text-slate-950">Git</div>
                <div class="skill-bar bg-slate-700">
                    <div class="skill-per bg-violet-400" style="max-width:75%"></div>
                </div>
            </div>
          
        </div>
          

        <!-- <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div> -->
        <p class="mx-auto text-2xl">So why not invest?</p> 

    </section>

</main>