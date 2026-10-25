
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Responsive Photo Gallery</title>
<style>
* { box-sizing: border-box; }

body {
    margin: 0;
    font-family: Arial;
}

/* Mobile First */
header, footer {
    background: navy;
    color: white;
    text-align: center;
    padding: 20px;
}
main { padding: 15px; }

.gallery {
    display: grid;
    grid-template-columns: 1fr;
    gap: 15px;
}
.card {
    background: #eee;
    padding: 10px;
    border-radius: 10px;
    min-width: 0;
    overflow-wrap: anywhere;
}
.card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-radius: 8px;
}

/* Tablet */
@media (min-width: 600px) {
    .gallery {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
    main { padding: 25px; }
}

/* Desktop */
@media (min-width: 1024px) {
    .gallery {
        grid-template-columns: repeat(3, minmax(0, 1fr));
    }
    main { padding: 40px; }
}
</style>
</head>
<body>
<header>
    <h1>My Photo Gallery</h1>
    <p>Responsive Nature Collection</p>
</header>

<main>
    <h2>Gallery</h2>
    <div class="gallery">
        <div class="card"><img src="images/1.jpg" alt="Mountains"><h3>Mountains</h3></div>
        <div class="card"><img src="images/2.jpg" alt="Forest"><h3>Forest</h3></div>
        <div class="card"><img src="images/3.jpg" alt="Beach"><h3>Beach</h3></div>
        <div class="card"><img src="images/4.jpg" alt="Sunset"><h3>Sunset</h3></div>
        <div class="card"><img src="images/5.jpg" alt="River"><h3>River</h3></div>
        <div class="card"><img src="images/6.jpg" alt="Flowers"><h3>Flowers</h3></div>
    </div>
</main>

<footer>
    <p>&copy; 2026 Prasoon Anand</p>
</footer>
</body>
</html>
