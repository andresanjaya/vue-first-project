<template>
  <li>
    <a :href="emailLink">{{ email }}</a>
    <p><b>Username: </b>{{ fullName }}</p>
    <p><b>Borrow Date: </b>{{ date }}</p>
    <p><b>Phone Number: </b>{{ phoneNumber }}</p>
  </li>
   
</template>

<script>
export default {
  props: ['fullName', 'email', 'phoneNumber' , 'date'],
  computed: {
    emailLink() {
      return 'mailto:' + this.email;
    }
  }
}
</script>

<style scoped>
li {
  margin: 1rem 0;
  border: 1px solid #ccc;
  padding: 1rem;
}

a {
  color: #3d008d;
  text-decoration: none;
  font-weight: bold;
}

a:hover,
a:active {
  color: #8d007a;
}

p {
  margin: 0.5rem 0 0 0;
}

h6 {
  margin-top: 5px;
}
</style>