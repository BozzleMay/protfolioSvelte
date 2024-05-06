<script>
    import Step from "./Step.svelte";
    let steps = [
        {name: "Muven", href: "https://muven.co.uk/"},
        {name: "Company Directory", img: "http://barrycompanydirectory.co.uk/"},
        {name: "The Pokédex", img: "src/lib/images/pokedex.png"},
    ]
    let benefits = [
        {
            name: "an excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
        {
            name: "a problem solver",
            description:
                "Effective problem-solving is a core strength of mine, driven by a commitment to identify and understand challenges at their root.",
        },
        {
            name: "a keen learner",
            description:
                "I am deeply committed to ongoing learning and progression in my programming career. I am always looking to learn new technologies and improve my skills.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semi-bold text-4xl sm:text-5xl md:text-6xl">Hi! I'm <span class="poppins text-violet-400">Barry</span> 
                May<br />Full Stack <span class="poppins text-violet-400">Developer</span> 
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-violet-400">favourite tech</span> includes Javascript, PHP, Codeigniter, MySQL, Bootstrap, and more!
            </p>
            <button class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src="public/images/images/barry_may_person_shaped.png" alt="Barry May" class="object-cover z-[2] max-h-[70vh]" />
        </div>

    </section>



    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Muven <strong
                        class="text-violet-400"
                        >PHP, Codeigniter4, MySQL, JavaScript, Bootstrap5!</strong
                    > Muven is an estate agency CRM system that allows agents to manage their properties, clients, and appointments.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Company Directory is a Full Stack <strong
                        class="text-violet-400">PHP</strong
                    >,
                    <strong class="text-violet-400">MySQL </strong
                    >
                    & <strong class="text-violet-400">JavaScript!</strong> CRUD application
                    this project was built with PHP and MySQL. It is a company directory that allows you to add, edit, delete employees and departments. It also has a search function that allows you to search for employees by name or department.
                </p>
            </Step>
            <!-- <Step step={steps[2]}>
                <p>
                    The Pokédex is a <strong class="text-violet-400"
                        >SvelteKit & TailwindCSS</strong
                    >
                    web application, hosted on
                    <strong class="text-violet-400">Netlify</strong>, that
                    consumes and caches the
                    <strong class="text-violet-400">Pokémon API</strong>
                    to display all Pokémon information. Gotta catch them all!
                </p>
            </Step> -->
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <!-- <div class="flex flex-col gap-2 mx-auto">
                    <div class="flex items-end gap-4">
                        <p
                            class="poppins text-6xl sm:text-7xl md:text-8xl text-slate-500 font-medium"
                        >
                            {benefit.metric}
                        </p>
                        <p
                            class="text-xl sm:text-2xl md:text-3xl capitalize pb-2"
                        >
                            {benefit.name}
                        </p>
                    </div>
                    <p class="text-center italic">- {benefit.description}</p>
                </div> -->
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
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
        
       
    </section>

</main>