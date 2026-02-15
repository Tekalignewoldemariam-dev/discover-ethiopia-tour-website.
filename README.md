# Discover Ethiopia Tour Website ET

Project Overview:

A fully functional tour booking website for Ethiopian travel destinations, built with a combination of frontend and backend technologies.



Quick Links:

View it live at:
https://github.com/Tekalignewoldemariam-dev/discover-ethiopia-tour-website
 GitHub Repository name is:
discover-ethiopia-tour-website
 URL: https://github.com/Tekalignewoldemariam-dev/discover-ethiopia-tour-website

Important Note: This is a dynamic PHP/MySQL website. GitHub Pages only hosts static sites, so the live demo will be  hosted on InfinityFree (free PHP hosting).

---

## 🛠️ Technologies Used

Technology :

HTML5(for Page structure ), CSS3(forStyling and layout ),JavaScript(for Interactive features ),PHP(for Backend logic ) ,Bootstrap (for Responsive design )


How HTML, CSS, JavaScript, and PHP Work Together

1. HTML + PHP Integration

In my PHP files, HTML provides the structure while PHP adds dynamic content:

```php
<!-- index.php -->
<!DOCTYPE html>
<html>
<head>
    <title>Discover Ethiopia</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <?php include 'includes/header.php'; ?>

    <!-- HTML section with PHP dynamic content -->
    <div class="tour-packages">
        <?php
        // PHP code to fetch tours from database
        $tours = getToursFromDatabase();
        foreach($tours as $tour) {
            echo '<div class="tour-card">';
            echo '<h3>' . $tour['name'] . '</h3>';
            echo '<p>' . $tour['description'] . '</p>';
            echo '</div>';
        }
        ?>
    </div>

    <script src="js/script.js"></script>
    <?php include 'includes/footer.php'; ?>
</body>
</html>




2. CSS Styling (style.css)



/ css/style.css /



.tour-card {
    border: 1px solid #ddd;
    padding: 20px;
    margin: 10px;
    border-radius: 8px;
    transition: transform 0.3s;
}

.tour-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
}

/ Responsive design /
@media (max-width: 768px) {
    .tour-card {
        margin: 5px;
        padding: 15px;
    }
}




3. JavaScript Interactivity (script.js)



// js/script.js
// Image slider functionality
document.addEventListener('DOMContentLoaded', function() {
    // Mobile menu toggle
    const menuToggle = document.querySelector('.menu-toggle');
    const navMenu = document.querySelector('.nav-menu');

    menuToggle.addEventListener('click', function() {
        navMenu.classList.toggle('active');
    });

    // Form validation
    const bookingForm = document.querySelector('#booking-form');
    if(bookingForm) {
        bookingForm.addEventListener('submit', validateForm);
    }
});

function validateForm(e) {
    // JavaScript form validation
    const name = document.querySelector('#name').value;
    if(name.length < 3) {
        alert('Please enter a valid name');
        e.preventDefault();
    }
}







How to Run This Project Locally



Step 1: Install Required Software


XAMPP (includes Apache, PHP, MySQL)

Web browser (Chrome, Firefox, etc.)

Git (optional, for cloning)




Step 2: Clone or Download




git clone https://github.com/Tekalignewoldemariam/discover-ethiopia-tour-website.git





Step 3: Move to XAMPP Directory



Copy the entire folder to: C:\xampp\htdocs\



Step 4: Start XAMPP


1.Open XAMPP Control Panel

2.Start Apache (for PHP)

3.Start MySQL (for database)


Step 5: Import Database:




1.Open browser and go to: http://localhost/phpmyadmin

2.Click "New" to create database

3.Name it: travel

4.Click "Import" tab

5.Choose file: /sql/travel.sql

6.Click "Go"


Step 6: Run the Website




Visit: http://localhost/discover-ethiopia-tour-website/admin





 Key Features Demonstrated:




Frontend (HTML/CSS/JavaScript):

✅ Responsive design (works on mobile, tablet, desktop)

✅ Image sliders and galleries

✅ Form validation

✅ Interactive UI elements

✅ CSS animations and transitions

✅ Bootstrap framework integration




Backend (PHP/MySQL):



✅ Dynamic content from database

✅ Tour booking system

✅ Admin panel for management

✅ Contact form processing

✅ User authentication

✅ Database CRUD operations




How Files Work Together:



User Request (index.php)
        ↓
HTML Structure (in PHP file)
        ↓
CSS Styling (/css/style.css) → JavaScript Interactions (/js/script.js)
        ↓
PHP Processing (/includes/functions.php)
        ↓
MySQL Database (/sql/database.sql)
        ↓
Dynamic Content Displayed



Author:



Tekalign Woldemariam

https://github.com/Tekalignewoldemariam-dev/discover-ethiopia-tour-website

GitHub: @Tekalignewoldemariam-dev

Project: discover-ethiopia-tour-website



 Information:



Project Type: Full Stack Web Application (HTML/CSS/JavaScript/PHP/MySQL)



