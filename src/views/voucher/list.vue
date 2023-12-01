<!-- 
Kelompok 5
Voucher
Nama : 1. Aditiya Budi Listianto (1402022002)
       2. Ahmad Bahauddin Alghozi (1402022005) 
-->

<template>
    <div>
        <Menu />
        <div class="container">
            <h1 class="m0">Voucher</h1>
            <div class="row">
                <div class="col">
                    <p class="mt5 mb20 tc-green">Manage user data here</p>
                </div>
                <div class="col flex">
                    <router-link to="/add-voucher">
                        <button class="bt-green">+ Add</button>
                    </router-link>
                </div>
            </div>
            <div class="row bg-blue mt10 p10">
                <div class="col">
                    <input class="search-field" type="text" id="deskripsi" placeholder="Tambah deskripsi..." />
                </div>
                <div class="col flex">
                    <button class="bt-blue">Filter</button>
                </div>
            </div>
            <div class="mt50">
                <table>
                    <thead>
                        <tr>
                            <th>VOUCHER CODE</th>
                            <th>VOUCHER NAME</th>
                            <th>VALID<br>FROM</th>
                            <th>VALID<br>UNTIL</th>
                            <th>VOUCHER<br>STATUS</th>
                            <th></th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="item of list_voucher" :key="item.id">
                            <td class="center">{{ item.voucher_code }}</td>
                            <td class="center">{{ item.voucher_name }}</td>
                            <td class="center"><label class="label-green">{{ item.valid_from }}</label></td>
                            <td class="center"><label class="label-green">{{ item.valid_until }}</label></td>
                            <td class="center">
                                <div v-if="item.voucher_status === 1">
                                    <label class="label-green">Active</label>
                                </div>
                                <div v-if="item.voucher_status === 2">
                                    <label class="label-red">Inactive</label>
                                </div>
                            </td>
                            <td class="center">
                                <div class="mt5">
                                    <router-link to="/edit-voucher">
                                        <img src="../../assets/icons/edit.svg">
                                    </router-link>
                                </div>
                                <div class="mt5">
                                    <router-link to="/detail-voucher">
                                        <img src="../../assets/icons/detail.svg">
                                    </router-link>
                                </div>
                                <div class="mt5">
                                    <img src="../../assets/icons/delete.svg">
                                </div>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
import Menu from "../../components/menu.vue"

export default {
    name: 'list-voucher',
    components: {
        Menu
    },
    data() {
        return {
            list_voucher: [
                {
                    id: "1",
                    voucher_code: "CERIA1",
                    voucher_name: "PROMO",
                    valid_from: "01-06-2021",
                    valid_until: "03-06-2021",
                    voucher_status: 1
                }
            ]

        }
    }
}
</script>