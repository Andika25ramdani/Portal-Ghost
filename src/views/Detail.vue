<template>
  <div class="all-meets flex flex-col justify-around items-center gap-16">
      <div class="flex flex-col-reverse sm:flex-row justify-between items-center mx-auto w-5/6 md:w-2/3 xl:w-1/2 pt-16 gap-4">
        <h1 class="font-bold text-center sm:text-left text-4xl text-gray-300">Detail Rapat</h1>
        <a href="/" class="main-button red-button rounded px-12 py-2 text-gray-300 font-medium bg-gradient-to-b from-red-600 to-red-800">Keluar</a>
      </div>
      <div class="content w-5/6 md:w-2/3 xl:w-1/2">
        <div class="toolbar w-full flex justify-center sm:justify-between flex-row">
					<a href="/semua-rapat" class="main-button mini-button rounded-lg py-1 px-4 border-gray-300 text-sm text-gray-300 border">Kembali</a>
        </div>
        <div class="meet-lists">
          <transition name="slide-up">
            <div class="meet-card rounded-lg p-12 flex flex-col gap-8 my-8 text-gray-300">
              <div class="mc-content grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="flex flex-col gap-1">
                  <h4 class="font-semibold text-left text-lg">ID Rapat : </h4>
                  <p class="text-left font-light">{{ id }}</p>
                </div>
                <div class="flex flex-col gap-1">
                  <h4 class="font-semibold text-left text-lg">Subjek Rapat : </h4>
                  <p class="text-left font-light">{{ subject }}</p>
                </div>
                <div class="flex flex-col gap-1">
                  <h4 class="font-semibold text-left text-lg">Tipe Rapat : </h4>
                  <p class="text-left font-light">{{ type }}</p>
                </div>
                <div class="flex flex-col gap-1">
                  <h4 class="font-semibold text-left text-lg">Penyelenggara : </h4>
                  <p class="text-left font-light">{{ organizer }}</p>
                </div>
                <div class="flex flex-col gap-1">
                  <h4 class="font-semibold text-left text-lg">Waktu Mulai : </h4>
                  <p class="text-left font-light">{{ startedAt }}</p>
                </div>
                <div class="flex flex-col gap-1">
                  <h4 class="font-semibold text-left text-lg">Durasi : </h4>
                  <p class="text-left font-light">{{ duration }}</p>
                </div>
              </div>
              <div class="mc-bottom flex flex-row justify-center pt-4 gap-4">
                <a href="" class="main-button green-button rounded-lg py-2 px-12 font-medium bg-gradient-to-b from-green-600 to-green-900">Gabung</a>
              </div>
            </div>
          </transition>
        </div>
      </div>
      <div class="footer w-5/6 md:w-2/3 xl:w-1/2 text-center sm:text-left text-gray-300 pb-16">©2021 Kejaksaan Agung Republik Indonesia</div>
  </div>
</template>

<script>
export default {
	name: 'Detail',
	data() {
		return {
			id: 123456,
			subject: 'Tes Meeting',
			type: 'Rapat Reguler',
			organizer: 'Yadi Rudiyansyah',
			startedAt: '2021-08-25 12:58',
			duration: '1 Jam'
		}
	}
}
</script>

<style lang="sass">

</style>