<template>
  <div class="container">
    <form
      class="contact_form"
      name="contact"
      method="POST"
      action="/thanks"
      data-netlify="true"
    >
      <input type="hidden" name="form-name" value="contact" />
      <div class="contact_item">
        <label for="name">お名前</label>
        <input type="text" id="name" name="name" autocomplete="name" required />
      </div>
      <div class="contact_item">
        <label for="email">メールアドレス</label>
        <input
          type="email"
          id="email"
          name="email"
          autocomplete="email"
          required
        />
      </div>
      <div class="contact_item">
        <label for="message">お問い合わせ内容</label>
        <textarea id="message" rows="12" name="message" required></textarea>
      </div>
      <div class="contact_item" v-show="false">
        <label for="message">スパムでない場合は空欄</label>
        <input type="text" name="bot-field" />
      </div>
      <div class="contact_submit">
        <button type="submit">送信</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>