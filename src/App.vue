<template>
  <div id="app">
    Tarea <input v-model="tarea" placeholder="Ingrese Nueva Tarea"/>
    <button @click="addTask">Agregar</button>
      <hr />
        <ul>
        <h1>Lista</h1>
          <li v-for="(TaskName, i) in tareas" :key="i">{{ TaskName }}</li>
        </ul>
  </div>
</template>
<script>
export default {
  name: "App",
    data() {
      return {
        tarea: "",
        tareas: [],
        
        };
      },
  methods: {
    addTask() {
      
      const { tarea } = this;
      this.tareas.push(tarea);
      this.tarea = "";
    },
  },
};

</script>

