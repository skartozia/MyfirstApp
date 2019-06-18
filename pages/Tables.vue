<template>
  <div class="container-fluid pt-1">
    <nuxt-link to="/">
      <button class="btn btn-primary">Home</button>
    </nuxt-link>
    <nuxt-link to="/datepicker">
      <button class="btn btn-primary">datepicker</button>
    </nuxt-link>
    <table class="table table-striped table-bordered my-3">
      <thead style="background-color: #f0f0f0">
        <tr>
          <th scope="col">Fullname</th>
          <th scope="col">Personal Number</th>
          <th scope="col">Gender</th>
          <th scope="col">BirthDate</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{user.name + ", " + user.email }}</td>
          <td>{{user.username}}</td>
          <td>{{user.email}}</td>
          <td>{{user.address.street}}</td>
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
      "https://jsonplaceholder.typicode.com/users?_limit=8"
    );
    const users = await response.json();
    console.log(users);
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
