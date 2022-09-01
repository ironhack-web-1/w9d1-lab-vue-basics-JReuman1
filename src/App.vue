<template>
  <div class="head">
    <header>
      <img alt="Vue logo" src="./assets/logo.png" />
      <ul>
        <li>Home</li>
      </ul>
    </header>
  </div>

  <div class="opeacion">El resultado de 10 + 10 = {{ vresult }}</div>
  <hr />
  <hr />

  <div class="vbutton">
    <button v-on:click="vresult += 1">Suma 1 al resultado</button>
    <button v-on:click="vresult -= 1">Resta 1 al resultado</button>
  </div>
  <hr />
  <hr />

  <h3>El valor actual es: {{ vresult }}</h3>
  <div v-if="vresult === 20">
    <h4>Esta sección solo se mostrara si la variable es 20</h4>
  </div>

  <hr />
  <hr />

  <div class="string">{{ vstring }}</div>
  <hr />
  <hr />

  <div v-for="(data, index) in vdata" :key="index">
    El UUID es: {{ vdata[index].uuid }} <br />
    El nombre es: {{ vdata[index].name }} <br />
    La descripción es: {{ vdata[index].description }} <hr /><br />
  </div>

  <hr />
  <hr />

  <div class="vbutton">
    <button v-on:click="dissapear" >Cambia el color de fondo</button>
  </div>
  
  <hr />
  <hr />

  <div>
    <footer>
      <ul>
        <li><p>This is your Vue.js footer</p></li>
      </ul>
    </footer>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      vresult: 10 + 10,
      vstring: "Esta es una app de VUE",
      vdata: [
        {
          uuid: "4",
          name: "Lorem ipsum",
          description: "Lorem ipsum",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          image:
            "https://github.com/ironhack-jc/mid-term-api/blob/main/4.jpg?raw=true",
          completed_on: "June 10, 2021",
        },
        {
          uuid: "3",
          name: "Vectorify",
          description: "User Experience Design",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          image:
            "https://github.com/ironhack-jc/mid-term-api/blob/main/3.jpg?raw=true",
          completed_on: "June 10, 2021",
        },
        {
          uuid: "2",
          name: "Dashcoin",
          description: "Web Development",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
          image:
            "https://github.com/ironhack-jc/mid-term-api/blob/main/2.jpg?raw=true",
          completed_on: "June 10, 2021",
        },
        {
          uuid: "1",
          name: "Simplify",
          description: "UI Design & App Development",
          content:
            "Aliqua id fugiat nostrud irure ex duis ea quis id quis ad et! Sunt qui esse pariatur duis deserunt mollit dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nisi. Aliqua id fugiat nostrud irure ex duis ea quis id quis ad et. Sunt qui esse pariatur duis deserunt mollit dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nisi.Aliqua id fugiat nostrud irure ex duis ea quis id quis ad et. Sunt quix duis ea quis id quis ad et. Sunt qui esse pariatur duis deserunt mollit dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nisi.<br><br>Aliqua id fugiat nostrud irure ex duis ea quis id quis ad et. Sunt qui esse pariatur duis deserunt mollit dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nisi.Aliqua id fugiat nostrud irure ex duis ea quis id quis ad e dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nisis ea quis id quis ad et. Sunt qui esse pariatur duis deserunt mollit dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nisi.Aliqua id fugiat nostrud irure ex duis ea quis id quis ad e dolore cillum minim tempor enim. Elit aute irure tempor cupidatat incididunt sint deserunt ut voluptate aute id deserunt nis cillum minim tempor enim.",
          image:
            "https://github.com/ironhack-jc/mid-term-api/blob/main/1.jpg?raw=true",
          completed_on: "June 22, 2021",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

header {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
}

header img {
  width: 15px;
  height: 15px;
}

header li {
  list-style: none;
}

footer {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

footer li {
  list-style: none;
}
</style>
