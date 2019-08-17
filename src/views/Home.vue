<template>
  <div>
    <b-table striped hover :items="items">
      <template slot="top-row" slot-scope="{ fields }">
        <td v-for="field in fields" :key="field.keys">
          <form>
            <select>
              <option v-for="key in dropDownSelectors[field.key]">{{ key }}</option>
            </select>
          </form>
        </td>
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
        ],
        dropDownSelectors: {
          'age': [1, 2, 3, 4, 5],
          'first_name': [1,2,3,4,5],
          'last_name': [1,2,3,4,5]
        }
      }
    }
  }
</script>