<script>
  import { Navbar } from "$lib";
  import About from "$lib/components/mission/mission.svelte";
  import Hero from "$lib/components/hero/hero.svelte";
  import Mission from "$lib/components/mission/mission.svelte";
</script>

<main class="min-w-2xl">
  <!-- <Navbar /> -->
  <div class="text-center w-[1000px] mx-auto space-y-5 py-20">
    <h1 class="text-5xl font-black my-5 text-center text-gray-800">
      Find a Solution with <br /> a Free Quote
    </h1>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolores,
      architecto, laborum distinctio placeat quae voluptatum accusamus officia
      odit veniam impedit libero, quasi iusto? Maxime soluta nulla, blanditiis
      numquam libero reiciendis.
    </p>
    <button
      class="cursor-pointer py-2 px-5 text-md rounded-full bg-gray-100 text-gray-700 hover:text-blue-600 font-semibold"
    >
      Get a quote
    </button>
  </div>
  <Hero />
  <Mission />
</main>
