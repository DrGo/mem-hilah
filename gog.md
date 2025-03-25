2. funeral.html (Funeral Stream)

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Funeral Stream - Remembering Hilah Lende Simmons</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Funeral Service Stream</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="messages.html">Leave a Message</a></li>
                <li><a href="photos.html">Photo Gallery</a></li>
                <li><a href="about.html">About Hilah</a></li>
            </ul>
        </nav>
    </header>
    <main class="container">
        <section class="video-embed">
            <h2>Live Stream</h2>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/YOUR_YOUTUBE_VIDEO_ID" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <p class="note">The live stream will begin at [Time of Memorial Service] on [Date of Memorial Service].</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 Remembering Hilah Lende Simmons</p>
    </footer>
</body>
</html>
3. messages.html (Leave Messages)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Leave a Message - Remembering Hilah Lende Simmons</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Leave a Message for Hilah</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="funeral.html">Funeral Stream</a></li>
                <li><a href="photos.html">Photo Gallery</a></li>
                <li><a href="about.html">About Hilah</a></li>
            </ul>
        </nav>
    </header>
    <main class="container">
        <section class="message-form">
            <h2>Share Your Thoughts</h2>
            <p>Your messages will be collected and a selection may be displayed on this page.</p>
            <form id="messageForm">
                <label for="name">Your Name:</label><br>
                <input type="text" id="name" name="name" required><br>
                <label for="message">Your Message:</label><br>
                <textarea id="message" name="message" rows="5" required></textarea><br><br>
                <button type="submit">Submit Message</button>
            </form>
        </section>

        <section class="messages-display">
            <h2>Messages</h2>
            <div id="displayedMessages">
                <p>Loading messages...</p>
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 Remembering Hilah Lende Simmons</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const form = document.getElementById('messageForm');
            const displayedMessages = document.getElementById('displayedMessages');

            form.addEventListener('submit', function(event) {
                event.preventDefault();
                const name = document.getElementById('name').value;
                const message = document.getElementById('message').value;

                // Instructions for Google Sheets integration (explained below)
                alert('Your message has been submitted. Thank you.');
                form.reset();
            });

            // Function to fetch and display selected messages (explained below)
            function fetchAndDisplayMessages() {
                // This would involve fetching data from your Google Sheet
                // and updating the displayedMessages div.
                // For a purely static site with minimal dependencies,
                // you might need to manually update this section with a few selected messages.

                // Example of manually adding messages:
                displayedMessages.innerHTML = `
                    <div class="message">
                        <p class="author">From [Name of Person 1]</p>
                        <p>"[Selected Message 1]"</p>
                    </div>
                    <div class="message">
                        <p class="author">From [Name of Person 2]</p>
                        <p>"[Selected Message 2]"</p>
                    </div>
                    // Add more messages as needed
                `;
            }

            fetchAndDisplayMessages(); // Load initial messages
        });
    </script>
</body>
</html>
4. photos.html (Photo Gallery)

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery - Remembering Hilah Lende Simmons</title>
    <link rel="stylesheet" href="style.css">
    <style>
        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .gallery img {
            width: calc(33.33% - 10px); /* Adjust for different screen sizes */
            height: auto;
            object-fit: cover;
            border-radius: 5px;
        }

        @media (max-width: 768px) {
            .gallery img {
                width: calc(50% - 10px);
            }
        }

        @media (max-width: 480px) {
            .gallery img {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Photo Gallery</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="funeral.html">Funeral Stream</a></li>
                <li><a href="messages.html">Leave a Message</a></li>
                <li><a href="about.html">About Hilah</a></li>
            </ul>
        </nav>
    </header>
    <main class="container">
        <section class="gallery">
            <img src="images/hilah_photo1.jpg" alt="Photo of Hilah">
            <img src="images/hilah_photo2.jpg" alt="Photo of Hilah">
            <img src="images/hilah_photo3.jpg" alt="Photo of Hilah">
            <img src="images/hilah_photo4.jpg" alt="Photo of Hilah">
            <img src="images/hilah_photo5.jpg" alt="Photo of Hilah">
            </section>
    </main>
    <footer>
        <p>&copy; 2025 Remembering Hilah Lende Simmons</p>
    </footer>
</body>
</html>
5. about.html (About Hilah)

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Hilah - Remembering Hilah Lende Simmons</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>About Hilah Lende Simmons</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="funeral.html">Funeral Stream</a></li>
                <li><a href="messages.html">Leave a Message</a></li>
                <li><a href="photos.html">Photo Gallery</a></li>
            </ul>
        </nav>
    </header>
    <main class="container">
        <section class="about-content">
            <div class="about-hero">
                <img src="images/hilah_about.jpg" alt="Hilah Lende Simmons" class="profile-image">
            </div>
            <p>Hilah Lende Simmons was born on [Date of Birth] and passed away on [Date of Passing]. [Insert a brief outline of her life here - e.g., key achievements, passions, family, etc.].</p>

            <h2>Writings</h2>
            <ul>
                <li><a href="[Link to Writing 1]">Title of Writing 1</a></li>
                <li><a href="[Link to Writing 2]">Title of Writing 2</a></li>
                </ul>

            <h2>Drawings</h2>
            <p>View some of Hilah's drawings:</p>
            <div class="drawings-gallery">
                <img src="images/hilah_drawing1.jpg" alt="Drawing by Hilah">
                <img src="images/hilah_drawing2.jpg" alt="Drawing by Hilah">
                </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 Remembering Hilah Lende Simmons</p>
    </footer>
</body>
</html>
6. style.css (Basic Styling)

CSS
body {
    font-family: sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #333;
    color: white;
    padding: 1em 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
    text-align: center;
    margin-top: 1em;
}

nav ul li {
    display: inline;
    margin: 0 1em;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

.container {
    max-width: 960px;
    margin: 20px auto;
    padding: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.hero {
    text-align: center;
    margin-bottom: 20px;
}

.profile-image {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 10px;
}

.name-dates {
    font-size: 1.2em;
    color: #555;
}

.memorial-details {
    text-align: center;
    margin-bottom: 20px;
}

.memorial-details h2 {
    color: #333;
}

.main-nav ul {
    text-align: center;
    margin-top: 20px;
}

.main-nav ul li {
    display: inline;
    margin: 0 15px;
}

.main-nav ul li a {
    color: #333;
    text-decoration: none;
    padding: 8px 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.main-nav ul li a:hover {
    background-color: #eee;
}

.video-embed {
    text-align: center;
    margin-top: 20px;
}

.video-embed iframe {
    max-width: 100%; /* Make iframe responsive */
}

.note {
    font-size: 0.9em;
    color: #777;
    margin-top: 10px;
}

.message-form label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

.message-form input[type="text"],
.message-form textarea {
    width: calc(100% - 12px);
    padding: 8px;
    margin-bottom: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-sizing: border-box;
}

.message-form button {
    background-color: #5cb85c;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
}

.message-form button:hover {
    background-color: #4cae4c;
}

.messages-display {
    margin-top: 30px;
    border-top: 1px solid #eee;
    padding-top: 20px;
}

.messages-display h2 {
    margin-bottom: 15px;
}

.message {
    border: 1px solid #ddd;
    padding: 15px;
    margin-bottom: 10px;
    border-radius: 5px;
    background-color: #f9f9f9;
}

.message .author {
    font-weight: bold;
    margin-bottom: 5px;
    color: #555;
}

.about-content {
    line-height: 1.6;
}

.about-hero {
    text-align: center;
    margin-bottom: 20px;
}

.drawings-gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
}

.drawings-gallery img {
    max-width: 200px;
    height: auto;
    border-radius: 5px;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
}

footer {
    text-align: center;
    padding: 1em 0;
    background-color: #333;
    color: white;
    position: static;
    bottom: 0;
    width: 100%;
    margin-top: 20px;
}

/* Mobile responsiveness */
@media (max-width: 600px) {
    .container {
        padding: 15px;
    }

    nav ul li {
        display: block;
        margin: 0.5em 0;
    }

    .main-nav ul li {
        display: block;
        margin: 10px 0;
    }

    .hero .profile-image {
        width: 100px;
        height: 100px;
    }
}
