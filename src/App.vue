<template>
  <div id='app'>
    <h2>{{ text }}</h2>
    <CustomInput v-model="text"/>
    <ApartmentsList :items="apartments">
      <template v-slot:apartment="{ apartment }">
        <ApartmentsItem
            :key="apartment.id"
            :descr="apartment.descr"
            :rating="apartment.rating"
            :imgSrc="apartment.imgUrl"
            :price="apartment.price"
            @click="handleItemClick"
        />
      </template>
    </ApartmentsList>
  </div>
</template>

<script>
import ApartmentsList from './components/apartment/ApartmentsList'
import ApartmentsItem from './components/apartment/ApartmentsItem'
import CustomInput from './components/shared/CustomInput'
import apartments from './components/apartment/apartments'
export default {
  name: 'App',
  components: {
    ApartmentsList,
    ApartmentsItem,
    CustomInput
  },
  data() {
    return {
      text: '',
      apartments
    }
  },
  methods:{
    handleItemClick() {
      console.log('item click')
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
