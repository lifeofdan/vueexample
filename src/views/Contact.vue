<template>
  <div>
    <h1>{{ pageName }}</h1>
    <div class="container">
      <ContactForm title="Contact Form" @data="personNameIs"/>
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

    function personNameIs (event) {
      console.log('the event', event)
      alert(`${event.name}, ${event.message}, ${event.email}`)
    }
    return { pageName, personNameIs }
  }
}
</script>

<style>
 .red {
   color: red;
 }
</style>
