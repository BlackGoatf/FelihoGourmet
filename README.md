# FelihoGourmet
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliho Gourmet</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Edu+AU+VIC+WA+NT+Hand:wght@400..700&display=swap" rel="stylesheet">

    <header>
        <div class="logosur">
        <img src="https://th.bing.com/th/id/OIP.I7MRxj-M0QooRegQ_ufvrAHaHa?w=185&h=198&c=7&r=0&o=5&dpr=1.3&pid=1.7" alt="logo" id="logo">
        <h1>Feliho Gourmet</h1>
        </div>
        <nav id="navigation">
            <ul>
                <li><a href="#about">A propos</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
        
    </header>
    <div id="about">
        <h2>Historique</h2>
        <p>Le restaurant Feliho Gourmet a été fondé en 2024 par la famille Feliho.
        Feliho Gourmet a très rapidemment conquis le coeur des parisiens. En effet, depuis
        sa création, le Feliho Gourmet est complet tous les soirs.
        </p>
        <h2>Style cuisine</h2>
        <p>Le Feliho Gourmet est un restaurant gastronomique, les plus grands chefs cuisiner
            d'Europe se doivent de passer par ce restaurant pour se former sur un style de cuisine
            très particulier; la gastronomie antillaise et béninoise.
        </p>
        <h2>Ambiance</h2>
        <p>"Fantastique", "Très relaxant", "Magnifique", sont les commentaires qui reviennent le plus souvent
            lorsqu'on cite l'ambiance des restaurants Feliho Gourmet. Avec des pianistes professioneelles et des groupes de musiques
            antillaies et béninois, les restaurants Feliho Gourmet offrent une ambiance unique au monde.
        </p>
    </div>
    <div id="menu">
        <h2 id="ca">Menu</h2>
        <h3>Colombo</h3>
        <img src="https://img-3.journaldesfemmes.fr/x0fIRwR_3qkwp6CrZTKK1b2CXYM=/748x499/smart/f442c3867aed47eeb482b8efccef8736/recipe-jdf/10026118.jpg" alt="colombo" class="photomenu">
        <p class="prix">29.99€</p>
        <h3>Foutou Banane</h3>
        <img src="https://lesgourmandisesdekarelle.com/wp-content/uploads/2017/01/Foutou-Banane-4-1024x683.jpg" alt="foutou" class="photomenu">
        <p class="prix">15.99€</p>
        <h3>Saumon mijoté</h3>
        <img src="https://i.pinimg.com/originals/e8/86/8b/e8868bd7bc07f82017f30af2e5865e98.jpg" alt="saumon" class="photomenu">
        <p class="prix">20.99€</p>
    </div>
    <div id="contact">
        <h2>Nous contacter</h2>
        <p>Adresse: 25 boulevard des Champs-Elysées</p>
        <p>Numéro de téléphone: 01 50 56 48 07 14</p>
        <img src="https://th.bing.com/th/id/R.9ea230c32cc9fee4fcd7766c69cf80ca?rik=GjYEuGqwesp9Ig&riu=http%3a%2f%2ffr.map-of-paris.com%2fimg%2f0%2fplan-champs-elys%c3%a9es.jpg&ehk=snnsq5Wo8b3jZVDQgPkVbqHMUWNL5yYUMxVJsXnhOyU%3d&risl=&pid=ImgRaw&r=0" alt="carte" id="carte">
    </div>
    <button>Réserver une table</button>
    <script>
        // Fonction pour vérifier si un élément est dans la vue
        function isInView(element) {
            const rect = element.getBoundingClientRect();
            return rect.top >= 0 && rect.bottom <= window.innerHeight;
        }
        
        // Fonction pour ajouter la classe "visible" aux éléments visibles
        function revealElements() {
            const menuImages = document.querySelectorAll('.photomenu');
            const menuTexts = document.querySelectorAll('h3, .prix');
        
            // Vérification des images
            menuImages.forEach(image => {
                if (isInView(image)) {
                    image.classList.add('visible');
                }
            });
        
            // Vérification des titres et prix
            menuTexts.forEach(text => {
                if (isInView(text)) {
                    text.classList.add('visible');
                }
            });
        }
        
        // Écouteur d'événement sur le scroll
        window.addEventListener('scroll', revealElements);
        
        // Appel initial de la fonction au cas où l'élément est déjà visible au chargement
        revealElements();
        </script>
</body>
</html>
