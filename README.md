<!DOCTYPE html>
<html lang="en">
<head>
    <title>Contact Form</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css">
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <div class="Contact-container">
        <h1>Contact Us</h1>
        <div class="contact-wrapper">
            <div class="Contact-form">
                <form action="">
                    <div class="form-group">
                        <input type="text" id="name" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" id="email" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <textarea name="message" id="message" rows="5" placeholder="Your message" required></textarea>
                    </div>
                    <button type="submit">Send Message</button>
                    <p class="status" id="statusMsg"></p>
                </form>
            </div>
            <div class="contact-info">
                <h2>Contact Information</h2>
                <p><i class="fas fa-phone"></i>+1 123 456 788</p>
                <p><i class="fas fa-envelope"></i>info@gmail.com</p>
                <p><i class="fas fa-map-marker alt"></i>148 Street, City, Country</p>
            </div>
        </div>
    </div>

    <script src="script.js"></script>

</body>
</html>
