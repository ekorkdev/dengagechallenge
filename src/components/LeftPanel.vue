<template>
  <div class="main">
    <ul>
      <div v-for="user in users" :key="user.id">
        <div v-if="user.parentId == null">{{ user.name }}
          <div v-for="usr in users" :key="usr.id">
            <div v-if="usr.parentId === user.id">{{ usr.name }}</div>
          </div>
        </div>
      </div>
    </ul>
  </div>
</template>

<script>
import users from '../assets/users.json'

export default {
  name: 'LeftPanel',
  data () {
    return {
      users
    }
  },
  props: {
  },
  components: {
  },
  return(){
    users
  }
}
</script>

<style scoped>
.main {
  width: 25%;
  border: 1px solid black;
  margin: 5px;
  display: block !important;
  padding: 10px; 
}

</style>
