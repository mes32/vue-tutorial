<template>
  <div id="employee-table">
    <table>
      <thead>
        <tr>
          <th>Employee name</th>
          <th>Employee email</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Ada Lovelace</td>
          <td>ada@vue-tutorial.com</td>
        </tr>
        <tr>
          <td>Alan Turing</td>
          <td>alan@vue-tutorial.com</td>
        </tr>
        <tr>
          <td>John von Neumann</td>
          <td>john@vue-tutorial.com</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'employee-table',
}
</script>

<style scoped></style>