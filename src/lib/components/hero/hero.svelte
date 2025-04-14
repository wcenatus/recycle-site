<script lang="ts">
  let selectedForm: "neutral" | "commercial" | "residential" = "neutral";
</script>

<!-- {selectedForm} -->
<div class="flex h-[70vh] space-x-2 transition-all duration-500 ease-in-out">
  <!-- Commercial Section -->
  <div
    class={`transition-all duration-500 ease-in-out rounded-xl flex items-center justify-center bg-yellow-200
        ${
          selectedForm === "commercial"
            ? "w-[90%]" // ~10/12
            : selectedForm === "neutral"
              ? "w-1/2"
              : "w-[10%]" // ~2/12
        }`}
  >
    <div class="text-center">
      <h1 class="text-5xl">Commercial</h1>
      <button
        on:click={() => (selectedForm = "commercial")}
        class="mt-4 cursor-pointer py-2 px-5 text-sm rounded-full bg-gray-100 text-gray-700 hover:text-blue-600 font-medium"
      >
        Commercial
      </button>
    </div>
  </div>

  <!-- Residential Section -->
  <div
    class={`transition-all duration-500 ease-in-out rounded-xl flex items-center justify-center bg-gray-50
        ${
          selectedForm === "residential"
            ? "w-[90%]"
            : selectedForm === "neutral"
              ? "w-1/2"
              : "w-[10%]"
        }`}
  >
    <div class="text-center">
      <h1 class="text-5xl">Residential</h1>
      <button
        on:click={() => (selectedForm = "residential")}
        class="mt-4 cursor-pointer py-2 px-5 text-sm rounded-full bg-gray-100 text-gray-700 hover:text-blue-600 font-medium"
      >
        Residential
      </button>
    </div>
  </div>
</div>
