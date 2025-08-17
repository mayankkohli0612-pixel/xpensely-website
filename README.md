<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Xpensely</title>
    <style>
a, .btn, button {
  background: #FFE600;      /* EY Yellow */
  color: #161D23;           /* EY Black */
  border: none;
  border-radius: 4px;
  font-weight: 600;
  padding: 10px 24px;
  text-decoration: none;
  cursor: pointer;
  transition: background 0.2s;
  display: inline-block;
}

a:hover, .btn:hover, button:hover {
  background: #ffd500;
  color: #161D23;
}

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body { 
            font-family: 'EYInterstate', Arial, sans-serif; 
            margin: 0; 
            padding: 0; 
            background-color: #fafafa;
            color: #2e2e38;
            line-height: 1.6;
        }
        
        header { 
            background-color: #2e2e38; 
            padding: 20px 40px; 
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        nav { 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
        }
        
        nav a { 
            margin-right: 30px; 
            text-decoration: none; 
            color: #000000;
            font-weight: 500;
            transition: color 0.3s ease;
            font-size: 16px;
        }
        
        nav a:hover { 
    color: #333333; 
} 
        }
        
        nav a:last-child { margin-right: 0; }
        
        .hero { 
            text-align: center; 
            padding: 80px 20px; 
            background: linear-gradient(135deg, #2e2e38 0%, #1a1a23 100%);
            color: #ffffff;
        }
        
        .hero h1 {
            font-size: 48px;
            font-weight: 700;
            margin-bottom: 20px;
            letter-spacing: -0.5px;
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 40px;
            color: #e0e0e0;
        }
        
        .hero a {
            display: inline-block;
            margin: 0 10px;
            padding: 12px 30px;
            background-color: #ffe600;
            color: #2e2e38;
            text-decoration: none;
            font-weight: 600;
            border-radius: 4px;
            transition: all 0.3s ease;
        }
        
        .hero a:hover {
            background-color: #ffd500;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .features { 
            padding: 60px 40px; 
            background-color: #ffffff;
        }
        
        .features h2 {
            font-size: 36px;
            color: #2e2e38;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .features > p {
            font-size: 18px;
            color: #666;
            margin-bottom: 40px;
        }
        
        .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); /* smaller boxes */
    gap: 15px; /* less space between boxes */
    padding: 10px;
}

.feature-card {
    border: 1px solid #e0e0e0;
    padding: 12px 16px; /* smaller padding inside the box */
    text-align: left; /* Align text left for better readability */
    border-radius: 8px;
    background-color: #ffffff;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.1);
    font-size: 14px; /* smaller text */
    max-width: 260px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    transition: all 0.3s ease;
    cursor: default;
}

.feature-card span {
    font-size: 24px; /* smaller emoji */
    margin-bottom: 8px;
}

.feature-card h3 {
    font-size: 16px;
    margin-bottom: 6px;
}

.feature-card p {
    margin-bottom: 10px;
    line-height: 1.3;
}

.feature-card a {
    font-size: 13px;
    padding: 6px 10px;
    background-color: #0078d4;
    color: white;
    border-radius: 4px;
    text-decoration: none;
}
.feature-card a:hover {
    background-color: #005a9e;
}

        .audit-section { 
            padding: 60px 40px; 
            background-color: #f5f5f5;
        }
        
        .audit-section > a {
            display: inline-block;
            color: #2e2e38;
            text-decoration: none;
            margin-bottom: 30px;
            font-weight: 600;
            transition: color 0.3s ease;
        }
        
        .audit-section > a:hover {
            color: #666;
        }
        
        .audit-section h2 {
            font-size: 36px;
            color: #2e2e38;
            margin-bottom: 40px;
            font-weight: 700;
        }
        
        .audit-section h3 {
            font-size: 24px;
            color: #2e2e38;
            margin: 30px 0 20px 0;
            font-weight: 600;
        }
        
        /* Filter Dropdown Styles */
        .filter-container {
            margin: 20px 0;
            position: relative;
        }
        
        .filter-dropdown {
            position: relative;
            display: inline-block;
        }
        
        .filter-btn {
            background-color: #2e2e38;
            color: #ffffff;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            font-size: 16px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }
        
        .filter-btn:hover {
            background-color: #1a1a23;
        }
        
        .filter-dropdown-content {
            display: none;
            position: absolute;
            background-color: #ffffff;
            min-width: 350px;
            max-height: 400px;
            overflow-y: auto;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            border-radius: 4px;
            z-index: 1000;
            border: 1px solid #e0e0e0;
            top: 100%;
            left: 0;
            margin-top: 5px;
        }
        
        .filter-dropdown-content.show {
            display: block;
        }
        
        .filter-header {
            padding: 15px;
            border-bottom: 1px solid #e0e0e0;
            background-color: #f8f8f8;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .filter-header h4 {
            margin: 0;
            color: #2e2e38;
            font-size: 16px;
        }
        
        .filter-actions {
            display: flex;
            gap: 10px;
        }
        
        .filter-actions button {
            background: none;
            border: none;
            color: #2e2e38;
            cursor: pointer;
            font-size: 14px;
            padding: 5px 10px;
            border-radius: 3px;
            transition: background-color 0.3s ease;
        }
        
        .filter-actions button:hover {
            background-color: #e0e0e0;
        }
        
        .filter-option {
            padding: 10px 15px;
            display: flex;
            align-items: center;
            border-bottom: 1px solid #f0f0f0;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .filter-option:hover {
            background-color: #f8f8f8;
        }
        
        .filter-option:last-child {
            border-bottom: none;
        }
        
        .filter-option input[type="checkbox"] {
            margin-right: 10px;
            cursor: pointer;
            width: 16px;
            height: 16px;
        }
        
        .filter-option label {
            cursor: pointer;
            font-size: 14px;
            color: #2e2e38;
            line-height: 1.3;
        }
        
        .clear-filters {
            margin-left: 15px;
            background-color: #ffe600;
            color: #2e2e38;
            border: none;
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            font-size: 14px;
            transition: all 0.3s ease;
        }
        
        .clear-filters:hover {
            background-color: #ffd500;
        }
        
        .audit-section table { 
            width: 100%; 
            border-collapse: collapse; 
            margin-top: 20px;
            background-color: #ffffff;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }
        
        .audit-section th, .audit-section td { 
            border: 1px solid #e0e0e0; 
            padding: 12px; 
            text-align: left; 
        }
        
        .audit-section th { 
            background-color: #2e2e38; 
            color: #ffffff;
            font-weight: 600;
            position: sticky;
            top: 0;
            z-index: 10;
        }
        
        .audit-section tr:hover {
            background-color: #fafafa;
        }
        
        .audit-section input[type="checkbox"] { 
            margin-right: 10px; 
            cursor: pointer;
            width: 18px;
            height: 18px;
        }
        
        .audit-section input[type="number"], .audit-section input[type="text"] { 
            width: 100%; 
            box-sizing: border-box; 
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
            transition: border-color 0.3s ease;
        }
        
        .audit-section input[type="number"]:focus, .audit-section input[type="text"]:focus {
            outline: none;
            border-color: #ffe600;
        }
        
        .audit-section button { 
            margin: 10px 5px; 
            padding: 12px 30px; 
            background-color: #ffe600; 
            color: #2e2e38; 
            border: none; 
            border-radius: 4px; 
            cursor: pointer;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .audit-section button:hover {
            background-color: #ffd500;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        #copy-comments {
            background-color: #2e2e38;
            color: #ffffff;
        }
        
        #copy-comments:hover {
            background-color: #1a1a23;
        }
        
        .stats { 
            display: flex; 
            gap: 20px; 
            margin-top: 40px; 
        }
        
        .stats div { 
            background-color: #2e2e38; 
            color: #ffffff;
            padding: 20px 30px; 
            border-radius: 8px;
            text-align: center;
            flex: 1;
        }
        
        .stats div strong {
            display: block;
            font-size: 32px;
            color: #ffe600;
            margin-bottom: 5px;
        }
        
        /* Hidden rows */
        .table-row-hidden {
            display: none !important;
        }
        
        /* Responsive improvements */
        @media (max-width: 768px) {
            .hero h1 { font-size: 36px; }
            .hero p { font-size: 18px; }
            .features h2, .audit-section h2 { font-size: 28px; }
            .stats { flex-direction: column; }
            .audit-section { padding: 40px 20px; }
            header { padding: 15px 20px; }
            nav a { margin-right: 15px; font-size: 14px; }
            
            .filter-dropdown-content {
                min-width: 300px;
                max-width: 90vw;
            }
        }
.feature-card a {
  background: #FFE600;
  color: #161D23 !important;
  border: none;
  border-radius: 4px;
  font-weight: 600;
  padding: 10px 24px;
  text-decoration: none;
  cursor: pointer;
  display: inline-block;
  transition: background 0.2s;
}

.feature-card a:hover {
  background: #ffd500;
  color: #161D23 !important;
}

    </style>
<style>
.audit-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 16px;
    background: #fff;
    font-size: 15px;
}
.audit-table th, .audit-table td {
    padding: 12px 10px;
    border: 1px solid #d4d9df;
    text-align: left;
    vertical-align: middle;
}
.audit-table thead {
    background: #212732;
    color: #fff;
}
.audit-table tbody tr:nth-child(even) {
    background: #f6f8fb;
}
.audit-table select,
.audit-table input[type="text"] {
    width: 98%;
    padding: 6px;
    font-size: 15px;
    border: 1px solid #ccc;
    border-radius: 3px;
}
.audit-table input[type="checkbox"] {
    width: 16px;
    height: 16px;
}
.audit-table th:first-child, .audit-table td:first-child {
    text-align: center;
}
</style>

</head>
<body>
    <header>
        <nav>
            <div>
                <a href="#comment-repository">📊 Repository</a>  // ← ADD THIS LINE
                <a href="https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Finhelpdesk.ey.net%2F%23%2FCreateSr&data=05%7C02%7CMayank.Kohli%40in.ey.com%7C3f9cf35eae294206334d08dd9e956ca2%7C5b973f9977df4bebb27daa0c70b8482c%7C0%7C0%7C638841086854456577%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=NaZZuIJQKCIlhvYGZKvSbVxiOKm4Fa1NHo1X6GGrV18%3D&reserved=0" target="_blank">🎧 Helpdesk</a>
            </div>
        </nav>
    </header>

    <section class="hero">
        <h1>Welcome to Xpensely</h1>
        <p>Your one-stop solution for everything related to Concur expense management</p>
        <div>
            <a href="#features">📚 Explore Features</a>
            <a href="#quick-links">🔗 Quick Links</a>
        </div>
    </section>

    <section class="features">
        <h2>Comprehensive Concur Solutions</h2>
        <p>Everything you need to streamline your expense management process</p>
        <div class="feature-grid">
                        
            <div class="feature-card">
                <span>📋</span>
                <h3>Concur Policy</h3>
                <p>Stay updated with the latest expense policies, approval matrices, and compliance requirements.</p>
                <a href="https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsites.ey.com%2Fsites%2Finfinbulletin%2FPolicies%2FConcur%2520Policy.pdf&data=05%7C02%7CMayank.Kohli%40in.ey.com%7C3f9cf35eae294206334d08dd9e956ca2%7C5b973f9977df4bebb27daa0c70b8482c%7C0%7C0%7C638841086854369489%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=Ehoh8jfalMnzAir1abAfrs%2Bw0HaFpza1BAzCllToAuY%3D&reserved=0" <a href="..." target="_blank" class="btn">Click to Access</a>

            </div>
            <div class="feature-card">
                <span>✈️</span>
                <h3>Travel Policy</h3>
                <p>Access comprehensive travel policy guidelines covering all aspects of business travel expenses.</p>
                <a href="https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsites.ey.com%2Fsites%2Finhronline%2FWhilst_policies%2FTravel%2520Policy.pdf&data=05%7C02%7CMayank.Kohli%40in.ey.com%7C3f9cf35eae294206334d08dd9e956ca2%7C5b973f9977df4bebb27daa0c70b8482c%7C0%7C0%7C638841086854381202%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=%2FRrzT2t2ljYRLpp7mbp0p%2FHJtQwTVKEaJZ8O20kMUvs%3D&reserved=0" <a href="..." target="_blank" class="btn">Click to Access</a>

            </div>
            <div class="feature-card">
                <span>🧮</span>
                <h3>TOA Form Calculator</h3>
                <p>Calculate per diem allowances for overseas travel based on your band and destination country.</p>
                <p>Coming Soon</p>
            </div>
<div class="feature-card">
    <span>🗂️</span>
    <h3>Template of expenses older than 180 days</h3>
    <p>Download the Excel template for expenses older than 180 days for your reference.</p>
    <a href="https://sites.ey.com/:x:/r/sites/infinbulletin/_layouts/15/Doc.aspx?sourcedoc=%7B59C4DD09-4D53-4043-ADA0-8ED32FE933F8%7D&file=Template%20of%20Expense%20older%20than%20180%20days.xlsx&action=default&mobileredirect=true" <a href="..." target="_blank" class="btn">Click to Access</a>

</div>

            <div class="feature-card">
                <span>❓</span>
                <h3>Concur FAQs</h3>
                <p>Find answers to frequently asked questions about Concur expense management system.</p>
                <a href="https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsites.ey.com%2Fsites%2Finfinbulletin%2FPolicies%2FConcur%2520FAQ%2527s.pdf&data=05%7C02%7CMayank.Kohli%40in.ey.com%7C3f9cf35eae294206334d08dd9e956ca2%7C5b973f9977df4bebb27daa0c70b8482c%7C0%7C0%7C638841086854392805%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=QTzaNglas4blXMUTGb%2FMduB8XhrwyvYhaJ%2B6PtQJgow%3D&reserved=0" <a href="..." target="_blank" class="btn">Click to Access</a>

            </div>

<div class="feature-card">
    <span>📁</span>
    <h3>Other Important Documents</h3>
    <p>Access the folder containing other important documents via Teams/SharePoint.</p>
    <a href="https://eyindia.sharepoint.com/:f:/r/sites/Concurinternal_New/Shared%20Documents/Concur%20(internal)/Important%20Documents?csf=1&web=1&e=zBsEA2" <a href="..." target="_blank" class="btn">Click to Access</a>

</div>

            <div class="feature-card">
                <span>🎥</span>
                <h3>Quick Video Reference</h3>
                <p>Watch quick video tutorials and guides for navigating and using the Concur expense management system effectively.</p>
                <a href="https://eyindia.sharepoint.com/sites/MercuryIndiaSharepoint/SitePages/What's-changed-.aspx?csf=1&web=1&e=vgoEqY&CID=246a32c6-8c35-4cbb-a965-056de9fe177a&xsdata=MDV8MDJ8TWF5YW5rLktvaGxpQGluLmV5LmNvbXwzZjljZjM1ZWFlMjk0MjA2MzM0ZDA4ZGQ5ZTk1NmNhMnw1Yjk3M2Y5OTc3ZGY0YmViYjI3ZGFhMGM3MGI4NDgyY3wwfDB8NjM4ODQxMDg2ODU0NDA1MzI4fFVua25vd258VFdGcGJHWnNiM2Q4ZXlKRmJYQjBlVTFoY0draU9uUnlkV1VzSWxZaU9pSXdMakF1TURBd01DSXNJbEFpT2lKWGFXNHpNaUlzSWtGT0lqb2lUV0ZwYkNJc0lsZFVJam95ZlE9PXwwfHx8&sdata=ckVvTlNXUnJqYmRYRHh6K0Y2cWM1Z3hYa2M0Znpobnovb1pmNFNvVHJsYz0%3d" <a href="..." target="_blank" class="btn">Click to Access</a>

            </div>
        </div>
    </section>

<!-- IN AUDIT EXPENSE REPORT (Auto-Auditor) MODULE START -->
<div class="audit-block">
    <div class="audit-title">In Audit Expense Report (Auto-Auditor)</div>
    <div class="info-msg">
        <b>Step 1:</b> Upload your expense report file (<span style="color:#335d92;">CSV/Excel</span>) with columns:
        <b>Report Key, Expense Type, Original Reimbursement Amount</b><br>
        <b>Step 2:</b> Enter (or paste) a Report Key below and click <b>Fetch</b>.<br>
        <b>Step 3:</b> Review auto-generated rows, select Send-Back comments (auto-filled per category), or enter your own.
    </div>

    <input type="file" id="auditFileInput" accept=".csv,.xls,.xlsx">
    <br>
    <label for="auditReportKey" style="font-weight:700;">Enter/Paste Report Key:</label>
    <input type="text" id="auditReportKey" placeholder="Paste report key here" style="max-width:300px;">
    <button id="auditFetchBtn">Fetch</button>
    <span id="auditLoadStatus" style="margin-left:12px;color:#308424;"></span>

<button id="copy-comments">📋 Copy Selected Comments</button>


    <div id="auditExpenseTableWrapper" class="hidden" style="margin-top:20px;">
    <table class="audit-table">
        <thead>
            <tr>
                <th style="width:40px;"><input type="checkbox" id="auditSelectAll"></th>
                <th style="min-width:140px;">Expense Type</th>
                <th style="min-width:100px; cursor:pointer;" id="auditAmountSortHeader">
  Amount (INR) <span id="auditAmountSortArrow">▲</span>
</th>

                <th style="min-width:240px;">Send-Back Comment</th>
                <th style="min-width:200px;">Custom Comment</th>
            </tr>
        </thead>
        <tbody>
        </tbody>
    </table>
</div>

<!-- IN AUDIT EXPENSE REPORT MODULE END -->


    <section class="audit-section" id="audit-comment-bank">
        <a href="#features">← Back to Features</a>
        <h2>Expense Audit Comment Bank</h2>

        <!-- Manual Comment Entry Section with Copy Button at Top -->
        <h3>Manual Comment Entry</h3>
        <table id="manual-comment-table">
            <thead>
                <tr>
                    <th><input type="checkbox" id="select-all-manual"></th>
                    <th>Send-Back Comment</th>
                    <th id="amountHeader" style="cursor:pointer;">Amount (INR) &#9650;</th>

                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><input type="checkbox" class="manual-comment-checkbox"></td>
                    <td><input type="text" placeholder="Enter Send-Back Comment"></td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="manual-comment-checkbox"></td>
                    <td><input type="text" placeholder="Enter Send-Back Comment"></td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="manual-comment-checkbox"></td>
                    <td><input type="text" placeholder="Enter Send-Back Comment"></td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="manual-comment-checkbox"></td>
                    <td><input type="text" placeholder="Enter Send-Back Comment"></td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
            </tbody>
        </table>

        <!-- Filter Section -->
        <h3>All Categories</h3>
        <div class="filter-container">
            <div class="filter-dropdown">
                <button class="filter-btn" id="filterToggle">
                    🏷️ Filter by Expense Categories 
                    <span>▼</span>
                </button>
                <div class="filter-dropdown-content" id="filterDropdown">
                    <div class="filter-header">
                        <h4>Select Expense Categories</h4>
                        <div class="filter-actions">
                            <button id="selectAllCategories">Select All</button>
                            <button id="deselectAllCategories">Deselect All</button>
                        </div>
                    </div>
                    <div id="filterOptions">
                        <!-- Filter options will be populated by JavaScript -->
                    </div>
                </div>
            </div>
            <button class="clear-filters" id="clearFilters">Clear Filters</button>
        </div>

        <!-- Existing Expense Audit Comment Bank Table -->
        <table id="comment-table">
            <thead>
                <tr>
                    <th><input type="checkbox" id="select-all"></th>
                    <th>Expense Head</th>
                    <th>Check Point</th>
                    <th>Send-Back Comment</th>
                    <th id="amountHeader" style="cursor: pointer;">Amount (INR) &#9650;</th>

                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Boarding passes or travel certificate for domestic claims</td>
                    <td>Please attach the boarding pass or a valid travel certificate for the domestic travel claimed, as per policy requirements.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Boarding passes or passport stamp for international travel</td>
                    <td>For international travel, boarding pass and passport stamp are required as proof of travel. Kindly attach the same.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Invoice issued by airlines/aggregators must capture name of the entity, address and GSTIN</td>
                    <td>The invoice does not clearly show entity name, address and GSTIN. Please upload a detailed invoice covering these elements.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Helicopter charges allowed based on engagement partner approval</td>
                    <td>Helicopter charges require engagement partner approval. Kindly attach the necessary approval email.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Domestic Travel - Engagement partner and Market Segment Service line leader approval must be attached for self booking, cancellation & rescheduling</td>
                    <td>For domestic travel self booking/cancellation/rescheduling, approval from engagement partner and Market Segment Service line leader is required. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Foreign Travel - For chargeable code approval from Engagement Partner and SL COO must be attached for self booking, cancellation & rescheduling</td>
                    <td>For foreign travel on chargeable code, approval from Engagement Partner and SL COO is required for self booking/cancellation/rescheduling. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare</td>
                    <td>Foreign Travel - For authorised codes approval from Firm's COO must be attached for self booking, cancellation & rescheduling</td>
                    <td>For foreign travel on authorized codes, approval from Firm's COO is required for self booking/cancellation/rescheduling. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare-Service fee</td>
                    <td>Seat selection charges allowed for Band 1, Non equity partners & CBS directors</td>
                    <td>Seat selection charges are allowed only for Band 1, Non equity partners & CBS directors. Please revise the claim or attach specific approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare-Service fee</td>
                    <td>Lounge charges can be claimed up to INR 5000 for Band 1, Non equity partners & CBS directors</td>
                    <td>Lounge charges up to INR 5000 are allowed for Band 1, Non equity partners & CBS directors. Please revise the amount or attach specific approval.</td>
                    <td><input type="number" placeholder="Enter Amount" value="5000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Airfare Baggage</td>
                    <td>Specific approval from the engagement partner is required to claim this expense (except partners)</td>
                    <td>Baggage charges require specific approval from the engagement partner. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Tax invoice/E-Invoice required with IRN no. & QR code for domestic claims</td>
                    <td>For domestic hotel claims, tax invoice/E-Invoice with IRN number and QR code is mandatory. Please replace with valid document.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Hotel helpdesk confirmation email required on internal codes for International & domestic</td>
                    <td>Hotel helpdesk confirmation email is required for internal codes (international & domestic). Please attach the confirmation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Check the eligibility for hotel if hotel helpdesk email attached if they advise for self booking</td>
                    <td>Please verify hotel eligibility as per helpdesk advice for self booking. Attach supporting documentation if required.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Supplementary bills should be attached for meals, laundry, internet, cab etc.</td>
                    <td>Supplementary bills for meals, laundry, internet, cab etc. are missing. Please attach detailed breakdown bills.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Vikas Dwivedi approval email (if not booked by hotel helpdesk) on internal codes for International & domestic</td>
                    <td>Approval email from Vikas Dwivedi is required for internal codes if not booked by hotel helpdesk. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>For every domestic hotel claims from 31st Jan 2025, we need go ahead from Rupali Kashyap</td>
                    <td>For domestic hotel claims from 31st Jan 2025, go ahead from Rupali Kashyap is required. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Correct entity, GSTIN details mentioned on E-invoice</td>
                    <td>The E-invoice does not contain correct entity and GSTIN details. Please request corrected invoice from hotel.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Check Band wise Limit - Above eligibility deviation cases are subject to approval of Engagement partner followed by Service line leader/service line COO for Band 1 and Band 2; Engagement partner and Procurement for Band 3-6</td>
                    <td>The claim exceeds band-wise hotel eligibility limit. Please attach required approval (EP + SL for Band 1&2, EP + Procurement for Band 3-6).</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Itemization is required</td>
                    <td>Itemized bill is required for hotel expenses. Please attach detailed breakdown of charges.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Room tariff</td>
                    <td>Check the eligibility for hotel if hotel helpdesk email not attached</td>
                    <td>Please verify hotel eligibility and attach hotel helpdesk email if booking was done through helpdesk.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-conference room</td>
                    <td>Invoice should be allowed up to 5,00,000</td>
                    <td>Conference room expenses are allowed up to INR 5,00,000. Please verify the amount or split the invoice if exceeding limit.</td>
                    <td><input type="number" placeholder="Enter Amount" value="500000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-conference room</td>
                    <td>Mic speaker/projector/screens etc</td>
                    <td>Please ensure the invoice clearly mentions conference room equipment (mic, speaker, projector, screens etc.) for processing.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-conference room</td>
                    <td>TCF is mandatory for overseas claims</td>
                    <td>TCF (Travel Claim Form) is mandatory for overseas conference room claims. Please attach the completed TCF.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Laundry</td>
                    <td>Bands 1 & 2 are permitted to claim reasonable laundry expenses subject to bills</td>
                    <td>Laundry expenses are permitted for Bands 1 & 2 only, subject to bills. Please verify eligibility or attach supporting bills.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Laundry</td>
                    <td>If stay exceeds 3 days, laundry up to Rs.250 for every additional three days may be claimed on actuals supported by bills</td>
                    <td>For stay exceeding 3 days, laundry up to Rs.250 for every additional three days is allowed. Please verify the calculation and attach bills.</td>
                    <td><input type="number" placeholder="Enter Amount" value="250"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Laundry</td>
                    <td>EP approval for excess claim</td>
                    <td>Engagement Partner approval is required for excess laundry claims. Please attach the approval email.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Other travel expense</td>
                    <td>Documents attestation charges</td>
                    <td>Engagement Partner approval is required for document attestation charges. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Other travel expense</td>
                    <td>Covid related expenses (Mask, sanitizer etc)</td>
                    <td>Engagement Partner approval is required for Covid-related expenses (mask, sanitizer etc.). Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Domestic travel- F&R stay</td>
                    <td>Check the Band wise eligibility for Band 5 & 6</td>
                    <td>Please verify band-wise eligibility for Band 5 & 6 for domestic F&R stay per diem.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Domestic travel- F&R stay</td>
                    <td>EM approval up to 15 days, more than 15 days EP approval</td>
                    <td>For domestic F&R stay: EM approval required up to 15 days, EP approval for more than 15 days. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Domestic travel- F&R stay</td>
                    <td>We can allow claim of 31 days in a single month</td>
                    <td>Per diem claims are allowed for maximum 31 days in a single month. Please verify the duration claimed.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Domestic travel- Hotel stay</td>
                    <td>Check the Band wise eligibility for Band 5 & 6</td>
                    <td>Please verify band-wise eligibility for Band 5 & 6 for domestic hotel stay per diem.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Domestic travel- Hotel stay</td>
                    <td>EM approval up to 15 days, more than 15 days EP approval</td>
                    <td>For domestic hotel stay: EM approval required up to 15 days, EP approval for more than 15 days. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Foreign travel</td>
                    <td>Check the Band wise eligibility</td>
                    <td>Please verify band-wise eligibility for foreign travel per diem as per policy.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Foreign travel</td>
                    <td>Nights can be calculated based on TCF</td>
                    <td>Number of nights should be calculated based on TCF. Please attach the TCF or verify the calculation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Foreign travel</td>
                    <td>We can allow claim of 31 days in a single month</td>
                    <td>Per diem claims are allowed for maximum 31 days in a single month. Please verify the duration claimed.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Travelling overseas</td>
                    <td>TOA form is required</td>
                    <td>TOA (Travel Overseas Authorization) form is required for overseas travel per diem. Please attach the form.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Travelling overseas</td>
                    <td>Eligibility to be checked</td>
                    <td>Please verify eligibility for overseas travel per diem as per policy guidelines.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Per diem- Travelling overseas</td>
                    <td>Nights can be calculated based on TCF</td>
                    <td>Number of nights should be calculated based on TCF. Please attach the TCF or verify the calculation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Travel Insurance</td>
                    <td>The invoice/policy should capture the name of the entity, address and GSTIN</td>
                    <td>The travel insurance invoice should capture entity name, address and GSTIN. Please request corrected invoice.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Travel Insurance</td>
                    <td>The approval from the engagement partner should be attached along with justification for such specific travel insurance</td>
                    <td>Engagement Partner approval with justification is required for travel insurance. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Travel Insurance</td>
                    <td>Insurance is not permitted except where it is mandated by country to book through their own channel</td>
                    <td>Travel insurance is not permitted except where mandated by the destination country. Please provide justification or remove the claim.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Travel Vaccine</td>
                    <td>Specific approval from the engagement partner is required to claim this expense</td>
                    <td>Specific approval from engagement partner is required for travel vaccine expenses. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Visa Fee</td>
                    <td>In case of Self booking-Approval email from Engagement partner approval</td>
                    <td>For self booking visa fee, engagement partner approval is required. Please attach the approval email.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Visa Fee</td>
                    <td>Claim of EP will processed without any approval</td>
                    <td>Engagement Partner visa fee claims are processed without additional approval as per policy.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Company car Maintenance- Partner</td>
                    <td>Car lease to be checked</td>
                    <td>Please verify car lease documentation for company car maintenance expenses.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Company car Maintenance- Partner</td>
                    <td>Cost center code to be used</td>
                    <td>Please ensure correct cost center code is used for company car maintenance expenses.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Company car Maintenance- Partner</td>
                    <td>Only allowed to Partners (Equity Partners)</td>
                    <td>Company car maintenance is only allowed to Equity Partners. Please verify eligibility.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Auto</td>
                    <td>Need EP approval if amount is more INR 1000/day or 10,000 in aggregates</td>
                    <td>EP approval required if auto charges exceed INR 1000/day or INR 10,000 in aggregate. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Auto</td>
                    <td>For partners, its allowed INR 1000/day</td>
                    <td>For partners, auto charges are allowed up to INR 1000 per day without additional approval.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Parking/toll</td>
                    <td>Same as above in header. Toll: Statement will work, we can check the transaction id for duplicate</td>
                    <td>EP approval required if parking/toll charges exceed INR 1000/day or INR 10,000 in aggregate. For toll, statement verification with transaction ID check for duplicates.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-rail/metro/bus</td>
                    <td>Invoice/ticket to be attached or Need EP approval if amount is more INR 1000/day or 10,000 in aggregates</td>
                    <td>Please attach invoice/ticket or EP approval if rail/metro/bus charges exceed INR 1000/day or INR 10,000 in aggregate.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Supporting not available</td>
                    <td>Need EP approval if amount is more INR 1000/day or 10,000 in aggregates</td>
                    <td>EP approval required if amount exceeds INR 1000/day or INR 10,000 in aggregate when supporting documents are not available.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Supporting not available</td>
                    <td>For partners, its allowed INR 1000/day</td>
                    <td>For partners, expenses without supporting documents are allowed up to INR 1000 per day.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Taxi radio cab- Manual bill</td>
                    <td>Same as above in header</td>
                    <td>For manual taxi bills, EP approval required if amount exceeds INR 1000/day or INR 10,000 in aggregate.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Ground Transportation-Taxi radio cab- System generated bill</td>
                    <td>Same as above in header. UBER: E-receipt without receipt no. can be allowed for domestic claim</td>
                    <td>For system generated taxi bills, UBER e-receipt without receipt number is acceptable for domestic claims. EP approval required if exceeding limits.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Mileage</td>
                    <td>Mileage calculator needs to be used</td>
                    <td>Mileage calculator must be used for distance calculation. Please attach the calculator output.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Mileage</td>
                    <td>Nearest location should be mentioned in origin & destination field</td>
                    <td>Please mention the nearest location in both origin and destination fields for mileage calculation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Mileage</td>
                    <td>Approval from the Engagement/Reporting Partner is required, If the amount claimed for daily mileage exceeds INR 1,500, or cumulative amount of mileage claims exceeds INR 10,000</td>
                    <td>Engagement Partner approval required if daily mileage exceeds INR 1500 or cumulative exceeds INR 10,000. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1500"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Breakfast, lunch, Dinner, snacks, grocery</td>
                    <td>List of attendees required</td>
                    <td>List of attendees is required for meal expenses. Please attach the attendee list.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Breakfast, lunch, Dinner, snacks, grocery</td>
                    <td>Impermissible items not allowed, chocolates not allowed etc</td>
                    <td>Impermissible items like chocolates are not allowed under meal expenses. Please revise the claim.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Breakfast, lunch, Dinner, snacks, grocery</td>
                    <td>Single Invoice should be allowed up to 5,00,000, splitting of invoice of same vendor/same date is not allowed</td>
                    <td>Single invoice should not exceed INR 5,00,000. Splitting of invoice from same vendor/date is not allowed.</td>
                    <td><input type="number" placeholder="Enter Amount" value="500000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Breakfast, lunch, Dinner, snacks, grocery</td>
                    <td>Liquor not allowed except partners & ED's, we can basis on partner approval</td>
                    <td>Liquor is not allowed except for partners & EDs with partner approval. Please remove or attach approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Breakfast, lunch, Dinner, snacks, grocery</td>
                    <td>Wizard claim are allowed up to 3000</td>
                    <td>Wizard meal claims are allowed up to INR 3000. Please verify the amount and revise if exceeding.</td>
                    <td><input type="number" placeholder="Enter Amount" value="3000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Breakfast, lunch, Dinner, snacks, grocery</td>
                    <td>Chocolates for team competition/welcome to EY/onboarding allowed under staff welfare code</td>
                    <td>Chocolates for team competition/welcome to EY/onboarding are allowed under staff welfare code only. Please ensure correct coding.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Weekend & late sitting</td>
                    <td>List of attendees required</td>
                    <td>List of attendees is required for weekend and late sitting meals. Please attach the attendee list.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Meals- Weekend & late sitting</td>
                    <td>Limit of INR 300/person to be checked</td>
                    <td>Weekend and late sitting meals are limited to INR 300 per person. Please verify the calculation and revise if exceeding.</td>
                    <td><input type="number" placeholder="Enter Amount" value="300"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Employee parties- Birthday cake</td>
                    <td>List of attendees required</td>
                    <td>List of attendees is required for birthday cake expenses. Please attach the attendee list.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Employee parties- Birthday cake</td>
                    <td>Claim on staff welfare code only</td>
                    <td>Birthday cake expenses should be claimed on staff welfare code only. Please ensure correct coding.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Employee parties- Birthday cake</td>
                    <td>Decorative items & props not allowed</td>
                    <td>Decorative items and props are not allowed for employee parties. Please revise the claim to exclude these items.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Entertainment expense- Liquor, Liquor with pre-approval, others</td>
                    <td>List of attendees required</td>
                    <td>List of attendees is required for entertainment expenses. Please attach the attendee list.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Entertainment expense- Liquor, Liquor with pre-approval, others</td>
                    <td>Single Invoice greater than 5,00,000 including GST can not be claimed in Concur</td>
                    <td>Single invoice greater than INR 5,00,000 including GST cannot be claimed in Concur. Splitting of invoice from same vendor/date is not allowed.</td>
                    <td><input type="number" placeholder="Enter Amount" value="500000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Entertainment expense- Liquor, Liquor with pre-approval, others</td>
                    <td>Claim on internal code only</td>
                    <td>Entertainment expenses should be claimed on internal code only. Please ensure correct coding.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Entertainment expense- Liquor, Liquor with pre-approval, others</td>
                    <td>EP approval for liquor except Band 1</td>
                    <td>Engagement Partner approval is required for liquor expenses except Band 1. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Courier service</td>
                    <td>Same as above in header</td>
                    <td>Please follow the same approval policy as applicable for courier service expenses.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Newspaper/Books/subscription</td>
                    <td>We can allow books & newspaper subscription</td>
                    <td>Books and newspaper subscription are allowed. Please ensure the claim is for official purposes.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Newspaper/Books/subscription</td>
                    <td>Official download from the website, should we allowed under this head e.g. (Bank VOD, Markables etc.)</td>
                    <td>Official downloads from websites (Bank VOD, Markables etc.) are allowed under this head. Please ensure proper documentation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Photocopy/Printing</td>
                    <td>In case the claim amount is >INR 20,000 in an invoice, it should be claimed through OPRS</td>
                    <td>Photocopy/printing expenses exceeding INR 20,000 should be claimed through OPRS. Please process accordingly.</td>
                    <td><input type="number" placeholder="Enter Amount" value="20000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Photocopy/Printing</td>
                    <td>Invoice should capture the full name of the entity, address and GSTIN</td>
                    <td>The photocopy/printing invoice should capture entity name, address and GSTIN. Please request corrected invoice.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Postage/Shipping</td>
                    <td>In case the claim amount is >INR 20,000 in an invoice, it should be claimed through OPRS</td>
                    <td>Postage/shipping expenses exceeding INR 20,000 should be claimed through OPRS. Please process accordingly.</td>
                    <td><input type="number" placeholder="Enter Amount" value="20000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Stationeries</td>
                    <td>IT consumable also allowed up to 5k</td>
                    <td>IT consumables are allowed up to INR 5000 under stationeries. Please verify the amount and category.</td>
                    <td><input type="number" placeholder="Enter Amount" value="5000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Stationeries</td>
                    <td>In case the claim amount is >INR 20,000 in an invoice, it should be claimed through OPRS</td>
                    <td>Stationery expenses exceeding INR 20,000 should be claimed through OPRS. Please process accordingly.</td>
                    <td><input type="number" placeholder="Enter Amount" value="20000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Stationeries</td>
                    <td>Invoice should capture full name of the entity, address and GSTIN</td>
                    <td>The stationery invoice should capture entity name, address and GSTIN details. Please request corrected invoice from vendor.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Insurance</td>
                    <td>Car lease to be checked - Only allowed to Partners (EP)</td>
                    <td>Insurance expenses are only allowed to Partners (EP). Please verify eligibility and car lease documentation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Insurance</td>
                    <td>C cost center to be used</td>
                    <td>Please ensure C cost center is used for insurance expenses as per policy.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Marathon</td>
                    <td>Marathon event email from HR required</td>
                    <td>Marathon event email from HR is required for processing marathon expenses. Please attach the HR confirmation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Medical Expenses</td>
                    <td>Only health checkup allowed to Partners (EP) & (NEP) & CBS director</td>
                    <td>Health checkup is only allowed to Partners (EP), (NEP) & CBS directors. Please verify eligibility.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Medical Expenses</td>
                    <td>Limit is INR 20,000/year</td>
                    <td>Medical expenses are limited to INR 20,000 per year. Please verify the annual limit and revise if exceeding.</td>
                    <td><input type="number" placeholder="Enter Amount" value="20000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Medical Expenses</td>
                    <td>Mandatory medical test for travel - EP approval required</td>
                    <td>Mandatory medical test for travel requires EP approval. Please attach the engagement partner approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Medical Expenses</td>
                    <td>International travel medical expenses - justification required</td>
                    <td>For international travel medical expenses, justification is required explaining why it couldn't be covered under travel insurance. Please attach EP approval and justification.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Mystery shopping for client deliverables</td>
                    <td>EP approval & client email approval mandatory</td>
                    <td>EP approval and client email approval for purchasing products is mandatory for mystery shopping. Please attach both approvals.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>PCR test</td>
                    <td>EP approval is mandatory</td>
                    <td>EP approval is mandatory for PCR test expenses. Please attach the engagement partner approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Gift to clients-Bouquet</td>
                    <td>Claim on BD code only - allowed to clients only</td>
                    <td>Client gifts should be claimed on BD code only and are allowed for clients only, not for internal EY staff. Please verify the recipient.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Gift to employees - Staff welfare gift</td>
                    <td>Limit is INR 2000 per person - EP approval required</td>
                    <td>Staff welfare gifts are limited to INR 2000 per person and require EP approval. Please attach the approval and verify the amount.</td>
                    <td><input type="number" placeholder="Enter Amount" value="2000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Gift to employees - Staff welfare gift</td>
                    <td>Gift should be of utility, value and easily consumable</td>
                    <td>The gift should be of utility, value and easily consumable (festive hampers, gift vouchers, EY Brand Store items). Please verify the gift type.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Entertainment Expenses-Employee Welfare/Teaming Activities</td>
                    <td>List of attendees required - internal code only</td>
                    <td>List of attendees is required for employee welfare/teaming activities. Please ensure it's claimed on internal code only.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Entertainment Expenses-Employee Welfare/Teaming Activities</td>
                    <td>Team activities up to 5 Lakh with EP approval</td>
                    <td>Team activities and sports (go karting, ground booking, bowling etc.) are allowed up to INR 5 Lakh with EP approval. Please attach the approval.</td>
                    <td><input type="number" placeholder="Enter Amount" value="500000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Hotel-Guest House Utility Expenses</td>
                    <td>Only electricity, water, society maintenance allowed - agreement required</td>
                    <td>Only electricity, water and society maintenance charges are allowed for guest house utilities. Maid and brokerage charges are not allowed. Please attach the agreement.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Cash advance return</td>
                    <td>Acknowledgement from Forex Vendor or treasury confirmation</td>
                    <td>Acknowledgement from Forex Vendor or confirmation from treasury is required for cash advance return. Please attach the confirmation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Cash advance return</td>
                    <td>Report name with FS number</td>
                    <td>Please ensure report name includes FS number for cash advance return processing.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Cellphone expenses</td>
                    <td>Monthly rental not allowed after 14 Feb 2023</td>
                    <td>Monthly rental for cellphone is not allowed after 14 Feb 2023. Please remove monthly rental charges from the claim.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Cellphone expenses</td>
                    <td>Only international roaming package allowed</td>
                    <td>Only international roaming package is allowed for cellphone expenses. Please verify the claim is for roaming charges only.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Cellphone expenses</td>
                    <td>Sim purchase/recharges/calling cards allowed</td>
                    <td>Sim purchase, recharges and calling cards are allowed as per policy. Please ensure proper documentation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Telephone-Broadband/internet & Landline</td>
                    <td>Monthly rental not allowed after 14 Feb 2023</td>
                    <td>Monthly rental for broadband/internet & landline is not allowed after 14 Feb 2023. Please remove monthly rental charges from the claim.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Telephone-Broadband/internet & Landline</td>
                    <td>International roaming allowed based on package</td>
                    <td>International roaming is allowed based on package. Please attach package details and verify the charges.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Cash withdrawal commission fee</td>
                    <td>Cash withdrawal receipt required</td>
                    <td>Cash withdrawal receipt is required for commission fee claims. Please attach the receipt.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Currency exchange commission fee</td>
                    <td>Card statement required with highlighted items</td>
                    <td>Card statement with highlighted items is required for currency exchange commission fee. Please attach the statement.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Professional subscription</td>
                    <td>Allowed to SRB group - engagement code to be checked</td>
                    <td>Professional subscription is allowed to SRB group only. Please verify engagement code and group eligibility.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Professional subscription</td>
                    <td>ICAI membership fees with specific limits</td>
                    <td>ICAI membership fees are allowed with specific limits (Paid Assistant-ACA: INR 1,180, Paid Assistant-FCA: INR 2,950, Partners-ACA: INR 4,720, Partners-FCA: INR 7,670). For excess, approval from Jiwan Jyoti, Gagandeep Singh & VK Vohra is required.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1180"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Registration/Tution fee</td>
                    <td>CA study fee - limit 15000 with approval from Jiwan Jyoti</td>
                    <td>CA study fee is limited to INR 15,000 and requires approval from Jiwan Jyoti. Please attach the approval and verify engagement code.</td>
                    <td><input type="number" placeholder="Enter Amount" value="15000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-Appeal</td>
                    <td>Approval required based on amount</td>
                    <td>Appeal filing fees require approval based on amount. Please attach the necessary approval.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-E TDS</td>
                    <td>E-filing charges allowed with proper documentation</td>
                    <td>E-TDS filing charges are allowed with proper documentation. Please ensure receipt is attached.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-India (ROC) & Bangladesh (RJSC)</td>
                    <td>Ministry of Corporate Affairs receipt required</td>
                    <td>Ministry of Corporate Affairs receipt is required for ROC/RJSC filing fees. Please attach the official receipt.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-MCA</td>
                    <td>MCA portal receipt required</td>
                    <td>MCA portal receipt is required for filing fees. Please attach the official receipt.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-PAN/TIN/BIN application</td>
                    <td>Application receipt with acknowledgement number</td>
                    <td>PAN/TIN/BIN application receipt with acknowledgement number is required. Please attach the official receipt.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-Stamp paper</td>
                    <td>Photocopies of stamp paper or notary charges allowed</td>
                    <td>Photocopies of stamp paper or notary charges are allowed with EM/EP approval for amounts up to/above INR 1000 respectively. For amounts > INR 5000, claim through OPRS.</td>
                    <td><input type="number" placeholder="Enter Amount" value="1000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Statutory filing fees-Other filing</td>
                    <td>Download documents from website</td>
                    <td>Please download supporting documents from the official website for other filing fees.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Audit Balance Confirmation Charges</td>
                    <td>Confirmation.com charges are allowed</td>
                    <td>Confirmation.com charges are allowed for audit balance confirmation. Please ensure proper documentation.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Insurance-Medical Interns</td>
                    <td>Original invoice/policy - limit INR 3500 plus taxes</td>
                    <td>Medical insurance for interns is limited to INR 3500 plus taxes and allowed only for interns 1,2 &3, industrial trainee & staff 1,2 & 3. Please attach original invoice/policy.</td>
                    <td><input type="number" placeholder="Enter Amount" value="3500"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Training</td>
                    <td>Actuarial institute expenses allowed with EP approval</td>
                    <td>Training expenses for Institute of Actuaries of India, Institute and Faculty of Actuaries, Society of Actuaries & Casualty Actuarial Society are allowed with EP approval. Please attach the approval and payment proof.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Training</td>
                    <td>Seminar & conference fee not allowed in Concur</td>
                    <td>Seminar and conference fee reimbursement are not allowed in Concur. Please process through alternate channel.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Transfer entry (Zero value reports)</td>
                    <td>Approval required (25k EP) and WIP report mandatory</td>
                    <td>Transfer entry requires approval (25k EP approval) and WIP report attachment is mandatory. Please attach the approval and WIP report.</td>
                    <td><input type="number" placeholder="Enter Amount" value="25000"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Transfer entry (Zero value reports)</td>
                    <td>Process if email from Sanjay Kumar & Ashish K Pandey attached</td>
                    <td>Transfer cases can be processed if email from Sanjay Kumar & Ashish K Pandey from internal audit team is attached. Please attach the approval email.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>Transfer entry (Zero value reports)</td>
                    <td>Airfare transfer only allowed from I to E engagement code</td>
                    <td>In airfare expense head, transfer is only allowed from I to E engagement code. Please verify the engagement codes.</td>
                    <td><input type="number" placeholder="Enter Amount"></td>
                </tr>
                <tr>
                    <td><input type="checkbox" class="comment-checkbox"></td>
                    <td>South Africa Expense</td>
                    <td>VAT registration number required on invoice > 750 Rand</td>
                    <td>For South Africa expenses > 750 Rand, entity name "Ernst & Young LLP" and VAT ID 4170266045 must be included on all invoices. Please request corrected invoice.</td>
                    <td><input type="number" placeholder="Enter Amount" value="750"></td>
                </tr>
            </tbody>
        </table>

        <div class="stats">
            <div><strong id="total-categories">58</strong> Expense Categories</div>
            <div><strong><span id="visible-items">137</span></strong> Visible Items</div>
            <div><strong><span id="selected-items">0</span></strong> Selected</div>
        </div>
    </section>
</section>

    <!-- ADD ALL THIS NEW SECTION HERE -->
    <section class="audit-section" id="comment-repository">
        <a href="#features">← Back to Features</a>
        <h2>Comment Repository & Analytics</h2>
        
        <div class="filter-container">
    <select id="dateFilter">
        <option value="7">Last 7 days</option>
        <option value="30">Last 30 days</option>
        <option value="90">Last 90 days</option>
        <option value="all">All time</option>
    </select>
    <button id="refreshRepository">Refresh Data</button>
    <button id="deleteAllData" style="background-color: #dc3545; margin-left: 10px;">🗑️ Delete All Data</button>
</div>
        
        <table id="repository-table">
            <thead>
                <tr>
                    <th>Rank</th>
                    <th>Comment</th>
                    <th>Times Used</th>
                    <th>Last Used</th>
                    <th>Trend</th>
                </tr>
            </thead>
            <tbody>
                <!-- Data will be filled by JavaScript -->
            </tbody>
        </table>
        
        <div class="stats">
            <div><strong id="total-comments-used">0</strong> Total Comments Used</div>
            <div><strong id="most-common-issue">-</strong> Most Common Issue</div>
            <div><strong id="trending-up">0</strong> Trending Issues</div>
        </div>
    </section>
    <!-- END OF NEW SECTION -->

    <script>  // ← THIS SHOULD ALREADY BE THERE
    <script>
        // Global variables
        let allCategories = [];
        let selectedCategories = new Set();
        let allRows = [];

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            initializeFilters();
            updateVisibleCount();
        });

        // Initialize filter functionality
        function initializeFilters() {
            // Extract unique expense categories from the table
            const table = document.getElementById('comment-table');
            const rows = table.querySelectorAll('tbody tr');
            allRows = Array.from(rows);
            
            const categorySet = new Set();
            rows.forEach(row => {
                const category = row.cells[1].textContent.trim();
                categorySet.add(category);
            });
            
            allCategories = Array.from(categorySet).sort();
            
            // Populate filter dropdown
            populateFilterDropdown();
            
            // Set up event listeners
            setupFilterEventListeners();
            
            // Update total categories count
            document.getElementById('total-categories').textContent = allCategories.length;
        }

        // Populate the filter dropdown with categories
        function populateFilterDropdown() {
            const filterOptions = document.getElementById('filterOptions');
            filterOptions.innerHTML = '';
            
            allCategories.forEach(category => {
                const option = document.createElement('div');
                option.className = 'filter-option';
                option.innerHTML = `
                    <input type="checkbox" id="category-${category.replace(/[^a-zA-Z0-9]/g, '-')}" value="${category}">
                    <label for="category-${category.replace(/[^a-zA-Z0-9]/g, '-')}">${category}</label>
                `;
                filterOptions.appendChild(option);
            });
        }

        // Set up all filter-related event listeners
        function setupFilterEventListeners() {
            // Toggle dropdown
            document.getElementById('filterToggle').addEventListener('click', function(e) {
                e.stopPropagation();
                const dropdown = document.getElementById('filterDropdown');
                dropdown.classList.toggle('show');
            });

            // Close dropdown when clicking outside
            document.addEventListener('click', function(e) {
                const dropdown = document.getElementById('filterDropdown');
                const filterBtn = document.getElementById('filterToggle');
                if (!dropdown.contains(e.target) && !filterBtn.contains(e.target)) {
                    dropdown.classList.remove('show');
                }
            });

            // Prevent dropdown from closing when clicking inside
            document.getElementById('filterDropdown').addEventListener('click', function(e) {
                e.stopPropagation();
            });

            // Category checkbox changes
            document.getElementById('filterOptions').addEventListener('change', function(e) {
                if (e.target.type === 'checkbox') {
                    if (e.target.checked) {
                        selectedCategories.add(e.target.value);
                    } else {
                        selectedCategories.delete(e.target.value);
                    }
                    applyFilters();
                    updateFilterButtonText();
                }
            });

            // Select all categories
            document.getElementById('selectAllCategories').addEventListener('click', function() {
                const checkboxes = document.querySelectorAll('#filterOptions input[type="checkbox"]');
                checkboxes.forEach(checkbox => {
                    checkbox.checked = true;
                    selectedCategories.add(checkbox.value);
                });
                applyFilters();
                updateFilterButtonText();
            });

            // Deselect all categories
            document.getElementById('deselectAllCategories').addEventListener('click', function() {
                const checkboxes = document.querySelectorAll('#filterOptions input[type="checkbox"]');
                checkboxes.forEach(checkbox => {
                    checkbox.checked = false;
                    selectedCategories.delete(checkbox.value);
                });
                applyFilters();
                updateFilterButtonText();
            });

            // Clear filters button
            document.getElementById('clearFilters').addEventListener('click', function() {
                selectedCategories.clear();
                const checkboxes = document.querySelectorAll('#filterOptions input[type="checkbox"]');
                checkboxes.forEach(checkbox => checkbox.checked = false);
                applyFilters();
                updateFilterButtonText();
            });
        }

        // Apply filters to the table
        function applyFilters() {
            let visibleCount = 0;
            
            allRows.forEach(row => {
                const category = row.cells[1].textContent.trim();
                
                if (selectedCategories.size === 0 || selectedCategories.has(category)) {
                    row.classList.remove('table-row-hidden');
                    visibleCount++;
                } else {
                    row.classList.add('table-row-hidden');
                }
            });
            
            updateVisibleCount();
            updateSelectedCount();
        }

        // Update filter button text
        function updateFilterButtonText() {
            const filterBtn = document.getElementById('filterToggle');
            const span = filterBtn.querySelector('span');
            
            if (selectedCategories.size === 0) {
                filterBtn.innerHTML = '🏷️ Filter by Expense Categories <span>▼</span>';
            } else if (selectedCategories.size === 1) {
                filterBtn.innerHTML = `🏷️ ${Array.from(selectedCategories)[0]} <span>▼</span>`;
            } else {
                filterBtn.innerHTML = `🏷️ ${selectedCategories.size} Categories Selected <span>▼</span>`;
            }
        }

        // Update visible items count
        function updateVisibleCount() {
            const visibleRows = document.querySelectorAll('#comment-table tbody tr:not(.table-row-hidden)');
            document.getElementById('visible-items').textContent = visibleRows.length;
        }

        // Select All Checkboxes for Manual Table
        document.getElementById('select-all-manual').addEventListener('change', function() {
            const checkboxes = document.querySelectorAll('#manual-comment-table .manual-comment-checkbox');
            checkboxes.forEach(checkbox => checkbox.checked = this.checked);
            updateSelectedCount();
        });

        // Select All Checkboxes for Comment Table (only visible rows)
        document.getElementById('select-all').addEventListener('change', function() {
            const checkboxes = document.querySelectorAll('#comment-table tbody tr:not(.table-row-hidden) .comment-checkbox');
            checkboxes.forEach(checkbox => checkbox.checked = this.checked);
            updateSelectedCount();
        });

        // Update Selected Items Count
        function updateSelectedCount() {
            const manualChecked = document.querySelectorAll('#manual-comment-table .manual-comment-checkbox:checked').length;
            const commentChecked = document.querySelectorAll('#comment-table tbody tr:not(.table-row-hidden) .comment-checkbox:checked').length;
            document.getElementById('selected-items').textContent = manualChecked + commentChecked;
        }

        // Copy Selected Comments with Numbered Sequence
        document.getElementById('copy-comments').addEventListener('click', function() {
            let comments = '';
            let index = 1;

            /// Collect comments from manual table
const manualRows = document.querySelectorAll('#manual-comment-table tbody tr');
manualRows.forEach(row => {
    const checkbox = row.querySelector('.manual-comment-checkbox');
    if (checkbox.checked) {
        const comment = row.cells[1].querySelector('input').value || 'N/A';
        const amount = row.cells[2].querySelector('input').value;
        if (amount && amount.trim() !== '') {
            comments += `${index}. INR ${amount} - ${comment}\n`;
        } else {
            comments += `${index}. ${comment}\n`;
        }
        index++;   // 
    }
});


// Collect comments from existing table (only visible rows)
const rows = document.querySelectorAll('#comment-table tbody tr:not(.table-row-hidden)');
rows.forEach(row => {
    const checkbox = row.querySelector('.comment-checkbox');
    if (checkbox.checked) {
        const comment = row.cells[3].textContent;
        const amount = row.cells[4].querySelector('input').value;
        if (amount && amount.trim() !== '') {
            comments += `${index}. INR ${amount} - ${comment}\n`;
        } else {
            comments += `${index}. ${comment}\n`;
        }
        index++;
    }
});

// Collect comments from auto-generated audit table (topmost table)
const auditRows = document.querySelectorAll('#auditExpenseTableWrapper .audit-table tbody tr');
auditRows.forEach(row => {
    const checkbox = row.querySelector('.auditRowChk');
    if (checkbox && checkbox.checked) {
        // Get selected send-back comment (from <select>)
        const sendBackSelect = row.cells[3].querySelector('select');
        const sendBack = sendBackSelect ? sendBackSelect.value || '' : '';
        // Get custom comment (from <input>)
        const customInput = row.cells[4].querySelector('input');
        const customComment = customInput ? customInput.value.trim() : '';
        // Which comment to use? Prefer custom if not empty, else send-back, else 'N/A'
        const commentToUse = customComment || sendBack || 'N/A';
        // Get amount from column 2 (amount is in plain text, not input field)
        const amount = row.cells[2].textContent.trim();
        if (amount && amount !== '' && amount !== '-') {
            comments += `${index}. INR ${amount} - ${commentToUse}\n`;
        } else {
            comments += `${index}. ${commentToUse}\n`;
        }
        index++;
    }
});
            // Add the note at the end of all comments
            if (comments) {
                comments += '\nNote: For general queries, we request you to please use the Amy chatbot. For reimbursement-related issues, concerns, or queries, kindly raise a service request through the Helpdesk by visiting "IN Help Desk (ey.net)" under the "Business Expense Reimbursement" section.';
            }

            // Copy to clipboard
            if (comments) {
                navigator.clipboard.writeText(comments).then(() => {
                    alert('Selected comments copied to clipboard!');
saveCommentsToRepository(comments);
                }).catch(err => {
                    alert('Failed to copy comments: ' + err);
                });
            } else {
                alert('No comments selected!');
            }
        });
        // Update selected count on checkbox change
        document.addEventListener('change', function(e) {
            if (e.target.classList.contains('manual-comment-checkbox') || 
                e.target.classList.contains('comment-checkbox')) {
                updateSelectedCount();
            }
        });
});
    // ← ADD THE NEW FUNCTION HERE, RIGHT AFTER THE CLOSING });
    
// ← Your saveCommentsToRepository function ends here
    
    // ADD THESE TWO FUNCTIONS RIGHT AFTER saveCommentsToRepository
    function loadRepositoryData() {
        // Get data from storage
        let data = JSON.parse(localStorage.getItem('commentRepository') || '[]');
        
        // Count how many times each comment was used
        let commentCounts = {};
        data.forEach(entry => {
            let comment = entry.comment;
            if (commentCounts[comment]) {
                commentCounts[comment].count++;
                commentCounts[comment].lastUsed = entry.date;
            } else {
                commentCounts[comment] = {
                    count: 1,
                    lastUsed: entry.date,
                    comment: comment
                };
            }
        });
        
        // Convert to array and sort by count
        let sortedComments = Object.values(commentCounts)
            .sort((a, b) => b.count - a.count);
        
        // Fill the table
        let tbody = document.querySelector('#repository-table tbody');
        if (tbody) {
            tbody.innerHTML = '';
            
            sortedComments.forEach((item, index) => {
                tbody.innerHTML += `
                    <tr>
                        <td>${index + 1}</td>
                        <td>${item.comment}</td>
                        <td>${item.count}</td>
                        <td>${item.lastUsed}</td>
                        <td>${item.count > 5 ? '📈 High' : item.count > 2 ? '📊 Medium' : '📉 Low'}</td>
                    </tr>
                `;
            });
            
            // Update stats
            document.getElementById('total-comments-used').textContent = data.length;
            if (sortedComments.length > 0) {
                document.getElementById('most-common-issue').textContent = 
                    sortedComments[0].comment.substring(0, 30) + '...';
            }
            document.getElementById('trending-up').textContent = 
                sortedComments.filter(item => item.count > 5).length;
        }
    }
    
    // Initialize repository when page loads
document.addEventListener('DOMContentLoaded', function() {
    // Add refresh button functionality
    let refreshBtn = document.getElementById('refreshRepository');
    if (refreshBtn) {
        refreshBtn.addEventListener('click', function() {
            loadRepositoryData();
            alert('Repository data refreshed!');
        });
    }
    
    // Add delete all data functionality
    let deleteBtn = document.getElementById('deleteAllData');
    if (deleteBtn) {
        deleteBtn.addEventListener('click', function() {
            // Ask user to confirm before deleting
            if (confirm('Are you sure you want to delete ALL repository data? This cannot be undone!')) {
                // Delete all data from browser storage
                localStorage.removeItem('commentRepository');
                // Refresh the table to show empty data
                loadRepositoryData();
                alert('All repository data has been deleted!');
            }
        });
    }
    
    // Load repository data when page opens
    setTimeout(loadRepositoryData, 1000); // Wait 1 second for page to fully load
});    
    </script>  // ← THIS CLOSING SCRIPT TAG SHOULD ALREADY BE THERE
    function saveCommentsToRepository(copiedComments) {
        // Get current date and time
        let now = new Date();
        let timestamp = now.toISOString();
        
        // Split comments into individual lines
        let commentLines = copiedComments.split('\n');
        
        // Get existing data from browser storage
        let repositoryData = JSON.parse(localStorage.getItem('commentRepository') || '[]');
        
        // Save each comment
        commentLines.forEach(line => {
            if (line.trim() && !line.includes('Note:')) {
                repositoryData.push({
                    comment: line.trim(),
                    timestamp: timestamp,
                    date: now.toDateString()
                });
            }
        });
        
        // Save back to browser storage
        localStorage.setItem('commentRepository', JSON.stringify(repositoryData));
        console.log('Comments saved to repository!');
    }
    <script>
document.addEventListener('DOMContentLoaded', function() {
    document.getElementById('copy-comments').addEventListener('click', function() {
        let comments = '';
        let index = 1;

        // Manual Comment Table
        document.querySelectorAll('#manual-comment-table tbody tr').forEach(row => {
            const checkbox = row.querySelector('.manual-comment-checkbox');
            if (checkbox && checkbox.checked) {
                const comment = row.cells[1].querySelector('input').value || 'N/A';
                const amount = row.cells[2].querySelector('input').value;
                if (amount && amount.trim() !== '') {
                    comments += `${index}. INR ${amount} - ${comment}\n`;
                } else {
                    comments += `${index}. ${comment}\n`;
                }
                index++;
            }
        });

        // Main Comment Bank Table (visible rows only)
        document.querySelectorAll('#comment-table tbody tr:not(.table-row-hidden)').forEach(row => {
            const checkbox = row.querySelector('.comment-checkbox');
            if (checkbox && checkbox.checked) {
                const comment = row.cells[3].textContent.trim();
                const amount = row.cells[4].querySelector('input').value;
                if (amount && amount.trim() !== '') {
                    comments += `${index}. INR ${amount} - ${comment}\n`;
                } else {
                    comments += `${index}. ${comment}\n`;
                }
                index++;
            }
        });

        // Audit Table (auto-generated)
        document.querySelectorAll('#auditExpenseTableWrapper .audit-table tbody tr').forEach(row => {
            const checkbox = row.querySelector('.auditRowChk');
            if (checkbox && checkbox.checked) {
                const sendBackSelect = row.cells[3].querySelector('select');
                const sendBack = sendBackSelect ? sendBackSelect.value || '' : '';
                const customInput = row.cells[4].querySelector('input');
                const customComment = customInput ? customInput.value.trim() : '';
                const commentToUse = customComment || sendBack || 'N/A';
                const amount = row.cells[2].textContent.trim();
                if (amount && amount !== '' && amount !== '-') {
                    comments += `${index}. INR ${amount} - ${commentToUse}\n`;
                } else {
                    comments += `${index}. ${commentToUse}\n`;
                }
                index++;
            }
        });

        // Add a note at the end
        if (comments) {
            comments += '\nNote: For general queries, please use Amy chatbot. For reimbursement-related queries, raise a service request via Helpdesk under "Business Expense Reimbursement".';
        }

        // Copy to clipboard and save
        if (comments) {
            navigator.clipboard.writeText(comments).then(() => {
                alert('Selected comments copied to clipboard!');
                saveCommentsToRepository(comments);
            }).catch(err => {
                alert('Failed to copy comments: ' + err);
            });
        } else {
            alert('No comments selected!');
        }
    });

    // Update count of selected items when checkboxes are changed
    document.addEventListener('change', function(e) {
        if (e.target.classList.contains('manual-comment-checkbox') || e.target.classList.contains('comment-checkbox') || e.target.classList.contains('auditRowChk')) {
            updateSelectedCount();
        }
    });

    // Initialize selected count on page load
    updateSelectedCount();

    // Function to update selected count display
    function updateSelectedCount() {
        const manualSelected = document.querySelectorAll('#manual-comment-table .manual-comment-checkbox:checked').length;
        const mainSelected = document.querySelectorAll('#comment-table tbody tr:not(.table-row-hidden) .comment-checkbox:checked').length;
        const auditSelected = document.querySelectorAll('#auditExpenseTableWrapper .audit-table .auditRowChk:checked').length;
        document.getElementById('selected-items').textContent = manualSelected + mainSelected + auditSelected;
    }
});

// This function stores copied comments into your browser's local storage, for analytics later
function saveCommentsToRepository(copiedComments) {
    let now = new Date();
    let timestamp = now.toISOString();

    let commentLines = copiedComments.split('\n');

    let repositoryData = JSON.parse(localStorage.getItem('commentRepository') || '[]');

    commentLines.forEach(line => {
        // Remove numbering and "INR amount -" prefix to keep comment text clean for counting
        let mainText = line.replace(/^\d+\.\s?(INR [\d,]+ - )?/, '').trim();
        if (mainText && !mainText.startsWith("Note:")) {
            repositoryData.push({
                comment: mainText,
                timestamp: timestamp,
                date: now.toDateString()
            });
        }
    });

    localStorage.setItem('commentRepository', JSON.stringify(repositoryData));
    console.log('Comments saved to repository!');
}
</script>

<script>
document.addEventListener('DOMContentLoaded', function() {
    // When the "Refresh Data" button is clicked, update the repository table
    const refreshBtn = document.getElementById('refreshRepository');
    if (refreshBtn) {
        refreshBtn.addEventListener('click', function() {
            loadRepositoryData();
            alert('Repository data refreshed!');
        });
    }

    // Add delete all data functionality
    const deleteBtn = document.getElementById('deleteAllData');
    if (deleteBtn) {
        deleteBtn.addEventListener('click', function() {
            // Ask user to confirm before deleting
            if (confirm('Are you sure you want to delete ALL repository data? This cannot be undone!')) {
                // Delete all data from browser storage
                localStorage.removeItem('commentRepository');
                // Refresh the table to show empty data
                loadRepositoryData();
                alert('All repository data has been deleted!');
            }
        });
    }

    // Load repository data initially after 1 second (so page fully loads first)
    setTimeout(loadRepositoryData, 1000);
});
function loadRepositoryData() {
    let data = JSON.parse(localStorage.getItem('commentRepository') || '[]');

    // Count how many times each comment used & last used date
    let commentCounts = {};
    data.forEach(entry => {
        let comment = entry.comment;
        if (commentCounts[comment]) {
            commentCounts[comment].count++;
            // Use latest date
            if (new Date(entry.date) > new Date(commentCounts[comment].lastUsed)) {
                commentCounts[comment].lastUsed = entry.date;
            }
        } else {
            commentCounts[comment] = {
                count: 1,
                lastUsed: entry.date,
                comment: comment
            };
        }
    });

    // Convert to array & sort by frequency descending
    let sortedComments = Object.values(commentCounts).sort((a, b) => b.count - a.count);

    let tbody = document.querySelector('#repository-table tbody');
    if (tbody) {
        tbody.innerHTML = '';

        sortedComments.forEach((item, index) => {
            tbody.innerHTML += `
                <tr>
                    <td>${index + 1}</td>
                    <td>${item.comment}</td>
                    <td>${item.count}</td>
                    <td>${item.lastUsed}</td>
                    <td>${item.count > 5 ? '📈 High' : item.count > 2 ? '📊 Medium' : '📉 Low'}</td>
                </tr>
            `;
        });

        // Update stats below the table
        document.getElementById('total-comments-used').textContent = data.length;
        if (sortedComments.length > 0) {
            document.getElementById('most-common-issue').textContent = sortedComments[0].comment.substring(0, 30) + '...';
        } else {
            document.getElementById('most-common-issue').textContent = '-';
        }
        document.getElementById('trending-up').textContent = sortedComments.filter(item => item.count > 5).length;
    }
}
</script>

   </body>
</html>
    </script>
<!-- Add these two lines before other JavaScript or before </body> -->
<script src="https://cdn.jsdelivr.net/npm/papaparse@5.3.2/papaparse.min.js"></script>
<script src="https://cdn.sheetjs.com/xlsx-0.20.0/package/dist/xlsx.full.min.js"></script>
<script>
// --- Audit Entry Generator JS ---

let auditReportData = [];

// Build map from audit comment bank using #comment-table
function buildExpenseTypeCommentMap() {
    let map = {};
    // Get the comment table (not manual)
    const commentTable = document.getElementById("comment-table");
    if (!commentTable) return map;
    commentTable.querySelectorAll("tbody tr").forEach(tr => {
        let tds = tr.querySelectorAll('td');
        if (tds.length < 4) return;
        let head = (tds[1].innerText || '').trim();
        let comment = (tds[3].innerText || '').trim();
        if (!head || !comment) return;
        
        // Store with original name
        if (!map[head]) map[head] = [];
        if (!map[head].includes(comment)) map[head].push(comment);
    });
    return map;
}

// NEW FUNCTION - Add this right after the above function
function findBestMatch(expenseType, availableCategories) {
    // First try exact match
    if (availableCategories[expenseType]) {
        return expenseType;
    }
    
    // Clean the expense type for comparison
    let cleanExpense = expenseType.toLowerCase().replace(/[^a-z0-9]/g, '');
    
    // Then try partial matches
    for (let category in availableCategories) {
        let cleanCategory = category.toLowerCase().replace(/[^a-z0-9]/g, '');
        
        // Check if main keywords match
        if (cleanExpense.includes(cleanCategory) || cleanCategory.includes(cleanExpense)) {
            return category;
        }
        
        // Special cases for common variations
        if ((cleanExpense.includes('perdiem') && cleanCategory.includes('perdiem')) ||
            (cleanExpense.includes('hotel') && cleanCategory.includes('hotel')) ||
            (cleanExpense.includes('airfare') && cleanCategory.includes('airfare')) ||
            (cleanExpense.includes('meal') && cleanCategory.includes('meal'))) {
            return category;
        }
    }
    
    return null; // No match found
}
// This runs after the page is loaded
document.addEventListener('DOMContentLoaded', function() {
    let AUDIT_COMMENT_MAP = buildExpenseTypeCommentMap();
// === Add this block right after let AUDIT_COMMENT_MAP = buildExpenseTypeCommentMap(); ===
let auditAmountSortAsc = true;
let sortHeader = document.getElementById('auditAmountSortHeader');
if (sortHeader) {
    sortHeader.addEventListener('click', function() {
        let table = document.querySelector('#auditExpenseTableWrapper .audit-table');
        if (!table) return;
        let tbody = table.tBodies[0];
        let rows = Array.from(tbody.rows);
        let amountColIdx = 2; // Amount is column 2 in audit auto table

        rows.sort(function (a, b) {
            // If column is missing or blank treat as 0
            let valA = parseFloat(a.cells[amountColIdx].textContent.replace(/[^0-9.\-]+/g, '')) || 0;
            let valB = parseFloat(b.cells[amountColIdx].textContent.replace(/[^0-9.\-]+/g, '')) || 0;
            return auditAmountSortAsc ? valA - valB : valB - valA;
        });

        rows.forEach(row => tbody.appendChild(row));

        auditAmountSortAsc = !auditAmountSortAsc;
        document.getElementById('auditAmountSortArrow').textContent = auditAmountSortAsc ? "▲" : "▼";
    });
}

    document.getElementById('auditFileInput').addEventListener('change', function (e) {
        let file = this.files[0];
        if (!file) return;
        let ext = file.name.split('.').pop().toLowerCase();
        let status = document.getElementById('auditLoadStatus');
        status.textContent = "";

        if (ext === "csv") {
            Papa.parse(file, {
                header: true,
                skipEmptyLines: true,
                complete: function (results) {
                    auditReportData = results.data;
                    status.textContent = "File loaded ✔";
                }
            });
        } else if (ext === "xls" || ext === "xlsx") {
            let reader = new FileReader();
            reader.onload = function (evt) {
                let data = new Uint8Array(evt.target.result);
                let workbook = XLSX.read(data, { type: "array" });
                let sheet = workbook.Sheets[workbook.SheetNames[0]];
                auditReportData = XLSX.utils.sheet_to_json(sheet, { defval: '' });
                status.textContent = "File loaded ✔";
            };
            reader.readAsArrayBuffer(file);
        } else {
            alert("Unsupported file type! Only CSV and Excel files are allowed.");
        }
        document.getElementById('auditExpenseTableWrapper').classList.add('hidden');
    });

    document.getElementById('auditFetchBtn').addEventListener('click', function () {
        let key = document.getElementById('auditReportKey').value.trim();
        if (!auditReportData.length) {
            alert("Please upload a file first.");
            return;
        }
        if (!key) {
            alert("Please enter a Report Key.");
            return;
        }
        // Flexible key names for various file formats
        let rows = auditReportData.filter(r =>
            String(
                r["Report Key"] || r["ReportKey"] || r["report key"] || r["REPORT KEY"] || ""
            ).trim() === key
        );

        let tbody = document.querySelector("#auditExpenseTableWrapper tbody");
        tbody.innerHTML = "";

        if (!rows.length) {
            document.getElementById('auditExpenseTableWrapper').classList.add('hidden');
            alert("No matching expenses found.");
            return;
        }

        rows.forEach(row => {
    let expenseType = row["Expense Type"] || row["ExpenseType"] || row["expense type"] || '-';
    let amount = row["Original Reimbursement Amount"] || row["original reimbursement amount"] || row["Amount"] || '-';
    let matchedCategory = findBestMatch(expenseType, AUDIT_COMMENT_MAP);
    let options = matchedCategory ? 
        AUDIT_COMMENT_MAP[matchedCategory].map(txt => `<option>${txt}</option>`).join('') : 
        '';
    if (!options) options = '<option disabled>No predefined comments</option>';
            tbody.innerHTML += `
            <tr>
                <td><input type="checkbox" class="auditRowChk"></td>
                <td>${expenseType}</td>
                <td>${amount}</td>
                <td><select><option value="">Select comment</option>${options}</select></td>
                <td><input type="text" placeholder="Type custom comment"></td>
            </tr>`;
        });

        document.getElementById('auditExpenseTableWrapper').classList.remove('hidden');
    });

    document.getElementById('auditSelectAll').addEventListener('change', function () {
        document.querySelectorAll('.auditRowChk').forEach(cb => cb.checked = this.checked);
    });
});
</script>
</body>
</html>
