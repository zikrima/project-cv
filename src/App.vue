<template>
  <div>
    <h1>{{ namaLengkap }}</h1>
    <p>{{ biodata }}</p>

    <h2>Keterampilan & Kemampuan:</h2>
    <ul>
      <li v-for="keterampilan in keterampilanKemampuan" :key="keterampilan">{{ keterampilan }}</li>
    </ul>

    <h2>Pengalaman:</h2>
    <ul>
      <li v-for="pengalaman in pengalamanDimiliki" :key="pengalaman.title">
        <h3>{{ pengalaman.title }}</h3>
        <p>{{ pengalaman.deskripsi }}</p>
      </li>
    </ul>
  <div>
    <ButtonX></ButtonX>
  </div>

  </div>
</template>
<script>
import ButtonX from './components/Button1.vue'
</script>

<script setup>
const namaLengkap = 'Zikri Maarif';
const biodata = 'Saya adalah seorang mahasiswa yang sedang belajar tentang pengembangan web. Saya lahir pada tahun 2003, dan saat ini saya berumur 20 tahun';
const keterampilanKemampuan = ['HTML', 'CSS', 'JavaScript'];
const pengalamanDimiliki = [
  { title: 'Magang di Perusahaan X', deskripsi: 'Belajar dasar-dasar pengembangan web dan bekerja dalam proyek kecil.' },
  { title: 'Proyek Kuliah: Website Sederhana', deskripsi: 'Membuat website sederhana sebagai tugas kuliah.' }
];

</script>

