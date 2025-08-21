---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Hello! My Name is Perry Say and I was borned and Raised in San Diego, California.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - forever"},
    
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Passions & Hobbies

Here is what I do in my free time:

- 🏀 I am an Avid Fan of Basketball and Enjoy Playing Basketball during the Weekend
- 🎮 I enjoy playing videogames such as Minecraft and Roblox with Friends during my Free Time
- 📚 I also enjoy reading lightnovels and ebooks in my freetime (Mainly Action, Fantasy, and Mystery)
- 🏊 During the summer, I like spending my time swimming the pool rather than out in the hot sun.
- 🎵 I enjoy listening to music while im working on homework or walking to class, with some of my favorite artists being Malcolm Todd, Bruno Mars, and Michael Jackson. 
- 🍔 When Im out with family, I enjoy trying all sorts of food, whether it be Mexican, Japanese, Chinese, or even trying Fusions of these foods.

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="https://finnsbeachclub.com/wp-content/uploads/2024/09/basketball-court-ball-and-sports-match-or-competi-2023-11-27-04-58-17-utc.jpg" alt="Image 1">
  <img src="https://images.alphacoders.com/246/246223.jpg" alt="Image 2">
  <img src="https://store-images.s-microsoft.com/image/apps.47252.13510798883386282.a1e5df65-8dd7-427c-9da9-506afa37b254.f4132380-deee-4518-8bbd-2a9b540046f3" alt="Image 3">
  <img src="https://m.media-amazon.com/images/I/515fsT6ty4L._UF1000,1000_QL80_.jpg" alt="Image 4">
  <img src="https://images.squarespace-cdn.com/content/v1/551b7247e4b04e2cba1e41ce/1696306155257-93OF7KRMDCU89XY3BR1G/image-asset.jpeg" alt="Image 5">
  <img src="https://encrypted-tbn0.gstatic.com/images q=tbn:ANd9GcR4LL-l9Cg2k7Mc2v4C3kRapvLBDXvUop4MECSqxf_PS8OKoPW6L63BU-_99oscOyLhp1jhB5OhonWR2_tygk896w" alt="Image 6">
  <img src="https://thehintofrosemary.com/wp-content/uploads/2020/02/ramen-cover-scaled.jpg" alt="Image 7">
</div>
