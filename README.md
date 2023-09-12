<!DOCTYPE html>
<html>
<head>
    <title>Product Recommendation</title>
</head>
<body>
    <h1>Welcome to our E-commerce Website</h1>
    <p>Start typing to get product recommendations:</p>
    <input type="text" id="userInput" onkeyup="getRecommendations()">
    <div id="suggestions"></div>

    <script>
        // Sample product data
        const products = [
            "Product 1",
            "Product 2",
            "Product 3",
            "Product 4",
            "Product 5",
            // Add more products here
        ];

        // Function to get product recommendations based on user input
        function getRecommendations() {
            const userInput = document.getElementById("userInput").value.toLowerCase();
            const suggestionsDiv = document.getElementById("suggestions");
            suggestionsDiv.innerHTML = "";

            // Filter products based on user input
            const filteredProducts = products.filter(product => product.toLowerCase().includes(userInput));

            // Display the filtered products as suggestions
            filteredProducts.forEach(product => {
                const suggestionItem = document.createElement("div");
                suggestionItem.textContent = product;
                suggestionsDiv.appendChild(suggestionItem);
            });
        }
    </script>
</body>
</html>
