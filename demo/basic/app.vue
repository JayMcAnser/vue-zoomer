<template>
  <div style="padding: 100px;">
    <div>
      zoomed: {{ zoomed }}
      <button @click="$refs.zoomer.zoomIn()">+</button>
      <button @click="$refs.zoomer.zoomOut()">-</button>
    </div>
    <v-zoomer
      ref="zoomer"
      style="width: 500px; height: 500px; border: solid 1px silver;"
      :max-scale="10"
      :zooming-elastic="false"
      :zoomed.sync="zoomed"
      @update:start="zoom('begin')"
      @update:end="zoom('end')"
      @update:zoomed="zoom('full')"
    >
      <img src="../assets/landscape-1.jpg" style="object-fit: contain; width: 100%; height: 100%;">
    </v-zoomer>
    <div>
      <ul>
        <li v-for="(message, index) in messages" :key="index">
          {{message}}
        </li>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      zoomed: false,
      messages: [
        'starting'
      ]
    }
  },
  methods: {
    zoom: function (msg) {
      this.messages.push(msg);
    }
  }
}
</script>
