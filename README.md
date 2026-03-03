<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Royal Academy</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        /* Header */
        header {
            background-color: #1e2a38;
            color: white;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 15px 40px;
        }

        .logo {
            width: 80px;
            height: auto;
        }

        .school-name {
            font-size: 24px;
            font-weight: bold;
            margin-left: 15px;
        }

        .logo-section {
            display: flex;
            align-items: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-size: 16px;
        }

        nav a:hover {
            text-decoration: underline;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 80px 20px;
            background-color: #f4f4f4;
        }

        .hero h1 {
            font-size: 40px;
            color: #1e2a38;
        }

        .hero p {
            font-size: 18px;
            color: #555;
        }

        /* Footer */
        footer {
            background-color: #1e2a38;
            color: white;
            text-align: center;
            padding: 15px;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo-section">
            <img src="logo.png" alt="Royal Academy Logo" class="logo">
            <div class="school-name">Royal Academy</div>
        </div>

        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Admissions</a>
            <a href="#">Contact</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Welcome to Royal Academy</h1>
        <p>Excellence • Leadership • Knowledge</p>
    </section>

    <!-- Footer -->
    <footer>
        © 2026 Royal Academy. All Rights Reserved.
    </footer>

</body>
</html>

<!DOCTYPE html>
<html lang="sw">
<head>
<meta charset="UTF-8">
<title>Session Report System</title>
<style>
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        background-color: #FFD700; /* Gold background */
    }
    h2, h3 {
        text-align: center;
    }
    .container {
        max-width: 1100px;
        margin: 30px auto;
        background-color: #fff8dc; /* Light gold-ish container */
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0px 0px 12px #aaa;
    }
    label {
        font-weight: bold;
        display: block;
        margin-top: 10px;
    }
    input, select, textarea {
        width: 100%;
        padding: 6px;
        margin-top: 4px;
        font-size: 14px;
        box-sizing: border-box;
    }
    button {
        margin-top: 10px;
        padding: 8px 16px;
        font-size: 14px;
        cursor: pointer;
        background-color: #DAA520;
        color: white;
        border: none;
        border-radius: 4px;
    }
    table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 20px;
    }
    th, td {
        border: 1px solid black;
        padding: 6px;
        text-align: center;
    }
    th {
        background-color: #f2e6b3;
    }
    textarea {
        resize: vertical;
    }
</style>
</head>
<body>

<div class="container" id="loginDiv">
    <h2>teacher's login</h2>
    <label>Name of school:</label>
    <input type="text" id="schoolNameInput" placeholder="Andika jina la shule">
    <label>Password:</label>
    <input type="password" id="passwordInput" placeholder="Andika password">
    <button onclick="login()">login</button>
</div>

<div class="container" id="reportDiv" style="display:none;">
    <h2>SESSION REPORT</h2>

    <p><strong>Shule:</strong> <span id="schoolNameDisplay"></span></p>
    <p><strong>Mwalimu:</strong> <input type="text" placeholder="Andika jina lako hapa" id="teacherNameInputReport"></p>

    <label>Combination:</label>
    <select id="combination">
        <option value="">-- Chagua Combination --</option>
        <option value="PCB">PCB</option>
        <option value="PCM">PCM</option>
        <option value="PMCs">PMCs</option>
        <option value="CBG">CBG</option>
        <option value="EGM">EGM</option>
        <option value="HGE">HGE</option>
        <option value="HGL">HGL</option>
        <option value="HGLi">HGLi</option>
        <option value="HGFa">HGFa</option>
        <option value="HGK">HGK</option>
        <option value="HKL">HKL</option>
    </select>

    <button onclick="autofillCodes()">Auto-fill Codes & Subjects</button>
    <button onclick="addRow()">Ongeza Row</button>
    <button onclick="downloadCSV()">Save / Download CSV</button>
    <button onclick="window.print()">Print Report</button>

    <table id="sessionTable">
        <tr>
            <th>Subject Code</th>
            <th>Jina la Somo</th>
            <th>Topic</th>
            <th>Subtopic</th>
            <th>Tarehe</th>
            <th>Muda Kuanzia</th>
            <th>Muda Kumaliza</th>
            <th>Sahihi ya Mwalimu</th>
        </tr>
        <!-- initial 5 editable rows -->
        <tr><td><input type="text"></td><td><input type="text"></td><td><textarea rows="2"></textarea></td><td><textarea rows="2"></textarea></td><td><input type="date"></td><td><input type="time"></td><td><input type="time"></td><td><input type="text"></td></tr>
        <tr><td><input type="text"></td><td><input type="text"></td><td><textarea rows="2"></textarea></td><td><textarea rows="2"></textarea></td><td><input type="date"></td><td><input type="time"></td><td><input type="time"></td><td><input type="text"></td></tr>
        <tr><td><input type="text"></td><td><input type="text"></td><td><textarea rows="2"></textarea></td><td><textarea rows="2"></textarea></td><td><input type="date"></td><td><input type="time"></td><td><input type="time"></td><td><input type="text"></td></tr>
        <tr><td><input type="text"></td><td><input type="text"></td><td><textarea rows="2"></textarea></td><td><textarea rows="2"></textarea></td><td><input type="date"></td><td><input type="time"></td><td><input type="time"></td><td><input type="text"></td></tr>
        <tr><td><input type="text"></td><td><input type="text"></td><td><textarea rows="2"></textarea></td><td><textarea rows="2"></textarea></td><td><input type="date"></td><td><input type="time"></td><td><input type="time"></td><td><input type="text"></td></tr>
    </table>
</div>
<script>
// Password ya umma validated
const PASSWORD = "walimu2026"; // Badilisha hapa password unayopenda

// Subject codes + names kwa combinations 11
const subjectData = {
    PCB: [["031","Physics"],["032","Chemistry"],["033","Biology"]],
    PCM: [["031","Physics"],["032","Chemistry"],["034","Mathematics"]],
    PMCs: [["031","Physics"],["034","Mathematics"],["035","Computer Science"]],
    CBG: [["032","Chemistry"],["033","Biology"],["036","Geography"]],
    EGM: [["037","Economics"],["036","Geography"],["034","Mathematics"]],
    HGE: [["038","History"],["036","Geography"],["037","Economics"]],
    HGL: [["038","History"],["036","Geography"],["002","Literature"]],
    HGLi: [["038","History"],["036","Geography"],["039","English Lit"]],
    HGFa: [["038","History"],["036","Geography"],["040","Fine Arts"]],
    HGK: [["038","History"],["036","Geography"],["001","Kiswahili"]],
    HKL: [["038","History"],["001","Kiswahili"],["002","Literature"]]
};

// Login validation
function login() {
    const schoolName = document.getElementById("schoolNameInput").value.trim();
    const password = document.getElementById("passwordInput").value;
    
    if(schoolName === "") { alert("Tafadhali andika jina la shule."); return; }
    if(password !== PASSWORD){ alert("Password si sahihi!"); return; }

    document.getElementById("schoolNameDisplay").innerText = schoolName;
    document.getElementById("loginDiv").style.display = "none";
    document.getElementById("reportDiv").style.display = "block";
}

// Auto-fill codes + subjects
function autofillCodes() {
    const comb = document.getElementById("combination").value;
    const table = document.getElementById("sessionTable");
    if(!subjectData[comb]) return;

    for(let i=1;i<=subjectData[comb].length;i++){
        const row = table.rows[i];
        row.cells[0].children[0].value = subjectData[comb][i-1][0]; // code
        row.cells[1].children[0].value = subjectData[comb][i-1][1]; // subject
    }
}

// Add new row
function addRow(){
    const table = document.getElementById("sessionTable");
    const row = table.insertRow();
    for(let i=0;i<8;i++){
        const cell = row.insertCell();
        if(i==2 || i==3){ // Topic / Subtopic textarea
            const textarea = document.createElement("textarea");
            textarea.rows = 2;
            cell.appendChild(textarea);
        } else if(i==4){ // Tarehe
            const input = document.createElement("input");
            input.type="date";
            cell.appendChild(input);
        } else if(i==5 || i==6){ // Muda Kuanzia/Kumaliza
            const input = document.createElement("input");
            input.type="time";
            cell.appendChild(input);
        } else { // Code, subject, sahihi
            const input = document.createElement("input");
            input.type="text";
            cell.appendChild(input);
        }
    }
}

// Download CSV
function downloadCSV() {
    const table = document.getElementById("sessionTable");
    let csvContent = "";

    for(let i=0; i<table.rows.length; i++){
        let row = [];
        for(let j=0;j<table.rows[i].cells.length;j++){
            const input = table.rows[i].cells[j].querySelector("input,textarea");
            if(input){
                row.push('"' + input.value.replace(/"/g,'""') + '"');
            } else {
                row.push('"' + table.rows[i].cells[j].innerText.replace(/"/g,'""') + '"');
            }
        }
        csvContent += row.join(",") + "\n";
    }

    const blob = new Blob([csvContent], {type:'text/csv;charset=utf-8;'});
    const link = document.createElement("a");
    link.href = URL.createObjectURL(blob);
    link.download = "session_report.csv";
    link.click();
}
</script>

</body>
</html>
