<template>
  <nav class="header ant-layout-header">
    <div class="headerContainer">
      <div class="logo">
        <img
          alt="logo"
          width=40
          height=40
          src="../assets/images/logo.svg"
        />
        <h1>
          HD UI Issue Helper
        </h1>
      </div>
      <div class="locale">
        <a-button size="small" @click="handleLocaleChange">
          {{lang === 'en' ? '中文' : 'English'}}
        </a-button>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  props: ['lang'],
  methods: {
    handleLocaleChange() {
      const lang = this.lang === 'en' ? 'zh' : 'en'
      this.$emit('change-lang', lang)
    }
  },
}
</script>
