<template lang="html">
  <div class="">
    <div class="h-64 flex flex-col justify-between border border-grey-lighter shadow">
      <!-- TODO: Relative Hover => Book Details (description, tages, related) -->
      <div class="h-48 text-xs p-2">
        <h4 class="text-xs text-grey-dark font-medium mb-2">
          #{{ book.title }}
        </h4>
        <router-link
          :to="{ name: 'book', params: { id: book._id } }"
          class="text-base text-grey-dark font-medium no-underline hover:underline"
          >{{ book.title }}
        </router-link>
      </div>
      <div class="flex flex-row justify-between p-2 bg-grey-lightest border-t border-grey-lighter">
        <h5 class="text-xs text-grey-darker font-medium">
          book.author
        </h5>
        <p class="text-xs text-grey-dark font-medium">
          {{ book.isbn }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['book']
}
</script>

<style lang="css">
</style>
