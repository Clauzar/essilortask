<template>
  <div class="bod">
    <h1>Contact</h1>
 <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group id="exampleInputGroup1"
                    label="Email address:"
                    label-for="exampleInput1"
                    description="Please Provide your company email address to allow us to route to your inquiry to the right contact">
        <b-form-input id="exampleInput1"
                      type="email"
                      v-model="form.email"
                      required
                      placeholder="Enter email"
                      >
        </b-form-input>
      </b-form-group>
      <b-form-group id="fname"
                    label="First Name:"
                    label-for="fname">
        <b-form-input id="fname"
                      type="text"
                      v-model="form.name"
                      required
                      placeholder="Enter name">
        </b-form-input>
      </b-form-group>
      <b-form-group id="lname"
                    label="Last Name:"
                    label-for="lname">
        <b-form-select id="lname"
                      :options="foods"
                      required
                      v-model="form.food">
        </b-form-select>
      </b-form-group>
      Job Role:
      <b-form-select v-model="selected" :options="options" class="mb-3" />

      <b-form-group id="tel"
                    label="Telephone:"
                    label-for="tel">
        <b-form-select id="tel"
                      :options="foods"
                      required
                      v-model="form.food">
        </b-form-select>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
  </div>
  
</template>

<script>
export default {
  data () {
    return {
      selected: null,
      options: [
        { value: null, text: 'Please select an option' },
        { value: 'a', text: '1' },
        { value: 'b', text: '2' },
      ],
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots', 'Beans', 'Tomatoes', 'Corn'
      ],
      show: true
    }
  },
  methods: {
    onSubmit (evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset (evt) {
      evt.preventDefault();
      /* Reset our form values */
      this.form.email = '';
      this.form.name = '';
      this.form.food = null;
      this.form.checked = [];
      /* Trick to reset/clear native browser form validation state */
      this.show = false;
      this.$nextTick(() => { this.show = true });
    }
  }
}
</script>

<style scoped>

</style>

    