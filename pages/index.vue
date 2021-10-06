<template>
  <div class="lg:pl-24 lg:pr-24 pt-4">
    <div class="text-center">
      <h1 class="blot-title">
        Jamstack Conf Talk
      </h1>
      <div class="py-8 px-8 mx-auto bg-white rounded-xl shadow-md space-y-2 sm:py-4 sm:flex sm:items-center sm:space-y-0 sm:space-x-6 md:py-4 md:flex md:items-center md:space-y-0 md:space-x-6">
        <nuxt-img
          provider="imgix"
          src="/artsy/3.jpg"
          fit="crop"
          class="lg:w-1/2 md:w-1/3 w-full"
          sizes="xl:100vw"
          :modifiers="{ ar: '1.8:1' }"
        />
        <div class="text-center space-y-2">
          <div class="space-y-0.5">
            <p class="blog-description inline">Hello everyone.</p>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-wrap">
      <div v-for="image in images" :key="image" v-bind:image="image" class="p-4 lg:w-1/3 md:w-1/2 sm:w-full">
        <nuxt-img
          provider="imgix"
          :src="image"
          fit="crop"
          sizes="sm:100vw md:50vw lg:33vw xl:33vw"
          :modifiers="{ ar: '1.8:1' }"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    images: [`/artsy/4.jpg`, `/artsy/5.jpg`, `/artsy/6.jpg`, `/artsy/7.jpg`, `/artsy/8.jpg`, `/artsy/9.jpg`, `/artsy/10.jpg`, `/artsy/11.jpg`, `/artsy/12.jpg`]
  })
}
</script>
