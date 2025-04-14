<script lang="ts">
  let selectedForm: "neutral" | "commercial" | "residential" = "neutral";

  let commercialInfo = {
    name: "",
    address: "",
    materials: "",
  };

  let residentialInfo = {
    name: "",
    address: "",
    materials: "",
  };

  const resetForm = () => {
    selectedForm = "neutral";
  };
</script>

<div
  class="flex h-[80vh] space-x-2 transition-all duration-500 ease-in-out relative"
>
  <!-- Commercial Section -->
  <div
    class={`transition-all duration-500 ease-in-out rounded-xl flex flex-col items-center justify-center bg-yellow-200 p-6 overflow-hidden relative
      ${
        selectedForm === "commercial"
          ? "w-[83.3333%]"
          : selectedForm === "neutral"
            ? "w-1/2"
            : "w-[16.6667%]"
      }`}
  >
    {#if selectedForm === "commercial"}
      <button
        on:click={resetForm}
        class="absolute top-4 right-4 text-gray-600 hover:text-red-500 text-xl font-bold"
        aria-label="Close commercial form"
      >
        &times;
      </button>
    {/if}

    <h1 class="text-5xl mb-4 text-center">Commercial</h1>
    <button
      on:click={() => (selectedForm = "commercial")}
      class="cursor-pointer py-2 px-5 text-sm rounded-full bg-gray-100 text-gray-700 hover:text-blue-600 font-semibold"
    >
      Select Commercial
    </button>

    {#if selectedForm === "commercial"}
      <form
        class="mt-6 space-y-4 w-full max-w-md transition-opacity duration-500 opacity-100"
      >
        <input
          type="text"
          placeholder="Business Name"
          bind:value={commercialInfo.name}
          class="w-full px-4 py-2 rounded border border-gray-300"
        />
        <input
          type="text"
          placeholder="Address"
          bind:value={commercialInfo.address}
          class="w-full px-4 py-2 rounded border border-gray-300"
        />
        <input
          type="text"
          placeholder="Recyclable Materials"
          bind:value={commercialInfo.materials}
          class="w-full px-4 py-2 rounded border border-gray-300"
        />
        <button
          type="submit"
          class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700"
        >
          Submit Commercial Request
        </button>
      </form>
    {/if}
  </div>

  <!-- Residential Section -->
  <div
    class={`transition-all duration-500 ease-in-out rounded-xl flex flex-col items-center justify-center bg-gray-50 p-6 overflow-hidden relative
      ${
        selectedForm === "residential"
          ? "w-[83.3333%]"
          : selectedForm === "neutral"
            ? "w-1/2"
            : "w-[16.6667%]"
      }`}
  >
    {#if selectedForm === "residential"}
      <button
        on:click={resetForm}
        class="absolute top-4 right-4 text-gray-600 hover:text-red-500 text-xl font-bold"
        aria-label="Close residential form"
      >
        &times;
      </button>
    {/if}

    <h1 class="text-5xl mb-4 text-center">Residential</h1>
    <button
      on:click={() => (selectedForm = "residential")}
      class="cursor-pointer py-2 px-5 text-sm rounded-full bg-gray-100 text-gray-700 hover:text-blue-600 font-semibold"
    >
      Select Residential
    </button>

    {#if selectedForm === "residential"}
      <form
        class="mt-6 space-y-4 w-full max-w-md transition-opacity duration-500 opacity-100"
      >
        <input
          type="text"
          placeholder="Full Name"
          bind:value={residentialInfo.name}
          class="w-full px-4 py-2 rounded border border-gray-300"
        />
        <input
          type="text"
          placeholder="Address"
          bind:value={residentialInfo.address}
          class="w-full px-4 py-2 rounded border border-gray-300"
        />
        <input
          type="text"
          placeholder="Recyclable Materials"
          bind:value={residentialInfo.materials}
          class="w-full px-4 py-2 rounded border border-gray-300"
        />
        <button
          type="submit"
          class="bg-blue-600 text-white py-2 px-6 rounded hover:bg-blue-700"
        >
          Submit Residential Request
        </button>
      </form>
    {/if}
  </div>
</div>
