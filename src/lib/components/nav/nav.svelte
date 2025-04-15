<script lang="ts">
  let links = [
    {
      label: "Home",
      href: "/",
    },
    {
      label: "About",
      href: "/about",
    },
    {
      label: "Our Mission",
      href: "/mission",
    },
  ];
</script>

<nav class="bg-white py-5">
  <div class=" flex justify-between">
    <ul class="flex space-x-6">
      {#each links as link}
        <li>
          <a
            href={link.href}
            class="py-2 px-5 text-sm rounded-full font-semibold bg-gray-100 text-gray-700 hover:text-blue-600"
            >{link.label}</a
          >
        </li>
      {/each}
    </ul>
    <!-- <h1 class="font-bold text-xl">LOGO</h1> -->
    <img alt="logo" src="/images/greenbyte_leaf.svg" class="w-14" />
    <ul class="flex space-x-6">
      {#each links as link}
        <li>
          <a
            href={link.href}
            class="py-2 px-5 text-sm rounded-full font-semibold bg-gray-100 text-gray-700 hover:text-blue-600"
            >{link.label}</a
          >
        </li>
      {/each}
    </ul>
  </div>
</nav>
