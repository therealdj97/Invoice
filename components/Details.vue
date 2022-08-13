    <template>
    <div>
        <section class="space-y-3">
            <h1 class="px-5 py-3 text-xl font-bold text-left bg-stone-500">Description of Services</h1>
            <table class="flex flex-col justify-between">
                <tr class="">
                    <th class="no">
                        <h1 id="no">Invoice Number</h1>
                        <input id placeholder="Invoice Number" required />
                    </th>
            
                    <th>
                        <h1>No of items</h1>
                        <input placeholder="units" type="number" required />
                    </th>
                    <th>
                        <h1>Invoice Date</h1>
                        <input placeholder="Date" type="date" required />
                    </th>
                
                    <th>
                        <h1>Final Amount</h1>
                        <input placeholder="₹" v-model="total" type="number" required />
                    </th>
                </tr>
                <tr>
                    <th>
                        <h2>No</h2>
                        <input class placeholder="No" type="number" />
                    </th>
                    <th>
                        <h2>Description</h2>
                        <input class placeholder v-model="Description" type="text" />
                    </th>
                    <th>
                        <h2>HSN/SAC Code</h2>
                        <input class placeholder="No" v-model="HSN_SAC" type="text" />
                    </th>
                    <th>
                        <h2>Quantity</h2>
                        <input class placeholder="No" v-model="Quantity" type="number" />
                    </th>
                    <th>
                        <h2>Unit</h2>
                        <input class placeholder="No" v-model="Unit" type="number" />
                    </th>
                    <th>
                        <h2>Rate</h2>
                        <input class placeholder="No" v-model="Rate" type="number" />
                    </th>
                    <th>
                        <h2>Taxable Amount</h2>
                        <input class placeholder="No" v-model="taxableAmount" type="number" />
                    </th>
                    <th>
                        <div class="flex space-x-3">
                            <h2>CGST</h2>
                            <h2>Rate</h2>
                            <h2>Amount</h2>
                        </div>

                        <div class="flex w-40">
                            <input class="w-1/2" placeholder="No" v-model="cgstRate" type="number" />

                            <input
                                class="w-1/2"
                                placeholder="No"
                                v-model="cgstAmount"
                                type="number"
                            />
                        </div>
                    </th>
                    <th>
                        <div class="flex space-x-3">
                            <h2>SGST</h2>
                            <h2>Rate</h2>
                            <h2>Amount</h2>
                        </div>

                        <div class="flex w-40">
                            <input class="w-1/2" placeholder="No" v-model="sgstRate" type="number" />

                            <input
                                class="w-1/2"
                                placeholder="No"
                                v-model="sgstAmount"
                                type="number"
                            />
                        </div>
                    </th>
                    <th>
                        <h2>Total</h2>
                        <h1>{{ Total }}</h1>
                        <input class placeholder="No" v-model="total" type="number" />
                    </th>
                </tr>
            </table>
            <section class="flex justify-between">
                <table>
                    <tr class="flex">
                        <th class="space-y-2">
                            <h1>Amount</h1>
                            <h1>CGST</h1>
                            <H1>SGST</H1>
                        </th>
                        <th class="space-y-2">
                            <input class="ml-3" placeholder=" Amount in text" type="string" />
                            <br />
                            <input class="ml-3" placeholder="CGST Amount in text" type="string" />
                            <br />
                            <input class="ml-3" placeholder="SGST Amount in text" type="string" />
                            <br />
                        </th>

                        <th>
                            <h1 class="pr-2">Total Amount(before Tax) ₹ :</h1>
                            {{ taxableAmount }} ₹
                        </th>
                    </tr>
                </table>
                <table class="">
                    <tr class="flex justify-between">
                        <th>CGST</th>
                        <th>SGST</th>
                        <th>IGST</th>
                        <th>Cess</th>
                    </tr>
                    <tr class="flex justify-between">
                        <th>
                            <h1 class="w-10">{{ cgstAmount }}</h1>
                        </th>
                        <th>
                            <h1 class="w-10">{{ sgstAmount }}</h1>
                        </th>
                        <th>
                            <input class="w-10 " placeholder="igst" />
                        </th>
                        <input class="border-2 border-red-800 " placeholder="Cess" />
                        <th>{{ Cess }}</th>
                    </tr>
                    <tr class="flex flex-col justify-between ">
                        <th>
                            <h1>Total Tax ₹</h1>
                        </th>
                        <th>
                            <h1>Total (after tax ) ₹ {{ total }}</h1>
                        </th>
                        <th>
                            <h1>Grand Total ₹ </h1>
                        </th>
                    </tr>
                </table>
            </section>
        </section>
    </div>
</template>
<script>
export default {
    data() {
        return {
            taxableAmount: "",
            cgstAmount: "",
            sgstAmount: "",
            Cess: "",
            total: "",
        }
    }
}
</script>
<style>
.no {
    width: 10px;
}
#no {
    width: 10px;
}
</style>