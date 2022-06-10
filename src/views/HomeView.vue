<template>
  <main class="mb-16 mt-2 bg-gray-300 m-auto p-4">
    <div>
      <h1 class="text-2xl text-center uppercase">Heading</h1>
      <p class="p-4">
        <b>Lorem ipsum</b> dolor sit amet, consectetur adipiscing elit, sed do
        eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
        minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip
        ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
        voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
        sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>
      <img class="m-auto" src="../assets/test_img.jpg" alt="test image" />
      <p class="p-4">
        <b>Lorem ipsum</b> dolor sit amet, consectetur adipiscing elit, sed do
        eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
        minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip
        ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
        voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
        sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>
      <div
        class="flex-col rounded-md card m-auto w-64 h-64 pb-8 bg-slate-100 shadow-xl divide-y-4 > * + *"
      >
        <h3
          class="text-center p-2 mt-6 text-lg uppercase font-bold text-slate-600"
        >
          This is a card
        </h3>
        <p class="p-2">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </p>
        <h3
          class="text-center p-2 mt-6 text-lg uppercase font-bold text-slate-600"
        >
          <a href="#" class="hover:text-slate-900">Click Here</a>
        </h3>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  width: 900px;
}
.card {
  position: relative;
  /* margin-bottom: 2rem; */
}
</style>
