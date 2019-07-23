<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>
    <EmployeeTable :employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from '@/components/EmployeeTable'

export default {
  name: 'app',
  components: {
    EmployeeTable
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Ada Lovelace',
          email: 'ada@vue-tutorial.com'
        },
        {
          id: 2,
          name: 'Alan Turing',
          email: 'alan@vue-tutorial.com'
        },
        {
          id: 3,
          name: 'John von Neumann',
          email: 'john@vue-tutorial.com'
        }
      ]
    }
  }
}
</script>

<style>
  button {
    background-color: #009435;
    border: 1px solid #009435;
  }

  .small-container {
    max-width: 680px;
  }
</style>
