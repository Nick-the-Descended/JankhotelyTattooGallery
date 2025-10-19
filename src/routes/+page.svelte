<script>
    import * as m from "$lib/paraglide/messages";
    import {Mail, Phone, Instagram, MapPin} from "lucide-svelte"
</script>

<section class="hero w-full relative">
    <div class="absolute bottom-8 left-8 z-1 text-2xl text-white">
        <h1 class="font-bold text-6xl leading-16">
            {m.heading_m1()}
        </h1>
        <h1 class="font-bold text-6xl leading-16">
            {m.heading_m2()}
        </h1>
        <h2 class="mt-4 opacity-90 text-4xl ">
            {m.heading_m3()}
            {m.heading_m4()}
        </h2>
    </div>
    <div class="max-h-[90vh] overflow-clip object-cover">
        <img src="/hero.png" class="w-full object-cover object-left max-h-[90vh]" alt="hero banner"/>
    </div>
</section>

<section class="w-full min-h-[65vh] flex flex-col items-center justify-between p-8 gap-4 bg-gray-200">
    <div class="flex gap-2 text-4xl font-bold">
        <h2>{m.subheading_m1()}</h2>
        •
        <h2>{m.subheading_m2()}</h2>
        •
        <h2>{m.subheading_m3()}</h2>
    </div>
    <div class="flex gap-2 text-2xl font-semibold">
        <h2>{m.subheading_m4()}</h2>
        <h2>{m.subheading_m5()}</h2>
    </div>
    <div class="grid grid-cols-2 gap-0 rounded-xl overflow-clip bg-gray-800 max-h-[80svh] aspect-[1272/953]">
        <img src="/banner2.png" class="object-fill">
        <img src="/banner1.png" class="object-fill">
    </div>
</section>

<section>
    <h1 class="text-6xl text-center py-8 mt-8">
        {m.our_work()}
    </h1>
    <div class="collage grid grid-rows-[repeat(3,240px)] overflow-hidden">
        <div class="grid grid-rows-subgrid grid-cols-[repeat(46,minmax(250px,250px))] h-full px-1 py-0.5 gap-1">
            {#each Array(23) as _, i}
                <img src="/coll/{i+1}.webp" alt="banner" class="rounded-sm">
            {/each}
        </div>
        <div class="grid grid-rows-subgrid grid-cols-[repeat(46,minmax(250px,250px))] h-full px-1 py-0.5 gap-1 ml-[-150px]">
            {#each Array(24) as _, i}
                <img src="/coll/{i+25}.webp" alt="banner" class="rounded-sm">
            {/each}
        </div>
        <div class="grid grid-rows-subgrid grid-cols-[repeat(46,minmax(250px,250px))] h-full px-1 py-0.5 gap-1">
            {#each Array(23) as _, i}
                <img src="/coll/{i+48}.webp" alt="banner" class="rounded-sm">
            {/each}
        </div>
    </div>
</section>

<section class="py-20 md:py-32 bg-card">
    <div class="container mx-auto px-4">
        <div class="max-w-4xl mx-auto">
            <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-6 text-center text-balance">
                {m.sec1_intro1()}
            </h2>
            <p class="text-lg md:text-xl text-muted-foreground mb-12 text-center text-pretty">
                {m.sec1_intro2()}
            </p>
            <div class="grid md:grid-cols-2 gap-6">
                {#each [
                    m.sec1_item1(),
                    m.sec1_item2(),
                    m.sec1_item3(),
                    m.sec1_item4(),
                    m.sec1_item5(),
                    m.sec1_item6()
                ] as detail}
                    <div class="flex gap-4 items-start">
                        <span class="text-green-600 text-center font-bold">✓</span>
                        <p class="text-base md:text-lg text-foreground/90">{detail}</p>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</section>

<section class="py-20 md:py-32 bg-background">
    <div class="container mx-auto px-4">
        <div class="grid sm:grid-cols-2 gap-8 max-w-6xl mx-auto">
            {#each [
                [m.sec1_details1_1(), m.sec1_details1_2()],
                [m.sec1_details2_1(), m.sec1_details2_2()],
                [m.sec1_details3_1(), m.sec1_details3_2()],
                [m.sec1_details4_1(), m.sec1_details4_2()],
            ] as detail}
                <div class="bg-card p-8 rounded-lg border border-border hover:border-primary/50 transition-colors">
                    <h3 class="text-sm font-semibold text-muted-foreground mb-3 uppercase tracking-wider">
                        {detail[0]}
                    </h3>
                    <p class="text-lg font-medium text-foreground leading-relaxed">
                        {detail[1]}
                    </p>
                </div>
            {/each}
        </div>
    </div>
</section>

<section class="w-full flex flex-col items-center justify-center gap-4 p-8">
    <div class="flex flex-col md:flex-row gap-4">
        <button class="px-8 py-4 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-colors text-xl font-semibold">{m.sec1_cta1()}</button>
        <button class="px-8 py-4 bg-orange-500 text-white rounded-lg hover:bg-orange-600 transition-colors text-xl font-semibold">{m.sec1_cta2()}</button>
    </div>
</section>

<footer class="bg-card bg-gray-200 border-border">
    <div class="container mx-auto px-4 py-16">
        <div class="max-w-4xl mx-auto">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center">{m.footer_h()}</h2>

            <div class="grid sm:grid-cols-2 max-w-[600px] mx-auto gap-8 mb-12">
                <a class="flex items-center justify-start gap-4" href="tel:+995593315185">
                    <div class="size-8 rounded-full bg-primary/20 flex items-center justify-center flex-shrink-0">
                        <Phone class="size-8 text-primary"/>
                    </div>
                    <div>
                        <h3 class="font-semibold mb-1">{m.footer_1()}</h3>
                        <p class="text-muted-foreground">+995 593 31 51 85</p>
                    </div>
                </a>

                <a class="flex items-center justify-start gap-4" href="mailto:g.jankhotely@gmail.com">
                    <div class="size-8 rounded-full bg-primary/20 flex items-center justify-center flex-shrink-0">
                        <Mail class="size-8 text-primary"/>
                    </div>
                    <div>
                        <h3 class="font-semibold mb-1">{m.footer_2()}</h3>
                        <p class="text-muted-foreground">g.jankhotely@gmail.com</p>
                    </div>
                </a>

                <a class="flex items-center justify-start gap-4" href="https://www.instagram.com/jankhotely/">
                    <div class="size-8 rounded-full bg-primary/20 flex items-center justify-center flex-shrink-0">
                        <Instagram class="size-8 text-primary"/>
                    </div>
                    <div>
                        <h3 class="font-semibold mb-1">{m.footer_3()}</h3>
                        <p class="text-muted-foreground">@jankhotely</p>
                    </div>
                </a>

                <div class="flex items-center justify-start gap-4">
                    <div class="size-8 rounded-full bg-primary/20 flex items-center justify-center flex-shrink-0">
                        <MapPin class="size-8 text-primary"/>
                    </div>
                    <div>
                        <h3 class="font-semibold mb-1">{m.footer_4()}</h3>
                        <p class="text-muted-foreground">{m.address()}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</footer>

<style>
    .hero::before {
        content: "";
        position: absolute;
        inset: 0;
        background-image: linear-gradient(to bottom, transparent 65%, black);
    }

    .collage {
        & > * {
            animation: linear infinite collage-animation 100s;
        }

        /*& > :nth-child(2) {*/
        /*    margin-left: -150px;*/
        /*}*/

        & img {
            @apply h-full w-full object-cover overflow-clip;
        }

        &:has(:hover) {
            & > * {
                animation-play-state: paused;

                & img:hover {
                    z-index: 2;
                    /*transform: scale(2);*/
                }

            }
        }
    }

    @keyframes collage-animation {
        from {
            transform: translateX(0);
        }
        50% {
            transform: translateX(-1900px);
        }
    }
</style>