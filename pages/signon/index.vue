<template>
  <b-container class="bv-example-row bv-example-row-flex-cols">
    <b-row style="margin-top:5cm">
        <b-col align-self="start"></b-col>
        <b-col align-self="center">
          <b-card border-variant="secondary"
            header="Login"
            header-bg-variant="secondary"
            header-text-variant="white"
            align="center">
              <b-form-group label="Username" label-for="exampleInput1">
                <b-form-input id="exampleInput1" type="text" v-model="form.username" required placeholder="Username"></b-form-input>
              </b-form-group>
              <b-form-group label="Password" label-for="exampleInput2">
                <b-form-input id="exampleInput2" type="password" v-model="form.password" required placeholder="Password">
              </b-form-input>
              </b-form-group>
              <b-button type="submit" variant="primary" @click="doAuthen">Submit</b-button>
              <b-button type="button" variant="warning">Register</b-button>
          </b-card>
        </b-col>
        <b-col align-self="end"></b-col>
    </b-row>
  </b-container>
</template>


<script>
export default {
  data () {
    return {
      form: {
        // email: '',
        username: '',
        password: ''
        // food: null,
        // checked: []
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots', 'Beans', 'Tomatoes', 'Corn'
      ],
      show: true
    }
  },
  methods: {
    doAuthen () {
      if (this.form.username === 'paramee') {
        this.$router.replace('/statistic')
      }
    },
    // onSubmit (evt) {
    //   evt.preventDefault()
    //   alert(JSON.stringify(this.form))
    // },
    // onReset (evt) {
    //   evt.preventDefault()
    //   /* Reset our form values */
    //   this.form.email = ''
    //   this.form.username = ''
    //   this.form.food = null
    //   this.form.checked = []
    //   /* Trick to reset/clear native browser form validation state */
    //   this.show = false
    //   this.$nextTick(() => { this.show = true })
    // }
  }
}
</script>