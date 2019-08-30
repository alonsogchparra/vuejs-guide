<template>
  <div class="component">
    <h1>The User Component</h1>
    <p>I'm an awesome User!</p>
    <button @click="changeName">Change My Name</button>
    <p>Name is {{ name }}</p>
    <p>Age is {{ age }}</p>
    <hr>
    <div class="row">
      <div class="col-xs-12 col-md-6">
        <app-user-detail
          :myName='name'
          @nameWasReset='name = $event'
          :resetFn='resetName'
          :userAge='age'
        ></app-user-detail>
      </div>
      <div class="col-xs-12 col-md-6">
        <app-user-edit
          :userAge='age'
          @ageWasEdited='age = $event'
        ></app-user-edit>
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from './UserDetail';
import UserEdit from './UserEdit';
export default {
  data: function() {
    return {
      name: 'Alonso',
      age: 27
    }
  },
  methods: {
    changeName() {
      return this.name = 'Anna';
    },
    resetName() {
      this.name = 'Alonzo'
    }
  },
  components: {
    appUserDetail: UserDetail,
    appUserEdit: UserEdit
  }
}
</script>

<style scoped>
  div {
    background-color: lightblue;
  }
</style>