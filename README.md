<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Clothing Products - Coming Soon</title>

    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap"
      rel="stylesheet"
    />

    <style>
      body {
        background: url("https://img.freepik.com/free-vector/hand-drawn-fashion-shop-pattern-background_23-2150849915.jpg")
          no-repeat center center fixed;
        background-size: cover;
        display: flex;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        margin: 0;
        font-family: "Poppins", sans-serif;
        color: #333;
        padding: 1rem;
      }
      main {
        width: 100%;
        max-width: 650px;
        padding: 2rem;
        background: rgba(255, 255, 255, 0.9);
        border-radius: 16px;
        box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
        animation: fadeInUp 1s ease-in-out;
        backdrop-filter: blur(6px);
      }
      main h1 {
        font-weight: 600;
        font-size: 2.2rem;
        color: #0d6efd;
        text-align: center;
        margin-bottom: 1.5rem;
      }
      .product-section {
        margin-bottom: 1.5rem;
        padding: 1rem;
        background: #f8f9fa;
        border-radius: 12px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      }
      .product-section h2 {
        font-size: 1.4rem;
        font-weight: 600;
        margin-bottom: 0.5rem;
        color: #333;
      }
      .product-section p {
        font-size: 1rem;
        color: #555;
        margin: 0;
      }
      form {
        margin-top: 2rem;
        text-align: center;
      }
      .confirmation-message {
        display: none;
        margin-top: 1rem;
        color: #198754;
        font-weight: 500;
      }
      @keyframes fadeInUp {
        from {
          opacity: 0;
          transform: translateY(30px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      @media (max-width: 576px) {
        main {
          padding: 1.5rem;
        }
        main h1 {
          font-size: 1.8rem;
        }
        .product-section h2 {
          font-size: 1.2rem;
        }
        .product-section p {
          font-size: 0.9rem;
        }
        form {
          flex-direction: column !important;
        }
        form button {
          width: 100%;
        }
      }
    </style>
  </head>
  <body>
    <main>
      <h1>Clothing Products</h1>

      <div class="product-section">
        <h2>Pants</h2>
        <p>Stylish and comfortable pants for every occasion.</p>
      </div>

      <div class="product-section">
        <h2>Shirts</h2>
        <p>Trendy shirts designed for both casual and formal wear.</p>
      </div>

      <div class="product-section">
        <h2>Jackets</h2>
        <p>Durable jackets to keep you warm and fashionable.</p>
      </div>

      <form id="subscribe-form" class="d-flex flex-column flex-sm-row gap-2">
        <input
          type="email"
          class="form-control"
          placeholder="Enter your email"
          required
        />
        <button type="submit" class="btn btn-primary px-4">Subscribe</button>
      </form>

      <div class="confirmation-message">Thanks for subscribing!</div>
    </main>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

    <script>
      $(document).ready(function () {
        $("#subscribe-form").on("submit", function (e) {
          e.preventDefault();
          $(".confirmation-message").fadeIn().delay(3000).fadeOut();
          $(this).trigger("reset");
        });
      });
    </script>
  </body>
</html>
