<script setup>
    import { ref } from 'vue'

    // Add code here
    const loginType = ref("username");

    const inputValue = ref("");
</script>

<template>
    <div>
      <h1>Please select your login option</h1>
      <!-- Add/modify code in the following to have a dropdown list
          which lets the user to select either to login with username or email -->
      <select v-model="loginType">
          <option value = "username" selected>Username login</option>
          <option value ="email">Email login</option>
      </select>



      <div v-if="loginType === 'username'">

          <label for="username">Username</label>
          <input

            id="username"
            type="text"
            v-model="inputValue"
            placeholder="Enter your username">
      </div>

      <div v-else>

          <label for="email">Email</label>
          <input

            id="email"
            type="email"
            v-model="inputValue"
            placeholder="Enter your email address">
      </div>
    </div>
</template>

