<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Search and Display</title>
    <style>
        /* Basic styling for demonstration */
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            max-width: 800px;
            margin: auto;
            text-align: center;
        }
        .search-form {
            margin-bottom: 20px;
        }
        .image-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            grid-gap: 10px;
        }
        .image-item {
            text-align: center;
        }
        .image-item img {
            max-width: 100%;
            max-height: 200px;
            object-fit: cover;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Image Search and Display</h1>
        <form class="search-form" onsubmit="searchImages(event)">
            <input type="text" id="searchInput" placeholder="Enter search term">
            <button type="submit">Search</button>
        </form>
        <div class="image-grid" id="imageGrid">
            <!-- Images will be displayed here -->
        </div>
    </div>

    <script>
        function searchImages(event) {
            event.preventDefault(); // Prevent form submission

            // Get search term from input field
            let searchTerm = document.getElementById('searchInput').value;

            // Dummy function to fetch images (replace with actual API call)
            fetchImages(searchTerm);
        }

        function fetchImages(vijeth) {
            // Dummy array of image URLs (replace with actual data retrieval logic)
            let images = [
                'https://drive.google.com/file/d/13UTBbzzVf8hVmZEU0n1Y2NmjcIIU1mOe/view?usp=drive_link',
                'https://via.placeholder.com/400',
                'https://via.placeholder.com/500'
            ];

            // Display images on the UI
            displayImages(images);
        }

        function displayImages(images) {
            let imageGrid = document.getElementById('imageGrid');
            imageGrid.innerHTML = ''; // Clear previous images

            images.forEach(imageUrl => {
                let imageItem = document.createElement('div');
                imageItem.classList.add('image-item');

                let img = document.createElement('img');
                img.src = imageUrl;

                imageItem.appendChild(img);
                imageGrid.appendChild(imageItem);
            });
        }
    </script>
</body>
</html>


