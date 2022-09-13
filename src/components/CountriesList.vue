<template>
  <!-- Bootstrap container wrapper div -->
  <div class="container">
    <!-- Bootstrap row wrapper div -->
    <div class="row">
      <!-- Countries List (Bootstrap column) -->
      <div class="col-5" style="max-height: 90vh; overflow: scroll">
        <div class="list-group">
          <a
            v-for="country in countries"
            class="list-group-item list-group-item-action"
            :href=idUrl(country)
          >
            <img src="https://flagpedia.net/data/flags/icon/72x54/aw.png" />
            <p>{{country.name.common}}</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import countries from "../countries.json";
export default {
  data() {
    return {
      countries: countries,
    };
  },
  methods: {
    idUrl(countrie){
        return countrie.name.common
    }
  }
};
</script>
