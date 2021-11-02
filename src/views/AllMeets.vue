<template>
<div class="">
  <div class="all-meets flex flex-col justify-around items-center gap-16">
      <div class="flex flex-col-reverse sm:flex-row justify-between items-center mx-auto w-5/6 md:w-2/3 xl:w-1/2 pt-16 gap-4">
        <h1 class="font-bold text-center sm:text-left text-4xl text-gray-300">Data Semua Rapat</h1>
        <a href="/" class="main-button red-button rounded px-12 py-2 text-gray-300 font-medium bg-gradient-to-b from-red-600 to-red-800">Keluar</a>
      </div>
      <div class="content w-5/6 md:w-2/3 xl:w-1/2">
        <div class="toolbar w-full flex justify-center sm:justify-between flex-row-reverse">
          <div class="search-panel">
            <form action="" class="w-full flex flex-row justify-center sm:justify-end items-center gap-4">
              <label for="search" class="text-gray-200 w-full">Pencarian :</label>
              <input type="search" class="search-input bg-transparent border border-gray-600 px-4 py-2 w-full rounded text-gray-400 placeholder-gray-400 placeholder-opacity-50 text-sm">
            </form>
          </div>
        </div>
        <div class="meet-lists">
          <transition-group name="slide-up">
            <div v-for="meet in meets" :key=meet.id class="meet-card rounded-lg py-4 px-8 gap-4 my-8 flex flex-col flex-nowrap text-gray-300">
              <div class="mc-top flex justify-between border-b border-green-900 pb-4">
                <p class="font-medium">ID Rapat : {{ meet.id }}</p>
                <p class="badge bg-green-600 text-xs text-gray-300 rounded-full py-1 px-4">{{ meet.status }}</p>
              </div>
              <div class="mc-content flex flex-col gap-2">
                <div class="flex gap-4">
                  <h4 class="font-medium text-left w-5/12 lg:w-1/4">Subjek Rapat</h4>
                  <p class="w-7/12 lg:w-3/4 text-left">: {{ meet.subject }}</p>
                </div>
                <div class="flex gap-4">
                  <h4 class="font-medium text-left w-5/12 lg:w-1/4">Tipe</h4>
                  <p class="w-7/12 lg:w-3/4 text-left">: {{ meet.type }}</p>
                </div>
                <div class="flex gap-4">
                  <h4 class="font-medium text-left w-5/12 lg:w-1/4">Penyelenggara</h4>
                  <p class="w-7/12 lg:w-3/4 text-left">: {{ meet.organizer }} ({{ meet.organizerMail }})</p>
                </div>
                <div class="flex gap-4">
                  <h4 class="font-medium text-left w-5/12 lg:w-1/4">Berlangsung</h4>
                  <p class="w-7/12 lg:w-3/4 text-left">: {{ meet.progress }}</p>
                </div>
              </div>
              <div class="mc-bottom flex flex-row justify-end border-t border-green-900 pt-4 text-xs gap-4">
                <a href="/detail-rapat" class="mini-button rounded-lg py-1 px-4 border-green-900 text-green-500 border-2">Detail</a>
                <a href="" class="mini-button rounded-lg py-1 px-4 bg-gradient-to-b from-green-600 to-green-900">Gabung</a>
              </div>
            </div>
          </transition-group>
        </div>
      </div>
      <div class="footer w-5/6 md:w-2/3 xl:w-1/2 text-center sm:text-left text-gray-300 pb-16">©2021 Kejaksaan Agung Republik Indonesia</div>
  </div>
</div>
</template>

<script>
export default {
  name: 'AllMeets',
  data() {
    return {
      meets: [
        {
          id: 123456,
          status: 'berlangsung',
          subject: 'Tes Meeting',
          type: 'Rapat Reguler',
          organizer: 'Yadi Rudiyansyah',
          organizerMail: 'yadi@jumpa.id',
          progress: '02:08'
        },
        {
          id: 234567,
          status: 'berlangsung',
          subject: 'Meeting',
          type: 'Reguler',
          organizer: 'Andika',
          organizerMail: 'andika@mail.ex',
          progress: '25:59'
        },
        {
          id: 345678,
          status: 'berlangsung',
          subject: 'Meeting',
          type: 'Reguler',
          organizer: 'contoh',
          organizerMail: 'andika@mail.ex',
          progress: '25:59'
        },
      ]
    }
  }
}
</script>

<style lang="sass">
.meet-lists
  padding: 0 1%
  @media screen and (min-width: 640px)
    padding: 0 10%
.main-button, .badge
  height: min-content
.meet-card
  background-color: #03303699
.search-input
  min-width: 12.5rem
</style>