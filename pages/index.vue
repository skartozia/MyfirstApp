<template>
  <div class="container-fluid pt-1">
    <nuxt-link to="/">
      <button class="btn btn-primary">Home</button>
    </nuxt-link>
    <nuxt-link to="/Tables">
      <button class="btn btn-primary">tables</button>
    </nuxt-link>
    <nuxt-link to="/datepicker">
      <button class="btn btn-primary">datepicker</button>
    </nuxt-link>


    <div class="AddNew">
      <form>
        <fieldset>
          <legend>Add New / Edit</legend>
          <div class="AddNewAll">
            <input type="text" placeholder="სახელი">
            <input type="text" placeholder="გვარი">
            <select name="city" id="city">
              <option selected value disabled>მოქალაქეობა</option>
              <option value="tbilisi">საქართველო</option>
              <option value="nokalakevi">კანადა</option>
            </select>
            <br>
            <select name="city" id="city">
              <option selected value disabled>სქესი</option>
              <option value="tbilisi">მამრობითი</option>
              <option value="nokalakevi">მდედრობითი</option>
            </select>
            <input type="text" placeholder="პირადი ნომერი">
            <div class="calimg">
              <input type="text" placeholder="დაბადების თარიღი">
              <img src="calendar.svg" alt="calendar">
            </div>
            <div class="calimg">
              <input type="text" placeholder="გაცემის თარიღი">
              <img src="calendar.svg" alt="calendar">
            </div>
            <div class="calimg">
              <input type="text" placeholder="მოქმედების ვადა">
              <img src="calendar.svg" alt="calendar">
            </div>
            <select name="city" id="city" placeholder="დაბადების ადგილი">
              <option selected value disabled>დაბადების ადგილი</option>
              <option value="tbilisi">თბილისი</option>
              <option value="nokalakevi">ნოქალაქევი</option>
              <option value="goresha">ღორეშა</option>
              <option value="sxva">სხვას</option>
            </select>
            <input type="text" placeholder="ბარათის No">
            <br>
            <div class="d-flex justify-content-end">
              <button class="btn btn-secondary">Create/Edit</button>
            </div>
          </div>
        </fieldset>
      </form>
    
    <Buttons />
    </div>
  </div>
</template>


<script>


import Buttons from "~/components/form/Button/Buttons";

export default {
  async addNew() {}
};
</script>

<style scoped>
.btn_btn {
  margin: 10px;
  background-color: #fff;
  border: 1px solid black;
  border-radius: 5px;
  outline: none;
  line-height: 1.5;
  font-size: 16px;
}

.btn_btn:hover {
  background-color: #c0c0c0;
  color: white;
}

.btn_btn:active {
  background-color: black;
  color: white;

  transition: all 0.5s ease;
}

fieldset {
  margin: 10px;
  padding-bottom: 30px;
}

input,
select {
  margin: 0 50px 10px 0;
  border: 2px solid black;
  outline: none;
  width: 250px;
  padding: 5px;
  box-sizing: border-box;
}

select {
  padding: 0 0 5px 0;

  width: 250px;
}

.AddNew {
  width: 300px;
  padding-bottom: 30px;
  position: relative;
}

/* .btn_create_edit {
  position: absolute;
  right: 10px;
} */

.calimg input {
  width: 210px;
}
.calimg {
  position: relative;
}
.calimg img {
  width: 40px;
  position: absolute;
  top: 0;
  right: 0;
  cursor: pointer;
}

.AddNewAll {
  margin: 10px 0 0 30px;
}
</style>
