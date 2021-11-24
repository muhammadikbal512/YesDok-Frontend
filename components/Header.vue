<template>
  <div class="header-2">
    <nav class="py-2 md:py-4" style="background-color: #024768">
      <div class="container px-4 mx-auto md:flex md:items-center">
        <div class="flex justify-between items-center">
          <img src="~/assets/img/yesdok.png" width="150px;" />
          <button
            class="
              border border-solid border-gray-600
              px-3
              py-1
              rounded
              text-gray-600
              opacity-50
              hover:opacity-75
              md:hidden
            "
            id="navbar-toggle"
          >
            <fa icon="bars" />
          </button>
        </div>

        <div
          class="hidden md:flex flex-col md:flex-row md:ml-auto mt-3 md:mt-0"
          id="navbar-collapse"
        >
          <a
            href="#"
            class="p-2 lg:px-4 md:mx-2 text-white rounded bg-indigo-600"
            >BERANDA</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white
              rounded
              hover:bg-indigo-600
              transition-colors
              duration-300
            "
            >PERUSAHAAN</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white
              rounded
              hover:bg-indigo-600
              transition-colors
              duration-300
            "
            >UNDUH</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white
              rounded
              hover:bg-indigo-600
              transition-colors
              duration-300
            "
            >STORE</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white
              rounded
              hover:bg-indigo-600
              transition-colors
              duration-300
            "
            >TENTANG KAMI</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white
              rounded
              hover:bg-indigo-600
              transition-colors
              duration-300
            "
            >HUBUNGI KAMI</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white text-center
              border border-solid border-indigo-600
              rounded
              hover:bg-indigo-600 hover:text-white
              transition-colors
              duration-300
            "
            >Login</a
          >
          <a
            href="#"
            class="
              p-2
              lg:px-4
              md:mx-2
              text-white text-center
              border border-solid border-indigo-600
              rounded
              hover:bg-indigo-600 hover:text-white
              transition-colors
              duration-300
              mt-1
              md:mt-0 md:ml-1
            "
            >Signup</a
          >
        </div>
      </div>
    </nav>

    <div class="bg-indigo-100 py-6 md:py-12">
      <div class="container px-4 mx-auto">
        <div class="text-center max-w-2xl mx-auto flex">
          <h1 class="text-3xl md:text-4xl font-medium mb-2">
            BINGUNG ? TANYA DOKTER !
          </h1>
          <button
            class="bg-indigo-600 text-white py-2 px-6 rounded-full text-xl"
          >
            Mulai Konsultasi
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  created() {
    axios.get('https://jsonplaceholder.typicode.com/posts?userId=1')
    .then(response => {
      console.log(response)
    })
  }
}
</script>
