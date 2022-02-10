<template>
  <header>
    <nav class="container"> 
      <ul>
        <li><a href="#">home</a></li>
        <li><a class="active" href="#">blog</a></li>
        <li><a href="#">chi siamo</a></li>
        <li><a href="#">contatti</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
  header{
    background-color: slategray;
    height: 70px;
    line-height: 70px;
    text-align: center;
    ul{
      list-style: none;
      li{
        display: inline-block;
        margin: 0 20px;
        a{
          text-decoration: none;
          color: white;
          &:hover{
            text-decoration: underline;
          }
          &:active{
            color: brown;
          }
        }
      }
    }
  }
</style>