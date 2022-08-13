<template>
    <div>
        <div class="w-full bg-white">
            <section class="text-center bg-slate-400">
                <div class="mx-5">
                    <h1 class="max-w-screen-sm pb-3 text-2xl font-bold">VP Delivery Services PVT. LTD.</h1>
                    <p>Unit no. E/128, 1st Floor, Wooden boxes Mfg Co-Op ind. Estate, Above Satara Bank
                        Kailash ind. Complex, Park site
                        Behind Godrej Colony
                        VIkhroli (West) Mumbai, (Maharashtra-27) India-400079</p>
                    <p>GSTIN 27AAHCV3427GIZ9</p>
                </div>

            </section>

            <section class="mx-5">
                <h1 class="py-3 text-lg font-bold"> Invoice Details</h1>
                <div class="flex space-x-3">
 <div class="">
                    <h1 id="">Invoice Number</h1>
                    <input class="w-full h-10 pl-5 border-2 border-blue-300 rounded-md " placeholder="Invoice Number" required />
                </div>
                <div>
                    <h1>Invoice Date</h1>
                    <input class= "w-full h-10 border-2 border-blue-300 rounded-md" placeholder="Date" type="date" required />
                </div>

                <div>
                    <h1>Final Amount</h1>
                    <input class="w-full h-10 border-2 border-blue-300 rounded-md" placeholder="₹" v-model="total" type="number" required />
                </div>
                </div>
               
            </section>
            <section>
                <div class="mx-5 ">
                    <h1 class="pb-3 text-2xl font-bold ">Name and Address of Buyer</h1>
                    <div class="flex space-x-3">
                        <input class="w-full h-10 pl-5 border-2 border-blue-300 rounded-md" v-model="buyerName" placeholder="Enter Name" />
                      
                        <input class="w-full h-10 pl-5 border-2 border-blue-300 rounded-md" v-model="buyerNumber"
                            placeholder="Enter Number" />
                        <input class="w-full h-10 pl-5 border-2 border-blue-300 rounded-md" v-model="buyerMail" placeholder="Enter Email ID" />
                        <input class="w-full h-10 pl-5 border-2 border-blue-300 rounded-md" v-model="GSTIN" placeholder="Enter GST Number" />
                  
                    </div>
                            <input class="w-full h-10 pl-5 my-5 border-2 border-blue-300 rounded-md" v-model="buyerAddress"
                            placeholder="Enter Address" />
                            <button class="h-10 mb-3 bg-white border-2 border-blue-300 rounded"> Save Details</button>
                </div>
            </section>
        </div>  
</div>
</template>
<script>
export default {
    name: "sec1",
    data() {
        return {
            buyerName: '',
            buyerAddress: '',
            buyerNumber: '',
            buyerMail: '',
            supplyPlace: '',
        }
    },
    methods: {
        click() {
            console.log('printed')
        }
    }
}
</script>
<style>
/* {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
} */
.table td,
tr {
    border: 1px solid black;
}
</style>