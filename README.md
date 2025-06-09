# Ggg

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <!-- Link to external CSS file -->
    <link rel="stylesheet" href="CSS/Style.css">

    <!-- ICON -->
    <link rel="icon" href="Resources/Logo-removebg-preview.png" type="image/png">
</head>

<body>

    <video  autoplay muted loop id="video-background">
        <source src="Resources/12716-241674181_small.mp4" type="video/mp4">
    </video>
        

 <!--Header of the website-->
 <header>
    <div class="logo-container">
        <img src="Resources/Logo-removebg-preview.png" alt="logo-portfolio">
    </div>

    <h1>Portfolio</h1>
    <!-- Navigation bar -->
    <nav>
        <ul>
            <li><a href="#About-section">About me</a></li>
            <li><a href="#Projects">Projects</a></li>
            <li><a href="#Skills">Skills</a></li>
            <li><a href="#Contact">Contact me</a></li>
        </ul>
    <h2>Anderson Estiduar Blandón ALvarez</h2>    
    </nav>
</header>


<!-- Main (About me, Projects, Skills, Contact ) -->
<main>

    <!-- About me section -->
    <section class="About-section">
        <div class="about-text">
            <h2>About me</h2>
            <p>I’m a software developer with strong skills in web development.
            I work with HTML and CSS to build responsive and user-friendly interfaces. 
            I use JavaScript to add interactivity and dynamic features to websites. 
            On the backend, I work with PHP to handle server-side logic and database connections.</p>
        </div>  
    </section>

<!-- Projects section
    <section class="Projects">
        <div class="Projects-text">
            <h2>Projects</h2>
        </div>
    </section> -->

<!-- Skills section -->
    <section class="Skills">
        <div class="Skills-text">
            <h2>My skills</h2>
        </div>
    </section>

    <!-- Skills contact
    <section class="Contact">
        <div class="Contact-text">
            <h2>Contact me</h2>
        </div>
    </section> -->


</main>






<!-- Footer section -->
<footer class="footer">

    &copy; <p>Anderson Estiduar Blandón - Riwi </p>
    <p>2025</p>
</footer>
   
</body>
</html>


/*Reset*/

html{
    scroll-behavior: unset;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body, html{
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    line-height: 1.6;
    color: #000;
}


header{
    padding: 5% 0;
    position: relative;
    text-align: center;   
}

header h1{
    text-transform: uppercase;
    letter-spacing: 30px;
    font-weight: bold;
    color: #000;
}

/* Hover effect on main title */
header h1:hover {
    color: #ffffff98;
    text-transform: uppercase;
    letter-spacing: 40px;

}

#video-background {
    position: fixed !important; /* Fullscreen fixed video */
    top: 50%;
    left: 50%;
    min-width: 100%;
    min-height: 100%;
    width: auto;
    height: auto;
    z-index: -1;
    transform: translate(-50%, -50%);
    object-fit: cover;
    opacity: 0.7;
}

/* Logo container layout */
.logo-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px 0;
}

/* Logo image size */
#logo {
    width: 270px;
    height: auto;
}

h2 {
    margin-top: 20px;
    text-transform: uppercase;
    letter-spacing: 5px;
    text-align: center;
    font-size: 1.5rem;
    margin-bottom: 20px;
}



1. Define una grid general para 
main {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    padding: 20px;
}
✅ 2. Usa grid para las secciones principales
.About-section,
.Skills {
    display: grid;
    grid-template-columns: 1fr;
    align-items: center;
    justify-items: center;
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.8); /* para mejor legibilidad sobre el video */
    border-radius: 10px;
}
✅ 3. Haz responsive el header y el nav
header {
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
    padding: 40px 20px;
    background-color: rgba(255, 255, 255, 0.6);
    border-bottom: 2px solid #000;
}

nav ul {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    gap: 10px;
    list-style: none;
    padding: 0;
}

nav ul li a {
    text-decoration: none;
    color: #000;
    font-weight: bold;
    padding: 10px;
    display: block;
    text-align: center;
    background-color: rgba(255, 255, 255, 0.4);
    border-radius: 8px;
    transition: background-color 0.3s;
}

nav ul li a:hover {
    background-color: #000;
    color: #fff;
}
✅ 4. Haz el video de fondo flexible y accesible
Tu código ya está bien para esto, solo asegúrate de que la propiedad object-fit: cover; esté aplicada como ya lo hiciste.

✅ 5. Haz el footer responsive y centrado
.footer {
    display: grid;
    grid-template-columns: 1fr;
    text-align: center;
    padding: 20px;
    background-color: rgba(255,255,255,0.7);
    font-size: 1rem;
    margin-top: 30px;
}
✅ 6. Media Queries para pantallas pequeñas
Agrega esto al final del archivo CSS:

@media (max-width: 768px) {
    header h1 {
        font-size: 1.8rem;
        letter-spacing: 10px;
    }

    nav ul {
        grid-template-columns: 1fr;
    }

    .about-text, .Skills-text {
        text-align: center;
        padding: 10px;
    }

    h2 {
        font-size: 1.2rem;
        letter-spacing: 2px;
    }
}

@media (max-width: 480px) {
    header h1 {
        font-size: 1.4rem;
        letter-spacing: 5px;
    }

    nav ul li a {
        font-size: 0.9rem;
        padding: 8px;
    }

    .logo-container img {
        width: 180px;
    }
}
🧩 Nota importante
Tu imagen del logo tiene este selector:

#logo {
    width: 270px;
}
Pero en el HTML no tienes el atributo id="logo" en el <img>, por eso no se aplica. Cámbialo así:

<img src="Resources/Logo-removebg-preview.png" alt="logo-portfolio" id="logo">
¿Q
