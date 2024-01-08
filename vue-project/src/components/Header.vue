<template lang="">
  <div>
    <header class="header">
      <nav class="nav">
        <ol>
          <li><router-link to="/page">Adicionar Tarefa</router-link></li>
        </ol>
      </nav>
    </header><!--header-->
  </div>
</template>


<script>

export default{
  name: "Header",
}

</script>


<style scoped >

.header{
  display: flex;
  flex-direction: row;
  justify-content: end;
  background-color: #000;
  padding: 30px 0px;
}

.nav ol{
  margin-right:90px ;
}

.nav ol li{
  list-style-type: none;
  border: 1px solid #000;
  padding: 10px 15px;
  background-color: #fff;
}
.nav ol li a{
  text-decoration: none;
  color: #000;
  font-weight: 800;
  font-size: 20px;
}

</style>