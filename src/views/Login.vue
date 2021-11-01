<template>
	<div class="login flex flex-col md:flex-row justify-center gap-4 lg:gap-28 items-center h-full p-8">
		<transition name="slide-left" appear>
			<img src="/./img/col-6 vector.png" class="" alt="Login Page">
		</transition>
		<div class="flex flex-nowrap flex-col items-start">
			<transition-group name="slide-right" appear>
				<h1 v-if="contentActive" class="font-bold text-left text-4xl text-gray-300">Portal Stealth Meeting</h1>
				<p v-if="contentActive" class="font-normal text-left text-gray-500 text-base pt-4">Silahkan isi formulir di bawah ini?</p>
				<p v-if="contentActive" class="font-normal text-left text-gray-500 text-base">Pastikan NIP dan nomor PIN yang Anda masukkan benar</p>
				<form action="" class="flex flex-nowrap flex-col items-start w-full">
					<transition-group name="slide-right" appear>
						<label v-if="contentActive" for="nip" class="text-gray-400 font-medium pt-4 pb-1">NIP</label>
						<input v-if="contentActive" type="text" name="" id="" placeholder="Masukkan NIP Anda" class="bg-gray-900 px-4 py-3 w-full rounded text-gray-400 placeholder-gray-400 placeholder-opacity-50">
						<label v-if="contentActive" for="pin" class="text-gray-400 font-medium pt-4 pb-1">Nomor PIN</label>
						<input v-if="contentActive" type="text" name="" id="" placeholder="Masukkan Nomor PIN Anda" class="bg-gray-900 px-4 py-3 w-full rounded text-gray-400 placeholder-gray-400 placeholder-opacity-50">
						<a v-if="contentActive" href="" class="w-full text-right text-gray-400 pt-2">Lupa Pin?</a>
						<input v-if="contentActive" type="submit" value="Masuk" class="rounded px-12 py-3 mt-7 bg-gradient-to-b from-green-600 to-green-900 text-gray-200 font-medium">
					</transition-group>
				</form>
			</transition-group>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Login',
	data(){
		return {
			contentActive: false
		}
	},
	mounted(){
		this.contentActive = true
	}
}
</script>

<style lang="sass">
.login
	background: radial-gradient(ellipse, #064E3BBB, black 75%) no-repeat
	height: 100vh
	width: 100%
input[type=text]
	outline: none
input[type=submit]
	border: 1px solid black
	transition: all .25s ease
	&:hover
		box-shadow: #047857 5px 6px 0
</style>