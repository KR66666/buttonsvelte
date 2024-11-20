<script>
    // Získání atributů z props s výchozími hodnotami
    let { label = "Nadpis", children } = $props();
  </script>
  
  <div class="card">
    <h2 class="card-title">{label}</h2>
    <p class="card-text">
      {@render children()} <!-- Vykreslení obsahu (children) -->
    </p>
  </div>
  
  <style lang="scss">
    .card {
      width: 100%;
      max-width: 350px; /* Maximální šířka kartičky */
      margin: 20px auto; /* Mezera mezi kartičkami */
      padding: 20px;
      background-color: #fff; /* Bílá barva pozadí */
      border-radius: 12px; /* Zaoblení rohů */
      box-shadow: 0 10px 10px #06610191; /* Stín pro 3D efekt */
      transition: all 0.3s ease; /* Hladká animace pro hover */

      
    }

    .card:hover {
        transform: translateY(-5px); /* Zvednutí kartičky při hoveru */
        box-shadow: 0 15px 15px #61015b7e;
    }
  
    /* Styly pro nadpis kartičky */
    .card-title {
      font-size: 1.8rem; /* Velikost písma pro nadpis */
      font-weight: bold; /* Tučné písmo pro nadpis */
      color: #333; /* Tmavě šedá barva pro nadpis */
      margin-bottom: 10px; /* Mezera pod nadpisem */
      text-transform: uppercase; /* Velká písmena pro nadpis */
      letter-spacing: 1px; /* Rozteč písmen */
    }
  
    /* Styly pro text kartičky */
    .card-text {
      font-size: 1rem; /* Velikost textu pro obsah */
      color: #555; /* Světlejší šedá pro text */
      line-height: 1.6; /* Větší řádkování pro lepší čitelnost */
      margin-top: 10px; /* Mezera nad obsahem */
      text-align: justify; /* Zarovnání textu do bloku */
    }
</style>
  