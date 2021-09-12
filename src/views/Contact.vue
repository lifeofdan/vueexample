<template>
  <div>
    <h1>{{ pageName }}</h1>
    <div class="container">
      <ContactForm />
    </div>

  </div>
</template>

<script>
import ContactForm from '../components/ContactForm.vue'
export default {
  name: 'ContactPage',
  components: { ContactForm },
  setup () {
    const pageName = 'Contact Page'

    return { pageName }
  }
}
</script>

<style>
 .red {
   color: red;
 }
</style>
