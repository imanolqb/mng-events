<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Ñoooo to guapo en veldaaa" />
  </div>
</template>

<script setup lang="ts">
import HelloWorld from "@/components/HelloWorld.vue";
import { useAuthStore } from "@/stores/auth";
import { onMounted } from "vue";

onMounted(() => {
  const userStore = useAuthStore();
  userStore.signIn('jj.quesadaacosta@hotmail.com', 'jotajota')
  console.log(userStore.user)
});



</script>
