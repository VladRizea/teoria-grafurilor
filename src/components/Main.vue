<template>
  <div class="main-section">
    <h3 class="section-title teko white">
      Graf neorientat
    </h3>
    <pre class="npm-code white">
               <p class="code">
Definiție: Se numește graf neorientat o pereche ordonată de mulțimi G=(X,U), unde:
<br>
X este o mulțime finită și nevidă de elemente numite vârfuri sau noduri;
<br>
U este o mulțime finită de submulțimi cu două elemente din X, numite muchii.
              </p>
     </pre>
    <br>
    <h3 class="section-title teko white">
      Graf interactiv
    </h3>
<d3-network :net-nodes="nodes" :net-links="links" :options="options">
    </d3-network>
    <br>
    <h3 class="section-title teko white">
      Tipuri de grafuri neorientate
    </h3>
  <div class="wrap-table">
      <table class="rwd-table">

        <thead>
          <tr>
            <th>Nume</th>
            <th>Part</th>
          </tr>
        </thead>

        <tr>
          <td data-th="Nume">Conex</td>
          <td data-th="Part">Între oricare 2 noduri distincte există cel puțin un lanț.</td>
        </tr>

        <tr>
          <td data-th="Nume">Aciclic</td>
          <td data-th="Part">Între oricare 2 noduri distincte există cel puțin un lanț.</td>
        </tr>

        <tr>
          <td data-th="Nume">Hamiltonian</td>
          <td data-th="Part">Conține cel puțin un ciclu Hamiltonian (trece prin toate vârfurile)</td>
        </tr>

        <tr>
          <td data-th="Nume">Eulerian</td>
          <td data-th="Part">Conține cel puțin un lant Eulerian (trece prin toate muchiile)</td>
        </tr>
        <tr>
          <td data-th="Nume">Arbori</td>
          <td data-th="Part">Conține cel puțin un lant Eulerian (trece prin toate muchiile)</td>
        </tr>

      </table>
    </div>
<br>

    <h3 class="section-title teko white">
      Graf orientat
    </h3>
    <pre class="npm-code white">
              <p class="code">
Se numeşte graf orientat sau digraf o pereche ordonată de mulțimi notată
<br>
G=(V, U), unde:
<br>
V este o mulțime finită şi nevidă ale cărei elemente se numesc noduri sau vârfuri;
<br>
U este o mulțime de perechi ordonate de elemente distincte din V ale cărei elemente se numesc arce.
              </p>
     </pre>
     <br>
        <h3 class="section-title teko white">
      Determinarea celui mai scurt drum dintre 2 puncte
    </h3>
<iframe src="https://anvaka.github.io/ngraph.path.demo/#?graph=amsterdam-roads" title="W3Schools Free Online Web Tutorials">
</iframe>
    <br>
        <h2 class="section-title teko white">
      Cum functioneaza?
    </h2>
    <pre class="npm-code white">
      <p class="code">
        Fiecare nod reprezinta o intersectie, iar fiecare muchie primește o greutate care in acest caz reprezintă lungimea drumului.
     </p>
    </pre>
    <img class="npm-code" src="../assets/greutate.png" alt="">
    <pre class="npm-code white">
      <p class="code">
        Algoritmul calculează toate drumurile posibile, în final returnând cel mai scurt drum între cele 2 puncte.
     </p>
    </pre>
    <img class="npm-code" src="../assets/roads.png" alt="">
    <pre class="npm-code white">
      <p class="code">
        Grafurile orientate pot fi folosite pentru a crea sensuri unice!
     </p>
    </pre>
    <img class="npm-code" src="../assets/sensUnic.png" alt="">

    <pre class="npm-code white">
      <p class="code">
        AC + CB = 14 <br>
        AD + DE + DB = 13 <br>
        AB = 10 <br>
        Răspuns AB.
     </p>
    </pre>

    <h3 class="section-title teko white">
      Arbori
    </h3>
    <pre class="npm-code white">
      <p class="code">
          Un arbore este un graf conex și aciclic.
      </p>
     </pre>
    <br>
    <h3 class="section-title teko white">
      Utilizarea arborilor
    </h3>
    <h2 class="section-title teko white">
      Arbori genealogici
    </h2>

<img class="npm-code" src="../assets/arboreGenealogic.jpg" alt="">
    <h2 class="section-title teko white">
      Cum functioneaza?
    </h2>
    <pre class="npm-code white">
      <p class="code">
      Fiecare nod copil provinde din 1 sau 2 noduri parinti.
      <br>
      Arborele genealogic este diferit de un arbore normal datorită aparitiei unor noi noduri ce nu apartin retelei originale. În acest caz rețeaua originală este familia Badea.
      </p>
    </pre>
<img class="npm-code" src="../assets/arboresange.png" alt="">
<br>
<br>
<img class="npm-code" src="../assets/arboreiar.jpg" alt="">
  </div>
</template>
<script>
import D3Network from 'vue-d3-network'
  /* eslint-disable */
  const appCode = `<template>
      <div id="app">
        <vue-particles color="#dedede"></vue-particles>
      </div>
   </template>`
  const appCodeFull = `<template>
      <div id="app">
        <vue-particles
          color="#dedede"
          :particleOpacity="0.7"
          :particlesNumber="80"
          shapeType="circle"
          :particleSize="4"
          linesColor="#dedede"
          :linesWidth="1"
          :lineLinked="true"
          :lineOpacity="0.4"
          :linesDistance="150"
          :moveSpeed="3"
          :hoverEffect="true"
          hoverMode="grab"
          :clickEffect="true"
          clickMode="push"
        >
        </vue-particles>
      </div>
   </template>`
    /* eslint-disable */
  export default {
    name: 'main-content',
      components: {
    D3Network
  },
    data () {
      return {
        appCode,
        appCodeFull,
        nodes: [
          { id: 1, name: 'nodul 1' },
          { id: 2, name: 'nodul 2' },
          { id: 3, _color:'orange', name: 'nodul 3' },
          { id: 4, name: 'nodul 4' },
          { id: 5, name: 'nodul 5' },
          { id: 6, name: 'nodul 6' },
          { id: 7, name: 'nodul 7' },
          { id: 8, name: 'nodul 8' },
          { id: 9, name: 'nodul 9' },
          { id: 10, name: 'nodul 10' }
        ],
        links: [
          { sid: 1, tid: 2, _color:'red' },
          { sid: 2, tid: 8, _color:'f0f' },
          { sid: 3, tid: 4,_color:'rebeccapurple' },
          { sid: 4, tid: 5 },
          { sid: 5, tid: 6 },
          { sid: 7, tid: 8 },
          { sid: 5, tid: 8 },
          { sid: 3, tid: 8 },
          { sid: 7, tid: 9 },
          { sid: 10, tid: 9 }
        ],
        options:
        {
          force: 3000,
          nodeSize: 20,
          nodeLabels: true,
          linkWidth:5
        }
      }
    },

  }
</script>


<style lang="scss">
iframe{
  width: 100%;
  height: 500px;
}
  .node {
  stroke: #fff;
  stroke-width: 1.5px;
  color: white;
  .node-label{
    color: white;
  }
}
  .node-labels{
    color: white;
  }
.link {
  stroke: #999;
  stroke-opacity: .6;
}
</style>
