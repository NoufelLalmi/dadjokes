<template>
  <div>
    <header>
      <ul>
        <li><NLink to="/" class="active">Home</NLink></li>
        <li><NLink to="about">About</NLink></li>
        <li><NLink to="jokes">Jokes</NLink></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </header>
  </div>
</template>

<script>
export default {}
</script>

<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}
</style>
