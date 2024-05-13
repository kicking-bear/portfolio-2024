<script>
    export let y;

    let tabs = [
        {name: "Projects", link: "#projects"},
        {name: "About Me", link:  "#about"},
        {name: "Blog", link: "#blog"},
        ];

        function scrollToElement(selector) {
        const element = document.querySelector(selector);
        if (element) {
            element.scrollIntoView({ behavior: 'smooth' });
        }
    }

    

</script>

<header class={"sticky z-[10] top-0 duration-200 px-6 py-2 flex items-center justify-between border-b border-transparent" + (y > 0 ? 'py-4 bg-slate-50 border-slate-200' : 'py-6 bg-slate-50/50 border-transparent')}>
    <h1 class="font-medium">
        <b class="font-bold Rubik">Daniel</b> Manning

    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-violet-400">
                <p>{tabs.name}</p>
            </a>
        {/each}
    </div>
    <a 
        on:click={() => scrollToElement('#contact-form')}
        class="blueShadow relative overflow-hidden px-5 py-2 group rounded-lg bg-white text-slate-950 cursor-pointer">
        <div class="absolute top-0 right-full w-full h-full bg-slate-400  opacity-20 group-hover:translate-x-full z-0 duration-200">
        </div>
        <h4 class="relative z-9">Get in touch</h4>
    </a>
</header>