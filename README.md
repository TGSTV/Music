<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Industry Business Platform</title>
    <!-- Add CSS link here -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navigation Bar -->
    <nav>
        <div class="logo">
            <h1>MusicBiz</h1>
        </div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#marketplace">Marketplace</a></li>
            <li><a href="#contact">Contact</a></li>
            <li><a href="#profile">Profile</a></li>
        </ul>
        <div class="auth-links">
            <a href="#login">Login</a>
            <a href="#signup">Sign Up</a>
        </div>
    </nav>

    <!-- Home Section -->
    <section id="home">
        <div class="home-content">
            <h2>Welcome to MusicBiz</h2>
            <p>The ultimate platform for all your music industry needs.</p>
            <a href="#signup" class="btn">Join Now</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2>Our Services</h2>
        <div class="service-grid">
            <div class="service-item">
                <h3>Music Artists</h3>
                <p>Connect with top music artists for your next project.</p>
            </div>
            <div class="service-item">
                <h3>Producers</h3>
                <p>Find skilled producers to bring your music to life.</p>
            </div>
            <div class="service-item">
                <h3>Videographers</h3>
                <p>Hire professional videographers for your music videos.</p>
            </div>
            <div class="service-item">
                <h3>Photographers</h3>
                <p>Get stunning photographs for your album covers and events.</p>
            </div>
            <div class="service-item">
                <h3>Dancers</h3>
                <p>Collaborate with talented dancers for performances and videos.</p>
            </div>
            <div class="service-item">
                <h3>Singers</h3>
                <p>Find vocalists to feature in your tracks and live performances.</p>
            </div>
            <div class="service-item">
                <h3>Models</h3>
                <p>Hire models for your music videos, promotions, and events.</p>
            </div>
            <div class="service-item">
                <h3>Radio Stations</h3>
                <p>Get your music played on popular radio stations.</p>
            </div>
            <div class="service-item">
                <h3>TV Stations</h3>
                <p>Promote your music on leading TV stations.</p>
            </div>
            <div class="service-item">
                <h3>DJs</h3>
                <p>Book DJs for your events and remix your tracks.</p>
            </div>
        </div>
    </section>

    <!-- Marketplace Section -->
    <section id="marketplace">
        <h2>Marketplace</h2>
        <div class="marketplace-grid">
            <!-- Repeat this block for each marketplace item -->
            <div class="marketplace-item">
                <img src="placeholder.jpg" alt="Service">
                <h3>Service Name</h3>
                <p>Short description of the service.</p>
                <a href="#details" class="btn">View Details</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Us</h2>
        <form action="/send-message" method="POST">
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn">Send Message</button>
        </form>
    </section>

    <!-- Profile Section -->
    <section id="profile">
        <h2>Your Profile</h2>
        <!-- Profile details and edit options will go here -->
    </section>

    <!-- Login Modal -->
    <div id="login" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2>Login</h2>
            <form action="/login" method="POST">
                <div class="form-group">
                    <label for="login-email">Email:</label>
                    <input type="email" id="login-email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="login-password">Password:</label>
                    <input type="password" id="login-password" name="password" required>
                </div>
                <button type="submit" class="btn">Login</button>
            </form>
        </div>
    </div>

    <!-- Signup Modal -->
    <div id="signup" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2>Sign Up</h2>
            <form action="/signup" method="POST">
                <div class="form-group">
                    <label for="signup-name">Name:</label>
                    <input type="text" id="signup-name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="signup-email">Email:</label>
                    <input type="email" id="signup-email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="signup-password">Password:</label>
                    <input type="password" id="signup-password" name="password" required>
                </div>
                <button type="submit" class="btn">Sign Up</button>
            </form>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 MusicBiz. All rights reserved.</p>
    </footer>

    <!-- JavaScript for modal functionality -->
    <script>
        const loginModal = document.getElementById('login');
        const signupModal = document.getElementById('signup');
        const closeBtns = document.querySelectorAll('.close-btn');

        closeBtns.forEach(btn => {
            btn.onclick = function() {
                loginModal.style.display = 'none';
                signupModal.style.display = 'none';
            };
        });

        window.onclick = function(event) {
            if (event.target === loginModal) {
                loginModal.style.display = 'none';
            } else if (event.target === signupModal) {
                signupModal.style.display = 'none';
            }
        };
    </script>
</body>
</html>
