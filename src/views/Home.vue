<template>
  <div>
    <b-table striped hover :items="items">
      <template slot="top-row" slot-scope="{ fields }">
        <td v-for="field in fields" :key="field.keys">
          <form>
            <select>
              <option>A</option>
              <option>B</option>
              <option>C</option>
              <option>D</option>
              <option>E</option>
            </select>
          </form>
        </td>
<!--         <td v-for="field in fields" :key="field.key">
          <input v-model="filters[field.key]" :placeholder="field.label">
        </td> -->
      </template>
    </b-table>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        items: [
          { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
          { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
          { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
          { age: 38, first_name: 'Jami', last_name: 'Carney' }
        ]
      }
    }
  }
</script>