<template>
    <br>
    
    <div class="flex justify-center">
    
        <img
          src="~assets/img/rent/R17-main-room-image.jpeg"
          width="500"
          alt="ROOM IMAGE"
      />
    </div>
    <br>
    <section>
    <div class="container">
      <div class="button-container">
        <button 
        @click="showContent(1)"
        :class="{'active-button': activeButton === 1}">
        Details
        </button>
    
      </div>
      
      <div v-if="activeButton === 1" class="text-post">
        <!-- Content for Button 1 -->
        <p>Call Justine  , For more information.</p>
        <p>Whatapps: 018 389 6589</p>
        <p>*10%  referral fee</p>
        <br>
        <p>FOR RENT LD LAGENDA studio unit </p>
        <br>
        <p>walking distance to Sarawak General Hospital</p>
        <br>
        <p>Immediate Availability</p>
        <p>>> Renting Price: <b>RM 900</b> / month</p>
        <br>
        <p>Disclaimer: Please obtain details from our sales person. </p>
        <p>Information in ad may not be fully descriptive.</p>
        <p>Apologize for any inconvenient cause. Thank you.</p>

        <br>
        <!--TABLE-->
        <table>
          <thead>
            <tr>
              <th colspan="2"> BUILDING DETAILS </th>
            </tr>
            <tr>
              <td style="width: 40%">Rental Period</td>
              <td style="width: 60%">Monthly</td>
            </tr>
            <tr>
              <td >Level</td>
              <td > </td>
            </tr>
            <tr>
              <td >Window View</td>
              <td > </td>
            </tr>
            <tr>
              <td >Furnishing</td>
              <td >Fully Furnished</td>
            </tr>
            <tr>
              <td >Carpark</td>
              <td >No</td>
            </tr>
            <tr>
              <td >Washing Machine</td>
              <td > </td>
            </tr>
          </thead>
        </table>
        </div>
    </div>
    </section>
    
    <section class="py-6">
          <router-link
            to="/rent"
            class="
              inline-flex
              items-center
              justify-center
              w-full
              px-3
              py-3
              text-white
              transition
              rounded
              sm:px-0
              hover:bg-blue-600
              bg-blue-300
            "
          >
            Back to Rent
          </router-link>
        </section>
    </template>
    <script>
    export default {
    data() {
      return {
        activeButton: 1,
      };
      },
    methods: {
      showContent(buttonNumber) {
        this.activeButton = buttonNumber;
      },
      selectImage(imagePath) {
      this.activeImage = imagePath; // Update the activeImage property with the clicked thumbnail
    
    }
    }
    }
    
    </script>
    
    <style scoped>
    
    .active-button{
    border-bottom: 2px solid rgb(132, 158, 190);
    color: blacks;
    }
    .button-container {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
    }
    
    .button-container button {
    
    padding: 5px 10px;
    margin: 5px;
    /* Optional: Set a background color for the buttons */
    }
    .container {
    border: 3px solid rgb(132, 158, 190);
    padding: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: left;
    max-width: 650px; /* Adjust the max width as needed */
    margin: auto;
    height: auto; /* Make the container take up the full viewport height */
    }
    .text-post{
    text-align: left;
    }
    
    /* Style for tables */
    .container table {
    border-collapse: collapse;
    width: 100%; /* Set the width to 100% to fill the container */
    border: 1px solid rgb(132, 158, 190); /* Add a border to the table */
    }
    
    /* Style for table headers */
    .container th {
    border: 1px solid rgb(132, 158, 190); /* Add a border to table headers */
    padding: 4px;
    width: 40%; /* Adjust the width as needed */
    }
    
    /* Style for table cells */
    .container td {
    border: 1px solid rgb(132, 158, 190); /* Add a border to table cells */
    padding: 10px;
    width: 40%; /* Adjust the width as needed */
    }
    /* Add your component-specific CSS styles here */
    
    </style>
    