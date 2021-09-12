<template>
  <div class="text-start">
    <div class="mb-3 text-start">
      <label for="exampleFormControlInput1" class="form-label">Name</label>
      <input type="text" class="form-control" placeholder="John Smith">
    </div>
    <div class="mb-3">
      <label for="exampleFormControlInput2" class="form-label">Email address</label>
      <input type="email" class="form-control" placeholder="name@example.com">
    </div>
    <div class="mb-3">
      <label for="exampleFormControlInput3" class="form-label">Message</label>
      <textarea class="form-control" placeholder="Type your message here."></textarea>
    </div>
    <button class="btn btn-primary">Submit</button>
  </div>
</template>

<script>
export default {
  name: 'ContactForm'

}
</script>

<style>

</style>
