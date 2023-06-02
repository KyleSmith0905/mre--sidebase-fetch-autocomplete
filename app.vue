<script lang="ts" setup>
const buttonClicked = async () => {
  const data = await $fetch('/api/test', {
    method: 'POST'
  })
  console.log(data.hello)
}
</script>
<template>
  <div>
    <TheWelcomeContainer />
    <button @click="buttonClicked()">
      Fetch Button
    </button>
  </div>
</template>
