<template>
  <div class="home-page">
    <h1>Welcome to <b>Archive.Earth</b></h1>
    <div class="folder">
      <img src="/assets/archive-earth-coloured-logo.svg" alt="archive-earth-coloured-logo">
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.home-page{
  position: absolute;
  left: 0;
  right: 0;
  top: 387px;
}

.home-page h1{
  font-size: 53px;
  font-weight: 200;
  color: black;
}

.home-page h1 b{
  font-size: 65px;
  font-weight: 600;
}

.home-page .folder{
  margin-top: 30px;
}

@media screen and (max-width: 1279px){
  .home-page h1 b{
    display: block;
  }
  
  .home-page{
    top: 287px;
  }
}

@media screen and (max-width:768px){

  .home-page{
    top: 200px;
  }

  .home-page h1 b{
    font-size: 45px;
    display: block;
  }

  .home-page h1{
    font-size: 37px;
  }

  .home-page .folder img{
    width: 245px;
  }

}

</style>
