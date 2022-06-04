<script lang="ts">
  import Tailwind from './Tailwind.svelte';
  export let name: string;
</script>

<Tailwind />

<main>
  <h1 class="bg-pink-500 text-gray-100 font-bold text-xl rounded-lg px-5">
    Hello {name} from the <span class="text-7xl">Svelte</span> Tailwind Nx template!
  </h1>
  <div>
    <span class="mt-4 text-red-500 text-5xl font-bold">Example goes here</span>
  </div>
</main>

