<template>
  <div id="employee-table">
    <p v-if="employees.length === 0">
      [ No Employees ]
    </p>
    <table v-else>
      <thead>
        <tr>
          <th>Employee name</th>
          <th>Employee email</th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="employee in employees" :key="employee.id">
          <td>{{ employee.name }}</td>
          <td>{{ employee.email }}</td>
          <td>
            <button>Edit</button>
            <button @click="$emit('delete:employee', employee.id)">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'EmployeeTable',
    props: {
      employees: Array
    }
  }
</script>

<style scoped>
  button {
    margin-right: 10px;
  }
</style>