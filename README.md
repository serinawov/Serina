<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Duggie Courses</title>
  <style>
    body { font-family: Arial; margin: 0; background: #f5f5f5; }
    header { background: #222; color: white; padding: 15px; text-align: center; }
    .container { padding: 20px; text-align: center; }
    .course { background: white; margin: 15px auto; padding: 20px; border-radius: 10px; width: 300px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    button { padding: 10px 15px; border: none; background: #007bff; color: white; border-radius: 5px; cursor: pointer; }
    button:hover { background: #0056b3; }
  </style>
</head>
<body>

<header>
  <h1>Duggie Online Courses</h1>
  <p>Learn & Grow 🚀</p>
</header>

<div class="container">
  <h2>Available Courses</h2>

  <div class="course">
    <h3>Course 1: Beginner Course</h3>
    <p>Price: FREE</p>
    <button onclick="accessCourse('Course 1')">Access</button>
  </div>

  <div class="course">
    <h3>Course 2: Intermediate Course</h3>
    <p>Price: ₹499</p>
    <button onclick="buyCourse('Course 2', 499)">Buy Now</button>
  </div>

  <div class="course">
    <h3>Course 3: Advanced Course</h3>
    <p>Price: ₹999</p>
    <button onclick="buyCourse('Course 3', 999)">Buy Now</button>
  </div>

</div>

<script>
  function accessCourse(course) {
    alert('Opening ' + course);
  }

  function buyCourse(course, price) {
    alert('Redirecting to payment for ' + course + ' (₹' + price + ')');
  }
</script>

</body>
</html>
