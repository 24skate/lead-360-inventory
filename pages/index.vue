<template>
  <div class="flex h-screen w-full bg-gray-700">
      <div class="m-auto w-full px-5 md:w1/3">
      <form>
          <inputElement
            :labelName="'EMAIL'"
            :labelId="'email'"
            :inputType="'email'"
            :model="email"
            @input="email = $event"
            :disabled="false"
          />
          <inputElement
            :labelName="'PASSWORD'"
            :labelId="'password'"
            :inputType="'password'"
            :model="password"
            @input="password = $event"
            :disabled="false"
          />
          <button type="button"> SIGN IN </button?
      </form>
  </div>
</template>

<script>
  import Logo from '~/components/Logo.vue'
  import InputElement from "~/components/items/Input.vue";

  export default {
    components: {
      Logo,
      InputElement
    },
  data: function(){
      return{
        email: "",
        password: ""
        }
    }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
