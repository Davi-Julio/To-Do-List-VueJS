<template lang="">
  <div>
    <li id="link" ><router-link to="/">Back</router-link></li>

    <form @submit.prevent="add" class="form" action="">
      <h1>Adicione Suas Tarefas</h1>
      <input required type="text" v-model="newNome" placeholder="Digite Suas tarefas">
      <input type="submit" value="Adicionar" name="" id="btn">
      <ul class="ul">
        <li v-for="(nome, index) in nomes " :key="index">
          {{nome}}
          <button id="btnRemove" @click="remove">Remover</button>
        </li>
      </ul>
    </form><!--form-->
  </div>
</template>

<script>
export default {
  name: "Page",

  data() {
    return {
      newNome: "",
      nomes: [],
    };
  },

  methods: {
    add(e) {
      e.preventDefault();
      if (this.newNome.trim() !== "") {
        this.nomes.push(this.newNome.trim());
        this.newNome = "";
      }
    },

    remove(index) {
      this.nomes.splice(index, 1);
    },
  },
};
</script>

<style scoped>
#link {
  margin: 0px 20px;
  font-size: 20px;
}

.form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 50px 0px;
}

.form input {
  width: 40vw;
  height: 6vh;
  padding-left: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  outline: none;
  margin-bottom: 20px;
}

#btn {
  width: 30vw;
  height: 6vh;
  background-color: #000;
  color: #fff;
  font-weight: 800;
  cursor: pointer;
}

#btnRemove{
  width: 10vw; height: 5vh;
  background-color: red;
  margin: 0px 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  color: #fff;
  font-weight: 800;
}

.ul li{

  margin: 20px 0px;
}
</style>