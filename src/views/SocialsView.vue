<template>
    <div id="container">
        <a class="social" target="_blank" href="https://www.instagram.com/honey.mby/">
          <img src="/img/insta.png" alt="" srcset="">
          <h1>@Honey.mby</h1>
          <p>É a rede social principal da Honey, é o lugar onde ela faz todas as interações e posta a maioria das fotos</p>
        </a>
        <a class="social" target="_blank" href="https://www.tiktok.com/@honey.mbee">
          <div id="img"><img src="/img/tiktok.png" alt="" srcset=""></div>
          <h1>@Honey.mby</h1>
          <p>É a rede social secundária da Honey, lá ela posta alguns videos criativos ou só biscoitando (CUIDADO PRA NAO SE APAIXONAR!!!!)</p>
        </a>
    </div>
  </template>
  

  
  <style scoped>

  #container {
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }
  a.social {
    display: flex;
    height: 300px;
    width: 80vh;
    background-image: linear-gradient(0.45turn,rgb(184, 98, 0), rgb(67, 0, 122));
    margin: 50px;
    flex-wrap: wrap;
    border-radius: 15px;
    padding: 15px;
    box-shadow: -1px 1px 3px 1px rgba(0, 0, 0, 0.308);
    transition: 0.5s;
    border: none;
    text-decoration: none;

  }

  h1 {
    margin-top: 25px;
    font-size: 1.3em;
    color: white;
  }

  p {
    font-family: Arial, Helvetica, sans-serif;
    color: white;
    font-size: 1.1em;
    font-weight: bold;
    margin-top: -70px;
    margin-left: 25px;
  }

  #img {
    background-color: white;
    width: 50px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    margin: 15px;
  }

  img {
    height: 80px;
    width: 83px;
    border-radius: 10px;
  }

  a.social:hover {
    height: 350px;
    width: 85vw;
    cursor: pointer;
  }
  </style>