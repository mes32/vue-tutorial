<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>
    <EmployeeForm @add:employee="addEmployee" />
    <EmployeeTable :employees="employees" @delete:employee="deleteEmployee" />
  </div>
</template>

<script>
  import EmployeeForm from '@/components/EmployeeForm'
  import EmployeeTable from '@/components/EmployeeTable'

  export default {
    name: 'app',
    components: {
      EmployeeForm,
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
    },
    methods: {
      addEmployee(employee) {
        const id = this.employees.length > 0 ? this.employees.length + 1 : 1
        const newEmployee = { ...employee, id }
        this.employees = [...this.employees, newEmployee]
      },
      deleteEmployee(id) {
        this.employees = this.employees.filter(
          employee => employee.id !== id
        )
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
