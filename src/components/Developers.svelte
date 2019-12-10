<script>
import Developer from './Developer.svelte'
  let developers = [
    { name: "Mikaela", skills: [
        {text: 'JS', id: 0 },
        {text: 'VUE', id: 1 },
        {text: 'SCSS', id: 2 }
    ] },
    { name: "Ellinor", skills: [
        {text: 'JS', id: 0 },
        {text: 'VUE', id: 1 },
        {text: 'SCSS', id: 2 }
    ] },
    { name: "Anna", skills: [
        {text: 'JS', id: 0 },
        {text: 'VUE', id: 1 },
        {text: 'SCSS', id: 2 }
    ] },
  ];
</script>

<style>
</style>

{#each developers as developer}
<Developer 
name={developer.name}
skills={developer.skills}
/>
{/each}
