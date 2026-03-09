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
</body>
</html>
