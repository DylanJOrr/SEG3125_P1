<script>
     /**
      * @type {String}
      */
     export let email = "name@example.com";
</script>

<section class="order-form m-4 vh-100">
<div class="container pt-     ">
     <div class="row">
          <div class="col-12 px-4">
               <h1>Appointment Confirmed.</h1>
               <h2>An email confirmation has been sent to you at:</h2>
               <h3 class="py-2 text-primary">{email}</h3>
               <hr class="mt-1" />
               <h5 class="text-center">We'll get back to you as soon as possible.</h5>
          </div>
     </div>
     <div class="d-flex justify-content-center">
          <i class="fa-regular fa-circle-check fa-8x p-5 text-success"></i>
     </div>
     <div class="text-center">
          <h4><a href="./login">Log in</a> if you want to check upcoming appointments!</h4>
     </div>
</div>
</section>

<style>
     .order-form .container {
      color: #4c4c4c;
      padding: 20px;
      box-shadow: 0 0 10px 0 rgba(0, 0, 0, .1);
      max-width: 650px;
    }

    .order-form-label {
      margin: 8px 0 0 0;
      font-size: 14px;
      font-weight: bold;
    }

     .order-form-input,
     .form-label,
     .form-check-label {
      font-family: 'Open Sans', sans-serif;
      font-size: 14px;
    }

    .btn-submit:hover {
      background-color: #0D47A1 !important;
    }
</style>