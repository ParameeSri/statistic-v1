<template>
  <div>
    <b-tabs pills card vertical nav-wrapper-class="col-2">
      <b-tab title="Overview" active>
        Overview
      </b-tab>
      <b-tab title="Account Profile">
        <AccountProfile></AccountProfile>
      </b-tab>
      <b-tab title="Statistic">
          Statistic
          <!-- <AccountProfile></AccountProfile> -->
      </b-tab>
      <b-tab title="Setup">
        <Setup></Setup>
      </b-tab>
    </b-tabs>
  </div>
</template>

<script>
import AccountProfile from '~/components/AccountProfile'
import Setup from '~/components/Setup'

export default {
  components: {
    AccountProfile,
    Setup
  },
  data () {
    return {

    }
  }
}
</script>

