<template>
  <div>
    <div class="message">
      <div v-for="m in message" :key="m.id" class="msg">
        {{m.msg}}
      </div>
    </div>

    <div class="animal">
      <div v-for="a in animal" :key="a.id" class="an">
        <img :src="a" alt="">
      </div>
    </div>

    <!-- <div class="myanimal">
        <img :src="animal[0]" alt="" class="horizontal">
        <img :src="animal[1]" alt="" class="big">
        <img :src="animal[3]" alt="" class="horizontal">
        <img :src="animal[4]" alt="" class="vertical">
        <img :src="animal[5]" alt="" class="big">
        <img :src="animal[6]" alt="" class="horizontal">
        <img :src="animal[7]" alt="" class="vertical">
        <img :src="animal[8]" alt="" class="horizontal">
        <img :src="animal[7]" alt="" class="horizontal">
        <img :src="animal[8]" alt="" class="big">
        <img :src="animal[9]" alt="" class="vertical">
    </div> -->

  </div>
</template>

<script>
export default {
  data(){
    return {
      message: [
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 1
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 2
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 3
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 4
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 5
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 6
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 7
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 8
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 9
        },
        {
          msg: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aut, atque!',
          id: 10
        },
      ],
      animal: [
        'https://source.unsplash.com/random/200x200?cat',
        'https://source.unsplash.com/random/200x200?dog',
        'https://source.unsplash.com/random/200x200?ant',
        'https://source.unsplash.com/random/200x200?spider',
        'https://source.unsplash.com/random/200x200?goat',
        'https://source.unsplash.com/random/200x200?lion',
        'https://source.unsplash.com/random/200x200?tiger',
        'https://source.unsplash.com/random/200x200?elephant',
        'https://source.unsplash.com/random/200x200?horse?',
        'https://source.unsplash.com/random/200x200?cow?',

      ]
    }
  }
}
</script>

<style>
.message{
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
  grid-row-gap: 10px;
  grid-column-gap: 20px;
}
.msg{
  background: #ddd;
  padding: 10px;
}
.animal{
  margin-top: 15px;
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
  gap: 10px;
}
.an{
  transition: all .4s ease-in;
}
.an:hover{
  scale: 2;
}
</style>