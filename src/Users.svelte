<script>
    let users = [];
        $: fetch('https://jsonplaceholder.typicode.com/users')
        .then(response => response.json())
        .then(data => {users = data})
   </script>
   
  
  
  <div class="container">
    <ul>
        {#each users as user }

        <li>{user.name}</li>

        <li>{user.email}</li>
            
        {/each}
    </ul>
  </div>
  