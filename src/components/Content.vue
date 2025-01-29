<template>
    <div class="w-full max-w-9/10 mx-auto py-5">
        <img class="w-full rounded-md" src="./img-slide/banner1.gif" />
    </div>
    <div class="bg-gray-800 w-full max-w-9/10 mx-auto py-5 rounded-md ">
        <p class=" text-center text-white font-khmer text-wrap ">សូម​ស្វាគមន៍​មក​កាន់​គេហទំព័រ Movie4kh ទស្សនា​រឿងភាគ​រឿងទោល​គ្រប់​ប្រភេទ​ដោយ​សេរី​និង​ឥតគិតថ្លៃ។</p>
    </div>
    <div class="bg-gray-800 w-full max-w-9/10 mx-auto py-2 mt-3 rounded-md">
        <p class=" text-base sm:text-lg md:text-xl text-white font-khmer font-bold ml-3">រឿងមានអ្នកទស្សនា ច្រើន​ប្រចាំ​សប្ភាហ៍</p>
    </div>
    <div class=" w-full max-w-9/10 mx-auto rounded-md grid-cols-5 gap-6 mt-3">
        <div class="grid grid-cols-2 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-6 ">
            <div v-for="(movie, index) in movies" :key="index" class="rounded-lg shadow-lg flex flex-col">
                <img :src="movie.image" :alt="movie.title" class="w-full h-auto" />
                <div class="p-2 ">
                    <h2 class="text-lg font-semibold  text-gray-800 text-wrap">{{ movie.title }}</h2>
                </div>
            </div>
        </div>
    </div>
    
</template>
  
  <script>
    export default {
  data() {
    return {
      movies: [
        { title: "Aku Tahu Kapan Kamu Mati", year: "2024",image: "./src/assets/img-content/PANDA-PLAN.jpg", type: "Movie" },
        { title: "Thaghut", year: "2024", image: "./src/assets/img-content/PANDA-PLAN.jpg", type: "Movie" },
        { title: "All of Us Are Dead", image: "./src/assets/img-content/PANDA-PLAN.jpg", type: "Series" },
        { title: "Pamali", year: "2023", image: "./src/assets/img-content/PANDA-PLAN.jpg", type: "Movie" },
        { title: "Operation Undead", year: "2024", image: "./src/assets/img-content/PANDA-PLAN.jpg", type: "Movie" },
        { title: "Operation Undead", year: "2024", image: "./src/assets/img-content/PANDA-PLAN.jpg", type: "Movie" },
      ]
    };
  }
};

  </script>
  
  <style scoped>
   .font-khmer {
    font-family: 'Khmer OS Battambang', sans-serif;
   }
  
  </style>
  