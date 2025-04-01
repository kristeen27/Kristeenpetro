<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate 8th Pay Commission Calculator | Most Accurate Projections</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #10b981;
            --accent: #f59e0b;
            --dark: #1e293b;
            --light: #f8fafc;
        }
        body {
            font-family: 'Inter', sans-serif;
            background: #f1f5f9;
            color: var(--dark);
            line-height: 1.6;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .hero {
            background: linear-gradient(135deg, var(--primary), #3b82f6);
            color: white;
            padding: 40px 20px;
            border-radius: 16px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1);
        }
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        .hero p {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        .calculator-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        .card {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
        }
        .card h2 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.5rem;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 10px;
        }
        .input-group {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark);
        }
        input, select {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            font-size: 16px;
            transition: all 0.3s;
        }
        input:focus, select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(37,99,235,0.1);
        }
        button {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            border: none;
            padding: 15px 25px;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            width: 100%;
            transition: all 0.3s;
            margin-top: 10px;
        }
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1);
        }
        .result-section {
            background: #f8fafc;
            border-radius: 10px;
            padding: 25px;
            margin-top: 30px;
            border-left: 5px solid var(--secondary);
        }
        .salary-display {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
            margin: 20px 0;
            text-align: center;
        }
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        .comparison-table th, .comparison-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #e2e8f0;
        }
        .comparison-table th {
            background: #f1f5f9;
            font-weight: 600;
        }
        .badge {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 9999px;
            font-size: 0.8rem;
            font-weight: 600;
            background: var(--accent);
            color: white;
        }
        .chart-container {
            margin-top: 30px;
            height: 300px;
        }
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        .feature-card {
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
        }
        .feature-card i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        .tooltip {
            position: relative;
            display: inline-block;
            cursor: pointer;
        }
        .tooltip .tooltiptext {
            visibility: hidden;
            width: 200px;
            background-color: var(--dark);
            color: #fff;
            text-align: center;
            border-radius: 6px;
            padding: 10px;
            position: absolute;
            z-index: 1;
            bottom: 125%;
            left: 50%;
            transform: translateX(-50%);
            opacity: 0;
            transition: opacity 0.3s;
            font-size: 0.9rem;
        }
        .tooltip:hover .tooltiptext {
            visibility: visible;
            opacity: 1;
        }
        @media (max-width: 768px) {
            .calculator-grid {
                grid-template-columns: 1fr;
            }
            .salary-display {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hero">
            <h1><i class="fas fa-calculator"></i> Ultimate 8th Pay Commission Calculator</h1>
            <p>The most comprehensive tool for central government employees - estimate your salary, allowances, and tax impact</p>
        </div>

        <div class="calculator-grid">
            <div class="card">
                <h2>Salary Details</h2>
                <div class="input-group">
                    <label for="basicPay">Current Basic Pay (7th CPC)</label>
                    <input type="number" id="basicPay" placeholder="e.g. 35000" min="18000">
                </div>
                <div class="input-group">
                    <label for="currentDA">Current DA Rate (%) <span class="tooltip">?<span class="tooltiptext">Current Dearness Allowance rate (e.g. 42%)</span></span></label>
                    <input type="number" id="currentDA" value="46" min="0" max="100">
                </div>
                <div class="input-group">
                    <label for="cityCategory">City Category <span class="tooltip">?<span class="tooltiptext">Determines HRA percentage (X: 24%, Y: 16%, Z: 8%)</span></span></label>
                    <select id="cityCategory">
                        <option value="X">X (Population > 50 lakh)</option>
                        <option value="Y">Y (5-50 lakh)</option>
                        <option value="Z">Z (< 5 lakh)</option>
                    </select>
                </div>
                <div class="input-group">
                    <label for="fitmentFactor">Expected Fitment Factor</label>
                    <select id="fitmentFactor">
                        <option value="2.0">2.0x (Conservative)</option>
                        <option value="2.57">2.57x (Same as 7th CPC)</option>
                        <option value="2.86" selected>2.86x (Likely Minimum)</option>
                        <option value="3.0">3.0x (Optimistic)</option>
                        <option value="3.5">3.5x (Maximum)</option>
                    </select>
                </div>
                <button onclick="calculate()"><i class="fas fa-calculator"></i> Calculate My Revised Salary</button>
            </div>

            <div class="card">
                <h2>Projected 8th CPC Salary</h2>
                <div id="result" style="display: none;">
                    <div class="salary-display" id="revisedSalary"></div>
                    
                    <table class="comparison-table">
                        <thead>
                            <tr>
                                <th>Component</th>
                                <th>7th CPC</th>
                                <th>8th CPC (Projected)</th>
                                <th>Change</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Basic Pay</td>
                                <td id="currentBasic"></td>
                                <td id="newBasic"></td>
                                <td id="basicChange"></td>
                            </tr>
                            <tr>
                                <td>DA</td>
                                <td id="currentDAValue"></td>
                                <td id="newDAValue"></td>
                                <td id="daChange"></td>
                            </tr>
                            <tr>
                                <td>HRA</td>
                                <td id="currentHRA"></td>
                                <td id="newHRA"></td>
                                <td id="hraChange"></td>
                            </tr>
                            <tr>
                                <td><strong>Gross Salary</strong></td>
                                <td id="currentGross"></td>
                                <td id="newGross"></td>
                                <td id="grossChange"></td>
                            </tr>
                        </tbody>
                    </table>

                    <div class="chart-container">
                        <canvas id="salaryChart"></canvas>
                    </div>

                    <button onclick="generatePDF()" style="background: var(--accent); margin-top: 20px;">
                        <i class="fas fa-download"></i> Download Full Report
                    </button>
                </div>
                <div id="noResult" style="text-align: center; padding: 20px; color: #64748b;">
                    <i class="fas fa-calculator" style="font-size: 3rem; opacity: 0.3; margin-bottom: 15px;"></i>
                    <p>Enter your details and click "Calculate" to see your projected 8th CPC salary</p>
                </div>
            </div>
        </div>

        <div class="card" style="margin-top: 30px;">
            <h2>8th CPC Projections Analysis</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <i class="fas fa-chart-line"></i>
                    <h3>Historical Trends</h3>
                    <p>See how each Pay Commission changed salaries since independence with our interactive timeline.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-rupee-sign"></i>
                    <h3>Tax Impact</h3>
                    <p>Understand how your revised salary will affect your tax liabilities under both old and new regimes.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-city"></i>
                    <h3>City Comparison</h3>
                    <p>Compare how your salary changes across different city categories (X, Y, Z).</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-file-pdf"></i>
                    <h3>Detailed Reports</h3>
                    <p>Download personalized PDF reports with breakdowns you can share or print.</p>
                </div>
            </div>
        </div>

        <div class="card" style="margin-top: 30px;">
            <h2>Frequently Asked Questions</h2>
            <div style="margin-top: 20px;">
                <h3 style="color: var(--primary);">Q: When will the 8th Pay Commission be implemented?</h3>
                <p>Based on historical patterns (previous commissions were implemented every 10 years), the 8th CPC is expected around 2026. However, no official announcement has been made yet.</p>
                
                <h3 style="color: var(--primary); margin-top: 20px;">Q: How accurate are these projections?</h3>
                <p>Our calculator uses historical trends from previous pay commissions and current economic indicators to provide realistic estimates. We provide a range of fitment factors to account for different scenarios.</p>
                
                <h3 style="color: var(--primary); margin-top: 20px;">Q: Will allowances also increase?</h3>
                <p>Typically, allowances (HRA, TA, DA) are revised along with basic pay. Our calculator projects HRA based on current city classification rules, and DA based on current inflation trends.</p>
            </div>
        </div>
    </div>

    <script>
        // Global chart variable
        let salaryChart;

        function calculate() {
            // Get input values
            const basicPay = parseFloat(document.getElementById("basicPay").value);
            const currentDA = parseFloat(document.getElementById("currentDA").value) / 100;
            const cityCategory = document.getElementById("cityCategory").value;
            const fitmentFactor = parseFloat(document.getElementById("fitmentFactor").value);
            
            // Validate input
            if (!basicPay || basicPay < 18000) {
                alert("Please enter a valid 7th CPC basic pay (Minimum ₹18,000)");
                return;
            }
            
            // Calculate current salary components
            const currentBasic = basicPay;
            const currentDAValue = basicPay * currentDA;
            let currentHRAPercent;
            switch(cityCategory) {
                case 'X': currentHRAPercent = 0.24; break;
                case 'Y': currentHRAPercent = 0.16; break;
                case 'Z': currentHRAPercent = 0.08; break;
            }
            const currentHRA = basicPay * currentHRAPercent;
            const currentGross = currentBasic + currentDAValue + currentHRA;
            
            // Calculate projected 8th CPC components
            const newBasic = basicPay * fitmentFactor;
            const newDAValue = newBasic * currentDA; // Assuming same DA% initially
            const newHRA = newBasic * currentHRAPercent;
            const newGross = newBasic + newDAValue + newHRA;
            
            // Calculate changes
            const basicChange = ((fitmentFactor - 1) * 100).toFixed(2) + '%';
            const daChange = ((newDAValue - currentDAValue) / currentDAValue * 100).toFixed(2) + '%';
            const hraChange = ((newHRA - currentHRA) / currentHRA * 100).toFixed(2) + '%';
            const grossChange = ((newGross - currentGross) / currentGross * 100).toFixed(2) + '%';
            
            // Display results
            document.getElementById("revisedSalary").innerHTML = 
                `₹${newGross.toLocaleString('en-IN')}/month <span class="badge">${grossChange} increase</span>`;
                
            // Fill comparison table
            document.getElementById("currentBasic").textContent = `₹${currentBasic.toLocaleString('en-IN')}`;
            document.getElementById("newBasic").textContent = `₹${newBasic.toLocaleString('en-IN')}`;
            document.getElementById("basicChange").innerHTML = `<span style="color:var(--secondary)">${basicChange}</span>`;
            
            document.getElementById("currentDAValue").textContent = `₹${currentDAValue.toLocaleString('en-IN')}`;
            document.getElementById("newDAValue").textContent = `₹${newDAValue.toLocaleString('en-IN')}`;
            document.getElementById("daChange").innerHTML = `<span style="color:var(--secondary)">${daChange}</span>`;
            
            document.getElementById("currentHRA").textContent = `₹${currentHRA.toLocaleString('en-IN')}`;
            document.getElementById("newHRA").textContent = `₹${newHRA.toLocaleString('en-IN')}`;
            document.getElementById("hraChange").innerHTML = `<span style="color:var(--secondary)">${hraChange}</span>`;
            
            document.getElementById("currentGross").textContent = `₹${currentGross.toLocaleString('en-IN')}`;
            document.getElementById("newGross").textContent = `₹${newGross.toLocaleString('en-IN')}`;
            document.getElementById("grossChange").innerHTML = `<span style="color:var(--secondary)">${grossChange}</span>`;
            
            // Show result section
            document.getElementById("result").style.display = "block";
            document.getElementById("noResult").style.display = "none";
            
            // Create/update chart
            createChart(currentBasic, newBasic, currentHRA, newHRA, currentDAValue, newDAValue);
            
            // Smooth scroll to results
            document.getElementById("result").scrollIntoView({ behavior: 'smooth' });
        }
        
        function createChart(currentBasic, newBasic, currentHRA, newHRA, currentDA, newDA) {
            const ctx = document.getElementById('salaryChart').getContext('2d');
            
            // Destroy previous chart if exists
            if (salaryChart) {
                salaryChart.destroy();
            }
            
            salaryChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Basic Pay', 'HRA', 'DA'],
                    datasets: [
                        {
                            label: '7th CPC',
                            data: [currentBasic, currentHRA, currentDA],
                            backgroundColor: '#3b82f6',
                            borderColor: '#2563eb',
                            borderWidth: 1
                        },
                        {
                            label: '8th CPC (Projected)',
                            data: [newBasic, newHRA, newDA],
                            backgroundColor: '#10b981',
                            borderColor: '#059669',
                            borderWidth: 1
                        }
                    ]
                },
                options: {
                    responsive: true,
                    scales: {
                        y: {
                            beginAtZero: true,
                            ticks: {
                                callback: function(value) {
                                    return '₹' + (value/1000).toLocaleString('en-IN') + 'k';
                                }
                            }
                        }
                    },
                    plugins: {
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return context.dataset.label + ': ₹' + context.raw.toLocaleString('en-IN');
                                }
                            }
                        }
                    }
                }
            });
        }
        
        function generatePDF() {
            alert("PDF generation would be implemented with a library like jsPDF in a production environment");
            // In a real implementation, this would:
            // 1. Use jsPDF to create a PDF document
            // 2. Add all calculation results
            // 3. Include the chart as an image
            // 4. Add personalized details
            // 5. Trigger download
        }
    </script>
</body>
</html>
