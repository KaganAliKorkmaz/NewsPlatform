
<h1>News Platform – Full-Stack Web Application</h1>

<h2> Overview</h2>
<p>
This project is a <strong>full-stack web application</strong> developed to practice and demonstrate
backend and frontend development concepts.
It provides a dynamic platform where <strong>News</strong> and <strong>Announcements</strong> can be managed
through an admin panel and displayed to end users in real time.
</p>
<p>
The system focuses on clean architecture, modern web technologies, and real-world patterns such as
inheritance mapping, real-time updates, and responsive UI design.
</p>

<h2> Tech Stack</h2>

<h3>Backend</h3>
<ul>
    <li><strong>Java 17</strong></li>
    <li><strong>Spring Boot 3.4.5</strong>
        <ul>
            <li>Spring Web</li>
            <li>Spring Data JPA</li>
            <li>Spring WebSocket</li>
        </ul>
    </li>
    <li><strong>Hibernate / JPA</strong></li>
    <li><strong>MySQL</strong></li>
    <li><strong>Lombok</strong></li>
    <li><strong>Maven</strong></li>
</ul>

<h3>Frontend</h3>
<ul>
    <li><strong>React 19</strong></li>
    <li><strong>Vite 6</strong></li>
    <li><strong>Tailwind CSS 4</strong></li>
    <li><strong>Axios</strong></li>
    <li><strong>React Router 7</strong></li>
    <li><strong>WebSocket (SockJS + STOMP)</strong></li>
</ul>

<h2> Features</h2>
<ul>
    <li>
        News and Announcements are modeled using an abstract
        <code>Event</code> class and persisted with
        <strong>Single Table Inheritance</strong>
    </li>
    <li>
        <strong>News</strong>
        <ul>
            <li>Title</li>
            <li>Content</li>
            <li>Validity date</li>
            <li>External link</li>
        </ul>
    </li>
    <li>
        <strong>Announcements</strong>
        <ul>
            <li>Title</li>
            <li>Content</li>
            <li>Validity date</li>
            <li>Image upload (file system based)</li>
        </ul>
    </li>
    <li><strong>Admin Panel:</strong> Create, update, and delete News and Announcements</li>
    <li>
        <strong>User Interface:</strong>
        <ul>
            <li>List view with search and sorting</li>
            <li>Popup-based detailed content display</li>
        </ul>
    </li>
    <li>
        <strong>Real-Time Updates:</strong>
        New announcements are pushed instantly to all connected clients via WebSocket
    </li>
    <li><strong>Responsive Design:</strong> Mobile, tablet, and desktop compatible</li>
</ul>

<h2> Requirements</h2>
<ul>
    <li>Java 17+</li>
    <li>Maven 3.6+</li>
    <li>Node.js 18+ and npm 8+</li>
    <li>MySQL database</li>
</ul>

<h2> Setup &amp; Run</h2>

<h3>1. Database Configuration</h3>
<pre>
CREATE DATABASE projedb;
CREATE USER 'springuser'@'localhost' IDENTIFIED BY 'springpass';
GRANT ALL PRIVILEGES ON projedb.* TO 'springuser'@'localhost';
FLUSH PRIVILEGES;
</pre>

<p>
Update backend configuration in
<code>backend/src/main/resources/application.properties</code>:
</p>

<pre>
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/projedb
spring.datasource.username=springuser
spring.datasource.password=springpass
</pre>

<h3>2. Backend</h3>
<pre>
cd backend
mvn clean install
mvn spring-boot:run
</pre>

<p>Backend runs on <code>http://localhost:8082</code></p>

<h3>3. Frontend</h3>
<pre>
cd frontend
npm install
npm run dev
</pre>

<p>Frontend runs on <code>http://localhost:5173</code></p>

<h2> Usage</h2>

<h3>Admin Account</h3>
<ul>
    <li><strong>Username:</strong> admin123</li>
    <li><strong>Password:</strong> 123456</li>
</ul>

<h3>URLs</h3>
<ul>
    <li><code>http://localhost:5173/</code> – User Interface</li>
    <li><code>http://localhost:5173/admin</code> – Admin Panel</li>
    <li><code>http://localhost:8082</code> – Backend API</li>
</ul>

<h2> Documentation</h2>
<ul>
    <li><strong>Backend Notes:</strong> backend/HELP.md</li>
    <li><strong>Frontend Notes:</strong> frontend/README.md</li>
</ul>


</body>
</html>
