<!-- 
Kelompok 5
Voucher
Nama : 1. Aditiya Budi Listianto (1402022002)
       2. Ahmad Bahauddin Alghozi (1402022005) 
-->

<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="mr40 mt20">
                    <router-link to="/list-voucher">
                        <img src="../../assets/icons/back.svg">
                    </router-link>
                </div>
                <div>
                    <h1 class="m0">Add Voucher</h1>
                    <p class="mt5 mb20 tc-green">Make your customers shop using vouchers</p>
                </div>
            </div>
            <hr class="uline-grey">
            <div class="mt50 row">
                <div class="w20">
                    <label class="form-label">Voucher Image</label>
                </div>
                <div class="w80">
                    <div class="form-img">
                        <label for="image">
                            <img src="../../assets/icons/upload.svg" style="width: 90px; padding-left: 6px;">
                        </label>
                        <input type="file" id="image" accept="image/*" style="display: none;">
                    </div>
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Vocher Code</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Masukkan Kode Voucher" maxlength="6">
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Voucher Name</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Masukkan Nama Voucher" maxlength="20" minlength="5">
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Deskripsi</label>
                </div>
                <div class="w80">
                    <textarea name="Deskripsi" class="form-description" placeholder="Masukkan Deskripsi"></textarea>
                    <!-- <input
                    class="form-description" 
                    type="text"
                    placeholder="Masukkan Voucher Deskripsi"
                    maxlength="5000"> -->
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Type</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Pilih Type">
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Min. Transaction</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Masukkan Minimal Transaksi">
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Amount</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Masukkan Amount">
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Valid From</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Masukkan Tanggal">
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Valid Until</label>
                </div>
                <div class="w80">
                    <input class="form-text" type="text" placeholder="Masukkan Tanggal">
                </div>
            </div>
            <div class="flex mt30">
                <router-link to="/list-voucher">
                    <button class="bt-submit-green">Add Voucher</button>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'add-user',
    data() {
        return {
            link_img: '../../assets/icons/upload.svg'
        }
    }
}


</script>