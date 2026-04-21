<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Course Store</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: white;
      text-align: center;
    }
    .container {
      padding: 20px;
    }
    .course-preview {
      border: 1px solid #ddd;
      padding: 15px;
      border-radius: 10px;
      max-width: 600px;
      margin: auto;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    iframe {
      width: 100%;
      height: 400px;
      border: none;
    }
    .locked {
      filter: blur(5px);
      pointer-events: none;
    }
    button {
      margin-top: 15px;
      padding: 10px 20px;
      background: black;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>My Course</h1>

  <div class="course-preview">
    <iframe id="courseFrame" src="https://canva.link/jwwtfdsjiy654jf"></iframe>
    <div id="lockOverlay">
      <p>🔒 Full course locked. Pay $25 to unlock.</p>
      <button onclick="payNow()">Buy Now</button>
    </div>
  </div>
</div>

<script>
  const coursePrice = 25;

  function payNow() {
    let email = prompt("Enter your email to continue:");
    if (!email) return;

    // Simulated payment (replace with real gateway like Stripe/Razorpay)
    let confirmPay = confirm("Pay $" + coursePrice + " to unlock?");

    if (confirmPay) {
      localStorage.setItem("paidUser", email);
      alert("Payment successful! Course unlocked.");
      unlockCourse(email);
    }
  }

  function unlockCourse(email) {
    document.getElementById("lockOverlay").style.display = "none";
    document.getElementById("courseFrame").classList.remove("locked");
  }

  function checkAccess() {
    let savedEmail = localStorage.getItem("paidUser");
    if (savedEmail) {
      unlockCourse(savedEmail);
    }
  }

  checkAccess();
</script>

</body>
</html>
