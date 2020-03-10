<template>
  <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group id="input-group-2" label="Adınız:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          required
          placeholder="Adınızı giriniz."
        >
        </b-form-input>
      </b-form-group>
      <b-form-group id="input-group-2" label="Soyadınız:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.surname"
          required
          placeholder="Soyadınızı giriniz."
        ></b-form-input>
      </b-form-group>
      <b-form-group id="input-group-2" label="Numaranız:" label-for="input-2">
        <b-form-input
          id="input-2"
          type="tel"
          v-model="form.phone"
          required
          placeholder="Numaranızı giriniz."
        ></b-form-input>
      </b-form-group>
      <b-form-group
        id="input-group-1"
        label="Eposta Adresiniz:"
        label-for="input-1"
        description="İletişim bilgileriniz başkalarıyla paylaşılmaz."
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          required
          placeholder="Eposta adresinizi giriniz."
        >
        </b-form-input>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: "",
        name: "",
        phone: null,
        surname: null
      },
      foods: [
        { text: "Select One", value: null },
        "Carrots",
        "Beans",
        "Tomatoes",
        "Corn"
      ],
      show: true
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.food = null;
      this.form.checked = [];
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    }
  }
};
</script>
<style lang="less" scoped>
input {
  background-color: transparent !important;
  color: #ffc107 !important;
}
</style>
