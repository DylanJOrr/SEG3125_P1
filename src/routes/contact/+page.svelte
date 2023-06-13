<script>
     import BarebonesNavbar from "../../lib/components/BarebonesNavbar.svelte";
     import Footer from "../../lib/components/Footer.svelte";
     import Form from "../../lib/components/Form.svelte";
	import FormSubmitted from "../../lib/components/FormSubmitted.svelte";

     /** @type {boolean} */
     let formSubmitted = false;

     let formInfo = {
          firstname: '',
          lastname: '',
          email: '',
          phone: '',
          service: '',
          specialist: '',
          date: '',
          notes: ''
     };
     
</script>

<BarebonesNavbar />

{#if !formSubmitted}
     <Form bind:formInfo={formInfo} bind:formSubmitted={formSubmitted}/>
{:else}
     <FormSubmitted bind:email={formInfo.email}/>
{/if}

<Footer />