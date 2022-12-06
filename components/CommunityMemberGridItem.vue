<template>
  <div class="pt-9 pb-5 w-1/4 lg:w-1/3 lg:flex lg:gap-x-8">
    <div class="flex w-16 lg:w-20 justify-end">
      <img
        :title="communityMemberType.imageAlt"
        :alt="communityMemberType.imageAlt"
        class="h-16 lg:h-20"
        :src="require(`~/assets/img/${communityMemberType.image}`)"
      />
    </div>
    <div class="mt-3 lg:mt-0">
      <h1 tabindex="2" class="community-cop-number satoshi-bold">
        {{ communityMemberType.count }}
      </h1>
      <h3 tabindex="2" class="community-cop-numb-metric">
        {{ communityMemberType.name }}
      </h3>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    communityMemberType: {
      type: Object,
      required: true,
    },
  },
}
</script>
