<template>
  <div class="container">
    <form class="card">
      <!-- <h1>{{ getName }}</h1>
      {{ setName() }} -->
      {{ age }}
      {{ name }}
<!--
      <div class="form-control">
        <label for="email">Email</label>
        <input type="email" id="email" />
      </div>
      <div class="form-control">
        <label for="password">Password</label>
        <input type="password" id="password" />
      </div>
      <button class="btn primary">Submit</button> -->
      <hello-world msg="Hello" />
    </form>
  </div>
</template>
<script>
import { computed, ref, watch } from "vue";
import Home from './views/Home';
export default {
  components: {
    Home,
  },
  setup() {
    let name = ref("Eduard");
    let age = ref(21);
    const getName = computed(() => {
      return name.value + " Barev";
    });
    watch(age, () => {
      name.value = 'Astghik'
    })
      console.log('Component is mounting');
      name.value = 'SDAFGBGER'
    const getAge = computed(() => {
      return age;
    });
    const setName = () => {
      name.value = 'Hayk'
    }
    const setAge = () => {
      age.value = 30
    }
    return {
      name,
      getName,
      setName,
      getAge,
      age,
      setAge,
    };
  },
};
</script>
<style></style>
