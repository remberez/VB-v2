<script>
    export let nameChapter = "Гостевой дом ";
    export let nameObject = "Вавилон";
    export let city = "Саратов";
    export let distans = 32;
    export let hrefs = "https://cache3.youla.io/files/images/780_780/5a/f3/5af3c7c9f8efdc8b0e3020b9.jpg";
    export let sale = 1904;
    export let tegs = []; // Изменили на массив
    
    let distansString = "м";
    if (distans > 999){
        distans/=1000
        distans.toFixed(2)
        distansString = "км";
    } 
  </script>
  
  <main class="animate__animated wow animate__fadeInUp">
    <a href="">
        <div class="block">
            <img src="{hrefs}" alt="{nameObject}">
        </div>
  
      <p id="one">{nameObject}</p>
      <p id="two">{city}, {distans}{distansString} до моря</p>
      <p id="sale">от {sale} руб <span>в сутки</span></p>
      
      <div id="tags">
        {#each tegs as tag}
          <span class="tag">{tag}</span>
        {/each}
      </div>
    </a>
  </main>

<style>
    main{
        box-shadow: 0 0 3px red;
    }

    .block{
        box-shadow: 0 0 3px red;
        width: 278px;
        height: 167px;
        top: 1391px;
        left: 348px;
        gap: 0px;
        border-radius: 10px 0px 0px 0px;
        opacity: 0px;
        object-fit: fill;
        margin-bottom: 10px;
    }

    #tags{
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 10px;
        margin-top: 10px;
    }

    .tag{
        font-size: 15px;
        color: gray;
        background-color: rgba(128, 128, 128, 0.185);
        padding: 2px 5px 2px 5px;
        border-radius: 5px;
    }

    #sale{
        font-family: Rubik;
        font-size: 18px;
        font-weight: 400;
        line-height: 21.33px;
        text-align: left;
        text-underline-position: from-font;
        text-decoration-skip-ink: none;
        margin-top: 10px;
    }

    #one{
        font-family: Rubik;
        font-size: 20px;
        font-weight: 300;
        line-height: 23.7px;
        text-align: left;
        text-underline-position: from-font;
        text-decoration-skip-ink: none;

    }

    #two{
        color: #8F8F8F;
        font-family: Rubik;
        font-size: 15px;
        font-weight: 300;
        line-height: 17.78px;
        text-align: left;
        text-underline-position: from-font;
        text-decoration-skip-ink: none;

    }

    main{
        display: flex;
        justify-content: center;
    }

    img{
        height: 100%;
        width: 100%;
        object-fit: cover;
    }

    a{
        text-decoration: none;
        color: black;
    }
</style>