# Sample

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Attendance System</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Login Section -->
    <div id="loginContainer" class="container">
        <h1>🔐 Login to Attendance System</h1>
        <div class="login-box">
            <input type="text" id="username" placeholder="Username">
            <input type="password" id="password" placeholder="Password">
            <button onclick="login()">Login</button>
            <p>Don't have an account? <a href="#" onclick="register()">Register Here</a></p>
            <div id="loginMessage" class="message"></div>
        </div>
    </div>

    <!-- Main App Section (Hidden by default) -->
    <div id="appContainer" class="container" style="display: none;">
        <div class="header">
            <h1>📋 Student Attendance System</h1>
            <button onclick="logout()" class="logout-btn">Logout</button>
        </div>

        <!-- Add Student Section -->
        <div class="section">
            <h2>Add Student</h2>
            <input type="text" id="studentName" placeholder="Enter student name">
            <input type="text" id="studentId" placeholder="Enter student ID">
            <button onclick="addStudent()">Add Student</button>
        </div>

        <!-- Mark Attendance Section -->
        <div class="section">
            <h2>Mark Attendance</h2>
            <p>Date: <span id="currentDate"></span></p>
            <table id="attendanceTable">
                <thead>
                    <tr>
                        <th>ID</th>
                        <th>Name</th>
                        <th>Status</th>
                    </tr>
                </thead>
                <tbody id="studentList">
                    <!-- Students will appear here -->
                </tbody>
            </table>
            <button class="save-btn" onclick="saveAttendance()">Save Attendance</button>
        </div>

        <!-- View Records Section -->
        <div class="section">
            <h2>View Attendance Records</h2>
            <button onclick="viewRecords()">Show Records</button>
            <div id="recordsContainer"></div>
        </div>
    </div>

    <script src="script.js"></script>
    <link rel= "stylesheet" href= "style.css"/>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background-color: #f4f4f9;
    padding: 20px;
}

.container {
    max-width: 800px;
    margin: 0 auto;
}

/* Login Styles */
#loginContainer {
    max-width: 400px;
    margin-top: 100px;
    text-align: center;
}

.login-box {
    background: white;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.login-box input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.login-box button {
    width: 100%;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
}

.login-box a {
    color: #2196F3;
    text-decoration: none;
    font-size: 14px;
}

.message {
    margin-top: 10px;
    font-size: 14px;
    color: red;
}

/* App Styles */
h1 {
    text-align: center;
    color: #333;
    margin-bottom: 30px;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.logout-btn {
    background-color: #f44336;
    padding: 8px 15px;
    font-size: 14px;
}

.section {
    background: white;
    padding: 20px;
    margin-bottom: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

h2 {
    color: #555;
    margin-bottom: 15px;
}

input {
    padding: 10px;
    margin-right: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    width: 200px;
}

button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background 0.3s;
}

button:hover {
    background-color: #45a049;
}

.save-btn {
    background-color: #2196F3;
    margin-top: 15px;
}

.save-btn:hover {
    background-color: #0b7dda;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 15px;
}

th, td {
    padding: 12px;
    text-align: left;
    border-bottom: 1px solid #ddd;
}

th {
    background-color: #f8f8f8;
}

.status-btn {
    padding: 5px 10px;
    margin-right: 5px;
    font-size: 12px;
}

.present {
    background-color: #4CAF50;
}

.absent {
    background-color: #f44336;
}

.selected {
    border: 2px solid #333;
}

#recordsContainer {
    margin-top: 15px;
}

.record-date {
    background: #e8f5e9;
    padding: 10px;
    margin: 5px 0;
    border-radius: 4px;
}
