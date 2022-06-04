<template>
  <div>
    <Teleport  to="#modal">
      <div class="modal" v-if="open">
        <div class="modal__content">
          <slot />

          <a href="#" @click.prevent="$emit('yes')">Yes</a>
          <a href="#" @click.prevent="$emit('no')">No</a>
        </div>
      </div>
    </Teleport >
  </div>
</template>

<script>
export default {
  props: {
    open: {
      required: true,
      type: Boolean
    }
  }
}
</script>