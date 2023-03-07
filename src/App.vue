<template>
<div id='app'>
  <ApartmentsItem
  :descr="apartment.descr"
  :price="apartment.price"
  :rating="apartment.rating"
  imgSrc="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg"
  />
</div>
  </template>

<script>
import ApartmentsItem from './components/apartment/ApartmentsItem.vue';
export default {
  name: 'App',
  components: {
    ApartmentsItem
  },
  data(){
    return {
      apartment: {
        id: '1',
        title: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        descr: 'Роскошные апартаменты в скайндинавском стиле с панорамным видом на реку и бесплатным Wi-Fi.',
        price: 2032,
        rating: 4.7,
        location:{
          city: 'Kherson',
        },
        owner:{
          name: 'Ellen',
          phone: '111-111-1111',
          email: 'Tracey.Morar86@hotmail.com',
        }
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
