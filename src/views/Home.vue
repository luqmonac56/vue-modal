<template>
  <div class="home">
    <button @click="toggleModal = !toggleModal" class="px-6 py-3 font-sans font-bold text-white bg-red-400 rounded shadow-lg outline-none active:outline-none focus:outline-none hover:bg-red-300 ">click here</button>
    
    <div class="fixed inset-0 z-50 flex items-center justify-center overflow-x-hidden overflow-y-auto" v-if="toggleModal">
      <div class="relative w-auto max-w-2xl mx-auto ">
        <div class="flex flex-col w-full bg-white">
        <div class="text-2xl font-bold"><h3 class="capitalize">Hello from vue modal</h3></div>
          <span>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vero quisquam, ducimus distinctio hic magni excepturi repellat voluptate odit laborum molestiae non ipsam nihil perferendis quas perspiciatis alias, dolorem repudiandae explicabo minima blanditiis quod nisi natus officia illum! Natus, doloribus excepturi pariatur itaque, maiores ab ipsa incidunt distinctio mollitia libero repellat!</span>
         <button class="w-3/12 px-6 py-2 m-auto mt-1 mb-3 text-white bg-green-500 rounded shadow-2xl" @click="toggleModal = false"> close</button>
          
        </div>
      </div>
    </div>
            
    
    <div v-if="toggleModal" class="absolute inset-0 z-30 bg-black opacity-25" >    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  data() {
    return {
      toggleModal: false
    };
  },
}
</script>
