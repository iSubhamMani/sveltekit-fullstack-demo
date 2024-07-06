<script lang="ts">
    import {PrivateKey} from "@bsv/sdk"

    let WIF: string
    let address: string

    function createKeys ( ) {
        const privKey = PrivateKey.fromRandom();
        WIF = privKey.toWif();
        console.log("Private Key WIF format is ", WIF);
        address = privKey.toAddress();
        console.log("Your bitcoin address is ", address);
    }
</script>

<section>
        <div class="flex justify-center my-8"><button class="bg-yellow-600 text-black font-bold py-3 px-4 rounded-md" on:click={createKeys}>Generate new wallet keys</button></div>
        <p class="my-6 text-lg text-center">Private key WIF format is <span class="font-bold">{WIF}</span></p>
        <p class="my-6 text-lg text-center">Your bitcoin address is <span class="font-bold">{address}</span></p>
</section>