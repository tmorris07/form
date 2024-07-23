<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SSD Purchase Form</title>
</head>
<body>
    <div class="form-container">
        <form id="ssdForm">
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="text" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="quantity">Quantity of SSDs:</label>
                <input type="number" id="quantity" name="quantity" required>
            </div>
            <button type="button" onclick="calculateTotal()">Calculate Total</button>
            <div class="total" id="total"></div>
        </form>
    </div>
    <script>
        function calculateTotal() {
            const quantity = document.getElementById('quantity').value;
            const pricePerSSD = 100; // Price per SSD
            const total = quantity * pricePerSSD;
            document.getElementById('total').textContent = 'Total: $' + total;
        }
    </script>
</body>
</html>
