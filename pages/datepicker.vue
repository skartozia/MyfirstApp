<template>
  <div class="container-fluid pt-1">
    <nuxt-link to="/">
      <button class="btn btn-primary">Home</button>
    </nuxt-link>
    <nuxt-link to="/Tables">
      <button class="btn btn-primary">tables</button>
    </nuxt-link>

    <h1>datepicker</h1>
    <main class="container">
    <div class="row" style="padding-top: 100px">
        <div class="col">
            <input data-date-format="dd/mm/yyyy" id="datepicker">
        </div>
    </div>
</main>

 <!-- <script type="text/javascript">
    $('#datepicker').datepicker({
        weekStart: 1,
        daysOfWeekHighlighted: "6,0",
        autoclose: true,
        todayHighlight: true,
    });
    $('#datepicker').datepicker("setDate", new Date());
</script> -->

  </div>
  
</template>

<script>

export default {

};
</script>

<style>
</style>
