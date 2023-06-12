<script>
	 import Footer from "./Footer.svelte";
	 import Navbar from "./Navbar.svelte";
	 import About from "./home-sections/About.svelte";
	 import Appointments from "./home-sections/Appointments.svelte";
	 import Experts from "./home-sections/Experts.svelte";
	 import Parts from "./home-sections/Parts.svelte";
	 import Repairs from "./home-sections/Repairs.svelte";
</script>

<Navbar />

<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<div data-bs-spy="scroll" data-bs-target="#navbar-example2" data-bs-root-margin="0px 0px -40%" data-bs-smooth-scroll="true" class="scrollspy-example bg-body-tertiary mx-0 d-flex flex-column" tabindex="0">
     <section id="scrollspyHeadingNews scrollspyHeadingHome" class="parts home-section bg-dark text-light p-5 pt-lg-5 text-center text-sm-start d-flex flex-column justify-content-center" style="height: 60vh;">
          <div class="container">
          <div class="d-sm-flex align-items-center justify-content-between">
          <div>
               <h1>Make What You Own <span class="text-warning"> YOURS </span></h1>
               <h3 class="me-5">At TechFix, we firmly believe that unless you can repair something yourself, or choose who you want to repair it, you don't own it.</h3>
               <p class="lead my-4 opacity-75">
               Looking for parts, repair guides or repair servies?
               </p>
               <button class="btn btn-primary btn-lg" data-bs-toggle="modal" data-bs-target="#enroll">
               Learn More
               </button>
          </div>
          </div>
          </div>
     </section>

     <Parts />

     <Repairs />

     <Experts />

     <Appointments />

     <About />
</div>

<Footer />