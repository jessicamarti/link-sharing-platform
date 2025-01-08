<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Link Sharing Platform</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #F8F8F8;
            color: #333;
        }
        header {
            background-color: #171717;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #FFFFFF;
            border-bottom: 2px solid #171717;
        }
        nav a {
            text-decoration: none;
            color: #171717;
            padding: 1rem;
        }
        nav a:hover {
            background-color: #E0D1E3;
        }
        .container {
            max-width: 1200px;
            margin: auto;
            padding: 1rem;
        }
        .featured-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1rem;
        }
        .card {
            background-color: #FFFFFF;
            padding: 1rem;
            border: 1px solid #E0E0E0;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        footer {
            background-color: #171717;
            color: white;
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
        }
        .category-list, .submission-form {
            margin: 2rem 0;
        }
        input[type="text"], input[type="url"], textarea {
            width: 100%;
            padding: 0.5rem;
            margin: 0.5rem 0;
            border: 1px solid #CCC;
            border-radius: 4px;
        }
        button {
            background-color: #171717;
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #A97AB1;
        }
    </style>
</head>
<body>

<header>
    <h1>Link Sharing Platform</h1>
    <p>Discover and share categorized links!</p>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#categories">Categories</a>
    <a href="#contact">Contact</a>
</nav>

<main class="container">
    <!-- Homepage with Featured Links -->
    <section id="home">
        <h2>Featured Links</h2>
        <div class="featured-links">
            <div class="card">
                <h3>Example Link 1</h3>
                <p>Description for the first link.</p>
                <a href="#" target="_blank">Visit Link</a>
            </div>
            <div class="card">
                <h3>Example Link 2</h3>
                <p>Description for the second link.</p>
                <a href="#" target="_blank">Visit Link</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <p>Welcome to my link sharing platform! Here, users can discover and share valuable links across various categories.</p>
    </section>

    <!-- Portfolio Page -->
    <section id="portfolio">
        <h2>Portfolio</h2>
        <p>Check out some of my curated projects and achievements!</p>
        <div class="featured-links">
            <div class="card">
                <h3>Portfolio Item 1</h3>
                <p>Description of the project.</p>
            </div>
        </div>
    </section>

    <!-- Categories Section -->
    <section id="categories">
        <h2>Categories</h2>
        <ul class="category-list">
            <li>Category 1</li>
            <li>Category 2</li>
            <li>Category 3</li>
        </ul>
    </section>

    <!-- Search Bar -->
    <section>
        <h2>Search Links</h2>
        <input type="text" placeholder="Search..." id="searchBar">
        <button onclick="searchLinks()">Search</button>
    </section>

    <!-- User Submission Form -->
    <section class="submission-form">
        <h2>Submit a Link</h2>
        <form id="submissionForm">
            <label for="linkTitle">Link Title:</label>
            <input type="text" id="linkTitle" required>

            <label for="linkURL">Link URL:</label>
            <input type="url" id="linkURL" required>

            <label for="linkDescription">Description:</label>
            <textarea id="linkDescription" rows="4"></textarea>

            <button type="submit">Submit</button>
        </form>
    </section>
</main>

<footer>
    <p>&copy; 2025 Link Sharing Platform. All rights reserved.</p>
</footer>

<script>
    function searchLinks() {
        const query = document.getElementById('searchBar').value;
        alert(`Searching for: ${query}`);
    }

    document.getElementById('submissionForm').addEventListener('submit', function(event) {
        event.preventDefault();
        const title = document.getElementById('linkTitle').value;
        const url = document.getElementById('linkURL').value;
        const description = document.getElementById('linkDescription').value;
        alert(`Link Submitted:\nTitle: ${title}\nURL: ${url}\nDescription: ${description}`);
    });
</script>

</body>
</html>

