<template>
  <div class="container-fluid">
    <h1>Add new</h1>
    <nuxt-link to="/">
      <h2>Home</h2>
    </nuxt-link>
    <nuxt-link to="/euf">
      <h2>js learn</h2>
    </nuxt-link>

    <table class="table table-striped table-bordered my-3">
      <thead style="background-color: #f0f0f0">
        <tr>
          <th scope="col">Fullname</th>
          <th scope="col">Personal Number</th>
          <th scope="col">Gender</th>
          <th scope="col">BirthDate</th>
          <th scope="col">Date of Expiry</th>
          <th scope="col">Actions</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row"></th>
          <td>nika</td>
          <td>Otto</td>
          <td>@mdo</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row"></th>
          <td>Jacob</td>
          <td>Thornton</td>
          <td>@fat</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <td scope="row"></td>
          <td>Larry</td>
          <td>the Bird</td>
          <td>@twitter</td>
          <td>Otto</td>
          <td>@mdo</td>
        </tr>
        <tr>
          <th scope="row"></th>
          <td>Larry</td>
          <td>the Bird</td>
          <td>@twitter</td>
          <td>@twitter</td>
          <td>
            <button type="button" class="btn btn-outline-secondary">Edit</button>
            <button type="button" class="btn btn-outline-secondary">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>

    <ul>
      <li v-for="user in users" :key="user.id">{{user}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData() {
    const response = await fetch(
      "https://jsonplaceholder.typicode.com/users?_limit=5"
    );
    const users = await response.json();
    return { users };
  },
  data: () => ({
    users: []
  }),
  async mounted() {}
};
</script>


<style scoped>
</style>
