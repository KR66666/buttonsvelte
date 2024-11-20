<script>
    // Získání atributů z `$props`, s výchozími hodnotami
    let { href = "#", color = "default", children } = $props();

    // Dynamická třída
    let Button_class = `${color} button`;
</script>

<a {href} class={Button_class}>
    {@render children()} <!-- Správné použití {@render} pro vykreslení children -->
</a>

<style lang="scss">
    .button {
        max-width: 85px;
        width: 100%;
        text-align: center;
        text-decoration: none;
        padding: 10px;
        margin-top: 25px;
        background-color: #fff; /* Bílá barva pozadí */
        border-radius: 12px; /* Zaoblení rohů */
        transition: all 0.3s ease; /* Hladká animace pro hover */
    }

    .button:hover {
        transform: translateY(-5px); /* Zvednutí kartičky při hoveru */
        box-shadow: 0 15px 15px #06610191;
    }


    .default {
        background-color: #ccc;
        color: #000;
    }
    .purple {
        background-color: #61015b;
        color: #ffffff;
    }
</style>