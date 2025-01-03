<script>
  let image1 = 3;
  let y;

  function preload(src) {
    return new Promise(function (resolve) {
      let img = new Image();
      img.onload = resolve;
      img.src = src;
    });
  }
  let src = "background1.jpg";
</script>

<style>
  .covid {
    background-color: white;
    padding: 2rem;
    margin-top: 2rem;
  }
  .parallax-container {
    position: fixed;
    width: 1000px;
    height: 712px;
    left: 50%;
    transform: translate(-50%, 0);
  }

  .parallax-container img {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    will-change: transform;
  }

  .parallax-container2 {
    position: fixed;
    width: 1000px;
    height: 712px;
    left: 50%;
    transform: translate(-50%, 0);
  }
  .parallax-container2 img {
    position: absolute;
    top: 300px;
    left: 0;
    width: 100%;
    will-change: transform;
  }
  .parallax-container3 {
    position: fixed;
    width: 1000px;
    height: 712px;
    left: 50%;
    transform: translate(-50%, 0);
  }
  .parallax-container3 img {
    position: absolute;
    top: 900px;
    left: 0;
    width: 100%;
    will-change: transform;
  }

  .text {
    font-size: 60px;
    position: relative;
    width: 100%;
    height: 160vh;
    color: white;
    text-align: center;
    padding: 1.5em 0.5em 0.5em 0.5em;
    box-sizing: border-box;
  }

  span {
    display: block;
    font-size: 1em;
    will-change: transform, opacity;
  }

  .salongen {
    position: absolute;
    top: 711px;
    left: 0;
    width: 100%;
    height: calc(2050px - 712px);
    background-color: white;
    color: rgb(14, 10, 10);
    padding: 10vh 0 0 0;
    font-size: 16px;
  }
  .frisorer {
    position: absolute;
    top: 1700px;
    left: 0;
    width: 100%;
    height: calc(4510px - 1701px);
    background-color: white;
    color: rgb(14, 10, 10);
    padding: 10vh 0 0 0;
    font-size: 16px;
  }

  .karta {
    position: absolute;
    top: 4000px;
    left: 0;
    width: 100%;
    height: calc(5030px - 4001px);
    background-color: white;
    color: rgb(14, 10, 10);
    padding: 10vh 0 0 0;
    font-size: 16px;
  }

  :global(body) {
    margin: 0;
    padding: 0;
  }

  #clipart {
    font-family: "Nunito", sans-serif;
    /* text-shadow: 2px 2px 5px #00000045; */
  }

  #welcome {
    /* font-family: "Nunito", sans-serif; */
    font-family: "Baloo Tamma 2", cursive;
    font-size: 30px;
    text-shadow: 2px 2px 5px #0000008a;
  }

  #phone {
    text-shadow: 2px 2px 5px #0000008a;
  }

  p {
    font-family: "Nunito", sans-serif;
    font-size: 20px;
    margin: 1rem;
  }

  .oppet {
    width: 300px;
    margin: auto;
    font-family: "Nunito", sans-serif;
    font-size: 20px;
  }

  table {
    border-collapse: collapse;
    width: 100%;
  }

  td {
    border: 1px solid #dddddd;
    text-align: left;
    padding: 8px;
  }

  tr:nth-child(even) {
    background-color: #dddddd;
  }

  .frisor {
    border-radius: 1rem;
  }

  .frisorerCell {
    margin-top: 3rem;
  }

  .facebook {
    border-radius: 0.1rem;
  }

  /* .footer {
    text-align: center;
    background-color: #9d9c9c;
  } */

  /* Bigger screen */

  @media (min-width: 640px) {
    .parallax-container {
      position: fixed;
      width: 100%;
      left: 0;
      transform: translate(0, 0);
    }

    .parallax-container2 {
      width: 100%;
    }
    .parallax-container3 {
      width: 100%;
    }
    .grid-container {
      display: grid;
      grid-template-areas: "salong-img salong-img salong-text" "salong-img salong-img oppet";
      grid-column-gap: 50px;
      margin: 0 2rem;
      background-color: white;
      border-radius: 6px;
    }
    .gridImage {
      grid-area: salong-img;
      background-color: #292219;
      border: none;
    }
    .gridText {
      grid-area: salong-text;
      max-width: 50vw;
      padding-top: 2rem;
    }
    .gridTextOppet {
      grid-area: oppet;
      max-width: 50vw;
      margin-bottom: 3rem;
    }
    p {
      font-size: 1.3vw;
    }
    .oppet {
      font-size: 1.5vw;
    }
    .salongen {
      opacity: 0.5;
      /* position: absolute; */
      top: 85vh;
      color: rgb(14, 10, 10);
      font-size: 1.5vw;
      height: 70vw;
      background-color: #d3d3d300;
      will-change: transform;
    }

    .overlay2 {
      background-color: white;
      padding: 2rem;
      margin: 0 2rem;
      border-radius: 6px;
    }

    .flex-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      background-color: white;
    }

    .frisorer {
      position: absolute;
      top: 700px;
      color: rgb(14, 10, 10);
      font-size: 1.5vw;
      height: 70vw;
      background-color: #d3d3d300;
    }
    .frisorerCell {
      font-size: 10px;
      width: 250px;
    }

    .karta {
      position: absolute;
      top: 1100px;
      color: rgb(14, 10, 10);
      font-size: 1.5vw;
      height: 40vw;
      background-color: #d3d3d300;
    }
  }
  @media (min-width: 1200px) {
    .parallax-container img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100vh;
      will-change: transform;
    }
  }
</style>

<svelte:window bind:scrollY={y} />

{#if y < 720}
  <!-- <div
    class="parallax parallax-container"
    style="opacity: {1 - Math.max(0, y / 2000)}">
    <img
      style="transform: translate(0,{(-y * image1) / 20}px);"
      src="background1.jpg"
      alt="Salongen" />
  </div> -->
  <div class="parallax parallax-container" style="background-color: #292219">
    <img
      style="transform: translate(0,{(-y * image1) / 20}px);"
      src="background1.jpg"
      alt="Salongen" />
  </div>
{:else if y > 721 && y < 4100}
  <div class="parallax2 parallax-container2" style=" background-color: #292219">
    <img
      style="transform: translate(0,{(-y * image1) / 20}px);"
      src="stolar2.jpg"
      alt="Salongen" />
  </div>
{:else if y > 4101 && y < 6600}
  <div
    class="parallax3 parallax-container3"
    style="opacity: {Math.max(0.8, y / 5000)}">
    <img
      style="transform: translate(0,{(-y * image1) / 20}px);"
      src="background3.jpg"
      alt="Salongen" />
  </div>
{:else}
  <p>&puncsp;</p>
{/if}

<div class="text">
  {#await preload(src) then _}
    <span
      id="clipart"
      style="opacity: {1 - Math.max(0, y / 150)}">clip.art</span>
    <p id="welcome" style="opacity: {1 - Math.max(0, y / 200)}">
      Välkommen till vår mysiga salong i Malmö
    </p>
    <p id="phone" style="font-size:26px; opacity: {1 - Math.max(0, y / 200)}">
      <i class="fas fa-phone fa-1x" />
      <a href="tel:040-124620" style="color:white">040-124620</a>
    </p>
  {/await}

  <div class="salongen" style="opacity: {Math.max(0.5, y / 150)}">
    <div class="grid-container">
      <div class="gridText">
        <h2>Salongen</h2>
        <p style="margin-bottom: 4rem">
          Mitt i centrala Malmö vid Carolikvarteren hittar ni vår frisörsalong.
          Till oss kommer man för att få en upplevelse i en mysig miljö och för
          att få slappna av samtidigt som man blir snygg i håret. Vi erbjuder
          olika hårvårdsbehandlingar för både kvinnor och män.
        </p>
      </div>
      <div class="gridImage">
        <img
          style="width: 100%"
          src="shamponeringen-s2.jpg"
          alt="shamponeringen" />
      </div>
      <div class="gridTextOppet">
        <h2>Öppettider</h2>
        <div class="oppet">
          <table style="text-align:left;">
            <tbody>
              <tr>
                <td>mån-tis</td>
                <td>10.00-18.00</td>
              </tr>
              <tr>
                <td>onsdag</td>
                <td>10.00-20.00</td>
              </tr>
              <tr>
                <td>torsd</td>
                <td>09.00-20.00</td>
              </tr>
              <tr>
                <td>fred</td>
                <td>10.00-18.00</td>
              </tr>
              <tr>
                <td>lörd</td>
                <td>10.00-14.00</td>
              </tr>
              <tr>
                <td>sönd</td>
                <td>stängt</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="text">
  <div class="frisorer">
    <div class="overlay2">
      <h2>Frisörer</h2>
      <div class="flex-container">
        <div class="frisorerCell">
          <img class="frisor" src="marie.jpg" alt="Marie" />
          <h2>Marie</h2>
          <p>
            Frisöryrket valdes redan vid 13-års ålder. Marie började sin
            yrkesbana hos Leif Ohlin i Malmö. Drev Head Quarters i Malmö i många
            år. Sedan 2005 arbetar Marie på clip.art.
          </p>
        </div>
        <div class="frisorerCell">
          <img width="200px" class="frisor" src="lisa.jpg" alt="Lisa" />
          <h2>Lisa</h2>
          <p>
            Lisa har lång erfarenhet inom frisöryrket. Har arbetat många år i
            Lund på salong “Rickard i Lund”. Varit egenföretagare sedan 1994. Är
            nu en i teamet på clip.art sedan 2008.
          </p>
        </div>
        <div class="frisorerCell">
          <img width="200px" class="frisor" src="velimir.jpg" alt="Velimir" />
          <h2>Velimir</h2>
          <p>
            Velimir har varit i frisöryrket sedan 1999 och började på clip.art
            2014. "Ville" är noggrann och kreativ, och söker ständigt efter nya
            trender. Hans specialité är färg och slingor.
          </p>
        </div>
        <div class="frisorerCell">
          <img width="200px" class="frisor" src="kim.jpg" alt="Kim" />
          <h2>Kim</h2>
          <p>
            Kim började som frisör på salong HÄR i Lund. 1993 började Kim arbeta
            på Klippodromen i Malmö. Driver nu clip.art sedan några år tillbaka.
          </p>
        </div>
      </div>
      <a href="http://frisor.se/">
        <img
          src="SFF-logo.png"
          style="margin-top:10vh"
          alt="Sveriges frisörföretagare" />
      </a>
      <h2 style="margin-top: 4rem;">Produkter</h2>
      <p>
        Vi använder oss av produkter från
        <a href="http://www.keune.com/se">Keune</a>
        ,
        <a href="https://www.paulmitchell.com/">Paul Mitchell</a>
        och
        <a href="http://us.davines.com/">Davines</a>
        .
      </p>
    </div>
  </div>
</div>

<div class="text">
  <div class="karta">
    <div class="grid-container">
      <div class="grid-text">
        <h2 style="margin-top: 3rem">Hitta hit</h2>
        <a
          href="https://www.google.com/maps/place/Clip.art,+Snapperupsgatan+2B,+211+35+Malm%C3%B6/@55.6051755,13.0063718,17z/data=!4m2!3m1!1s0x4653a3fcd44c84db:0x16d72c147476ca4b">
          <img width="100%" src="maps.jpg" alt="Google maps" />
        </a>
      </div>
      <div class="gridimage" style="margin-bottom: 2rem;">
        <h2 style="margin-top: 3rem;">Adress</h2>
        <p>clip.art</p>
        <p>Snapperupsgatan 2</p>
        <p>211 35 Malmö</p>
        <h2 style="margin-top: 4rem">Tidsbokning</h2>
        <a href="tel:040-124620">040-124620</a>
        <p>Drop-in i mån av tid</p>
      </div>
      <div class="facebook">
        <h2 style="margin-top: 3rem">Vi finns på facebook</h2>
        <a href="https://sv-se.facebook.com/Clipart-135619699844728/">
          <img class="facebook" width="60%" src="facebook.png" alt="Facebook" />
        </a>
      </div>
    </div>
    <div class="covid">
      <!-- <h2>Covid-19</h2> -->
      <div>
        <p>
          På clip.art följer vi alla rekommendationer från Folkhälsomyndigheten
          så gott vi kan, för att ni som kunder ska känna er trygga.
        </p>
        <p>
          Vi rengör verktyg, byter klippkappor och tvättar händerna efter
          varje kund. Använder munskydd eller visir, erbjuder handsprit till er vid
          våra platser och vid kassan och har även dagar då det enbart är en
          frisör som arbetar för er som är i riskgruppen.
        </p>
        <p>
          Vi stannar hemma om vi inte är friska och är tacksamma om ni också gör det.
        </p>
        <br />
        Ta hand om er ❤️
      </div>
    </div>
  </div>
</div>
