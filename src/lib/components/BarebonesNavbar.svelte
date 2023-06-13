<script>
     import { base } from '$app/paths';

     let user = {
          id: "",
          username: "",
          loggedin: false,
     }
</script>

<nav class="navbar navbar-expand-lg bg-dark navbar-dark sticky-top">
  <div class="container-fluid">
    <a class="navbar-brand ms-5" style="padding: var(--bs-nav-link-padding-y);" href="{base}/">TechFix</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mx-5 justify-content-evenly container-sm">
               <li class="nav-item">
                    <a class="nav-link" href="{base}/parts">Parts</a>
               </li>
               <li class="nav-item">
                    <a class="nav-link" href="{base}/guides">Guides</a>
               </li>
               <li class="nav-item">
                    <a class="nav-link" href="/#scrollspyHeadingExperts">Experts</a>
               </li>
               <li class="nav-item">
                    <a class="nav-link" href="{base}/contact">Repairs</a>
               </li>
               <li class="nav-item">
                    <a class="nav-link" href="/#scrollspyHeadingAbout">About</a>
               </li>
               <li class="nav-item">
                    <a class="nav-link" href="#">Orders</a>
               </li>
               <li class="nav-item">
                    <a class="nav-link" href="#">Messages</a>
               </li>
          </ul>
     <!-- <form class="d-flex" role="search">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Search</button>
     </form> -->
     </div>
     {#if !user.loggedin}
          <a class="btn btn-outline-primary m-1" type="button" href="{base}/login">Log In</a>
          <a class="btn btn-primary m-1" type="button" href="{base}/login">Sign Up</a>
     {:else}
          <!-- Profile Icon -->
     {/if}
  </div>
</nav>