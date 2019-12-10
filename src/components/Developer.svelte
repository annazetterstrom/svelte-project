<script>
export let name;
export let skills; 

  let newSkillText = '';

  const addSkill = () => {
      let newSkill = {text: newSkillText, id: skills.length}
      newSkillText = '';
      if (!newSkill) return;
      skills = [...skills, newSkill];
  }
</script>

<style>
/* $pink: #D96C9F;
$lgtpink: #F2AECE;
$purple: #582C59;
$darkpurple: #230F26;
$pinkapricot: #F2BBBB; */

  .card {
    padding: 1rem;
    border: #D96C9F 1px solid;
    margin: 0.7rem 0;
    background: linear-gradient(to bottom, #582c59 0%, #230f26 100%);
    width: 80%;
    margin: 2% auto 2% auto;
  }

.btn {
  display: inline-block;
  background: linear-gradient(to bottom, #f2bbbb 0%, #f2aece 100%);
  color: #230F26;
  padding: 0.4rem 1.3rem;
  font-size: 1rem;
  border: none;
  cursor: pointer;
  margin-right: 0.5rem;
  transition: opacity 0.2s ease-in;
  outline: none;
  text-transform: uppercase;
  font-weight: 500;
}

h1 {
    color: #F2AECE;
}

h2 {
    color: #F2BBBB; 
}

ul {
    margin: 0% 0% 2% 0%;
    padding: 0% 0% 2% 0%;
    color: #F2BBBB;
    list-style: none;
}

li {
    display: inline;
    padding: 1% 2% 1% 0%;
  text-transform: uppercase;
    
}


</style>

 <div class="card">
    <h1>
      Developer: {name}
    </h1>
    <h2>My skills:</h2>
    <ul>
      {#each skills as skill (skill.id)}
        <li>{skill.text}</li>
      {/each}
    </ul>
    <form>
    <input type="text" placeholder="Add skill" bind:value={newSkillText} />
    <button class="btn" type="submit" on:click|preventDefault={() => addSkill()}>Add skill</button>
    </form>
    <!-- <button class="btn btn-sm" on:click={addSkill}>Add skill</button> -->
  </div>