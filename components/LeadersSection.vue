<template>
  <div class="px-16 bg-white">
    <h1 tabindex="2" class="satoshi-black font-bold font-36px text-darkbrown">
      Leadership
    </h1>
    <ul id="leaderApp" class="pt-2.5 flex flex-wrap justify-center pb-4">
      <li
        v-for="leader in leaders"
        :key="leader['title']"
        class="w-full flex flex-col basis-full lg:basis-1/5 p-2"
      >
        <img
          :title="leader['image-alt']"
          :alt="leader['image-alt']"
          class="pb-2.5"
          :src="require(`~/assets/img/headshots/${leader['image']}`)"
        />
        <a
          tabindex="2"
          class="satoshi-bold underline"
          target="_blank"
          :href="leader['link']"
          >{{ leader['name'] }}</a
        >
        <h3 tabindex="2" class="font-medium text-medgrey">
          {{ leader['title'] }}
        </h3>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: {
    leaders: {
      type: Array,
      required: true,
    },
  },
}
</script>
