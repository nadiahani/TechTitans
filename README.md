# TechTitans
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Learning Platform</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        /* Styles from your main page */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
        }
        .sidebar {
            width: 200px;
            background-color: #2c3e50;
            color: white;
            padding: 20px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            position: fixed; /* Fixed position */
            top: 0;
            left: 0;
            height: 100%;
        }
        .sidebar .links,
        .sidebar .bottom-links {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        .sidebar a {
            color: white;
            text-decoration: none;
            padding: 5px 10px;
            background-color: #34495e;
            border-radius: 5px;
        }
        .sidebar a:hover {
            background-color: #1abc9c;
        }
        .main-content {
            flex-grow: 1;
            padding: 20px;
            background-color: #ecf0f1;
            margin-left: 200px; /* Adjusted for sidebar width */
        }
        .header {
            background-color: #BDB5D5;
            color: white;
            padding: 10px 20px;
        }
        .card {
            background-color: white;
            border-radius: 4px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }
        .grid-item {
            background-color: white;
            border-radius: 5px;
            padding: 30px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            text-align: center;
            transition: background-color 0.3s;
        }
        .grid-item a {
            text-decoration: none;
            color: #34495e;
            display: block;
        }
        .grid-item img {
            width: 80px;
            height: 80px;
        }
        .grid-item:hover {
            background-color: #1abc9c;
        }
        /* Styles for notes section */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f3f8;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        h1 {
            color: #5e2b97;
            margin-top: 30px;
        }
        form {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 80%;
            max-width: 600px;
            margin-top: 20px;
        }
        label {
            font-weight: bold;
            color: #5e2b97;
            margin-top: 10px;
        }
        input[type="text"], input[type="file"] {
            width: calc(100% - 22px);
            padding: 10px;
            margin-top: 5px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #7b42f6;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
            margin-bottom: 10px;
        }
        button:hover {
            background-color: #5e2b97;
        }
        #noteDisplay h2 {
            margin-top: 40px;
            color: #5e2b97;
        }
        .note {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 10px;
            background-color: #fff;
        }
        .note h3 {
            margin: 0;
        }
        .note iframe {
            width: 100%;
            height: 300px;
            border: 1px solid #ccc;
            margin-top: 10px;
        }
        .delete-btn {
            background-color: #ff4d4d;
            color: white;
            padding: 5px 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        .delete-btn:hover {
            background-color: #cc0000;
        }
        .container {
            width: 100%;
            max-width: 800px;
            padding: 20px;
            margin: 0 auto;
        }
        .add-more-btn {
            margin-bottom: 20px;
            background-color: #6c63ff;
        }
        .add-more-btn:hover {
            background-color: #4b3f94;
        }
        .file-inputs {
            margin-bottom: 15px;
        }
        /*Style for Timer*/
        #task-form {
            display: flex;
            margin-bottom: 20px;
        }
        #task-input {
            padding: 8px;
            font-size: 16px;
            border: 2px solid #8B5DA6;
            border-radius: 4px 0 0 4px;
            outline: none;
        }
        #task-input:focus {
            border-color: #6C3483;
        }
        #task-input::placeholder {
            color: #aaa;
        }
        #task-form button {
            padding: 8px 20px;
            font-size: 16px;
            background-color: #8B5DA6;
            color: white;
            border: none;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
        }
        #task-form button:hover {
            background-color: #6C3483;
        }
        #task-list {
            list-style-type: none;
            padding: 0;
            width: 100%;
            max-width: 400px;
        }
        #task-list li {
            background-color: #fff;
            padding: 10px;
            margin-bottom: 5px;
            border-radius: 4px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        #task-list li button {
            padding: 4px 10px;
            font-size: 14px;
            background-color: #E59866;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        #task-list li button:hover {
            background-color: #DC7633;
        }
        #timer-container {
            display: flex;
            align-items: center;
            margin-top: 20px;
        }
        #timer-container > div {
            margin-right: 10px;
        }
        #minutes,
        #seconds {
            font-size: 48px;
            color: #8B5DA6;
            padding: 0 5px;
        }
        #custom-timer-input {
            padding: 8px;
            font-size: 16px;
            border: 2px solid #8B5DA6;
            border-radius: 4px 0 0 4px;
            outline: none;
            width: 80px;
        }
        #custom-timer-input:focus {
            border-color: #6C3483;
        }
        #set-custom-timer {
            padding: 8px 20px;
            font-size: 16px;
            background-color: #8B5DA6;
            color: white;
            border: none;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
        }
        #set-custom-timer:hover {
            background-color: #6C3483;
        }
        .button-container {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        .button-container button {
            padding: 12px 20px;
            font-size: 16px;
            background-color: #8B5DA6;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin: 0 10px;
        }
        .button-container button:hover {
            background-color: #6C3483;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            padding: 10px;
            border: 1px solid #ddd;
        }
        th {
            background-color: #f4f4f4;
        }
        .action-buttons button {
            margin-right: 5px;
        }   
    </style>
</head>
<body>
    <div class="sidebar">
        <div>
            <h2>Dashboard</h2>
            <div class="links">
                <a href="#" onclick="showDashboard()">Home</a>
                <a href="#" onclick="showNotes()">Notes</a>
                <a href="#" onclick="showTimer()">Timer</a>
                <a href="#" onclick="showToDoList()">To-Do List</a>
                <a href="#" onclick="showStudySession()">Study Session</a>
                <a href="#" onclick="showViewSchedule()">View Schedule</a>
            </div>
        </div>
        <div class="bottom-links">
            <a href="#">Profile</a>
            <a href="#">Settings</a>
            <a href="#">Logout</a>
        </div>
    </div>  
    <div class="main-content" id="dashboard">
        <div class="header">
            <h1>Welcome to Your Dashboard</h1>
        </div>
        <div class="card">
            <h2>Overview</h2>
            <p>This is the main dashboard where you can see an overview of your courses, assignments, and progress.</p>
        </div>
        <div class="grid">
            <div class="grid-item"><a href="#" onclick="showDashboard()"><img src="C:\Users\user\OneDrive\Desktop\hackathon\home.png" alt="Home">Home</a></div>
            <div class="grid-item"><a href="#" onclick="showNotes()"><img src="C:\Users\user\OneDrive\Desktop\hackathon\notes.png" alt="Notes">Notes</a></div>
            <div class="grid-item"><a href="#" onclick="showTimer()"><img src="C:\Users\user\OneDrive\Desktop\hackathon\timer.png" alt="Timer">Timer</a></div>
            <div class="grid-item"><a href="#" onclick="showToDoList()"><img src="C:\Users\user\OneDrive\Desktop\hackathon\task.png" alt="Task Management">To-Do List</a></div>
            <div class="grid-item"><a href="#" onclick="showStudySession()"><img src="C:\Users\user\OneDrive\Desktop\hackathon\studysesh.png" alt="Student Session">Study Session</a></div>
            <div class="grid-item"><a href="#" onclick="showViewSchedule()"><img src="C:\Users\user\OneDrive\Desktop\hackathon\schedule.png" alt="View Schedule">View Schedule</a></div>
        </div>
    </div>
    <div class="container" id="notes" style="display: none;">
        <h1>Upload Your Notes</h1>
        <form id="uploadForm">
            <div id="noteSections">
                <!-- Initial note section -->
                <div class="note-section">
                    <label for="noteTitle">Note Title:</label>
                    <input type="text" class="noteTitle" required>
                    <div class="file-inputs">
                        <label for="noteFiles">Upload Note Files (PDF only):</label>
                        <input type="file" class="noteFiles" accept=".pdf" multiple required>
                    </div>
                </div>
            </div>
            <button type="button" class="add-more-btn" onclick="addNoteSection()">Add More Notes</button>
            <button type="submit">Upload Notes</button>
        </form>
        <div id="noteDisplay">
            <h2>Uploaded Notes:</h2>
        </div>
    </div>
    <script>
        function addNoteSection() {
            var noteSections = document.getElementById('noteSections');
            var noteSection = document.createElement('div');
            noteSection.className = 'note-section';
            noteSection.innerHTML = `
                <label for="noteTitle">Note Title:</label>
                <input type="text" class="noteTitle" required>
                <div class="file-inputs">
                    <label for="noteFiles">Upload Note Files (PDF only):</label>
                    <input type="file" class="noteFiles" accept=".pdf" multiple required>
                </div>
            `;
            noteSections.appendChild(noteSection);
        }
        document.getElementById('uploadForm').addEventListener('submit', function(event) {
            event.preventDefault();
            var noteSections = document.querySelectorAll('.note-section');
            noteSections.forEach(function(section) {
                var title = section.querySelector('.noteTitle').value;
                var files = section.querySelector('.noteFiles').files;
                if (files.length > 0) {
                    for (var i = 0; i < files.length; i++) {
                        var file = files[i];
                        if (file.type === 'application/pdf') {
                            var reader = new FileReader();
                            reader.onload = (function(file, title) {
                                return function(e) {
                                    var content = e.target.result;
                                    displayNoteWithBlob(title, file);
                                };
                            })(file, title);
                            reader.readAsDataURL(file);
                        } else {
                            alert('Please upload a valid PDF file.');
                        }
                    }
                }
            });
        });
        function displayNoteWithBlob(title, file) {
            var displayDiv = document.getElementById('noteDisplay');
            var blob = new Blob([file], { type: 'application/pdf' });
            var url = URL.createObjectURL(blob);
            var noteDiv = document.createElement('div');
            noteDiv.className = 'note';
            noteDiv.innerHTML = `
                <h3>${title}</h3>
                <iframe src="${url}" type="application/pdf"></iframe>
                <button class="delete-btn" onclick="deleteNote(this)">Delete Note</button>
            `;
            displayDiv.appendChild(noteDiv);
        }
        function deleteNote(button) {
            var noteDiv = button.parentElement;
            noteDiv.remove();
        }
    </script>
    <div class="container" id="task-management" style="display: none;">
        <h1>To-Do List</h1>
    <form id="task-form">
        <input type="text" id="task-input" placeholder="Enter task" required>
        <input type="date" id="due-date-input" required>
        <button type="submit">Add Task</button>
    </form>
    <table id="task-table">
        <thead>
            <tr>
                <th>Task</th>
                <th>Due Date</th>
                <th>Status</th>
                <th>Action</th>
            </tr>
        </thead>
        <tbody id="task-list"></tbody>
    </table>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const taskForm = document.getElementById('task-form');
            const taskList = document.getElementById('task-list');
            const taskInput = document.getElementById('task-input');
            const dueDateInput = document.getElementById('due-date-input');
            taskForm.addEventListener('submit', (e) => {
                e.preventDefault();
                const task = taskInput.value;
                const dueDate = dueDateInput.value;
                if (task && dueDate) {
                    const tr = document.createElement('tr');
                    const taskTd = document.createElement('td');
                    taskTd.textContent = task;
                    const dueDateTd = document.createElement('td');
                    dueDateTd.textContent = dueDate;
                    const statusTd = document.createElement('td');
                    statusTd.textContent = 'In Progress';
                    const actionTd = document.createElement('td');
                    const inProgressButton = document.createElement('button');
                    inProgressButton.textContent = 'In Progress';
                    inProgressButton.style.display = 'none';
                    const doneButton = document.createElement('button');
                    doneButton.textContent = 'Done';
                    const deleteButton = document.createElement('button');
                    deleteButton.textContent = 'Delete';
                    doneButton.addEventListener('click', () => {
                        doneButton.style.display = 'none';
                        inProgressButton.style.display = 'inline';
                        statusTd.textContent = 'Done';
                    });
                    inProgressButton.addEventListener('click', () => {
                        inProgressButton.style.display = 'none';
                        doneButton.style.display = 'inline';
                        statusTd.textContent = 'In Progress';
                    });
                    deleteButton.addEventListener('click', () => {
                        taskList.removeChild(tr);
                    });
                    actionTd.appendChild(doneButton);
                    actionTd.appendChild(inProgressButton);
                    actionTd.appendChild(deleteButton);
                    tr.appendChild(taskTd);
                    tr.appendChild(dueDateTd);
                    tr.appendChild(statusTd);
                    tr.appendChild(actionTd);
                    taskList.appendChild(tr);
                    taskInput.value = '';
                    dueDateInput.value = '';
                }
            });
        });
    </script>
    </div>
    <div class="container" id="timer" style="display: none;">
        <h1>Task List with Timer</h1>
            <form id="task-form">
                <input type="text" id="task-input" placeholder="Enter a task">
                <button type="submit">Add Task</button>
            </form>
            <ul id="task-list"></ul>
            <div id="timer-container">
                <div>
                    <span id="minutes">25</span>:<span id="seconds">00</span>
                </div>
                <div>
                    <input type="number" id="custom-timer-input" placeholder="Set minutes" min="1">
                    <button id="set-custom-timer">Set Custom Timer</button>
                </div>
            </div>
            <div class="button-container">
                <button id="start-timer">Start Timer</button>
                <button id="stop-timer">Stop Timer</button>
                <button id="reset-timer">Reset Timer</button>
                <button id="short-break">Short Break</button>
                <button id="long-break">Long Break</button>
            </div>
            <script>
                document.addEventListener('DOMContentLoaded', () => {
                    const taskForm = document.getElementById('task-form');
                    const taskList = document.getElementById('task-list');
                    const taskInput = document.getElementById('task-input');
                    const startTimerButton = document.getElementById('start-timer');
                    const stopTimerButton = document.getElementById('stop-timer');
                    const resetTimerButton = document.getElementById('reset-timer');
                    const shortBreakButton = document.getElementById('short-break');
                    const longBreakButton = document.getElementById('long-break');
                    const setCustomTimerButton = document.getElementById('set-custom-timer');
                    const customTimerInput = document.getElementById('custom-timer-input');
                    let timer;
                    let minutes = 25;
                    let seconds = 0;
                    function updateTimerDisplay() {
                        document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
                        document.getElementById('seconds').textContent = String(seconds).padStart(2, '0');
                    }
                    function startTimer(duration) {
                        minutes = duration;
                        seconds = 0;
                        updateTimerDisplay();
                        if (timer) clearInterval(timer);
                        timer = setInterval(() => {
                            if (seconds === 0) {
                                if (minutes === 0) {
                                    clearInterval(timer);
                                    timer = null;
                                    alert('Time is up!');
                                } else {
                                    minutes -= 1;
                                    seconds = 59;
                                }
                            } else {
                                seconds -= 1;
                            }
                            updateTimerDisplay();
                        }, 1000);
                    }
                    taskForm.addEventListener('submit', (e) => {
                        e.preventDefault();
                        const task = taskInput.value;
                        if (task) {
                            const li = document.createElement('li');
                            li.textContent = task;
                            const deleteButton = document.createElement('button');
                            deleteButton.textContent = 'Delete';
                            deleteButton.addEventListener('click', () => {
                                taskList.removeChild(li);
                            });
                            li.appendChild(deleteButton);
                            taskList.appendChild(li);
                            taskInput.value = '';
                        }
                    });
                    startTimerButton.addEventListener('click', () => {
                        startTimer(25);
                    });
                    stopTimerButton.addEventListener('click', () => {
                        clearInterval(timer);
                        timer = null;
                    });
                    resetTimerButton.addEventListener('click', () => {
                        clearInterval(timer);
                        timer = null;
                        minutes = 25;
                        seconds = 0;
                        updateTimerDisplay();
                    });
                    shortBreakButton.addEventListener('click', () => {
                        startTimer(5);
                    });
                    longBreakButton.addEventListener('click', () => {
                        startTimer(15);
                    });
                    setCustomTimerButton.addEventListener('click', () => {
                        const customMinutes = parseInt(customTimerInput.value);
                        if (customMinutes > 0) {
                            startTimer(customMinutes);
                        } else {
                            alert('Please enter a valid number of minutes.');
                        }
                    });
                });
            </script>
    </div>
    <!-- JANGAN GANGGU CODE NI -->
    <script src="script.js"></script>
    <script>
        function showDashboard() {
            document.getElementById('dashboard').style.display = 'block';
            document.getElementById('notes').style.display = 'none';
            document.getElementById('task-management').style.display = 'none';
            document.getElementById('timer').style.display = 'none';
        }
        function showNotes() {
            document.getElementById('dashboard').style.display = 'none';
            document.getElementById('notes').style.display = 'block';
            document.getElementById('task-management').style.display = 'none';
            document.getElementById('timer').style.display = 'none';
        }
        function showToDoList() {
            document.getElementById('dashboard').style.display = 'none';
            document.getElementById('notes').style.display = 'none';
            document.getElementById('task-management').style.display = 'block';
            document.getElementById('timer').style.display = 'none';
        }
        function showTimer() {
            document.getElementById('dashboard').style.display = 'none';
            document.getElementById('notes').style.display = 'none';
            document.getElementById('task-management').style.display = 'none';
            document.getElementById('timer').style.display = 'block';
        }
        function addNoteSection() {
            var noteSections = document.getElementById('noteSections');
            var newNoteSection = document.createElement('div');
            newNoteSection.classList.add('note-section');
            newNoteSection.innerHTML = `
                <label for="noteTitle">Note Title:</label>
                <input type="text" class="noteTitle" required>
                <div class="file-inputs">
                    <label for="noteFiles">Upload Note Files (PDF only):</label>
                    <input type="file" class="noteFiles" accept=".pdf" multiple required>
                </div>
            `;
            noteSections.appendChild(newNoteSection);
        }
    </script>
</body>
</html>
