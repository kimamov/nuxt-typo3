<template>
  <div class="t3-form-cta">
    <button type="reset">
      {{ i18n.resetButton }}
    </button>
    <button type="submit" :disabled="state.sending">
      <template v-if="state.sending">
        {{ i18n.sendingLabel }}
      </template>
      <template v-else emplate>
        {{ i18n.submitButton }}
      </template>
    </button>
  </div>
</template>
<script>
export default {
  name: 'T3FormCta',
  props: {
    state: {
      type: Object,
      required: true
    },
    i18n: {
      type: Object,
      required: true
    }
  }
}
</script>
