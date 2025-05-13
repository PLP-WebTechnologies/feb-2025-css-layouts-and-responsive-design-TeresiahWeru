# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


/* Updated styles.css */

/* Global Styles */
body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  color: #333;
  line-height: 1.6;
}

h1 {
  color: #2c3e50;
  text-align: center;
  margin-bottom: 20px;
}

p {
  margin-bottom: 16px;
}

/* --- Navigation Bar --- */
.navbar {
  background-color: #34495e; /* Dark gray background */
  overflow: hidden;
  position: sticky; /* Stick to the top */
  top: 0;
  z-index: 100;
}

.navbar a {
  float: left;
  display: block;
  color: white;
  text-align: center;
  padding: 14px 20px;
  text-decoration: none;
  font-size: 1em;
}

.navbar a:hover {
  background-color: #2c3e50; /* Slightly darker on hover */
}

.navbar-brand {
  font-weight: bold;
  font-size: 1.2em;
}

.navbar-right {
  float: right;
}

/* Responsive Navbar */
@media screen and (max-width: 600px) {
  .navbar a {
    float: none;
    display: block;
    text-align: left;
  }
  .navbar-right {
    float: none;
  }
}


/* --- Main Content Area (Grid Layout) --- */
.main-content {
  display: grid;
  grid-template-columns: 1fr; /* Default: 1 column */
  gap: 30px;
  padding: 20px;
  max-width: 1200px; /* Maximum width for the container */
  margin: 0 auto; /* Center the container */
}

.intro {
  font-size: 1.1em;
  color: #555;
  line-height: 1.5;
  padding: 15px;
  border-left: 4px solid #3498db;
  background-color: #f9f9f9;
}

/* Image Styling */
img {
  border-radius: 8px;
  width: 100%; /* Make image responsive within its grid cell */
  height: auto;
  object-fit: cover;
}

/* Button Styling */
.button {
  background-color: #3498db;
  color: white;
  padding: 12px 25px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1em;
  transition: background-color 0.3s ease;
  margin-top: 10px;
}

.button:hover {
  background-color: #217dbb;
}

/* --- Sidebar (Flexbox) --- */
.sidebar {
  background-color: #ecf0f1; /* Light gray */
  padding: 20px;
  border-radius: 8px;
  /* Make it sticky */
  position: sticky;
  top: 80px; /* Adjust as needed based on navbar height */
  height: fit-content; /* Make it only as tall as its content */
}

.sidebar h3 {
  margin-bottom: 20px;
  color: #34495e;
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.sidebar li {
  margin-bottom: 10px;
}

.sidebar a {
  color: #3498db;
  text-decoration: none;
}

.sidebar a:hover {
  color: #217dbb;
}


/* --- Footer --- */
.footer {
  background-color: #2c3e50;
  color: white;
  text-align: center;
  padding: 20px;
  margin-top: 30px;
}


/* --- Media Queries for Responsiveness --- */

/* Tablet Layout (768px and up) */
@media screen and (min-width: 768px) {
  .main-content {
    grid-template-columns: 2fr 1fr; /* 2 columns: main, sidebar */
  }
  .navbar a {
    font-size: 1.1em;
  }
}

/* Desktop Layout (992px and up) */
@media screen and (min-width: 992px) {
  .main-content {
    grid-template-columns: 3fr 1fr; /* Wider main content on desktop */
  }
  .navbar a {
    font-size: 1.2em;
  }
}

/* Mobile Layout (below 768px) */
@media screen and (max-width: 767px) {
  .main-content {
    padding: 10px;
  }
  .navbar a {
    padding: 12px 15px;
    font-size: 1em;
  }
  .intro{
    padding: 10px;
  }
  img{
    width: 90%;
    height: auto;
  }
}

