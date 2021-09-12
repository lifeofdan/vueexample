<template>

  {{heading}}
  <div class="text-start">
    <div class="mb-3 text-start">
      <label for="exampleFormControlInput1" class="form-label">Name</label>
      <input type="text" v-model="name" class="form-control" placeholder="John Smith">
    </div>
    <div class="mb-3">
      <label for="exampleFormControlInput2" class="form-label">Email address</label>
      <input type="email" v-model="email" class="form-control" placeholder="name@example.com">
    </div>
    <div class="mb-3">
      <label for="exampleFormControlInput3" class="form-label">Message</label>
      <textarea v-model="message" class="form-control" placeholder="Type your message here."></textarea>
    </div>
    <button class="btn btn-primary" @click="submit">Submit</button>
  </div>
</template>

<script>
import { ref, reactive } from 'vue'
export default {
  name: 'ContactForm',
  props: {
    title: {
      type: String,
      default: ''
    }
  },
  emits: [
    'data'
  ],
  setup (props, context) {
    const heading = props.title.valueOf()
    const name = ref('')
    const email = ref('')
    const message = ref('')
    const data = reactive({ name: name, email: email, message: message })

    function submit () {
      context.emit('data', data)
    }
    return { heading, name, email, message, submit }
  }
}
</script>

<style>

</style>
