<!DOCTYPE html>
<html dir="rtl" lang="he">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>דו"ח פיננסי - משפחות הקהילה</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', 'Rubik', Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
            line-height: 1.6;
        }
        
        .main-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            animation: slideDown 0.8s ease-out;
        }
        
        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        h1 {
            font-size: 3em;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
            font-weight: 800;
        }
        
        .subtitle {
            font-size: 1.3em;
            color: #666;
            font-weight: 300;
        }
        
        .alert-banner {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
            color: white;
            padding: 30px;
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(238, 90, 36, 0.3);
            animation: pulse 2s infinite;
            position: relative;
            overflow: hidden;
        }
        
        .alert-banner::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }
        
        .crisis-header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }
        
        .crisis-icon {
            font-size: 3em;
            animation: shake 0.5s ease-in-out infinite alternate;
        }
        
        @keyframes shake {
            from { transform: rotate(-5deg); }
            to { transform: rotate(5deg); }
        }
        
        .crisis-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
            position: relative;
            z-index: 1;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            border: 2px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        
        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .stat-label {
            font-size: 1.1em;
            opacity: 0.9;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            animation: fadeIn 0.8s ease-out;
            transition: all 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .family-header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px 30px;
            margin: -30px -30px 30px -30px;
            border-radius: 20px 20px 0 0;
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .family-icon {
            font-size: 2.5em;
        }
        
        .family-title {
            flex: 1;
        }
        
        .family-title h2 {
            margin: 0;
            font-size: 1.8em;
            font-weight: 600;
        }
        
        .family-title p {
            margin: 5px 0 0 0;
            opacity: 0.9;
            font-size: 1.1em;
        }
        
        table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
            margin: 20px 0;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
        }
        
        th {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px;
            text-align: right;
            font-weight: 600;
            font-size: 1.1em;
        }
        
        td {
            padding: 15px;
            text-align: right;
            border-bottom: 1px solid #eee;
            transition: all 0.3s ease;
        }
        
        tr:hover td {
            background-color: rgba(102, 126, 234, 0.05);
        }
        
        tr:nth-child(even) td {
            background-color: rgba(0, 0, 0, 0.02);
        }
        
        .income-row td {
            background-color: rgba(46, 213, 115, 0.1);
            color: #27ae60;
            font-weight: 500;
        }
        
        .expense-row td {
            background-color: rgba(255, 107, 107, 0.1);
            color: #e74c3c;
        }
        
        .total-row td {
            background: linear-gradient(135deg, #f5f3f0 0%, #e8e6e3 100%);
            font-weight: bold;
            font-size: 1.2em;
            color: #2c3e50;
        }
        
        .deficit-row td {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
            color: white;
            font-weight: bold;
            font-size: 1.3em;
        }
        
        .section-divider {
            text-align: center;
            margin: 40px 0;
            font-weight: bold;
            color: #666;
            position: relative;
        }
        
        .section-divider::before,
        .section-divider::after {
            content: '';
            position: absolute;
            top: 50%;
            width: 35%;
            height: 1px;
            background: linear-gradient(to right, transparent, #ddd);
        }
        
        .section-divider::before {
            right: 65%;
        }
        
        .section-divider::after {
            left: 65%;
            background: linear-gradient(to left, transparent, #ddd);
        }
        
        .chart-container {
            background: white;
            border-radius: 20px;
            padding: 40px 30px;
            margin: 30px 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
        }
        
        .chart-title {
            font-size: 1.8em;
            color: #2c3e50;
            margin-bottom: 40px;
            font-weight: 600;
        }
        
        .comparison-bars {
            display: flex;
            justify-content: space-around;
            align-items: flex-end;
            height: 350px;
            margin: 50px 0;
            position: relative;
            padding: 40px 0;
        }
        
        .bar-wrapper {
            flex: 1;
            max-width: 200px;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
        }
        
        .bar {
            width: 100%;
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
            border-radius: 10px 10px 0 0;
            position: relative;
            transition: all 0.5s ease;
            cursor: pointer;
        }
        
        .bar:hover {
            transform: scaleY(1.05);
        }
        
        .bar.positive {
            background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%);
        }
        
        .bar-value {
            position: absolute;
            top: -50px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2.2em;
            font-weight: bold;
            color: #2c3e50;
            white-space: nowrap;
        }
        
        .bar-label {
            margin-top: 25px;
            font-size: 1.1em;
            color: #666;
            text-align: center;
            line-height: 1.5;
        }
        
        .pie-chart-wrapper {
            display: inline-block;
            position: relative;
            margin: 50px auto;
        }
        
        .legend {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin-top: 40px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 15px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px;
            background: #f8f9fa;
            border-radius: 10px;
            transition: all 0.3s ease;
        }
        
        .legend-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .legend-color {
            width: 30px;
            height: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .recommendations {
            background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%);
            color: white;
            padding: 40px;
            border-radius: 20px;
            margin: 30px 0;
            box-shadow: 0 15px 35px rgba(46, 204, 113, 0.3);
        }
        
        .recommendations h2 {
            font-size: 2em;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .recommendation-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .recommendation-card {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            padding: 25px;
            border-radius: 15px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
        }
        
        .recommendation-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.3);
        }
        
        .recommendation-card h3 {
            font-size: 1.4em;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .recommendation-table {
            background: white;
            color: #333;
            border-radius: 10px;
            overflow: hidden;
            margin-top: 20px;
        }
        
        .recommendation-table th {
            background: rgba(0,0,0,0.1);
            color: #2c3e50;
        }
        
        .final-summary {
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
            color: white;
            padding: 40px;
            border-radius: 20px;
            margin: 30px 0;
            text-align: center;
            box-shadow: 0 15px 35px rgba(231, 76, 60, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .final-summary::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 30s linear infinite;
        }
        
        .final-summary h2 {
            font-size: 2.5em;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }
        
        .final-summary p {
            font-size: 1.3em;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }
        
        .highlight {
            background: rgba(255, 255, 255, 0.2);
            padding: 2px 8px;
            border-radius: 5px;
            font-weight: bold;
        }
        
        @media (max-width: 768px) {
            .main-container {
                padding: 10px;
            }
            
            h1 {
                font-size: 2em;
            }
            
            .crisis-stats {
                grid-template-columns: 1fr;
            }
            
            .comparison-bars {
                flex-direction: column;
                height: auto;
                gap: 40px;
            }
            
            .bar-wrapper {
                width: 100%;
                max-width: none;
            }
            
            .recommendation-grid {
                grid-template-columns: 1fr;
            }
        }
        
        @media print {
            body {
                background: white;
            }
            
            .card {
                box-shadow: none;
                border: 1px solid #ddd;
                page-break-inside: avoid;
            }
            
            .alert-banner::before,
            .final-summary::before {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div class="main-container">
        <div class="header">
            <h1>דו"ח פיננסי מקיף</h1>
            <p class="subtitle">מצב כלכלי של משפחות הקהילה - ינואר 2025</p>
        </div>

        <!-- משפחה צעירה -->
        <div class="card">
            <div class="family-header">
                <div class="family-icon">👨‍👩‍👧‍👦</div>
                <div class="family-title">
                    <h2>משפחה צעירה</h2>
                    <p>2 פעוטות (תינוק 9 חודשים בבית, ילד בן שנתיים בגן)</p>
                </div>
            </div>
            
            <h3 style="color: #27ae60; margin-bottom: 20px;">📊 הכנסות חודשיות</h3>
            <table>
                <tr>
                    <th>סעיף</th>
                    <th>סכום ($)</th>
                </tr>
                <tr class="income-row">
                    <td>משכורת הבעל</td>
                    <td>2,450</td>
                </tr>
                <tr class="income-row">
                    <td>משכורת האישה</td>
                    <td>1,500</td>
                </tr>
                <tr class="income-row">
                    <td>קצבת ילדים (250$ × 2)</td>
                    <td>500</td>
                </tr>
                <tr class="income-row">
                    <td>מענק חג (500$ בממוצע לשנה ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="total-row">
                    <td>סה"כ הכנסות</td>
                    <td>4,492</td>
                </tr>
            </table>

            <h3 style="color: #e74c3c; margin: 30px 0 20px;">💸 הוצאות חודשיות</h3>
            <table>
                <tr>
                    <th>סעיף</th>
                    <th>סכום ($)</th>
                </tr>
                <tr class="expense-row">
                    <td>שכר דירה</td>
                    <td>1,000</td>
                </tr>
                <tr class="expense-row">
                    <td>מטפלת (4.5$ × 9 שעות × 26 ימים)</td>
                    <td>1,053</td>
                </tr>
                <tr class="expense-row">
                    <td>אוכל</td>
                    <td>1,000</td>
                </tr>
                <tr class="expense-row">
                    <td>שכר לימוד (ילד אחד בגן)</td>
                    <td>200</td>
                </tr>
                <tr class="expense-row">
                    <td>הסעות (ילד אחד)</td>
                    <td>100</td>
                </tr>
                <tr class="expense-row">
                    <td>מעשר לקהילה</td>
                    <td>300</td>
                </tr>
                <tr class="expense-row">
                    <td>ביגוד</td>
                    <td>150</td>
                </tr>
                <tr class="expense-row">
                    <td>חשמל, מים, טלפון, אינטרנט</td>
                    <td>150</td>
                </tr>
                <tr class="expense-row">
                    <td>תחבורה</td>
                    <td>100</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות רפואיות</td>
                    <td>50</td>
                </tr>
                <tr class="expense-row">
                    <td>תחזוקת בית ואחרות</td>
                    <td>150</td>
                </tr>
                <tr>
                    <td colspan="2" class="section-divider">הוצאות שנתיות מחולקות לחודש</td>
                </tr>
                <tr class="expense-row">
                    <td>טיסות לארץ - <strong>פעם בשנתיים</strong> (3 כרטיסים × 850$ ÷ 24 חודשים)</td>
                    <td>106</td>
                </tr>
                <tr class="expense-row">
                    <td>פאה - <strong>פעם ב-3 שנים</strong> (5,600$ ÷ 36 חודשים)</td>
                    <td>156</td>
                </tr>
                <tr class="expense-row">
                    <td>מתנות למשפחה (1,000$ ÷ 12)</td>
                    <td>83</td>
                </tr>
                <tr class="expense-row">
                    <td>חסכון לשמחות (1,700$ ÷ 12)</td>
                    <td>142</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות ויזה (500$ ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות חגים (500$ ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="total-row">
                    <td>סה"כ הוצאות</td>
                    <td>4,824</td>
                </tr>
                <tr class="deficit-row">
                    <td>גירעון חודשי</td>
                    <td>-332</td>
                </tr>
                <tr class="deficit-row">
                    <td>גירעון שנתי</td>
                    <td>-3,984</td>
                </tr>
            </table>
        </div>

        <!-- משפחה בינונית -->
        <div class="card">
            <div class="family-header">
                <div class="family-icon">👨‍👩‍👧‍👦👶</div>
                <div class="family-title">
                    <h2>משפחה בינונית</h2>
                    <p>5 ילדים (גילאי 2, 5, 8, 11, 13)</p>
                </div>
            </div>
            
            <h3 style="color: #27ae60; margin-bottom: 20px;">📊 הכנסות חודשיות</h3>
            <table>
                <tr>
                    <th>סעיף</th>
                    <th>סכום ($)</th>
                </tr>
                <tr class="income-row">
                    <td>משכורת הבעל</td>
                    <td>2,450</td>
                </tr>
                <tr class="income-row">
                    <td>משכורת האישה</td>
                    <td>1,500</td>
                </tr>
                <tr class="income-row">
                    <td>קצבת ילדים (250$ × 5)</td>
                    <td>1,250</td>
                </tr>
                <tr class="income-row">
                    <td>מענק חג (500$ בממוצע לשנה ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="total-row">
                    <td>סה"כ הכנסות</td>
                    <td>5,242</td>
                </tr>
            </table>

            <h3 style="color: #e74c3c; margin: 30px 0 20px;">💸 הוצאות חודשיות</h3>
            <table>
                <tr>
                    <th>סעיף</th>
                    <th>סכום ($)</th>
                </tr>
                <tr class="expense-row">
                    <td>שכר דירה</td>
                    <td>1,000</td>
                </tr>
                <tr class="expense-row">
                    <td>מטפלת (4.5$ × 9 שעות × 26 ימים)</td>
                    <td>1,053</td>
                </tr>
                <tr class="expense-row">
                    <td>אוכל</td>
                    <td>2,000</td>
                </tr>
                <tr class="expense-row">
                    <td>שכר לימוד (200$ + 50$×3 + 50$)</td>
                    <td>400</td>
                </tr>
                <tr class="expense-row">
                    <td>הסעות (100$ × 2 ילדים)</td>
                    <td>200</td>
                </tr>
                <tr class="expense-row">
                    <td>מעשר לקהילה</td>
                    <td>300</td>
                </tr>
                <tr class="expense-row">
                    <td>ביגוד</td>
                    <td>200</td>
                </tr>
                <tr class="expense-row">
                    <td>חשמל, מים, טלפון, אינטרנט</td>
                    <td>150</td>
                </tr>
                <tr class="expense-row">
                    <td>תחבורה</td>
                    <td>100</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות רפואיות</td>
                    <td>100</td>
                </tr>
                <tr class="expense-row">
                    <td>חוגים והעשרה</td>
                    <td>100</td>
                </tr>
                <tr class="expense-row">
                    <td>תחזוקת בית ואחרות</td>
                    <td>150</td>
                </tr>
                <tr>
                    <td colspan="2" class="section-divider">הוצאות שנתיות מחולקות לחודש</td>
                </tr>
                <tr class="expense-row">
                    <td>טיסות לארץ - <strong>פעם בשנתיים</strong> (6 כרטיסים × 850$ ÷ 24 חודשים)</td>
                    <td>213</td>
                </tr>
                <tr class="expense-row">
                    <td>פאה - <strong>פעם ב-3 שנים</strong> (5,600$ ÷ 36 חודשים)</td>
                    <td>156</td>
                </tr>
                <tr class="expense-row">
                    <td>מתנות למשפחה (1,000$ ÷ 12)</td>
                    <td>83</td>
                </tr>
                <tr class="expense-row">
                    <td>חסכון לשמחות (1,700$ ÷ 12)</td>
                    <td>142</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות ויזה (500$ ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות חגים (1,000$ ÷ 12)</td>
                    <td>83</td>
                </tr>
                <tr class="total-row">
                    <td>סה"כ הוצאות</td>
                    <td>6,472</td>
                </tr>
                <tr class="deficit-row">
                    <td>גירעון חודשי</td>
                    <td>-1,230</td>
                </tr>
                <tr class="deficit-row">
                    <td>גירעון שנתי</td>
                    <td>-14,760</td>
                </tr>
            </table>
        </div>

        <!-- משפחה גדולה -->
        <div class="card">
            <div class="family-header">
                <div class="family-icon">👨‍👩‍👧‍👦👨‍👩‍👧‍👦</div>
                <div class="family-title">
                    <h2>משפחה גדולה</h2>
                    <p>8 ילדים (גילאי 2, 4, 6, 8, 10, 12, 15, 17)</p>
                </div>
            </div>
            
            <h3 style="color: #27ae60; margin-bottom: 20px;">📊 הכנסות חודשיות</h3>
            <table>
                <tr>
                    <th>סעיף</th>
                    <th>סכום ($)</th>
                </tr>
                <tr class="income-row">
                    <td>משכורת הבעל</td>
                    <td>2,450</td>
                </tr>
                <tr class="income-row">
                    <td>משכורת האישה</td>
                    <td>1,500</td>
                </tr>
                <tr class="income-row">
                    <td>קצבת ילדים (250$ × 8)</td>
                    <td>2,000</td>
                </tr>
                <tr class="income-row">
                    <td>מענק חג (500$ בממוצע לשנה ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="income-row">
                    <td>השתתפות בשכ"ל ישיבה בחו"ל (250$)</td>
                    <td>250</td>
                </tr>
                <tr class="total-row">
                    <td>סה"כ הכנסות</td>
                    <td>6,242</td>
                </tr>
            </table>

            <h3 style="color: #e74c3c; margin: 30px 0 20px;">💸 הוצאות חודשיות</h3>
            <table>
                <tr>
                    <th>סעיף</th>
                    <th>סכום ($)</th>
                </tr>
                <tr class="expense-row">
                    <td>שכר דירה</td>
                    <td>1,000</td>
                </tr>
                <tr class="expense-row">
                    <td>מטפלת (4.5$ × 9 שעות × 26 ימים)</td>
                    <td>1,053</td>
                </tr>
                <tr class="expense-row">
                    <td>אוכל</td>
                    <td>2,500</td>
                </tr>
                <tr class="expense-row">
                    <td>שכר לימוד (200$ + 50$×4 + 400$ + 500$)</td>
                    <td>1,300</td>
                </tr>
                <tr class="expense-row">
                    <td>הסעות (100$ × 3 ילדים)</td>
                    <td>300</td>
                </tr>
                <tr class="expense-row">
                    <td>מעשר לקהילה</td>
                    <td>300</td>
                </tr>
                <tr class="expense-row">
                    <td>ביגוד</td>
                    <td>400</td>
                </tr>
                <tr class="expense-row">
                    <td>חשמל, מים, טלפון, אינטרנט</td>
                    <td>150</td>
                </tr>
                <tr class="expense-row">
                    <td>תחבורה</td>
                    <td>100</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות רפואיות</td>
                    <td>200</td>
                </tr>
                <tr class="expense-row">
                    <td>חוגים והעשרה</td>
                    <td>200</td>
                </tr>
                <tr class="expense-row">
                    <td>תחזוקת בית ואחרות</td>
                    <td>150</td>
                </tr>
                <tr>
                    <td colspan="2" class="section-divider">הוצאות שנתיות מחולקות לחודש</td>
                </tr>
                <tr class="expense-row">
                    <td>טיסות משפחה לארץ - <strong>פעם בשנתיים</strong> (9 × 850$ ÷ 24)</td>
                    <td>319</td>
                </tr>
                <tr class="expense-row">
                    <td>טיסות נוספות לילד בישיבה (2 × 850$ ÷ 12)</td>
                    <td>142</td>
                </tr>
                <tr class="expense-row">
                    <td>פאה - <strong>פעם ב-3 שנים</strong> (5,600$ ÷ 36 חודשים)</td>
                    <td>156</td>
                </tr>
                <tr class="expense-row">
                    <td>מתנות למשפחה (1,000$ ÷ 12)</td>
                    <td>83</td>
                </tr>
                <tr class="expense-row">
                    <td>חסכון לשמחות (1,700$ ÷ 12)</td>
                    <td>142</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות ויזה (500$ ÷ 12)</td>
                    <td>42</td>
                </tr>
                <tr class="expense-row">
                    <td>הוצאות חגים (1,500$ ÷ 12)</td>
                    <td>125</td>
                </tr>
                <tr class="total-row">
                    <td>סה"כ הוצאות</td>
                    <td>8,662</td>
                </tr>
                <tr class="deficit-row">
                    <td>גירעון חודשי</td>
                    <td>-2,420</td>
                </tr>
                <tr class="deficit-row">
                    <td>גירעון שנתי</td>
                    <td>-29,040</td>
                </tr>
            </table>
        </div>

        <!-- משבר כלכלי חמור -->
        <div class="alert-banner">
            <div class="crisis-header">
                <div class="crisis-icon">🚨</div>
                <div>
                    <h2 style="margin: 0; font-size: 2em;">משבר כלכלי חמור</h2>
                    <p style="margin: 5px 0; font-size: 1.2em;">פער קריטי בין עליית המחירים לעדכון המשכורות</p>
                </div>
            </div>
            <div class="crisis-stats">
                <div class="stat-card">
                    <div class="stat-number">96%</div>
                    <div class="stat-label">אינפלציה מצטברת</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">10%</div>
                    <div class="stat-label">עדכון משכורות</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">86%</div>
                    <div class="stat-label">פער ריאלי</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">45%</div>
                    <div class="stat-label">ירידה בכוח קנייה</div>
                </div>
            </div>
        </div>

        <!-- סיכום גירעונות -->
        <div class="card">
            <h2 style="color: #e74c3c; text-align: center; margin-bottom: 30px;">📊 סיכום הגירעונות</h2>
            <table style="font-size: 1.1em;">
                <tr>
                    <th>סוג משפחה</th>
                    <th>גירעון חודשי</th>
                    <th>גירעון שנתי</th>
                    <th>אחוז גירעון מההכנסה</th>
                </tr>
                <tr>
                    <td><strong>משפחה צעירה (2 ילדים)</strong></td>
                    <td style="color: #e74c3c; font-weight: bold;">$332-</td>
                    <td style="color: #e74c3c; font-weight: bold;">$3,984-</td>
                    <td style="color: #e74c3c; font-weight: bold;">7.4%</td>
                </tr>
                <tr>
                    <td><strong>משפחה בינונית (5 ילדים)</strong></td>
                    <td style="color: #e74c3c; font-weight: bold;">$1,230-</td>
                    <td style="color: #e74c3c; font-weight: bold;">$14,760-</td>
                    <td style="color: #e74c3c; font-weight: bold;">23.5%</td>
                </tr>
                <tr style="background: rgba(255, 107, 107, 0.1);">
                    <td><strong>משפחה גדולה (8 ילדים)</strong></td>
                    <td style="color: #e74c3c; font-weight: bold;">$2,420-</td>
                    <td style="color: #e74c3c; font-weight: bold;">$29,040-</td>
                    <td style="color: #e74c3c; font-weight: bold;">38.8%</td>
                </tr>
            </table>
        </div>

        <!-- נתוני אינפלציה -->
        <div class="chart-container">
            <h2 class="chart-title">📈 נתוני אינפלציה ועליית מחירים (2015-2024)</h2>
            
            <h3 style="margin: 30px 0 20px;">אינפלציה שנתית ברוסיה</h3>
            <table>
                <tr>
                    <th>שנה</th>
                    <th>אינפלציה שנתית (%)</th>
                    <th>אינפלציה מצטברת מ-2015 (%)</th>
                </tr>
                <tr><td>2015</td><td>12.9%</td><td>12.9%</td></tr>
                <tr><td>2016</td><td>5.4%</td><td>19.0%</td></tr>
                <tr><td>2017</td><td>2.5%</td><td>21.9%</td></tr>
                <tr><td>2018</td><td>4.3%</td><td>27.1%</td></tr>
                <tr><td>2019</td><td>3.0%</td><td>30.9%</td></tr>
                <tr><td>2020</td><td>4.9%</td><td>37.4%</td></tr>
                <tr><td>2021</td><td>8.4%</td><td>48.9%</td></tr>
                <tr><td>2022</td><td>11.9%</td><td>66.7%</td></tr>
                <tr><td>2023</td><td>7.4%</td><td>79.0%</td></tr>
                <tr><td>2024</td><td>9.5%</td><td>96.0%</td></tr>
                <tr class="deficit-row">
                    <td colspan="2"><strong>סה"כ אינפלציה מצטברת</strong></td>
                    <td><strong>96%</strong></td>
                </tr>
            </table>

            <h3 style="margin: 40px 0 20px;">עליית מחירים בקטגוריות ספציפיות</h3>
            <table>
                <tr>
                    <th>קטגוריה</th>
                    <th>עלייה בשנה האחרונה</th>
                    <th>הערות</th>
                </tr>
                <tr class="expense-row">
                    <td><strong>🏠 שכירות</strong></td>
                    <td><strong>31.4%</strong></td>
                    <td>דירת חדר במוסקבה: 73,000 רובל (עלייה של 43%)</td>
                </tr>
                <tr class="expense-row">
                    <td><strong>🍕 מזון</strong></td>
                    <td><strong>8-10%</strong></td>
                    <td>ביצים: +61%, פלפל ירוק: +46%</td>
                </tr>
                <tr class="expense-row">
                    <td><strong>✈️ טיסות פנים</strong></td>
                    <td><strong>22.2%</strong></td>
                    <td>7,600 רובל ל-1,000 ק"מ</td>
                </tr>
                <tr class="expense-row">
                    <td><strong>🚇 תחבורה ציבורית</strong></td>
                    <td><strong>15.7%</strong></td>
                    <td>מטרו במוסקבה: עלה ל-60 רובל</td>
                </tr>
                <tr class="expense-row">
                    <td><strong>👔 ביגוד והנעלה</strong></td>
                    <td><strong>6%</strong></td>
                    <td>עקב עליית חומרי גלם</td>
                </tr>
                <tr class="expense-row">
                    <td><strong>🏥 שירותים</strong></td>
                    <td><strong>8.3%</strong></td>
                    <td>כולל שירותי בריאות וחינוך</td>
                </tr>
            </table>
        </div>

        <!-- גרף השוואה -->
        <div class="chart-container">
            <h2 class="chart-title" style="margin-bottom: 60px;">📊 השוואה: אינפלציה מול עדכון משכורות (10 שנים)</h2>
            <div class="comparison-bars" style="height: 350px; padding: 40px 0 60px 0;">
                <div class="bar-wrapper">
                    <div class="bar" style="height: 280px;">
                        <div class="bar-value" style="top: -50px;">96%</div>
                    </div>
                    <div class="bar-label" style="margin-top: 30px;">
                        <strong style="font-size: 1.3em;">אינפלציה מצטברת</strong><br>
                        <span style="color: #e74c3c;">2015-2024</span>
                    </div>
                </div>
                <div class="bar-wrapper">
                    <div class="bar positive" style="height: 29px;">
                        <div class="bar-value" style="top: -50px;">10%</div>
                    </div>
                    <div class="bar-label" style="margin-top: 30px;">
                        <strong style="font-size: 1.3em;">עדכון משכורות</strong><br>
                        <span style="color: #27ae60;">5 שנים אחרונות</span>
                    </div>
                </div>
            </div>
            <div style="background: rgba(255, 193, 7, 0.1); padding: 25px; border-radius: 15px; margin-top: 30px;">
                <p style="color: #f39c12; margin: 0; font-size: 1.5em; font-weight: bold;">
                    ⚠️ הפער: 86% - ירידה ריאלית של כ-45% בכוח הקנייה
                </p>
                <p style="color: #666; margin-top: 15px; font-size: 1.1em;">
                    בעוד שהמחירים כמעט הוכפלו, המשכורות כמעט לא השתנו
                </p>
            </div>
        </div>

        <!-- גרף עלות מטפלת -->
        <div class="chart-container">
            <h2 class="chart-title" style="margin-bottom: 60px;">🏚️ ➡️ 🏠 עליית עלות מטפלת - השוואה 2015 מול 2025</h2>
            <div class="comparison-bars" style="height: 350px; padding: 40px 0 60px 0;">
                <div class="bar-wrapper">
                    <div class="bar positive" style="height: 80px; background: linear-gradient(135deg, #4ecdc4 0%, #44a08d 100%);">
                        <div class="bar-value" style="top: -50px;">140 ₽</div>
                    </div>
                    <div class="bar-label" style="margin-top: 30px;">
                        <strong style="font-size: 1.3em;">2015</strong><br>
                        <span style="color: #666;">לשעה</span>
                    </div>
                </div>
                <div class="bar-wrapper">
                    <div class="bar" style="height: 280px;">
                        <div class="bar-value" style="top: -50px;">500 ₽</div>
                    </div>
                    <div class="bar-label" style="margin-top: 30px;">
                        <strong style="font-size: 1.3em;">2025</strong><br>
                        <span style="color: #666;">לשעה</span>
                    </div>
                </div>
            </div>
            <div style="background: rgba(231, 76, 60, 0.1); padding: 25px; border-radius: 15px; margin-top: 30px;">
                <p style="color: #e74c3c; margin: 0; font-size: 1.5em; font-weight: bold;">
                    📈 עלייה של 257% בעלות שעת מטפלת!
                </p>
                <p style="color: #333; margin-top: 15px; font-size: 1.2em;">
                    <strong>בדולרים:</strong> מ-378$ לחודש (2015) ➡️ ל-1,053$ לחודש (2025)
                </p>
                <p style="color: #666; margin-top: 10px; font-size: 1em;">
                    *חישוב למשפחה עם מטפלת 9 שעות ביום, 6 ימים בשבוע
                </p>
            </div>
        </div>

        <!-- גרף עוגה -->
        <div class="chart-container">
            <h2 class="chart-title">🥧 התפלגות הוצאות - משפחה עם 5 ילדים</h2>
            <div class="pie-chart-wrapper" style="margin: 50px auto;">
                <svg width="450" height="450" viewBox="0 0 450 450">
                    <g transform="translate(225,225)">
                        <!-- מזון 30.9% -->
                        <path d="M 0,0 L 0,-170 A 170,170 0 0,1 161.6,-52.6 Z" fill="#ff6b6b" stroke="white" stroke-width="3"/>
                        <text x="60" y="-90" text-anchor="middle" font-weight="bold" fill="white">מזון</text>
                        <text x="60" y="-70" text-anchor="middle" font-size="1.2em" font-weight="bold" fill="white">30.9%</text>
                        
                        <!-- מטפלת 16.3% -->
                        <path d="M 0,0 L 161.6,-52.6 A 170,170 0 0,1 170,17 Z" fill="#4ecdc4" stroke="white" stroke-width="3"/>
                        <text x="140" y="-10" text-anchor="middle" font-weight="bold" fill="white">מטפלת</text>
                        <text x="140" y="10" text-anchor="middle" font-size="1.1em" font-weight="bold" fill="white">16.3%</text>
                        
                        <!-- דיור 15.5% -->
                        <path d="M 0,0 L 170,17 A 170,170 0 0,1 98.6,138.5 Z" fill="#45b7d1" stroke="white" stroke-width="3"/>
                        <text x="100" y="70" text-anchor="middle" font-weight="bold" fill="white">דיור</text>
                        <text x="100" y="90" text-anchor="middle" font-size="1.1em" font-weight="bold" fill="white">15.5%</text>
                        
                        <!-- חינוך 6.2% -->
                        <path d="M 0,0 L 98.6,138.5 A 170,170 0 0,1 37.4,165.8 Z" fill="#f39c12" stroke="white" stroke-width="3"/>
                        
                        <!-- שאר 31.1% -->
                        <path d="M 0,0 L 37.4,165.8 A 170,170 0 0,1 0,-170 Z" fill="#95a5a6" stroke="white" stroke-width="3"/>
                        <text x="-70" y="50" text-anchor="middle" font-weight="bold" fill="white">שאר</text>
                        <text x="-70" y="70" text-anchor="middle" font-size="1.1em" font-weight="bold" fill="white">31.1%</text>
                    </g>
                </svg>
            </div>
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background: #ff6b6b;"></div>
                    <span>מזון (30.9%)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background: #4ecdc4;"></div>
                    <span>מטפלת (16.3%)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background: #45b7d1;"></div>
                    <span>דיור (15.5%)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background: #f39c12;"></div>
                    <span>חינוך (6.2%)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background: #95a5a6;"></div>
                    <span>אחר (31.1%)</span>
                </div>
            </div>
        </div>

        <!-- המלצות -->
        <div class="recommendations">
            <h2><span>📋</span> המלצות להנהלת הקהילה</h2>
            
            <div class="recommendation-grid">
                <div class="recommendation-card">
                    <h3><span>💰</span> עדכון מיידי של המשכורות</h3>
                    <ul style="list-style: none; padding: 0;">
                        <li>✅ <strong>העלאה מינימלית של 50%</strong></li>
                        <li style="margin: 10px 0;">✅ <strong>העלאה מומלצת של 75-100%</strong></li>
                        <li>✅ הצמדה שנתית לאינפלציה</li>
                    </ul>
                </div>
                
                <div class="recommendation-card">
                    <h3><span>🎯</span> תוספות ייעודיות מיידיות</h3>
                    <table class="recommendation-table">
                        <tr>
                            <th>תוספת</th>
                            <th>סכום מומלץ</th>
                        </tr>
                        <tr>
                            <td>סבסוד מטפלת</td>
                            <td><strong>600-800$</strong></td>
                        </tr>
                        <tr>
                            <td>קרן חסכון/פנסיה</td>
                            <td><strong>15%</strong></td>
                        </tr>
                        <tr>
                            <td>מענק טיסות</td>
                            <td><strong>2,000-4,000$</strong></td>
                        </tr>
                        <tr>
                            <td>תוספת יוקר</td>
                            <td><strong>10%</strong></td>
                        </tr>
                    </table>
                </div>
                
                <div class="recommendation-card">
                    <h3><span>🏠</span> סבסוד דיור</h3>
                    <ul style="list-style: none; padding: 0;">
                        <li>✅ <strong>סבסוד מוגבר לשכר דירה</strong></li>
                        <li style="margin: 10px 0;">✅ <strong>אפשרות לדיור קהילתי</strong></li>
                        <li>✅ השתתפות בהוצאות החשמל והגז</li>
                    </ul>
                </div>
                
                <div class="recommendation-card">
                    <h3><span>👨‍👩‍👧‍👦</span> תמיכה במשפחות גדולות</h3>
                    <ul style="list-style: none; padding: 0;">
                        <li>✅ <strong>העלאת משכורת של 100%</strong></li>
                        <li style="margin: 10px 0;">✅ <strong>500$ לכל ילד מעל החמישי</strong></li>
                        <li>✅ סבסוד מלא למטפלת</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- סיכום סופי -->
        <div class="final-summary">
            <h2>⏰ סיכום - פעולה דחופה נדרשת</h2>
            <p>
                <strong>המצב הנוכחי אינו בר-קיימא.</strong> משפחות הקהילה חיות בגירעון קבוע ומצטבר, 
                ללא יכולת לחסוך לעתיד או להתמודד עם הוצאות בלתי צפויות. 
                העלאת המשכורות אינה "בקשה" - היא <span class="highlight">הכרח קיומי</span>.
            </p>
            <p style="margin-top: 20px;">
                <strong>ללא פעולה מיידית:</strong> משפחות ייאלצו להיכנס לחובות, 
                או לוותר על צרכים בסיסיים. זהו משבר אמיתי הדורש פתרון דחוף.
            </p>
        </div>
    </div>
</body>
</html>
