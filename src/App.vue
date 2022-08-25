<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import TheHeader from './components/TheHeader.vue';

export default {
  name: 'APP',
  components: {
    TheHeader,
  },
  data() {
    return {
      showName: true,
      firstName: 'Jon',
      lastName: 'Snow',
      accessLevel: 'admin',
      todos: [
        {
          id: 1,
          name: 'Leanne Graham',
          username: 'Bret',
          email: 'Sincere@april.biz',
          img: 'https://via.placeholder.com/50x50.png',
          alt: 'Avatar de Leanne Graham',
          address: {
            street: 'Kulas Light',
            suite: 'Apt. 556',
            city: 'Gwenborough',
            zipcode: '92998-3874',
            geo: {
              lat: '-37.3159',
              lng: '81.1496',
            },
          },
          phone: '1-770-736-8031 x56442',
          website: 'hildegard.org',
          company: {
            name: 'Romaguera-Crona',
            catchPhrase: 'Multi-layered client-server neural-net',
            bs: 'harness real-time e-markets',
          },
        },
        {
          id: 2,
          name: 'Ervin Howell',
          username: 'Antonette',
          email: 'Shanna@melissa.tv',
          img: 'https://via.placeholder.com/50x50.png',
          alt: 'Avatar de Ervin Howell',
          address: {
            street: 'Victor Plains',
            suite: 'Suite 879',
            city: 'Wisokyburgh',
            zipcode: '90566-7771',
            geo: {
              lat: '-43.9509',
              lng: '-34.4618',
            },
          },
          phone: '010-692-6593 x09125',
          website: 'anastasia.net',
          company: {
            name: 'Deckow-Crist',
            catchPhrase: 'Proactive didactic contingency',
            bs: 'synergize scalable supply-chains',
          },
        },
        {
          id: 3,
          name: 'Clementine Bauch',
          username: 'Samantha',
          email: 'Nathan@yesenia.net',
          address: {
            street: 'Douglas Extension',
            suite: 'Suite 847',
            city: 'McKenziehaven',
            zipcode: '59590-4157',
            geo: {
              lat: '-68.6102',
              lng: '-47.0653',
            },
          },
          phone: '1-463-123-4447',
          website: 'ramiro.info',
          company: {
            name: 'Romaguera-Jacobson',
            catchPhrase: 'Face to face bifurcated interface',
            bs: 'e-enable strategic applications',
          },
        },
        {
          id: 4,
          name: 'Patricia Lebsack',
          username: 'Karianne',
          email: 'Julianne.OConner@kory.org',
          address: {
            street: 'Hoeger Mall',
            suite: 'Apt. 692',
            city: 'South Elvis',
            zipcode: '53919-4257',
            geo: {
              lat: '29.4572',
              lng: '-164.2990',
            },
          },
          phone: '493-170-9623 x156',
          website: 'kale.biz',
          company: {
            name: 'Robel-Corkery',
            catchPhrase: 'Multi-tiered zero tolerance productivity',
            bs: 'transition cutting-edge web services',
          },
        },
        {
          id: 5,
          name: 'Chelsey Dietrich',
          username: 'Kamren',
          email: 'Lucio_Hettinger@annie.ca',
          address: {
            street: 'Skiles Walks',
            suite: 'Suite 351',
            city: 'Roscoeview',
            zipcode: '33263',
            geo: {
              lat: '-31.8129',
              lng: '62.5342',
            },
          },
          phone: '(254)954-1289',
          website: 'demarco.info',
          company: {
            name: 'Keebler LLC',
            catchPhrase: 'User-centric fault-tolerant solution',
            bs: 'revolutionize end-to-end systems',
          },
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <!-- Loop Example -->
    <h5 class="title">Loop Example</h5>
    <div v-for="(obj, index) in todos" v-bind:key="obj.id" class="todos-item">
      <!-- dinamizando atributos com v-bind ou : faz a mesma coisa-->
      <img v-if="obj.img" v-bind:src="obj.img" :alt="obj.alt" />
      {{ index }} - {{ obj.name }}
    </div>
    <hr />
    <!-- If Example -->
    <h5 class="title">IF Example</h5>
    <div v-show="showName">
      Nome: {{ firstName }} <br />
      Sobrenome: {{ lastName }}
    </div>
    <hr />
    <!-- If Else Example -->
    <h5 class="title">IF ELSE Example</h5>
    <div>
      <div v-if="accessLevel === 'admin'">Usuário Admin</div>
      <div v-else-if="accessLevel === 'marketing'">Usuário Marketing</div>
      <div v-else>Usuário normal</div>
    </div>
  </div>
</template>

<style scoped>
.title {
  margin: 0;
}
.todos-item {
  background: red;
  text-align: left;
}
.header {
  background: #000;
  color: #fff;
}
</style>
