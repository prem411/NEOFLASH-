<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NEO FLASH - Team Balance Tracker</title>
    <style>
        :root {
            --primary: #ff4757;
            --bg: #0f0f13;
            --card-bg: #1a1a24;
            --text: #ffffff;
            --accent: #2ed573;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            padding: 20px 0;
            border-bottom: 2px solid #2f3542;
            margin-bottom: 30px;
        }

        header h1 {
            color: var(--primary);
            letter-spacing: 2px;
            margin: 0;
        }

        .summary-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .card {
            background: var(--card-bg);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid var(--primary);
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }

        .card.green { border-left-color: var(--accent); }
        .card.yellow { border-left-color: #ffa502; }

        .card h3 {
            margin: 0 0 10px 0;
            font-size: 0.9em;
            color: #a4b0be;
        }

        .card .amount {
            font-size: 1.8em;
            font-weight: bold;
        }

        .form-section {
            background: var(--card-bg);
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .form-section h2 {
            margin-top: 0;
            font-size: 1.2em;
            color: var(--primary);
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }

        input, select, button {
            width: 100%;
            padding: 12px;
            background: #2f3542;
            border: 1px solid #57606f;
            color: #fff;
            border-radius: 6px;
            box-sizing: border-box;
        }

        button.btn-add {
            background: var(--primary);
            border: none;
            cursor: pointer;
            font-weight: bold;
            grid-column: 1 / -1;
            margin-top: 10px;
        }

        button.btn-add:hover {
            opacity: 0.9;
        }

        button.btn-export {
            background: var(--accent);
            color: #000;
            font-weight: bold;
            border: none;
            cursor: pointer;
            margin-bottom: 20px;
            float: right;
            width: auto;
            padding: 10px 20px;
        }

        .table-section {
            background: var(--card-bg);
            padding: 20px;
            border-radius: 10px;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            text-align: left;
        }

        th, td {
            padding: 12px;
            border-bottom: 1px solid #2f3542;
        }

        th {
            background: #2f3542;
            color: #ffa502;
        }

        .badge-income { color: var(--accent); font-weight: bold; }
        .badge-expense { color: var(--primary); font-weight: bold; }
        .badge-loan { color: #eccc68; font-weight: bold; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>NEO FLASH BALANCING SYSTEM</h1>
        <p>Official Team Expense & Tournament Ledger</p>
    </header>

    <!-- Total Summary Cards -->
    <div class="summary-cards">
        <div class="card green">
            <h3>মোট আয় / Prize</h3>
            <div class="amount" id="totalIncome">৳ 0</div>
        </div>
        <div class="card">
            <h3>মোট খরচ (Entry/GFX)</h3>
            <div class="amount" id="totalExpense">৳ 0</div>
        </div>
        <div class="card yellow">
            <h3>টিম লেনদেন (Net Loan)</h3>
            <div class="amount" id="totalLoan">৳ 0</div>
        </div>
        <div class="card green">
            <h3>বর্তমান নেট ব্যালেন্স</h3>
            <div class="amount" id="netBalance">৳ 0</div>
        </div>
    </div>

    <!-- New Entry Form -->
    <div class="form-section">
        <h2>নতুন হিসেব যোগ করুন (অপরিবর্তনযোগ্য)</h2>
        <div class="form-grid">
            <input type="date" id="date">
            <input type="text" id="title" placeholder="টুর্নামেন্ট বা বিষয় (e.g. Mangrove Pro Series)">
            <select id="type">
                <option value="Expense - Entry">Entry Fee (খরচ)</option>
                <option value="Expense - GFX">GFX / Designer Fee (খরচ)</option>
                <option value="Income - Prize">Prize Money / Income (আয়)</option>
                <option value="Lend - Out">অন্য টিমকে দেয়া হলো (Lend)</option>
                <option value="Lend - In">অন্য টিমের কাছ থেকে নেওয়া হলো (Borrow)</option>
            </select>
            <input type="number" id="amount" placeholder="টাকার পরিমাণ (BDT)">
            <input type="text" id="note" placeholder="নোট/বিস্তারিত (e.g. Paid via bKash)">
            <button class="btn-add" onclick="addTransaction()">হিসেব এন্ট্রি দিন</button>
        </div>
    </div>

    <!-- Export & Table List -->
    <div style="clear: both;">
        <button class="btn-export" onclick="exportToCSV()">Google Sheets / CSV-তে এক্সপোর্ট</button>
        <h2 style="display:inline-block;">সব লেনদেনের তালিকা</h2>
    </div>

    <div class="table-section">
        <table>
            <thead>
                <tr>
                    <th>তারিখ</th>
                    <th>বিষয় / টুর্নামেন্ট</th>
                    <th>ধরণ</th>
                    <th>টাকা (BDT)</th>
                    <th>নোট</th>
                </tr>
            </thead>
            <tbody id="transactionList">
                <!-- Transactions will load here -->
            </tbody>
        </table>
    </div>
</div>

<script>
    // Load stored transactions or initialize empty array
    let transactions = JSON.parse(localStorage.getItem('neo_flash_ledger')) || [];

    // Set today's date by default
    document.getElementById('date').valueAsDate = new Date();

    function renderTable() {
        const list = document.getElementById('transactionList');
        list.innerHTML = '';

        let totalIncome = 0;
        let totalExpense = 0;
        let totalLoan = 0;

        // Render in reverse order so newest shows on top
        transactions.slice().reverse().forEach(item => {
            const tr = document.createElement('tr');
            
            let badgeClass = 'badge-expense';
            if (item.type.includes('Income')) badgeClass = 'badge-income';
            if (item.type.includes('Lend')) badgeClass = 'badge-loan';

            tr.innerHTML = `
                <td>${item.date}</td>
                <td><strong>${item.title}</strong></td>
                <td><span class="${badgeClass}">${item.type}</span></td>
                <td>৳ ${item.amount}</td>
                <td>${item.note || '-'}</td>
            `;
            list.appendChild(tr);

            // Calculation
            const amt = parseFloat(item.amount);
            if (item.type.includes('Income')) {
                totalIncome += amt;
            } else if (item.type.includes('Expense')) {
                totalExpense += amt;
            } else if (item.type === 'Lend - Out') {
                totalLoan += amt; // Positive means team gets money back
            } else if (item.type === 'Lend - In') {
                totalLoan -= amt; // Negative means team owes money
            }
        });

        document.getElementById('totalIncome').innerText = '৳ ' + totalIncome;
        document.getElementById('totalExpense').innerText = '৳ ' + totalExpense;
        document.getElementById('totalLoan').innerText = '৳ ' + totalLoan;
        document.getElementById('netBalance').innerText = '৳ ' + (totalIncome - totalExpense + totalLoan);
    }

    function addTransaction() {
        const date = document.getElementById('date').value;
        const title = document.getElementById('title').value;
        const type = document.getElementById('type').value;
        const amount = document.getElementById('amount').value;
        const note = document.getElementById('note').value;

        if (!date || !title || !amount) {
            alert('অনুগ্রহ করে তারিখ, বিষয় এবং টাকার পরিমাণ লিখুন!');
            return;
        }

        const newEntry = {
            id: Date.now(),
            date,
            title,
            type,
            amount: parseFloat(amount),
            note
        };

        transactions.push(newEntry);
        localStorage.setItem('neo_flash_ledger', JSON.stringify(transactions));
        
        // Reset Inputs
        document.getElementById('title').value = '';
        document.getElementById('amount').value = '';
        document.getElementById('note').value = '';

        renderTable();
        alert('হিসেব সফলভাবে যুক্ত হয়েছে! এটি আর পরিবর্তন বা ডিলিট করা যাবে না।');
    }

    function exportToCSV() {
        if (transactions.length === 0) {
            alert('এক্সপোর্ট করার মতো কোনো ডেটা নেই!');
            return;
        }

        let csvContent = "data:text/csv;charset=utf-8,";
        csvContent += "Date,Title,Type,Amount (BDT),Note\n";

        transactions.forEach(row => {
            csvContent += `"${row.date}","${row.title}","${row.type}","${row.amount}","${row.note}"\n`;
        });

        const encodedUri = encodeURI(csvContent);
        const link = document.createElement("a");
        link.setAttribute("href", encodedUri);
        link.setAttribute("download", `NEO_FLASH_Financial_Report_${new Date().toISOString().slice(0,7)}.csv`);
        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
    }

    // Initial Render
    renderTable();
</script>

</body>
</html>
