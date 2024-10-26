<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inventory Management System</title>
    <style>
        /* Base styles - modify font-size here to change the base size for the entire app */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
            /* Modify base font size here */
            font-size: 16px;
        }

        body {
            /* Modify overall page padding here */
            padding: 20px;
            background-color: #f5f5f5;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header styles - modify padding and font-size for the title */
        .header {
            background-color: #2c3e50;
            color: white;
            /* Modify header padding here */
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .header h1 {
            /* Modify title font size here */
            font-size: 24px;
        }

        /* Card grid layout - modify gaps between cards here */
        .operations {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            /* Modify space between operation cards here */
            gap: 20px;
            margin-bottom: 20px;
        }

        /* Card styles - modify internal spacing here */
        .card {
            background-color: white;
            /* Modify card internal padding here */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .card h2 {
            /* Modify card title font size here */
            font-size: 20px;
            /* Modify space below card titles here */
            margin-bottom: 15px;
        }

        /* Form group styles - modify spacing between form elements */
        .form-group {
            /* Modify space between form groups here */
            margin-bottom: 15px;
        }

        /* Label styles - modify label spacing and size */
        label {
            display: block;
            /* Modify space below labels here */
            margin-bottom: 5px;
            color: #333;
            /* Modify label font size here */
            font-size: 14px;
        }

        /* Input and select styles - modify input appearance */
        input,
        select {
            width: 100%;
            /* Modify input padding here */
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            /* Modify space below inputs here */
            margin-bottom: 10px;
            /* Modify input text size here */
            font-size: 14px;
        }

        /* Button styles - modify button appearance */
        button {
            background-color: #3498db;
            color: white;
            /* Modify button padding here */
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
            /* Modify button text size here */
            font-size: 14px;
        }

        button:hover {
            background-color: #2980b9;
        }

        /* Table styles - modify table appearance */
        table {
            width: 100%;
            border-collapse: collapse;
            background-color: white;
            /* Modify space above tables here */
            margin-top: 20px;
        }

        /* Table cell styles - modify cell spacing and text size */
        th,
        td {
            /* Modify cell padding here */
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
            /* Modify table text size here */
            font-size: 14px;
        }

        th {
            background-color: #2c3e50;
            color: white;
        }

        tr:hover {
            background-color: #f5f5f5;
        }

        /* History section styles */
        .history {
            /* Modify space above history section here */
            margin-top: 20px;
        }

        /* Message styles */
        .error {
            color: #e74c3c;
            margin-top: 5px;
        }

        .success {
            color: #27ae60;
            margin-top: 5px;
        }

        /* Search type dropdown styles */
        .search-type {
            /* Modify space below search type section here */
            margin-bottom: 15px;
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="header">
            <h1>Inventory Management System</h1>
        </div>

        <div class="operations">
            <div class="card">
                <h2>Add New Item</h2>
                <form id="addItemForm">
                    <div class="form-group">
                        <label for="skuCode">SKU Code:</label>
                        <input type="text" id="skuCode" required>
                    </div>
                    <div class="form-group">
                        <label for="itemName">Item Name:</label>
                        <input type="text" id="itemName" required>
                    </div>
                    <div class="form-group">
                        <label for="initialStock">Initial Stock:</label>
                        <input type="number" id="initialStock" required min="0">
                    </div>
                    <button type="submit">Add Item</button>
                </form>
            </div>

            <div class="card">
                <h2>Stock Operations</h2>
                <form id="stockOperationForm">
                    <div class="form-group">
                        <label for="searchType">Search by:</label>
                        <select id="searchType">
                            <option value="sku">SKU Code</option>
                            <option value="name">Item Name</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="itemSelector">Select Item:</label>
                        <select id="itemSelector" required></select>
                    </div>
                    <div class="form-group">
                        <label for="quantity">Quantity:</label>
                        <input type="number" id="quantity" required min="1">
                    </div>
                    <button type="button" onclick="handleStockIn()">Stock In</button>
                    <button type="button" onclick="handleStockOut()"
                        style="background-color: #e74c3c; margin-top: 10px;">Stock Out</button>
                </form>
            </div>
        </div>

        <div class="card">
            <h2>Current Inventory</h2>
            <table id="inventoryTable">
                <thead>
                    <tr>
                        <th>SKU Code</th>
                        <th>Name</th>
                        <th>Stock</th>
                    </tr>
                </thead>
                <tbody id="inventoryBody"></tbody>
            </table>
        </div>

        <div class="card history">
            <h2>Transaction History</h2>
            <table id="historyTable">
                <thead>
                    <tr>
                        <th>Date</th>
                        <th>Type</th>
                        <th>SKU Code</th>
                        <th>Item Name</th>
                        <th>Quantity</th>
                    </tr>
                </thead>
                <tbody id="historyBody"></tbody>
            </table>
        </div>
    </div>

    <script>
        // Initialize inventory data structure
        let inventory = {};
        let transactionHistory = [];

        // Load data from localStorage if available
        function loadData() {
            const savedInventory = localStorage.getItem('inventory');
            const savedHistory = localStorage.getItem('transactionHistory');
            if (savedInventory) inventory = JSON.parse(savedInventory);
            if (savedHistory) transactionHistory = JSON.parse(savedHistory);
            updateTables();
            updateItemSelector();
        }

        // Save data to localStorage
        function saveData() {
            localStorage.setItem('inventory', JSON.stringify(inventory));
            localStorage.setItem('transactionHistory', JSON.stringify(transactionHistory));
        }

        // Update dropdown based on search type
        function updateItemSelector() {
            const selector = document.getElementById('itemSelector');
            const searchType = document.getElementById('searchType').value;
            selector.innerHTML = '';

            const defaultOption = document.createElement('option');
            defaultOption.value = '';
            defaultOption.textContent = '-- Select --';
            selector.appendChild(defaultOption);

            if (searchType === 'sku') {
                // Sort by SKU
                Object.entries(inventory)
                    .sort((a, b) => a[0].localeCompare(b[0]))
                    .forEach(([sku, item]) => {
                        const option = document.createElement('option');
                        option.value = sku;
                        option.textContent = `${sku} - ${item.name}`;
                        selector.appendChild(option);
                    });
            } else {
                // Sort by name
                Object.entries(inventory)
                    .sort((a, b) => a[1].name.localeCompare(b[1].name))
                    .forEach(([sku, item]) => {
                        const option = document.createElement('option');
                        option.value = sku;
                        option.textContent = `${item.name} - ${sku}`;
                        selector.appendChild(option);
                    });
            }
        }

        // Add event listener for search type dropdown
        document.getElementById('searchType').addEventListener('change', updateItemSelector);

        // Add new item
        document.getElementById('addItemForm').addEventListener('submit', function (e) {
            e.preventDefault();
            const code = document.getElementById('skuCode').value;
            const name = document.getElementById('itemName').value;
            const stock = parseInt(document.getElementById('initialStock').value);

            if (inventory[code]) {
                alert('SKU code already exists!');
                return;
            }

            inventory[code] = {
                name: name,
                stock: stock
            };

            addToHistory('INIT', code, stock);
            saveData();
            updateTables();
            updateItemSelector();
            this.reset();
        });

        // Handle stock in
        function handleStockIn() {
            const code = document.getElementById('itemSelector').value;
            const quantity = parseInt(document.getElementById('quantity').value);

            if (!code) {
                alert('Please select an item!');
                return;
            }

            inventory[code].stock += quantity;
            addToHistory('IN', code, quantity);
            saveData();
            updateTables();
            document.getElementById('stockOperationForm').reset();
            updateItemSelector();
        }

        // Handle stock out
        function handleStockOut() {
            const code = document.getElementById('itemSelector').value;
            const quantity = parseInt(document.getElementById('quantity').value);

            if (!code) {
                alert('Please select an item!');
                return;
            }

            if (inventory[code].stock < quantity) {
                alert('Insufficient stock!');
                return;
            }

            inventory[code].stock -= quantity;
            addToHistory('OUT', code, quantity);
            saveData();
            updateTables();
            document.getElementById('stockOperationForm').reset();
            updateItemSelector();
        }

        // Add transaction to history
        function addToHistory(type, code, quantity) {
            transactionHistory.push({
                date: new Date().toLocaleString(),
                type: type,
                itemCode: code,
                itemName: inventory[code].name,
                quantity: quantity
            });
        }

        // Update tables
        function updateTables() {
            // Update inventory table
            const inventoryBody = document.getElementById('inventoryBody');
            inventoryBody.innerHTML = '';

            for (const [code, item] of Object.entries(inventory)) {
                const row = inventoryBody.insertRow();
                row.insertCell(0).textContent = code;
                row.insertCell(1).textContent = item.name;
                row.insertCell(2).textContent = item.stock;
            }

            // Update history table
            const historyBody = document.getElementById('historyBody');
            historyBody.innerHTML = '';

            for (const transaction of transactionHistory.reverse()) {
                const row = historyBody.insertRow();
                row.insertCell(0).textContent = transaction.date;
                row.insertCell(1).textContent = transaction.type;
                row.insertCell(2).textContent = transaction.itemCode;
                row.insertCell(3).textContent = transaction.itemName;
                row.insertCell(4).textContent = transaction.quantity;
            }
        }

        // Load data when page loads
        loadData();
    </script>
</body>

</html>
