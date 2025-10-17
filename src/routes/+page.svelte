<script>
    import * as m from "$lib/paraglide/messages";
</script>

<section class="hero w-full relative">
    <h1 class="absolute bottom-4 left-4 z-1 font-bold text-5xl text-white">
        {m.heading_m1()}
        <br/>
        {m.heading_m2()}
    </h1>
    <div class="max-h-[90vh] overflow-clip object-cover">
        <img src="/hero.png" class="w-full object-cover object-left max-h-[90vh]" alt="hero banner"/>
    </div>
</section>

<section class="w-full min-h-[65vh] flex flex-col items-center justify-between p-8 gap-4">
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
    <div class="flex rounded-xl overflow-clip">
        <img src="/banner2.png">
        <img src="/banner1.png">
    </div>
</section>

<section class="w-full flex flex-col items-center justify-center p-8 gap-6 bg-white">
    <div class="max-w-3xl text-center">
        <h3 class="text-2xl font-bold mb-2">{m.sec1_intro1()}</h3>
        <p class="text-xl text-gray-700 mb-4">{m.sec1_intro2()}</p>
    </div>
    <ul class="max-w-2xl space-y-3 text-lg">
        {#each [
            m.sec1_item1(),
            m.sec1_item2(),
            m.sec1_item3(),
            m.sec1_item4(),
            m.sec1_item5(),
            m.sec1_item6()
        ] as detail}
            <li class="flex items-center gap-2">✓ {detail}</li>
        {/each}
    </ul>
</section>

<section class="w-full flex items-start justify-center p-8 gap-4 bg-gray-100">
    <ul class="grid md:grid-cols-2 gap-4 text-lg">
        {#each [
            m.sec1_details1(),
            m.sec1_details2(),
            m.sec1_details3(),
            m.sec1_details4()
        ] as detail}
            <li class="flex items-center gap-2">{detail}</li>
        {/each}
    </ul>
</section>

<section class="w-full flex flex-col items-center justify-center gap-4 p-8">
    <div class="flex flex-col md:flex-row gap-4">
        <button class="px-8 py-4 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-colors text-xl font-semibold">{m.sec1_cta1()}</button>
        <button class="px-8 py-4 bg-orange-500 text-white rounded-lg hover:bg-orange-600 transition-colors text-xl font-semibold">{m.sec1_cta2()}</button>
    </div>
    <p class="text-gray-700 text-lg mt-8">{m.address()}</p>
</section>


<style>
    .hero::before {
        content: "";
        position: absolute;
        inset: 0;
        background-image: linear-gradient(to bottom, transparent 80%, black);
    }
</style>