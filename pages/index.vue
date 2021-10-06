<template>
  <div class="lg:pl-24 lg:pr-24 pt-4">
    <div class="text-center">
      <h1 class="blot-title">
        Jamstack Conf Talk
      </h1>
      <div class="py-8 px-8 mx-auto bg-white rounded-xl shadow-md space-y-2 sm:py-4 sm:flex sm:items-center sm:space-y-0 sm:space-x-6 md:py-4 md:flex md:items-center md:space-y-0 md:space-x-6">
        <nuxt-img
        provider="imgix"
        fit="crop"
          src="artsy/3.jpg"
          class="lg:w-3/5 md:w-1/3 w-full"
          sizes="sm:100vw md:33vw lg:60vw xl:60vw"
          width="600"
          height="334"
          :modifiers="{ ar: '1.8:1', auto: 'format' }"
        />
        <div class="text-center space-y-2">
          <div class="space-y-0.5">
            <p class="blog-description inline">Hello everyone. This is for a talk at the Jamstack conf lounge. We are focusing on optimizing images in the JAMSTACK.  Specifically, how to accelerate your pagespeed performance on Pagespeed Insights.  Our first focus is on the Largest Contentful Paint, which is one of the new Core Web Vitals released by Google.  We want to identify some methods to improve our LCP using Google Pagespeed Insights.  The LCP is often the hero image. On this site, the LCP is the image to the left of this text.  When running a test, you will notice a major issue with the size of this image.  Ensuring the proper sizing of your images is one of the basic fundamental methods for improving your Pagespeed Performance with your LCP image.  Next, we will want to focus on the format of this image.  Is it being served in a next-gen format for the browser?  We should expect an AVIF in Chrome, Webp in Firefox and some Safari, and then a jpg or png for other browsers. Finally, let's ensure you are using proper encoding for your images.</p>
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
          width="360"
          height="200"
          loading="lazy"
          sizes="sm:100vw md:50vw lg:33vw xl:33vw"
          :modifiers="{ ar: '1.8:1', auto: 'format'  }"
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
