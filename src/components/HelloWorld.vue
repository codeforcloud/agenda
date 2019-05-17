<template>
  <div class="hello">
    <h1>Welcome to Your Vue.js + TypeScript App</h1>
    <ul v-for="conference in conferencesData" v-bind:key="conference">
      <li>{{ conference.name }}</li>
      <li><a :href="conference.url">{{ conference.url }}</a></li>
      <ul>
        <li>{{ conference.date.start }}</li>
        <li>{{ conference.date.end }}</li>
      </ul>
      <li><a :href="conference.cfp.url">{{ conference.cfp.url }}</a></li>
      <li>{{ conference.cfp.date }}</li>
      <ul>
        <li>{{ conference.cfp.date.start }}</li>
        <li>{{ conference.cfp.date.end }}</li>
      </ul>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  public conferencesData = [
            {
            "name": "Toto",
            "url": "https://www.google.fr",
            "date": {
                "start": "2018",
                "end": "2018"
            },
            "cfp": {
                "url": "https://www.google.fr",
                "date": {
                    "start": "2018",
                    "end": "2018"
                }
            }
        },
        {
            "name": "Tata",
            "url": "https://www.google.fr",
            "date": {
                "start": "2018",
                "end": "2018"
            },
            "cfp": {
                "url": "https://www.google.fr",
                "date": {
                    "start": "2018",
                    "end": "2018"
                }
            }
        }
  ];
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
/* ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
} */
a {
  color: #42b983;
}
</style>
