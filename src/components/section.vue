<template>
  <div>
    <div class="row">
      <div class="col-md-6">
        <h2>Liste des apprenants</h2>
        <ul>
          <li v-for="apprenant in apprenants" :key="apprenant">
            {{apprenant}}
            <button
              class="btn btn-primary ml-3 mb-3"
              v-on:click="devFront(apprenant)"
            >frontend</button>
            <button class="btn btn-secondary ml-3 mb-3" v-on:click="devBack(apprenant)">backend</button>
          </li>
        </ul>
      </div>
      <div class="col-md-6">
        <div class="row">
          <div class="col-md-6">
            <h2 v-if="backend.length > 0">Dev Backend</h2>
            <div>
              <p v-for:="item in backend">{{item}}</p>
            </div>
          </div>
          <div class="col-md-6">
            <h2 v-if="frontend.length > 0">Dev Frontend</h2>
            <div>
              <p v-for:="item in frontend">{{item}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Section",
  data: () => ({
    apprenants: [
      "claude",
      "joseph",
      "françois",
      "peniel",
      "camille",
      "osée",
      "dido",
      "thesy",
      "murduch",
    ],
    frontend: [],
    backend: [],
  }),
  methods: {
    devFront: function (apprenant) {
      this.frontend.push(apprenant);
    },
    devBack: function (apprenant) {
      this.backend.push(apprenant);
    },
  },
};
</script>