<template>
 
 <h1>{{ header.toUpperCase() || "Welcome" }}</h1>
    <input v-model.trim="message" placeholder="Me edite" />
    <p>A mensagem é: {{ message }}</p>
    <li v-for="(item, key) in items" :key="item.id">
      {{ key }} {{ item.label }}
    </li>

<br><br>
    <select v-model='newItemPriority'>
      <option value='low'> Low</option>
      <option value='high'> high</option>
      </select>
      {{newItemPriority}}
<br><br>

  <label><input type='checkbox' v-model='isChecked'>{{isChecked ? 'Checked' : 'no checked'}}</label>


</template>

<script>
 
export default {
  name: 'App',
  data() {
    return {
      header: "Testing my header",
      message: "",
      newItemPriority: 'high',
      isChecked: false,
      items: [
        { id: 2, label: "second item" },
        { id: 1, label: "first item" },
        { id: 3, label: "third item " },
      ],
    };
  },
}
</script>

<style>
 
</style>
