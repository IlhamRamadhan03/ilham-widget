<template>
    <div class="homepage">
      <h1>Selamat Datang di Halaman Home <br>ホームページへようこそ</h1>
      <p>Ini adalah halaman utama Vue.js</p>
      <div class="button-f">
        <button class="button" @click="masukKeCuaca">Cuaca</button>
        <button class="button" @click="MasukKeLokasi">Lokasi</button>
        <button class="button" @click="masukKeStopwatch">Stopwatch</button>
        <button class="button" @click="masukKeTikTakToe">Tic Tac Toe</button>
        <button class="button" @click="masukKeFoto">Foto</button>
      </div>
    </div>
  </template>
  
  <script>
  import HelloWorld from '../components/HelloWorld.vue'
  
  export default {
    components: {
      HelloWorld
    },
  
  methods: {
      masukKeCuaca() {
        this.$router.push('/cuaca')
      },
      masukKeStopwatch() {
        this.$router.push('/stopwatch')
      },
      MasukKeLokasi() {
        this.$router.push('/lokasi')
      },
      masukKeFoto() {
        this.$router.push('/foto')
      },
      masukKeTikTakToe() {
        this.$router.push('/tictactoe')
      },
    }
  }
  </script>

<style>
.homepage{
    background-image: url('../assets/1.jpeg');
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }

h1 {
  font-size: 24px;
  color: #ff0000;
  margin-bottom: 10px;
}

p {
  font-size: 16px;
  color: #ff0000;
}

.button-f {
  margin-top: 20px;
}

.button {
  display: inline-block;
  margin: 5px;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 5px;
  background-color: #3498db;
  color: #fff;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: #3dff3d;
}

.custom-button {
  display: inline-block;
  margin: 5px;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 5px;
  background-color: #e67e22;
  color: #fff;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.custom-button:hover {
  background-color: #d35400;
}
</style>