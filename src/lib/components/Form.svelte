<script>
     /** @type {boolean} */
     export let formSubmitted = false;

     export let formInfo = {
          firstname: '',
          lastname: '',
          email: '',
          phone: '',
          service: '',
          specialist: '',
          date: '',
          notes: ''
     };

     const submitContactForm = () => {
          console.log(formInfo);
          if (validateForm()) {
               formSubmitted = true;
          } else {
               alert("Please fill out all forms correctly.");
          }
     }

     const validateEmail = () => {
          return String(formInfo.email)
          .toLowerCase()
          .match(
               /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|.(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
          );
     };

     const validatePhone = () => {
          return String(formInfo.phone).match(
               /^[\+]?[(]?[0-9]{3}[)]?[-\s\.]?[0-9]{3}[-\s\.]?[0-9]{4,6}$/im
          );
     }

     const validateForm = () => {
          return validateEmail() 
          && formInfo.firstname.replace(/\s/g, '') != '' 
          && formInfo.lastname.replace(/\s/g, '') != '' 
          && validatePhone()
     }
</script>

<section class="order-form m-4 rounded">
<div class="container pt-4">
     <div class="row">
     <div class="col-12 px-4">
          <h1>Book an appointment,</h1>
          <span>Or just get a quote.</span>
          <hr class="mt-1" />
     </div>

     <div class="col-12">
          <form method="POST" class="row mx-4">
               <div class="col-12">
                    <label class="order-form-label">Name</label>
               </div>
               <div class="col-sm-6">
                    <div class="form-outline">
                         <input type="text" id="form1" class="form-control order-form-input" bind:value={formInfo.firstname}/>
                         <label class="form-label" for="form1">First</label>
                    </div>
               </div>
               <div class="col-sm-6 mt-2 mt-sm-0">
                    <div class="form-outline">
                         <input type="text" id="form2" class="form-control order-form-input" bind:value={formInfo.lastname}/>
                         <label class="form-label" for="form2">Last</label>
                    </div>
               </div>
          </form>

          <div class="row mx-4">
               <div class="">
                    <label for="exampleInputEmail1" class="order-form-label">Email address</label>
                    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="name@example.com" bind:value={formInfo.email}>
                    <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
               </div>
               <div class="">
                    <label for="exampleInputEmail1" class="order-form-label">Phone Number</label>
                    <input type="phone" class="form-control" id="exampleInputPhone1" aria-describedby="phoneHelp" placeholder="+1" bind:value={formInfo.phone}>
                    <div id="phoneHelp" class="form-text">We'll never share your phone number with anyone else.</div>
               </div>
               <div class="col-12 mt-3">
                    <div class="row">
                         <div class="col-12">
                              <label class="order-form-label">Service</label>
                              <select id="serviceSelect" class="form-select">
                                   <option>Quote</option>
                                   <option>Phone Repair</option>
                                   <option>Laptop Repair</option>
                                   <option>General Repair</option>
                                   <option>Diagnostic Session</option>
                                   <option>I don't know</option>
                              </select>
                         </div>
                    </div>
               </div>
               <div class="col-12">
                    <div class="row">
                         <div class="col-12">
                              <label class="order-form-label">Specialist</label>
                              <select id="specialistSelect" class="form-select" disabled>
                                   <option>Any</option>
                                   <option>Sarah</option>
                                   <option>Emily</option>
                              </select>
                         </div>
                    </div>
               </div>
          </div>

          <div class="row mx-4">
               <div class="col-12">
                    <label class="order-form-label" for="date-picker-example">Date</label>
               </div>
               <div class="col-12">
                    <div class="form-outline datepicker" data-mdb-toggle-button="false">
                    <div class="input-group date" id="datepicker">
                         <input id="startDate" class="form-control" type="date" disabled/>
                    </div>
                    </div>
               </div>
          </div>

          <div class="row mt-3 mx-4">
               <div class="col-12">
                    <label class="order-form-label">Additional Notes</label>
               </div>
               <div class="col-12">
                    <div class="mb-3">
                         <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" bind:value={formInfo.notes}></textarea>
                    </div>
               </div>
          </div>

          <div class="row mt-3">
               <div class="col-12">
                    <button type="button" id="btnSubmit" class="btn btn-primary d-block mx-auto btn-submit" on:click={submitContactForm}>Submit</button>
               </div>
          </div>
     </div>
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