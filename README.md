# Grade Statistics Distributed System

A comprehensive web application for managing student grades, equipped with chat and video chat functionalities to facilitate communication, built with Node.js, Express, Socket.IO, MySQL and WebRTC. It allows professors and administrators to manage student grades, enroll students in subjects, view overall grade statistics, message in groupchats and privately.

## Features

- **User Management**: Handle professor and admin logins.
- **Student Management**: Add, search, and manage students.
- **Enrollment**: Enroll students in subjects.
- **Grading**: Save and retrieve grades for students.
- **Statistics**: View overall grade statistics.
- **Real-time Video Chat**: Users can join a room and engage in live video conversations.
- **Text Chat**: Users can send and receive text messages within the room.
- **Screen Sharing**: Users can share their screen with other participants.
- **Mute/Unmute Microphone**: Users can mute or unmute their microphone.
- **Toggle Video**: Users can show or hide their video stream.
- **Join/Leave Notifications**: Notifications for when users join or leave the chat room.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/502ermira/Grading-System.git
    cd Grading-System
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

3. Set up your MySQL database and update the `connection` configuration in the code:
    ```javascript
    const connection = mysql.createConnection({
      host: 'localhost',
      user: 'root',
      password: '',
      database: 'Ushtrime1',
    });
    ```

4. Start the server:
    ```bash
    node server.js
    ```

## Usage

- Access the application at `http://localhost:3000`
- Use the provided endpoints and socket events to interact with the system.

## Endpoints

- `GET /video`: Serve the video call page.

## Socket Events

### User Events

- `new-user-joined`: Notify server of a new user joining.
- `message-sended`: Send a message to all users.
- `pvt-message-sended`: Send a private message to a specific user.
- `disconnect`: Notify server of a user disconnecting.

### Student Events

- `addStudent`: Add a new student.
- `searchStudents`: Search for students by ID, name, or lastname.
- `getStudentsBySubject`: Get students enrolled in a specific subject.
- `saveGrade`: Save a grade for a student.

### Professor Events

- `addProfessor`: Add a new professor.
- `professorLogin`: Handle professor login.

### Admin Events

- `adminLogin`: Handle admin login.

### Enrollment Events

- `enrollStudents`: Enroll students in a subject.

### Grade Statistics Events

- `getOverallGradeStatistics`: Get overall grade statistics for all students.

